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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1d0130dde256706460e58e5efc445bc5f4d5c595
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="abfef-103">Definere eller endre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="abfef-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="abfef-104">Kontoplanen viser finanskontoene som lagrer dine økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="abfef-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="abfef-105"> inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.</span><span class="sxs-lookup"><span data-stu-id="abfef-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="abfef-106">Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.</span><span class="sxs-lookup"><span data-stu-id="abfef-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="abfef-107">Legge til eller endre kontoer</span><span class="sxs-lookup"><span data-stu-id="abfef-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="abfef-108">For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger.</span><span class="sxs-lookup"><span data-stu-id="abfef-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="abfef-109">Du kan slette en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="abfef-109">You can delete a general ledger account.</span></span> <span data-ttu-id="abfef-110">Før du sletter den, må imidlertid følgende være oppfylt:</span><span class="sxs-lookup"><span data-stu-id="abfef-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="abfef-111">Saldo på kontoen må være null.</span><span class="sxs-lookup"><span data-stu-id="abfef-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="abfef-112">Feltet **Tillat sletting av finanskto. før** må være satt i vinduet **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.</span><span class="sxs-lookup"><span data-stu-id="abfef-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="abfef-113">Hvis feltet **Kontroller finanskontobruk** er valgt i vinduet **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="abfef-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="abfef-114"> hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="abfef-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="abfef-115">Se også</span><span class="sxs-lookup"><span data-stu-id="abfef-115">See Also</span></span>
[<span data-ttu-id="abfef-116">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="abfef-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="abfef-117">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="abfef-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="abfef-118">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="abfef-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="abfef-119">Importere data fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="abfef-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="abfef-120">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="abfef-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

