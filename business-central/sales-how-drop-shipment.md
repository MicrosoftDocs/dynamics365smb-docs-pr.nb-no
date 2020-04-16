---
title: Knytte en ordre til en bestilling for direkte levering | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c61f55701ecb07862f42d3cce242756001529588
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193686"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="3ce03-103">Foreta direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="3ce03-103">Make Drop Shipments</span></span>
<span data-ttu-id="3ce03-104">En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.</span><span class="sxs-lookup"><span data-stu-id="3ce03-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="3ce03-105">Når en ordre er merket for direkte levering, og du oppretter en bestilling for kunden i **Forsendelsesadresse**-feltet, **Kundeadresse**, kan du koble de to dokumentene og på den måten instruere leverandøren til å levere direkte til kunden.</span><span class="sxs-lookup"><span data-stu-id="3ce03-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="3ce03-106">Slik oppretter du en ordre med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="3ce03-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="3ce03-107">Hvis du vil klargjøre en direkte levering, kan du opprette en ordre for en vare som vanlig, bortsett fra at du må vise på salgslinjen at salget krever direkte levering.</span><span class="sxs-lookup"><span data-stu-id="3ce03-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="3ce03-108">Opprett en ordre for en vare.</span><span class="sxs-lookup"><span data-stu-id="3ce03-108">Create a sales order for an item.</span></span> <span data-ttu-id="3ce03-109">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="3ce03-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="3ce03-110">På ordrelinjen for direkte levering, merker du av for **Direkte levering**.</span><span class="sxs-lookup"><span data-stu-id="3ce03-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="3ce03-111">Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig.</span><span class="sxs-lookup"><span data-stu-id="3ce03-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="3ce03-112">Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="3ce03-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="3ce03-113">Slik oppretter du bestillingen med direkte levering:</span><span class="sxs-lookup"><span data-stu-id="3ce03-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="3ce03-114">Hvis du vil klargjøre en direkte levering for varen som skal selges, oppretter du en bestilling som vanlig, bortsett fra at du må angi på bestillingen at den må leveres til kunden, ikke til deg selv.</span><span class="sxs-lookup"><span data-stu-id="3ce03-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="3ce03-115">Opprett en bestilling.</span><span class="sxs-lookup"><span data-stu-id="3ce03-115">Create a purchase order.</span></span> <span data-ttu-id="3ce03-116">Ikke fyll ut noen felt på linjene.</span><span class="sxs-lookup"><span data-stu-id="3ce03-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="3ce03-117">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="3ce03-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="3ce03-118">I **Forsendelsesadresse**-feltet velger du **Kundeadresse**.</span><span class="sxs-lookup"><span data-stu-id="3ce03-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="3ce03-119">I **Kunde**-feltet velger du kunden som du selger til.</span><span class="sxs-lookup"><span data-stu-id="3ce03-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="3ce03-120">Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="3ce03-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="3ce03-121">På siden **Salgsliste** merker du ordren som du har forberedt i [Slik oppretter du en ordre med direkte levering](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="3ce03-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="3ce03-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ce03-122">Choose the **OK** button.</span></span>

<span data-ttu-id="3ce03-123">Linjeinformasjonen fra ordren settes inn på bestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="3ce03-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="3ce03-124">Nå kan du angi at leverandøren skal levere varene til kunden, for eksempel, ved å sende bestillingen på e-post som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="3ce03-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="3ce03-125">Slik viser du den tilknyttede bestillingen fra ordren:</span><span class="sxs-lookup"><span data-stu-id="3ce03-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="3ce03-126">Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="3ce03-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="3ce03-127">Bokføre en direkte levering</span><span class="sxs-lookup"><span data-stu-id="3ce03-127">To post a drop shipment</span></span>
<span data-ttu-id="3ce03-128">Når leverandøren har levert varene, kan du bokføre ordren som levert.</span><span class="sxs-lookup"><span data-stu-id="3ce03-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="3ce03-129">Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.</span><span class="sxs-lookup"><span data-stu-id="3ce03-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="3ce03-130">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3ce03-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="3ce03-131">Åpne ordren som du laget i [Slik oppretter du en ordre med direkte levering]().</span><span class="sxs-lookup"><span data-stu-id="3ce03-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="3ce03-132">I **Levere (antall)**-feltet angir du hvor mye av ordreantallet som skal leveres, hele eller deler av ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="3ce03-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="3ce03-133">Velg handlingen **Bokfør** eller **Bokfør og send**.</span><span class="sxs-lookup"><span data-stu-id="3ce03-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="3ce03-134">Velg **Levere** hvis du vil fakturere senere, eller **Levere og fakturere** hvis du vil fakturere med en gang.</span><span class="sxs-lookup"><span data-stu-id="3ce03-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ce03-135">Se også</span><span class="sxs-lookup"><span data-stu-id="3ce03-135">See Also</span></span>
[<span data-ttu-id="3ce03-136">Opprette spesialbestillinger</span><span class="sxs-lookup"><span data-stu-id="3ce03-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="3ce03-137">Kjøpe varer for salg</span><span class="sxs-lookup"><span data-stu-id="3ce03-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="3ce03-138">Selge produkter</span><span class="sxs-lookup"><span data-stu-id="3ce03-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="3ce03-139">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="3ce03-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="3ce03-140">Salg</span><span class="sxs-lookup"><span data-stu-id="3ce03-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="3ce03-141">Lager</span><span class="sxs-lookup"><span data-stu-id="3ce03-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="3ce03-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3ce03-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
