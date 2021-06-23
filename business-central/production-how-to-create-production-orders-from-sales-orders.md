---
title: Opprette produksjonsordrer fra ordrer
description: Du kan opprette produksjonsordrer fra ordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115239"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="4db81-103">Opprette produksjonsordrer fra ordrer</span><span class="sxs-lookup"><span data-stu-id="4db81-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="4db81-104">Du kan opprette produksjonsordrer for produserte varer direkte fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="4db81-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="4db81-105">Slik oppretter du en produksjonsordre fra en ordre</span><span class="sxs-lookup"><span data-stu-id="4db81-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="4db81-106">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4db81-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4db81-107">Velg ordren du vil opprette en produksjonsordre for.</span><span class="sxs-lookup"><span data-stu-id="4db81-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="4db81-108">Velg handlingen **Planlegging**.</span><span class="sxs-lookup"><span data-stu-id="4db81-108">Choose the **Planning** action.</span></span> <span data-ttu-id="4db81-109">På **Ordreplanlegging**-siden kan du se tilgjengeligheten til ordrevaren.</span><span class="sxs-lookup"><span data-stu-id="4db81-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="4db81-110">Velg handlingen **Opprett prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="4db81-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="4db81-111">Angi status og ordretype.</span><span class="sxs-lookup"><span data-stu-id="4db81-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="4db81-112">Velg knappen **Ja** for å opprette en eller flere produksjonsordrer for linjene med **Prod.ordre** i feltet **Etterfyllingssystem**.</span><span class="sxs-lookup"><span data-stu-id="4db81-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="4db81-113">Behovslinjer i den opprettede produksjonsordren som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="4db81-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="4db81-114">Når du har generert disse produksjonsordrene, må du huske å identifisere eventuelle komponentbehov som ikke er oppfylt, for dem ved å bruke siden **Ordreplanlegging** eller funksjonen **Planlegg på nytt** fra opprettede ordrer.</span><span class="sxs-lookup"><span data-stu-id="4db81-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="4db81-115">Ordretype</span><span class="sxs-lookup"><span data-stu-id="4db81-115">Order type</span></span>  
<span data-ttu-id="4db81-116">Du kan velge mellom to måter å opprette produksjonsordrer på, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4db81-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="4db81-117">Alternativ</span><span class="sxs-lookup"><span data-stu-id="4db81-117">Option</span></span>|<span data-ttu-id="4db81-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4db81-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4db81-119">Vareordre</span><span class="sxs-lookup"><span data-stu-id="4db81-119">Item Order</span></span>|<span data-ttu-id="4db81-120">Det opprettes en produksjonsordre for hver nødvendige ordre for produksjonsordren som representeres av en linje i **Ordreplanlegging**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="4db81-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="4db81-121">Prosjektordre</span><span class="sxs-lookup"><span data-stu-id="4db81-121">Project Order</span></span>|<span data-ttu-id="4db81-122">Det opprettes en produksjonsordre for alle nødvendige ordrer for produksjonsordren som representeres av linjer i **Ordreplanlegging**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="4db81-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="4db81-123">Når du bruker prosjektordrer, inneholder feltet **Kildetype** i produksjonsordren **Salgshode**, og ordren har flere linjer, en for hver salgslinjevare som må produseres.</span><span class="sxs-lookup"><span data-stu-id="4db81-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="4db81-124">Se også</span><span class="sxs-lookup"><span data-stu-id="4db81-124">See Also</span></span>  
[<span data-ttu-id="4db81-125">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="4db81-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4db81-126">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4db81-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4db81-127">Lager</span><span class="sxs-lookup"><span data-stu-id="4db81-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4db81-128">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4db81-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4db81-129">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="4db81-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="4db81-130">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="4db81-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="4db81-131">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4db81-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
