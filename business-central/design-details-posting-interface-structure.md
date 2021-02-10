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
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="8b785-103">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="8b785-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="8b785-104">I strukturen til bokføringsgrensesnittet i [!INCLUDE[prod_short](includes/prod_short.md)] er det flere globale prosedyrer der samme struktur brukes:</span><span class="sxs-lookup"><span data-stu-id="8b785-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="8b785-105">RunWithCheck og RunWithoutCheck kaller prosedyrekode – generisk bokføringsgrensesnitt for</span><span class="sxs-lookup"><span data-stu-id="8b785-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="8b785-106">finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="8b785-106">Jnl Line.</span></span>  
* <span data-ttu-id="8b785-107">CustPostApplyCustLedgEntry – bokfør kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster.</span><span class="sxs-lookup"><span data-stu-id="8b785-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8b785-108">VendPostApplyVendLedgEntry – bokfør leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster.</span><span class="sxs-lookup"><span data-stu-id="8b785-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="8b785-109">UnapplyCustLedgEntry – bokfør oppheving av kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster</span><span class="sxs-lookup"><span data-stu-id="8b785-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="8b785-110">UnapplyVendLedgEntry – bokfør oppheving av leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster</span><span class="sxs-lookup"><span data-stu-id="8b785-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b785-111">Se også</span><span class="sxs-lookup"><span data-stu-id="8b785-111">See Also</span></span>  
[<span data-ttu-id="8b785-112">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="8b785-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)