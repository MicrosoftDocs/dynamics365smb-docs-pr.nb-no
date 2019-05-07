---
title: Resultater av overføringen | Microsoft-dokumentasjon
description: Dette emnet beskriver hva som skjer når du overfører finansposter til kostposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 590c1501f9da2c7c343b5c2f3617df873fcd3b7a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "926712"
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
[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
