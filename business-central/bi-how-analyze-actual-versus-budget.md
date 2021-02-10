---
title: Analysere faktiske i forhold til budsjetterte beløp | Microsoft-dokumentasjon
description: Beskriver hvordan du analyserer faktiske beløp i forhold til budsjetterte beløp.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0a2a8ba7de175ae717dae42da44b719a9c920a15
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752258"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="dccf8-103">Analysere faktiske beløp i forhold til budsjetterte beløp</span><span class="sxs-lookup"><span data-stu-id="dccf8-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="dccf8-104">Som en del av innsamling, analyse og deling av selskapsdataene viser du faktiske beløp sammenlignet med budsjetterte beløp for alle konti og for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="dccf8-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="dccf8-105">Hvis du vil analysere budsjetterte beløp, må du først opprette finansbudsjetter.</span><span class="sxs-lookup"><span data-stu-id="dccf8-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="dccf8-106">Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).</span><span class="sxs-lookup"><span data-stu-id="dccf8-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="dccf8-107">Slik viser du et finansbudsjett</span><span class="sxs-lookup"><span data-stu-id="dccf8-107">To view a G/L budget</span></span>
<span data-ttu-id="dccf8-108">I et budsjett med dimensjoner kan du filtrere postene og se de bestemte budsjettene.</span><span class="sxs-lookup"><span data-stu-id="dccf8-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="dccf8-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansbudsjetter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="dccf8-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="dccf8-110">Åpne budsjettet du vil vise, på siden **Finansbudsjetter**.</span><span class="sxs-lookup"><span data-stu-id="dccf8-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="dccf8-111">Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="dccf8-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="dccf8-112">Hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, må du fylle ut **Vis etter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dccf8-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="dccf8-113">Hvis du ikke har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**, angir du riktig periode i **Datofilter**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dccf8-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="dccf8-114">Beregningen tar bare med poster fra finansbudsjettet som har filterkodene du angir på hurtigfanen **Filtre**.</span><span class="sxs-lookup"><span data-stu-id="dccf8-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="dccf8-115">Budsjettposter med andre filterkoder, eller uten filterkoder, tas ikke med.</span><span class="sxs-lookup"><span data-stu-id="dccf8-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="dccf8-116">Så lenge filteret beholdes på siden, viser budsjettet bare budsjettpostene med disse filterkodene.</span><span class="sxs-lookup"><span data-stu-id="dccf8-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="dccf8-117">Hvis du vil endre budsjettet, kan du endre budsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="dccf8-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="dccf8-118">Velg et beløp for å vise de underliggende finansbudsjettpostene.</span><span class="sxs-lookup"><span data-stu-id="dccf8-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="dccf8-119">Slik viser du faktiske og budsjetterte beløp for alle konti</span><span class="sxs-lookup"><span data-stu-id="dccf8-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="dccf8-120">Du kan vise finansbudsjetter og sammenligne dem med reelle tall, i flere moduler i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="dccf8-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

1. <span data-ttu-id="dccf8-121">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="dccf8-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dccf8-122">På siden **Kontoplan** velger du handlingen **Finanssaldo/Budsjett**.</span><span class="sxs-lookup"><span data-stu-id="dccf8-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="dccf8-123">Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="dccf8-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="dccf8-124">Hvis du vil vise en spesifisering som utgjør beløpet som vises, velger du feltet.</span><span class="sxs-lookup"><span data-stu-id="dccf8-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="dccf8-125">Filtrene du angir på sidetoppteksten, brukes på finansposter og også på budsjettposter.</span><span class="sxs-lookup"><span data-stu-id="dccf8-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="dccf8-126">Kolonnene ytterst til venstre inneholder kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="dccf8-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="dccf8-127">Av de fem kolonnene lengst til høyr, viser de fire første de faktiske og budsjetterte debet- og kreditbeløpene for hver konto.</span><span class="sxs-lookup"><span data-stu-id="dccf8-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="dccf8-128">Den femte kolonnen viser det proporsjonale forholdet mellom de faktiske og de budsjetterte beløpene på finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="dccf8-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="dccf8-129">Bruk **Vis etter**-feltet på siden **Finanssaldo/budsjett** til å velge periodelengden.</span><span class="sxs-lookup"><span data-stu-id="dccf8-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="dccf8-130">Bruk **Vis som**-feltet til å velge hvordan beløpene skal beregnes, **Bevegelse** eller **Saldo per dato**.</span><span class="sxs-lookup"><span data-stu-id="dccf8-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="dccf8-131">Velg handlingen **Forrige periode** eller **Neste periode** for å endre perioden.</span><span class="sxs-lookup"><span data-stu-id="dccf8-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="dccf8-132">Slik viser du faktiske og budsjetterte beløp for flere perioder</span><span class="sxs-lookup"><span data-stu-id="dccf8-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="dccf8-133">I stedet for å vise de faktiske og budsjetterte beløpene for alle konti i én enkelt periode, kan du vise et antall perioder for én enkelt konto.</span><span class="sxs-lookup"><span data-stu-id="dccf8-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="dccf8-134">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="dccf8-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dccf8-135">På siden **Kontoplan** velger du den aktuelle finanskontoen, og deretter velger du handlingen **Finanskontosaldo/Budsjett**.</span><span class="sxs-lookup"><span data-stu-id="dccf8-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="dccf8-136">Øverst på siden fyller du ut feltene etter behov for å definere det som skal vises.</span><span class="sxs-lookup"><span data-stu-id="dccf8-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="dccf8-137">Hvis du vil vise en spesifisering av et beløp som vises, velger du feltet.</span><span class="sxs-lookup"><span data-stu-id="dccf8-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="dccf8-138">Se relatert opplæring på [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="dccf8-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="dccf8-139">Se også</span><span class="sxs-lookup"><span data-stu-id="dccf8-139">See Also</span></span>
[<span data-ttu-id="dccf8-140">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="dccf8-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="dccf8-141">Arbeide med kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="dccf8-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="dccf8-142">Finans</span><span class="sxs-lookup"><span data-stu-id="dccf8-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="dccf8-143">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="dccf8-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="dccf8-144">Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="dccf8-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="dccf8-145">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dccf8-145">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
