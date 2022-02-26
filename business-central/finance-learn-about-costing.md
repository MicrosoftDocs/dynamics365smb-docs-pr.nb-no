---
title: Om lagerkost
description: Håndtering av lagerkost handler om å registrere og rapportere kostnader for forretningskostnader, inkludert rapportering av produksjonskost og lagerkost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 36420747117425e1f66e30ed6090f300e27776f4
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325764"
---
# <a name="about-inventory-costing"></a>Om lagerkost
Administrering av lagerkost handler om å registrere og rapportere forretningsdriftskost. Det inkluderer rapportering av produksjonskost og lagerkost, det vil si verdien av varene.  

 Sentrale prinsipper å forstå er at lagermetoder definerer hvordan varer verdsettes når de forlater lageret, at kostjustering oppdaterer solgte varers kost med relatert kjøpskost bokført etter salget, og at lagerverdier må bokføres til dedikerte finanskonti ved regelmessige intervaller.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Skille mellom de fem ulike lagermetodene og virkningen de har på kostflyter.|[Designdetaljer: Kostmetoder](design-details-costing-methods.md)|  
|Lære hvordan vareutligningsposter dynamisk kobler lagerreduksjoner til økninger for å holde kontroll over kostflyter.|[Designdetaljer: Vareutligning](design-details-item-application.md)|  
|Lære hvordan enhetskost for en vare kontinuerlig oppdateres med kost for den siste transaksjonen i henhold til varens lagermetode.|[Designdetaljer: Kostjustering](design-details-cost-adjustment.md)|  
|Lære hvordan gjennomsnittskost for en vare beregnes dynamisk i henhold til den valgte gjennomsnittskostperioden.|[Designdetaljer: Gjennomsnittskost](design-details-average-cost.md)|  
|Skille forventet kost (ikke fakturert ennå) fra faktisk kost og lære hvordan dette håndteres i Finans.|[Designdetaljer: Bokføre forventet kost](design-details-expected-cost-posting.md)|  
|Forstå mekanismen for kostjustering, som sikrer at kost videreføres selv om lagertransaksjoner skjer tilfeldig.|[Designdetaljer: Kostjustering](design-details-cost-adjustment.md)|  
|Lese hvorfor standardkost ofte brukes som verdisettingsgrunnlag for komponenter og sluttvarer i produksjonsselskaper.|[Om beregning av standardkost](finance-about-calculating-standard-cost.md)|  
|Forstå hvordan lagerverdien gjenspeiles i Finans.|[Avstemme lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|Lære hvordan varegebyrer, for eksempel frakt og forsikring, kan tilordne tilleggskostkomponenter til en vares enhetskost.|[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)|  
|Lese hvordan lagerperioder hjelper et selskap med å styre lagerverdi over tid ved å definere kortere perioder som kan lukkes for bokføring underveis i regnskapsåret.|[Arbeide med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Forstå alle mekanismene i kostmotoren, inkludert hva som skjer når du bokfører transaksjoner for montering og produksjon.|[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)|  

## <a name="see-also"></a>Se også
[Administrere lagerkostnader](finance-manage-inventory-costs.md)    
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]