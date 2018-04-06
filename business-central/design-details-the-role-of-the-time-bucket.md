---
title: "Designdetaljer – Rollen til tidsperioden | Microsoft-dokumentasjon"
description: "Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre."
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
ms.openlocfilehash: 099465f0ef7bdafa3df80c377cd83b177bb68072
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Designdetaljer: Rollen til tidsperioden
Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre.  
  
 Du kan angi en tidsperiode for gjenbestillingsprinsipper som bruker et gjenbestillingspunkt. Dette sikrer at behov i samme tidsperiode akkumuleres før virkningen på den beregnede beholdningen kontrolleres, og før det kontrolleres om gjenbestillingspunktet er overskredet. Hvis gjenbestillingspunktet er overskredet, blir det planlagt en ny forsyningsordre fremover fra slutten av perioden som er angitt av tidsperioden. Tidsperiodene begynner på den planlagte startdatoen.  
  
 Tidsperiodebegrepet gjenspeiler den manuelle fremgangsmåten for å kontrollere lagernivået hyppig i stedet for ved hver transaksjon. Brukeren må angi frekvensen (tidsperioden). Brukeren samler for eksempel inn alle behov fra én leverandør for å registrere en ukentlig ordre.  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 Tidsperioden brukes vanligvis til å unngå en kaskadeeffekt. Det opprettes for eksempel en balansert rad av behov og forsyning der et tidlig behov blir avbrutt, eller det opprettes en ny. Resultatet blir at hver forsyningsordre (unntatt den siste) tidsplanlegges på nytt.  
  
## <a name="see-also"></a>Se også  
 [Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
 [Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
 [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
