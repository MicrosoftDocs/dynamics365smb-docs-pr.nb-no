---
title: "Designdetaljer – Kostkomponenter | Microsoft-dokumentasjon"
description: "Kostkomponenter er ulike typer kostnader som utgjør verdien av en lagerøkning eller -reduksjon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e1410e2511b2f1dd27e80ea23d6e08b2b5063158
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-cost-components"></a>Designdetaljer: Kostkomponenter
Kostkomponenter er ulike typer kostnader som utgjør verdien av en lagerøkning eller -reduksjon.  

 Tabellen nedenfor viser de ulike kostnadskomponentene og eventuelle underordnede kostnadskomponenter de består av.  

|Kostkomponent|Underordnet kostkomponent|Beskrivelse|  
|--------------------|--------------------------------|---------------------------------------|  
|Direkte kostnad|Enhetskost (direktekjøpspris)|Kostnader som kan spores til et kostobjekt.|  
|Direkte kostnad|Fraktkostnader (varegebyr)|Kostnader som kan spores til et kostobjekt.|  
|Direkte kostnad|Forsikringskostnader (varegebyr)|Kostnader som kan spores til et kostobjekt.|  
|Indirekte kost||Kostnad som ikke kan spores til et kostobjekt.|  
|Avvik|Kjøpsavvik|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Avvik|Materialavvik|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Avvik|Kapasitetsavvik|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Avvik|Avvik i underleveranse|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Avvik|Avvik for indirekte kapasitetskost|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Avvik|Avvik i indirekte produksjonskostnader|Differansen mellom faktiske kostnader og standardkostnader, som bare bokføres for varer som bruker lagermetoden **Standard**.|  
|Revaluering||En nedskrivning eller oppskrivning av den aktuelle lagerverdien.|  
|Avrunding||Rest som skyldes måten verdsetting av lagerreduksjoner beregnes på.|  

> [!NOTE]  
>  Frakt- og forsikringskostnader er varegebyr som kan legges til varens kostnad når som helst. Når du kjører kjørselen **Juster kostverdi - vareposter**, oppdateres verdien til tilknyttede lagerreduksjoner tilsvarende.  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Avvik](design-details-variance.md) [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
