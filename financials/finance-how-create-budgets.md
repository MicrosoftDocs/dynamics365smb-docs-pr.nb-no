---
title: Opprette budsjetter | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter budsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cda69d70ece090a149a13e5e1f4ed02fa70c49f7
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create--budgets"></a><span data-ttu-id="b520b-103">Opprette budsjetter</span><span class="sxs-lookup"><span data-stu-id="b520b-103">How to: Create  Budgets</span></span>
<span data-ttu-id="b520b-104">Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn.</span><span class="sxs-lookup"><span data-stu-id="b520b-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="b520b-105">Først definerer du budsjettnavn og angir budsjettallene.</span><span class="sxs-lookup"><span data-stu-id="b520b-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="b520b-106">Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.</span><span class="sxs-lookup"><span data-stu-id="b520b-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="b520b-107">Når du oppretter et budsjett, kan du definere fire dimensjoner for hvert budsjett.</span><span class="sxs-lookup"><span data-stu-id="b520b-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="b520b-108">Disse budsjettspesifikke dimensjonene kalles budsjettdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="b520b-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="b520b-109">Du kan velge budsjettdimensjoner for hvert budsjett, blant de dimensjonene du allerede har definert.</span><span class="sxs-lookup"><span data-stu-id="b520b-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="b520b-110">Budsjettdimensjoner kan brukes til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter.</span><span class="sxs-lookup"><span data-stu-id="b520b-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="b520b-111">Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b520b-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="b520b-112">Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b520b-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="b520b-113">Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).</span><span class="sxs-lookup"><span data-stu-id="b520b-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="b520b-114">Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b520b-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="b520b-115">Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).</span><span class="sxs-lookup"><span data-stu-id="b520b-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="b520b-116">I Kostregnskap arbeider du med kostbudsjetter på lignende måte.</span><span class="sxs-lookup"><span data-stu-id="b520b-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="b520b-117">Hvis du vil ha mer informasjon, kan du se [Opprette kostbudsjetter](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="b520b-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="b520b-118">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="b520b-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="b520b-119">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="b520b-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="b520b-120">Opprette et nytt budsjett</span><span class="sxs-lookup"><span data-stu-id="b520b-120">To create a new budget</span></span>  

1. <span data-ttu-id="b520b-121">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b520b-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b520b-122">Velg handlingen **Rediger oversikt**, og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b520b-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="b520b-123">Velg handlingen **Rediger budsjett**.</span><span class="sxs-lookup"><span data-stu-id="b520b-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="b520b-124">Øverst i vinduet **Budsjett** fyller du ut feltene etter behov for å definere det som vises.</span><span class="sxs-lookup"><span data-stu-id="b520b-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="b520b-125">Bare poster som inneholder budsjettnavnet du har angitt i feltet **Budsjettnavn**, vises.</span><span class="sxs-lookup"><span data-stu-id="b520b-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="b520b-126">Ettersom budsjettnavnet nettopp er opprettet, finnes det ingen poster som passer til filteret.</span><span class="sxs-lookup"><span data-stu-id="b520b-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="b520b-127">Vinduet er derfor tomt.</span><span class="sxs-lookup"><span data-stu-id="b520b-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="b520b-128">Angi et beløp ved å velge relevant celle i matrisen.</span><span class="sxs-lookup"><span data-stu-id="b520b-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="b520b-129">**Budsjettposter**-vinduet åpnes.</span><span class="sxs-lookup"><span data-stu-id="b520b-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="b520b-130">Opprett en ny linje, og fyll ut **Beløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b520b-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="b520b-131">Lukk **Budsjettposter**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="b520b-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="b520b-132">Gjenta trinn 5 og 6 til du har angitt alle budsjettbeløpene.</span><span class="sxs-lookup"><span data-stu-id="b520b-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b520b-133">I hurtigfanen **Filtre** kan du filtrere budsjettopplysningene etter budsjettdimensjoner du har definert under budsjettnavnet.</span><span class="sxs-lookup"><span data-stu-id="b520b-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="b520b-134">Se også</span><span class="sxs-lookup"><span data-stu-id="b520b-134">See Also</span></span>
[<span data-ttu-id="b520b-135">Finans</span><span class="sxs-lookup"><span data-stu-id="b520b-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="b520b-136">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="b520b-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="b520b-137">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="b520b-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="b520b-138">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="b520b-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="b520b-139">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b520b-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

