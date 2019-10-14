---
title: Angre en bokføring ved å bokføre en tilbakeføringspost | Microsoft-dokumentasjon
description: Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 808459f9c77d797c58a5956a5641c97bc398734e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306223"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a><span data-ttu-id="603ce-103">Tilbakeføre kladdebokføringer og angre mottak/leveringer</span><span class="sxs-lookup"><span data-stu-id="603ce-103">Reverse Journal Postings and Undo Receipts/Shipments</span></span>
<span data-ttu-id="603ce-104">Hvis du vil angre en feilaktig kladdebokføring, velger du posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten.</span><span class="sxs-lookup"><span data-stu-id="603ce-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="603ce-105">Når du har tilbakeført en post, må du lage den riktige posten.</span><span class="sxs-lookup"><span data-stu-id="603ce-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="603ce-106">Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje.</span><span class="sxs-lookup"><span data-stu-id="603ce-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="603ce-107">En post kan bare tilbakeføres én gang.</span><span class="sxs-lookup"><span data-stu-id="603ce-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="603ce-108">Hvis du vil angre en mottaks- eller leveringsbokføring, kan du bruke funksjonen **Angre** på det bokførte bilaget før de bokføres som fakturert.</span><span class="sxs-lookup"><span data-stu-id="603ce-108">To undo a receipt or shipment posting, before they are posted as invoiced, you can use the **Undo** function on the posted document.</span></span> <span data-ttu-id="603ce-109">Du kan angre mengder av typen **Vare**.</span><span class="sxs-lookup"><span data-stu-id="603ce-109">You can undo quantities of type **Item**.</span></span>

<span data-ttu-id="603ce-110">Hvis du har utført en ukorrekt negativ antallsbokføring, for eksempel en bestilling med galt vareantall, og bokført denne som mottatt (men ikke fakturert), kan du angre bokføringen.</span><span class="sxs-lookup"><span data-stu-id="603ce-110">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items, and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="603ce-111">Hvis du har utført en ukorrekt positiv antallsbokføring, for eksempel en følgeseddelen eller bestillingsreturforsendelse med galt vareantall, og bokført denne som sendt, men ikke fakturert, kan du angre bokføringen.</span><span class="sxs-lookup"><span data-stu-id="603ce-111">If you have made an incorrect positive quantity posting, such as a sales shipment or a purchase return shipment with the wrong number of items, and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="603ce-112">Tilbakeføre kladdebokføring av en finanspost</span><span class="sxs-lookup"><span data-stu-id="603ce-112">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="603ce-113">Du kan tilbakeføre poster fra alle **Poster**-sider.</span><span class="sxs-lookup"><span data-stu-id="603ce-113">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="603ce-114">Fremgangsmåten nedenfor er basert på siden **Finansposter**.</span><span class="sxs-lookup"><span data-stu-id="603ce-114">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="603ce-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Finansposter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="603ce-116">Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="603ce-116">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="603ce-117">Vær oppmerksom på at den må stamme fra en kladdebokføring.</span><span class="sxs-lookup"><span data-stu-id="603ce-117">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="603ce-118">På siden **Tilbakefør transaksjonsposter** velger du den relevante posten og deretter handlingen **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="603ce-118">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="603ce-119">Velg **Ja** i bekreftelsesmeldingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-119">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="603ce-120">Bokføre en negativ post</span><span class="sxs-lookup"><span data-stu-id="603ce-120">To post a negative entry</span></span>  
<span data-ttu-id="603ce-121">Du kan bruke **Korreksjon**-feltet til å bokføre en negativ debet i stedet for en kredit, eller til å bokfører en negativ kredit i stedet for en debet på kontoen.</span><span class="sxs-lookup"><span data-stu-id="603ce-121">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="603ce-122">For å dekke juridiske krav vises dette feltet som standard i alle kladder.</span><span class="sxs-lookup"><span data-stu-id="603ce-122">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="603ce-123">Feltet **Debetbeløp** og **Kreditbeløp** omfatter den opprinnelige posten og den korrigert posten.</span><span class="sxs-lookup"><span data-stu-id="603ce-123">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="603ce-124">Disse feltene har ingen innvirkning på kontoens saldo.</span><span class="sxs-lookup"><span data-stu-id="603ce-124">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="603ce-125">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="603ce-126">Velg ønsket kladdenavn i **Bunkenavn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="603ce-126">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="603ce-127">Angi informasjon i de aktuelle feltene.</span><span class="sxs-lookup"><span data-stu-id="603ce-127">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="603ce-128">På kladdelinjen som du vil aktivere for negative poster merker du av for **Korreksjon**.</span><span class="sxs-lookup"><span data-stu-id="603ce-128">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="603ce-129">Hvis du vil bokføre kladden, velger du **Bokfør** og deretter **Ja**.</span><span class="sxs-lookup"><span data-stu-id="603ce-129">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="603ce-130">Slik angrer du antallsbokføring på bokførte kjøpsmottak</span><span class="sxs-lookup"><span data-stu-id="603ce-130">To undo a quantity posting on a posted purchase receipt</span></span>  
<span data-ttu-id="603ce-131">Nedenfor beskrives hvordan du angrer et bokført mottak.</span><span class="sxs-lookup"><span data-stu-id="603ce-131">The following described how to undo a posted receipt.</span></span> <span data-ttu-id="603ce-132">Trinnene er de samme for bokførte leveringer.</span><span class="sxs-lookup"><span data-stu-id="603ce-132">The steps are similar for posted shipments.</span></span>

1.  <span data-ttu-id="603ce-133">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="603ce-134">Åpne det bokførte mottaket som du vil angre.</span><span class="sxs-lookup"><span data-stu-id="603ce-134">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="603ce-135">Velg linjen(e) du vil angre.</span><span class="sxs-lookup"><span data-stu-id="603ce-135">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="603ce-136">Velg **Angre mottak**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-136">Choose **Undo Receipt** action.</span></span>

<span data-ttu-id="603ce-137">Det settes inn en korreksjonslinje under den valgte mottakslinjen.</span><span class="sxs-lookup"><span data-stu-id="603ce-137">A corrective line is inserted under the selected receipt line.</span></span> <span data-ttu-id="603ce-138">Hvis antallet ble mottatt i et lagermottak, settes en korreksjonslinje inn i det bokførte lagermottaket.</span><span class="sxs-lookup"><span data-stu-id="603ce-138">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

<span data-ttu-id="603ce-139">Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.</span><span class="sxs-lookup"><span data-stu-id="603ce-139">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="603ce-140">Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse</span><span class="sxs-lookup"><span data-stu-id="603ce-140">To undo and then redo a quantity posting on a posted return shipment</span></span>
<span data-ttu-id="603ce-141">Følgende beskriver hvordan du angrer en bokført returforsendelse og deretter bokfører bestillingsreturen med et nytt antall.</span><span class="sxs-lookup"><span data-stu-id="603ce-141">The following described how to undo a posted return shipment and then repost the purchase return with a new quantity.</span></span>

1.  <span data-ttu-id="603ce-142">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="603ce-143">Åpne den bokførte returforsendelsen som du vil angre.</span><span class="sxs-lookup"><span data-stu-id="603ce-143">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="603ce-144">Velg linjen(e) du vil angre.</span><span class="sxs-lookup"><span data-stu-id="603ce-144">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="603ce-145">Velg handlingen **Angre returforsendelse**.</span><span class="sxs-lookup"><span data-stu-id="603ce-145">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="603ce-146">En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.</span><span class="sxs-lookup"><span data-stu-id="603ce-146">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="603ce-147">Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.</span><span class="sxs-lookup"><span data-stu-id="603ce-147">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="603ce-148">Noter nummeret i feltet **Ordrereturnr.** på siden **Bokført bestillingsreturseddel**.</span><span class="sxs-lookup"><span data-stu-id="603ce-148">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="603ce-149">.</span><span class="sxs-lookup"><span data-stu-id="603ce-149">field.</span></span>  
6.  <span data-ttu-id="603ce-150">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="603ce-150">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="603ce-151">Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.</span><span class="sxs-lookup"><span data-stu-id="603ce-151">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="603ce-152">Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.</span><span class="sxs-lookup"><span data-stu-id="603ce-152">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="see-also"></a><span data-ttu-id="603ce-153">Se også</span><span class="sxs-lookup"><span data-stu-id="603ce-153">See Also</span></span>
[<span data-ttu-id="603ce-154">Angre monteringsbokføring</span><span class="sxs-lookup"><span data-stu-id="603ce-154">Undo Assembly Posting</span></span>](assembly-how-to-undo-assembly-posting.md)  
[<span data-ttu-id="603ce-155">Bokføre transaksjoner direkte i Finans</span><span class="sxs-lookup"><span data-stu-id="603ce-155">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="603ce-156">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="603ce-156">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="603ce-157">Finans</span><span class="sxs-lookup"><span data-stu-id="603ce-157">Finance</span></span>](finance.md)  
<span data-ttu-id="603ce-158">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="603ce-158">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
