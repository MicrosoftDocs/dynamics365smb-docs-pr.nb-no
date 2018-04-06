---
title: "Overføre finansposter til kostposter | Microsoft-dokumentasjon"
description: "Du kan overføre finansposter til kostposter."
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
ms.openlocfilehash: cd52387ec1396164f6da1b87a2a97227901df592
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Overføre finansposter til kostposter
Du kan overføre finansposter til kostposter.  

Før du kjører prosessen for overføring av finansposter til kostposter, må du klargjøre overføringen for å unngå manuell korrigeringsbokføring.  

## <a name="to-prepare-the-transfer"></a>Klargjøre overføringen  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kostregnskapsoppsett**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Kostregnskapsoppsett** kontrollerer du at feltet **Startdato for finansoverføring** er satt til den riktige verdien.  
3.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.  
4.  Kontroller at feltet **Finanskto. fra/til** i vinduet **Kosttypekort** er riktig koblet for hver kosttype, slik at poster hentes fra finans.  
5.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
6.  For hver relevant finanskonto i **Finanskort-vinduet** kontrollerer du at **Kosttypenr.** -feltet er riktig tilknyttet en kostnadstype. Hvis du vil ha mer informasjon, kan du se [Definere forholdet mellom kostnadstyper og finanskontoer](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)  
7.  Kontroller at alle relevante finansposter har dimensjonsverdier som svarer til et kostsenter og et kostobjekt.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Slik overfører du finansposter til kostposter:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Overfør finansposter til KR**, og velg deretter den relaterte koblingen.  
2.  Velg **Ja**-knappen for å starte overføringen. Prosessen overfører alle finansposter som ikke allerede er overført.  

    Under overføringen oppretter prosessen forbindelser i postene i tabellen **Kostpost** og i tabellen **Kostjournal**. Dette gjør det mulig å spore kilden til kostposter.  

## <a name="see-also"></a>Se også  
 [Kriterier for overføring av finansposter til kostposter](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Automatisk overføring og sammensatte poster](finance-automatic-transfer-combined-entries.md)   
 [Resultater av overføringen](finance-results-of-the-transfer.md)   
 [Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
 [Definere forholdet mellom kostnadstyper og finanskontoer](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

