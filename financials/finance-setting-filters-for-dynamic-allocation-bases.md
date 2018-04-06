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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cd6aaf4ca0c1de1cea400ce5abe434f7c37040f9
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

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

