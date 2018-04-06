---
title: "Designdetaljer – Holde seg under overflytnivået | Microsoft-dokumentasjon"
description: "Når Maks.ant. og Fast gjenbest.ant. brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden. Dette betyr at planleggingssystemet kan foreslå overflødig forsyning når endring av negativt behov eller positiv forsyning skjer utenfor den angitte tidsperioden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="ce5ae-104">Designdetaljer: Holde seg under overflytnivået</span><span class="sxs-lookup"><span data-stu-id="ce5ae-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="ce5ae-105">Når Maks.ant. og Fast gjenbest.ant. brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="ce5ae-106">Dette betyr at planleggingssystemet kan foreslå overflødig forsyning når endring av negativt behov eller positiv forsyning skjer utenfor den angitte tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="ce5ae-107">Hvis det derfor blir foreslått en overflødig forsyning, vil planleggingssystemet beregne antallet forsyningen skal reduseres til (eller slettes) for å unngå overflødig forsyning.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="ce5ae-108">Dette antallet kalles "overflyt nivået."</span><span class="sxs-lookup"><span data-stu-id="ce5ae-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="ce5ae-109">Overflyt formidles som en planleggingslinje med handlingen **Endre ant. (reduksjon)** eller **Avbryt** og følgende advarsel:</span><span class="sxs-lookup"><span data-stu-id="ce5ae-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="ce5ae-110">*Viktig: Den beregnede beholdningen [xx] er høyere enn overflytnivået [xx] på forfallsdatoen [xx].*</span><span class="sxs-lookup"><span data-stu-id="ce5ae-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="ce5ae-111">![Lageroverflytnivå](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="ce5ae-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="ce5ae-112">Beregne overflytnivået</span><span class="sxs-lookup"><span data-stu-id="ce5ae-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="ce5ae-113">Overflytnivået beregnes på ulike måter avhengig av planleggingsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="ce5ae-114">Gjenbestillingsprinsippet Maks.ant</span><span class="sxs-lookup"><span data-stu-id="ce5ae-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="ce5ae-115">Overflytnivå = Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="ce5ae-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce5ae-116">Hvis det finnes et minimumsordreantall, blir det lagt til som følger: Overflytnivå = Maksimumsbeholdning + Min. bestillingsantall.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="ce5ae-117">Gjenbestillingsprinsippet for Fast gjenbest.ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="ce5ae-118">Overflytnivå = Gjenbestillingsantall + Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="ce5ae-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce5ae-119">Hvis minimumsordreantallet er høyere enn gjenbestillingspunktet, vil dette erstatte slik: Overflytnivå = Gjenbestillingsantall + Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="ce5ae-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="ce5ae-120">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="ce5ae-120">Order Multiple</span></span>  
<span data-ttu-id="ce5ae-121">Hvis det finnes en bestillingsfaktor, vil den justere overflytnivået for gjenbestillingsprinsippene Maks.ant og Fast gjenbest.ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="ce5ae-122">Opprette planleggingslinjen med overflytadvarsel</span><span class="sxs-lookup"><span data-stu-id="ce5ae-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="ce5ae-123">Når en eksisterende forsyning fører til at den beregnede beholdningen blir høyere enn overflytnivået på slutten av en tidsperiode, opprettes en planleggingslinje.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="ce5ae-124">For å advare om den potensielt overflødige forsyningen vises en advarsel på planleggingslinjen, feltet **Godta handlingsmelding** er ikke valgt og handlingsmeldingen er enten Avbryt eller Endre ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="ce5ae-125">Beregne antall for planleggingslinjen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="ce5ae-126">Antall for planleggingslinje = Gjeldende forsyningsantall - (Beregnet beholdning – Overflytnivå)</span><span class="sxs-lookup"><span data-stu-id="ce5ae-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce5ae-127">Som med alle advarselslinjer vil alle maksimum/minimum ordreantall eller bestillingsfaktor bli ignorert.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="ce5ae-128">Angi handlingsmeldingstype</span><span class="sxs-lookup"><span data-stu-id="ce5ae-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="ce5ae-129">Hvis planleggingslinjeantall er større enn 0, er handlingsmeldingen Endre ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="ce5ae-130">Hvis planleggingslinjeantall er lik eller mindre enn 0, er handlingsmeldingen Avbryt</span><span class="sxs-lookup"><span data-stu-id="ce5ae-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="ce5ae-131">Skrive advarselsmeldingen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-131">Composing the Warning Message</span></span>  
<span data-ttu-id="ce5ae-132">Hvis det oppstår overflyt, viser vinduet **Ikke-sporede planleggingselementer** en advarsel med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="ce5ae-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="ce5ae-133">Det beregnede beholdningsnivået som utløste advarselen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="ce5ae-134">Det beregnede overflytnivået</span><span class="sxs-lookup"><span data-stu-id="ce5ae-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="ce5ae-135">Forfallsdatoen for forsyningshendelsen.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-135">The due date of the supply event.</span></span>  

<span data-ttu-id="ce5ae-136">Eksempel: "Den beregnede beholdningen 120 er høyere enn overflytnivået 60 28.01.11."</span><span class="sxs-lookup"><span data-stu-id="ce5ae-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="ce5ae-137">Scenario</span><span class="sxs-lookup"><span data-stu-id="ce5ae-137">Scenario</span></span>  
<span data-ttu-id="ce5ae-138">I dette scenariet endrer en kunde en ordre fra 70 til 40 enheter mellom to planleggingskjøringer.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="ce5ae-139">Overflytfunksjonen trer i kraft for å redusere kjøpet som ble foreslått for det første salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="ce5ae-140">Vareoppsett</span><span class="sxs-lookup"><span data-stu-id="ce5ae-140">Item setup</span></span>  

|<span data-ttu-id="ce5ae-141">Gjenbestillingsprinsipp</span><span class="sxs-lookup"><span data-stu-id="ce5ae-141">Reordering Policy</span></span>|<span data-ttu-id="ce5ae-142">Maks.ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="ce5ae-143">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="ce5ae-143">Maximum Order Quantity</span></span>|<span data-ttu-id="ce5ae-144">100</span><span class="sxs-lookup"><span data-stu-id="ce5ae-144">100</span></span>|  
|<span data-ttu-id="ce5ae-145">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="ce5ae-145">Reorder Point</span></span>|<span data-ttu-id="ce5ae-146">50</span><span class="sxs-lookup"><span data-stu-id="ce5ae-146">50</span></span>|  
|<span data-ttu-id="ce5ae-147">Beholdning</span><span class="sxs-lookup"><span data-stu-id="ce5ae-147">Inventory</span></span>|<span data-ttu-id="ce5ae-148">80</span><span class="sxs-lookup"><span data-stu-id="ce5ae-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="ce5ae-149">Situasjonen før salgsreduksjon</span><span class="sxs-lookup"><span data-stu-id="ce5ae-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="ce5ae-150">Hendelse</span><span class="sxs-lookup"><span data-stu-id="ce5ae-150">Event</span></span>|<span data-ttu-id="ce5ae-151">Endre ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-151">Change Qty.</span></span>|<span data-ttu-id="ce5ae-152">Beregnet lager</span><span class="sxs-lookup"><span data-stu-id="ce5ae-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="ce5ae-153">Dag én</span><span class="sxs-lookup"><span data-stu-id="ce5ae-153">Day one</span></span>|<span data-ttu-id="ce5ae-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-154">None</span></span>|<span data-ttu-id="ce5ae-155">80</span><span class="sxs-lookup"><span data-stu-id="ce5ae-155">80</span></span>|  
|<span data-ttu-id="ce5ae-156">Salg</span><span class="sxs-lookup"><span data-stu-id="ce5ae-156">Sale</span></span>|<span data-ttu-id="ce5ae-157">-70</span><span class="sxs-lookup"><span data-stu-id="ce5ae-157">-70</span></span>|<span data-ttu-id="ce5ae-158">10</span><span class="sxs-lookup"><span data-stu-id="ce5ae-158">10</span></span>|  
|<span data-ttu-id="ce5ae-159">Slutten av tidsperioden</span><span class="sxs-lookup"><span data-stu-id="ce5ae-159">End of time bucket</span></span>|<span data-ttu-id="ce5ae-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-160">None</span></span>|<span data-ttu-id="ce5ae-161">10</span><span class="sxs-lookup"><span data-stu-id="ce5ae-161">10</span></span>|  
|<span data-ttu-id="ce5ae-162">Foreslå ny bestilling</span><span class="sxs-lookup"><span data-stu-id="ce5ae-162">Suggest new purchase order</span></span>|<span data-ttu-id="ce5ae-163">+90</span><span class="sxs-lookup"><span data-stu-id="ce5ae-163">+90</span></span>|<span data-ttu-id="ce5ae-164">100</span><span class="sxs-lookup"><span data-stu-id="ce5ae-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="ce5ae-165">Situasjonen etter salgsreduksjon</span><span class="sxs-lookup"><span data-stu-id="ce5ae-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="ce5ae-166">Endre</span><span class="sxs-lookup"><span data-stu-id="ce5ae-166">Change</span></span>|<span data-ttu-id="ce5ae-167">Endre ant.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-167">Change Qty.</span></span>|<span data-ttu-id="ce5ae-168">Beregnet lager</span><span class="sxs-lookup"><span data-stu-id="ce5ae-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="ce5ae-169">Dag én</span><span class="sxs-lookup"><span data-stu-id="ce5ae-169">Day one</span></span>|<span data-ttu-id="ce5ae-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-170">None</span></span>|<span data-ttu-id="ce5ae-171">80</span><span class="sxs-lookup"><span data-stu-id="ce5ae-171">80</span></span>|  
|<span data-ttu-id="ce5ae-172">Salg</span><span class="sxs-lookup"><span data-stu-id="ce5ae-172">Sale</span></span>|<span data-ttu-id="ce5ae-173">-40</span><span class="sxs-lookup"><span data-stu-id="ce5ae-173">-40</span></span>|<span data-ttu-id="ce5ae-174">40</span><span class="sxs-lookup"><span data-stu-id="ce5ae-174">40</span></span>|  
|<span data-ttu-id="ce5ae-175">Kjøp</span><span class="sxs-lookup"><span data-stu-id="ce5ae-175">Purchase</span></span>|<span data-ttu-id="ce5ae-176">+90</span><span class="sxs-lookup"><span data-stu-id="ce5ae-176">+90</span></span>|<span data-ttu-id="ce5ae-177">130</span><span class="sxs-lookup"><span data-stu-id="ce5ae-177">130</span></span>|  
|<span data-ttu-id="ce5ae-178">Slutten av tidsperioden</span><span class="sxs-lookup"><span data-stu-id="ce5ae-178">End of time bucket</span></span>|<span data-ttu-id="ce5ae-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce5ae-179">None</span></span>|<span data-ttu-id="ce5ae-180">130</span><span class="sxs-lookup"><span data-stu-id="ce5ae-180">130</span></span>|  
|<span data-ttu-id="ce5ae-181">Foreslå å redusere bestilling</span><span class="sxs-lookup"><span data-stu-id="ce5ae-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="ce5ae-182">ordre fra 90 til 60</span><span class="sxs-lookup"><span data-stu-id="ce5ae-182">order from 90 to 60</span></span>|<span data-ttu-id="ce5ae-183">-30</span><span class="sxs-lookup"><span data-stu-id="ce5ae-183">-30</span></span>|<span data-ttu-id="ce5ae-184">100</span><span class="sxs-lookup"><span data-stu-id="ce5ae-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="ce5ae-185">Resulterende planleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="ce5ae-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="ce5ae-186">Én planleggingslinje (advarsel) blir opprettet for å redusere kjøpet med 30 fra 90 til 60, for å holde den beregnede beholdningen på 100 i henhold til overflytnivået.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="ce5ae-187">![Planlegg i henhold til overflytnivå](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="ce5ae-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ce5ae-188">Uten overflytsfunksjonen vises det ingen advarsel hvis det beregnede beholdningsnivået er over maksimumsbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="ce5ae-189">Dette kan føre til en overflødig forsyning på 30.</span><span class="sxs-lookup"><span data-stu-id="ce5ae-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce5ae-190">Se også</span><span class="sxs-lookup"><span data-stu-id="ce5ae-190">See Also</span></span>  
<span data-ttu-id="ce5ae-191">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="ce5ae-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="ce5ae-192">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="ce5ae-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="ce5ae-193">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="ce5ae-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="ce5ae-194">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="ce5ae-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

