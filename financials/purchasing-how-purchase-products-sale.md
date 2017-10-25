---
title: "Opprette en kjøpsfaktura fra en salgsfaktura for å kjøpe varer for salg | Microsoft-dokumentasjon"
description: "Du kan opprette en faktura for en leverandør fra en salgsfaktura for å kjøpe produkter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a><span data-ttu-id="4ca4a-103">Kjøpe varer for salg</span><span class="sxs-lookup"><span data-stu-id="4ca4a-103">How to: Purchase Items for a Sale</span></span>
<span data-ttu-id="4ca4a-104">I ordrer og på salgsfakturaer kan du bruke funksjoner til raskt å opprette kjøpsdokumenter for manglende vareantall som kreves av salget.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-104">From sales orders and sales invoices, you can use functions to quickly create purchase documents for missing item quantities that are required by the sale.</span></span> <span data-ttu-id="4ca4a-105">Du kan bruke to ulike funksjoner, avhengig av dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-105">You can use two different functions depending on the document type.</span></span>
|<span data-ttu-id="4ca4a-106">Funksjon</span><span class="sxs-lookup"><span data-stu-id="4ca4a-106">Function</span></span>|<span data-ttu-id="4ca4a-107">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4ca4a-107">Description</span></span>|
|--------|-----------|
|<span data-ttu-id="4ca4a-108">**Opprett bestillinger**</span><span class="sxs-lookup"><span data-stu-id="4ca4a-108">**Create Purchase Orders**</span></span>|<span data-ttu-id="4ca4a-109">I en ordre oppretter denne funksjonen en bestilling for hver enkelt leverandør av varene i ordren.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-109">From a sales order, this function creates a purchase order for each vendor of items on the sales order.</span></span> <span data-ttu-id="4ca4a-110">Du kan redigere kjøpsantallet før du oppretter bestillingene.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-110">You can edit the purchase quantity before you create the purchase orders.</span></span> <span data-ttu-id="4ca4a-111">Det er bare utilgjengelige salgsantall som foreslås.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-111">Only unavailable sales quantities are suggested.</span></span>
|<span data-ttu-id="4ca4a-112">**Opprett kjøpsfaktura**</span><span class="sxs-lookup"><span data-stu-id="4ca4a-112">**Create Purchase Invoice**</span></span>|<span data-ttu-id="4ca4a-113">I en ordre og på en salgsfaktura oppretter denne funksjonen en kjøpsfaktura for en valgt leverandør for alle linjene eller valgte linjer i salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-113">From a sales order and from a sales invoice, this function creates a purchase invoice for a selected vendor for all lines or selected lines on the sales document.</span></span> <span data-ttu-id="4ca4a-114">Hele salgsantallet foreslås.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-114">The full sales quantity is suggested.</span></span>|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a><span data-ttu-id="4ca4a-115">Opprette én eller flere bestillinger fra en ordre</span><span class="sxs-lookup"><span data-stu-id="4ca4a-115">To create one or more purchase orders from a sales order</span></span>
<span data-ttu-id="4ca4a-116">Hvis du vil opprette en bestilling for hvert utilgjengelige vareantall i ordren, bruker du funksjonen **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-116">To create a purchase order for each unavailable item quantity on the sales order, you use the **Create Purchase Orders** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="4ca4a-117">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-117">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="4ca4a-118">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="4ca4a-118">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

1. <span data-ttu-id="4ca4a-119">Velg flisen **Pågående ordrer** på Hjem-siden.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-119">On the Home page, choose the **Ongoing Sales Orders** tile.</span></span>
2. <span data-ttu-id="4ca4a-120">Åpne en ordre du vil kjøpe varer for.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-120">Open a sales order that you want to purchase items for.</span></span>
3. <span data-ttu-id="4ca4a-121">Velg handlingen **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-121">Choose the **Create Purchase Orders** action.</span></span>

    <span data-ttu-id="4ca4a-122">Vinduet **Opprett bestillinger** åpnes med en linje for hver unike vare i ordren.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-122">The **Create Purchase Orders** window opens showing a line for each different item on the sales order.</span></span> <span data-ttu-id="4ca4a-123">Som standard vises linjer for både helt tilgjengelige salgsantall og utilgjengelige salgsantall (nedtonet).</span><span class="sxs-lookup"><span data-stu-id="4ca4a-123">Lines for both fully available sales quantities and unavailable sales quantities (grayed) are shown by default.</span></span> <span data-ttu-id="4ca4a-124">Du kan velge handlingen **Vis utilgjengelige** hvis du bare vil se linjer for utilgjengelige salgsantall.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-124">You can choose the **Show Unavailable** action to only see lines for unavailable sales quantities.</span></span>

    <span data-ttu-id="4ca4a-125">Feltet **Antall å kjøpe** inneholder som standard det utilgjengelige salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-125">The **Quantity to Purchase** field contains the unavailable sales quantity by default.</span></span>
4. <span data-ttu-id="4ca4a-126">Hvis du vil kjøpe et annet antall enn det utilgjengelige salgsantallet, endrer du verdien i feltet **Antall å kjøpe**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-126">To purchase another quantity than the unavailable sales quantity, edit the value in the **Quantity to Purchase** field.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="4ca4a-127">Du kan også endre feltet **Antall å kjøpe** på nedtonede linjer selv om de representerer helt tilgjengelige salgsantall.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-127">You can also change the **Quantity to Purchase** field on grayed lines even though they represent fully available sales quantities.</span></span>
5. <span data-ttu-id="4ca4a-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-128">Choose the **OK** button.</span></span> 
    
    <span data-ttu-id="4ca4a-129">En bestilling opprettes for hver enkelt leverandør av varene i ordren, inkludert eventuelle antallsendringer du har foretatt i vinduet **Opprett bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-129">A purchase order is created for each vendor of items on the sales order, including any quantity changes that you made in the **Create Purchase Orders** window.</span></span>
7. <span data-ttu-id="4ca4a-130">Fortsett behandlingen av for eksempel bestillingen eller bestillingene ved å redigere eller legge til bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-130">Proceed to process the purchase order or orders, for example, by editing or adding purchase order lines.</span></span> <span data-ttu-id="4ca4a-131">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4ca4a-131">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a><span data-ttu-id="4ca4a-132">Opprette en kjøpsfaktura fra en ordre eller salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="4ca4a-132">To create a purchase invoice from a sales order or sales invoice</span></span>
<span data-ttu-id="4ca4a-133">Hvis du vil opprette én kjøpsfaktura for én eller flere linjer i et salgsdokument ved først å velge leverandøren du vil kjøpe fra, bruker du funksjonen **Opprett kjøpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-133">To create a single purchase invoice for one or more lines on a sales document by first selecting which vendor to buy from, you use the **Create Purchase Invoice** function.</span></span> 

> [!NOTE]  
>   <span data-ttu-id="4ca4a-134">Denne funksjonen oppretter en kjøpsfaktura for det nøyaktige vareantallet i det valgte salgsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-134">This function creates a purchase invoice for the exact item quantity on the selected sales document.</span></span> <span data-ttu-id="4ca4a-135">Hvis du vil endre kjøpsantallet, må du redigere kjøpsfakturaen etter at den er opprettet.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-135">To change the purchase quantity, you must edit the purchase invoice after it is created.</span></span>  

1. <span data-ttu-id="4ca4a-136">Velg flisen **Pågående salgsfakturaer** på Hjem-siden.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-136">On the Home page, choose the **Ongoing Sales Invoices** tile.</span></span>
2. <span data-ttu-id="4ca4a-137">Åpne en salgsfaktura du vil kjøpe varer for.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-137">Open a sales invoice that you want to purchase items for.</span></span>
3. <span data-ttu-id="4ca4a-138">Velg én eller flere salgsfakturalinjer du vil bruke på kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-138">Select one or more sales invoice lines that you want to use on the purchase invoice.</span></span> <span data-ttu-id="4ca4a-139">Hvis du vil bruke alle salgsfakturalinjene, merker du dem alle eller ingen av dem.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-139">To use all the sales invoice lines, select either all of them or do not select any lines.</span></span>
4. <span data-ttu-id="4ca4a-140">Velg handlingen **Opprett kjøpsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-140">Choose the **Create Purchase Invoice** action.</span></span>
5. <span data-ttu-id="4ca4a-141">Velg **Alle linjer** eller **Valgte linjer**, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-141">Select either **All Lines** or **Selected Lines**, and then choose the **OK** button.</span></span>  
6. <span data-ttu-id="4ca4a-142">I listen over leverandører som vises, velger du leverandøren du vil kjøpe alle varene fra, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-142">In the list of vendors that appears, select the vendor that you want to buy all the items from, and then choose the **OK** button.</span></span>

    <span data-ttu-id="4ca4a-143">Det opprettes en kjøpsfaktura som inneholder én, flere eller alle linjene på salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-143">A purchase invoice is created that contains one, more, or all the lines on the sales invoice.</span></span>
7. <span data-ttu-id="4ca4a-144">Fortsette med å behandle kjøpsfakturaen, for eksempel ved å redigere eller legge til kjøpsfakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="4ca4a-144">Proceed to process the purchase invoice, for example, by editing or adding purchase invoice lines.</span></span> <span data-ttu-id="4ca4a-145">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4ca4a-145">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ca4a-146">Se også</span><span class="sxs-lookup"><span data-stu-id="4ca4a-146">See Also</span></span>
[<span data-ttu-id="4ca4a-147">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4ca4a-147">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4ca4a-148">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="4ca4a-148">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="4ca4a-149">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="4ca4a-149">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="4ca4a-150">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="4ca4a-150">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="4ca4a-151">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ca4a-151">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

