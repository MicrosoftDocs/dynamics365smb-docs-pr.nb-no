---
title: Definere forholdet mellom kostnadstyper og finanskontoer | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer relasjonen mellom kosttypen og finanskontoen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: c5b4549e330bd9b3369b6fe5b18361f6662291c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "918033"
---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definere forholdet mellom kostnadstyper og finanskontoer
Forholdet mellom kosttypen og finanskontoen opprettes i kosttypen og finanskontoen.  

* Feltet **Finanskto. fra/til** i **Kosttype**-tabellen angir hvilke finanskontoer som tilhører en kostnadstype.  
* Feltet **Kosttypenr.** i kontoplanen angir hvilken kostnadstype en finanskontoer tilhører.  

Disse to feltene er automatisk utfylt når du bruker funksjonen **Hent kosttyper fra kontoplan**.  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Forhold mellom finanskontoer og kostnadstyper  
Det er et n:1-forhold mellom finanskonti og kosttyper. Flere finanskontoer kan tilhøre én kosttype, men hver finanskonto tilhører bare én kosttype. Tabellen nedenfor beskriver detaljene om forholdet.  

|Forbindelser|**Finanskto. fra/til**|**Kosttypenr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Én finanskonto for hver kosttype|Én finanskonto|En kosttype|  
|Flere finanskontoer for én kosttype.|Finanskontoområdet, for eksempel 7110–7193 for hver finanskonto|For hver finanskonto i området er det bare én kosttype|  
|Kosttyper uten tilsvarende finanskontoer|<Empty>||  
|Finanskonti der poster ikke overføres||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kosttyper uten en relasjon til finans  
En kostnadstype kan ikke ha en relasjon til finanskontoer hvis én av følgende betingelser er oppfylt:  

* Kontoer for driftsregnskap, for eksempel beregnede renter og avskrivning, tar bare kostnader fra driftsregnskapet.  
* Hjelpekosttyper, for eksempel kosttypene 9901, 9902 og 9903 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, brukes som kredit- og debetkontoer for fordelinger.  
* Hjelpekontoen, 9920 i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen, inneholder faktiske avsetninger som viser differansen mellom kost og utgiftene fra Finans.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Definere kost.regnskap](finance-set-up-cost-accounting.md)   
[Om kostregnskap](finance-about-cost-accounting.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
