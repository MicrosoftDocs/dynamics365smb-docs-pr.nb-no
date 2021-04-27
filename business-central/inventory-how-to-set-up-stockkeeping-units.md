---
title: Definere lagerføringsenheter | Microsoft-dokumentasjon
description: Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 18923708fdad1b88714d2dcb2c61bfd2e4259f4b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785720"
---
# <a name="set-up-stockkeeping-units"></a>Definere lagerføringsenheter
Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.  

 Lagerføringsenheter er et tillegg til varekort. De erstatter dem ikke, selv om de er knyttet til dem. Med lagerføringsenheter kan du skille mellom opplysninger om en vare for en bestemt lokasjon (for eksempel et lager eller et distribusjonssenter) eller en bestemt variant (for eksempel ulike hyllenumre og ulike opplysninger om etterfylling), for den samme varen.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Slik definerer du lagerføringsenheter  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.  
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
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]