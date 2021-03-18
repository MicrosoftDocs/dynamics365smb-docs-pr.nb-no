---
title: Definere kontoplanen
description: Du kan endre standardkontoene i kontoplanen, og du kan legge til nye kontoer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f14859a641ddf6368a213f396a111a3423f49c4a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377115"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="1c3eb-103">Definere eller endre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="1c3eb-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="1c3eb-104">Kontoplanen viser finanskontoene som lagrer dine økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1c3eb-105">inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="1c3eb-106">Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="1c3eb-107">Legge til eller endre kontoer</span><span class="sxs-lookup"><span data-stu-id="1c3eb-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="1c3eb-108">For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1c3eb-109">Du kan slette en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-109">You can delete a general ledger account.</span></span> <span data-ttu-id="1c3eb-110">Før du sletter den, må imidlertid følgende være oppfylt:</span><span class="sxs-lookup"><span data-stu-id="1c3eb-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="1c3eb-111">Saldo på kontoen må være null.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="1c3eb-112">Feltet **Tillat sletting av finanskto. før** må være satt på siden **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="1c3eb-113">Hvis feltet **Kontroller finanskontobruk** er valgt på siden **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1c3eb-114">hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="1c3eb-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="1c3eb-115">Se relatert opplæring på [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="1c3eb-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="1c3eb-116">Se også</span><span class="sxs-lookup"><span data-stu-id="1c3eb-116">See Also</span></span>
[<span data-ttu-id="1c3eb-117">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="1c3eb-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="1c3eb-118">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="1c3eb-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="1c3eb-119">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="1c3eb-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="1c3eb-120">Importere data fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="1c3eb-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="1c3eb-121">Arbeide med kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="1c3eb-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="1c3eb-122">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1c3eb-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]