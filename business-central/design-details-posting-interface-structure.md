---
title: Designdetaljer – Strukturen til bokføringsgrensesnittet
description: Dette emnet gir en oversikt over de globale fremgangsmåtene og designdetaljene i strukturen til bokføringsgrensesnittet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: edupont
---
# Designdetaljer: Strukturen til bokføringsgrensesnittet
I strukturen til bokføringsgrensesnittet i [!INCLUDE[prod_short](includes/prod_short.md)] er det flere globale prosedyrer der samme struktur brukes:  
  
* RunWithCheck og RunWithoutCheck kaller prosedyrekode – generisk bokføringsgrensesnitt for finanskladdelinje.  
* CustPostApplyCustLedgEntry – bokfør kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster.  
* VendPostApplyVendLedgEntry – bokfør leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster.  
* UnapplyCustLedgEntry – bokfør oppheving av kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster  
* UnapplyVendLedgEntry – bokfør oppheving av leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster  
  
## Se også  
[Designdetaljer: Strukturen til bokføringsmotoren](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]