---
title: Definere kontoplanen| Microsoft-dokumentasjon
description: Du kan endre standardkontoene i kontoplanen, og du kan legge til nye kontoer.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d4a8d4482999ed9d622d73654c3d8a4c3d8394
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="6c049-103">Definere eller endre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="6c049-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="6c049-104">Kontoplanen viser finanskontoene som lagrer dine økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="6c049-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="6c049-105"> inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.</span><span class="sxs-lookup"><span data-stu-id="6c049-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="6c049-106">Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.</span><span class="sxs-lookup"><span data-stu-id="6c049-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="6c049-107">Legge til eller endre kontoer</span><span class="sxs-lookup"><span data-stu-id="6c049-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="6c049-108">For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger.</span><span class="sxs-lookup"><span data-stu-id="6c049-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6c049-109">Du kan slette en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="6c049-109">You can delete a general ledger account.</span></span> <span data-ttu-id="6c049-110">Før du sletter den, må imidlertid følgende være oppfylt:</span><span class="sxs-lookup"><span data-stu-id="6c049-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="6c049-111">Saldo på kontoen må være null.</span><span class="sxs-lookup"><span data-stu-id="6c049-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="6c049-112">Feltet **Tillat sletting av finanskto. før** må være satt i vinduet **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.</span><span class="sxs-lookup"><span data-stu-id="6c049-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="6c049-113">Hvis feltet **Kontroller finanskontobruk** er valgt i vinduet **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="6c049-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="6c049-114"> hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="6c049-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6c049-115">Se også</span><span class="sxs-lookup"><span data-stu-id="6c049-115">See Also</span></span>
[<span data-ttu-id="6c049-116">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="6c049-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="6c049-117">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="6c049-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="6c049-118">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="6c049-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="6c049-119">Importere data fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="6c049-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="6c049-120">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6c049-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

