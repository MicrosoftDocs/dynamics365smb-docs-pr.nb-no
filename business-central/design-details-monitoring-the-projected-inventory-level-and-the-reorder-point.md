---
title: Designdetaljer – Overvåke forventet lagernivå og gjenbestillingspunkt | Microsoft-dokumentasjon
description: Lær hvordan lagerplanlegging skiller mellom forventet lagernivå og forventet disponibelt lagernivå.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3ab1fbc381638a31b601f872e7280d7dc5200fdb
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "935115"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a><span data-ttu-id="5cab5-103">Designdetaljer: Overvåke forventet lagernivå og gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="5cab5-103">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>
<span data-ttu-id="5cab5-104">Beholdning er en type forsyning, men for lagerplanlegging skiller planleggingssystemet mellom to lagernivåer:</span><span class="sxs-lookup"><span data-stu-id="5cab5-104">Inventory is a type of supply, but for inventory planning, the planning system distinguishes between two inventory levels:</span></span>  

* <span data-ttu-id="5cab5-105">Beregnet beholdning</span><span class="sxs-lookup"><span data-stu-id="5cab5-105">Projected inventory</span></span>  
* <span data-ttu-id="5cab5-106">Forventet disponibel beholdning</span><span class="sxs-lookup"><span data-stu-id="5cab5-106">Projected available inventory</span></span>  

## <a name="projected-inventory"></a><span data-ttu-id="5cab5-107">Beregnet lager</span><span class="sxs-lookup"><span data-stu-id="5cab5-107">Projected Inventory</span></span>  
<span data-ttu-id="5cab5-108">I utgangspunktet er den beregnede beholdningen antallet bruttobeholdning, inkludert forsyning og behov i fortiden, selv om det ikke er bokført, når du starter planleggingen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-108">Initially, projected inventory is the quantity of gross inventory, including supply and demand in the past even if not posted, when starting the planning process.</span></span> <span data-ttu-id="5cab5-109">I fremtiden blir dette et glidende beregnet beholdningsnivå som vedlikeholdes av bruttoantallene fra fremtidig forsyning og behov, fordi de innføres langs tidslinjen (reservert eller tildelt på andre måter).</span><span class="sxs-lookup"><span data-stu-id="5cab5-109">In the future, this becomes a moving projected inventory level that is maintained by gross quantities from future supply and demand because those are introduced along the time line (whether reserved or in other ways allocated).</span></span>  

<span data-ttu-id="5cab5-110">Den beregnede beholdningen brukes av planleggingssystemet til å overvåke gjenbestillingspunktet, og til å bestemme gjenbestillingsantallet når gjenbestillingsprinsippet Maks.ant. brukes.</span><span class="sxs-lookup"><span data-stu-id="5cab5-110">The projected inventory is used by the planning system to monitor the reorder point and to determine the reorder quantity when using the Maximum Qty. reordering policy.</span></span>  

## <a name="projected-available-inventory"></a><span data-ttu-id="5cab5-111">Forventet disponibel beholdning</span><span class="sxs-lookup"><span data-stu-id="5cab5-111">Projected Available Inventory</span></span>  
<span data-ttu-id="5cab5-112">Den forventede disponible beholdningen er delen av den beregnede beholdningen som på et gitt tidspunkt er disponibelt for å dekke behov.</span><span class="sxs-lookup"><span data-stu-id="5cab5-112">The projected available inventory is the part of the projected inventory that at a given point in time is available to fulfill demand.</span></span> <span data-ttu-id="5cab5-113">Den forventede disponible beholdningen brukes av planleggingsmotoren ved overvåking av sikkerhetslagernivået.</span><span class="sxs-lookup"><span data-stu-id="5cab5-113">The projected available inventory is used by the planning engine when monitoring the safety stock level.</span></span>  

<span data-ttu-id="5cab5-114">Den forventede disponible beholdningen brukes av planleggingssystemet til å overvåke sikkerhetslagernivået, siden sikkerhetslageret alltid må være disponibelt for å dekke uventet behov.</span><span class="sxs-lookup"><span data-stu-id="5cab5-114">The projected available inventory is used by the planning system to monitor the safety stock level, since the safety stock must always be available to serve unexpected demand.</span></span>  

## <a name="time-buckets"></a><span data-ttu-id="5cab5-115">Tidsperioder</span><span class="sxs-lookup"><span data-stu-id="5cab5-115">Time Buckets</span></span>  
<span data-ttu-id="5cab5-116">Det er svært viktig å ha god kontroll over det beregnede lagernivået for å oppdage når gjenbestillingspunktet nås eller overskrides og for å beregne riktig ordreantall gjenbestillingsprinsippet Maks.ant. brukes.</span><span class="sxs-lookup"><span data-stu-id="5cab5-116">Having a tight control of the projected inventory is crucial to detect when the reorder point is reached or crossed and to calculate the right order quantity when using the Maximum Qty. reordering policy.</span></span>  

<span data-ttu-id="5cab5-117">Som nevnt tidligere, blir forventet lagernivå beregnet ved starten av planleggingsperioden.</span><span class="sxs-lookup"><span data-stu-id="5cab5-117">As stated earlier, the projected inventory level is calculated at the start of the planning period.</span></span> <span data-ttu-id="5cab5-118">Det er et bruttonivå som ikke tar hensyn til reservasjoner og lignende fordelinger.</span><span class="sxs-lookup"><span data-stu-id="5cab5-118">It is a gross level that does not consider reservations and similar allocations.</span></span> <span data-ttu-id="5cab5-119">For å overvåke dette beholdningsnivået i løpet av planleggingssekvensen overvåker systemet de aggregerte endringene gjennom en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="5cab5-119">To monitor this inventory level during the planning sequence, the system monitors the aggregated changes over a period of time, a time bucket.</span></span> <span data-ttu-id="5cab5-120">Systemet sikrer at tidsperioden er minst én dag, siden dette er den mest nøyaktige tidsenheten for en behovs- eller forsyningshendelse.</span><span class="sxs-lookup"><span data-stu-id="5cab5-120">The system ensures that the time bucket is at least one day since it is the most precise unit of time for a demand or supply event.</span></span>  

## <a name="determining-the-projected-inventory-level"></a><span data-ttu-id="5cab5-121">Fastslå forventet beholdningsnivå</span><span class="sxs-lookup"><span data-stu-id="5cab5-121">Determining the Projected Inventory Level</span></span>  
<span data-ttu-id="5cab5-122">Følgende sekvens beskriver hvordan det forventede beholdningsnivået fastsettes:</span><span class="sxs-lookup"><span data-stu-id="5cab5-122">The following sequence describes how the projected inventory level is determined:</span></span>  

* <span data-ttu-id="5cab5-123">Når en forsyningshendelse, for eksempel en bestilling er helt planlagt, økes den beregnede beholdningen på forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-123">When a supply event, such as a purchase order has been totally planned, it will increase the projected inventory on its due date.</span></span>  
* <span data-ttu-id="5cab5-124">Når en behovshendelse er fullstendig dekket, reduserer den ikke den beregnede beholdningen med en gang.</span><span class="sxs-lookup"><span data-stu-id="5cab5-124">When a demand event has been fully satisfied, it will not decrease the projected inventory right away.</span></span> <span data-ttu-id="5cab5-125">I stedet bokføres en reduksjonspåminnelse, som er en intern post som inneholder dato og antall for bidrag til den beregnede beholdningen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-125">Instead, it posts a decrease reminder, which is an internal record that holds the date and quantity of the contribution to the projected inventory.</span></span>  
* <span data-ttu-id="5cab5-126">Når en påfølgende forsyningshendelse planlegges og plasseres på tidslinjen, undersøkes de bokførte reduksjonspåminnelsene enkeltvis frem til den planlagte datoen for forsyningen samtidig som den beregnede beholdningen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="5cab5-126">When a subsequent supply event is planned and placed on the time line, the posted decrease reminders are investigated one by one up until the planned date of the supply while updating the projected inventory.</span></span> <span data-ttu-id="5cab5-127">Under denne prosessen kan det hende at gjenbestillingspunktnivået for påminnelsen om intern økning nås eller passeres.</span><span class="sxs-lookup"><span data-stu-id="5cab5-127">During this process, the reorder point level of the internal increase reminder may be reached or crossed.</span></span>  
* <span data-ttu-id="5cab5-128">Hvis en ny forsyningsordre blir introdusert, kontrollerer systemet om det er angitt før gjeldende forsyning.</span><span class="sxs-lookup"><span data-stu-id="5cab5-128">If a new supply order is introduced, the system checks if it is entered before the current supply.</span></span> <span data-ttu-id="5cab5-129">Hvis det er tilfelle, blir den nye forsyningen gjeldende forsyning og balanseringen starter på nytt.</span><span class="sxs-lookup"><span data-stu-id="5cab5-129">If it is, the new supply becomes current supply and the balancing procedure starts over.</span></span>  

<span data-ttu-id="5cab5-130">Nedenfor vises en grafisk illustrasjon av dette prinsippet:</span><span class="sxs-lookup"><span data-stu-id="5cab5-130">The following shows a graphical illustration of this principle:</span></span>  

<span data-ttu-id="5cab5-131">![Fastslå forventet lagernivå](media/nav_app_supply_planning_2_projected_inventory.png "Fastslå forventet lagernivå")</span><span class="sxs-lookup"><span data-stu-id="5cab5-131">![Determining the Projected Inventory Level](media/nav_app_supply_planning_2_projected_inventory.png "Determining the Projected Inventory Level")</span></span>  

1. <span data-ttu-id="5cab5-132">Forsyning **Sa** med 4 (fast) lukker behov **Da** med -3.</span><span class="sxs-lookup"><span data-stu-id="5cab5-132">Supply **Sa** of 4 (fixed) closes Demand **Da** of -3.</span></span>  
2. <span data-ttu-id="5cab5-133">CloseDemand: Opprett en reduksjonspåminnelse med verdien -3 (vises ikke).</span><span class="sxs-lookup"><span data-stu-id="5cab5-133">CloseDemand: Create a decrease reminder of -3 (not shown).</span></span>  
3. <span data-ttu-id="5cab5-134">Forsyning **Sa** lukkes med et overskudd på 1 (det finnes ikke mer behov).</span><span class="sxs-lookup"><span data-stu-id="5cab5-134">Supply **Sa** is closed with a surplus of 1 (no more demand exists).</span></span>  

     <span data-ttu-id="5cab5-135">Dermed økes det beregnede beholdningsnivået til + 4, mens den forventede **disponible** beholdningen blir -1.</span><span class="sxs-lookup"><span data-stu-id="5cab5-135">This increases the projected inventory level to +4, while the projected **available** inventory becomes -1.</span></span>  

4. <span data-ttu-id="5cab5-136">Den neste forsyningen **Sb** 2 (en annen ordre) er allerede plassert på tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-136">The next supply **Sb** of 2 (another order) has already been placed on the timeline.</span></span>  
5. <span data-ttu-id="5cab5-137">Systemet kontrollerer om det kommer en reduksjonspåminnelse før **Sb** (det gjør det ikke, så ingen handling utføres).</span><span class="sxs-lookup"><span data-stu-id="5cab5-137">System checks if there is any decrease reminder preceding **Sb** (there is not, so no action is taken).</span></span>  
6. <span data-ttu-id="5cab5-138">Systemet lukker forsyning **Sb** (det finnes ikke mer behov), ved å A: redusere den til 0 (annullere) eller B: la den være som den er.</span><span class="sxs-lookup"><span data-stu-id="5cab5-138">System closes supply **Sb** (no more demand exists)—either A: by reducing it to 0 (cancel) or B: by leaving as is.</span></span>  

     <span data-ttu-id="5cab5-139">Dette øker det beregnede beholdningsnivået (A: +0 => +4 eller B: +2 = +6).</span><span class="sxs-lookup"><span data-stu-id="5cab5-139">This increases the projected inventory level (A: +0 => +4 or B: +2 = +6).</span></span>  

7. <span data-ttu-id="5cab5-140">Systemet foretar en sluttkontroll: Finnes det noen reduksjonspåminnelse?</span><span class="sxs-lookup"><span data-stu-id="5cab5-140">System makes a final check: Is there any decrease reminder?</span></span> <span data-ttu-id="5cab5-141">Ja, det er en på datoen for **Da**.</span><span class="sxs-lookup"><span data-stu-id="5cab5-141">Yes, there is one on the date of **Da**.</span></span>  
8. <span data-ttu-id="5cab5-142">Systemet legger til reduksjonspåminnelsen på -3 i det beregnede beholdningsnivået, enten A: +4 -3 = 1 eller B: +6 -3 = +3.</span><span class="sxs-lookup"><span data-stu-id="5cab5-142">System adds the decrease reminder of -3 reminder to the projected inventory level, either A: +4 -3 = 1 or B: +6 -3 = +3.</span></span>  
9. <span data-ttu-id="5cab5-143">I A-tilfeller oppretter systemet en fremoverplanlagt ordre på datoen **Da**.</span><span class="sxs-lookup"><span data-stu-id="5cab5-143">In case of A, the system creates a forward-scheduled order starting on date **Da**.</span></span>  

     <span data-ttu-id="5cab5-144">I B-tilfeller nås gjenbestillingspunktet, og det opprettes en ny ordre.</span><span class="sxs-lookup"><span data-stu-id="5cab5-144">In case of B, the reorder point is reached and a new order is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5cab5-145">Se også</span><span class="sxs-lookup"><span data-stu-id="5cab5-145">See Also</span></span>  
<span data-ttu-id="5cab5-146">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5cab5-146">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="5cab5-147">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="5cab5-147">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="5cab5-148">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="5cab5-148">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="5cab5-149">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="5cab5-149">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
