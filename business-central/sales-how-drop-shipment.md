---
title: Knytte en ordre til en bestilling for direkte levering | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 938b0cc9f35e980ca9121cb037665b8699ca336f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393376"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="b9f9d-103">Foreta direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="b9f9d-103">Make Drop Shipments</span></span>

<span data-ttu-id="b9f9d-104">En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="b9f9d-105">Når en ordre er merket for direkte levering, og du oppretter en bestilling for kunden i **Forsendelsesadresse**-feltet, **Kundeadresse**, kan du koble de to dokumentene og instruere leverandøren til å levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="b9f9d-106">Slik oppretter du en ordre med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="b9f9d-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="b9f9d-107">Hvis du vil klargjøre en direkte levering, kan du opprette en ordre og vise på salgslinjen at salget krever direkte levering.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="b9f9d-108">Opprett en ordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-108">Create a sales order for an item.</span></span> <span data-ttu-id="b9f9d-109">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="b9f9d-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="b9f9d-110">På ordrelinjen for direkte levering, merker du av for **Direkte levering**.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="b9f9d-111">Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="b9f9d-112">Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="b9f9d-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="b9f9d-113">Slik oppretter du bestillingen med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="b9f9d-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="b9f9d-114">For å klargjøre en direkte levering angir du på bestilling at den må leveres til kunden, ikke til deg selv.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="b9f9d-115">Opprett en bestilling.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-115">Create a purchase order.</span></span> <span data-ttu-id="b9f9d-116">Ikke fyll ut noen felt på linjene.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="b9f9d-117">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="b9f9d-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="b9f9d-118">I **Forsendelsesadresse**-feltet velger du **Kundeadresse**.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="b9f9d-119">I **Kunde**-feltet velger du kunden som du selger til.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="b9f9d-120">Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="b9f9d-121">På siden **Salgsliste** merker du ordren som du har forberedt i [Slik oppretter du en ordre med direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="b9f9d-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="b9f9d-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-122">Choose the **OK** button.</span></span>

<span data-ttu-id="b9f9d-123">Linjeinformasjonen fra ordren settes inn på bestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="b9f9d-124">Nå kan du angi at leverandøren skal levere varene til kunden, for eksempel, ved å sende bestillingen på e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="b9f9d-125">Slik oppretter du flere bestillinger med direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="b9f9d-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="b9f9d-126">Du kan også bruke bestillingsforslaget til å opprette bestillingen for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="b9f9d-127">Fordelen med å bruke bestillingsforslaget er at det kan opprette bestillinger for alle utestående direkte leveringer, slik at du ikke trenger å opprette hver enkelt individuelt.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="b9f9d-128">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9f9d-129">Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="b9f9d-130">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="b9f9d-131">Se gjennom bestillingslinjene, og velg leverandør som leverer nødvendige varer, i feltet **Leverandørnummer**.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="b9f9d-132">Velg handlingen **Utfør handlingsmelding** for å konvertere korrekturleste linjer til en bestilling.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="b9f9d-133">Slik viser du den tilknyttede bestillingen fra ordren:</span><span class="sxs-lookup"><span data-stu-id="b9f9d-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="b9f9d-134">Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="b9f9d-135">Bokføre en direkte levering</span><span class="sxs-lookup"><span data-stu-id="b9f9d-135">To post a drop shipment</span></span>

<span data-ttu-id="b9f9d-136">Når leverandøren har levert varene, kan du bokføre ordren som levert.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="b9f9d-137">Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="b9f9d-138">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="b9f9d-139">Åpne ordren du opprettet i [Slik oppretter du en ordre med direkte levering:](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="b9f9d-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="b9f9d-140">I **Levere (antall)**-feltet angir du hvor mye av ordreantallet som skal leveres, hele eller deler av ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="b9f9d-141">Velg handlingen **Bokfør** eller **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="b9f9d-142">Velg **Levere** hvis du vil fakturere senere, eller **Levere og fakturere** hvis du vil fakturere med en gang.</span><span class="sxs-lookup"><span data-stu-id="b9f9d-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9f9d-143">Se også</span><span class="sxs-lookup"><span data-stu-id="b9f9d-143">See Also</span></span>

[<span data-ttu-id="b9f9d-144">Opprette spesialbestillinger</span><span class="sxs-lookup"><span data-stu-id="b9f9d-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="b9f9d-145">Kjøpe varer for salg</span><span class="sxs-lookup"><span data-stu-id="b9f9d-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="b9f9d-146">Selge produkter</span><span class="sxs-lookup"><span data-stu-id="b9f9d-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="b9f9d-147">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="b9f9d-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="b9f9d-148">Salg</span><span class="sxs-lookup"><span data-stu-id="b9f9d-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="b9f9d-149">Lager</span><span class="sxs-lookup"><span data-stu-id="b9f9d-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b9f9d-150">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9f9d-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]