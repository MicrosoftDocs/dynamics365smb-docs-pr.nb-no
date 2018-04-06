---
title: Registrere utgifter og inntekter direkte i Finans | Microsoft-dokumentasjon
description: "Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i Financials, for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer i Finanskladd-vinduet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b7e1fc0cda3dadfac73cf0c9a2e599aa78d06bd6
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="b14c4-103">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="b14c4-103">Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="b14c4-104">De fleste finanstransaksjoner bokføres i Finans via dedikerte forretningsdokumenter, for eksempel kjøpsfakturaer eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="b14c4-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="b14c4-105">Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer i **Finanskladd**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="b14c4-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="b14c4-106">Vanlig bruk av finanskladden er å bokføre ansattes utgifter av egne penger under forretningsaktiviteter for senere refusjon.</span><span class="sxs-lookup"><span data-stu-id="b14c4-106">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="b14c4-107">Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="b14c4-107">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="b14c4-108">Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.</span><span class="sxs-lookup"><span data-stu-id="b14c4-108">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="b14c4-109">Bokføring med en finanskladd oppretter alltid poster på finanskonti.</span><span class="sxs-lookup"><span data-stu-id="b14c4-109">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="b14c4-110">Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b14c4-110">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="b14c4-111">Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal.</span><span class="sxs-lookup"><span data-stu-id="b14c4-111">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="b14c4-112">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="b14c4-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="b14c4-113">I motsetning til poster som bokføres med dokumenter, som krever en kreditnotaprosess, kan du foreta riktig tilbakeføring av poster som bokføres med finanskladden.</span><span class="sxs-lookup"><span data-stu-id="b14c4-113">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="b14c4-114">Hvis du vil ha mer informasjon, kan du se [Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="b14c4-114">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="b14c4-115">Bokføre en transaksjon direkte på en finanskonto</span><span class="sxs-lookup"><span data-stu-id="b14c4-115">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="b14c4-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b14c4-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="b14c4-117">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="b14c4-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="b14c4-118">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="b14c4-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="b14c4-119">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="b14c4-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="b14c4-120">Gjenta trinn 3 for alle separate transaksjoner du vil bokføre.</span><span class="sxs-lookup"><span data-stu-id="b14c4-120">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="b14c4-121">Hvis du for eksempel vil angi flere transaksjonslinjer ovenfor én motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden i vinduet **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="b14c4-121">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="b14c4-122">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="b14c4-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="b14c4-123">Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.</span><span class="sxs-lookup"><span data-stu-id="b14c4-123">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="b14c4-124">Se også</span><span class="sxs-lookup"><span data-stu-id="b14c4-124">See Also</span></span>
[<span data-ttu-id="b14c4-125">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="b14c4-125">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="b14c4-126">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="b14c4-126">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="b14c4-127">Tilbakeføre bokføringer</span><span class="sxs-lookup"><span data-stu-id="b14c4-127">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="b14c4-128">Finans</span><span class="sxs-lookup"><span data-stu-id="b14c4-128">Finance</span></span>](finance.md)  
<span data-ttu-id="b14c4-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b14c4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

