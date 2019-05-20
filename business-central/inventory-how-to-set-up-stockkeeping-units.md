---
title: Definere lagerføringsenheter | Microsoft-dokumentasjon
description: Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 50bf3695a135652ec422bb187f1ff2fef06f3a35
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239386"
---
# <a name="set-up-stockkeeping-units"></a>Definere lagerføringsenheter
Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.  

 Lagerføringsenheter er et tillegg til varekort. De erstatter dem ikke, selv om de er knyttet til dem. Med lagerføringsenheter kan du skille mellom opplysninger om en vare for en bestemt lokasjon (for eksempel et lager eller et distribusjonssenter) eller en bestemt variant (for eksempel ulike hyllenumre og ulike opplysninger om etterfylling), for den samme varen.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Slik definerer du lagerføringsenheter  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Fyll ut feltene på kortet. Følgende felt er obligatoriske: **Varenr.**, **Lokasjonskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har definert den første lagerføringsenheten for en vare, blir det merket av for **Lagerføringsenhet** på **vare** kortet.  

Hvis du vil opprette flere lagerføringsenheter for en vare, bruker du kjørselen **Opprett lagerføringsenhet**.  

> [!NOTE]  
>  Opplysningene på **lagerføringsenhetskortet** har høyere prioritet enn opplysningene på **varekortet**.

> [!Warning]
> Hvis LFE angis via produksjon, brukes ikke **Kostpris (standard)**-feltet når faktisk kost for den produserte varen faktureres og justeres. I stedet brukes **Kostpris (standard)**-feltet på det underliggende varekortet, og eventuelle avvik beregnes mot kostandelene for denne varen.<br /><br />
> Siden produksjonsstykklister og ruting ikke kan tilordnes til LFEer, er heller ikke opprulling av enhetskost og den relaterte beregningen av kostandeler tilgjengelig på LFEer. Hvis du vil ha mer informasjon, kan du se [Om beregning av standardkost](finance-about-calculating-standard-cost.md).

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
