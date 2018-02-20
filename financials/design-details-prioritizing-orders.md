---
title: "Designdetaljer – Prioritere ordrer | Microsoft-dokumentasjon"
description: "Les mer om hvordan du prioriterer for å dekke både behov og forsyningskrav."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="5c047-103">Designdetaljer: Prioritere ordrer</span><span class="sxs-lookup"><span data-stu-id="5c047-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="5c047-104">I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i neste uke.</span><span class="sxs-lookup"><span data-stu-id="5c047-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="5c047-105">I tillegg til denne generelle prioriteten vil planleggingssystemet også foreslå hvilken type behov som må være oppfylt før andre behov oppfylles.</span><span class="sxs-lookup"><span data-stu-id="5c047-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="5c047-106">Det vil foreslå hvilken forsyningskilde som skal brukes før du bruker andre forsyningskilder.</span><span class="sxs-lookup"><span data-stu-id="5c047-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="5c047-107">Dette gjøres i henhold til ordreprioriteter.</span><span class="sxs-lookup"><span data-stu-id="5c047-107">This is done according to order priorities.</span></span>  
  
<span data-ttu-id="5c047-108">Innlastet behov og forsyning bidrar til en profil for den beregnede beholdningen i henhold til følgende prioriteter:</span><span class="sxs-lookup"><span data-stu-id="5c047-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  
  
## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="5c047-109">Prioriteter på behovssiden</span><span class="sxs-lookup"><span data-stu-id="5c047-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="5c047-110">Allerede levert: Varepost</span><span class="sxs-lookup"><span data-stu-id="5c047-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="5c047-111">Bestillingsretur</span><span class="sxs-lookup"><span data-stu-id="5c047-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="5c047-112">Ordre</span><span class="sxs-lookup"><span data-stu-id="5c047-112">Sales Order</span></span>  
4. <span data-ttu-id="5c047-113">Serviceordre</span><span class="sxs-lookup"><span data-stu-id="5c047-113">Service Order</span></span>  
5. <span data-ttu-id="5c047-114">Produksjonskomponentbehov</span><span class="sxs-lookup"><span data-stu-id="5c047-114">Production Component Need</span></span>  
6. <span data-ttu-id="5c047-115">Monteringsordrelinje</span><span class="sxs-lookup"><span data-stu-id="5c047-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="5c047-116">Utgående overføringsordre</span><span class="sxs-lookup"><span data-stu-id="5c047-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="5c047-117">Rammebestilling (som ikke allerede er brukt av tilknyttede salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="5c047-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="5c047-118">Prognose (som ikke allerede er brukt av andre salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="5c047-118">Forecast (that has not already been consumed by other sales orders)</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="5c047-119">Bestillingsreturer tas vanligvis ikke med i forsyningsplanlegging. De skal alltid reserveres fra partiet som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="5c047-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="5c047-120">Hvis den ikke er reservert, spiller bestillingsreturer en rolle i tilgjengeligheten og er høyt prioritert for å unngå at planleggingssystemet foreslår at en forsyningsordre bare skal fungere som en bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="5c047-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  
  
## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="5c047-121">Prioriteter på forsyningssiden</span><span class="sxs-lookup"><span data-stu-id="5c047-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="5c047-122">Allerede på lager: Varepost (planleggingsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="5c047-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="5c047-123">Ordreretur (Planleggingsfleksibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="5c047-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="5c047-124">Inngående overføringsordre</span><span class="sxs-lookup"><span data-stu-id="5c047-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="5c047-125">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="5c047-125">Production Order</span></span>  
5. <span data-ttu-id="5c047-126">Monteringsordre</span><span class="sxs-lookup"><span data-stu-id="5c047-126">Assembly Order</span></span>  
6. <span data-ttu-id="5c047-127">Bestilling</span><span class="sxs-lookup"><span data-stu-id="5c047-127">Purchase Order</span></span>  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="5c047-128">Prioritet som er knyttet til statusen for behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="5c047-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="5c047-129">I tillegg til prioriteter som er angitt av behov og forsyning, definerer den nåværende ordretilstanden i utføringsprosessen, en prioritet.</span><span class="sxs-lookup"><span data-stu-id="5c047-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="5c047-130">Lageraktiviteter har for eksempel innvirkning, og det tas hensyn til statusen for salgs-, kjøps-, overførings-, monterings- og produksjonsordrer:</span><span class="sxs-lookup"><span data-stu-id="5c047-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  
  
1. <span data-ttu-id="5c047-131">Delvis behandlet (Planleggingsfleksibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="5c047-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="5c047-132">Allerede i prosessen i lageret (planleggingsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="5c047-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="5c047-133">Frigitt – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="5c047-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="5c047-134">Fast planlagt produksjonsordre (planleggingsfleksibiliteten = ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="5c047-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="5c047-135">Planlagt/åpen – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="5c047-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c047-136">Se også</span><span class="sxs-lookup"><span data-stu-id="5c047-136">See Also</span></span>  
<span data-ttu-id="5c047-137">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="5c047-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="5c047-138">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="5c047-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="5c047-139">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="5c047-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
