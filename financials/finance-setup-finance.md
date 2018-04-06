---
title: "Definere økonomiske prosesser | Microsoft-dokumentasjon"
description: "Få informasjon om oppgavene for å konfigurere finans i virksomheten slik at alle regnskaps-, revisjons- og bokføringsbehov dekkes."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 08/10/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ec4748db61410128b7a61336e52ea6f066fae34
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-finance"></a><span data-ttu-id="5e7e2-103">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="5e7e2-103">Setting Up Finance</span></span>
<span data-ttu-id="5e7e2-104">For å få deg raskt i gang inkluderer [!INCLUDE[d365fin](includes/d365fin_md.md)] standardkonfigurasjoner for de fleste økonomiske prosesser.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-104">To help you get going quickly, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="5e7e2-105">Hvis du vil endre konfigurasjoner til bedriften din, er det bare å fortsette.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="5e7e2-106">Fra Rollesenteret kan du for eksempel bruke en assistert installasjonsveiledningen til å definere mva-satsen for din plassering.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-106">For example, from the Role Center, you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="5e7e2-107">Det er imidlertid noen ting du må definere selv.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="5e7e2-108">For eksempel hvis du vil bruke dimensjoner som grunnlag for forretningsanalyse.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="5e7e2-109">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="5e7e2-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="5e7e2-110">To</span></span> | <span data-ttu-id="5e7e2-111">Se</span><span class="sxs-lookup"><span data-stu-id="5e7e2-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="5e7e2-112">Velg hvordan du betaler dine leverandører.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="5e7e2-113">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="5e7e2-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="5e7e2-114">Angi bokføringsgruppene som tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="5e7e2-115">Definere bokføringsgrupper</span><span class="sxs-lookup"><span data-stu-id="5e7e2-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="5e7e2-116">Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="5e7e2-117">Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="5e7e2-117">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="5e7e2-118">Definere regnskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="5e7e2-119">Åpne et nytt regnskapsår</span><span class="sxs-lookup"><span data-stu-id="5e7e2-119">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="5e7e2-120">Definere hvordan du rapporterer merverdiavgiftsbeløp du har innkrevd for salg, til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="5e7e2-121">Rapportere mva til skattemyndighetene</span><span class="sxs-lookup"><span data-stu-id="5e7e2-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="5e7e2-122">Angi funksjoner for salg og kjøp til å håndtere betalinger i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="5e7e2-123">Aktivere utligning av kundeposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="5e7e2-123">Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="5e7e2-124">Legg til nye kontoer i den eksisterende kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="5e7e2-125">Definere kontoplanen</span><span class="sxs-lookup"><span data-stu-id="5e7e2-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="5e7e2-126">Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="5e7e2-127">Definere kontantstrømanalyse</span><span class="sxs-lookup"><span data-stu-id="5e7e2-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="5e7e2-128">Aktiver fakturering av en kunde som ikke er definert i systemet.</span><span class="sxs-lookup"><span data-stu-id="5e7e2-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="5e7e2-129">Definere kontantkunder</span><span class="sxs-lookup"><span data-stu-id="5e7e2-129">Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="5e7e2-130">Definere Intrastat-rapportering, og send inn rapporten til myndighetene</span><span class="sxs-lookup"><span data-stu-id="5e7e2-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="5e7e2-131">Konfigurere og rapportere Intrastat</span><span class="sxs-lookup"><span data-stu-id="5e7e2-131">Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="5e7e2-132">Se også</span><span class="sxs-lookup"><span data-stu-id="5e7e2-132">See Also</span></span>
[<span data-ttu-id="5e7e2-133">Finans</span><span class="sxs-lookup"><span data-stu-id="5e7e2-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="5e7e2-134">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="5e7e2-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="5e7e2-135">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="5e7e2-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="5e7e2-136">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="5e7e2-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="5e7e2-137">Analysere kontantstrømmen i firmaet</span><span class="sxs-lookup"><span data-stu-id="5e7e2-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="5e7e2-138">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e7e2-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

