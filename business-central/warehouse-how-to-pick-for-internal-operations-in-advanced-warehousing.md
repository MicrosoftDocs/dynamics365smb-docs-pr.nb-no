---
title: Plukk for interne operasjoner i avansert lageroppsett
description: 'Hvis lokasjonene bruker plukking og levering, kan du plukke komponenter for produksjons-, monterings- og prosjektaktiviteter på Lagerplukk-siden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-projects-in-advanced-warehouse-configurations"></a>Plukke for produksjon, montering eller prosjekter i avanserte lagerkonfigurasjoner

Hvordan du plukker komponenter for produksjons-, prosjekt- eller monteringsordrer, avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

Bruk følgende innstillinger på **Lokasjon kort**  siden for lokasjonen i en avansert lagerkonfigurasjon for den utgående flyten (plukk):

* Produksjon, i **prod. forbruk whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk)**.
* Montering, i **Asm. Forbruk Whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk).**
* Prosjektstyring, i Prosjektforbruk **whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk).**

Når lokasjonen er definert til å kreve plukkbehandling, bruker du plukkdokumenter til å opprette og behandle plukkinformasjon før du bokfører forbruk eller forbruk av komponenter.  

Du kan ikke opprette et lagerplukkdokument fra bunnen av. Plukk er en del av en arbeidsflyt der en person som behandler en ordre, oppretter dem på en push-måte, eller den lageransatte oppretter dem på en pull-måte:

- På en push-måte, der du bruker **Opprett Plukk**-handlingen på siden **Produksjonsordre**, **Monteringsordre**, siden **Prosjektkort**. Velg linjene som skal plukkes, og klargjør plukkingene ved å angi hvilke hyller det skal tas fra og hvilke det skal plasseres i, og hvor mange enheter som skal håndteres. Hyllene kan være forhåndsdefinert for lagerlokasjonen eller ressursen.
- I en pull-måte, der du frigir **produksjonsordre**, **monteringsordre**, **prosjektkort** til lager og gjør varene tilgjengelige for plukking. Deretter på siden **Plukkforslag** kan lageransatte bruke handlingen **Hent lagerdokumenter** til å hente tildelte plukkinger.

Når du skal plukke eller flytte komponenter for kildedokumenter på en pull-måte, må du frigi kildedokumentet for å gjøre det klart for plukking. Frigi kildedokumenter for interne operasjoner på følgende måter.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produksjonsordre|Endre ordrestatusen til Frigitt eller Opprett en frigitt produksjonsordre med en gang.|  
|Monteringsordre|Endre status til Frigitt.|
|Prosjekter | Endre status til Åpne eller opprett prosjekt med statusen Åpne med en gang.|  

## <a name="production"></a>Produksjon

Bruk **Lagerplukkdokumenter** for plukking av produksjonskomponenter i flyten til produksjon.

For en lokasjon som bruker hyller til å flytte varer for åpne produksjonshyller, kan du bruke følgende metoder:

* For en lokasjon som bruker lagerstyring, følger du fremgangsmåten i artikkelen [Flytt varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).
* For andre lokasjoner følger du fremgangsmåten i artikkelen [Flytt varer internt i grunnleggende lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a>Montering

Bruk **lagerplukkingsdokumenter** til å flytte monteringskomponenter til monteringsområdet.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-typer for monteringsflyter. Hvis du vil lære mer om monter-til-ordre i utgående lagerflyt, kan du gå til [Hndtering av monter-til-ordre-varer i lagerleveringer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Prosjektstyring

Bruk **Lagerplukk-dokumenter** til å plukke prosjektkomponenter i flyten til prosjektstyring.

> [!NOTE]
> Project støtter ikke avanserte konfigurasjoner der veksleknappen **Direkte plukking og plassering** er aktivert.

## <a name="check-whether-items-are-available-for-picking"></a>Kontrollere om varene er tilgjengelige for plukking

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Slik oppretter du plukkdokumenter i bulk med plukkforslaget

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Hent lagerdokumenter**.  

    Listen viser frigitte produksjons-, prosjekt- og monteringsordrer som er videresendt til plukkfunksjonen. Ordrene inkluderer ordrene som det allerede er opprettet plukkinstruksjoner for. Dokumenter med plukklinjer som er plukket og registrert, vises ikke i denne oversikten.  
3. Velg ordrene du vil forberede plukking for.

    > [!NOTE]  
    > Hvis du velger et dokument som allerede har instruksjoner for alle linjene, gir [!INCLUDE [prod_short](includes/prod_short.md)] beskjed om at det ikke finnes noe å håndtere. For å kombinere allerede opprettede lagerplukkinstruksjoner til én plukkinstruks, må du slette individuelle lagerplukk først.

4. Fyll ut feltet **Sorteringsmetode** for å sortere linjene på den måten du foretrekker.  

    > [!NOTE]  
    > Måten linjene blir sortert på i forslaget, overføres ikke automatisk ved plukkinstruksen. De samme sorteringsverktøyene er imidlertid tilgjengelige sammen med hylleprioriteringen. Du kan enkelt opprette odren for linjene du planlegger i forslaget på nytt, når du oppretter plukkinstruksjonene eller etter sortering i plukkinstruksjonene.

5. Fyll ut feltet **Ant. som skal håndt.**. Velg handlingen **Autoutfyll ant. som skal hndt.**, eller fyll ut feltene manuelt.  

    Siden viser antall som er tilgjengelig i kryssoverføringshyller, som er nyttig når du skal planlegge arbeidsoppgaver i situasjoner for kryssoverføring. [!INCLUDE[prod_short](includes/prod_short.md)] foreslår alltid en plukking fra en kryssoverføringshylle først.

6. Du kan redigere linjene manuelt om nødvendig. Du kan også slette noen av linjene for gjør plukk mer effektiv. Hvis det for eksempel finnes flere linjer med varer som er i kryssoverføringshyller, er det mulig at du vil opprette en plukking for alle linjene. De kryssoverførte varene blir plukket med andre varer på kildedokumentet, og kryssoverføringshyllene har plass til flere inngående varer.

    > [!NOTE]  
    >  Linjene slettes blir fra dette forslaget, ikke fra plukkutvalgsoversikten.  

7. Velg handlingen **Opprett plukk**. Siden **Opprett plukk** åpnes, der du kan legge til mer informasjon i plukkingen.  

    Angi hvordan du kombinerer plukklinjer i plukkdokumentene ved å velge ett av følgende alternativer.  

    |Alternativ|Beskrivelse|
    |-|-|
    |Per lager Dokument|Oppretter separate plukkdokumenter for forslagslinjer med samme lagerkildedokumentet.|
    |Per kund/levrd/lok|Oppretter separate plukkdokumenter for hver kunde (prosjekt)|
    |Per vare|Oppretter separate plukkdokumenter for hver vare i plukkforslaget.|
    |Per fra-sone|Oppretter separate plukkdokumenter for hver sone du plukker varene fra.|
    |Per hylle|Oppretter separate plukkdokumenter for hver hylle du plukker varene fra.|
    |Per forfallsdato|Oppretter separate plukkdokumenter for kildedokumenter som har samme forfallsdato.|

    Bruk følgende alternativer til å angi hvordan du oppretter plukkdokumentene.  

    |Alternativ|Description|
    |-|-|
    |Maks Nr. plukklinjer|Oppretter plukkdokumenter som ikke har flere enn det angitte antallet linjer i hvert dokument.|
    |Maks Antall plukkildedok.|Oppretter plukkdokumenter som dekker opp til det angitte antallet kildedokumenter.|
    |Tilordnet bruker-ID|Oppretter plukkdokumenter bare for forslagslinjer som er tilordnet til den valgte lageransatte.|
    |Sorteringsmetode for plukklinjer|Velg fra de tilgjengelige alternativene for å sortere linjene plukkdokumentet som er opprettet.|
    |Angi anbrekksfilter|Skjuler midlertidige anbrekksplukklinjer når en større enhet konverteres til en mindre enhet og plukkes.|
    |Ikke fyll ut ant. som skal hnd|Lar feltet **Ant. som skal håndt** være tomt i de opprettede plukklinjene.|
    |Skriv ut plukk|Skriver ut plukkdokumenter når de opprettes. Du kan også skrive ut fra de opprettede plukkdokumentene.|

8. Velg **OK**-knappen.  

## <a name="to-pick-items-for-a-production-order-assembly-order-or-project"></a>Slik plukker du varer til en produksjonsordre, en monteringsordre eller et prosjekt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Plukking** og velger den relaterte koblingen.  

    Hvis du skal arbeide med en bestem plukking, velger du plukkingen fra oversikten eller filtrerer oversikten for å finne plukkingene som er tildelt til deg. Åpne kortet for plukkingen.  
2. Hvis feltet **Tildelt bruker-ID** er tomt, angir du om nødvendig ID-en for å identifisere deg selv.  
3. Plukke varene.  

    Hvis lageret er definert slik at hyller brukes, brukes varenes standardhyller til å foreslå hvor du skal ta varene fra. Instruksjonene inneholder minst to separate linjer for handlingene Hent og Plasser.  

    Operasjonsområder, for eksempel produksjonsutførelse, kan ha en standardhylle for komponentene de trenger. Hvis dette er tilfellet, legges standard hyllekode til i lagerplukkdokumentet for å angi hvor varene skal plasseres. Hvis du vil ha mer informasjon, kan du se verktøytipsene for feltene **Hyllekode** for Til-produksjon, **Hyllekode** for Til-montering, **Hyllekode** for Til-prosjekt.

    Hvis lageret er definert slik at lagerstyring brukes, brukes hylleprioriteringen til å beregne de beste hyllene å plukke fra. Disse hyllene foreslås på plukklinjene. Instruksjonene inneholder minst to separate linjer for handlingene Hent og Plasser.  

    * Den første linjen, med **Hent** i **Handlingstype**-feltet, angir hvor varene er plassert i plukkområdet. Hvis du leverer et stort antall varer på én leveringslinje, kan det hende at du må plukk varene i flere hyller, det finnes derfor en Hent-linje for hver hylle.
    * Den neste linjen, med **Plasser** i **Handlingstype**-feltet, viser hvor du må plassere varene i lageret. Du kan ikke endre sonen og hyllen på denne linjen.

    > [!NOTE]
    > Hvis du må plukke eller plassere varene for én linje i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.

      Du kan sortere plukklinjene etter ulike kriterier, for eksempel etter vare, hyllenummer eller forfallsdato. Sortering kan bidra til å optimalisere plasseringsprosessen, for eksempel:

    * Hvis Hent- og Plasser-linjene for hver leveringslinje ikke følger umiddelbart etter hverandre, og du vil at de skal gjøre det, kan du sortere linjene ved å velge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis hylleprioritering gjenspeiler det fysiske oppsettet av lageret, kan du bruke sorteringsmetoden **hylleprioriteringen** til å organisere arbeidet etter hyllelokasjoner.

  > [!NOTE]  
  > Linjer sorteres i stigende rekkefølge etter det valgte kriteriet. Hvis du sorterer etter dokument, utføres sorteringen først etter dokumenttype basert på feltet **Kildedokument for lageraktivitet**. Hvis du sorterer etter levering, gjøres sorteringen først etter måltype basert på feltet **Lagermåltype**.

4. Når du har plukket og plassert varene i produksjons-, monterings- eller prosjektområdet eller hyllen, velger du handlingen **Registrer plukk** .  

    Du kan nå samle varene i det tilsvarende området og bokføre bruken eller forbruket av de plukkede komponentene ved å bokføre forbrukskladd, monteringsrekkefølge eller prosjektkladd. Følgende artikler gir mer informasjon:

    * [Registrere forbruk og avgang for én frigitt produksjonsordrelinje](production-how-to-register-consumption-and-output.md)
    * [Monter varer](assembly-how-to-assemble-items.md)
    * [Registrere forbruk eller bruk for prosjekter](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Trekk produksjonskomponenter i et avansert lageroppsett

Trekkmetodene påvirker flyten av komponenter i produksjon. Finn ut mer under [Lagertrekk komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md). Avhengig av den valgte trekkmetoden kan du plukke komponenter for produksjon på følgende måter:

* Bruk et **lagerplukkdokument** til å registrere plukkingen for varer som bruker **manuell**  trekkmetode. Du må registrere forbruk separat. Finn ut mer under [Massebokføre produksjonsforbruk](production-how-to-post-consumption.md).
* Bruk et **lagerplukkdokument** til å registrere plukkingen for varer som bruker trekkmetoden **Plukk + fremover**, **Plukk + bakover**. Forbruk av komponentene utføres automatisk enten når du endrer statusen for produksjonsordren, eller ved å starte eller avslutte en operasjon. Alle obligatoriske komponenter må være tilgjengelig. Ellers stoppes bokføring av trukket forbruk for komponenten.
* Bruk et **lagerflyttingsdokument** uten referanse til et kildedokument eller andre måter å registrere flytting av komponenter som bruker trekkmetoden **Fremover** eller **Bakover**. Komponenter forbrukes automatisk enten når du endrer statusen for produksjonsordren, eller ved å starte eller avslutte en operasjon. Alle obligatoriske komponenter må være tilgjengelig. Ellers stoppes bokføring av trukket forbruk for komponenten. Finn ut mer under [Flytt varer](warehouse-move-items.md).

### <a name="example"></a>Eksempel

Du har en produksjonsordre for 15 STK av varen SP-SCM1004. Noen av varene på komponentoversikten må trekkes manuelt i en forbrukskladd. Andre varer kan plukkes og trekkes automatisk ved hjelp av trekkmetoden **Plukk + bakover**.  

Fremgangsmåten nedenfor beskriver handlingene ulike personer gjør og det relaterte svaret:  

1. Verkstedlederen frigir produksjonsordren. Varer med trekkmetoden **Fremover** og ingen rutekobling, trekkes fra den åpne produksjonshylle.  
2. Verkstedlederen velger handlingen **Opprett lagerplukk** på produksjonsordren. Et lagerplukkdokumentet opprettet plukking for varer med trekkmetodene **Manuell**, **Plukk + Bakover** og **Plukk + Fremover**. Disse varene plasseres i hyllen til produksjon.  
3. Lagerlederen tilordner plukkingene til en lagermedansatt.  
4. Den lageransatte plukker varene fra aktuelle hyller og plasserer dem i hyllen til produksjon eller i hyllen som er angitt i plukkingen. Hyllen kan være en hylle for arbeidssenter eller produksjonsressurs.
5. Den lageransatte registrerer plukkingen. Antallet overføres fra plukkhyllen og legges til forbrukshyllen. **Plukket ant.**-feltet oppdateres i komponentoversikten for alle plukkede varer.

    > [!NOTE]  
    >  Bare antallet som plukkes kan brukes.  
6. Maskinoperatøren gir produksjonssjefen beskjed om at sluttvarene er ferdige.
7. Verkstedlederen bruker forbrukskladden eller produksjonskladden til å bokføre forbruk av komponentvarer som bruker enten trekkmetoden **Manuell**.
8. Butikklederen bruker ferdigmeldingskladden eller produksjonskladden til å bokføre avgangen. Antallet komponentvarer som bruker trekkmetoden **Plukk + fremover** eller **Plukk + bakover** med rutekoblinger, trekkes fra til hyllen til produksjon.
9. Produksjonssjefen endrer statusen for produksjonsordren til **Ferdig**. Antallet komponentvarer som bruker trekkmetoden **Bakover**, trekkes fra den åpne produksjonshyllen, og antallet komponentvarer som bruker trekkmetoden **Plukk + Bakover**, og ingen rutekobling trekkes fra hyllen til produksjon.  

Illustrasjonen nedenfor viser når **Hyllekode**-feltet i komponentoversikten fylles i henhold til lokasjonsoppsettet eller oppsettet for produksjonsressurs/arbeidssenter.  

:::image type="content" source="media/binflow.png" alt-text="Oversikt over når og hvordan Hyllekode-feltet fylles ut.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Produser til ordre-produksjonskomponenter i et avansert lageroppsett

I scenarioer der en produsert vare består av råvarer og halvfabrikata med produksjonspolicyen satt til **Produser på ordre**, blir lagerplukkingen for de halvferdige komponentene lagt til i den samme produksjonsordren med feltet **Planleggingsnivåkode** fylt ut. Det forventes at de halvferdige varene er tilgjengelige for forbruk umiddelbart og ikke krever plukking, slik at de ikke inkluderes i plukkdokumentet. De opprettede lagerplukkene inkluderer bare råvarer for produsert vare og halvfabrikata.

Hvis halvfabrikata imidlertid er tilgjengelig på lager, foreslår planleggingssystemet at du forbruker disse i stedet for å produsere hele antallet. En produsert vare krever for eksempel fem halvfabrikata, mens tre allerede er på lager. I dette tilfellet er fem halvfabrikata oppført i produksjonsordrekomponentene, men bare to produseres i samme produksjonsordre som en separat produksjonsordrelinje.
Et slikt oppsett er ikke kompatibelt med lagerplukk, og avhengig av frekvensen må du enten endre produksjonspolicyen for halvfabrikata til **Produser til lager** eller dele produksjonsordrekomponentlinjen manuelt når du skal plukke de halvfabrikata som ble produsert tidligere.


## <a name="see-also"></a>Se også

- [Håndtere lager](inventory-manage-inventory.md)  
- [Definer lagerstyring](warehouse-setup-warehouse.md)  
- [Monteringsstyring](assembly-assemble-items.md)  
- [Oversikt over lagerstyring](design-details-warehouse-management.md)
- [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
