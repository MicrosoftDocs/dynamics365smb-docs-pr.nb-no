---
title: Opprette kostbudsjetter | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over hvor du kan opprette og analysere kostbudsjetter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: da976e1e8ac2988aa2842925c2b10f4f8515ea47
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785247"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="0af92-103">Opprette kostbudsjetter</span><span class="sxs-lookup"><span data-stu-id="0af92-103">Creating Cost Budgets</span></span>
<span data-ttu-id="0af92-104">Budsjettering i kostregnskap ligner budsjettering i finans.</span><span class="sxs-lookup"><span data-stu-id="0af92-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="0af92-105">Et kostnadsbudsjett opprettes basert på kostnadstyper på samme måte som et finansbudsjett opprettes basert på finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="0af92-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="0af92-106">Et kostnadsbudsjett opprettes for en bestemt tidsperiode, for eksempel et regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="0af92-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="0af92-107">Du kan opprette så mange kostbudsjetter som nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0af92-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="0af92-108">Du kan opprette et nytt kostbudsjett manuelt, ved å importere et kostbudsjett eller ved å kopiere et eksisterende kostbudsjett som grunnlag for budsjettet.</span><span class="sxs-lookup"><span data-stu-id="0af92-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="0af92-109">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="0af92-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="0af92-110">Du kan bruke følgende sider til å opprette og analysere kostbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="0af92-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="0af92-111">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") for å finne en side, og les deretter verktøytipset for hvert vindu.</span><span class="sxs-lookup"><span data-stu-id="0af92-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="0af92-112">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="0af92-112">To</span></span>|<span data-ttu-id="0af92-113">Se</span><span class="sxs-lookup"><span data-stu-id="0af92-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="0af92-114">Overfør budsjetter fra finans.</span><span class="sxs-lookup"><span data-stu-id="0af92-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="0af92-115">Kjørselen **Kopier finansbudsjett til kostregnskap**</span><span class="sxs-lookup"><span data-stu-id="0af92-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="0af92-116">Kopier kostbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="0af92-116">Copy cost budgets.</span></span>|<span data-ttu-id="0af92-117">Kjørselen **Kopier kostbudsjett**</span><span class="sxs-lookup"><span data-stu-id="0af92-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="0af92-118">Tildele budsjetter.</span><span class="sxs-lookup"><span data-stu-id="0af92-118">Allocate budgets.</span></span>|<span data-ttu-id="0af92-119">Siden **Kostfordeling**</span><span class="sxs-lookup"><span data-stu-id="0af92-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="0af92-120">Se kostbudsjettjournaler og kostbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="0af92-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="0af92-121">Siden **Kostbudsjettjournaler**</span><span class="sxs-lookup"><span data-stu-id="0af92-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="0af92-122">Skrive ut budsjettsammenligninger ved hjelp av ulike rapporter.</span><span class="sxs-lookup"><span data-stu-id="0af92-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="0af92-123">Rapporten **Kostregnskap – saldo/budsjett**</span><span class="sxs-lookup"><span data-stu-id="0af92-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="0af92-124">Rapporten **Kostregnskap – utdrag/budsjett**</span><span class="sxs-lookup"><span data-stu-id="0af92-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="0af92-125">Rapporten **Kostbudsjett etter kostsenter**</span><span class="sxs-lookup"><span data-stu-id="0af92-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="0af92-126">Rapporten **Kostbudsjett etter kostobjekt**</span><span class="sxs-lookup"><span data-stu-id="0af92-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="0af92-127">Se også</span><span class="sxs-lookup"><span data-stu-id="0af92-127">See Also</span></span>  
[<span data-ttu-id="0af92-128">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="0af92-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="0af92-129">Opprette finansbudsjetter</span><span class="sxs-lookup"><span data-stu-id="0af92-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="0af92-130">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="0af92-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="0af92-131">Definere og fordele kostnader</span><span class="sxs-lookup"><span data-stu-id="0af92-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="0af92-132">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0af92-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]