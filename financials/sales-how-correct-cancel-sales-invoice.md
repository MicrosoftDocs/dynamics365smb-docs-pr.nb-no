---
title: "Korrigere eller annullere en bokført salgsfaktura | Microsoft-dokumentasjon"
description: "Beskriver hvordan du korrigerer, angrer eller annullerer en bokført salgsfaktura og utligner en salgskreditnota."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3cfa755b60a7ea24cc992e32a8f10d967e383f0f
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a><span data-ttu-id="b74a5-103">Korrigere eller annullere ubetalte salgsfakturaer</span><span class="sxs-lookup"><span data-stu-id="b74a5-103">How to: Correct or Cancel Unpaid Sales Invoices</span></span>
<span data-ttu-id="b74a5-104">Du kan korrigere eller annullere en bokført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="b74a5-104">You can correct or cancel a posted sales invoice.</span></span> <span data-ttu-id="b74a5-105">Dette er nyttig hvis du gjør en feil eller hvis kunden ber om en endring tidlig.</span><span class="sxs-lookup"><span data-stu-id="b74a5-105">This is useful if you make a mistake or if the customer requests a change.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b74a5-106">Etter at en bokført salgsfaktura er delvis eller helt betalt, kan du ikke korrigere eller annullere den fra den bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-106">After a posted sales invoice has been partially or fully paid, you cannot correct or cancel it from the posted sales invoice itself.</span></span> <span data-ttu-id="b74a5-107">I stedet må du manuelt opprette en salgskreditnota for å annullere salget og refundere kunden.</span><span class="sxs-lookup"><span data-stu-id="b74a5-107">Instead, you must manually create a sales credit memo to void the sale and reimburse the customer.</span></span> <span data-ttu-id="b74a5-108">Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="b74a5-108">For more information, see [How to: Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>

<span data-ttu-id="b74a5-109">I vinduet **Bokført salgsfaktura** kan du velge handlingen **Korriger** eller **Avbryt** for å utføre handlingene som er beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b74a5-109">In the **Posted Sales Invoice** window, you can choose the **Correct** action or the **Cancel** action to perform the actions that are described in the following table.</span></span>

| <span data-ttu-id="b74a5-110">Handling</span><span class="sxs-lookup"><span data-stu-id="b74a5-110">Action</span></span> | <span data-ttu-id="b74a5-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b74a5-111">Description</span></span> |
| --- | --- |
| <span data-ttu-id="b74a5-112">**Korriger**</span><span class="sxs-lookup"><span data-stu-id="b74a5-112">**Correct**</span></span> |<span data-ttu-id="b74a5-113">Den bokførte salgsfakturaen er annullert.</span><span class="sxs-lookup"><span data-stu-id="b74a5-113">The posted sales invoice is canceled.</span></span> <span data-ttu-id="b74a5-114">Det opprettes en ny salgsfaktura med samme informasjon.</span><span class="sxs-lookup"><span data-stu-id="b74a5-114">A new sales invoice with the same information is created.</span></span> <span data-ttu-id="b74a5-115">Du kan foreta korrigeringen og deretter fortsette salgsprosessen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-115">You can make the correction and then continue the sales process.</span></span> <span data-ttu-id="b74a5-116">Nye salgsfakturaen har et annet nummer enn den opprinnelige salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-116">The new sales invoice has a different number than the initial sales invoice.</span></span> <span data-ttu-id="b74a5-117">En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-117">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="b74a5-118">På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt.</span><span class="sxs-lookup"><span data-stu-id="b74a5-118">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |
| <span data-ttu-id="b74a5-119">**Avbryt**</span><span class="sxs-lookup"><span data-stu-id="b74a5-119">**Cancel**</span></span> |<span data-ttu-id="b74a5-120">Den bokførte salgsfakturaen er annullert.</span><span class="sxs-lookup"><span data-stu-id="b74a5-120">The posted sales invoice is canceled.</span></span> <span data-ttu-id="b74a5-121">En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-121">A corrective sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="b74a5-122">På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt.</span><span class="sxs-lookup"><span data-stu-id="b74a5-122">On the initial posted sales invoice, the Canceled and Paid check boxes are selected.</span></span> |

<span data-ttu-id="b74a5-123">Når du korrigerer eller annullerer en bokført salgsfaktura, utlignes den korrigerende salgskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige salgsfakturaen ble bokført.</span><span class="sxs-lookup"><span data-stu-id="b74a5-123">When you correct or cancel a posted sales invoice, the corrective sales credit memo is applied to all general ledger and inventory ledger entries that were created when the initial sales invoice was posted.</span></span> <span data-ttu-id="b74a5-124">Dette tilbakefører den bokførte salgsfakturaen i finanspostene og etterlater den korrigerende bokførte salgskreditnotaen for revisjonssporingen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-124">This reverses the posted sales invoice in your financial records and leaves the corrective posted sales credit memo for your audit trail.</span></span>

## <a name="to-correct-a-posted-sales-invoice"></a><span data-ttu-id="b74a5-125">Slik korrigerer du en bokført salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="b74a5-125">To correct a posted sales invoice</span></span>
1. <span data-ttu-id="b74a5-126">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b74a5-127">Velg den bokførte salgsfakturaen du vil rette.</span><span class="sxs-lookup"><span data-stu-id="b74a5-127">Select the posted sales invoice that you want to correct.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="b74a5-128">Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte salgsfakturaen fordi den allerede er korrigert eller annullert.</span><span class="sxs-lookup"><span data-stu-id="b74a5-128">If the **Canceled** check box is selected, then you cannot correct the posted sales invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="b74a5-129">I vinduet **Bokført salgsfaktura** velger du handlingen **Korriger**.</span><span class="sxs-lookup"><span data-stu-id="b74a5-129">In the **Posted Sales Invoice** window, choose the **Correct** action.</span></span>  
4. <span data-ttu-id="b74a5-130">Det opprettes en ny salgsfaktura med den samme informasjonen, der du kan foreta korrigeringen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-130">A new sales invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="b74a5-131">Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b74a5-131">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="b74a5-132">En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-132">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span>
5. <span data-ttu-id="b74a5-133">Velg handlingen **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-133">Choose the **Show Corrective Credit Memo** action to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="to-cancel-a-posted-sales-invoice"></a><span data-ttu-id="b74a5-134">Slik annullerer du en bokført salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="b74a5-134">To cancel a posted sales invoice</span></span>
1. <span data-ttu-id="b74a5-135">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b74a5-136">Velg den bokførte salgsfakturaen du vil avbryte.</span><span class="sxs-lookup"><span data-stu-id="b74a5-136">Select the posted sales invoice that you want to cancel.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="b74a5-137">Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte salgsfakturaen fordi den allerede er annullert eller korrigert.</span><span class="sxs-lookup"><span data-stu-id="b74a5-137">If the **Canceled** check box is selected, then you cannot cancel the posted sales invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="b74a5-138">I vinduet **Bokført salgsfaktura** velger du handlingen **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="b74a5-138">In the **Posted Sales Invoice** window, choose the **Cancel** action.</span></span>

    <span data-ttu-id="b74a5-139">En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-139">A sales credit memo is automatically created and posted to void the initial posted sales invoice.</span></span> <span data-ttu-id="b74a5-140">Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b74a5-140">The **Canceled** field on the initial posted sales invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="b74a5-141">Velg **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="b74a5-141">Choose **Show Corrective Credit Memo** to view the posted sales credit memo that voids the initial posted sales invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="b74a5-142">Se også</span><span class="sxs-lookup"><span data-stu-id="b74a5-142">See Also</span></span>
[<span data-ttu-id="b74a5-143">Salg</span><span class="sxs-lookup"><span data-stu-id="b74a5-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="b74a5-144">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="b74a5-144">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="b74a5-145">Sende dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="b74a5-145">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="b74a5-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b74a5-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

