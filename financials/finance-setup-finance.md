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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b63e2e65f92edbbe10bcb5e2c340db31b1acda28
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-finance"></a><span data-ttu-id="13a17-103">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="13a17-103">Setting Up Finance</span></span>
<span data-ttu-id="13a17-104">For å få deg raskt i gang inkluderer [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] standardkonfigurasjoner for de fleste økonomiske prosesser.</span><span class="sxs-lookup"><span data-stu-id="13a17-104">To help you get going quickly, [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] includes standard configurations for most financial processes.</span></span> <span data-ttu-id="13a17-105">Hvis du vil endre konfigurasjoner til bedriften din, er det bare å fortsette.</span><span class="sxs-lookup"><span data-stu-id="13a17-105">If you need to change the configurations to suit your business, go right ahead.</span></span> <span data-ttu-id="13a17-106">Fra hjemmesiden kan du for eksempel bruke en assistert installasjonsveiledningen til å definere mva-satsen for din plassering.</span><span class="sxs-lookup"><span data-stu-id="13a17-106">For example, from the Home page you can use an assisted setup guide to set up sales tax rate for your location.</span></span>  

<span data-ttu-id="13a17-107">Det er imidlertid noen ting du må definere selv.</span><span class="sxs-lookup"><span data-stu-id="13a17-107">However, there are some things you need to set up yourself.</span></span> <span data-ttu-id="13a17-108">For eksempel hvis du vil bruke dimensjoner som grunnlag for forretningsanalyse.</span><span class="sxs-lookup"><span data-stu-id="13a17-108">For example, if you want to use dimensions as a basis for business intelligence.</span></span>  

<span data-ttu-id="13a17-109">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="13a17-109">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="13a17-110">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="13a17-110">To</span></span> | <span data-ttu-id="13a17-111">Se</span><span class="sxs-lookup"><span data-stu-id="13a17-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="13a17-112">Velg hvordan du betaler dine leverandører.</span><span class="sxs-lookup"><span data-stu-id="13a17-112">Choose how you pay your vendors.</span></span> |[<span data-ttu-id="13a17-113">Definere betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="13a17-113">Defining Payment Methods</span></span>](finance-payment-methods.md) |
| <span data-ttu-id="13a17-114">Angi bokføringsgruppene som tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="13a17-114">Specify the posting groups that map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> |[<span data-ttu-id="13a17-115">Definere bokføringsgrupper</span><span class="sxs-lookup"><span data-stu-id="13a17-115">Setting Up Posting Groups</span></span>](finance-posting-groups.md)|
|<span data-ttu-id="13a17-116">Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="13a17-116">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="13a17-117">Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt</span><span class="sxs-lookup"><span data-stu-id="13a17-117">How to: Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| <span data-ttu-id="13a17-118">Definere regnskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="13a17-118">Set up fiscal periods.</span></span> |[<span data-ttu-id="13a17-119">Åpne et nytt regnskapsår</span><span class="sxs-lookup"><span data-stu-id="13a17-119">How to: Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md) |
| <span data-ttu-id="13a17-120">Definere hvordan du rapporterer merverdiavgiftsbeløp du har innkrevd for salg, til skattemyndighetene.</span><span class="sxs-lookup"><span data-stu-id="13a17-120">Define how you report value-added tax amounts that you have collected for sales to the tax authorities.</span></span> |[<span data-ttu-id="13a17-121">Rapportere mva til skattemyndighetene</span><span class="sxs-lookup"><span data-stu-id="13a17-121">How To: Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)|
| <span data-ttu-id="13a17-122">Angi funksjoner for salg og kjøp til å håndtere betalinger i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="13a17-122">Set your Sales and Purchases features up to handle payments in foreign currencies.</span></span>|[<span data-ttu-id="13a17-123">Aktivere utligning av kundeposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="13a17-123">How to: Enable Application of Ledger Entries in Different Currencies</span></span>](finance-how-enable-application-ledger-entries-different-currencies.md)
| <span data-ttu-id="13a17-124">Legg til nye kontoer i den eksisterende kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="13a17-124">Add new accounts to the existing chart of accounts.</span></span> |[<span data-ttu-id="13a17-125">Definere kontoplanen</span><span class="sxs-lookup"><span data-stu-id="13a17-125">Setting Up the Chart of Accounts</span></span>](finance-setup-chart-accounts.md) |
| <span data-ttu-id="13a17-126">Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="13a17-126">Set up business intelligence (BI) charts to analyze cash flow.</span></span> |[<span data-ttu-id="13a17-127">Definere kontantstrømanalyse</span><span class="sxs-lookup"><span data-stu-id="13a17-127">Setting Up Cash Flow Analysis</span></span>](finance-setup-cash-flow-analyses.md) |
|<span data-ttu-id="13a17-128">Aktiver fakturering av en kunde som ikke er definert i systemet.</span><span class="sxs-lookup"><span data-stu-id="13a17-128">Enable invoicing of a customer who is not set up in the system.</span></span>|[<span data-ttu-id="13a17-129">Definere kontantkunder</span><span class="sxs-lookup"><span data-stu-id="13a17-129">How to: Set Up Cash Customers</span></span>](finance-how-to-set-up-cash-customers.md)|
| <span data-ttu-id="13a17-130">Definere Intrastat-rapportering, og send inn rapporten til myndighetene</span><span class="sxs-lookup"><span data-stu-id="13a17-130">Set up Intrastat reporting, and submit the report to an authority</span></span> | [<span data-ttu-id="13a17-131">Konfigurere og rapportere Intrastat</span><span class="sxs-lookup"><span data-stu-id="13a17-131">How to: Set Up and Report Intrastat</span></span>](finance-how-setup-report-intrastat.md)|

## <a name="see-also"></a><span data-ttu-id="13a17-132">Se også</span><span class="sxs-lookup"><span data-stu-id="13a17-132">See Also</span></span>
<span data-ttu-id="13a17-133">[Finans](finance.md)]</span><span class="sxs-lookup"><span data-stu-id="13a17-133">[Finance](finance.md)]</span></span>  
[<span data-ttu-id="13a17-134">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="13a17-134">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="13a17-135">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="13a17-135">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="13a17-136">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="13a17-136">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="13a17-137">Analysere kontantstrømmen i firmaet</span><span class="sxs-lookup"><span data-stu-id="13a17-137">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="13a17-138">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13a17-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

