---
title: Valgfrie aktiviteter for lukking av perioder | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av regnskapsperioder i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 678cebc065594ed0ed6fea897676f109ff2c1dce
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="44440-103">Oversikt over oppgaver for lukking av regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="44440-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="44440-104"> tvinger deg ikke å lukke perioder, men det er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre.</span><span class="sxs-lookup"><span data-stu-id="44440-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="44440-105">Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av perioder.</span><span class="sxs-lookup"><span data-stu-id="44440-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="44440-106">Finans</span><span class="sxs-lookup"><span data-stu-id="44440-106">General Ledger</span></span>
* <span data-ttu-id="44440-107">Angi systemomfattende og brukerspesifikke bokføringsperioder.</span><span class="sxs-lookup"><span data-stu-id="44440-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="44440-108">Dette angir datoene som bokføringer som er tillatt mellom.</span><span class="sxs-lookup"><span data-stu-id="44440-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="44440-109">Avhengig av forretningsbehovene vil du kanskje tillate bokføring ved begynnelsen av perioden eller mot slutten.</span><span class="sxs-lookup"><span data-stu-id="44440-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="44440-110">Hvis du vil ha mer informasjon, kan du se [Angi bokføringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="44440-110">For more information, see [How to: Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="44440-111">Foreta alle nødvendige finansjusteringer.</span><span class="sxs-lookup"><span data-stu-id="44440-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="44440-112">Oppdater og bokfør gjentakelseskladder.</span><span class="sxs-lookup"><span data-stu-id="44440-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="44440-113">Kjør kontoskjemaer som følger:</span><span class="sxs-lookup"><span data-stu-id="44440-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="44440-114">Åpne **Kontoskjema**-vinduet, og velg deretter handlingen **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="44440-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="44440-115">Salg</span><span class="sxs-lookup"><span data-stu-id="44440-115">Sales and Receivables</span></span>
* <span data-ttu-id="44440-116">Bokfør alle ordrer, fakturaer, kreditnotaer og ordrereturer.</span><span class="sxs-lookup"><span data-stu-id="44440-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="44440-117">Bokfør alle innbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="44440-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="44440-118">Oppdater og bokfør gjentakelseskladder som er relatert til salg.</span><span class="sxs-lookup"><span data-stu-id="44440-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="44440-119">Avstem kortsiktige fordringer mot Finans.</span><span class="sxs-lookup"><span data-stu-id="44440-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="44440-120">Kjør kjørselen **Slett fakturerte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="44440-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="44440-121">Kjøp</span><span class="sxs-lookup"><span data-stu-id="44440-121">Purchases and Payables</span></span>
* <span data-ttu-id="44440-122">Bokfør alle bestillinger, fakturaer, kreditnotaer og ordrereturer.</span><span class="sxs-lookup"><span data-stu-id="44440-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="44440-123">Bokfør alle utbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="44440-123">Post all payment journals.</span></span>  
* <span data-ttu-id="44440-124">Oppdater og bokfør gjentakelseskladder som er relatert til kjøp.</span><span class="sxs-lookup"><span data-stu-id="44440-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="44440-125">Kjør rapporten **Aldersfordelt saldoliste - lev.**, og avstem leverandørgjeld mot Finans.</span><span class="sxs-lookup"><span data-stu-id="44440-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="44440-126">Kjør kjørselen **Slett fakturerte bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="44440-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="44440-127">Beregn og behandle mva.</span><span class="sxs-lookup"><span data-stu-id="44440-127">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="44440-128">Fullfør mva-oppgaver.</span><span class="sxs-lookup"><span data-stu-id="44440-128">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44440-129">Se også</span><span class="sxs-lookup"><span data-stu-id="44440-129">See Also</span></span>
[<span data-ttu-id="44440-130">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="44440-130">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="44440-131">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="44440-131">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="44440-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44440-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

