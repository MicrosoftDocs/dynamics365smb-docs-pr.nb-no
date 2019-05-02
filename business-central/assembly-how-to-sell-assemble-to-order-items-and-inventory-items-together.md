---
title: Selge montere-til-ordre-varer og lagervarer sammen | Microsoft-dokumentasjon
description: Hvis en monteringsvare er definert for Monter til lager, forutsetter standard ordreprosess at varen allerede er montert og kan plukkes fra lager, hvis den er tilgjengelig. Men hvis det er en del av (eller hele) antallet som ikke er tilgjengelig, må du å opprette en monteringsordre for det gjenværende antallet direkte.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 2f71dbbb4e7e4af19829f08243371bea1998b093
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802601"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a><span data-ttu-id="6ec84-104">Selge montere til ordre-varer og lagervarer sammen</span><span class="sxs-lookup"><span data-stu-id="6ec84-104">Sell Assemble-to-Order Items and Inventory Items Together</span></span>
<span data-ttu-id="6ec84-105">Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare inneholder **Monter til lager**, forutsetter standard ordreprosess at varen allerede er montert og kan plukkes fra lager, hvis den er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="6ec84-105">If the **Assembly Policy** field on the item card of an assembly item contains **Assemble-to-Stock**, then the default sales order process assumes that the item is already assembled and can be picked from inventory, if it is available.</span></span> <span data-ttu-id="6ec84-106">Ingen monteringsordre blir derfor automatisk opprettet og koblet til ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="6ec84-106">Therefore, no assembly order is automatically created and linked to the sales order line.</span></span> <span data-ttu-id="6ec84-107">Hvis en del av (eller hele) antallet imidlertid ikke er tilgjengelig, kan du opprette en monteringsordre for restantallet ved å fylle ut feltet **Ant. som skal monteres til ordre** på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="6ec84-107">However, if a part (or all) of the quantity is not available, then you have the flexibility to create an assembly order for the remaining quantity by filling in the **Qty. to Assemble to Order** field on the sales order line.</span></span> <span data-ttu-id="6ec84-108">Slik kan du montere varen til ordre selv om den er definert slik at den monteres til lager som standard.</span><span class="sxs-lookup"><span data-stu-id="6ec84-108">In this manner, you can assemble the item to order although it is set up to be assembled to stock by default.</span></span>  

<span data-ttu-id="6ec84-109">Det finnes en lignende fleksibilitet når du selger varer som skal monteres til ordre og en del av antallet, som du vil trekke fra monteringsordren, finnes på lager.</span><span class="sxs-lookup"><span data-stu-id="6ec84-109">Similar flexibility exists when you are selling items to be assembled to the order and a part of the quantity is in inventory, which you want to deduct from the assembly order.</span></span> <span data-ttu-id="6ec84-110">Hvis du vil ha mer informasjon, kan du se [Selge lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span><span class="sxs-lookup"><span data-stu-id="6ec84-110">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6ec84-111">Visse regler gjelder for feltet **Levere (antall)** på ordrelinjer som inneholder en kombinasjon av monter-til-ordre-antall og lagerantall.</span><span class="sxs-lookup"><span data-stu-id="6ec84-111">Certain rules apply to the **Qty. to Ship** field on sales order lines that contain a combination of assemble-to-order quantities and inventory quantities.</span></span> <span data-ttu-id="6ec84-112">Hvis du vil ha mer informasjon, kan du se delen Kombinasjonsscenarier i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="6ec84-112">For more information, see the Combination Scenarios section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6ec84-113">Følgende fremgangsmåte omfatter ikke standardtrinnene for ordrer som du må følge før du oppretter en monteringsordre for utilgjengelige antall.</span><span class="sxs-lookup"><span data-stu-id="6ec84-113">The following procedure does not include the standard sales order steps that you need to follow before you create an assembly order for unavailable quantities.</span></span>

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a><span data-ttu-id="6ec84-114">Selge montere til ordre-varer og lagervarer sammen</span><span class="sxs-lookup"><span data-stu-id="6ec84-114">To sell assemble-to-order items and inventory items together</span></span>  
1.  <span data-ttu-id="6ec84-115">På en salgsordrelinje for en vare som er definert slik at den monteres til lager angir du et antall i feltet **Antall** som overskrider beholdningen.</span><span class="sxs-lookup"><span data-stu-id="6ec84-115">On a sales order line for an item that is set up to be assembled to stock, enter a quantity in the **Quantity** field that exceeds inventory.</span></span> <span data-ttu-id="6ec84-116">Siden **Kontroller tilgjengelighet** vises.</span><span class="sxs-lookup"><span data-stu-id="6ec84-116">The **Check Availability** page appears.</span></span> <span data-ttu-id="6ec84-117">Hvis du vil ha mer informasjon, kan du se [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ec84-117">For more information, see [View the Availability of Items](inventory-how-availability-overview.md).</span></span>
2.  <span data-ttu-id="6ec84-118">Noter verdien i feltet **Antall i alt** (en negativ verdi), som du vil angi i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="6ec84-118">Note the **Total Quantity** field (a negative value), which you will enter in the next step.</span></span>  
3.  <span data-ttu-id="6ec84-119">Angi verdien fra forrige trinn i feltet **Ant. som skal monteres til ordre**.</span><span class="sxs-lookup"><span data-stu-id="6ec84-119">In the **Qty. to Assemble to Order** field, enter the value from the previous step.</span></span>  
4.  <span data-ttu-id="6ec84-120">Gjør eventuelle endringer i monteringskomponentene.</span><span class="sxs-lookup"><span data-stu-id="6ec84-120">Perform any changes to the assembly components.</span></span> <span data-ttu-id="6ec84-121">Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="6ec84-121">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  
5.  <span data-ttu-id="6ec84-122">Fortsett med å frigi ordren, for å klargjøre den for plukking av lagervarer og for montering av de utilgjengelige varene.</span><span class="sxs-lookup"><span data-stu-id="6ec84-122">Proceed to release the sales order, to prepare it for picking of the inventory items and for assembly of the unavailable items.</span></span> <span data-ttu-id="6ec84-123">Hvis du vil ha mer informasjon om disse standardtrinnene for montering, kan du se [Montere varer](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="6ec84-123">For more information about these standard assembly steps, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="6ec84-124">**Hyllekode**-feltet på ordren kan bli forhåndsutfylt i henhold til feltet **Hyllek. lev. fra m. til ordre** eller **Fra Hyllekode for montering** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="6ec84-124">The **Bin Code** field on the sales order may be prefilled according to the **Assemble-to-Order Shpt. Bin Code** field or the **From-Assembly Bin Code** field on the location card.</span></span> <span data-ttu-id="6ec84-125">I dette tilfellet er kanskje **Hyllekode**-feltet på ordrelinjen feil i denne kombinasjonen av montere-til-ordre- og montere-til-lager-antall.</span><span class="sxs-lookup"><span data-stu-id="6ec84-125">In that case, the **Bin Code** field on the sales order line may be incorrect in this combination of assemble-to-order and assemble-to-stock quantities.</span></span> <span data-ttu-id="6ec84-126">Det er en god idé å undersøke **Hyllekode**-feltet og kontrollere at plasseringen fungerer for alle antall.</span><span class="sxs-lookup"><span data-stu-id="6ec84-126">It is a good idea to examine the **Bin Code** field and make sure that the placement works for all quantities.</span></span> <span data-ttu-id="6ec84-127">Du kan også angi to forskjellige antall på separate ordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="6ec84-127">Alternatively, enter the two different quantities on separate sales order lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ec84-128">Se også</span><span class="sxs-lookup"><span data-stu-id="6ec84-128">See Also</span></span>  
[<span data-ttu-id="6ec84-129">Monteringsstyring</span><span class="sxs-lookup"><span data-stu-id="6ec84-129">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="6ec84-130">Arbeide med stykklister</span><span class="sxs-lookup"><span data-stu-id="6ec84-130">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="6ec84-131">Lager</span><span class="sxs-lookup"><span data-stu-id="6ec84-131">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6ec84-132">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="6ec84-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6ec84-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ec84-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>