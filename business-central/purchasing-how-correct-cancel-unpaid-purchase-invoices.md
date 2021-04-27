---
title: Endre eller annullere ubetalte kjøpsfakturaer | Microsoft-dokumentasjon
description: Forklarer hvordan du korrigerer, annullerer eller angrer en bokført kjøpsfaktura og oppretter en kjøpskreditnota automatisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2e2e64cd3845f20e9c3e0fea5c114ebcd08491d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780235"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="2c610-103">Korrigere eller annullere ubetalte kjøpsfakturaer</span><span class="sxs-lookup"><span data-stu-id="2c610-103">Correct or Cancel Unpaid Purchase Invoices</span></span>

<span data-ttu-id="2c610-104">Du kan korrigere eller annullere en bokført kjøpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="2c610-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="2c610-105">Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="2c610-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="2c610-106">Hvis du allerede har betalt for produkter på den bokførte kjøpsfakturaen, kan du ikke rette eller avbryte den fra den bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c610-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="2c610-107">I stedet må du manuelt opprette en kjøpskreditnota for å tilbakeføre kjøpet, eventuelt behandlet med en bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="2c610-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="2c610-108">Det samme gjelder hvis du vil endre en bokført kjøpsfaktura som er basert på kombinerte kjøpsmottak.</span><span class="sxs-lookup"><span data-stu-id="2c610-108">The same applies if you want to modify a posted purchase invoice that was based on combined purchase receipts.</span></span> <span data-ttu-id="2c610-109">Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="2c610-109">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="2c610-110">På siden **Bokført kjøpsfaktura** kan du velge knappen **Korriger** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="2c610-110">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="2c610-111">Når du korrigerer eller annullerer en bokført kjøpsfaktura, utlignes den korrigerende kjøpskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige kjøpsfakturaen ble bokført.</span><span class="sxs-lookup"><span data-stu-id="2c610-111">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="2c610-112">Dette tilbakefører den bokførte kjøpsfakturaen i finanspostene og etterlater den korrigerende bokførte kjøpskreditnotaen for revisjonssporingen.</span><span class="sxs-lookup"><span data-stu-id="2c610-112">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="2c610-113">Nedenfor beskrives bruk av **Korriger** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="2c610-113">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="2c610-114">Slik korrigerer du en bokført kjøpsfaktura:</span><span class="sxs-lookup"><span data-stu-id="2c610-114">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="2c610-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c610-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c610-116">Velg den bokførte kjøpsfakturaen du vil korrigere.</span><span class="sxs-lookup"><span data-stu-id="2c610-116">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="2c610-117">Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte kjøpsfakturaen fordi den allerede er korrigert eller annullert.</span><span class="sxs-lookup"><span data-stu-id="2c610-117">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="2c610-118">På siden **Bokført kjøpsfaktura** velger du **Korriger**.</span><span class="sxs-lookup"><span data-stu-id="2c610-118">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="2c610-119">Det opprettes en ny kjøpsfaktura med den samme informasjonen, der du kan foreta korrigeringen.</span><span class="sxs-lookup"><span data-stu-id="2c610-119">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="2c610-120">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="2c610-120">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="2c610-121">Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2c610-121">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="2c610-122">En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c610-122">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="2c610-123">Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c610-123">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="2c610-124">Slik annullerer du en bokført kjøpsfaktura:</span><span class="sxs-lookup"><span data-stu-id="2c610-124">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="2c610-125">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c610-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c610-126">Velg den bokførte kjøpsfakturaen du vil avbryte.</span><span class="sxs-lookup"><span data-stu-id="2c610-126">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="2c610-127">Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte kjøpsfakturaen fordi den allerede er annullert eller korrigert.</span><span class="sxs-lookup"><span data-stu-id="2c610-127">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="2c610-128">På siden **Bokført kjøpsfaktura** velger du **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="2c610-128">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="2c610-129">En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c610-129">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="2c610-130">Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2c610-130">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="2c610-131">Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c610-131">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="2c610-132">Delvis fakturabokføring støttes også</span><span class="sxs-lookup"><span data-stu-id="2c610-132">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="2c610-133">Hvis annulleringen er knyttet til en delvis fakturabokføring, oppdateres den opprinnelige bestillingslinjen for å gjenspeile det annullerte fakturerte antallet.</span><span class="sxs-lookup"><span data-stu-id="2c610-133">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="2c610-134">Feltene **Ant. som skal fakt.** og **Ant. fakturert** på den tilknyttede bestillingslinjen tilbakestilles til verdiene før den delvise bokføringen.</span><span class="sxs-lookup"><span data-stu-id="2c610-134">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c610-135">Se også</span><span class="sxs-lookup"><span data-stu-id="2c610-135">See Also</span></span>
[<span data-ttu-id="2c610-136">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2c610-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="2c610-137">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="2c610-137">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="2c610-138">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2c610-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]