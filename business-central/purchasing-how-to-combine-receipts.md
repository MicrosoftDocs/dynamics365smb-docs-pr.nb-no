---
title: Slik kombinerer du mottak | Microsoft-dokumentasjon
description: Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen Kombinere mottak.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: edupont
ms.openlocfilehash: 70433ce496c79edcd053ae345b3b0559cf60b744
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782902"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="fa9a4-103">Kombinere mottak på én faktura</span><span class="sxs-lookup"><span data-stu-id="fa9a4-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="fa9a4-104">Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen **Kombinere mottak**.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="fa9a4-105">Før du kan opprette et kombinert kjøpsmottak, må du bokføre mer enn ett mottak for den samme leverandøren i samme valuta.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="fa9a4-106">Du må med andre ord ha fylt ut minst to bestillinger og bokført disse som mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="fa9a4-107">Når kjøpsmottak kombineres i en faktura og bokføres, opprettes det en bokført kjøpsfaktura for fakturert(e) linje(r).</span><span class="sxs-lookup"><span data-stu-id="fa9a4-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="fa9a4-108">**Fakturert (antall)**-feltet på den opprinnelige bestillingen eller rammebestillingen oppdateres basert på det fakturerte antallet.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="fa9a4-109">Dette opprinnelige kjøpsdokumentet slettes imidlertid ikke, selv om det er fullstendig mottatt og fakturert, og derfor må du slette kjøpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="fa9a4-110">Den resulterende kjøpsfakturaen kan senere ikke rettes eller kanselleres.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="fa9a4-111">Hvis du vil endre en kjøpsfaktura som er opprettet på denne måten, må du bruke kjøpskreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="fa9a4-112">Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="fa9a4-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="fa9a4-113">Slik kombinerer du mottak</span><span class="sxs-lookup"><span data-stu-id="fa9a4-113">To combine receipts</span></span>

1. <span data-ttu-id="fa9a4-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fa9a4-115">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-115">Choose the **New** action.</span></span> <span data-ttu-id="fa9a4-116">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="fa9a4-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="fa9a4-117">På hurtigfanen **Linjer** velger du handlingen **Hent mottakslinjer**.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="fa9a4-118">Velg flere mottakslinjer du vil inkludere på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="fa9a4-119">Hvis feil mottakslinje ble merket eller du vil begynne på nytt, kan du ganske enkelt slette linjene på kjøpsfakturaen og deretter bruke funksjonen **Hent mottakslinje** på nytt.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="fa9a4-120">Velg handlingen **Bokfør** for å bokføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="fa9a4-121">Fjerne åpne bestillinger etter kombinert mottaksbokføring</span><span class="sxs-lookup"><span data-stu-id="fa9a4-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="fa9a4-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett fakturerte bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="fa9a4-123">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="fa9a4-124">.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-124">.</span></span>
3. <span data-ttu-id="fa9a4-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="fa9a4-126">Du kan også slette de individuelle ordrene manuelt.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="fa9a4-127">Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel bestillinger.</span><span class="sxs-lookup"><span data-stu-id="fa9a4-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa9a4-128">Se også</span><span class="sxs-lookup"><span data-stu-id="fa9a4-128">See Also</span></span>

[<span data-ttu-id="fa9a4-129">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="fa9a4-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="fa9a4-130">Korrigere eller annullere ubetalte kjøpsfakturaer</span><span class="sxs-lookup"><span data-stu-id="fa9a4-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="fa9a4-131">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa9a4-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
