---
title: Om lagerkost | Microsoft-dokumentasjon
description: Administrering av lagerkost handler om å registrere og rapportere forretningsdriftskost. Det inkluderer rapportering av produksjonskost og lagerkost, det vil si verdien av varene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 89769cf8ad8299c32805bf15b1cc447dac8beabc
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803242"
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
|Forstå hvordan lagerverdien gjenspeiles i Finans.|[Rapportere kostnader og avstemme med Finans](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|Lære hvordan varegebyrer, for eksempel frakt og forsikring, kan tilordne tilleggskostkomponenter til en vares enhetskost.|[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)|  
|Lese hvordan lagerperioder hjelper et selskap med å styre lagerverdi over tid ved å definere kortere perioder som kan lukkes for bokføring underveis i regnskapsåret.|[Arbeide med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Forstå alle mekanismene i kostmotoren, inkludert hva som skjer når du bokfører transaksjoner for montering og produksjon.|[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)|

## <a name="see-also"></a>Se også
[Administrere lagerkostnader](finance-manage-inventory-costs.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
