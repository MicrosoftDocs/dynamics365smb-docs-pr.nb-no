---
title: Massebokføre forbruk | Microsoft-dokumentasjon
description: Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9200256cec074e547bc594950b1eb2d975a8ad9b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877886"
---
# <a name="batch-post-production-consumption"></a>Massebokføre produksjonsforbruk
Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.

Du kan også definere at systemet automatisk skal bokføre (*utføre lagertrekk*) komponenter når du starter eller ferdigstiller produksjonsordrer. Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Slik bokfører du forbruk for en eller flere produksjonsordrelinjer  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forbrukskladd**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene med produksjonsordre- og forbruksinformasjonen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Hvis lagerlokasjonen der komponentene er lagret er definert for å bruke hyller, men ikke krever plukkbehandling, tildeler du en hyllekode til kladdelinjen for å vise hvor varene skal tas fra på lageret. Hvis du vil ha mer informasjon, kan du se [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md).  
3.  Velg handlingen **Bokfør** for å bokføre forbruket. De relaterte varepostene reduseres.

## <a name="see-also"></a>Se også  
[Produksjon](production-manage-manufacturing.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
