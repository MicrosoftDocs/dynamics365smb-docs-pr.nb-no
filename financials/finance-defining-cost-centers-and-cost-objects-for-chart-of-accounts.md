---
title: Definere kostsentre og kostobjekter for kontoplanen | Microsoft-dokumentasjon
description: "Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel. Når du foretar overføringen, overfører systemet bare postene som allerede er koblet til et kostsenter eller et kostobjekt. Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definere kostsentre og kostobjekter for kontoplanen
Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel. Når du foretar overføringen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bare postene som allerede er koblet til et kostsenter eller et kostobjekt. Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definere standard dimensjonsverdier for finanskontoer  
For hver finanskonto kan du definere standarddimensjonsverdier i **Standarddimensjon**-tabellen. Eksempelet nedenfor viser hvordan du definerer at det alltid skal finnes et kostsenter for AVDELING, men aldri et kostobjekt for PROSJEKT, ved bokføring til en finanskonto.  

|**Dimensjonskode**|**Verdibokføring**|  
|------------------------------------------|-----------------------------------------|  
|Avdeling|Obligatorisk kode|  
|Prosjekt|Ingen kode|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definere dimensjonsverdier for indirekte kostnader og direkte kostnader  
 Du kan overføre indirekte kostnader til et kostsenter og direkte kostnader til et kostobjekt. Følgende tabell viser den optimale kombinasjonen av dimensjonsoppsettsverdier.  

|Overfør til|Kostsenterbokføring|Bokføring av kostobjekt|  
|-----------------|-------------------------|-------------------------|  
|Kostsenter|Obligatorisk kode|Ingen kode|  
|Kostobjekt|Ingen kode|Obligatorisk kode|  

> [!NOTE]  
>  For å sørge for at det forhåndsdefinerte kostsenteret og kostobjekt som du setter opp i finans, overføres automatisk til kostregnskapet, kan du merke av for **Kontroller finansbokføringer** i vinduet Kostregnskapsoppsett.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Definere kostsentre](finance-how-to-set-up-cost-centers.md)   
[Definere kostobjekter](finance-how-to-set-up-cost-objects.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

