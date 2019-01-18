---
title: "Angre en bokføring ved å bokføre en tilbakeføringspost | Microsoft-dokumentasjon"
description: "Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: cc624d52ce61cea4a8e92bb7d37e07ad8c769393
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="reverse-postings"></a><span data-ttu-id="440d2-103">Tilbakeføre bokføringer</span><span class="sxs-lookup"><span data-stu-id="440d2-103">Reverse Postings</span></span>
<span data-ttu-id="440d2-104">Hvis du vil angre en feilaktig kladdebokføring, velger du posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten.</span><span class="sxs-lookup"><span data-stu-id="440d2-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="440d2-105">Når du har tilbakeført en post, må du lage den riktige posten.</span><span class="sxs-lookup"><span data-stu-id="440d2-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="440d2-106">Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="440d2-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="440d2-107">En post kan bare tilbakeføres én gang.</span><span class="sxs-lookup"><span data-stu-id="440d2-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="440d2-108">Hvis du vil ha mer informasjon om bokføring fra en finanskladd, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="440d2-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="440d2-109">Hvis du har utført en ukorrekt nagativ antallsbokføring, for eksempel en bestilling med galt vareantall, og bokført denne som mottatt (men ikke fakturert), kan du angre bokføringen.</span><span class="sxs-lookup"><span data-stu-id="440d2-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="440d2-110">Hvis du har utført en ukorrekt positiv antallsbokføring, for eksempel en bestillingsretur med galt vareantall, og bokført denne som sendt (men ikke fakturert), kan du angre bokføringen.</span><span class="sxs-lookup"><span data-stu-id="440d2-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="440d2-111">Tilbakeføre kladdebokføring av en finanspost</span><span class="sxs-lookup"><span data-stu-id="440d2-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="440d2-112">Du kan tilbakeføre poster fra alle **Poster**-sider.</span><span class="sxs-lookup"><span data-stu-id="440d2-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="440d2-113">Fremgangsmåten nedenfor er basert på siden **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="440d2-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="440d2-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Finansposter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="440d2-115">Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="440d2-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="440d2-116">Vær oppmerksom på at den må stamme fra en kladdebokføring.</span><span class="sxs-lookup"><span data-stu-id="440d2-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="440d2-117">På siden **Tilbakefør transaksjonsposter** velger du den relevante posten og deretter handlingen **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="440d2-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="440d2-118">Velg **Ja** i bekreftelsesmeldingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="440d2-119">Slik angrer du antallsbokføring på bokførte kjøpsmottak</span><span class="sxs-lookup"><span data-stu-id="440d2-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="440d2-120">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="440d2-121">Åpne det bokførte mottaket som du vil angre.</span><span class="sxs-lookup"><span data-stu-id="440d2-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="440d2-122">Velg linjen(e) du vil angre.</span><span class="sxs-lookup"><span data-stu-id="440d2-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="440d2-123">Velg **Angre mottak**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="440d2-124">Det settes inn en korreksjonslinje under den valgte mottakslinjen.</span><span class="sxs-lookup"><span data-stu-id="440d2-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="440d2-125">Hvis antallet ble mottatt i et lagermottak, settes en korreksjonslinje inn i det bokførte lagermottaket.</span><span class="sxs-lookup"><span data-stu-id="440d2-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="440d2-126">Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.</span><span class="sxs-lookup"><span data-stu-id="440d2-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="440d2-127">Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse</span><span class="sxs-lookup"><span data-stu-id="440d2-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="440d2-128">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="440d2-129">Åpne den bokførte returforsendelsen som du vil angre.</span><span class="sxs-lookup"><span data-stu-id="440d2-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="440d2-130">Velg linjen(e) du vil angre.</span><span class="sxs-lookup"><span data-stu-id="440d2-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="440d2-131">Velg handlingen **Angre returforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="440d2-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="440d2-132">En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.</span><span class="sxs-lookup"><span data-stu-id="440d2-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="440d2-133">Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.</span><span class="sxs-lookup"><span data-stu-id="440d2-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="440d2-134">Noter nummeret i feltet **Ordrereturnr.** på siden **Bokført bestillingsreturseddel**.</span><span class="sxs-lookup"><span data-stu-id="440d2-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="440d2-135">.</span><span class="sxs-lookup"><span data-stu-id="440d2-135">field.</span></span>  
6.  <span data-ttu-id="440d2-136">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="440d2-137">Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="440d2-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="440d2-138">Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.</span><span class="sxs-lookup"><span data-stu-id="440d2-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="440d2-139">Bokføre en negativ post</span><span class="sxs-lookup"><span data-stu-id="440d2-139">To post a negative entry</span></span>  
<span data-ttu-id="440d2-140">Du kan bruke **Korreksjon**-feltet til å bokføre en negativ debet i stedet for en kredit, eller til å bokfører en negativ kredit i stedet for en debet på kontoen.</span><span class="sxs-lookup"><span data-stu-id="440d2-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="440d2-141">For å dekke juridiske krav vises dette feltet som standard i alle kladder.</span><span class="sxs-lookup"><span data-stu-id="440d2-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="440d2-142">Feltet **Debetbeløp** og **Kreditbeløp** omfatter den opprinnelige posten og den korrigert posten.</span><span class="sxs-lookup"><span data-stu-id="440d2-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="440d2-143">Disse feltene har ingen innvirkning på kontoens saldo.</span><span class="sxs-lookup"><span data-stu-id="440d2-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="440d2-144">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="440d2-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="440d2-145">Velg ønsket kladdenavn i **Bunkenavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="440d2-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="440d2-146">Angi informasjon i de aktuelle feltene.</span><span class="sxs-lookup"><span data-stu-id="440d2-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="440d2-147">På kladdelinjen som du vil aktivere for negative poster merker du av for **Korreksjon**.</span><span class="sxs-lookup"><span data-stu-id="440d2-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="440d2-148">Hvis du vil bokføre kladden, velger du **Bokfør** og deretter **Ja**.</span><span class="sxs-lookup"><span data-stu-id="440d2-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="440d2-149">Se også</span><span class="sxs-lookup"><span data-stu-id="440d2-149">See Also</span></span>
[<span data-ttu-id="440d2-150">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="440d2-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="440d2-151">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="440d2-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="440d2-152">Finans</span><span class="sxs-lookup"><span data-stu-id="440d2-152">Finance</span></span>](finance.md)  
<span data-ttu-id="440d2-153">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="440d2-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

