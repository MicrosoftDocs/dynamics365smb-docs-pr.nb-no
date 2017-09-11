---
title: "Angre en kladdebokføring ved å bokføre en tilbakeføringspost | Microsoft-dokumentasjon"
description: "Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="f0726-103">Tilbakeføre kladdebokføringer</span><span class="sxs-lookup"><span data-stu-id="f0726-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="f0726-104">Hvis du vil angre en feilaktig kladdebokføring, velger du posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten.</span><span class="sxs-lookup"><span data-stu-id="f0726-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="f0726-105">Når du har tilbakeført en post, må du lage den riktige posten.</span><span class="sxs-lookup"><span data-stu-id="f0726-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="f0726-106">Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="f0726-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="f0726-107">En post kan bare tilbakeføres én gang.</span><span class="sxs-lookup"><span data-stu-id="f0726-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="f0726-108">Hvis du vil ha mer informasjon om bokføring fra en finanskladd, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="f0726-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="f0726-109">Du kan tilbakeføre poster i alle **Poster**-vinduer.</span><span class="sxs-lookup"><span data-stu-id="f0726-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="f0726-110">Fremgangsmåten nedenfor er basert på vinduet **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="f0726-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="f0726-111">Tilbakeføre kladdebokføring av en finanspost</span><span class="sxs-lookup"><span data-stu-id="f0726-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="f0726-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finansposter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f0726-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="f0726-113">Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="f0726-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="f0726-114">Vær oppmerksom på at den må stamme fra en kladdebokføring.</span><span class="sxs-lookup"><span data-stu-id="f0726-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="f0726-115">I vinduet **Tilbakefør transaksjonsposter** velger du den relevante posten og deretter handlingen **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="f0726-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="f0726-116">Velg **Ja** i bekreftelsesmeldingen.</span><span class="sxs-lookup"><span data-stu-id="f0726-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0726-117">Se også</span><span class="sxs-lookup"><span data-stu-id="f0726-117">See Also</span></span>
[<span data-ttu-id="f0726-118">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="f0726-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="f0726-119">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="f0726-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="f0726-120">Finans</span><span class="sxs-lookup"><span data-stu-id="f0726-120">Finance</span></span>](finance.md)  
<span data-ttu-id="f0726-121">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f0726-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

