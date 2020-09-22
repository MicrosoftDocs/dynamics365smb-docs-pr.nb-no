---
title: Designdetaljer – Kostkomponenter | Microsoft-dokumentasjon
description: Kostkomponenter er ulike typer kostnader som utgjør verdien av en lagerøkning eller -reduksjon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 639a982c81b29a2a51f24551d9c0814f7a3ac1c5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788049"
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
