---
title: Opprette finansbudsjetter | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter finansbudsjetter for å prognostisere ulike økonomiske aktiviteter og tilordne dimensjoner for forretningsanalyseformål."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1311d566a8166a8a8720bb09789f42c65a1b6e7
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="69c18-103">Opprette finansbudsjetter</span><span class="sxs-lookup"><span data-stu-id="69c18-103">Create G/L Budgets</span></span>
<span data-ttu-id="69c18-104">Du kan ha flere budsjetter for de samme periodene hvis du oppretter budsjetter med forskjellige navn.</span><span class="sxs-lookup"><span data-stu-id="69c18-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="69c18-105">Først definerer du budsjettnavn og angir budsjettallene.</span><span class="sxs-lookup"><span data-stu-id="69c18-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="69c18-106">Budsjettnavnet inkluderes da på alle budsjettpostene du oppretter.</span><span class="sxs-lookup"><span data-stu-id="69c18-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="69c18-107">Når du oppretter et budsjett, kan du definere fire dimensjoner for hvert budsjett.</span><span class="sxs-lookup"><span data-stu-id="69c18-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="69c18-108">Disse budsjettspesifikke dimensjonene kalles budsjettdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="69c18-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="69c18-109">Du kan velge budsjettdimensjoner for hvert budsjett, blant de dimensjonene du allerede har definert.</span><span class="sxs-lookup"><span data-stu-id="69c18-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="69c18-110">Budsjettdimensjoner kan brukes til å definere filtre i budsjetter og til å legge til dimensjonsopplysninger i budsjettposter.</span><span class="sxs-lookup"><span data-stu-id="69c18-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="69c18-111">Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="69c18-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="69c18-112">Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="69c18-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="69c18-113">Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).</span><span class="sxs-lookup"><span data-stu-id="69c18-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="69c18-114">Budsjetter spiller en viktig rolle i forretningsintelligens, for eksempel i årsregnskap basert på kontoskjemaer som inneholder budsjettposter, eller når du analyserer budsjetterte i forhold til faktiske beløp i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="69c18-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="69c18-115">Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).</span><span class="sxs-lookup"><span data-stu-id="69c18-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="69c18-116">I Kostregnskap arbeider du med kostbudsjetter på lignende måte.</span><span class="sxs-lookup"><span data-stu-id="69c18-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="69c18-117">Hvis du vil ha mer informasjon, kan du se [Opprette kostbudsjetter](finance-create-cost-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="69c18-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="69c18-118">Opprette et nytt finansbudsjett</span><span class="sxs-lookup"><span data-stu-id="69c18-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="69c18-119">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="69c18-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="69c18-120">Velg handlingen **Rediger oversikt**, og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="69c18-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="69c18-121">Velg handlingen **Rediger budsjett**.</span><span class="sxs-lookup"><span data-stu-id="69c18-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="69c18-122">Øverst i vinduet **Budsjett** fyller du ut feltene etter behov for å definere det som vises.</span><span class="sxs-lookup"><span data-stu-id="69c18-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="69c18-123">Bare poster som inneholder budsjettnavnet du har angitt i feltet **Budsjettnavn**, vises.</span><span class="sxs-lookup"><span data-stu-id="69c18-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="69c18-124">Ettersom budsjettnavnet nettopp er opprettet, finnes det ingen poster som passer til filteret.</span><span class="sxs-lookup"><span data-stu-id="69c18-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="69c18-125">Vinduet er derfor tomt.</span><span class="sxs-lookup"><span data-stu-id="69c18-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="69c18-126">Angi et beløp ved å velge relevant celle i matrisen.</span><span class="sxs-lookup"><span data-stu-id="69c18-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="69c18-127">**Budsjettposter**-vinduet åpnes.</span><span class="sxs-lookup"><span data-stu-id="69c18-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="69c18-128">Opprett en ny linje, og fyll ut **Beløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69c18-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="69c18-129">Lukk **Budsjettposter**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="69c18-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="69c18-130">Gjenta trinn 5 og 6 til du har angitt alle budsjettbeløpene.</span><span class="sxs-lookup"><span data-stu-id="69c18-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="69c18-131">I hurtigfanen **Filtre** kan du filtrere budsjettopplysningene etter budsjettdimensjoner du har definert under budsjettnavnet.</span><span class="sxs-lookup"><span data-stu-id="69c18-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="69c18-132">Se også</span><span class="sxs-lookup"><span data-stu-id="69c18-132">See Also</span></span>
[<span data-ttu-id="69c18-133">Finans</span><span class="sxs-lookup"><span data-stu-id="69c18-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="69c18-134">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="69c18-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="69c18-135">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="69c18-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="69c18-136">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="69c18-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="69c18-137">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="69c18-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

