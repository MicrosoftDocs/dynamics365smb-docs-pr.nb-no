---
title: Bruke vareserier i produksjon | Microsoft-dokumentasjon
description: Hovedoppgaven med å tilpasse en hovedkalender for selskapet, eller selskapets forretningspartner, er å angi eventuelle endringer i statusen for arbeids- eller fridager.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9d0b27a1bdcc2aa544c50cf9993d46405f519b0c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787605"
---
# <a name="work-with-production-families"></a>Arbeide med produksjonsfamilier
En produksjonsfamilie er en gruppe individuelle varer der forbindelsen er basert på likheten i produksjonsprosessen. Ved hjelp av produksjonsfamilier kan noen varer produseres to eller flere ganger i én produksjon, noe som optimaliserer materialforbruket.

I **Antall**-feltet på **Familie**-siden angir du antallet som skal produseres når hele familien er produsert én gang.

## <a name="example"></a>Eksempel
I utstansingsprosesser kan fire enheter av samme vare produseres fra ett ark, samtidig med 10 enheter av en annen, forskjellig vare. Utstansingsmaskinen utstanser alle de 14 enhetene i én operasjon.

Når du definerer produksjonsfamilier, reduseres vrakantallet, fordi det som vanligvis ville blitt overflødig vrak ved produksjon av store enheter, i stedet brukes til å produsere små varer.

## <a name="to-set-up-a-production-family"></a>Slik konfigurerer du produksjonsfamilier
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Familier**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Produsere basert på en produksjonsfamilie
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.
2. Opprett en ny produksjonsordre. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).
3. Velg **Familie** i **Kildetype**-feltet.  
4. Velg den aktuelle produksjonsfamilien i **Kildenr.**-feltet.

## <a name="see-also"></a>Se også
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]