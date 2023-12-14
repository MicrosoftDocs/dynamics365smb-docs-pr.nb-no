---
title: Plasser produksjonsavgang
description: Denne artikkelen beskriver hvordan du plasserer produksjonsavgangen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Plassere produksjonsavgang eller monteringsavgang

Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).  

I grunnleggende lageroppsett hvor lokasjonen krever plasseringsbehandling, bruker du dokumentet **Lagerplassering** til å bokføre produksjonsavgang og registrere plasseringer for den.  

> [!NOTE]  
> Monteringsprosesser støtter ikke lagerplasseringer. Du bokfører en monteringsordre for å registrere avgang. Hvis du bruker hyller, kan du flytte varer mellom hyllene senere. Finn ut mer under [Flytt varer ad hoc i grunnleggende lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

I avanserte lageroppsett hvor en lokasjon krever både plasserings- og mottaksbehandling, kan du opprette enten et internt plasseringsdokument eller et flyttedokument for å plassere avgangen.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Slik plasseres produksjonsavgang med lagerplassering

Det første trinnet til å plassere avgang er å opprette den inngående lagerforespørselen. Denne forespørselen informerer lageret om at produksjons- eller monteringsordreavgangen er klar til å plasseres.

### <a name="to-create-the-inbound-warehouse-request"></a>Slik oppretter du den inngående lagerforespørselen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  
2. Velg produksjonsordren som er klar til plassering, og velg handlingen **Opprett inngående lagerforespørsel**.  

> [!NOTE]  
> Du kan også opprette den inngående lagerforespørselen ved å velge feltet **Opprett inngående foresp.** når du fornyer produksjonsordren. Finn ut mer under [Oppdater eller planlegg produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md)  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Slik plasseres varer med lagerplassering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplassering** og velg den relaterte koblingen.  
2. Opprett en ny lagerplassering. Finn ut mer under [Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Du får tilgang til produksjonsordreavgang ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
4. Fyll ut plasseringslinjene etter behov.
5. Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføring oppretter lagerpostene og bokføre avgangen av varene.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Du kan også opprette en **Lagerplassering** direkte fra den frigitte produksjonsordren. Finn ut mer under [Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bokfører en lagerplassering, antas det at alle operasjonene bokføres i henhold til standardruten. Det vil si avgangsantallet som bokføres i henhold til den siste operasjonen. Du kan bruke ferdigmeldingskladden til å bokføre avvik i avgangsantallet og oppstillingstid og operasjonstid. Hvis du må bokføre delvis etter at du opprettet lagerplasseringen, kan du gjøre dette for oppstillingstider og antall for alle operasjoner bortsett fra den siste. Den siste operasjonen styres av lagerplasseringen.  

Hvis du bare trenger å bokføre oppsett eller kjøretid i den siste operasjonen, kan du sette avgangsantallet i den siste operasjonen til 0. Du kan velge ikke å bokføre den siste linjen i det hele tatt ved å slette den.

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Slik plasserer du monterings- og produksavgang i avanserte lagerkonfigurasjoner

Når du bokfører avgangen for produksjons- eller monteringsordrer i et lager som bruker lagerstrying, plasseres avgangen i hyllen som er definert i produksjons- eller monteringsordren. Finn ut mer om ulike måter å flytte varer på i lageret med avanserte oppsett, går du til [Flytt varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Du kan ikke angi kildedokumentnummeret, for eksempel produksjonsordrenummeret, i dokumentene for intern plassering, plukking eller flytting for monterings- eller produksjonsavgangsprosesser.  

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
