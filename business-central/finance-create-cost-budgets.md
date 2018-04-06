---
title: Opprette kostbudsjetter | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over hvor du kan opprette og analysere kostbudsjetter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ab66e5b2404f512816d1a4fcb3b110a95265e1f7
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="creating-cost-budgets"></a><span data-ttu-id="32a84-103">Opprette kostbudsjetter</span><span class="sxs-lookup"><span data-stu-id="32a84-103">Creating Cost Budgets</span></span>
<span data-ttu-id="32a84-104">Budsjettering i kostregnskap ligner budsjettering i finans.</span><span class="sxs-lookup"><span data-stu-id="32a84-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="32a84-105">Et kostnadsbudsjett opprettes basert på kostnadstyper på samme måte som et finansbudsjett opprettes basert på finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="32a84-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="32a84-106">Et kostnadsbudsjett opprettes for en bestemt tidsperiode, for eksempel et regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="32a84-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="32a84-107">Du kan opprette så mange kostbudsjetter som nødvendig.</span><span class="sxs-lookup"><span data-stu-id="32a84-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="32a84-108">Du kan opprette et nytt kostbudsjett manuelt, ved å importere et kostbudsjett eller ved å kopiere et eksisterende kostbudsjett som grunnlag for budsjettet.</span><span class="sxs-lookup"><span data-stu-id="32a84-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="32a84-109">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="32a84-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="32a84-110">Du kan bruke følgende vinduer til å opprette og analysere kostbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="32a84-110">You use the following windows to create and analyze cost budgets.</span></span> <span data-ttu-id="32a84-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport") for å finne et vindu, og les deretter verktøytipset for hvert.</span><span class="sxs-lookup"><span data-stu-id="32a84-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon to find a window, and then read the tooltip for each.</span></span>

|<span data-ttu-id="32a84-112">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="32a84-112">To</span></span>|<span data-ttu-id="32a84-113">Se</span><span class="sxs-lookup"><span data-stu-id="32a84-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="32a84-114">Overfør budsjetter fra finans.</span><span class="sxs-lookup"><span data-stu-id="32a84-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="32a84-115">Kjørselen **Kopier finansbudsjett til kostregnskap**</span><span class="sxs-lookup"><span data-stu-id="32a84-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="32a84-116">Kopier kostbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="32a84-116">Copy cost budgets.</span></span>|<span data-ttu-id="32a84-117">Kjørselen **Kopier kostbudsjett**</span><span class="sxs-lookup"><span data-stu-id="32a84-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="32a84-118">Tildele budsjetter.</span><span class="sxs-lookup"><span data-stu-id="32a84-118">Allocate budgets.</span></span>|<span data-ttu-id="32a84-119">Siden **Kostfordeling**</span><span class="sxs-lookup"><span data-stu-id="32a84-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="32a84-120">Se kostbudsjettjournaler og kostbudsjettposter.</span><span class="sxs-lookup"><span data-stu-id="32a84-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="32a84-121">Siden **Kostbudsjettjournaler**</span><span class="sxs-lookup"><span data-stu-id="32a84-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="32a84-122">Skrive ut budsjettsammenligninger ved hjelp av ulike rapporter.</span><span class="sxs-lookup"><span data-stu-id="32a84-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="32a84-123">Rapporten **Kostregnskap – saldo/budsjett**</span><span class="sxs-lookup"><span data-stu-id="32a84-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="32a84-124">Rapporten **Kostregnskap – utdrag/budsjett**</span><span class="sxs-lookup"><span data-stu-id="32a84-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="32a84-125">Rapporten **Kostbudsjett etter kostsenter**</span><span class="sxs-lookup"><span data-stu-id="32a84-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="32a84-126">Rapporten **Kostbudsjett etter kostobjekt**</span><span class="sxs-lookup"><span data-stu-id="32a84-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="32a84-127">Se også</span><span class="sxs-lookup"><span data-stu-id="32a84-127">See Also</span></span>  
[<span data-ttu-id="32a84-128">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="32a84-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="32a84-129">Opprette finansbudsjetter</span><span class="sxs-lookup"><span data-stu-id="32a84-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="32a84-130">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="32a84-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="32a84-131">Definere og fordele kostnader</span><span class="sxs-lookup"><span data-stu-id="32a84-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="32a84-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="32a84-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

