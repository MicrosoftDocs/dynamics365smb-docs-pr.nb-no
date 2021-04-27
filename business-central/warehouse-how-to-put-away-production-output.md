---
title: Plasser produksjonsavgang
description: Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2b04e07a6660ebeb32cc93594c77b8ff8e782766
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784220"
---
# <a name="put-away-production-or-assembly-output"></a>Plassere produksjonsavgang eller monteringsavgang

Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

I grunnleggende lageroppsett hvor lokasjonen krever plasseringsbehandling, bruker du dokumentet **Lagerplassering** til å bokføre produksjonsavgang og registrere plasseringen av avgang.  

> [!NOTE]  
> Lagerplassering støttes ikke for samlingsprosesser. Du bokfører en monteringsordre for å registrere avgang. Hvis du bruker hyller, kan du flytte varer mellom hyller senere. Hvis du vil ha mer informasjon, kan du se [Flytte varer ad hoc i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

I avanserte lageroppsett hvor lokasjonen krever både plasserings- og mottaksbehandling, kan du opprette enten et internt plasseringsdokument eller et flyttedokument for å plassere avgangen.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>Slik plasseres produksjonsavgang med lagerplassering

Det første trinnet ved opprettelse av plasseringsavgang, er å opprette den inngående lagerforespørselen. Denne forespørselen informerer lageret om at produksjons- eller monteringsordreavgangen er klar til å plasseres.

### <a name="to-create-the-inbound-warehouse-request"></a>Slik oppretter du den inngående lagerforespørselen  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  
2.  På produksjonsordren som er klar til plassering, velger du handlingen **Opprett inngående lagerforespørsel**.  

> [!NOTE]  
> Du kan også opprette den inngående lagerforespørselen ved å velge feltet **Opprett inngående foresp.** når du fornyer produksjonsordren. Hvis du vil ha mer informasjon, se [Fornye eller planlegge produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>Slik plasseres varer med lagerplassering  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplassering**, og velg deretter den relaterte koblingen.  
2.  Opprett en ny lagerplassering. Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Du får tilgang til produksjonsordreavgang ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
4.  Fyll ut plasseringslinjene.
5.  Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføringen vil opprette de nødvendige lagerpostene og bokføre avgangen av varene.  

Du kan også opprette en **Lagerplassering** direkte fra den frigitte produksjonsordren. Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Når du bokfører en lagerplassering, antas det at alle operasjonene bokføres i henhold til standardruten, det vil si at avgangsantall bokføres i henhold til den siste operasjonen. Du kan bruke ferdigmeldingskladden til å bokføre avvik i avgangsantall og oppstillingstid og operasjonstid. Hvis det er nødvendig å bokføre delvis etter at du har opprettet lagerplasseringen, kan du gjøre dette for oppstillingstider og antall for alle operasjoner bortsett fra den siste. I dette tilfellet styres den siste operasjonen av lagerplasseringen.  

Hvis du bare trenger å bokføre oppsett eller kjøretid i den siste operasjonen, kan du sette avgangsantallet i den siste operasjonen til 0. Du kan også velge ikke å bokføre den siste linjen i det hele tatt ved å slette den.  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Slik plasserer du monterings- og produksavgang i avanserte lagerkonfigurasjoner
Når du bokfører avgangen for produksjons- eller monteringsordrer i lageret som er definert til å bruke dirigert plassering og plukking, plasseres avgangen i hyllen som er definert i produksjons- eller monteringsordren. 

Tabellen nedenfor beskriver ulike måter å flytte varer på i lageret med avanserte konfigurasjoner der alle lageraktiviteter må utføres i en styrt arbeidsflyt. 

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytt varer med lagerflytteforslaget.|[Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Opprett en intern plassering for å plassere produserte eller monterte varer i et avansert lageroppsett.|[Opprett en intern plassering](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Du kan ikke angi kildedokumentnummeret, for eksempel produksjonsordrenummeret, i dokumentene for intern plassering, plukking eller plassering for noen av disse prosedyrene.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
