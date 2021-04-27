---
title: Kjøpe varer som er på salg ved å opprette kjøpsfakturaer | Microsoft dokumenter
description: Du kan opprette en faktura for en leverandør fra en salgsfaktura for å kjøpe produkter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2d956b7e22e4fe079c47ca8693d717a2b451f146
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772732"
---
# <a name="purchase-items-for-a-sale"></a><span data-ttu-id="a9c1b-103">Kjøpe varer for salg</span><span class="sxs-lookup"><span data-stu-id="a9c1b-103">Purchase Items for a Sale</span></span>
<span data-ttu-id="a9c1b-104">I ordrer og på salgsfakturaer kan du bruke funksjoner til raskt å opprette kjøpsdokumenter for manglende vareantall som kreves av salget.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="a9c1b-105">Du kan bruke to ulike funksjoner, avhengig av dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-105">You can use two different functions depending on the document type.</span></span>

> [!Note]
> <span data-ttu-id="a9c1b-106">Denne funksjonen er for påfyll av salgsvarer i ditt eget lager.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-106">This functionality is for replenishing sales items into your own inventory.</span></span> <span data-ttu-id="a9c1b-107">Hvis du vil kjøpe varer for direkte levering fra leverandøren til kunden, må du opprette en direkte levering.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-107">To purchase items for direct delivery from your vendor to your customer, you must create a drop shipment.</span></span> <span data-ttu-id="a9c1b-108">Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="a9c1b-108">For more information, see [Make Drop Shipments](sales-how-drop-shipment.md).</span></span>   

|<span data-ttu-id="a9c1b-109">Funksjon</span><span class="sxs-lookup"><span data-stu-id="a9c1b-109">Function</span></span>|<span data-ttu-id="a9c1b-110">Description</span><span class="sxs-lookup"><span data-stu-id="a9c1b-110">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="a9c1b-111">**Opprett bestillinger**</span><span class="sxs-lookup"><span data-stu-id="a9c1b-111">**Create Purchase Orders**</span></span>|<span data-ttu-id="a9c1b-112">I en ordre oppretter denne funksjonen en bestilling for hver enkelt leverandør av varene i ordren.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-112">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="a9c1b-113">Du kan redigere kjøpsantallet før du oppretter bestillingene.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-113">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="a9c1b-114">Det er bare utilgjengelige salgsantall som foreslås.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-114">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="a9c1b-115">**Opprett kjøpsfaktura**</span><span class="sxs-lookup"><span data-stu-id="a9c1b-115">**Create Purchase Invoice**</span></span>|<span data-ttu-id="a9c1b-116">I en ordre og på en salgsfaktura oppretter denne funksjonen en kjøpsfaktura for en valgt leverandør for alle linjene eller valgte linjer i salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-116">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="a9c1b-117">Hele salgsantallet foreslås.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-117">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="a9c1b-118">Opprette én eller flere bestillinger fra en ordre</span><span class="sxs-lookup"><span data-stu-id="a9c1b-118">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="a9c1b-119">Hvis du vil opprette en bestilling for hvert utilgjengelige vareantall i ordren, bruker du funksjonen **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-119">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span>

1. <span data-ttu-id="a9c1b-120">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a9c1b-121">Åpne en ordre du vil kjøpe varer for.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-121">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="a9c1b-122">Velg handlingen **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-122">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="a9c1b-123">Siden **Opprett bestillinger** åpnes med en linje for hver unike vare i ordren.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-123">The **Create Purchase Orders** page opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="a9c1b-124">Som standard vises linjer for både helt tilgjengelige salgsantall og utilgjengelige salgsantall (nedtonet).</span><span class="sxs-lookup"><span data-stu-id="a9c1b-124">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="a9c1b-125">Du kan velge handlingen **Vis utilgjengelige** hvis du bare vil se linjer for utilgjengelige salgsantall.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-125">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="a9c1b-126">Feltet **Antall å kjøpe** inneholder som standard det utilgjengelige salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-126">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="a9c1b-127">Hvis du vil kjøpe et annet antall enn det utilgjengelige salgsantallet, endrer du verdien i feltet **Antall å kjøpe**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-127">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="a9c1b-128">Du kan også endre feltet **Antall å kjøpe** på nedtonede linjer selv om de representerer helt tilgjengelige salgsantall.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-128">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="a9c1b-129">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-129">Choose the **OK** button.</span></span>

    <span data-ttu-id="a9c1b-130">En bestilling opprettes for hver enkelt leverandør av varene i ordren, inkludert eventuelle antallsendringer du har foretatt på siden **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-130">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made on the **Create Purchase Orders** page.</span></span>
7. <span data-ttu-id="a9c1b-131">Fortsett behandlingen av for eksempel bestillingen eller bestillingene ved å redigere eller legge til bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-131">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="a9c1b-132">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a9c1b-132">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="a9c1b-133">Opprette en kjøpsfaktura fra en ordre eller salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="a9c1b-133">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="a9c1b-134">Hvis du vil opprette én kjøpsfaktura for én eller flere linjer i et salgsdokument ved først å velge leverandøren du vil kjøpe fra, bruker du funksjonen **Opprett kjøpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-134">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a9c1b-135">Denne funksjonen oppretter en kjøpsfaktura for det nøyaktige vareantallet i det valgte salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-135">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="a9c1b-136">Hvis du vil endre kjøpsantallet, må du redigere kjøpsfakturaen etter at den er opprettet.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-136">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="a9c1b-137">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a9c1b-138">Åpne en salgsfaktura du vil kjøpe varer for.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-138">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="a9c1b-139">Velg én eller flere salgsfakturalinjer du vil bruke på kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-139">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="a9c1b-140">Hvis du vil bruke alle salgsfakturalinjene, merker du dem alle eller ingen av dem.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-140">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="a9c1b-141">Velg handlingen **Opprett kjøpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-141">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="a9c1b-142">Velg **Alle linjer** eller **Valgte linjer**, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-142">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="a9c1b-143">I listen over leverandører som vises, velger du leverandøren du vil kjøpe alle varene fra, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-143">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="a9c1b-144">Det opprettes en kjøpsfaktura som inneholder én, flere enn én eller alle linjene på salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-144">A purchase invoice is created that contains one, more than one, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="a9c1b-145">Fortsette med å behandle kjøpsfakturaen, for eksempel ved å redigere eller legge til kjøpsfakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="a9c1b-145">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="a9c1b-146">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="a9c1b-146">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a9c1b-147">Se også</span><span class="sxs-lookup"><span data-stu-id="a9c1b-147">See Also</span></span>
[<span data-ttu-id="a9c1b-148">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="a9c1b-148">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a9c1b-149">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="a9c1b-149">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="a9c1b-150">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="a9c1b-150">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="a9c1b-151">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="a9c1b-151">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="a9c1b-152">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a9c1b-152">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]