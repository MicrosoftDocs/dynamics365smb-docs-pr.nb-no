---
title: Valgfrie aktiviteter for lukking av perioder | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av regnskapsperioder i Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 104f63e07e4bfd8945f73581a4fb7810f946304f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755570"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="1afb5-103">Oversikt over oppgaver for lukking av regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="1afb5-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="1afb5-104">tvinger deg ikke å lukke perioder, men det er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre.</span><span class="sxs-lookup"><span data-stu-id="1afb5-104">does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="1afb5-105">Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av perioder.</span><span class="sxs-lookup"><span data-stu-id="1afb5-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="1afb5-106">Finans</span><span class="sxs-lookup"><span data-stu-id="1afb5-106">General Ledger</span></span>
* <span data-ttu-id="1afb5-107">Angi systemomfattende og brukerspesifikke bokføringsperioder.</span><span class="sxs-lookup"><span data-stu-id="1afb5-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="1afb5-108">Dette angir datoene som bokføringer som er tillatt mellom.</span><span class="sxs-lookup"><span data-stu-id="1afb5-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="1afb5-109">Avhengig av forretningsbehovene vil du kanskje tillate bokføring ved begynnelsen av perioden eller mot slutten.</span><span class="sxs-lookup"><span data-stu-id="1afb5-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="1afb5-110">Hvis du vil ha mer informasjon, kan du se [Angi bokføringsperioder](finance-how-specify-posting-periods.md).</span><span class="sxs-lookup"><span data-stu-id="1afb5-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="1afb5-111">Foreta alle nødvendige finansjusteringer.</span><span class="sxs-lookup"><span data-stu-id="1afb5-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="1afb5-112">Oppdater og bokfør gjentakelseskladder.</span><span class="sxs-lookup"><span data-stu-id="1afb5-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="1afb5-113">Kjør kontoskjemaer som følger:</span><span class="sxs-lookup"><span data-stu-id="1afb5-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="1afb5-114">Åpne **Kontoskjema**-siden, og velg deretter handlingen **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="1afb5-114">Open the **Account Schedule** page, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="1afb5-115">Salg</span><span class="sxs-lookup"><span data-stu-id="1afb5-115">Sales and Receivables</span></span>
* <span data-ttu-id="1afb5-116">Bokfør alle ordrer, fakturaer, kreditnotaer og ordrereturer.</span><span class="sxs-lookup"><span data-stu-id="1afb5-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="1afb5-117">Bokfør alle innbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="1afb5-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="1afb5-118">Oppdater og bokfør gjentakelseskladder som er relatert til salg.</span><span class="sxs-lookup"><span data-stu-id="1afb5-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="1afb5-119">Avstem kortsiktige fordringer mot Finans.</span><span class="sxs-lookup"><span data-stu-id="1afb5-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="1afb5-120">Kjør kjørselen **Slett fakturerte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="1afb5-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="1afb5-121">Kjøp</span><span class="sxs-lookup"><span data-stu-id="1afb5-121">Purchases and Payables</span></span>
* <span data-ttu-id="1afb5-122">Bokfør alle bestillinger, fakturaer, kreditnotaer og ordrereturer.</span><span class="sxs-lookup"><span data-stu-id="1afb5-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="1afb5-123">Bokfør alle utbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="1afb5-123">Post all payment journals.</span></span>  
* <span data-ttu-id="1afb5-124">Oppdater og bokfør gjentakelseskladder som er relatert til kjøp.</span><span class="sxs-lookup"><span data-stu-id="1afb5-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="1afb5-125">Kjør rapporten **Aldersfordelt saldoliste - lev.**, og avstem leverandørgjeld mot Finans.</span><span class="sxs-lookup"><span data-stu-id="1afb5-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="1afb5-126">Kjør kjørselen **Slett fakturerte bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="1afb5-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="1afb5-127">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="1afb5-127">Fixed Assets</span></span>
* <span data-ttu-id="1afb5-128">Bokfør all vedlikeholdskost gjennom aktivakladdene eller fakturaene.</span><span class="sxs-lookup"><span data-stu-id="1afb5-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="1afb5-129">Bokfør justeringer.</span><span class="sxs-lookup"><span data-stu-id="1afb5-129">Post adjustments.</span></span>
* <span data-ttu-id="1afb5-130">Bokfør oppskrivning.</span><span class="sxs-lookup"><span data-stu-id="1afb5-130">Post appreciation.</span></span>
* <span data-ttu-id="1afb5-131">Bokfør avskrivning.</span><span class="sxs-lookup"><span data-stu-id="1afb5-131">Post depreciation.</span></span>
* <span data-ttu-id="1afb5-132">Oppdater og bokfør gjentakende aktivakladd.</span><span class="sxs-lookup"><span data-stu-id="1afb5-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="1afb5-133">Konsernintern</span><span class="sxs-lookup"><span data-stu-id="1afb5-133">Intercompany</span></span>
* <span data-ttu-id="1afb5-134">Behandle konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="1afb5-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="1afb5-135">Beregn og behandle mva.</span><span class="sxs-lookup"><span data-stu-id="1afb5-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="1afb5-136">Fullfør mva-oppgaver.</span><span class="sxs-lookup"><span data-stu-id="1afb5-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1afb5-137">Se også</span><span class="sxs-lookup"><span data-stu-id="1afb5-137">See Also</span></span>
[<span data-ttu-id="1afb5-138">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="1afb5-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="1afb5-139">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="1afb5-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="1afb5-140">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1afb5-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
