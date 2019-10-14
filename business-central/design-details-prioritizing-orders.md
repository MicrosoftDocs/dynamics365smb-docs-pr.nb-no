---
title: Designdetaljer – Prioritere ordrer | Microsoft-dokumentasjon
description: Les mer om hvordan du prioriterer for å dekke både behov og forsyningskrav.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 0a14b00b1172d616642495e3963097ddef48c54c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306919"
---
# <a name="design-details-prioritizing-orders"></a><span data-ttu-id="0ad18-103">Designdetaljer: Prioritere ordrer</span><span class="sxs-lookup"><span data-stu-id="0ad18-103">Design Details: Prioritizing Orders</span></span>
<span data-ttu-id="0ad18-104">I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i neste uke.</span><span class="sxs-lookup"><span data-stu-id="0ad18-104">Within a given SKU, the requested or available date represents the highest priority; the demand of today should be dealt with before the demand of next week.</span></span> <span data-ttu-id="0ad18-105">I tillegg til denne generelle prioriteten vil planleggingssystemet også foreslå hvilken type behov som må være oppfylt før andre behov oppfylles.</span><span class="sxs-lookup"><span data-stu-id="0ad18-105">But in addition to this overall priority, the planning system will also suggest which type of demand should be fulfilled before fulfilling another demand.</span></span> <span data-ttu-id="0ad18-106">Det vil foreslå hvilken forsyningskilde som skal brukes før du bruker andre forsyningskilder.</span><span class="sxs-lookup"><span data-stu-id="0ad18-106">Likewise, it will suggest what source of supply should be applied before applying other sources of supply.</span></span> <span data-ttu-id="0ad18-107">Dette gjøres i henhold til ordreprioriteter.</span><span class="sxs-lookup"><span data-stu-id="0ad18-107">This is done according to order priorities.</span></span>  

<span data-ttu-id="0ad18-108">Innlastet behov og forsyning bidrar til en profil for den beregnede beholdningen i henhold til følgende prioriteter:</span><span class="sxs-lookup"><span data-stu-id="0ad18-108">Loaded demand and supply contribute to a profile for the projected inventory according to the following priorities:</span></span>  

## <a name="priorities-on-the-demand-side"></a><span data-ttu-id="0ad18-109">Prioriteter på behovssiden</span><span class="sxs-lookup"><span data-stu-id="0ad18-109">Priorities on the Demand Side</span></span>  
1. <span data-ttu-id="0ad18-110">Allerede levert: Varepost</span><span class="sxs-lookup"><span data-stu-id="0ad18-110">Already shipped: Item Ledger Entry</span></span>  
2. <span data-ttu-id="0ad18-111">Bestillingsretur</span><span class="sxs-lookup"><span data-stu-id="0ad18-111">Purchase Return Order</span></span>  
3. <span data-ttu-id="0ad18-112">Ordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-112">Sales Order</span></span>  
4. <span data-ttu-id="0ad18-113">Serviceordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-113">Service Order</span></span>  
5. <span data-ttu-id="0ad18-114">Produksjonskomponentbehov</span><span class="sxs-lookup"><span data-stu-id="0ad18-114">Production Component Need</span></span>  
6. <span data-ttu-id="0ad18-115">Monteringsordrelinje</span><span class="sxs-lookup"><span data-stu-id="0ad18-115">Assembly Order Line</span></span>  
7. <span data-ttu-id="0ad18-116">Utgående overføringsordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-116">Outbound Transfer Order</span></span>  
8. <span data-ttu-id="0ad18-117">Rammebestilling (som ikke allerede er brukt av tilknyttede salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="0ad18-117">Blanket Order (that has not already been consumed by related sales orders)</span></span>  
9. <span data-ttu-id="0ad18-118">Prognose (som ikke allerede er brukt av andre salgsordrer)</span><span class="sxs-lookup"><span data-stu-id="0ad18-118">Forecast (that has not already been consumed by other sales orders)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0ad18-119">Bestillingsreturer tas vanligvis ikke med i forsyningsplanlegging. De skal alltid reserveres fra partiet som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="0ad18-119">Purchase returns are usually not involved in supply planning; they should always be reserved from the lot that is going to be returned.</span></span> <span data-ttu-id="0ad18-120">Hvis den ikke er reservert, spiller bestillingsreturer en rolle i tilgjengeligheten og er høyt prioritert for å unngå at planleggingssystemet foreslår at en forsyningsordre bare skal fungere som en bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="0ad18-120">If not reserved, purchase returns play a role in the availability and are highly prioritized to avoid that the planning system suggests a supply order just to serve a purchase return.</span></span>  

## <a name="priorities-on-the-supply-side"></a><span data-ttu-id="0ad18-121">Prioriteter på forsyningssiden</span><span class="sxs-lookup"><span data-stu-id="0ad18-121">Priorities on the Supply Side</span></span>  
1. <span data-ttu-id="0ad18-122">Allerede på lager: Varepost (planleggingsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="0ad18-122">Already in inventory: Item Ledger Entry (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="0ad18-123">Ordreretur (Planleggingsfleksibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="0ad18-123">Sales Return Order (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="0ad18-124">Inngående overføringsordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-124">Inbound Transfer Order</span></span>  
4. <span data-ttu-id="0ad18-125">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-125">Production Order</span></span>  
5. <span data-ttu-id="0ad18-126">Monteringsordre</span><span class="sxs-lookup"><span data-stu-id="0ad18-126">Assembly Order</span></span>  
6. <span data-ttu-id="0ad18-127">Bestilling</span><span class="sxs-lookup"><span data-stu-id="0ad18-127">Purchase Order</span></span>  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a><span data-ttu-id="0ad18-128">Prioritet som er knyttet til statusen for behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="0ad18-128">Priority Related to the State of Demand and Supply</span></span>  
<span data-ttu-id="0ad18-129">I tillegg til prioriteter som er angitt av behov og forsyning, definerer den nåværende ordretilstanden i utføringsprosessen, en prioritet.</span><span class="sxs-lookup"><span data-stu-id="0ad18-129">Apart from priorities given by the type of demand and supply, the present state of the orders in the execution process also defines a priority.</span></span> <span data-ttu-id="0ad18-130">Lageraktiviteter har for eksempel innvirkning, og det tas hensyn til statusen for salgs-, kjøps-, overførings-, monterings- og produksjonsordrer:</span><span class="sxs-lookup"><span data-stu-id="0ad18-130">For example, warehouse activities have an impact, and the status of sales, purchase, transfer, assembly, and production orders is taken into account:</span></span>  

1. <span data-ttu-id="0ad18-131">Delvis behandlet (Planleggingsfleksibilitet = Ingen)</span><span class="sxs-lookup"><span data-stu-id="0ad18-131">Partly handled (Planning Flexibility = None)</span></span>  
2. <span data-ttu-id="0ad18-132">Allerede i prosessen i lageret (planleggingsfleksibilitet = ingen)</span><span class="sxs-lookup"><span data-stu-id="0ad18-132">Already in process in the warehouse (Planning Flexibility = None)</span></span>  
3. <span data-ttu-id="0ad18-133">Frigitt – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="0ad18-133">Released – all order types (Planning Flexibility = Unlimited)</span></span>  
4. <span data-ttu-id="0ad18-134">Fast planlagt produksjonsordre (planleggingsfleksibiliteten = ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="0ad18-134">Firm Planned Production Order (Planning Flexibility = Unlimited)</span></span>  
5. <span data-ttu-id="0ad18-135">Planlagt/åpen – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)</span><span class="sxs-lookup"><span data-stu-id="0ad18-135">Planned/Open – all order types (Planning Flexibility = Unlimited)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ad18-136">Se også</span><span class="sxs-lookup"><span data-stu-id="0ad18-136">See Also</span></span>  
<span data-ttu-id="0ad18-137">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="0ad18-137">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="0ad18-138">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="0ad18-138">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="0ad18-139">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="0ad18-139">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
