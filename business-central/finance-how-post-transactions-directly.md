---
title: Registrere utgifter og inntekter direkte i Finans | Microsoft-dokumentasjon
description: Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i Financials, for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer på Finanskladd-siden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 54f2cf573d12c50ba26c26fd4c11ad20a1d52db3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "937460"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="af3c2-103">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="af3c2-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="af3c2-104">Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.</span><span class="sxs-lookup"><span data-stu-id="af3c2-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="af3c2-105">Vanlig bruk av finanskladden er å bokføre ansattes utgifter av egne penger under forretningsaktiviteter for senere refusjon.</span><span class="sxs-lookup"><span data-stu-id="af3c2-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="af3c2-106">Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="af3c2-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="af3c2-107">Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.</span><span class="sxs-lookup"><span data-stu-id="af3c2-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="af3c2-108">Bokføring med en finanskladd oppretter alltid poster på finanskonti.</span><span class="sxs-lookup"><span data-stu-id="af3c2-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="af3c2-109">Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="af3c2-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="af3c2-110">Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal.</span><span class="sxs-lookup"><span data-stu-id="af3c2-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="af3c2-111">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="af3c2-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="af3c2-112">I motsetning til poster som bokføres med dokumenter, som krever en kreditnotaprosess, kan du foreta riktig tilbakeføring av poster som bokføres med finanskladden.</span><span class="sxs-lookup"><span data-stu-id="af3c2-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="af3c2-113">Hvis du vil ha mer informasjon, kan du se [Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="af3c2-113">For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="af3c2-114">Bokføre en transaksjon direkte på en finanskonto</span><span class="sxs-lookup"><span data-stu-id="af3c2-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="af3c2-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="af3c2-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="af3c2-116">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="af3c2-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="af3c2-117">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="af3c2-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="af3c2-118">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="af3c2-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="af3c2-119">Gjenta trinn 3 for alle separate transaksjoner du vil bokføre.</span><span class="sxs-lookup"><span data-stu-id="af3c2-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="af3c2-120">Hvis du for eksempel vil angi flere transaksjonslinjer ovenfor én motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="af3c2-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="af3c2-121">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="af3c2-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="af3c2-122">Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.</span><span class="sxs-lookup"><span data-stu-id="af3c2-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="af3c2-123">Se også</span><span class="sxs-lookup"><span data-stu-id="af3c2-123">See Also</span></span>

[<span data-ttu-id="af3c2-124">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="af3c2-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="af3c2-125">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="af3c2-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="af3c2-126">Tilbakeføre bokføringer</span><span class="sxs-lookup"><span data-stu-id="af3c2-126">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="af3c2-127">Finans</span><span class="sxs-lookup"><span data-stu-id="af3c2-127">Finance</span></span>](finance.md)  
<span data-ttu-id="af3c2-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af3c2-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
