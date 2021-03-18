---
title: Registrere utgifter og inntekter direkte i Finans | Microsoft-dokumentasjon
description: Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i Financials, for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer på Finanskladd-siden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 04fb69cb471596065df0a05deefe51080bd2fdbd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386427"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="6a171-103">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="6a171-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="6a171-104">Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.</span><span class="sxs-lookup"><span data-stu-id="6a171-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="6a171-105">Vanlig bruk av finanskladden er å bokføre ansattes utgifter av egne penger under forretningsaktiviteter for senere refusjon.</span><span class="sxs-lookup"><span data-stu-id="6a171-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="6a171-106">Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="6a171-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="6a171-107">Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.</span><span class="sxs-lookup"><span data-stu-id="6a171-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="6a171-108">Bokføring med en finanskladd oppretter alltid poster på finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6a171-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="6a171-109">Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6a171-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="6a171-110">Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal.</span><span class="sxs-lookup"><span data-stu-id="6a171-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="6a171-111">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6a171-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="6a171-112">I motsetning til poster som bokføres med dokumenter, som krever en kreditnotaprosess, kan du foreta riktig tilbakeføring av poster som bokføres med finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6a171-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="6a171-113">Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="6a171-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="6a171-114">Bokføre en transaksjon direkte på en finanskonto</span><span class="sxs-lookup"><span data-stu-id="6a171-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="6a171-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="6a171-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="6a171-116">Åpne den relevante finanskladden.</span><span class="sxs-lookup"><span data-stu-id="6a171-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="6a171-117">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="6a171-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="6a171-118">Fyll ut feltene etter behov på en ny kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="6a171-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="6a171-119">Gjenta trinn 3 for alle separate transaksjoner du vil bokføre.</span><span class="sxs-lookup"><span data-stu-id="6a171-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="6a171-120">Hvis du for eksempel vil angi flere transaksjonslinjer ovenfor én motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="6a171-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="6a171-121">Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="6a171-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="6a171-122">Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.</span><span class="sxs-lookup"><span data-stu-id="6a171-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a171-123">Se også</span><span class="sxs-lookup"><span data-stu-id="6a171-123">See Also</span></span>

[<span data-ttu-id="6a171-124">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="6a171-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="6a171-125">Registrere og refundere ansattes utgifter</span><span class="sxs-lookup"><span data-stu-id="6a171-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="6a171-126">Tilbakeføre kladdebokføringer og angre mottak/leveringer</span><span class="sxs-lookup"><span data-stu-id="6a171-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="6a171-127">Finans</span><span class="sxs-lookup"><span data-stu-id="6a171-127">Finance</span></span>](finance.md)  
<span data-ttu-id="6a171-128">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6a171-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]