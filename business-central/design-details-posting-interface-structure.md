---
title: Designdetaljer – Strukturen til bokføringsgrensesnittet | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over de globale fremgangsmåtene i strukturen til bokføringsgrensesnittet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e306b0caeb58bfe7bd04f93ac64d8b593f70f695
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751258"
---
# <a name="design-details-posting-interface-structure"></a>Designdetaljer: Strukturen til bokføringsgrensesnittet
I strukturen til bokføringsgrensesnittet i [!INCLUDE[prod_short](includes/prod_short.md)] er det flere globale prosedyrer der samme struktur brukes:  
  
* RunWithCheck og RunWithoutCheck kaller prosedyrekode – generisk bokføringsgrensesnitt for finanskladdelinje.  
* CustPostApplyCustLedgEntry – bokfør kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster.  
* VendPostApplyVendLedgEntry – bokfør leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster.  
* UnapplyCustLedgEntry – bokfør oppheving av kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster  
* UnapplyVendLedgEntry – bokfør oppheving av leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Strukturen til bokføringsmotoren](design-details-posting-engine-structure.md)