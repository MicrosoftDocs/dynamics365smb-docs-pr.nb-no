---
title: Angi filtre for dynamisk fordelingsgrunnlag | Microsoft-dokumentasjon
description: "Metoden for dynamisk fordeling er basert på verdier som kan endres. Eksempel: Antall ansatte i et kostsenter eller solgte varer av et kostobjekt i en bestemt tidsperiode. Det finnes ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller. Du angir ulike filtre basert på fordelingsgrunnlaget."
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
ms.openlocfilehash: 317e924f3297946f3d933cecf21593f0791ebec0
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Angi filtre for dynamisk fordelingsgrunnlag
Metoden for dynamisk fordeling er basert på verdier som kan endres. Eksempel: Antall ansatte i et kostsenter eller solgte varer av et kostobjekt i en bestemt tidsperiode. Det finnes ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller. Du angir ulike filtre basert på fordelingsgrunnlaget.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Angi filtre for dynamisk fordelingsgrunnlag  
 Tabellen nedenfor viser hvilke filtre som kan brukes for ulike fordelingsgrunnlag og hvilke verdier som er gyldige i feltene **Nr.filter** og **Gruppefilter**. Trykk på F1 i **Datofilterkode**-feltet for å lese detaljerte beskrivelser.  

|**Base**|**Nr.filter**|**Datofilterkode**|**Kostsenterfilter**|**Kostobjektfilter**|**Gruppefilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Finansposter|Finanskonto|Ja|Ja|Ja|I/T|  
|Budsjettposter|Finanskonto|Ja|Ja|Ja|Budsjettnavn|  
|Kosttypeposter|Kosttype|Ja|Ja|Ja|I/T|  
|Kostbudsjettposter|Kosttype|Ja|Ja|Ja|Budsjettnavn|  
|Antall ansatte|I/T|Ja|Ja|Ja|I/T|  
|Solgte varer (antall)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Kjøpte varer (antall)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Solgte varer (beløp)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  
|Kjøpte varer (beløp)|Varenr.|Ja|Ja|Ja|Bokføringsgruppe - lager|  

## <a name="see-also"></a>Se også  
 [Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definere og fordele kostnader](finance-define-and-allocate-costs.md)

