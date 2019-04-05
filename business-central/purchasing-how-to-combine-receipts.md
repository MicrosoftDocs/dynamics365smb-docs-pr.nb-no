---
title: Slik kombinerer du mottak | Microsoft-dokumentasjon
description: Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen Kombinere mottak.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802540"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="be384-103">Kombinere mottak på én faktura</span><span class="sxs-lookup"><span data-stu-id="be384-103">Combine Receipts on a Single Invoice</span></span>
<span data-ttu-id="be384-104">Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen **Kombinere mottak**.</span><span class="sxs-lookup"><span data-stu-id="be384-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="be384-105">Før du kan opprette et kombinert kjøpsmottak, må du bokføre mer enn ett mottak for den samme leverandøren i samme valuta.</span><span class="sxs-lookup"><span data-stu-id="be384-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="be384-106">Du må med andre ord ha fylt ut minst to bestillinger og bokført disse som mottatt, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="be384-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="be384-107">Når kjøpsmottak kombineres i en faktura og bokføres, opprettes det en bokført kjøpsfaktura for fakturert(e) linje(r).</span><span class="sxs-lookup"><span data-stu-id="be384-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="be384-108">**Fakturert (antall)**-feltet på den opprinnelige bestillingen eller rammebestillingen oppdateres basert på det fakturerte antallet.</span><span class="sxs-lookup"><span data-stu-id="be384-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="be384-109">Dette opprinnelige kjøpsdokumentet slettes imidlertid ikke, selv om det er fullstendig mottatt og fakturert, og derfor må du slette kjøpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="be384-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

## <a name="to-combine-receipts"></a><span data-ttu-id="be384-110">Slik kombinerer du mottak</span><span class="sxs-lookup"><span data-stu-id="be384-110">To combine receipts</span></span>  
1. <span data-ttu-id="be384-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="be384-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="be384-112">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="be384-112">Choose the **New** action.</span></span> <span data-ttu-id="be384-113">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="be384-113">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="be384-114">På hurtigfanen **Linjer** velger du handlingen **Hent mottakslinjer**.</span><span class="sxs-lookup"><span data-stu-id="be384-114">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="be384-115">Velg flere mottakslinjer du vil inkludere på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="be384-115">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="be384-116">Hvis feil mottakslinje ble merket eller du vil begynne på nytt, kan du ganske enkelt slette linjene på kjøpsfakturaen og deretter bruke funksjonen **Hent mottakslinje** på nytt.</span><span class="sxs-lookup"><span data-stu-id="be384-116">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="be384-117">Velg handlingen **Bokfør** for å bokføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="be384-117">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="be384-118">Fjerne åpne bestillinger etter kombinert mottaksbokføring</span><span class="sxs-lookup"><span data-stu-id="be384-118">To remove open purchase orders after combined receipt posting</span></span>  
1. <span data-ttu-id="be384-119">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett fakturerte bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="be384-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="be384-120">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="be384-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="be384-121">.</span><span class="sxs-lookup"><span data-stu-id="be384-121">.</span></span>
3. <span data-ttu-id="be384-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="be384-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="be384-123">Du kan også slette de individuelle ordrene manuelt.</span><span class="sxs-lookup"><span data-stu-id="be384-123">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="be384-124">Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel bestillinger.</span><span class="sxs-lookup"><span data-stu-id="be384-124">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="be384-125">Se også</span><span class="sxs-lookup"><span data-stu-id="be384-125">See Also</span></span>  
[<span data-ttu-id="be384-126">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="be384-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="be384-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be384-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
