---
title: Overføre finansposter til kostposter | Microsoft-dokumentasjon
description: Du kan overføre finansposter til kostposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803575"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Overføre finansposter til kostposter
Du kan overføre finansposter til kostposter.  

Før du kjører prosessen for overføring av finansposter til kostposter, må du klargjøre overføringen for å unngå manuell korrigeringsbokføring.  

## <a name="to-prepare-the-transfer"></a>Klargjøre overføringen  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostregnskapsoppsett**, og velg deretter den relaterte koblingen.  
2.  På siden **Kostregnskapsoppsett** kontrollerer du at feltet **Startdato for finansoverføring** er satt til den riktige verdien.  
3.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.  
4.  Kontroller at feltet **Finanskto. fra/til** på siden **Kosttypekort** er riktig koblet for hver kosttype, slik at poster hentes fra finans.  
5.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoplan**, og velg deretter den relaterte koblingen.  
6.  For hver relevant finanskonto på **Finanskort-siden** kontrollerer du at **Kosttypenr.** -feltet er riktig tilknyttet en kostnadstype. Hvis du vil ha mer informasjon, kan du se [Definere kostregnskap](finance-set-up-cost-accounting.md).  
7.  Kontroller at alle relevante finansposter har dimensjonsverdier som svarer til et kostsenter og et kostobjekt.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Slik overfører du finansposter til kostposter:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overfør finansposter til KR**, og velg deretter den relaterte koblingen.  
2.  Velg **Ja**-knappen for å starte overføringen. Prosessen overfører alle finansposter som ikke allerede er overført.  

    Under overføringen oppretter prosessen forbindelser i postene i tabellen **Kostpost** og i tabellen **Kostjournal**. Dette gjør det mulig å spore kilden til kostposter.  

## <a name="see-also"></a>Se også  
[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
[Definere kostregnskap](finance-set-up-cost-accounting.md)   
