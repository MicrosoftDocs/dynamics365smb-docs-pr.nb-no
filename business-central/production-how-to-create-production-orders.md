---
title: Opprette produksjonsordrehoder | Microsoft-dokumentasjon
description: Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70a6f2e583e5ba78eecae0a25d6533d8265414ca
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253312"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="07323-103">Opprette produksjonsordrehoder</span><span class="sxs-lookup"><span data-stu-id="07323-103">Create Production Order Headers</span></span>
<span data-ttu-id="07323-104">Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.</span><span class="sxs-lookup"><span data-stu-id="07323-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="07323-105">Produksjonsordrer opprettes vanligvis automatisk etter en planleggingsfunksjonen for å dekke et kjente behov.</span><span class="sxs-lookup"><span data-stu-id="07323-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="07323-106">Hvis du vil ha mer informasjon , kan du se [Planlegging](production-planning.md).</span><span class="sxs-lookup"><span data-stu-id="07323-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="07323-107">I fremgangsmåten nedenfor opprettes det en fast planlagt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="07323-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="07323-108">Du kan også opprette produksjonsordrer med en annen status.</span><span class="sxs-lookup"><span data-stu-id="07323-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="07323-109">Slik oppretter du et produksjonsordrehode</span><span class="sxs-lookup"><span data-stu-id="07323-109">To create a production order header</span></span>  
1.  <span data-ttu-id="07323-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="07323-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="07323-111">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="07323-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="07323-112">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="07323-112">In the **No.**</span></span> <span data-ttu-id="07323-113">-feltet setter du inn neste nummer i serien.</span><span class="sxs-lookup"><span data-stu-id="07323-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="07323-114">I feltet **Kildetype** velger du produksjonsordrens kilde.</span><span class="sxs-lookup"><span data-stu-id="07323-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="07323-115">Her kan du velge å produsere for en rekke varer.</span><span class="sxs-lookup"><span data-stu-id="07323-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="07323-116">Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsfamilier](production-how-work-family.md).</span><span class="sxs-lookup"><span data-stu-id="07323-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="07323-117">I feltet **Kildenr.** velger du varenummer, familie eller salgshode for produksjonsordren som skal genereres.</span><span class="sxs-lookup"><span data-stu-id="07323-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="07323-118">Fyll ut feltene **Antall** og **Forfallsdato** i henhold til dine spesifikasjoner.</span><span class="sxs-lookup"><span data-stu-id="07323-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="07323-119">Når produksjonskrav endres, for eksempel komponenter eller operasjoner, kan du raskt planlegge produksjonsordren på nytt.</span><span class="sxs-lookup"><span data-stu-id="07323-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="07323-120">Hvis du vil ha mer informasjon, se [Planlegge på nytt eller fornye produksjonsordrer direkte](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="07323-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="07323-121">Se også</span><span class="sxs-lookup"><span data-stu-id="07323-121">See Also</span></span>  
<span data-ttu-id="07323-122">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="07323-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="07323-123">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="07323-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="07323-124">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="07323-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="07323-125">Lager</span><span class="sxs-lookup"><span data-stu-id="07323-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="07323-126">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="07323-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="07323-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="07323-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
