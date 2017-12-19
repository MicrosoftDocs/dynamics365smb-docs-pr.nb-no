---
title: "Analysere faktiske i forhold til budsjetterte beløp | Microsoft-dokumentasjon"
description: "Beskriver hvordan du analyserer faktiske beløp i forhold til budsjetterte beløp."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: e76d590476b1236bf1d82a7f5e4f502ffdd9d02d
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="3f41c-103">Analysere faktiske beløp i forhold til budsjetterte beløp</span><span class="sxs-lookup"><span data-stu-id="3f41c-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="3f41c-104">Som en del av innsamling, analyse og deling av selskapsdataene viser du faktiske beløp sammenlignet med budsjetterte beløp for alle konti og for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="3f41c-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="3f41c-105">Hvis du vil analysere budsjetterte beløp, må du først opprette finansbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="3f41c-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="3f41c-106">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="3f41c-106">For more information, see [How to: Create G/L Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="3f41c-107">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="3f41c-108">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="3f41c-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="3f41c-109">Slik viser du et finansbudsjett</span><span class="sxs-lookup"><span data-stu-id="3f41c-109">To view a G/L budget</span></span>
<span data-ttu-id="3f41c-110">I et budsjett med dimensjoner kan du filtrere postene og se de bestemte budsjettene.</span><span class="sxs-lookup"><span data-stu-id="3f41c-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="3f41c-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3f41c-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="3f41c-112">Åpne budsjettet du vil vise, i vinduet **Finansbudsjetter**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="3f41c-113">Øverst i vinduet fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="3f41c-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="3f41c-114">Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, må du fylle ut **Vis etter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f41c-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="3f41c-115">Hvis du ikke har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, angir du riktig periode i **Datofilter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f41c-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3f41c-116">Beregningen tar bare med poster fra finansbudsjettet som har filterkodene du angir på hurtigfanen **Filtre**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="3f41c-117">Budsjettposter med andre filterkoder, eller uten filterkoder, tas ikke med.</span><span class="sxs-lookup"><span data-stu-id="3f41c-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="3f41c-118">Så lenge filteret beholdes i vinduet, viser budsjettet bare budsjettpostene med disse filterkodene.</span><span class="sxs-lookup"><span data-stu-id="3f41c-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="3f41c-119">Hvis du vil endre budsjettet, kan du endre budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="3f41c-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="3f41c-120">Velg et beløp for å vise de underliggende finansbudsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="3f41c-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="3f41c-121">Slik viser du faktiske og budsjetterte beløp for alle konti</span><span class="sxs-lookup"><span data-stu-id="3f41c-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="3f41c-122">Du kan vise finansbudsjetter og sammenligne dem med reelle tall, i flere moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="3f41c-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="3f41c-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3f41c-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3f41c-124">I vinduet **Kontoplan** velger du handlingen **Finanssaldo/Budsjett**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="3f41c-125">Øverst i vinduet fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="3f41c-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="3f41c-126">Hvis du vil vise en spesifisering som utgjør beløpet som vises, velger du feltet.</span><span class="sxs-lookup"><span data-stu-id="3f41c-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3f41c-127">Filtrene du angir i hodet, brukes på finansposter og også på budsjettposter.</span><span class="sxs-lookup"><span data-stu-id="3f41c-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="3f41c-128">Kolonnene ytterst til venstre inneholder kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="3f41c-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="3f41c-129">Av de fem kolonnene lengst til høyr, viser de fire første de faktiske og budsjetterte debet- og kreditbeløpene for hver konto.</span><span class="sxs-lookup"><span data-stu-id="3f41c-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="3f41c-130">Den femte kolonnen viser det proporsjonale forholdet mellom de faktiske og de budsjetterte beløpene på finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="3f41c-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="3f41c-131">Bruk **Vis etter**-feltet i vinduet **Finanssaldo/budsjett** til å velge periodelengden.</span><span class="sxs-lookup"><span data-stu-id="3f41c-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="3f41c-132">Bruk **Vis som**-feltet til å velge hvordan beløpene skal beregnes, **Bevegelse** eller **Saldo per dato**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="3f41c-133">Velg handlingen **Forrige periode** eller **Neste periode** for å endre perioden.</span><span class="sxs-lookup"><span data-stu-id="3f41c-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="3f41c-134">Slik viser du faktiske og budsjetterte beløp for flere perioder</span><span class="sxs-lookup"><span data-stu-id="3f41c-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="3f41c-135">I stedet for å vise de faktiske og budsjetterte beløpene for alle konti i én enkelt periode, kan du vise et antall perioder for én enkelt konto.</span><span class="sxs-lookup"><span data-stu-id="3f41c-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="3f41c-136">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3f41c-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3f41c-137">I vinduet **Kontoplan** velger du den aktuelle finanskontoen, og deretter velger du handlingen **Finanskontosaldo/Budsjett**.</span><span class="sxs-lookup"><span data-stu-id="3f41c-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="3f41c-138">Øverst i vinduet fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="3f41c-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="3f41c-139">Hvis du vil vise en spesifisering av et beløp som vises, velger du feltet.</span><span class="sxs-lookup"><span data-stu-id="3f41c-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f41c-140">Se også</span><span class="sxs-lookup"><span data-stu-id="3f41c-140">See Also</span></span>
[<span data-ttu-id="3f41c-141">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="3f41c-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="3f41c-142">Arbeide med kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="3f41c-142">How to: Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="3f41c-143">Finans</span><span class="sxs-lookup"><span data-stu-id="3f41c-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="3f41c-144">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="3f41c-144">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="3f41c-145">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="3f41c-145">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="3f41c-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f41c-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

