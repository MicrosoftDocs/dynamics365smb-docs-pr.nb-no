---
title: Registrere og refundere ansattes firmarelaterte utgifter | Microsoft-dokumentasjon
description: Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 660cb4d9f2238bffeb1c7eaf49d5d70dbb654f45
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244794"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="6d8c4-103">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="6d8c4-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="6d8c4-104">støtter transaksjoner for en ansatt på lignende måte som for leverandører.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="6d8c4-105">Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="6d8c4-106">Ansattes transaksjoner kan bare bokføres i den lokale valutaen.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="6d8c4-107">Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="6d8c4-108">Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="6d8c4-109">Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="6d8c4-110">Slik registrerer du utgifter for en ansatt</span><span class="sxs-lookup"><span data-stu-id="6d8c4-110">To record an employee's expense</span></span>
<span data-ttu-id="6d8c4-111">Du bokfører utgifter for de ansatte på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-111">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="6d8c4-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="6d8c4-113">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="6d8c4-114">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6d8c4-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="6d8c4-115">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="6d8c4-116">Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="6d8c4-117">Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="6d8c4-118">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="6d8c4-119">Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="6d8c4-120">Slik refunderer du en ansatt</span><span class="sxs-lookup"><span data-stu-id="6d8c4-120">To reimburse an employee</span></span>
<span data-ttu-id="6d8c4-121">Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer på siden **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-121">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="6d8c4-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="6d8c4-123">Åpne den relevante kjørselen for utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="6d8c4-124">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6d8c4-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="6d8c4-125">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="6d8c4-126">Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="6d8c4-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="6d8c4-127">Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="6d8c4-128">Velg handlingen **Bokfør** for å registrere refusjonen.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="6d8c4-129">Slik avstemmer du refusjoner med finansposter for ansatte</span><span class="sxs-lookup"><span data-stu-id="6d8c4-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="6d8c4-130">Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel på siden **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="6d8c4-131">Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="6d8c4-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="6d8c4-132">Du kan også utligne manuelt på siden **Ansattposter**.</span><span class="sxs-lookup"><span data-stu-id="6d8c4-132">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="6d8c4-133">Hvis du vil ha mer informasjon, kan du se relatert [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="6d8c4-133">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="6d8c4-134">Se også</span><span class="sxs-lookup"><span data-stu-id="6d8c4-134">See Also</span></span>
[<span data-ttu-id="6d8c4-135">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="6d8c4-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="6d8c4-136">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="6d8c4-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="6d8c4-137">Tilbakeføre bokføringer</span><span class="sxs-lookup"><span data-stu-id="6d8c4-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="6d8c4-138">Finans</span><span class="sxs-lookup"><span data-stu-id="6d8c4-138">Finance</span></span>](finance.md)  
<span data-ttu-id="6d8c4-139">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6d8c4-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
