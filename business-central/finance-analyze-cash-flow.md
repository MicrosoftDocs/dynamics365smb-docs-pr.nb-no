---
title: "Analysere kontantstrømmer | Microsoft-dokumentasjon"
description: "Beskriver hvordan du bruker diagrammene for kontantsyklus, inntekter og utgifter, kontantstrøm og kontantstrømprognose til å analysere tidligere og fremtidige pengestrømmer inn og ut av firmaet."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 686f678c7459c608f0ef0dccb7bf959bf843e5e6
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="analyzing-cash-flow-in-your-company"></a><span data-ttu-id="66b40-103">Analysere kontantstrømmen i firmaet</span><span class="sxs-lookup"><span data-stu-id="66b40-103">Analyzing Cash Flow in Your Company</span></span>
<span data-ttu-id="66b40-104">Som de sier, er kontanter konge.</span><span class="sxs-lookup"><span data-stu-id="66b40-104">As they say, cash is king.</span></span> <span data-ttu-id="66b40-105">Diagrammer i rollesenteret regnskapsfører gir innsikt som kan hjelpe deg med å gjøre solid avgjørelser om hva du skal gjøre med din kontanter.</span><span class="sxs-lookup"><span data-stu-id="66b40-105">The charts on the Accountant Role Center provide insight that can help you make solid decisions about what to do with your cash.</span></span>  

| <span data-ttu-id="66b40-106">Svare på spørsmål som disse</span><span class="sxs-lookup"><span data-stu-id="66b40-106">To answer questions like these</span></span> | <span data-ttu-id="66b40-107">Bruk dette diagrammet</span><span class="sxs-lookup"><span data-stu-id="66b40-107">Use this chart</span></span> |
| --- | --- |
| <span data-ttu-id="66b40-108">Hvor lenge binder salgsprosessen opp mine kontanter?</span><span class="sxs-lookup"><span data-stu-id="66b40-108">How long does the sales process tie up my cash?</span></span></br> <span data-ttu-id="66b40-109">Bør jeg øke eller redusere lagernivåer?</span><span class="sxs-lookup"><span data-stu-id="66b40-109">Should I increase or reduce inventory levels?</span></span> |<span data-ttu-id="66b40-110">Kontantsyklus</span><span class="sxs-lookup"><span data-stu-id="66b40-110">Cash Cycle</span></span> |
| <span data-ttu-id="66b40-111">Når kontanter flytter inn og ut av firmaet?</span><span class="sxs-lookup"><span data-stu-id="66b40-111">When did cash move in and out of my company?</span></span></br> <span data-ttu-id="66b40-112">Er noen perioder bedre enn andre?</span><span class="sxs-lookup"><span data-stu-id="66b40-112">Are some periods better than others?</span></span> |<span data-ttu-id="66b40-113">Kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="66b40-113">Cash Flow</span></span> |
| <span data-ttu-id="66b40-114">Tallene ser ut av en periode?</span><span class="sxs-lookup"><span data-stu-id="66b40-114">Do the numbers seem off for a period?</span></span></br> <span data-ttu-id="66b40-115">Bør jeg undersøke?</span><span class="sxs-lookup"><span data-stu-id="66b40-115">Should I investigate?</span></span> |<span data-ttu-id="66b40-116">Inntekter og utgifter</span><span class="sxs-lookup"><span data-stu-id="66b40-116">Income & Expense</span></span> |
| <span data-ttu-id="66b40-117">Når kan en kontant overskudd eller underskudd skje?</span><span class="sxs-lookup"><span data-stu-id="66b40-117">When might a cash surplus or deficit happen?</span></span></br> <span data-ttu-id="66b40-118">Må jeg betale ned gjelden, eller låne for å dekke utgifter for kommende?</span><span class="sxs-lookup"><span data-stu-id="66b40-118">Should I pay down debt, or borrow to meet upcoming expenses?</span></span> |<span data-ttu-id="66b40-119">Kontantstrømprognoser</span><span class="sxs-lookup"><span data-stu-id="66b40-119">Cash Flow Forecasts</span></span> |

<span data-ttu-id="66b40-120">På rollesenter for regnskapsfører under **Finansytelse**, **Kontantsyklus**, **Kontantstrøm** og **Inntekter og utgifter** diagrammer gir muligheter til å analysere kontantstrøm:</span><span class="sxs-lookup"><span data-stu-id="66b40-120">On the Accountant Role Center, under **Finance Performance**, the **Cash Cycle**, **Cash Flow**, and **Income & Expense** charts offer ways to analyze cash flow:</span></span>  

* <span data-ttu-id="66b40-121">Se tallene i en periode ved hjelp av skyvekontrollen for tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="66b40-121">See figures for a period by using the timeline slider.</span></span>  
* <span data-ttu-id="66b40-122">Filtrere diagrammet ved å velge kilden i forklaringen.</span><span class="sxs-lookup"><span data-stu-id="66b40-122">Filter the chart by choosing the source in the legend.</span></span>  
* <span data-ttu-id="66b40-123">Endre lengden på perioden, eller gå til forrige eller neste periode, ved å velge alternativer på den **Finansytelse** rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="66b40-123">Change the length of the period, or go to the previous or next period, by choosing options on the **Finance Performance** drop down.</span></span>  
* <span data-ttu-id="66b40-124">Vise poster ved å velge et punkt i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="66b40-124">View the entries by choosing a point in the chart.</span></span> <span data-ttu-id="66b40-125">Et punkt på tidslinjen eller et kolonnesegment.</span><span class="sxs-lookup"><span data-stu-id="66b40-125">For example, a point on the timeline or a column segment.</span></span> <span data-ttu-id="66b40-126">Hvis numrene ser ut av, er der du kan foreta justeringer.</span><span class="sxs-lookup"><span data-stu-id="66b40-126">If the numbers seem off, this is where you can make adjustments.</span></span>  

<span data-ttu-id="66b40-127">Selv om det er separate, den **Kontantstrømprognose** diagram ligner.</span><span class="sxs-lookup"><span data-stu-id="66b40-127">Although it's separate, the **Cash Flow Forecast** chart is similar.</span></span> <span data-ttu-id="66b40-128">Du viser detaljer, filtrerer resultater og endrer det som vises på samme måte.</span><span class="sxs-lookup"><span data-stu-id="66b40-128">You view details, filter results, and change what is displayed in the same ways.</span></span> <span data-ttu-id="66b40-129">Hvis du endrer en innstilling, kan du oppdatere prognosen ved å velge **Kontantstrømprognose**, og deretter **Beregn prognose på nytt**.</span><span class="sxs-lookup"><span data-stu-id="66b40-129">If you change a setting, you can refresh the forecast by choosing **Cash Flow Forecast**, and then **Recalculate Forecast**.</span></span>

<span data-ttu-id="66b40-130">Hvis du vil undersøke prognosen, i tillegg til prognosen oppføringer, kan du også se på regnearket kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="66b40-130">If you want to examine the forecast, in addition to forecast entries, you can also look at the cash flow worksheet.</span></span> <span data-ttu-id="66b40-131">Du kan for eksempel se hvordan prognosen:</span><span class="sxs-lookup"><span data-stu-id="66b40-131">For example, you can see how the forecast:</span></span>

* <span data-ttu-id="66b40-132">Håndterer bekreftede salg og innkjøp.</span><span class="sxs-lookup"><span data-stu-id="66b40-132">Handles confirmed sales and purchases.</span></span>  
* <span data-ttu-id="66b40-133">Trekker fra tilgodehavende og legger til skyldig beløp.</span><span class="sxs-lookup"><span data-stu-id="66b40-133">Subtracts payables and adds receivables.</span></span>  
* <span data-ttu-id="66b40-134">Hopper over dupliserte salgsordrer og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="66b40-134">Skips duplicate sales orders and purchase orders.</span></span>  

## <a name="to-view-a-cash-flow-worksheet"></a><span data-ttu-id="66b40-135">Slik viser du et forslag for kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="66b40-135">To view a cash flow worksheet</span></span>
1. <span data-ttu-id="66b40-136">Søk etter **Kontantstrømprognoser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="66b40-136">Search for **Cash Flow Forecasts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="66b40-137">Velg en kontantstrømprognose, og velg deretter den **Kontantstrømforslag**.</span><span class="sxs-lookup"><span data-stu-id="66b40-137">Choose a cash flow forecast, and then choose the **Cash Flow Worksheet** action.</span></span>  
3. <span data-ttu-id="66b40-138">På siden **Kontantstrømforslag** velger du handlingen **Foreslå forslagslinjer**.</span><span class="sxs-lookup"><span data-stu-id="66b40-138">On the **Cash Flow Worksheet** page, choose the **Suggest Worksheet Lines** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66b40-139">Se også</span><span class="sxs-lookup"><span data-stu-id="66b40-139">See Also</span></span>
[<span data-ttu-id="66b40-140">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="66b40-140">Setting Up Finance</span></span>](finance-setup-finance.md)  
<span data-ttu-id="66b40-141">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66b40-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="66b40-142">Definere kontantstrømanalyse</span><span class="sxs-lookup"><span data-stu-id="66b40-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  

