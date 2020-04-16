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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c50f045cf1a379d4fb908e0c17d7b9775fd1a9ee
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184871"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="346ed-103">Designdetaljer: Strukturen til bokføringsgrensesnittet</span><span class="sxs-lookup"><span data-stu-id="346ed-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="346ed-104">I strukturen til bokføringsgrensesnittet i [!INCLUDE[d365fin](includes/d365fin_md.md)] er det flere globale prosedyrer der samme struktur brukes:</span><span class="sxs-lookup"><span data-stu-id="346ed-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="346ed-105">RunWithCheck og RunWithoutCheck kaller prosedyrekode – generisk bokføringsgrensesnitt for</span><span class="sxs-lookup"><span data-stu-id="346ed-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="346ed-106">finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="346ed-106">Jnl Line.</span></span>  
* <span data-ttu-id="346ed-107">CustPostApplyCustLedgEntry – bokfør kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster.</span><span class="sxs-lookup"><span data-stu-id="346ed-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="346ed-108">VendPostApplyVendLedgEntry – bokfør leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster.</span><span class="sxs-lookup"><span data-stu-id="346ed-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="346ed-109">UnapplyCustLedgEntry – bokfør oppheving av kundeutligning, kalles fra kodeenhet 226 Kundepost – utlign bokførte poster</span><span class="sxs-lookup"><span data-stu-id="346ed-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="346ed-110">UnapplyVendLedgEntry – bokfør oppheving av leverandørutligning, kalles fra kodeenhet 227 Leverandørpost – utlign bokførte poster</span><span class="sxs-lookup"><span data-stu-id="346ed-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="346ed-111">Se også</span><span class="sxs-lookup"><span data-stu-id="346ed-111">See Also</span></span>  
[<span data-ttu-id="346ed-112">Designdetaljer: Strukturen til bokføringsmotoren</span><span class="sxs-lookup"><span data-stu-id="346ed-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)