---
title: Plukke varer med lagerplukk
description: Finn ut hvordan du bruker lagerplukk til å registrere og bokføre plukk- og leveringsinformasjon for kildedokumenter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 7377'
---
# <a name="pick-items-with-inventory-picks" />Plukke varer med lagerplukk

I [!INCLUDE[prod_short](includes/prod_short.md)] plukker og leverer du varer ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Utgående prosess|Plukk nødv.|Levering nødv.|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre plukking og levering fra et lagerplukkdokument|Slått på||Grunnleggende: ordre for ordre.|  
|U|Bokføre plukking og levering fra en lagerfølgeseddel||Slått på|Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel|Slått på|Slått på|Avansert|  

Finn ut mer under [Utgående lagerflyt](design-details-outbound-warehouse-flow.md).

Denne artikkelen refererer til metode B i tabellen.

Når lokasjonen din er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du **Lagerplukk**-siden til å registrere og bokføre plukkings- og leveringsopplysninger for kildedokumentene. Utgående kildedokumenter kan være ordrer, bestillingsreturer og utgående overføringsordrer.

> [!NOTE]
> Produksjons- og monteringsordrekomponentbehov representerer også utgående kildedokumenter. Finn ut mer om håndtering av produksjons- og monteringsordrer for interne prosesser under [Designdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md).
>
> Selv om serviceordrer også er utgående kildedokumenter, støtter de ikke basisnivået for ordre for ordre.
>
> Når du plukker og leverer salgslinjeantall som er montert til ordre, er det visse regler du må følge når du oppretter lagerplukklinjene. Finn ut mer under [Håndter montere-til-ordre-varer med lagerplukk](#handling-assemble-to-order-items-with-inventory-picks).  

Du kan opprette lagerplukk på tre måter:

* Opprette lagerplukket direkte fra kildedokumentet  
* Opprett lagerplukk for flere kildedokumenter samtidig ved hjelp av en kjørsel.
* Be om plukket i to trinn, ved først å frigi kildedokumentet, som fungerer som et signal til lageret om at kildedokumentet er klart for plukking.

Lagerplukket kan så opprettes fra siden **Lagerplukk** basert på kildedokumentet.  

## <a name="to-create-an-inventory-pick-from-the-source-document" />Slik oppretter du et lagerplukk fra kildedokumentet

1. I kildedokumentet, som kan være en ordre, bestillingsretur, eller utgående overføringsordre, velger du handlingen **Opprett lagerplassering/-plukking**.
2. Merk av for **Opprett lagerplukking**.  
3. Velg **OK**. Et nytt lagerplukk opprettes.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job" />Slik oppretter du flere lagerplukk med en kjørsel:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett plassering/plukk/flytting for lager**, og velg deretter den relaterte koblingen.  
2. På hurtigfanen **Lagerforespørsel** bruker du filtrene **Kildedokumentet** og **Kildenr.** for å filtrere etter bestemte dokumenttyper eller dokumentnummerintervaller. Du kan for eksempel bare opprette plukk for ordrer.  
3. Merk av for **Opprett lagerplukking** på hurtigfanen **Alternativer**.
4. Velg **OK**-knappen.

## <a name="to-create-the-pick-in-two-steps" />Slik oppretter du plukking i to trinn

### <a name="to-request-an-inventory-pick-by-releasing-the-source-document" />Be om et lagerplukk ved å frigi kildedokumentet

Når det gjelder ordrer, bestillingsreturer og utgående overføringsordrer, oppretter du lagerforespørselen ved å frigi ordren. Ved å frigi ordren blir varene tilgjengelig for plukking.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg ordren som skal frigis, og velg deretter **Frigi**-handlingen.

### <a name="to-create-an-inventory-pick-based-on-the-source-document" />Slik oppretter du et lagerplukk basert på kildedokumentet:

Når en ordre er frigitt, kan den ansatte opprette et lagerplukk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg hvilken type dokument du plukker for, i **Kildedokument**-feltet.  
4. Velg kildedokumentet i **Kildenr.**-feltet.  
5. Du kan også velge handlingen **Hent kildedokument** for å opprette en liste over utgående kildedokumenter som er klare for plukking på lokasjonen.  
6. Velg **OK**-knappen for å fylle ut plukklinjene i henhold til de valgte kildedokumentene.  

## <a name="to-record-inventory-picks" />Slik registrerer du lagerplukk

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. I **Hyllekode**-feltet på plukklinjene foreslås hyllen som varene skal plukkes fra, per varens standardhylle. Du kan endre hylle på denne siden hvis det er nødvendig.  
3. Utfør plukkingen, og angi deretter faktisk antall i feltet **Ant. som skal håndt.**.

    Hvis du må plukke varene for en linje fra mer enn én hylle, for eksempel fordi hele antallet ikke er i hyllen, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.

4. Velg handlingen **Bokfør**.  

    * Bokfør leveringen for kildedokumentlinjene som ble plukket.
    * Hvis lokasjonen bruker hyller, oppretter bokføring også lagerposter for bokføring av endringene i hylleantallet.  

## <a name="handling-assemble-to-order-items-with-inventory-picks" />Håndter montere-til-ordre-varer med lagerplukk

Du kan også bruke **Lagerplukk**-siden til å plukke og levere for salg der varer må monteres før de kan leveres. Finn ut mer under [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Monter-til-ordre-varer er ikke fysisk til stede i en hylle før de er montert og bokført som avgang til en hylle. Plukking av monter-til-ordre-varer fra en hylle for leveringer følger en spesiell flyt.

1. Lagermedarbeidere tar monteringsvarene fra en hylle til leveringssonen og bokfører deretter lagerplukkingen.
2. Det bokførte lagerplukket bokfører monteringsavgangen, komponentforbruket og følgeseddelen.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til å automatisk opprette en lagerflytting når lagerplukkingen for monteringsvaren opprettes. Velg feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**. Finn ut mer under [Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md).

Lagerplukklinjer for salgsvarer opprettes på forskjellige måter avhengig av om ingen, noen eller alle salgslinjeantallene er montert til ordre. I scenarioer der noe av antallet monteres og noe plukkes fra lager, opprettes det minst to lagerplukklinjer.

For salg der hele antallet på ordrelinjen er montert til ordre, opprettes én lagerplukklinje for dette antallet. Verdien i feltet **Antall å montere** er det samme som verdien i feltet **Levere (antall)**. **Monter til ordre**-feltet er valgt på linjen.

Hvis en monteringsavgangsflyt er angitt for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen inneholder verdien fra følgende felter i følgende rekkefølge.

* ***Hyllek. lev. fra m. til ordre** <!-- not applicable for inv pick-->
* **Fra-Hyllekode for montering**

Hvis en hyllekode ikke er angitt på ordrelinjen og ingen monteringsavgangsflyt er definert for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen tomt. Lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der monteringsvarene er montert.

I scenarioer der en del av antallet monteres og en annen del plukkes, opprettes minst to plukklinjer.

* Én plukklinje til montere-til-ordre-antallet. [!INCLUDE [prod_short](includes/prod_short.md)] bruker følgende felter, i denne rekkefølgen, til å fastslå hyllekoden: **Hyllekode**, **Hyllek. lev. fra m. til ordre** og deretter **Fra-Hyllekode for montering**. Hvis disse feltene er tomme, må lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der varene er montert.  
* Den andre plukklinjen avhenger av hvilke hyller som kan oppfylle det gjenværende antallet. Hvis varen beholdes i flere hyller, opprettes det flere linjer. Hent-linjen er basert på antallet i **Levere (antall)**-feltet.

> [!NOTE]  
> Hvis varer monteres til ordre, opprett lagerplukkingen for den koblede ordren en lagerflytting for alle monteringskomponentene.  

## <a name="see-related-microsoft-trainingtrainingpathspick-ship-items-business-central" />Se relatert [Microsoft-opplæring](/training/paths/pick-ship-items-business-central/)

## <a name="see-also" />Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Gjennomgang: Plukking og levering i grunnleggende lageroppsett](walkthrough-picking-and-shipping-in-basic-warehousing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
