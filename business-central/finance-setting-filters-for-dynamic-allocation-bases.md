---
title: Angi filtre for dynamisk fordelingsgrunnlag | Microsoft-dokumentasjon
description: 'Metoden for dynamisk fordeling er basert på verdier som kan endres. Eksempel: Antall ansatte i et kostsenter eller solgte varer av et kostobjekt i en bestemt tidsperiode. Det finnes ni forhåndsdefinerte fordelingsgrunnlag og tolv dynamiske datointervaller. Du angir ulike filtre basert på fordelingsgrunnlaget.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241965"
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
[Definere og fordele kostnader](finance-define-and-allocate-costs.md)
