---
title: Plassere varer med lagerplasseringer
description: Finn ut hvordan du bruker lagerplasseringsdokumenter til å registrere og bokføre plasserings- og mottaksopplysninger.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '7375,'
---
# <a name="put-items-away-with-inventory-put-aways" />Plassere varer med lagerplasseringer

I [!INCLUDE[prod_short](includes/prod_short.md)] mottar du varer og plasserer dem ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Finn ut mer under [Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

Denne artikkelen refererer til metode B i tabellen.

Hvis lokasjonen er definert for å kreve lagerplasseringsbehandling, men ikke mottaksbehandling, bruker du dokumentet **Lagerplassering** til å registrere og bokføre plasserings- og mottaksopplysninger for kildedokumentet. Inngående kildedokumenter kan være bestillinger, ordrereturer og inngående overføringsordrer.

> [!NOTE]
> Produksjons- og monteringsutdata representerer også inngående kildedokumenter. Finn ut mer om håndtering av produksjons- og monteringsutdata for interne prosesser under [Designdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md).

Du kan opprette lagerplassering på tre måter:  

* Opprette lagerplassering direkte fra selve kildedokumentet.  
* Opprett lagerplasseringer for flere kildedokumenter samtidig, ved hjelp av en kjørsel.  
* Opprett plasseringen i to trinn, ved først å frigi kildedokumentet for å gjøre varene tilgjengelig for plassering. Du kan opprette lagerplasseringen basert på kildedokumentet ved å bruke siden **Lagerplassering**.  

## <a name="to-create-an-inventory-put-away-from-the-source-document" />Slik oppretter du en lagerplassering fra kildedokumentet

1. I kildedokumentet, som kan være en bestilling, ordreretur eller inngående overføringsordre, velger du handlingen **Opprett lagerplassering/-plukking**.  
2. Merk av for **Opprett lagerplassering**.
3. Velg **OK**. En ny lagerplassering er opprettet.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job" />Slik oppretter du flere lagerplasseringer med en kjørsel:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett plassering/plukk/flytting for lager**, og velg deretter den relaterte koblingen. 
2. På hurtigfanen **Lagerforespørsel** bruker du filtrene **Kildedokumentet** og **Kildenr.** for å filtrere etter bestemte dokumenttyper eller dokumentnummerintervaller. Du kan for eksempel bare opprette plasseringer for bestillinger.
3. Merk av for **Opprett lagerplassering** på hurtigfanen **Alternativer**.
4. Velg **OK**-knappen. De angitte lagerplasseringene blir opprettet.

## <a name="to-create-the-put-away-in-two-steps" />Slik oppretter du plasseringen i to trinn

### <a name="to-request-an-inventory-put-away-by-releasing-the-source-document" />Be om en lagerplassering ved å frigi kildedokumentet

Når du frigir bestillinger, ordrereturer og inngående overføringsordrer, blir varene på ordrene tilgjengelige for plassering. Trinnene nedenfor beskriver hvordan du gjør varene i en bestilling klar til å plasseres.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Velg bestillingen som skal frigis, og velg deretter **Frigi**-handlingen.  

### <a name="to-create-an-inventory-put-away-based-on-the-source-document" />Slik oppretter du en lagerplassering basert på kildedokumentet

En lageransatt kan opprette en ny lagerplassering basert på det frigitte kildedokumentet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplassering** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg hvilken type kildedokument du plasserer for, i **Kildedokument**-feltet.  
4. Velg kildedokumentet i **Kildenr.**-feltet.  
5. Du kan også velge handlingen **Hent kildedokument** for å velge dokumentet fra en liste over inngående kildedokumenter som er klare for plassering på lokasjonen.  
6. Velg **OK**-knappen for å fylle ut plasseringslinjene i henhold til det valgte kildedokumentet.  

## <a name="to-record-the-inventory-put-away" />Slik registrerer du lagerplasseringen

1. Åpne et tidligere opprettet plasseringsdokument på siden **Lagerplasseringer**.  
2. I **Hyllekode**-feltet på plasseringslinjene foreslås hyllene der varene må plasseres, basert på varenes standardhylle. Du kan endre hyllen ved behov.  
3. Utfør plasseringen, og angi det faktiske plasseringsantallet som ble plassert, i feltet **Ant. som skal håndt**.

    Hvis du må plassere varene for én linje i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.  
4. Når du har plassert varene, velger du handlingen **Bokfør**.  

    * Bokfør mottaket av kildedokumentlinjene som er plassert
    * Hvis lokasjonen bruker hyller, oppretter bokføring også lagerposter for bokføring av hylleantallendringer.

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-put-away-items" />Se relatert [Microsoft-opplæring](/training/modules/receive-put-away-items/)

## <a name="see-also" />Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
