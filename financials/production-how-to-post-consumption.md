---
title: "Massebokføre forbruk | Microsoft-dokumentasjon"
description: "Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 29e85f5264f007db3712d4f6227d689b2a3de926
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-production-consumption"></a>Massebokføre produksjonsforbruk
Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.

Du kan også definere at systemet automatisk skal bokføre (*utføre lagertrekk*) komponenter når du starter eller ferdigstiller produksjonsordrer. Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Slik bokfører du forbruk for en eller flere produksjonsordrelinjer  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forbrukskladd**, og velg deretter den relaterte koblingen.  
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

