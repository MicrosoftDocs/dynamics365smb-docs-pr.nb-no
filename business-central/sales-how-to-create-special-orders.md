---
title: Opprette spesialbestillinger | Microsoft-dokumentasjon
description: Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde. Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fbd22ee25cb472a827468c578ccdb8a7427490bc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383028"
---
# <a name="create-special-orders"></a><span data-ttu-id="79fe2-104">Opprette spesialbestillinger</span><span class="sxs-lookup"><span data-stu-id="79fe2-104">Create Special Orders</span></span>
<span data-ttu-id="79fe2-105">Du kan opprette en spesialbestilling for en bestemt katalogvare som skal leveres til en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="79fe2-105">You can create a special order for a specific catalog item to be shipped to a specific customer.</span></span> <span data-ttu-id="79fe2-106">Leverandøren din leverer varen til lageret ditt, og du kan deretter sende bare denne varen videre til kunden eller sammen med andre varer i en annen ordre.</span><span class="sxs-lookup"><span data-stu-id="79fe2-106">Your vendor ships the item to your warehouse and you can then ship the item on to your customer either independently or together with other items on another order.</span></span>  

<span data-ttu-id="79fe2-107">Spesialbestillinger betyr at bestillingen og ordren er knyttet til hverandre for å sikre at den bestemte katalogvaren plukkes og leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="79fe2-107">Special orders imply that the purchase and sales order are linked to ensure that the specific catalog item is picked and delivered to the customer.</span></span>  

<span data-ttu-id="79fe2-108">Før du kan bruke denne funksjonen, må du først konfigurere kunden, leverandøren og de varekortene som kreves for ordren.</span><span class="sxs-lookup"><span data-stu-id="79fe2-108">Before you can use this feature, you must first set up the customer, vendor, and item cards necessary for the order.</span></span>  

## <a name="to-create-a-special-order"></a><span data-ttu-id="79fe2-109">Slik oppretter du en spesialbestilling</span><span class="sxs-lookup"><span data-stu-id="79fe2-109">To create a special order</span></span>  
1.  <span data-ttu-id="79fe2-110">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="79fe2-111">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-111">Choose the **New** action.</span></span> <span data-ttu-id="79fe2-112">Opprett og fyll ut en  ordre for varen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-112">Create and fill in a  sales order for the item.</span></span> <span data-ttu-id="79fe2-113">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="79fe2-113">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3.  <span data-ttu-id="79fe2-114">På hurtigfanen **Linjer** fyller du inn salgslinjen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-114">On the **Lines** FastTab, fill in the sales line.</span></span> <span data-ttu-id="79fe2-115">Velg en kjøpskode som **Spesialbestilling**-feltet er valgt for, i **Kjøpskode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79fe2-115">In the **Purchasing Code** field, select a purchasing code that has the **Special Order** field selected.</span></span>

    <span data-ttu-id="79fe2-116">Du må nå opprette en bestilling fra et bestillingsforslag.</span><span class="sxs-lookup"><span data-stu-id="79fe2-116">You must now create a purchase order from a requisition worksheet.</span></span>  
4. <span data-ttu-id="79fe2-117">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillingsforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requisition Worksheet**, and then choose the related link.</span></span>  
5. <span data-ttu-id="79fe2-118">Velg **Spesialbestilling**-handlingen, og velg deretter **Hent ordre**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-118">Choose the **Special Order** action, and then choose the **Get Sales Orders** action.</span></span>  
6.  <span data-ttu-id="79fe2-119">Vis resultater der **Bilagsnr.** er ordrenummeret, på siden **Hent ordrer**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-119">On the **Get Sales Orders** page, show results where the **Document No.** is the sales order number.</span></span> <span data-ttu-id="79fe2-120">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-120">Choose the **OK** button.</span></span> <span data-ttu-id="79fe2-121">Det opprettes en bestillingsforslagslinje for varen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-121">A requisition worksheet line is created for the item.</span></span>  
7.  <span data-ttu-id="79fe2-122">På bestillingsforslagslinjen velger du **Ny** i feltet **Handlingsmelding**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-122">On the requisition worksheet line, in the **Action Message** field, select **New**.</span></span>  
8.  <span data-ttu-id="79fe2-123">På siden **Best.forslag** velger du handlingen **Utfør handlingsmelding**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-123">On the **Req. Worksheet** page, choose the **Carry Out Action Message** action.</span></span> <span data-ttu-id="79fe2-124">Siden **Utfør handlingsmeld. - forslag** åpnes.</span><span class="sxs-lookup"><span data-stu-id="79fe2-124">The **Carry Out Action Msg. - Req.** page opens.</span></span> <span data-ttu-id="79fe2-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-125">Choose the **OK** button.</span></span>  

    <span data-ttu-id="79fe2-126">Det vises en melding om at bestillingene er opprettet.</span><span class="sxs-lookup"><span data-stu-id="79fe2-126">A message appears telling you that the purchase orders have been created.</span></span> <span data-ttu-id="79fe2-127">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="79fe2-127">Choost the **OK** button.</span></span>  

<span data-ttu-id="79fe2-128">En bestilling som er opprettet som en spesialbestilling for en salgsordre, blir respektert av planleggingssystemet som balanserer behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="79fe2-128">A purchase order created as a special order for a sales order is respected by the planning system as it balances demand and supply.</span></span> <span data-ttu-id="79fe2-129">Det vil si at bestillingen (tilbud) forblir koblet til ordren (etterspørsel), selv om den aktuelle bestillingen ville kunnet forsyne et annet tidligere behov.</span><span class="sxs-lookup"><span data-stu-id="79fe2-129">That is, the purchase order (supply) remains linked to the sales order (demand), even if that purchase order could supply another earlier demand.</span></span> <span data-ttu-id="79fe2-130">Hvis du vil ha mer informasjon, se [Designdetaljer: Gjenbestillingsprinsipper](design-details-reservation-order-tracking-and-action-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="79fe2-130">For more information, see [Design Details: Reordering Policies](design-details-reservation-order-tracking-and-action-messaging.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="79fe2-131">Du kan ikke bruke funksjonen for spesialbestilling hvis varen allerede er reservert.</span><span class="sxs-lookup"><span data-stu-id="79fe2-131">You cannot use the special order functionality if the item is already reserved.</span></span> <span data-ttu-id="79fe2-132">For varer som selges på spesialbestilling, må du derfor passe på at feltet **Reserver** på varekortet ikke er satt til **Alltid**.</span><span class="sxs-lookup"><span data-stu-id="79fe2-132">Therefore, for items that are sold on special orders, make sure the **Reserve** field on the item card is not set to **Always**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79fe2-133">Se også</span><span class="sxs-lookup"><span data-stu-id="79fe2-133">See Also</span></span>  
[<span data-ttu-id="79fe2-134">Arbeide med katalogvarer</span><span class="sxs-lookup"><span data-stu-id="79fe2-134">Work with Catalog Items</span></span>](inventory-how-work-nonstock-items.md)  
[<span data-ttu-id="79fe2-135">Salg</span><span class="sxs-lookup"><span data-stu-id="79fe2-135">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="79fe2-136">[Foreta direkte leveringer](sales-how-drop-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="79fe2-136">[Make Drop Shipments](sales-how-drop-shipment.md) </span></span>  
[<span data-ttu-id="79fe2-137">Designdetaljer: Gjenbestillingsprinsipper</span><span class="sxs-lookup"><span data-stu-id="79fe2-137">Design Details: Reordering Policies</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="79fe2-138">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79fe2-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]