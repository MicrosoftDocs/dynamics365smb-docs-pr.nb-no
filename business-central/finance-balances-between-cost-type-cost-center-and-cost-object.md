---
title: Balanser mellom kosttype, kostsenter og kostobjekt | Microsoft-dokumentasjon
description: "Når du definerer kostregnskap, må du kontrollere at alle poster tilordnes en kosttype i tillegg til et kostsenter eller et kostobjekt. Dette betyr at hver kostpost må ha en kosttype tilordnet og en kostsenterkode eller et kostobjekt tilordnet. Denne regelen sikrer at hver kostpost vises i kostsentrene eller kostobjektene, men aldri på begge steder."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 31e66e98f854758ee479220803c42e61fe2d3c44
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Balanser mellom kosttype, kostsenter og kostobjekt
Når du definerer kostregnskap, må du kontrollere at alle poster tilordnes en kosttype i tillegg til et kostsenter eller et kostobjekt. Dette betyr at hver kostpost må ha en kosttype tilordnet og en kostsenterkode eller et kostobjekt tilordnet. Denne regelen sikrer at hver kostpost vises i kostsentrene eller kostobjektene, men aldri på begge steder.  

 Ved å gjøre dette oppretter du følgende regnskapsformel:  

 Kosttypesaldo = Kostsentersaldo + Kostobjektsaldo  

 Når du skriver ut rapporter for oversikten over kosttyper, diagrammet med kostsentre og diagrammet med kostobjekter, kan du analysere dette forholdet.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
 [Definere kost.regnskap](finance-set-up-cost-accounting.md)   
 [Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
 [Om kostregnskap](finance-about-cost-accounting.md)  
 [Opprette kostbudsjetter](finance-create-cost-budgets.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

