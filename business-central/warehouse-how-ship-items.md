---
title: Levere varer
description: Denne artikkelen beskriver hvordan du leverer varer fra lageret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# Lever varer med en lagerlevering

I [!INCLUDE[prod_short](includes/prod_short.md)] plukker og leverer du varer ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Utgående prosess|Plukk nødv.|Levering nødv.|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre plukking og levering fra et lagerplukkdokument|Slått på||Grunnleggende: ordre for ordre.|  
|U|Bokføre plukking og levering fra en lagerfølgeseddel||Slått på|Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel|Slått på|Slått på|Avansert|  

Gå til [Utgående lagerflyt](design-details-outbound-warehouse-flow.md) hvis du vil ha mer informasjon om levering av varer.

Denne artikkelen refererer til metode C og D i tabellen. I begge metodene starter du med å opprette et leveringsdokument fra et forretningskildedokument. Deretter plukker du de angitte varene for leveringen.

Når en lokasjon krever lagerleveringer, kan du levere varer basert på kildedokumenter som er frigitt til lageret. Når du frigir kildedokumenter, blir varene som er klare til å håndteres på lageret, håndtert. Følgende er eksempler på kildedokumenter:

* Ordrer
* Bestillingsreturer
* Overføringsordrer
* Serviceordrer

Du kan opprette en lagerlevering på en av to måter:

* På en push-måte, når arbeid gjøres på ordre-for-ordre-basis. Velg **Opprett lagerlevering**-handlingen i kildedokumentet for å opprette en lagerlevering for dokumentet.
* I en pull-måte der du bruker **Frigi**-handlingen i kildedokumentet til å frigi den til lageret. En lageransatt oppretter en **lagerlevering** for et eller flere frigitte kildedokumenter. Følgende fremgangsmåte forklarer hvordan du oppretter lagerlevering på en pull-måte.

## Slik leverer du varer med et lagerleveringsdokument

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerleveringer** og velg den relaterte koblingen.  
2. Velg **Ny**.  
3. I **Nr.** -feltet velger du nummerserien som skal brukes til å opprette en ID for leveringen.  
4. I feltet **Lokasjonskode** velger du lokasjonen du vil levere fra. 

    Når du mottar kildedokumentlinjer, kopieres noe av informasjonen fra lokasjonen til hver linje.  
5. Hvis lokasjonen krever hyller, fyller du feltet **Hyllekode**. [!INCLUDE[prod_short](includes/prod_short.md)]] kan legge til hyllekoden for deg, avhengig av oppsettet. Finn ut mer under [Sone- og hyllekoder](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Du kan hente kildedokumentet på to måter:

    * Velg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter – utgående** åpnes. Her kan du velge et eller flere kildedokumenter som er frigitt til lageret, som krever levering.
    * Velg handlingen **Bruk filtre til å hente k.dok...**. Siden **Filtre for å hente kildedokumenter** åpnes. Du kan velge kildedokumentfilteret og bruke det. Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, legges til på siden **Lagerlevering**. Finn ut mer under [Bruke filtre til å hente kildedokumenter](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Hvis lokasjonen bruker kryssoverføring og hyller for hver linje, kan du se gjennom antall varer plassert i kryssoverføringshyllene. [!INCLUDE [prod_short](includes/prod_short.md)] beregner antallene automatisk hver gang feltene på følgeseddelen oppdateres. Hvis dette er varer på leveringen du forbereder, kan du opprette en plukking for alle varene, og deretter fullføre leveringen. Finn ut mer under [Kryssoverføringsvarer](warehouse-how-to-cross-dock-items.md).

7. Opprett et lagerplukk. Hvis lokasjonen krever plukking, kan du opprette plukkaktiviteter for lagerleveringer på en av to måter:

    * På en push-måte, der du bruker **Opprett plukk**-handlingen. Velg linjene for å plukke og angi informasjon om plukkingen. For eksempel hvilke hyller det skal tas fra og plasseres i, og hvor mange enheter som skal håndteres. Hyllene kan være forhåndsdefinert for lagerlokasjonen eller ressursen.
    * På en pull-måte, der du bruker **Frigi**-handlingen. På siden **Plukkforslag** kan du bruke handlingen **Hent lagerdokumenter** til å få tildelte plukkinger. Når lagerplukkingene er fullstendig registrert, slettes linjene i **Plukkforslag**. Finn ut mer under [Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > For en lokasjon som ikke krever plukking, kan du skrive ut lagerleveringen og bruke den som en plukkliste.

8. Angi antallet som skal leveres.  

    For en lokasjon som krever plukking, oppdateres feltet **Lever (antall)** automatisk når plukkingen registreres. Eller fylles feltet **Levere (antall)** ut med antall utestående for hver linje når lagerleveringslinjen opprettes.

    Du kan endre antallet, men du kan ikke levere flere varer enn det som er satt inn i feltet **Restantall** på kildedokumentlinjen eller fra feltet **Ant. plukket** hvis det kreves plukking.

    Når du skal angi verdien i **Lever (antall)**-feltet på alle linjene til null, velger du handlingen **Slett antall som skal leveres**. Det kan for eksempel være nyttig å sette antallene til null hvis du bruker en strekkodeskanner til å oppdatere de leverte antallene. Du kan legge til antallet som er tilgjengelig for levering, ved å velge handlingen **Autoutfyll ant. som skal lev.**.

9. Bokfør leveringen.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## Bruke filtre til å hente kildedokumenter

Fra en lagerlevering kan du bruke siden **Filtre for henting av kildedok** til å hente linjene i det frigitte kildedokument som definerer hvilke varer som skal leveres.

1. I lagerleveringen velger du handlingen **Bruk filtre til å hente k.dok.**. 
2. Hvis du vil definere et nytt filter, angir du en beskrivende kode i feltet **Kode** og velger deretter handlingen **Endre**.

    Siden **Filterkort for kildedokument – utgående** åpnes.

3. Bruk filtre til å definere hvilken type kildedokumentlinjer som skal hentes. Du kan for eksempel velge ulike typer kildedokumenter, for eksempel ordrer eller overføringsordrer.
4. Velg **Kjør**.  

Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, legges til på siden **Lagerlevering** der du angav filtrene.

Du kan opprette et ubegrenset antall filterkombinasjoner. Filtrer lagres på siden **Filtre for henting av kildedok**, og de er tilgjengelige neste gang du trenger dem. Du kan når som helst endre kriteriene ved å velge handlingen **Endre**.

## Sone- og hyllekoder

Hvis hyller er obligatoriske på lokasjonen, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] en sone- og hyllekode på lagerleveringsdokumentet.

* Når det gjelder avanserte oppsett der en lokasjon bruker lagerstyring, bruker [!INCLUDE [prod_short](includes/prod_short.md)] hyllen som er angitt i feltet **Hyllekode for levering** på **lokasjonskortet**. Hvis en **hyllekode for levering** ikke er angitt, er feltet tomt. Hvis varen og leveringshyllen ikke samsvarer, lar [!INCLUDE [prod_short](includes/prod_short.md)] leveringshyllen være tom.
* I andre tilfeller bruker [!INCLUDE [prod_short](includes/prod_short.md)] alltid hyllen som er angitt i feltet **Hyllekode for levering** på **lokasjonskortet** først. Hvis det ikke er angitt en leveringshyllekode, bruker [!INCLUDE [prod_short](includes/prod_short.md)] hyllekoden fra kildedokumentet.

## Håndtere montere-til-ordre-varer i lagerleveringer

I montere-til-ordre-scenarier brukes feltet **Levere (antall)** på lagerleveringslinjer til å registrere hvor mange enheter som monteres. Antallet bokføres deretter som monteringsavgang når du bokfører lagerleveringen. Når det gjelder andre lagerfølgeseddellinjer, er verdien i feltet **Levere (antall)** null.

Når medarbeidere er ferdige med monteringen av noe av eller hele montere-til-ordre-antallet, registrerer antallet i feltet **Levere (antall)** på lagerleveringslinjen. Velg deretter handlingen **Bokfør levering**. Monteringsresultatet bokføres, inkludert komponentforbruket. En følgeseddel for antallet som er postert for salgsordren.

Fra monteringsordren kan du velge **Monter til ordre – lagerfølgeseddellinje** for å få tilgang til lagerfølgeseddellinjen.

Når du bokfører lagerleveringen, oppdateres forskjellige felt på ordrelinjen for å vise fremdrift i lageret. Følgende felt oppdateres også for å vise hvor mange montere-til-ordre-antall som foreløpig ikke er montert og levert:

* **Restantall for ATO-lager**
* **Restantall for ATO-lager (lagerenhet)**

> [!NOTE]
> I kombinasjonsscenarier, der en del av antallet må monteres og en annen del må leveres fra lager, opprettes to lagerleveringslinjer. Én er for montere-til-ordre-antallet og én er for varebeholdningen.
>
> Monter-til-ordre-antallet håndteres som beskrevet i denne artikkelen. Lagerantallet håndteres som en vanlig lagerleveringslinje. Hvis du vil ha mer informasjon om kombinasjonsscenarioer, går du til [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## Se også

[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
