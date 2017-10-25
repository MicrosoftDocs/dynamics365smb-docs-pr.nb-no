---
title: Opprette produksjonsordrehoder | Microsoft-dokumentasjon
description: "Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a><span data-ttu-id="a529b-103">Opprette produksjonsordrehoder</span><span class="sxs-lookup"><span data-stu-id="a529b-103">How to: Create Production Order Headers</span></span>
<span data-ttu-id="a529b-104">Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.</span><span class="sxs-lookup"><span data-stu-id="a529b-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="a529b-105">Produksjonsordrer opprettes vanligvis automatisk etter en planleggingsfunksjonen for å dekke et kjente behov.</span><span class="sxs-lookup"><span data-stu-id="a529b-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="a529b-106">Hvis du vil ha mer informasjon , kan du se [Planlegging](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="a529b-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="a529b-107">I fremgangsmåten nedenfor opprettes det en fast planlagt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="a529b-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="a529b-108">Du kan også opprette produksjonsordrer med en annen status.</span><span class="sxs-lookup"><span data-stu-id="a529b-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="a529b-109">Slik oppretter du et produksjonsordrehode</span><span class="sxs-lookup"><span data-stu-id="a529b-109">To create a production order header</span></span>  
1.  <span data-ttu-id="a529b-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a529b-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a529b-111">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a529b-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="a529b-112">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="a529b-112">In the **No.**</span></span> <span data-ttu-id="a529b-113">-feltet setter du inn neste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="a529b-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="a529b-114">I feltet **Kildetype** velger du produksjonsordrens kilde.</span><span class="sxs-lookup"><span data-stu-id="a529b-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="a529b-115">Her kan du velge å produsere for en rekke varer.</span><span class="sxs-lookup"><span data-stu-id="a529b-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="a529b-116">Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="a529b-116">For more information, see [How to: Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="a529b-117">I feltet **Kildenr.** velger du varenummer, familie eller salgshode for produksjonsordren som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="a529b-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="a529b-118">Fyll ut feltene **Antall** og **Forfallsdato** i henhold til dine spesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="a529b-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="a529b-119">Når produksjonskrav endres, for eksempel komponenter eller operasjoner, kan du raskt planlegge produksjonsordren på nytt.</span><span class="sxs-lookup"><span data-stu-id="a529b-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="a529b-120">Hvis du vil ha mer informasjon, se [Slik planlegger du på nytt eller fornyer produksjonsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a529b-120">For more information, see [How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a529b-121">Se også</span><span class="sxs-lookup"><span data-stu-id="a529b-121">See Also</span></span>  
<span data-ttu-id="a529b-122">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a529b-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a529b-123">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="a529b-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a529b-124">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a529b-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="a529b-125">Lager</span><span class="sxs-lookup"><span data-stu-id="a529b-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a529b-126">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="a529b-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a529b-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a529b-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

