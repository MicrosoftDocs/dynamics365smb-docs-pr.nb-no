---
title: Opprette produksjonsordrehoder | Microsoft-dokumentasjon
description: "Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 00ecc7031bc1c208444e89fbd13e2f2faf5fd413
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-production-order-headers"></a><span data-ttu-id="d9172-103">Opprette produksjonsordrehoder</span><span class="sxs-lookup"><span data-stu-id="d9172-103">Create Production Order Headers</span></span>
<span data-ttu-id="d9172-104">Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.</span><span class="sxs-lookup"><span data-stu-id="d9172-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="d9172-105">Produksjonsordrer opprettes vanligvis automatisk etter en planleggingsfunksjonen for å dekke et kjente behov.</span><span class="sxs-lookup"><span data-stu-id="d9172-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="d9172-106">Hvis du vil ha mer informasjon , kan du se [Planlegging](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="d9172-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="d9172-107">I fremgangsmåten nedenfor opprettes det en fast planlagt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="d9172-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="d9172-108">Du kan også opprette produksjonsordrer med en annen status.</span><span class="sxs-lookup"><span data-stu-id="d9172-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="d9172-109">Slik oppretter du et produksjonsordrehode</span><span class="sxs-lookup"><span data-stu-id="d9172-109">To create a production order header</span></span>  
1.  <span data-ttu-id="d9172-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d9172-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d9172-111">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d9172-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="d9172-112">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="d9172-112">In the **No.**</span></span> <span data-ttu-id="d9172-113">-feltet setter du inn neste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="d9172-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="d9172-114">I feltet **Kildetype** velger du produksjonsordrens kilde.</span><span class="sxs-lookup"><span data-stu-id="d9172-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="d9172-115">Her kan du velge å produsere for en rekke varer.</span><span class="sxs-lookup"><span data-stu-id="d9172-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="d9172-116">Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="d9172-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="d9172-117">I feltet **Kildenr.** velger du varenummer, familie eller salgshode for produksjonsordren som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="d9172-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="d9172-118">Fyll ut feltene **Antall** og **Forfallsdato** i henhold til dine spesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="d9172-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="d9172-119">Når produksjonskrav endres, for eksempel komponenter eller operasjoner, kan du raskt planlegge produksjonsordren på nytt.</span><span class="sxs-lookup"><span data-stu-id="d9172-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="d9172-120">Hvis du vil ha mer informasjon, se [Planlegge på nytt eller fornye produksjonsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="d9172-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="d9172-121">Se også</span><span class="sxs-lookup"><span data-stu-id="d9172-121">See Also</span></span>  
<span data-ttu-id="d9172-122">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d9172-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="d9172-123">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="d9172-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="d9172-124">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d9172-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="d9172-125">Lager</span><span class="sxs-lookup"><span data-stu-id="d9172-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d9172-126">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d9172-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d9172-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9172-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

