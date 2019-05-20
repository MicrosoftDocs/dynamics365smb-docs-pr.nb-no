---
title: Endre eller annullere ubetalte kjøpsfakturaer | Microsoft-dokumentasjon
description: Forklarer hvordan du korrigerer, annullerer eller angrer en bokført kjøpsfaktura og oppretter en kjøpskreditnota automatisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 76ef3837801a5841a39228f956db48caba264336
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252576"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="93bc9-103">Korrigere eller annullere ubetalte kjøpsfakturaer</span><span class="sxs-lookup"><span data-stu-id="93bc9-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="93bc9-104">Du kan korrigere eller annullere en bokført kjøpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="93bc9-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="93bc9-105">Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="93bc9-106">Hvis du allerede har betalt for produkter på den bokførte kjøpsfakturaen, kan du ikke rette eller avbryte den fra den bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="93bc9-107">I stedet må du manuelt opprette en kjøpskreditnota for å tilbakeføre kjøpet, eventuelt behandlet med en bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="93bc9-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="93bc9-108">Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="93bc9-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="93bc9-109">På siden **Bokført kjøpsfaktura** kan du velge knappen **Korriger** eller **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="93bc9-110">Når du korrigerer eller annullerer en bokført kjøpsfaktura, utlignes den korrigerende kjøpskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige kjøpsfakturaen ble bokført.</span><span class="sxs-lookup"><span data-stu-id="93bc9-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="93bc9-111">Dette tilbakefører den bokførte kjøpsfakturaen i finanspostene og etterlater den korrigerende bokførte kjøpskreditnotaen for revisjonssporingen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="93bc9-112">Nedenfor beskrives bruk av **Korriger** og **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="93bc9-113">Slik korrigerer du en bokført kjøpsfaktura:</span><span class="sxs-lookup"><span data-stu-id="93bc9-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="93bc9-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93bc9-115">Velg den bokførte kjøpsfakturaen du vil korrigere.</span><span class="sxs-lookup"><span data-stu-id="93bc9-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="93bc9-116">Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte kjøpsfakturaen fordi den allerede er korrigert eller annullert.</span><span class="sxs-lookup"><span data-stu-id="93bc9-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="93bc9-117">På siden **Bokført kjøpsfaktura** velger du **Korriger**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="93bc9-118">Det opprettes en ny kjøpsfaktura med den samme informasjonen, der du kan foreta korrigeringen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="93bc9-119">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="93bc9-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="93bc9-120">Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="93bc9-121">En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="93bc9-122">Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="93bc9-123">Slik annullerer du en bokført kjøpsfaktura:</span><span class="sxs-lookup"><span data-stu-id="93bc9-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="93bc9-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93bc9-125">Velg den bokførte kjøpsfakturaen du vil avbryte.</span><span class="sxs-lookup"><span data-stu-id="93bc9-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="93bc9-126">Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte kjøpsfakturaen fordi den allerede er annullert eller korrigert.</span><span class="sxs-lookup"><span data-stu-id="93bc9-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="93bc9-127">På siden **Bokført kjøpsfaktura** velger du **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="93bc9-128">En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="93bc9-129">Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="93bc9-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="93bc9-130">Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="93bc9-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="93bc9-131">Se også</span><span class="sxs-lookup"><span data-stu-id="93bc9-131">See Also</span></span>
[<span data-ttu-id="93bc9-132">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="93bc9-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="93bc9-133">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="93bc9-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="93bc9-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93bc9-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
