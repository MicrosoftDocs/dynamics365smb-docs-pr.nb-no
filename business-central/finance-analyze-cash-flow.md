---
title: Analysere kontantstrømmer | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker diagrammene for kontantsyklus, inntekter og utgifter, kontantstrøm og kontantstrømprognose til å analysere tidligere og fremtidige pengestrømmer inn og ut av firmaet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 7bc87f8fc096241e7f77efb0eb4e7bceb1d28aef
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391177"
---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="ea5d2-103">Analysere kontantstrømmen i firmaet</span><span class="sxs-lookup"><span data-stu-id="ea5d2-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="ea5d2-104">Diagrammer i rollesenteret regnskapsfører gir innsikt som kan hjelpe deg med å gjøre solid avgjørelser om hva du skal gjøre med din kontanter.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-104">The charts on the Accountant Role Center provide insights that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="ea5d2-105">Svare på spørsmål som disse</span><span class="sxs-lookup"><span data-stu-id="ea5d2-105">To answer questions like these</span></span> | <span data-ttu-id="ea5d2-106">Bruk dette diagrammet</span><span class="sxs-lookup"><span data-stu-id="ea5d2-106">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="ea5d2-107">Hvor lenge binder salgsprosessen opp mine kontanter?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-107">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="ea5d2-108">Bør jeg øke eller redusere lagernivåer?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-108">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="ea5d2-109">Kontantsyklus</span><span class="sxs-lookup"><span data-stu-id="ea5d2-109">Cash Cycle</span></span> |
| <span data-ttu-id="ea5d2-110">Når kontanter flytter inn og ut av firmaet?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-110">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="ea5d2-111">Er noen perioder bedre enn andre?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-111">Are some periods better than others?</span></span> |<span data-ttu-id="ea5d2-112">Kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="ea5d2-112">Cash Flow</span></span> |
| <span data-ttu-id="ea5d2-113">Tallene ser ut av en periode?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-113">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="ea5d2-114">Bør jeg undersøke?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-114">Should I investigate?</span></span> |<span data-ttu-id="ea5d2-115">Inntekter og utgifter</span><span class="sxs-lookup"><span data-stu-id="ea5d2-115">Income & Expense</span></span> |
| <span data-ttu-id="ea5d2-116">Når kan en kontant overskudd eller underskudd skje?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-116">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="ea5d2-117">Må jeg betale ned gjelden, eller låne for å dekke utgifter for kommende?</span><span class="sxs-lookup"><span data-stu-id="ea5d2-117">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="ea5d2-118">Kontantstrømprognoser</span><span class="sxs-lookup"><span data-stu-id="ea5d2-118">Cash Flow Forecasts</span></span> |

<span data-ttu-id="ea5d2-119">På rollesenter for regnskapsfører under **Finansytelse**, **Kontantsyklus**, **Kontantstrøm** og **Inntekter og utgifter** diagrammer gir muligheter til å analysere kontantstrøm:</span><span class="sxs-lookup"><span data-stu-id="ea5d2-119">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="ea5d2-120">Se tallene i en periode ved hjelp av skyvekontrollen for tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-120">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="ea5d2-121">Filtrere diagrammet ved å velge kilden i forklaringen.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-121">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="ea5d2-122">Endre lengden på perioden, eller gå til forrige eller neste periode, ved å velge alternativer på den **Finansytelse** rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-122">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="ea5d2-123">Vise poster ved å velge et punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-123">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="ea5d2-124">Et punkt på tidslinjen eller et kolonnesegment.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-124">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="ea5d2-125">Hvis numrene ser ut av, er der du kan foreta justeringer.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-125">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="ea5d2-126">Selv om det er separate, den **Kontantstrømprognose** diagram ligner.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-126">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="ea5d2-127">Du viser detaljer, filtrerer resultater og endrer det som vises på samme måte.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-127">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="ea5d2-128">Hvis du endrer en innstilling, kan du oppdatere prognosen ved å velge **Kontantstrømprognose**, og deretter **Beregn prognose på nytt**.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-128">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="ea5d2-129">Hvis du vil undersøke prognosen, i tillegg til prognosen oppføringer, kan du også se på regnearket kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-129">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="ea5d2-130">Du kan for eksempel se hvordan prognosen:</span><span class="sxs-lookup"><span data-stu-id="ea5d2-130">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="ea5d2-131">Håndterer bekreftede salg og innkjøp.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-131">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="ea5d2-132">Trekker fra tilgodehavende og legger til skyldig beløp.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-132">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="ea5d2-133">Hopper over dupliserte salgsordrer og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-133">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="ea5d2-134">Slik viser du et forslag for kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="ea5d2-134">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="ea5d2-135">Søk etter **Kontantstrømprognoser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-135">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ea5d2-136">Velg en kontantstrømprognose, og velg deretter den **Kontantstrømforslag**.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-136">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="ea5d2-137">På siden **Kontantstrømforslag** velger du handlingen **Foreslå forslagslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ea5d2-137">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="ea5d2-138">Se relatert opplæring på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="ea5d2-138">See Related Training at [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="ea5d2-139">Se også</span><span class="sxs-lookup"><span data-stu-id="ea5d2-139">See Also</span></span>
[<span data-ttu-id="ea5d2-140">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="ea5d2-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="ea5d2-141">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea5d2-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ea5d2-142">Definere kontantstrømanalyse</span><span class="sxs-lookup"><span data-stu-id="ea5d2-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]