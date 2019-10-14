---
title: Designdetaljer – Holde seg under overflytnivået | Microsoft-dokumentasjon
description: Når Maks.ant. og Fast gjenbest.ant. brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden. Dette betyr at planleggingssystemet kan foreslå overflødig forsyning når endring av negativt behov eller positiv forsyning skjer utenfor den angitte tidsperioden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: bf602a0a7688c0459b4f7a3711e4f3d75bd8ef00
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306799"
---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="1637f-104">Designdetaljer: Holde seg under overflytnivået</span><span class="sxs-lookup"><span data-stu-id="1637f-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="1637f-105">Når Maks.ant. og Fast gjenbest.ant. brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="1637f-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="1637f-106">Dette betyr at planleggingssystemet kan foreslå overflødig forsyning når endring av negativt behov eller positiv forsyning skjer utenfor den angitte tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="1637f-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="1637f-107">Hvis det derfor blir foreslått en overflødig forsyning, vil planleggingssystemet beregne antallet forsyningen skal reduseres til (eller slettes) for å unngå overflødig forsyning.</span><span class="sxs-lookup"><span data-stu-id="1637f-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="1637f-108">Dette antallet kalles "overflyt nivået."</span><span class="sxs-lookup"><span data-stu-id="1637f-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="1637f-109">Overflyt formidles som en planleggingslinje med handlingen **Endre ant. (reduksjon)** eller **Avbryt** og følgende advarsel:</span><span class="sxs-lookup"><span data-stu-id="1637f-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="1637f-110">*Viktig: Den beregnede beholdningen [xx] er høyere enn overflytnivået [xx] på forfallsdatoen [xx].*</span><span class="sxs-lookup"><span data-stu-id="1637f-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="1637f-111">![Lageroverflytnivå](media/supplyplanning_2_overflow1_new.png "Lageroverflytnivå")</span><span class="sxs-lookup"><span data-stu-id="1637f-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "Inventory overflow level")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="1637f-112">Beregne overflytnivået</span><span class="sxs-lookup"><span data-stu-id="1637f-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="1637f-113">Overflytnivået beregnes på ulike måter avhengig av planleggingsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="1637f-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="1637f-114">Gjenbestillingsprinsippet Maks.ant</span><span class="sxs-lookup"><span data-stu-id="1637f-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="1637f-115">Overflytnivå = Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="1637f-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1637f-116">Hvis det finnes et minimumsordreantall, blir det lagt til som følger: Overflytnivå = Maksimumsbeholdning + Min. bestillingsantall.</span><span class="sxs-lookup"><span data-stu-id="1637f-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="1637f-117">Gjenbestillingsprinsippet for Fast gjenbest.ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="1637f-118">Overflytnivå = Gjenbestillingsantall + Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="1637f-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1637f-119">Hvis minimumsordreantallet er høyere enn gjenbestillingspunktet, vil dette erstatte slik: Overflytnivå = Gjenbestillingsantall + Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="1637f-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="1637f-120">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="1637f-120">Order Multiple</span></span>  
<span data-ttu-id="1637f-121">Hvis det finnes en bestillingsfaktor, vil den justere overflytnivået for gjenbestillingsprinsippene Maks.ant og Fast gjenbest.ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="1637f-122">Opprette planleggingslinjen med overflytadvarsel</span><span class="sxs-lookup"><span data-stu-id="1637f-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="1637f-123">Når en eksisterende forsyning fører til at den beregnede beholdningen blir høyere enn overflytnivået på slutten av en tidsperiode, opprettes en planleggingslinje.</span><span class="sxs-lookup"><span data-stu-id="1637f-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="1637f-124">For å advare om den potensielt overflødige forsyningen vises en advarsel på planleggingslinjen, feltet **Godta handlingsmelding** er ikke valgt og handlingsmeldingen er enten Avbryt eller Endre ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="1637f-125">Beregne antall for planleggingslinjen</span><span class="sxs-lookup"><span data-stu-id="1637f-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="1637f-126">Antall for planleggingslinje = Gjeldende forsyningsantall - (Beregnet beholdning – Overflytnivå)</span><span class="sxs-lookup"><span data-stu-id="1637f-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1637f-127">Som med alle advarselslinjer vil alle maksimum/minimum ordreantall eller bestillingsfaktor bli ignorert.</span><span class="sxs-lookup"><span data-stu-id="1637f-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="1637f-128">Angi handlingsmeldingstype</span><span class="sxs-lookup"><span data-stu-id="1637f-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="1637f-129">Hvis planleggingslinjeantall er større enn 0, er handlingsmeldingen Endre ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="1637f-130">Hvis planleggingslinjeantall er lik eller mindre enn 0, er handlingsmeldingen Avbryt</span><span class="sxs-lookup"><span data-stu-id="1637f-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="1637f-131">Skrive advarselsmeldingen</span><span class="sxs-lookup"><span data-stu-id="1637f-131">Composing the Warning Message</span></span>  
<span data-ttu-id="1637f-132">Hvis det oppstår overflyt, viser siden **Ikke-sporede planleggingselementer** en advarsel med følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="1637f-132">In case of overflow, the **Untracked Planning Elements** page displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="1637f-133">Det beregnede beholdningsnivået som utløste advarselen</span><span class="sxs-lookup"><span data-stu-id="1637f-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="1637f-134">Det beregnede overflytnivået</span><span class="sxs-lookup"><span data-stu-id="1637f-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="1637f-135">Forfallsdatoen for forsyningshendelsen.</span><span class="sxs-lookup"><span data-stu-id="1637f-135">The due date of the supply event.</span></span>  

<span data-ttu-id="1637f-136">Eksempel: "Den beregnede beholdningen 120 er høyere enn overflytnivået 60 28.01.11."</span><span class="sxs-lookup"><span data-stu-id="1637f-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="1637f-137">Scenario</span><span class="sxs-lookup"><span data-stu-id="1637f-137">Scenario</span></span>  
<span data-ttu-id="1637f-138">I dette scenariet endrer en kunde en ordre fra 70 til 40 enheter mellom to planleggingskjøringer.</span><span class="sxs-lookup"><span data-stu-id="1637f-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="1637f-139">Overflytfunksjonen trer i kraft for å redusere kjøpet som ble foreslått for det første salgsantallet.</span><span class="sxs-lookup"><span data-stu-id="1637f-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="1637f-140">Vareoppsett</span><span class="sxs-lookup"><span data-stu-id="1637f-140">Item setup</span></span>  

|<span data-ttu-id="1637f-141">Gjenbestillingsprinsipp</span><span class="sxs-lookup"><span data-stu-id="1637f-141">Reordering Policy</span></span>|<span data-ttu-id="1637f-142">Maks.ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="1637f-143">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="1637f-143">Maximum Order Quantity</span></span>|<span data-ttu-id="1637f-144">100</span><span class="sxs-lookup"><span data-stu-id="1637f-144">100</span></span>|  
|<span data-ttu-id="1637f-145">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="1637f-145">Reorder Point</span></span>|<span data-ttu-id="1637f-146">50</span><span class="sxs-lookup"><span data-stu-id="1637f-146">50</span></span>|  
|<span data-ttu-id="1637f-147">Beholdning</span><span class="sxs-lookup"><span data-stu-id="1637f-147">Inventory</span></span>|<span data-ttu-id="1637f-148">80</span><span class="sxs-lookup"><span data-stu-id="1637f-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="1637f-149">Situasjonen før salgsreduksjon</span><span class="sxs-lookup"><span data-stu-id="1637f-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="1637f-150">Hendelse</span><span class="sxs-lookup"><span data-stu-id="1637f-150">Event</span></span>|<span data-ttu-id="1637f-151">Endre ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-151">Change Qty.</span></span>|<span data-ttu-id="1637f-152">Beregnet lager</span><span class="sxs-lookup"><span data-stu-id="1637f-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="1637f-153">Dag én</span><span class="sxs-lookup"><span data-stu-id="1637f-153">Day one</span></span>|<span data-ttu-id="1637f-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="1637f-154">None</span></span>|<span data-ttu-id="1637f-155">80</span><span class="sxs-lookup"><span data-stu-id="1637f-155">80</span></span>|  
|<span data-ttu-id="1637f-156">Salg</span><span class="sxs-lookup"><span data-stu-id="1637f-156">Sale</span></span>|<span data-ttu-id="1637f-157">-70</span><span class="sxs-lookup"><span data-stu-id="1637f-157">-70</span></span>|<span data-ttu-id="1637f-158">10</span><span class="sxs-lookup"><span data-stu-id="1637f-158">10</span></span>|  
|<span data-ttu-id="1637f-159">Slutten av tidsperioden</span><span class="sxs-lookup"><span data-stu-id="1637f-159">End of time bucket</span></span>|<span data-ttu-id="1637f-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="1637f-160">None</span></span>|<span data-ttu-id="1637f-161">10</span><span class="sxs-lookup"><span data-stu-id="1637f-161">10</span></span>|  
|<span data-ttu-id="1637f-162">Foreslå ny bestilling</span><span class="sxs-lookup"><span data-stu-id="1637f-162">Suggest new purchase order</span></span>|<span data-ttu-id="1637f-163">+90</span><span class="sxs-lookup"><span data-stu-id="1637f-163">+90</span></span>|<span data-ttu-id="1637f-164">100</span><span class="sxs-lookup"><span data-stu-id="1637f-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="1637f-165">Situasjonen etter salgsreduksjon</span><span class="sxs-lookup"><span data-stu-id="1637f-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="1637f-166">Endre</span><span class="sxs-lookup"><span data-stu-id="1637f-166">Change</span></span>|<span data-ttu-id="1637f-167">Endre ant.</span><span class="sxs-lookup"><span data-stu-id="1637f-167">Change Qty.</span></span>|<span data-ttu-id="1637f-168">Beregnet lager</span><span class="sxs-lookup"><span data-stu-id="1637f-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="1637f-169">Dag én</span><span class="sxs-lookup"><span data-stu-id="1637f-169">Day one</span></span>|<span data-ttu-id="1637f-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="1637f-170">None</span></span>|<span data-ttu-id="1637f-171">80</span><span class="sxs-lookup"><span data-stu-id="1637f-171">80</span></span>|  
|<span data-ttu-id="1637f-172">Salg</span><span class="sxs-lookup"><span data-stu-id="1637f-172">Sale</span></span>|<span data-ttu-id="1637f-173">-40</span><span class="sxs-lookup"><span data-stu-id="1637f-173">-40</span></span>|<span data-ttu-id="1637f-174">40</span><span class="sxs-lookup"><span data-stu-id="1637f-174">40</span></span>|  
|<span data-ttu-id="1637f-175">Kjøp</span><span class="sxs-lookup"><span data-stu-id="1637f-175">Purchase</span></span>|<span data-ttu-id="1637f-176">+90</span><span class="sxs-lookup"><span data-stu-id="1637f-176">+90</span></span>|<span data-ttu-id="1637f-177">130</span><span class="sxs-lookup"><span data-stu-id="1637f-177">130</span></span>|  
|<span data-ttu-id="1637f-178">Slutten av tidsperioden</span><span class="sxs-lookup"><span data-stu-id="1637f-178">End of time bucket</span></span>|<span data-ttu-id="1637f-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="1637f-179">None</span></span>|<span data-ttu-id="1637f-180">130</span><span class="sxs-lookup"><span data-stu-id="1637f-180">130</span></span>|  
|<span data-ttu-id="1637f-181">Foreslå å redusere bestilling</span><span class="sxs-lookup"><span data-stu-id="1637f-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="1637f-182">ordre fra 90 til 60</span><span class="sxs-lookup"><span data-stu-id="1637f-182">order from 90 to 60</span></span>|<span data-ttu-id="1637f-183">-30</span><span class="sxs-lookup"><span data-stu-id="1637f-183">-30</span></span>|<span data-ttu-id="1637f-184">100</span><span class="sxs-lookup"><span data-stu-id="1637f-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="1637f-185">Resulterende planleggingslinjer</span><span class="sxs-lookup"><span data-stu-id="1637f-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="1637f-186">Én planleggingslinje (advarsel) blir opprettet for å redusere kjøpet med 30 fra 90 til 60, for å holde den beregnede beholdningen på 100 i henhold til overflytnivået.</span><span class="sxs-lookup"><span data-stu-id="1637f-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="1637f-187">![Planlegge i henhold til overflytnivå](media/nav_app_supply_planning_2_overflow2.png "Planlegge i henhold til overflytnivå")</span><span class="sxs-lookup"><span data-stu-id="1637f-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "Plan according to overflow level")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1637f-188">Uten overflytsfunksjonen vises det ingen advarsel hvis det beregnede beholdningsnivået er over maksimumsbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="1637f-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="1637f-189">Dette kan føre til en overflødig forsyning på 30.</span><span class="sxs-lookup"><span data-stu-id="1637f-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1637f-190">Se også</span><span class="sxs-lookup"><span data-stu-id="1637f-190">See Also</span></span>  
<span data-ttu-id="1637f-191">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1637f-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="1637f-192">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="1637f-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="1637f-193">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="1637f-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="1637f-194">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="1637f-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
