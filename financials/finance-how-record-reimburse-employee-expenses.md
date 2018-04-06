---
title: Registrere og refundere ansattes firmarelaterte utgifter | Microsoft-dokumentasjon
description: "Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c12561f4851cd75bdc4098e506c113e50d3bc3be
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="5155a-103">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="5155a-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5155a-104"> støtter transaksjoner for en ansatt på lignende måte som for leverandører.</span><span class="sxs-lookup"><span data-stu-id="5155a-104"> supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="5155a-105">Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.</span><span class="sxs-lookup"><span data-stu-id="5155a-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="5155a-106">Ansattes transaksjoner kan bare bokføres i den lokale valutaen.</span><span class="sxs-lookup"><span data-stu-id="5155a-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="5155a-107">Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.</span><span class="sxs-lookup"><span data-stu-id="5155a-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="5155a-108">Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="5155a-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="5155a-109">Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.</span><span class="sxs-lookup"><span data-stu-id="5155a-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="5155a-110">Slik registrerer du utgifter for en ansatt</span><span class="sxs-lookup"><span data-stu-id="5155a-110">To record an employee's expense</span></span>
<span data-ttu-id="5155a-111">Du bokfører utgifter for de ansatte i vinduet **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="5155a-111">You post employees' expenses in the **General Journal** window.</span></span>
1. <span data-ttu-id="5155a-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5155a-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="5155a-113">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="5155a-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="5155a-114">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="5155a-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="5155a-115">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="5155a-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="5155a-116">Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="5155a-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="5155a-117">Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden i vinduet **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="5155a-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="5155a-118">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.</span><span class="sxs-lookup"><span data-stu-id="5155a-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="5155a-119">Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="5155a-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="5155a-120">Slik refunderer du en ansatt</span><span class="sxs-lookup"><span data-stu-id="5155a-120">To reimburse an employee</span></span>
<span data-ttu-id="5155a-121">Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer i vinduet **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="5155a-121">You reimburse employees by posting payments to their bank account in the **Payment Journal** window.</span></span>
1. <span data-ttu-id="5155a-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5155a-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="5155a-123">Åpne den relevante kjørselen for utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="5155a-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="5155a-124">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="5155a-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="5155a-125">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="5155a-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="5155a-126">Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="5155a-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="5155a-127">Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.</span><span class="sxs-lookup"><span data-stu-id="5155a-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="5155a-128">Velg handlingen **Bokfør** for å registrere refusjonen.</span><span class="sxs-lookup"><span data-stu-id="5155a-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="5155a-129">Slik avstemmer du refusjoner med finansposter for ansatte</span><span class="sxs-lookup"><span data-stu-id="5155a-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="5155a-130">Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel vinduet **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene.</span><span class="sxs-lookup"><span data-stu-id="5155a-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example in the **Payment Reconciliation Journal** window, based on the related bank statement entries.</span></span> <span data-ttu-id="5155a-131">Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="5155a-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="5155a-132">Du kan også utligne manuelt i vinduet **Ansattposter**.</span><span class="sxs-lookup"><span data-stu-id="5155a-132">Alternatively, you can apply manually in the **Employee Ledger Entries** window.</span></span> <span data-ttu-id="5155a-133">Hvis du vil ha mer informasjon, kan du se det relaterte emnet [Avstemme leverandørbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="5155a-133">For more information, see the related [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="5155a-134">Se også</span><span class="sxs-lookup"><span data-stu-id="5155a-134">See Also</span></span>
[<span data-ttu-id="5155a-135">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="5155a-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="5155a-136">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="5155a-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="5155a-137">Tilbakeføre bokføringer</span><span class="sxs-lookup"><span data-stu-id="5155a-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="5155a-138">Finans</span><span class="sxs-lookup"><span data-stu-id="5155a-138">Finance</span></span>](finance.md)  
<span data-ttu-id="5155a-139">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5155a-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

