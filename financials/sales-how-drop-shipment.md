---
title: Opprette en ordre som er koblet til en bestilling for en direkte levering | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="352a6-103">Foreta direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="352a6-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="352a6-104">En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="352a6-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="352a6-105">Når en ordre merkes for direkte levering, og du oppretter en bestilling som angir kunden i **Salg til kundenr.**-feltet,</span><span class="sxs-lookup"><span data-stu-id="352a6-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="352a6-106">kan du koble de to dokumentene og dermed be leverandøren levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="352a6-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="352a6-107">Slik oppretter du en ordre med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="352a6-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="352a6-108">Hvis du vil klargjøre en direkte levering, kan du opprette en ordre for en vare som vanlig, bortsett fra at du må vise på salgslinjen at salget krever direkte levering.</span><span class="sxs-lookup"><span data-stu-id="352a6-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="352a6-109">Opprett en ordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="352a6-109">Create a sales order for an item.</span></span> <span data-ttu-id="352a6-110">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="352a6-111">På ordrelinjen for direkte levering, merker du av for **Direkte levering**.</span><span class="sxs-lookup"><span data-stu-id="352a6-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="352a6-112">Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig.</span><span class="sxs-lookup"><span data-stu-id="352a6-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="352a6-113">Hvis du vil ha mer informasjon, kan du se [Brukertilpasning](ui-user-personalization.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="352a6-114">Denne funksjonen krever at opplevelsen er satt til **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="352a6-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="352a6-115">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="352a6-116">Slik oppretter du bestillingen med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="352a6-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="352a6-117">Hvis du vil klargjøre en direkte levering for varen som skal selges, oppretter du en bestilling som vanlig, bortsett fra at du må angi på bestillingen at den må leveres til kunden, ikke til deg selv.</span><span class="sxs-lookup"><span data-stu-id="352a6-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="352a6-118">Opprett en bestilling.</span><span class="sxs-lookup"><span data-stu-id="352a6-118">Create a purchase order.</span></span> <span data-ttu-id="352a6-119">Ikke fyll ut noen felt på linjene.</span><span class="sxs-lookup"><span data-stu-id="352a6-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="352a6-120">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="352a6-121">I feltet **Salg til-kundenr.**</span><span class="sxs-lookup"><span data-stu-id="352a6-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="352a6-122">velger du kunden som du selger til.</span><span class="sxs-lookup"><span data-stu-id="352a6-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="352a6-123">Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="352a6-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="352a6-124">I **Salgsliste**-vinduet merker du ordren som du har forberedt i "Slik oppretter du en ordre med direkte levering".</span><span class="sxs-lookup"><span data-stu-id="352a6-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="352a6-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="352a6-125">Choose the **OK** button.</span></span>

<span data-ttu-id="352a6-126">Linjeinformasjonen fra ordren settes inn på bestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="352a6-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="352a6-127">Nå kan du angi at leverandøren skal levere varene til kunden, for eksempel, ved å sende bestillingen på e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="352a6-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="352a6-128">Slik viser du den tilknyttede bestillingen fra ordren:</span><span class="sxs-lookup"><span data-stu-id="352a6-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="352a6-129">Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="352a6-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="352a6-130">Bokføre en direkte levering</span><span class="sxs-lookup"><span data-stu-id="352a6-130">To post a drop shipment</span></span>
<span data-ttu-id="352a6-131">Når leverandøren har levert varene, kan du bokføre ordren som levert.</span><span class="sxs-lookup"><span data-stu-id="352a6-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="352a6-132">Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.</span><span class="sxs-lookup"><span data-stu-id="352a6-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="352a6-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="352a6-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="352a6-134">Åpne ordren som du laget i "Slik oppretter du en ordre med direkte levering".</span><span class="sxs-lookup"><span data-stu-id="352a6-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="352a6-135">I **Levere (antall)**-feltet angir du hvor mye av ordreantallet som skal leveres, hele eller deler av ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="352a6-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="352a6-136">Velg handlingen **Bokfør** eller **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="352a6-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="352a6-137">Velg **Levere** hvis du vil fakturere senere, eller **Levere og fakturere** hvis du vil fakturere med en gang.</span><span class="sxs-lookup"><span data-stu-id="352a6-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="352a6-138">Se også</span><span class="sxs-lookup"><span data-stu-id="352a6-138">See Also</span></span>
[<span data-ttu-id="352a6-139">Selge produkter</span><span class="sxs-lookup"><span data-stu-id="352a6-139">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="352a6-140">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="352a6-140">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="352a6-141">Salg</span><span class="sxs-lookup"><span data-stu-id="352a6-141">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="352a6-142">Lager</span><span class="sxs-lookup"><span data-stu-id="352a6-142">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="352a6-143">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="352a6-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

