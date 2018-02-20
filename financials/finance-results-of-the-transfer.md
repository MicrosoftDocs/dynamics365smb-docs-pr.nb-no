---
title: "Resultater av overføringen | Microsoft-dokumentasjon"
description: "Dette emnet beskriver hva som skjer når du overfører finansposter til kostposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d479727b8d0cbb4b4ec9f127136f4e0578b8afb7
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultater av overføring av finansposter til kostposter
Under overføring av finansposter til kostposter oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] forbindelser i postene i tabellen **Finanspost**, **Kostpri.** og **Kostjournal** for å gjøre det mulig å spore forbindelsene mellom kostposter og finansposter.  

## <a name="general-ledger-entries"></a>Finansposter  
For hver finanspost som overføres til kostregnskap, fyller [!INCLUDE[d365fin](includes/d365fin_md.md)] ut feltet **Postnr.**-feltet for kost.  

## <a name="cost-entries"></a>Kostposter  
For hver kostpost lagrer [!INCLUDE[d365fin](includes/d365fin_md.md)] postnummeret for tilsvarende finanspost i feltet **Finansløpenr.** i tabellen **Kostpri.**  

For kombinerte kostposter lagrer [!INCLUDE[d365fin](includes/d365fin_md.md)] postnummeret på den siste finansposten, som er posten med det høyeste postnummeret.  

Feltet **Finanskonto** i tabellen **Kostpri.**-tabellen inneholder nummeret på finanskontoen som kostposten kom fra.  

Når det gjelder enkeltkostposter, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bokføringsteksten fra finansposten til **Beskrivelse**-tekstfeltet. Når det gjelder kombinerte poster, viser tekstfeltet at disse postene overføres som kombinerte poster. For en kombinert post for oktober i 2013 kan for eksempel teksten være **Kombinerte poster, oktober 2013**.  

## <a name="cost-register"></a>Kostjournal  
I **Kostjournal**-tabellen oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] en post med kildeoverføringen fra finans. Posten registrerer det første og det siste løpenummeret for finanspostene som overføres, i tillegg til det første og det siste løpenummeret for kostpostene som opprettes.  

## <a name="see-also"></a>Se også  
[Overføre finansposter til kostposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
[Kriterier for overføring av finansposter til kostposter](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
[Automatisk overføring og sammensatte poster](finance-automatic-transfer-combined-entries.md)   
[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)  

