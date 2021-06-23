---
title: Registrer og refunder ansattes firmarelaterte utgifter
description: Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184402"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="0c782-103">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="0c782-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0c782-104">støtter transaksjoner for ansatte på lignende måte som for leverandører.</span><span class="sxs-lookup"><span data-stu-id="0c782-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="0c782-105">Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.</span><span class="sxs-lookup"><span data-stu-id="0c782-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="0c782-106">Ansattes transaksjoner kan bare bokføres i den lokale valutaen.</span><span class="sxs-lookup"><span data-stu-id="0c782-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="0c782-107">Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.</span><span class="sxs-lookup"><span data-stu-id="0c782-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="0c782-108">Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0c782-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="0c782-109">Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.</span><span class="sxs-lookup"><span data-stu-id="0c782-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="0c782-110">Denne artikkelen forklarer hvordan du registrerer utgiftene i bøkene og hvordan du refunderer den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0c782-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="0c782-111">Organisasjonen kan ha en portal eller app der ansatte kan sende reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="0c782-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="0c782-112">[!INCLUDE [prod_short](includes/prod_short.md)] er fleksibel nok til å dekke mange forskjellige rutiner.</span><span class="sxs-lookup"><span data-stu-id="0c782-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="0c782-113">De nøyaktige kontonumrene som skal brukes, avhenger av organisasjonens konfigurasjon og prosesser.</span><span class="sxs-lookup"><span data-stu-id="0c782-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="0c782-114">Slik registrerer du utgifter for en ansatt</span><span class="sxs-lookup"><span data-stu-id="0c782-114">To record an employee's expense</span></span>

<span data-ttu-id="0c782-115">Du bokfører utgifter for de ansatte på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="0c782-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="0c782-116">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0c782-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0c782-117">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="0c782-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="0c782-118">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="0c782-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="0c782-119">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="0c782-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="0c782-120">Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0c782-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="0c782-121">Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="0c782-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="0c782-122">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.</span><span class="sxs-lookup"><span data-stu-id="0c782-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="0c782-123">Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="0c782-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="0c782-124">Slik refunderer du en ansatt</span><span class="sxs-lookup"><span data-stu-id="0c782-124">To reimburse an employee</span></span>

<span data-ttu-id="0c782-125">Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer på siden **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="0c782-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="0c782-126">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0c782-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c782-127">Åpne den relevante kjørselen for utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="0c782-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="0c782-128">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="0c782-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="0c782-129">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0c782-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="0c782-130">Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="0c782-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="0c782-131">Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.</span><span class="sxs-lookup"><span data-stu-id="0c782-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="0c782-132">Velg handlingen **Bokfør** for å registrere refusjonen.</span><span class="sxs-lookup"><span data-stu-id="0c782-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="0c782-133">Slik avstemmer du refusjoner med finansposter for ansatte</span><span class="sxs-lookup"><span data-stu-id="0c782-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="0c782-134">Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel på siden **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene.</span><span class="sxs-lookup"><span data-stu-id="0c782-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="0c782-135">Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="0c782-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="0c782-136">Du kan også utligne manuelt på siden **Ansattposter**.</span><span class="sxs-lookup"><span data-stu-id="0c782-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="0c782-137">Hvis du vil ha mer informasjon, kan du se relatert [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="0c782-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c782-138">Se også</span><span class="sxs-lookup"><span data-stu-id="0c782-138">See Also</span></span>

[<span data-ttu-id="0c782-139">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="0c782-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="0c782-140">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="0c782-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="0c782-141">Tilbakeføre kladdebokføringer og angre mottak/leveringer</span><span class="sxs-lookup"><span data-stu-id="0c782-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="0c782-142">Finans</span><span class="sxs-lookup"><span data-stu-id="0c782-142">Finance</span></span>](finance.md)  
<span data-ttu-id="0c782-143">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c782-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]