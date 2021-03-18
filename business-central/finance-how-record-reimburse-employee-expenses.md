---
title: Registrere og refundere ansattes firmarelaterte utgifter | Microsoft-dokumentasjon
description: Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 82fc662bee4fd288dda3a5e546fa408b2bef1ce4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391502"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="0d123-103">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="0d123-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0d123-104">støtter transaksjoner for en ansatt på lignende måte som for leverandører.</span><span class="sxs-lookup"><span data-stu-id="0d123-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="0d123-105">Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.</span><span class="sxs-lookup"><span data-stu-id="0d123-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="0d123-106">Ansattes transaksjoner kan bare bokføres i den lokale valutaen.</span><span class="sxs-lookup"><span data-stu-id="0d123-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="0d123-107">Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.</span><span class="sxs-lookup"><span data-stu-id="0d123-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="0d123-108">Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0d123-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="0d123-109">Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.</span><span class="sxs-lookup"><span data-stu-id="0d123-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="0d123-110">Denne artikkelen forklarer hvordan du registrerer utgiftene i bøkene og hvordan du refunderer den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0d123-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="0d123-111">Organisasjonen kan ha en portal eller app der ansatte kan sende reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0d123-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="0d123-112">Slik registrerer du utgifter for en ansatt</span><span class="sxs-lookup"><span data-stu-id="0d123-112">To record an employee's expense</span></span>
<span data-ttu-id="0d123-113">Du bokfører utgifter for de ansatte på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="0d123-113">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="0d123-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0d123-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d123-115">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="0d123-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="0d123-116">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="0d123-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="0d123-117">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="0d123-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="0d123-118">Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0d123-118">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="0d123-119">Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="0d123-119">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="0d123-120">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.</span><span class="sxs-lookup"><span data-stu-id="0d123-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="0d123-121">Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0d123-121">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="0d123-122">Slik refunderer du en ansatt</span><span class="sxs-lookup"><span data-stu-id="0d123-122">To reimburse an employee</span></span>
<span data-ttu-id="0d123-123">Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer på siden **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="0d123-123">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="0d123-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0d123-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="0d123-125">Åpne den relevante kjørselen for utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="0d123-125">Open the relevant payment journal batch.</span></span> <span data-ttu-id="0d123-126">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="0d123-126">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="0d123-127">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0d123-127">Fill in the fields as necessary.</span></span> <span data-ttu-id="0d123-128">Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="0d123-128">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="0d123-129">Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.</span><span class="sxs-lookup"><span data-stu-id="0d123-129">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="0d123-130">Velg handlingen **Bokfør** for å registrere refusjonen.</span><span class="sxs-lookup"><span data-stu-id="0d123-130">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="0d123-131">Slik avstemmer du refusjoner med finansposter for ansatte</span><span class="sxs-lookup"><span data-stu-id="0d123-131">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="0d123-132">Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel på siden **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene.</span><span class="sxs-lookup"><span data-stu-id="0d123-132">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="0d123-133">Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="0d123-133">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="0d123-134">Du kan også utligne manuelt på siden **Ansattposter**.</span><span class="sxs-lookup"><span data-stu-id="0d123-134">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="0d123-135">Hvis du vil ha mer informasjon, kan du se relatert [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="0d123-135">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d123-136">Se også</span><span class="sxs-lookup"><span data-stu-id="0d123-136">See Also</span></span>
[<span data-ttu-id="0d123-137">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="0d123-137">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="0d123-138">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="0d123-138">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="0d123-139">Tilbakeføre kladdebokføringer og angre mottak/leveringer</span><span class="sxs-lookup"><span data-stu-id="0d123-139">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="0d123-140">Finans</span><span class="sxs-lookup"><span data-stu-id="0d123-140">Finance</span></span>](finance.md)  
<span data-ttu-id="0d123-141">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d123-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]