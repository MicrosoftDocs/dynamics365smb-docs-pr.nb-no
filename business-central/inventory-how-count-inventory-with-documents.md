---
title: Telle og justere lagerbeholdningen
description: Beskriver hvordan du skal telle fysisk lager og bruke lagerdokumenter til å justere lagerbeholdning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 04/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="count-and-adjust-inventory-using-documents"></a>Telle og justere lagerbeholdning ved hjelp av dokumenter

Du kan utføre en vareopptelling ved hjelp av dokumentene for vareopptellingordre og registrering for vareopptelling. Siden **Vareopptellingsordre** brukes til å organisere hele lagertellingsprosjektet, for eksempel ett per lokasjon. Bruk siden **Registrering for vareopptelling** til å registrere og formidle det faktiske antallet varer. Du kan opprette flere registreringer for én ordre, for eksempel for å fordele grupper med varer til ulike ansatte.

Du kan skrive ut rapporten **Registrering for vareopptelling** fra hver registrering, og den inneholder tomme felter for antall der du kan angi den opptalte lagerbeholdningen. Når du er ferdig med å telle og antallene er angitt på siden **Registrering for vareopptelling**, velger du **Fullfør**-handlingen. Denne handlingen overfører antallet i de relaterte linjene på siden **Vareopptellingsordre**. [!INCLUDE [prod_short](includes/prod_short.md)]sikrer at du ikke kan registrere en vareopptelling to ganger.  

> [!NOTE]
> Bruk av dokumenter til å utføre en vareopptelling gir mer kontroll og støtter distribusjon av opptellingen til flere ansatte. Du kan også bruke kladder til å utføre aktiviteten, som sidene **Vareopptellingskladder** og **Lagervareopptellingskladd**. Du kan få mer informasjon ved å gå til [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md). Denne artikkelen beskriver hvordan du bruker dokumenter til å utføre en vareopptelling.
>
> Hvis du bruker soner på lageret, kan du ikke bruke vare opptellingsordrer. I stedet kan du bruke siden **Lagervareopptellingskladd** til å telle lagerpostene før du synkroniserer dem med varepostene.

Telling av beholdningen ved hjelp av dokumenter består av følgende generelle trinn:

1. Opprette en vareopptellingsordre med forventede antall forhåndsutfylt.
2. Generere én eller flere vareopptellingsregistreringer fra ordren.
3. Angi opptalt vareantall på registreringene, som registrert på utskrifter for eksempel, og sette den til **Fullført**.
4. Fyll ut og bokfør vareopptellingsordren.

## <a name="to-create-a-physical-inventory-order"></a>Slik opprettes en vareopptellingsordre

En vareopptellingsordre er et fullstendig dokument som består av et ordrehode for vareopptelling og ordrelinjer. Informasjonen i et vareopptellingshode beskriver hvordan du utfører vareopptellingen. Ordrelinjene inneholder opplysninger om varene og plasseringen.

Hvis du vil opprette vareopptellingsordrelinjer, bruker du vanligvis handlingen **Beregn linjer** til å legge til gjeldende beholdning som linjer i ordren. Du kan også bruke handlingen **Kopier fra dokument** til å fylle ut linjene med innholdet til en annen åpen eller bokført vareopptellingsordre. Følgende fremgangsmåte viser hvordan du bruker handlingen **Beregn linjer**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut de obligatoriske feltene på hurtigfanen **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg Annet i Funksjoner-gruppen **i kategorien Handlinger**  **, og velg** deretter Beregn linjer. **·** **·**
5. Velg alternativer etter behov.
6. Angi filtre, for eksempel for å inkludere bare et delsett av varene som skal telles sammen med den første registreringen.

    > [!TIP]
    > Hvis du vil planlegge for flere ansatte for vareopptelling, kan du angi forskjellige filtre hver gang du bruker handlingen **Beregn linjer**, for å bare fylle ut ordren med delsettet av lagervarer som en bruker skal registrere. Når du deretter genererer flere vareopptellingsregistreringer for flere ansatte, kan du minimere risikoen for å telle varene to ganger. Hvis du vil vite mer, kan du gå til [Slik opprettes en vareopptellingsregistrering](#to-create-a-physical-inventory-recording).

7. Velg **OK**-knappen.

En linje for hver vare som finnes i den valgte lokasjonen, og per angitte filtre og alternativer, legges til i ordren. For varer som er definert for varesporing, merkes det av for **Bruk varesporing**, og opplysninger om forventet antall for serie- og partinumre er tilgjengelig ved å velge **Linjer** og deretter **Varesporingslinjer**. Hvis du vil vite mer, kan du gå til [Håndtering av varesporing ved telling av varelager](#handle-item-tracking-when-counting-inventory).

Du kan nå opprette én eller flere registreringer, som er instruksjoner til de ansatte som utfører den faktiske tellingen.  

> [!NOTE]
> Hvis du bruker pakkespesifikk sporing, kan du også bruke dokumenter til å telle og justere lagerbeholdningen med pakkenumre. For å komme i gang med å bruke denne funksjonen må du aktivere **Funksjonsoppdatering: Aktiver bruk av pakkesporing i fysiske lagerordrer** på siden **Funksjonsstyring**. Eksisterende vareopptellingsordrer oppdateres, men [!INCLUDE [prod_short](includes/prod_short.md)] kan imidlertid ikke fylle ut **Pakkesporingsnr.** . Du må opprette disse linjene på nytt ved hjelp av handlingen **Beregn linjer** på siden **Vareopptellingsordre**.
>
> Du kan angi pakkenummeret for varer der pakkesporing er nødvendig, på siden **Vareopptellingslinjer** . Velg **Fullfør** for å fullføre opptellingen.
>
> Når du har valgt **Fullfør** på siden **Vareopptellingsordre**, beregner [!INCLUDE [prod_short](includes/prod_short.md)] differanser med hensyn til pakken og andre varesporingsdetaljer og foretar positive eller negative justeringer.

## <a name="to-create-a-physical-inventory-recording"></a>Slik opprettes en vareopptellingsregistrering

For hver vareopptellingsordre kan du opprette én eller flere vareopptellingsregistreringsdokumenter der ansatte angir de opptalte antallene. Ansatte kan angi antall manuelt eller med en skanneenhet.

En registrering opprettes som standard for alle linjene i den relaterte vareopptellingsordren. For å unngå at to ansatte teller de samme varene hvis du distribuerer opptelling, fyller du gradvis ut vareopptellingsordren ved å angi filtre i den satsvise jobben **Beregn linjer**. Deretter oppretter du vareopptellingsregistreringen med **Bare linjer som ikke finnes i registreringer** avmerket. Denne innstillingen sørger for at hver nye registrering inneholder andre varer enn i andre registreringer.

For manuell opptelling kan du skrive rapporten **Registrering for vareopptelling**, som har en tom kolonne der lageransatte kan skrive de opptalte antallene. Når tellingen er fullført, angir du de registrerte antallene på siden **Registrering for vareopptelling**. Til slutt overføre du de registrerte antallene til den relaterte vareopptellingsordren ved å sette status til **Fullført**.

1. På siden Ordre **for fysisk opptelling som inneholder linjer for varene som skal telles i ett opptak, må du velge** handlingen **Lag ny registrering** .
1. Velg Annet i Funksjoner-gruppen **i kategorien Handlinger**  **, og velg** deretter Gjør nytt opptak **.** **·**
1. Velg alternativer, og angi filtre etter behov.
1. Velg **OK**-knappen.
1. For hvert sett med varer som skal telles, last varene på den relaterte vareopptellingsordren, og gjenta trinn 1 til 3 med **Bare linjer som ikke finnes i registreringer** avmerket.
1. Velg Ordre i **kategorien Relatert**, og velg deretter handlingen **Opptak** for å åpne siden Oversikt over registrering **av** fysisk inventar **.** 
1. Åpne den aktuelle registreringen.
1. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
1. For varer som bruker varesporing, opprett en ekstra linje for hver parti- eller serienummerkode ved å velge handlingen **Funksjon**, og klikk deretter på **Kopier linjen**-handlingen. Hvis du vil vite mer, kan du gå til [Håndtering av varesporing ved telling av varelager](#handle-item-tracking-when-counting-inventory).  
1. Velg **Skriv ut**-handlingen for å forberede det fysiske dokumentet som de ansatte skal bruke til å notere antallene de teller.

## <a name="to-finish-a-physical-inventory-recording"></a>Slik avsluttes vareopptellingsregistrering

Når de ansatte har talt antallene, registrerer du antallene i [!INCLUDE [prod_short](includes/prod_short.md)].

1. Fra siden **Liste over registreringer for vareopptelling** velger du vareopptellingsregistreringen som du vil fullføre, og velg deretter **Rediger**-handlingen.
2. På hurtigfanen **Linjer** fyller du ut det faktisk opptalte antallet i feltet **Antall** for hver linje.
3. For varer med serie- eller partinumre (boksen **Bruk varesporing** er avmerket), angi de opptalte antallene på linjene for henholdsvis varens serie- og partinumre. Hvis du vil vite mer, kan du gå til [Håndtering av varesporing ved telling av varelager](#handle-item-tracking-when-counting-inventory).
4. Merk av for **Registrert** for hver linje.
5. Når du har angitt alle data for registrering av en vareopptelling, velger du **Fullfør**-handlingen. Vær oppmerksom på at alle linjene må ha **Registrert**-alternativet valgt.

    > [!NOTE]
    > Når du har fullført en vareopptellingsregistrering, overføres hver linje til linjen på den relaterte vareopptellingsordre som samsvarer nøyaktig med linjen. For å samsvare må verdiene i feltene **Varenr.**, **Variantkode**, **Lokasjonskode** og **Hyllekode** være like på registreringen og ordrelinjene.>
    > 
    > Hvis det ikke finnes noen tilsvarende vareopptellingsordrelinje, og hvis det er merket av for **Tillat registrering uten ordre**, blir en ny linje lagt til automatisk, og det merkes av for **Registrert uten ordre** på den relaterte vareopptellingsordrelinjen. Ellers vises det en feilmelding, og prosessen avbrytes. Hvis mer enn én vareopptellingsregistreringslinje samsvarer med en vareopptellingsordrelinje, vises en melding, og prosessen avbrytes. Hvis to identiske vareopptellingslinjer av én eller annen grunn havner i vareopptellingsordren, kan du bruke en handling for å løse problemet. Hvis du vil ha mer informasjon, kan du gå til [Slik finner du duplikate vareopptellingsordrelinjer](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Slik fullføres en vareopptellingsordre

Når du er ferdig med et opptak av **vareopptellingen, oppdateres feltet Ant.opptaker (lagerenhet)** i den relaterte ordren for fysisk opptelling med de opptalte (innspilte) verdiene, og det er merket av for **På opptakslinjer** . Hvis et opptalt antall er forskjellig fra forventet antall, viser feltene **Ordreantall (grunntall)**  og **Neg antall (basis)**  forskjellen.

For tilgang til forventet antall og eventuelle registrerte avvik for varer som har varesporing, kan du velge handlingen **Linjer** og deretter velge handlingen **Varesporingslinjer** for å velge ulike visninger for serie- og partinumre i vareopptellingen.

Du kan også velge handlingen **Differanse for vareopptellingsordre** for å vise eventuelle differanser mellom det forventede antallet og det opptalte antallet.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Slik finner du duplikate vareopptellingsordrelinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Åpne vareopptellingsordren du vil vise dupliserte linjer for.
1. Velg **Annet i kategorien Relatert**, og velg **deretter Vis dupliserte linjer**. **·**

Dupliserte vareopptellingsordrelinjer vises, slik at du kan slette dem og bare beholde én linje med et unikt sett med verdier i feltene **Varenr.**, **Variantkode**, **Lokasjonskode** og **Hyllekode**.

### <a name="to-post-a-physical-inventory-order"></a>Slik bokføres en vareopptellingsordre

Når du har fullført en vareopptellingsordre og endret statusen til **Fullført**, kan du bokføre den. Du kan bare angi status for en vareopptellingsordre til **Fullført** under følgende betingelser:

- Alle relaterte vareopptellingsregistreringer har statusen **Fullført**.
- Hver vareopptellingsordrelinje er talt opp av minst én registering for vareopptelling.
- Boksene **På registreringslinjer** og **Antall forventet (beregnet)** er merket av for alle vareopptellingsordrelinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Velg vareopptellingsordren som skal fullføres, og velg deretter **Rediger**-handlingen.

    På siden **Vareopptellingsordre** vises antallet som er registrert i feltet **Antall registrert (lagerenhet)**.
3. Velg handlingen **Fullfør**.

    Verdien i **Status**-feltet er **Fullført**. Du kan nå bare endre rekkefølgen ved å velge handlingen **Åpne på nytt**.
4. Hvis du vil bokføre ordren, velger du **Bokfør** og deretter **OK**.

    Varepostene oppdateres sammen med eventuelle tilknyttede varesporingspostene.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### <a name="to-view-posted-physical-inventory-orders"></a>Slik viser du bokførte vareopptellingsordrer

Etter bokføring slettes vareopptellingsordren, og du kan vise og evaluere dokumentet som en bokført vareopptellingsordre. Den bokførte ordren inkluderer vareopptellingsregistreringer og eventuelle merknader som er opprettet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ordrer for bokført vareopptelling** og velg den relaterte koblingen.
2. På siden **Ordrer for bokført vareopptelling** velger du den bokførte vareopptellingsordren som du vil vise, og velg deretter handlingen **Vis**.
3. Velg Ordre i **kategorien Relatert**, og velg **deretter handlingen Opptak** for å vise en liste over relaterte registreringer av fysisk **lager.**   

## <a name="handle-item-tracking-when-counting-inventory"></a>Håndtering av varesporing ved telling av varelager

Varesporing er relatert til serie- eller partinumrene som er tilordnet til varer. Når du teller en vare som er lagret i lageret som for eksempel 10 ulike partinumre, må den ansatte kunne registrere hvilke og hvor mange enheter av hvert partinummer som er på lager. Du kan finne ut mer ved å gå til [Arbeid med serie- og partinumre](inventory-how-work-item-tracking.md).

Boksen for **Bruk varesporing** på vareopptellingsordrelinjer velges automatisk hvis en varesporingskode er definert for en vare. Du kan også velge eller fjerne den manuelt.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Eksempel: Forberede en registrering for vareopptelling for en varesporet vare

Vurder en vareopptellingen for Vare A, som er lagret i lageret som ti ulike serienumre.

1. På registreringslinjen for varen merker du av for **Bruk varesporing**.
2. Velg **Serienr.**-feltet, velg det første serienummeret som finnes i beholdningen for varen, og velger deretter **OK**-knappen.

    Kopier linjen for den første varesporede varen for å sette inn flere linjer som svarer til antall serienumre som er lagret i lageret.

3. Velg **Funksjoner**-handlingen og deretter **Kopier linje**.
4. På siden **Kopier postlinje for vareopptelling** skriver du inn **9** i feltet **Antall eksemplarer**, og velg deretter **OK**-knappen.
5. På den første linjen velger du feltet **Serienr.** og deretter det neste serienummeret for varen.
6. Gjenta trinn 5 for de resterende åtte serienumrene. Pass på at du ikke velger det samme nummeret to ganger.
7. Velg **Skriv ut**-handlingen for å forberede utskriften som ansatte skal bruke til å notere det opptalte antallet varer og serie-/partinumre.

Legg merke til at rapporten **Registrering for vareopptelling** inneholder ti linjer for vare A, én for hver serienummer.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Eksempel – Registrere og bokføre talte partinummerforskjeller

En partisporet vare lagres i lageret med "PARTI"-nummerserier.

**Forventet beholdning**:

|Partinr.|Antall|
|-|-|
|PARTI1001|80|
|PARTI1003|30|
|PARTI1006|10|
|Sum|120|

**Registrert antall**:

|Partinr.|Antall|
|-|-|
|PARTI1001|80|
|PARTI0002|12|
|PARTI1003|20|
|PARTI1006|10|
|Sum|112|

**Antall som skal bokføres**:

|Partinr.|Forventet antall|Registrert antall|Antall som skal bokføres|
|-|-|-|-|
|PARTI1001|80|80|0|
|PARTI1002|0|12|+12|
|PARTI1003|30|20|-10|
|PARTI1006|10|0|-10|
|Sum|120|112|-8|

På siden **Vareopptellingsordre** inneholder feltet **Negativt antall (lagerenhet)** **8**. For ordrelinjen viser siden **Liste over varesporinger for vareopptelling** de positive eller negative antallene for hvert partinummer.

## <a name="inventory-documents"></a>Lagerdokumenter

Følgende dokumenttyper er nyttige når du skal håndtere lageret:

* Bruk **Lagermottak** til å registrere positive justeringer av varer basert på kvalitet, antall og kostnad.
* Bruk **Lagerleveringer** til å skrive av manglende eller skadde varer.

Du kan skrive ut disse dokumentene når som helst, frigi og åpne dem på nytt og tilordne vanlige verdier som dimensjoner i hodet. Hvis du vil skrive ut dokumentene på nytt etter at de er bokført, kan du bruke sidene **Bokført lagermottak** og **Bokført lagerlevering**.

> [!NOTE]
> Før du kan bruke disse dokumentene, må du angi en nummerserie for å opprette ID-ene. For mer informasjon, gå til [Definere nummerering for lagerdokumenter](#to-set-up-numbering-for-inventory-documents).

### <a name="to-set-up-numbering-for-inventory-documents"></a>Definere nummerering for lagerdokumenter

Følgende fremgangsmåte viser hvordan du definerer nummerering for lagerdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.
2. I hurtigfanen **Nummerering** angir du følgende nummerserien for dokumenter i følgende felt:

   - **Invt. Mottaksnr.**  
   - **Skrevet Invt. Mottaksnr.**  
   - **Invt. Forsendelsesnr.**  
   - **Skrevet Invt. Forsendelsesnr.**  

### <a name="to-create-and-post-an-inventory-document"></a>Opprette og bokføre et lagerdokument

Følgende fremgangsmåte viser hvordan du oppretter, skriver ut og bokfører et lagermottak. Trinnene er de samme for lagerleveringer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2. I overskriften til **Invt. Mottakssiden**, velg lokasjonen **i Lokasjonskode-feltet**, og fyll deretter ut de resterende feltene etter behov.
3. I hurtigfanen **Linjer** velger du lagervaren i feltet **Vare**. I feltet **Antall** angir du hvor mange varer som skal legges til.
4. Slik skriver du ut en **lagermottaksrapport** fra lagerbygningen **: Mottaksside**, velger du handlingen **Skriv ut** .

Følgende funksjoner er tilgjengelige på **Invt. Kvitteringsside** :

- Velg handlingene **Frigi** eller **Åpne på nytt** for å angi statusen for neste behandlingsfase.  
- Velge handlingen **Bokfør** for å bokføre lagermottaket, eller velg **Bokfør og skriv ut** for å bokføre mottaket og skrive ut testrapporten.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="printing-inventory-documents"></a>Skrive ut lagerdokumenter

Du kan angi rapportene som skal skrives ut i forskjellige faser, ved å velge ett av følgende alternativer i feltet **Bruk** på siden **Rapportvalg – beholdning**:

* Beholdningsmottak
* Lagerlevering
* Bokført beholdningsmottak
* Bokført lagerlevering

> [!NOTE]
> De tilgjengelige rapportene kan variere avhengig av lokaliseringen for landet/området. Basisprogrammet inkluderer ikke oppsett.

## <a name="see-also"></a>Se også

[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)    
[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)    
[Lager](inventory-manage-inventory.md)    
[Oversikt over lagerstyring](design-details-warehouse-management.md)    
[Salg](sales-manage-sales.md)    
[Innkjøp](purchasing-manage-purchasing.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
