---
title: Bruke produksjonsbunkeenheten | Microsoft-dokumentasjon
description: Hvis en vare lagerføres i én enhet, men produseres i en annen, må produksjonsordren bruke en produksjonsbunkeenhet til å beregne riktig antall komponenter. Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c78430de1c45646e54fb8551cd4a8dcfbbfcc4e4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383303"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a><span data-ttu-id="be296-104">Arbeide med produksjonsbunkeenhet</span><span class="sxs-lookup"><span data-stu-id="be296-104">Work with Manufacturing Batch Units of Measure</span></span>
<span data-ttu-id="be296-105">Hvis en vare lagerføres i én enhet, men produseres i en annen, opprettes en produksjonsordre som bruker en produksjonsbunkeenhet til å beregne riktig antall komponenter mens kjørselen **Forny produksjonsordre** kjøres.</span><span class="sxs-lookup"><span data-stu-id="be296-105">If an item is stocked in one unit of measure but produced in another, a production order is created that uses a manufacturing batch unit of measure to calculate the correct quantity of the components during the **Refresh Production Order** batch job.</span></span> <span data-ttu-id="be296-106">Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn.</span><span class="sxs-lookup"><span data-stu-id="be296-106">An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.</span></span>  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a><span data-ttu-id="be296-107">Slik oppretter du en produksjonsstykkliste ved å bruke en produksjonsbunkeenhet</span><span class="sxs-lookup"><span data-stu-id="be296-107">To create a production BOM using a batch unit of measure</span></span>  
1.  <span data-ttu-id="be296-108">Produksjonsbunkeenheten defineres som en alternativ enhet på **Vareenheter**-siden for varen som skal produseres.</span><span class="sxs-lookup"><span data-stu-id="be296-108">The manufacturing batch unit of measure is set up as an alternative unit of measure on the **Item Units of Measure** page on the item to be produced.</span></span> <span data-ttu-id="be296-109">Bunkeenheten erstatter ikke lagerenheten for varen.</span><span class="sxs-lookup"><span data-stu-id="be296-109">The batch unit of measure will not replace the base unit of measure on the item.</span></span>  
2.  <span data-ttu-id="be296-110">Opprett en produksjonsstykkliste for varen som er definert med produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-110">Create a production BOM for the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="be296-111">Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsstykklister](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="be296-111">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>  
3.  <span data-ttu-id="be296-112">I **Enhetskode**-feltet velger du den relevante produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-112">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure.</span></span>  
4.  <span data-ttu-id="be296-113">Angi antallet av komponentvaren som trengs for å opprette denne bunkeenheten, i **Antall per**-feltet for hver linje i produksjonsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="be296-113">For each production BOM line, in the **Quantity Per** field, enter the quantity of this component item that is required to create this batch unit of measure.</span></span>  
5.  <span data-ttu-id="be296-114">Åpne **varekortet** for den relaterte varen.</span><span class="sxs-lookup"><span data-stu-id="be296-114">Open the **Item Card** for the related item.</span></span>  

    <span data-ttu-id="be296-115">På hurtigfanen **Etterfylling**, i feltet **Produksjonsstykklistenr.**, velger du produksjonsstykklisten du opprettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="be296-115">On the **Replenishment** FastTab, in the **Production BOM No.** field, select the production BOM created above.</span></span>  
6.  <span data-ttu-id="be296-116">Opprett et produksjonsordrehode ved å bruke varen som er definert med produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-116">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span> <span data-ttu-id="be296-117">Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="be296-117">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  
7.  <span data-ttu-id="be296-118">Velg **Forny**-handlingen, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="be296-118">Choose the **Refresh** action, and then choose  the **OK** button.</span></span>  

<span data-ttu-id="be296-119">På hurtigfanen **Linjer** velger du **Linje**-handlingen, og deretter **Komponenter**-handlingen for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="be296-119">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="be296-120">Programmet beregner det riktige antallet av komponentene som trengs for å oppfylle produksjonsstykklisten, basert på produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-120">The application calculates the correct quantity of the components needed to satisfy the production BOM based on the manufacturing batch unit of measure.</span></span>  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a><span data-ttu-id="be296-121">Slik beregner du en produksjonsbunkeenhet i en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="be296-121">To calculate a manufacturing batch unit of measure on a production order</span></span>  
1.  <span data-ttu-id="be296-122">Opprett et produksjonsordrehode ved å bruke varen som er definert med produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-122">Create a production order header using the item set up with the manufacturing batch unit of measure.</span></span>  
2.  <span data-ttu-id="be296-123">Skriv inn det samme varenummeret som brukes i hodet, i feltet **Varenr.** på produksjonsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="be296-123">In the **Item No.** field in the Production Order line, type the same item number used in the header.</span></span>  
3.  <span data-ttu-id="be296-124">Angi samme antall som brukes i hodet, i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="be296-124">In the **Quantity** field, enter the same quantity used in the header.</span></span>  
4.  <span data-ttu-id="be296-125">I **Enhetskode**-feltet velger du den relevante enhetskoden for produksjonsbunken.</span><span class="sxs-lookup"><span data-stu-id="be296-125">In the **Unit of Measure Code** field, select the manufacturing batch unit of measure code.</span></span>  
5.  <span data-ttu-id="be296-126">Velg handlingen **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="be296-126">Choose the **Refresh** action.</span></span>
6.  <span data-ttu-id="be296-127">Fjern merket for **Linjer** på hurtigfanen **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="be296-127">On the **Calculate** FastTab, clear the **Lines** check box.</span></span>  
7.  <span data-ttu-id="be296-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="be296-128">Choose the **OK** button.</span></span>  
8.  <span data-ttu-id="be296-129">På hurtigfanen **Linjer** velger du **Linje**-handlingen, og deretter **Komponenter**-handlingen for å vise resultatet.</span><span class="sxs-lookup"><span data-stu-id="be296-129">On the **Lines** FastTab, choose the **Line** action, and then choose the **Components** action to view the result.</span></span> <span data-ttu-id="be296-130">Det riktige antallet av komponentene som trengs for å oppfylle produksjonsstykklisten, beregnes basert på produksjonsbunkeenheten.</span><span class="sxs-lookup"><span data-stu-id="be296-130">The correct quantity of the components needed to satisfy the production BOM is calculated based on the manufacturing batch unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be296-131">Se også</span><span class="sxs-lookup"><span data-stu-id="be296-131">See Also</span></span>  
[<span data-ttu-id="be296-132">Opprette ruter</span><span class="sxs-lookup"><span data-stu-id="be296-132">Create Routings</span></span>](production-how-to-create-routings.md)  
<span data-ttu-id="be296-133">[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)   </span><span class="sxs-lookup"><span data-stu-id="be296-133">[Create Production BOMs](production-how-to-create-production-boms.md)   </span></span>  
[<span data-ttu-id="be296-134">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="be296-134">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="be296-135">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="be296-135">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="be296-136">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="be296-136">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="be296-137">Lager</span><span class="sxs-lookup"><span data-stu-id="be296-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="be296-138">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="be296-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="be296-139">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be296-139">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]