---
title: Oversikt over kontantstrøm
description: Oversikt over kontantstrømmer inn og ut for å hjelpe forutsi penger som skal mottas og utbetales.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash flow, money flow, expense and income, liquidity, cash receipts minus cash payments
ms.date: 06/08/2021
ms.author: a-jillk
ms.reviewer: edupont
ms.openlocfilehash: 8359d95b36d6c16b179de2fce400c44fd93ec0f1
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216387"
---
# <a name="cash-flow-overview"></a><span data-ttu-id="54261-103">Oversikt over kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="54261-103">Cash Flow Overview</span></span>

<span data-ttu-id="54261-104">Å forstå kontantstrømmer inn og ut er nøkkelen til en fremgangsrik virksomhet.</span><span class="sxs-lookup"><span data-stu-id="54261-104">Understanding cash inflows and outflows is the key to running a successful business.</span></span> <span data-ttu-id="54261-105">Du kan bruke kontantstrøm til å enkelt opprette en prognose på kort sikt som forutsier hvordan og når du forventer at penger skal mottas og betales av bedriften din.</span><span class="sxs-lookup"><span data-stu-id="54261-105">You can use cash flow to easily create a short-term forecast that predicts how and when you expect money to be received and paid out by your business.</span></span> <span data-ttu-id="54261-106">Det er viktig for deg å vite at bedriften har nok kontanter til å betale kreditorer og utgifter når de forfaller.</span><span class="sxs-lookup"><span data-stu-id="54261-106">It is important for you to know that your business will have enough cash to pay creditors and expenses when they fall due.</span></span>

## <a name="definition-of-cash-flow"></a><span data-ttu-id="54261-107">Definisjon av kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="54261-107">Definition of Cash Flow</span></span>

<span data-ttu-id="54261-108">Begrepet *kontantstrøm* brukes til å angi innbetalinger minus utbetalinger i en valgt periode.</span><span class="sxs-lookup"><span data-stu-id="54261-108">The term *cash flow* is used to designate cash receipts minus cash payments over a selected period.</span></span> <span data-ttu-id="54261-109">Det er et anslag over hvor mye penger som du forventer vil flyte inn og ut av bedriften, og det inkluderer prognoseberegnede inntekter og utgifter.</span><span class="sxs-lookup"><span data-stu-id="54261-109">It is an estimate of the amount of money that you expect to flow in and out of your business, and it includes all your forecasted income and expenses.</span></span>

## <a name="cash-flow-overview"></a><span data-ttu-id="54261-110">Oversikt over kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="54261-110">Cash Flow Overview</span></span>

<span data-ttu-id="54261-111">Illustrasjonen nedenfor viser en oversikt over hvordan du kan arbeide med kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="54261-111">The following illustration shows an overview of how you can work with cash flow.</span></span>

<span data-ttu-id="54261-112">![Oversikt over kontantstrøm](media/finance_cash_flow_overview.png "Oversikt over kontantstrøm")</span><span class="sxs-lookup"><span data-stu-id="54261-112">![Cash Flow overview](media/finance_cash_flow_overview.png "Cash Flow overview")</span></span>

- <span data-ttu-id="54261-113">Du definerer en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-113">You set up a cash flow forecast.</span></span>  

- <span data-ttu-id="54261-114">Du får kontantstrømprognosekilder fra følgende områder:</span><span class="sxs-lookup"><span data-stu-id="54261-114">You get cash flow forecast sources from the following areas:</span></span>  

  - <span data-ttu-id="54261-115">Finans – Informasjon om likvide midler og budsjetterte inntekter og utgifter i selskapet.</span><span class="sxs-lookup"><span data-stu-id="54261-115">General ledger – Information about the liquid funds and the budgeted revenues and expenses of your company.</span></span>  
  - <span data-ttu-id="54261-116">Kjøp – informasjon om de gjeldende åpne leverandørkontoer og eventuell prognoseberegnet gjeld fra åpne bestillinger.</span><span class="sxs-lookup"><span data-stu-id="54261-116">Purchasing – Information about the current payables and any forecasted debts from open purchase orders.</span></span>  
  - <span data-ttu-id="54261-117">Salg – informasjon om de gjeldende åpne kundekontoer og eventuell prognoseberegnet mottak fra åpne ordrer.</span><span class="sxs-lookup"><span data-stu-id="54261-117">Sales – Information about the current receivables and any forecasted receipts from open sales orders.</span></span>  
  - <span data-ttu-id="54261-118">Service – informasjon om åpne serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="54261-118">Service – Information about open service orders.</span></span>  
  - <span data-ttu-id="54261-119">Aktiva – Informasjon om planlagte salg og budsjetterte innkjøp av aktiva.</span><span class="sxs-lookup"><span data-stu-id="54261-119">Fixed assets – Information about planned disposal and budgeted purchases of fixed assets.</span></span>  
  - <span data-ttu-id="54261-120">Manuell inntekter og utgifter – administrere manuell inntekter og utgifter og inkludere dem i kontantstrømprognosen.</span><span class="sxs-lookup"><span data-stu-id="54261-120">Manual revenues and expenses – Manage manual revenues and expenses and include them in the cash flow forecast.</span></span>  
- <span data-ttu-id="54261-121">Du bruker en satsvis jobb til å overføre informasjon fra områdene i finans, salg, kjøp, tjenester og aktiva til kontantstrømforslaget. Deretter registrerer du forslagslinjer for å generere en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-121">You use a batch job to transfer information from the areas of general ledger, sales, purchasing, service, and fixed assets to the worksheet Then, you register worksheet lines to make a cash flow forecast.</span></span>  
- <span data-ttu-id="54261-122">Du bruker forskjellige vinduer, rapporter og diagrammer til å analysere og skrive ut en kontantstrømprognose som er relatert til tilgjengelighets- og tidslinjeoversikter.</span><span class="sxs-lookup"><span data-stu-id="54261-122">You use various windows, reports, and charts to analyze and print a cash flow forecast that relates to availability and timeline overviews.</span></span>  

## <a name="making-a-cash-flow-forecast"></a><span data-ttu-id="54261-123">Lage en kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="54261-123">Making a Cash Flow Forecast</span></span>

<span data-ttu-id="54261-124">Basert på de registrerte forslagslinjene kan du regelmessig lage en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-124">Based on the registered worksheet lines, you can periodically make a cash flow forecast.</span></span> <span data-ttu-id="54261-125">Følgende oppsett brukes ofte for en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-125">The following layout is a frequently used layout for a cash flow forecast.</span></span> <span data-ttu-id="54261-126">Oppsettet har tre deler:</span><span class="sxs-lookup"><span data-stu-id="54261-126">The layout has three sections:</span></span>

  - <span data-ttu-id="54261-127">Innbetalinger</span><span class="sxs-lookup"><span data-stu-id="54261-127">Cash receipts</span></span>  
  - <span data-ttu-id="54261-128">Kontantutbetalinger</span><span class="sxs-lookup"><span data-stu-id="54261-128">Cash disbursements</span></span>  
  - <span data-ttu-id="54261-129">Netto kontantstrøm eller kassebeholdning</span><span class="sxs-lookup"><span data-stu-id="54261-129">Net cash flow or cash-in-hand</span></span>  

<span data-ttu-id="54261-130">Innbetalinger gir detaljer om inntekter som bedriften mottar.</span><span class="sxs-lookup"><span data-stu-id="54261-130">Cash receipts provide details of the income that the business receives.</span></span>

<span data-ttu-id="54261-131">*kontantmottak totalt* = *fordringer* + *åpne ordrer* + *åpne serviceordrer* + *salg av aktiva* + *manuelle inntekter* + *budsjetterte inntekter*</span><span class="sxs-lookup"><span data-stu-id="54261-131">*total cash receipts* = *receivables* + *open sales orders* + *open service orders* + *fixed assets disposals* + *manual revenues* + *budgeted revenues*</span></span>

> [!NOTE]
> <span data-ttu-id="54261-132">Manuelle inntekter kan være leieinntekter, renter fra økonomiske aktiva eller ny privat kapital.</span><span class="sxs-lookup"><span data-stu-id="54261-132">Manual revenues can be rental income, interest from financial assets, or new private capital.</span></span> <span data-ttu-id="54261-133">Du kan planlegge manuelle inntekter for en tidsperiode og bruke dem i beregningen av kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-133">You can plan manual revenues for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="54261-134">Kontantutbetalinger gir detaljer om betalinger gjort av bedriften.</span><span class="sxs-lookup"><span data-stu-id="54261-134">Cash disbursements provide details of the payments made by the business.</span></span>

<span data-ttu-id="54261-135">*total for kontantutbetalinger* = *beløp* + *åpne bestillinger* + *aktivainvestering* + *manuelle utgifter* + *budsjetterte utgifter*</span><span class="sxs-lookup"><span data-stu-id="54261-135">*total cash disbursements* = *payables* + *open purchase orders* + *fixed asset investment* + *manual expenses* + *budgeted expenses*</span></span>

> [!NOTE]
> <span data-ttu-id="54261-136">Manuelle utgifter kan være lønn, renter på kreditt eller privat forbruk.</span><span class="sxs-lookup"><span data-stu-id="54261-136">Manual expenses can be salaries, interest on credit, or private consumptions.</span></span> <span data-ttu-id="54261-137">Du kan planlegge manuelle utgifter for en tidsperiode og bruke dem i beregningen av kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="54261-137">You can plan manual expenses for a period of time and use them in the calculation of cash flow forecast.</span></span>

<span data-ttu-id="54261-138">Netto kontantstrøm eller kassebeholdning beregnes som totale kontantmottak minus totale kontantutbetalinger ved slutten av hver periode.</span><span class="sxs-lookup"><span data-stu-id="54261-138">Net cash flow or cash-in-hand is calculated as total receipts minus total disbursements at the end of each period.</span></span>

<span data-ttu-id="54261-139">*netto kontantstrøm* = *kontantmottak totalt* – *total for kontantutbetalinger* + *likvide midler*</span><span class="sxs-lookup"><span data-stu-id="54261-139">*net cash flow* = *total cash receipts* – *total cash disbursements* + *liquid funds*</span></span>

<span data-ttu-id="54261-140">Prognosen kan deretter brukes som et internt verktøy for administrativ beslutningstaking som hjelper deg med å planlegge fremover og ta viktige strategiske beslutninger om driften av virksomheten.</span><span class="sxs-lookup"><span data-stu-id="54261-140">The forecast can then be used as an internal management decision-making tool that helps you plan ahead and make important strategic decisions about the operation of the business.</span></span>

## <a name="see-also"></a><span data-ttu-id="54261-141">Se også</span><span class="sxs-lookup"><span data-stu-id="54261-141">See Also</span></span>
[<span data-ttu-id="54261-142">Definere kontantstrømanalyse</span><span class="sxs-lookup"><span data-stu-id="54261-142">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md)  
[<span data-ttu-id="54261-143">Analyser kontantstrøm</span><span class="sxs-lookup"><span data-stu-id="54261-143">Analyze Cash Flow</span></span>](finance-analyze-cash-flow.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
