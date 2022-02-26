---
title: Telle og justere lager
description: Beskriver hvordan du skal telle fysisk lager og bruke lagerdokumenter til å justere lagerbeholdning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease, inventory
ms.search.forms: 5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 45001f05d2ddedcd254fafbd78f38e03cd87b93c
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115287"
---
# <a name="count-and-adjust-inventory-using-documents"></a>Telle og justere lagerbeholdning ved hjelp av dokumenter

Du kan utføre en vareopptelling ved hjelp av dokumentene for vareopptellingordre og registrering for vareopptelling. Siden **Vareopptellingsordre** brukes til å organisere hele lagertellingsprosjektet, for eksempel ett per lokasjon. Siden **Registrering for vareopptelling** brukes til å formidle og registrere det faktiske antallet varer. Du kan opprette flere registreringer for én ordre, for eksempel for å fordele grupper med varer til ulike ansatte.

Rapporten **Registrering for vareopptelling** kan skrives ut fra hver registrering og inneholder tomme felt for antall for å angi den opptalte lagerbeholdningen. Når en bruker er ferdig med å telle, og antallet angis på siden **Registrering for vareopptelling**, kan du velge **Fullfør**-handlingen. Dette overfører antallet i de relaterte linjene på siden **Vareopptellingsordre**. Funksjonalitet sikrer at ingen vareopptelling kan registreres to ganger.  

> [!NOTE]
> Bruk av dokumenter til å utføre en vareopptelling, gir mer kontroll og støtter distribusjon av opptellingen til flere ansatte. Du kan også utføre aktiviteten ved hjelp av kladder, som sidene **Vareopptellingskladder** og **Lagervareopptellingskladd**. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md) Denne artikkelen beskriver hvordan du utfører en vareopptelling ved hjelp av dokumenter.
>
> Hvis du bruker soner, kan du ikke bruke vare opptellingsordrer. I stedet kan du bruke siden **Lagervareopptellingskladd** til å telle lagerpostene før synkronisering med varepostene.

Telling av beholdningen ved hjelp av dokumenter består av følgende generelle trinn:

1. Opprette en vareopptellingsordre med forventede antall forhåndsutfylt.
2. Generere én eller flere vareopptellingsregistreringer fra ordren.
3. Angi opptalt vareantall på registreringene, som registrert på utskrifter for eksempel, og sette den til **Fullført**.
4. Fyll ut og bokfør vareopptellingsordren.

## <a name="to-create-a-physical-inventory-order"></a>Slik opprettes en vareopptellingsordre
En vareopptellingsordre er et fullstendig dokument som består av et ordrehode for vareopptelling og noen vareopptellingordrelinjer. Informasjonen i et vareopptellingshode beskriver hvordan du utfører vareopptellingen. Vareopptellingordrelinjer inneholder opplysninger om varene og plasseringen.

Hvis du vil opprette vareopptellingsordrelinjer, bruker du vanligvis funksjonen **Beregn linjer** for å gjenspeile gjeldende beholdning som linjer i ordren. Du kan også bruke funksjonen **Kopier fra dokument** til å fylle ut linjene med innholdet til en annen åpen eller bokført vareopptellingsordre. Følgende fremgangsmåte viser hvordan du bruker funksjonen **Beregn linjer**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut de obligatoriske feltene på hurtigfanen **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **Beregn linjer**-handlingen.
5. Velg alternativer etter behov.
6. Angi filtre, for eksempel for å inkludere bare et delsett av varene som skal telles sammen med den første registreringen.

    > [!TIP]
    > Hvis du vil planlegge for flere ansatte for vareopptelling, er det lurt å angi forskjellige filtre hver gang du bruker handlingen **Beregn linjer**, for å bare fylle ordren med delsettet av lagervarer som én bruker skal registrere. Når du deretter genererer flere vareopptellingsregistreringer for flere ansatte, kan du minimere risikoen for å telle varene to ganger. Hvis du vil ha mer informasjon, kan du se delen [Slik opprettes en vareopptellingsregistrering](#to-create-a-physical-inventory-recording).

7. Velg **OK**-knappen.

En linje for hver vare som finnes i den valgte lokasjonen, og per angitte filtre og alternativer, settes inn på ordren. For varer som er definert for varesporing, merkes det av for **Bruk varesporing**, og opplysninger om forventet antall for serie- og partinumre er tilgjengelig ved å velge **Linjer**-handlinger og deretter **Varesporingslinjer**. Hvis du vil ha mer informasjon, kan du se delen [Håndtering av varesporing ved telling av varelager](#handling-item-tracking-when-counting-inventory).

Du kan deretter fortsette med å opprette én eller flere registreringer, som er instruksjoner til de ansatte som utfører den faktiske tellingen.  

## <a name="to-create-a-physical-inventory-recording"></a>Slik opprettes en vareopptellingsregistrering
For hver vareopptellingsordre kan du opprette én eller flere vareopptellingsregistreringsdokumenter der ansatte angir de opptalte antallene, enten manuelt eller gjennom en integrert skannerenheten.

En registrering opprettes som standard for alle linjene i den relaterte vareopptellingsordren. For å unngå at to ansatte teller de samme varene ved distribuert opptelling, er det lurt å gradvis fylle vareopptellingsordren ved å definere filtre i kjørselen **Beregn linjer** (se delen "Slik opprettes en vareopptellingsordre") og deretter opprette vareopptellingsregistreringen og merke av for **Bare linjer som ikke finnes i registreringer**. Denne innstillingen sørger for at hver nye registrering du oppretter, bare inneholder ulike varer enn de på andre registreringer.

Ved manuell opptellingsdato kan du skrive ut en liste, rapporten **Registrering for vareopptelling**, som har en tom kolonne til å skrive de opptalte antallene i. Når tellingen er utført, angir du de registrerte antallene på siden **Registrering for vareopptelling**. Til slutt overføre du de registrerte antallene til den relaterte vareopptellingsordren ved å sette status til **Fullført**.

1. På en **Vareopptellingsordre**-side som inneholder linjer for varene som skal telles i én registrering, velger du handlingen **Lag ny registrering**.
2. Velg alternativer, og angi filtre etter behov.
3. Velg **OK**-knappen.

    Et dokument for vareopptellingsregistrering opprettes.

4. For hvert sett med varer som skal telles, lastes varene på den relaterte vareopptellingsordren, og gjenta trinn 1 til 3 med **Bare linjer som ikke finnes i registreringer** avmerket.

5. Velg handlingen **Registreringer**, og åpne siden **Liste over registreringer for vareopptelling**.
6. Åpne den aktuelle registreringen.
7. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
8. For varer som bruker varesporing, opprett en ekstra linje for hver parti- eller serienummerkode ved å velge handlingen **Funksjon**, og klikk deretter på **Kopier linjen**-handlingen. Hvis du vil ha mer informasjon, kan du se delen [Håndtering av varesporing ved telling av varelager](#handling-item-tracking-when-counting-inventory).  
9. Velg **Skriv ut**-handlingen for å forberede det fysiske dokumentet som de ansatte skal bruke til å notere det opptalte antallet.

## <a name="to-finish-a-physical-inventory-recording"></a>Slik avsluttes vareopptellingsregistrering
Når de ansatte har talt lagerantallene, må du forberede registrering av antallet i systemet.

1. Fra siden **Liste over registreringer for vareopptelling** velger du vareopptellingsregistreringen som du vil fullføre, og velg deretter **Rediger**-handlingen.
2. På hurtigfanen **Linjer** fyller du ut det faktisk opptalte antallet i feltet **Antall** for hver linje.
3. For varer med serie- eller partinumre (boksen **Bruk varesporing** er avmerket) angi de opptalte antallene på linjene som er reservert for henholdsvis varens serie- og partinumre. Hvis du vil ha mer informasjon, kan du se delen [Håndtering av varesporing ved telling av varelager](#handling-item-tracking-when-counting-inventory).
4. Merk av for **Registrert** for hver linje.
5. Når du har angitt alle data for registrering av en vareopptelling, velger du **Fullfør**-handlingen. Vær oppmerksom på at alle linjene må ha **Registrert**-alternativet valgt.

> [!NOTE]
> Når du har fullført en vareopptellingsregistrering, overføres hver linje til linjen på den relaterte vareopptellingsordre som samsvarer nøyaktig med linjen. For å samsvare med verdiene i feltene **Varenr.**, **Variantkode**, **Lokasjonskode** og **Hyllekode** være like på registreringen og ordrelinjene.<br /><br />
> Hvis det ikke finnes noen tilsvarende vareopptellingsordrelinje, og hvis det er merket av for **Tillat registrering uten ordre**, settes det inn en ny linje automatisk, det merkes av for **Registrert uten ordre** på den relaterte vareopptellingsordrelinjen. Ellers vises det en feilmelding, og prosessen avbrytes.<br /><br />
> Hvis mer enn én vareopptellingsregistreringslinje samsvarer med en vareopptellingsordrelinje, vises en melding, og prosessen avbrytes. Hvis to identiske vareopptellingslinjer av én eller annen grunn havner i vareopptellingsordren, kan du bruke en funksjon for å løse problemet. Hvis du vil ha mer informasjon, kan du se delen [Slik finner du dupliserte vareopptellingsordrelinjer](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Slik fullføres en vareopptellingsordre
Når du har en fullført vareopptellingsregistrering, oppdateres feltet **Antall registrert (lagerenhet)** i den relaterte vareopptellingsordren med opptalte (registrerte) verdier, og det merkes av for **På registreringslinjer**. Hvis en opptalt verdi avviker fra forventet, vises differansen i henholdsvis feltet **Positivt antall (lagerenhet)** og **Negativt antall (lagerenhet)**.

Hvis du vil se forventet antall og eventuelle registrerte avvik for varer som har varesporing, kan du velge handlingen **Linjer** og deretter velge handlingen **Varesporingslinjer** for å velge ulike visninger for serie- og partinumre i vareopptellingen.

Du kan også velge handlingen **Differanse for vareopptellingsordre** for å vise eventuelle differanser mellom det forventede antallet og det opptalte antallet.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Slik finner du duplikate vareopptellingsordrelinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Åpne vareopptellingsordren du vil vise dupliserte linjer for.
3. Velg **Vis dupliserte linjer**-handlingen.

Eventuelle like vareopptellingsordrelinjer vises, slik at du kan slette dem og bare beholde én linje med et unikt sett med verdier i feltene **Varenr.**, **Variantkode**, **Lokasjonskode** og **Hyllekode**.

### <a name="to-post-a-physical-inventory-order"></a>Slik bokføres en vareopptellingsordre
Når du har fullført en vareopptellingsordre og endre statusen til **Fullført**, kan du bokføre den. Du kan bare angi status for en vareopptellingsordre til **Fullført** hvis følgende er oppfylt:

- Alle relaterte vareopptellingsregistreringer har statusen **Fullført**.
- Hver vareopptellingsordrelinje er talt opp av minst én registeringen for vareopptelling.
- Boksene **På registreringslinjer** og **Antall forventet (beregnet)** er merket av for alle vareopptellingsordrelinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareopptellingsordrer** og velg den relaterte koblingen.
2. Velg vareopptellingsordren som skal fullføres, og velg deretter **Rediger**-handlingen.

    På siden **Vareopptellingsordre** vises antallet som er registrert i feltet **Antall registrert (lagerenhet)**.
3. Velg handlingen **Fullfør**.

    Verdien i feltet **Status** endres til **Fullført**, og du kan nå bare endre rekkefølgen ved først å velge handlingen **Åpne på nytt**.
4. Hvis du vil bokføre ordren, velger du **Bokfør** og deretter **OK**.

De involverte varepostene oppdateres sammen med eventuelle tilknyttede varesporingspostene.

### <a name="to-view-posted-physical-inventory-orders"></a>Slik viser du bokførte vareopptellingsordrer
Etter bokføring slettes vareopptellingsordren, og du kan vise og evaluere dokumentet som en bokført vareopptellingsordre, inkludert vareopptellingsregistreringer og eventuelle merknader som er opprettet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ordrer for bokført vareopptelling** og velg den relaterte koblingen.
2. På siden **Ordrer for bokført vareopptelling** velger du den bokførte vareopptellingsordren som du vil vise, og velg deretter handlingen **Vis**.
3. Hvis du vil se en oversikt over relaterte vareopptellingsregistreringer, velger du **Registreringer**-handlingen.

## <a name="handling-item-tracking-when-counting-inventory"></a>Håndtering av varesporing ved telling av varelager
Varesporing gjelder serie- eller partinumrene som er tilordnet til varer. Når du teller en vare som er lagret i lageret som for eksempel 10 ulike partinumre, må den ansatte kunne registrere hvilke og hvor mange enheter av hvert partinummer som er på lager. Hvis du vil ha mer informasjonom varesporingsfunksjonalitet, se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).

Boksen for **Bruk varesporing** på vareopptellingsordrelinjer velges automatisk hvis en varesporingskode er definert for en vare, men du kan også velge eller fjerne den manuelt.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Eksempel: Forberede en registrering for vareopptelling for en varesporet vare
Vurder en vareopptellingen for Vare A, som er lagret i lageret som ti ulike serienumre.
1. På registreringslinjen for varen merker du av for **Bruk varesporing**.
2.  Velg **Serienr.**-feltet, velg det første serienummeret som finnes i beholdningen for varen, og velger deretter **OK**-knappen.

    Fortsett med å kopiere linjen for den første varesporede varen for å sette inn flere linjer i henhold til antall serienumre som er lagret i lageret.

3. Velg **Funksjoner**-handling og deretter **Kopier linje**-handlingen.
4. På siden **Kopier postlinje for vareopptelling**, skriver du inn 9 i feltet **Antall eksemplarer**, og velg deretter **OK**-knappen.
5. På den første av kopilinjene velger du feltet **Serienr.**, og deretter velger du det neste serienummeret for varen.
6. Gjenta trinn 5 for de gjenstående åtte serienumrene, og det er viktig at du ikke velger den samme to ganger.
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

På siden **Vareopptellingsordre** inneholder feltet **Negativt antall (lagerenhet)** *8*. For den aktuelle ordrelinjen vil siden **Liste over varesporinger for vareopptelling** inneholde de positive eller negative antallene for de enkelte partinumrene.

## <a name="inventory-documents"></a>Lagerdokumenter
Følgende dokumenttyper er nyttige når du skal håndtere lageret:

- Bruke **Lagermottak** til å registrere positive justeringer av varer basert på kvalitet, antall og kostnad.
- Bruk **Lagerleveringer** til å skrive av manglende eller skadde varer.

Du kan skrive ut disse dokumentene når som helst, frigi og åpne dem på nytt, og tilordne felles verdier, inkludert dimensjoner, i hodet. Hvis du vil skrive ut dokumentene på nytt etter at de er bokført, kan du gjøre det på sidene **Bokført lagermottak** og **Bokført lagerlevering**.

> [!NOTE]
> Før du kan bruke disse dokumentene, må du angi en nummerserie for å opprette ID-ene. Hvis du vil ha mer informasjon, kan du se neste avsnitt.

### <a name="to-set-up-numbering-for-inventory-documents"></a>Definere nummerering for lagerdokumenter
Følgende fremgangsmåte viser hvordan du definerer nummerering for lagerdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.
2. I hurtigfanen **Nummerering** angir du følgende nummerserien for dokumenter i følgende felt:
   - **Numre for lagermottak**  
   - **Numre for bokførte lagermottak**  
   - **Numre for lagerlevering**  
   - **Numre for bokført lagerlevering**  

### <a name="to-create-and-post-an-inventory-document"></a>Opprette og bokføre et lagerdokument
Følgende fremgangsmåte viser hvordan du oppretter, skriver ut og bokfører et lagermottak. Trinnene er de samme for lagerleveringer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2. I toppteksten på siden **Lagermottak** velger du lokasjonen i feltet **Lokasjonskode**, og deretter fyller du ut de gjenværende feltene etter behov.
3. I hurtigfanen **Linjer** velger du lagervaren i feltet **Vare**. I feltet **Antall** angir du hvor mange varer som skal legges til. 
4. Hvis du vil skrive ut en rapport kalt **Lagermottak** fra siden **Lagermottak**, velger du handlingen **Skriv ut**.

Følgende funksjoner er tilgjengelige på siden **Lagermottak**:

- Velg handlingene **Frigi** eller **Åpne på nytt** for å angi statusen for neste behandlingsfase  
- Velge handlingen **Bokfør** for å bokføre lagermottaket, eller velg **Bokfør og skriv ut** for å bokføre mottaket og skrive ut testrapporten  

## <a name="printing-inventory-documents"></a>Skrive ut lagerdokumenter
Du kan angi rapportene som skal skrives ut i forskjellige faser, ved å velge ett av følgende alternativer i feltet **Bruk** på siden **Rapportvalg – beholdning**:

- Lagermottak
- Lagerlevering
- Bokført lagermottak
- Bokført lagerlevering

> [!NOTE]
> De tilgjengelige rapportene kan variere avhengig av hvor landet befinner seg. Basisprogrammet inkluderer ikke oppsett.

## <a name="see-also"></a>Se også
[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)  
[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Lager](inventory-manage-inventory.md)  
[Lagerstyring](warehouse-manage-warehouse.md)    
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]