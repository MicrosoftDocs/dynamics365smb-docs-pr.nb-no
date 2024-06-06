---
title: Designdetaljer – Strukturen til bokføringsgrensesnittet
description: Dette emnet gir en oversikt over de globale fremgangsmåtene og designdetaljene i strukturen til bokføringsgrensesnittet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
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

[!INCLUDE[footer-include](includes/footer-banner.md)]
