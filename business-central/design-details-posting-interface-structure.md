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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7600e8ebfee6b6eda6f872b0de2f4c8238338340
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880091"
---
# <a name="design-details-posting-interface-structure"></a>Designdetaljer: Strukturen til bokføringsgrensesnittet
I strukturen til bokføringsgrensesnittet i [!INCLUDE[d365fin](includes/d365fin_md.md)] er det flere globale prosedyrer der samme struktur brukes:  
  
* RunWithCheck og RunWithoutCheck kaller prosedyrekode – generisk bokføringsgrensesnitt for finanskladdelinje.  
* CustPostApplyCustLedgEntry – bokfør kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster.  
* VendPostApplyVendLedgEntry – bokfør leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster.  
* UnapplyCustLedgEntry – bokfør oppheving av kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster  
* UnapplyVendLedgEntry – bokfør oppheving av leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Strukturen til bokføringsmotoren](design-details-posting-engine-structure.md)