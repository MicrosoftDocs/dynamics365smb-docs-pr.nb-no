---
title: Opprette rammemonteringsordrer | Microsoft-dokumentasjon
description: Opprett rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom oppretter de faktiske ordrene i henhold til rammeordreavtalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9e96cf7edd4a2080b92c88215f67e93bc4e0f7f8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772982"
---
# <a name="create-blanket-assembly-orders"></a><span data-ttu-id="1cfde-103">Opprette rammemonteringsordrer</span><span class="sxs-lookup"><span data-stu-id="1cfde-103">Create Blanket Assembly Orders</span></span>
<span data-ttu-id="1cfde-104">Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="1cfde-105">Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="1cfde-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="1cfde-106">Som med alle andre typer varer kan du også opprette rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom lager de faktiske ordrene i henhold til rammeordreavtalen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-106">As with any other type of item, you can also create blanket sales orders for customized assembly items before periodically making the actual sales orders according to the blanket order agreement.</span></span> <span data-ttu-id="1cfde-107">Denne prosessen omfatter flere ekstra trinn når du sammenligner den med å opprette en vanlig rammeordre, og den bruker en variant av en koblet monteringsordre, som er en rammemonteringsordre.</span><span class="sxs-lookup"><span data-stu-id="1cfde-107">This process involves several extra steps when you compare it to creating a regular blanket sales order, and it uses a variation of a linked assembly order, which is a blanket assembly order.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1cfde-108">I likhet med alle rammebestillinger er antallene på monteringsrammebestillinger bare prognoser og ikke operative før de konverteres til faktiske monteringsordrer.</span><span class="sxs-lookup"><span data-stu-id="1cfde-108">Like all blanket orders, quantities on assembly blanket orders are only forecasts and are not operational until they are converted to actual assembly orders.</span></span> <span data-ttu-id="1cfde-109">Derfor er ordrefunksjonalitet som beregning av tilgjengelighet, reservasjon og varesporing ikke aktiv for rammemonteringsordrer.</span><span class="sxs-lookup"><span data-stu-id="1cfde-109">Therefore, order functionality, such as availability calculation, reservation, and item tracking, is not active on blanket assembly orders.</span></span>  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><span data-ttu-id="1cfde-110">Slik oppretter du en rammemonteringsordre for en montere\-til\-ordre-vare</span><span class="sxs-lookup"><span data-stu-id="1cfde-110">To create a blanket assembly order for an assemble\-to\-order item</span></span>  
1. <span data-ttu-id="1cfde-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rammeordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1cfde-112">Opprette en ny rammeordre med én linje for en monteringsvare.</span><span class="sxs-lookup"><span data-stu-id="1cfde-112">Create a new blanket sales order with one line for an assembly item.</span></span> <span data-ttu-id="1cfde-113">Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1cfde-113">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>  
3. <span data-ttu-id="1cfde-114">Angi hele antallet i feltet **Ant. som skal monteres til ordre** på linjen for rammemonteringsordre.</span><span class="sxs-lookup"><span data-stu-id="1cfde-114">In the **Qty. to Assemble to Order** field on the blanket assembly order line, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="1cfde-115">Du bør ikke opprette rammebestillingsavtaler for et delvist antall.</span><span class="sxs-lookup"><span data-stu-id="1cfde-115">You should not create blanket order agreements for a partial quantity.</span></span> <span data-ttu-id="1cfde-116">Du må derfor angi samme antall som du skrev inn i feltet **Antall** på rammeordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-116">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the blanket sales order line.</span></span>  

4. <span data-ttu-id="1cfde-117">Velg handingen **Monter til ordre**, og velg deretter handlingen **Montere til ordre – linjer**.</span><span class="sxs-lookup"><span data-stu-id="1cfde-117">Choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action.</span></span> <span data-ttu-id="1cfde-118">Du kan også merke feltet **Ant. som skal monteres til ordre** på linjen.</span><span class="sxs-lookup"><span data-stu-id="1cfde-118">Alternatively, choose the **Qty. to Assemble to Order)** field on the line.</span></span>  
5. <span data-ttu-id="1cfde-119">Gå gjennom eller endre monteringsordrelinjene i henhold til rammeordreavtalen du har med kunden, på siden **Montere til ordre – linjer**.</span><span class="sxs-lookup"><span data-stu-id="1cfde-119">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the blanket order agreement that you have made with the customer.</span></span> <span data-ttu-id="1cfde-120">Hvis du vil vise mer informasjon, velger du **Vis dokument** for å åpne hele rammemonteringsordren.</span><span class="sxs-lookup"><span data-stu-id="1cfde-120">If you want to view more information, choose the **Show Document** action to open the complete blanket assembly order.</span></span> <span data-ttu-id="1cfde-121">Du kan ikke endre innholdet i de fleste av feltene, og du kan ikke bokføre.</span><span class="sxs-lookup"><span data-stu-id="1cfde-121">You cannot change the contents of most fields, and you cannot post.</span></span>  
6. <span data-ttu-id="1cfde-122">Når du har justert monteringsordrelinjene i henhold til rammeordreavtalen, lukker du siden **Montere til ordre – linjer** for å gå tilbake til siden **Rammeordre**.</span><span class="sxs-lookup"><span data-stu-id="1cfde-122">When you have adjusted the assembly order lines according to the blanket order agreement, close the **Assemble-to-Order Lines** page to return to the **Blanket Sales Order** page.</span></span>  
7. <span data-ttu-id="1cfde-123">Når kunden ber om å få opprettet en ordre basert på den avtalte rammeordren, oppretter du en ordre for den/de avtalte monteringsvaren(e).</span><span class="sxs-lookup"><span data-stu-id="1cfde-123">When the customer requests to create a sales order based on the agreed blanket sales order, create a sales order for the agreed assembly item or items.</span></span> <span data-ttu-id="1cfde-124">Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1cfde-124">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>

<span data-ttu-id="1cfde-125">Den koblede rammemonteringsordren og eventuelle tilpasninger knyttes til denne nye salgsordren for å klargjøre for montering av varen(e) som skal selges.</span><span class="sxs-lookup"><span data-stu-id="1cfde-125">The linked blanket assembly order and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1cfde-126">Se også</span><span class="sxs-lookup"><span data-stu-id="1cfde-126">See Also</span></span>
[<span data-ttu-id="1cfde-127">Opprette rammeordrer</span><span class="sxs-lookup"><span data-stu-id="1cfde-127">Create Blanket Sales Orders</span></span>](sales-how-to-create-blanket-sales-orders.md)  
[<span data-ttu-id="1cfde-128">Monteringsstyring</span><span class="sxs-lookup"><span data-stu-id="1cfde-128">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="1cfde-129">Arbeide med stykklister</span><span class="sxs-lookup"><span data-stu-id="1cfde-129">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="1cfde-130">Lager</span><span class="sxs-lookup"><span data-stu-id="1cfde-130">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1cfde-131">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="1cfde-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1cfde-132">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1cfde-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]