---
title: Plassere produksjonsavgang
description: Denne artikkelen beskriver hvordan du plasserer produksjonsavgangen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Plassere produksjons- eller monteringsutgang

Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).  

I en grunnleggende lagerkonfigurasjon for den innkommende flyten (plassering) aktiverer du følgende innstillinger på **Lokasjon kort-siden**  for lokasjonen:

* For produksjon, i **Prod. Output Whse. Håndtering-feltet**, Velg **Lagerplassering**.
* Monteringsprosesser støtter ikke lagerplasseringer. Du bokfører en monteringsordre for å registrere avgang. Hvis du bruker hyller, kan du flytte varer mellom hyllene senere. Finn ut mer under [Flytt varer ad hoc i grunnleggende lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  
* For prosjekter er ikke plassering aktuelt.

I avanserte lagerkonfigurasjoner der en lokasjon krever plassering, oppretter du et internt plasseringsdokument eller et flyttedokument for å plassere avgangen.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Slik plasseres produksjonsavgang med lagerplassering

Det første trinnet til å plassere avgang er å opprette den inngående lagerforespørselen. Denne forespørselen informerer lageret om at produksjons- eller monteringsordreavgangen er klar til å plasseres.

### <a name="to-create-the-inbound-warehouse-request"></a>Slik oppretter du den inngående lagerforespørselen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  
2. Velg produksjonsordren som er klar til plassering, og velg handlingen **Opprett inngående lagerforespørsel**.  

> [!NOTE]  
> Du kan også opprette den inngående lagerforespørselen ved å velge feltet **Opprett inngående foresp.** når du fornyer produksjonsordren. Finn ut mer under [Oppdater eller planlegg produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md)  

### <a name="to-put-away-output-with-an-inventory-put-away"></a>Slik plasserer du avgang med en lagerplassering:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplassering** og velg den relaterte koblingen.  
2. Opprett en ny lagerplassering. Finn ut mer under [Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Du får tilgang til produksjonsordreavgang ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
4. Fyll ut plasseringslinjene etter behov.
5. Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføring oppretter lagerpostene og bokfører avgangen for varene.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Du kan også opprette en **Lagerplassering** direkte fra den frigitte produksjonsordren. Finn ut mer under [Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bokfører en lagerplassering,forutsetter [!INCLUDE [prod_short](includes/prod_short.md)]  at alle operasjonene er bokført i henhold til standardruten. Det vil si avgangsantallet som bokføres i henhold til den siste operasjonen. Du kan bruke ferdigmeldingskladden til å bokføre avvik i avgangsantallet og oppstillingstid og operasjonstid. Hvis du må bokføre delvis etter at du opprettet lagerplasseringen, kan du gjøre det på oppstillingstider og -antall for alle operasjoner unntatt den siste. Lagerplasseringen styrer den siste operasjonen.  

Hvis du bare trenger å bokføre oppsetts- eller operasjonstiden for den siste operasjonen, setter du avgangsantallet for den siste operasjonen til 0. Du kan velge å ikke bokføre den siste linjen i det hele tatt ved å slette den.

## <a name="to-put-away-assembly-and-production-output-in-advanced-warehouse-configurations"></a>Slik plasserer du montering og produksjonsavgang i avanserte lagerkonfigurasjoner

Når du bokfører produksjons- eller monteringsordreavgang på et lager som bruker lagerstyring, går avgangen til hyllen som er definert i produksjons- eller monteringsordren. Hvis du vil lære mer om ulike måter å flytte varer på i lageret med avanserte konfigurasjoner, kan du gå til [Flytte varer i avanserte lagerkonfigurasjoner](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Du kan ikke angi kildedokumentnummeret, for eksempel produksjonsordrenummeret, i dokumentene for intern plassering, plukking eller flytting for monterings- eller produksjonsavgangsprosesser.  

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
