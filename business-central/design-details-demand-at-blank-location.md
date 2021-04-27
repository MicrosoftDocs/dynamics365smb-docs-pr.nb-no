---
title: Designdetaljer – Behov og forsyning | Microsoft-dokumentasjon
description: Dette emnet introduserer konseptet med behov, som er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7dc15352b232a7dd4dc63d50db3b151e65f0fd51
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774208"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="689cd-103">Designdetaljer: Behov på tom lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="689cd-104">Når en bruker oppretter en behovshendelse, for eksempel en salgsordrelinje, tillater programmet at brukeren noen ganger angir en lokasjonskode og andre ganger ikke, dvs. bruker en tom lokasjon.</span><span class="sxs-lookup"><span data-stu-id="689cd-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="689cd-105">Når det gjelder behov med eller uten lokasjonskoder, fungerer planleggingssystemet på en enkel måte når følgende er tilfelle:</span><span class="sxs-lookup"><span data-stu-id="689cd-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="689cd-106">Behovslinjer har alltid lokasjonskoder, og systemet bruker LFEer fullt ut, inkludert det relevante lokasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="689cd-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="689cd-107">Behovslinjer har aldri lokasjonskoder, og systemet bruker ikke LFEer eller lokasjonsoppsett (se siste scenario i delen nedenfor).</span><span class="sxs-lookup"><span data-stu-id="689cd-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="689cd-108">Hvis behovshendelser imidlertid noen ganger har lokasjonskoder og andre ganger ikke, følger planleggingssystemet visse regler avhengig av oppsettet.</span><span class="sxs-lookup"><span data-stu-id="689cd-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="689cd-109">Behov i lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-109">Demand at Location</span></span>
<span data-ttu-id="689cd-110">Når planleggingssystemet oppdager behov i en lokasjon, fungerer det på ulike måter avhengig av tre viktige oppsettverdier.</span><span class="sxs-lookup"><span data-stu-id="689cd-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="689cd-111">Systemet søker etter tre oppsettsverdier etter tur under en planleggingskjøring, og planlegger i henhold til dem.</span><span class="sxs-lookup"><span data-stu-id="689cd-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="689cd-112">Er det merket av i feltet **Lokasjon obligatorisk**?</span><span class="sxs-lookup"><span data-stu-id="689cd-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="689cd-113">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="689cd-113">If yes, then:</span></span>

2. <span data-ttu-id="689cd-114">Finnes det lagerføringsenhet for varen?</span><span class="sxs-lookup"><span data-stu-id="689cd-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="689cd-115">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="689cd-115">If yes, then:</span></span>

    <span data-ttu-id="689cd-116">Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="689cd-117">Hvis nei:</span><span class="sxs-lookup"><span data-stu-id="689cd-117">If no, then:</span></span>

3. <span data-ttu-id="689cd-118">Inneholder feltet Komponenter ved lokasjon den nødvendige lokasjonskoden?</span><span class="sxs-lookup"><span data-stu-id="689cd-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="689cd-119">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="689cd-119">If yes, then:</span></span>

  <span data-ttu-id="689cd-120">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="689cd-121">Hvis nei:</span><span class="sxs-lookup"><span data-stu-id="689cd-121">If no, then:</span></span>

  <span data-ttu-id="689cd-122">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti, Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom, varer som bruker Gjenbestillingsprinsipp = Ordre, fortsetter å bruke Ordre sammen med de andre innstillingene.</span><span class="sxs-lookup"><span data-stu-id="689cd-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="689cd-123">Oppsettet for unntaksplanlegging som avgis som siste reaksjon i trinn 3 ovenfor, kalles "minimumsalternativet" i det følgende.</span><span class="sxs-lookup"><span data-stu-id="689cd-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="689cd-124">Dette planleggingsoppsettet dekker bare eksakt behov, og alle andre planleggingsparametere ignoreres.</span><span class="sxs-lookup"><span data-stu-id="689cd-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="689cd-125">Hvis du vil ha informasjon om variasjoner av planleggingslogikken, kan du se avsnittet nedenfor om scenarier.</span><span class="sxs-lookup"><span data-stu-id="689cd-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="689cd-126">Behov i tom lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-126">Demand at Blank Location</span></span>
<span data-ttu-id="689cd-127">Selv om det er merket av i feltet **Lokasjon obligatorisk**, tillater programmet at det opprettes behovslinjer uten en lokasjonskode, også kalt tom lokasjon.</span><span class="sxs-lookup"><span data-stu-id="689cd-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="689cd-128">Dette er et systemavvik fordi ulike oppsettsverdier er rettet mot lokasjoner (se ovenfor), og planleggingsmotoren vil derfor ikke opprette en planleggingslinje for en slik behovslinje.</span><span class="sxs-lookup"><span data-stu-id="689cd-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="689cd-129">Hvis det ikke er merket av for feltet **Lokasjon obligatorisk**, men noen av verdiene for oppsett av lokasjon finnes, blir dette også betraktet som et avvik, og planleggingssystemet vil reagere med å bruke "minimumsalternativet": Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (ordre forblir ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="689cd-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="689cd-130">Scenarier</span><span class="sxs-lookup"><span data-stu-id="689cd-130">Scenarios</span></span>
<span data-ttu-id="689cd-131">Følgende scenarier beskriver ulike behov på en tom lokasjon og hvordan planleggingssystemet løses til "minimumsalternativet".</span><span class="sxs-lookup"><span data-stu-id="689cd-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="689cd-132">Oppsett 1:</span><span class="sxs-lookup"><span data-stu-id="689cd-132">Setup 1:</span></span>
<span data-ttu-id="689cd-133">Lokasjon obligatorisk = Ja</span><span class="sxs-lookup"><span data-stu-id="689cd-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="689cd-134">LFE er definert for RØD</span><span class="sxs-lookup"><span data-stu-id="689cd-134">SKU is set up for RED</span></span>

<span data-ttu-id="689cd-135">Komponenter ved lokasjon = BLÅ</span><span class="sxs-lookup"><span data-stu-id="689cd-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="689cd-136">Eksempel 1.1: Behovet er i RØD lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="689cd-137">Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="689cd-138">Eksempel 1.2: Behovet er i BLÅ lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="689cd-139">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="689cd-140">Eksempel 1.3: Behovet er i GRØNN lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="689cd-141">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="689cd-142">Eksempel 1.4: Behovet er i TOM lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="689cd-143">Varen planlegges ikke fordi ingen lokasjon er definert på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="689cd-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="689cd-144">Oppsett 2:</span><span class="sxs-lookup"><span data-stu-id="689cd-144">Setup 2:</span></span>
<span data-ttu-id="689cd-145">Lokasjon obligatorisk = Ja</span><span class="sxs-lookup"><span data-stu-id="689cd-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="689cd-146">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="689cd-146">No SKU exists</span></span>

<span data-ttu-id="689cd-147">Komponenter ved lokasjon = BLÅ</span><span class="sxs-lookup"><span data-stu-id="689cd-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="689cd-148">Eksempel 2.1: Behovet er i RØD lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="689cd-149">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="689cd-150">Eksempel 2.2: Behovet er i BLÅ lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="689cd-151">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="689cd-152">Oppsett 3:</span><span class="sxs-lookup"><span data-stu-id="689cd-152">Setup 3:</span></span>
<span data-ttu-id="689cd-153">Lokasjon obligatorisk = Nei</span><span class="sxs-lookup"><span data-stu-id="689cd-153">Location Mandatory = No</span></span>

<span data-ttu-id="689cd-154">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="689cd-154">No SKU exists</span></span>

<span data-ttu-id="689cd-155">Komponenter ved lokasjon = BLÅ</span><span class="sxs-lookup"><span data-stu-id="689cd-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="689cd-156">Eksempel 3.1: Behovet er i RØD lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="689cd-157">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="689cd-158">Eksempel 3.2: Behovet er i BLÅ lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="689cd-159">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="689cd-160">Eksempel 3.3: Behovet er i TOM lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="689cd-161">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="689cd-162">Oppsett 4:</span><span class="sxs-lookup"><span data-stu-id="689cd-162">Setup 4:</span></span>
<span data-ttu-id="689cd-163">Lokasjon obligatorisk = Nei</span><span class="sxs-lookup"><span data-stu-id="689cd-163">Location Mandatory = No</span></span>

<span data-ttu-id="689cd-164">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="689cd-164">No SKU exists</span></span>

<span data-ttu-id="689cd-165">Komponenter ved lokasjon = TOM</span><span class="sxs-lookup"><span data-stu-id="689cd-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="689cd-166">Eksempel 4.1: Behovet er i BLÅ lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="689cd-167">Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.</span><span class="sxs-lookup"><span data-stu-id="689cd-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="689cd-168">Eksempel 4.2: Behovet er i TOM lokasjon</span><span class="sxs-lookup"><span data-stu-id="689cd-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="689cd-169">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="689cd-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="689cd-170">Som illustrert i det siste scenariet kan du bare få et riktig resultat for en behovslinje uten lokasjonskode ved å deaktivere alle oppsettsverdier som gjelder lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="689cd-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="689cd-171">Likeledes kan du bare få stabile planleggingsresultater for behov i lokasjoner ved å bruke LFEer.</span><span class="sxs-lookup"><span data-stu-id="689cd-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="689cd-172">Hvis selskap ofte planlegger for behov i lokasjoner, anbefales de på det sterkeste å bruke granulen Lagerføringsenheter.</span><span class="sxs-lookup"><span data-stu-id="689cd-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="689cd-173">Se også</span><span class="sxs-lookup"><span data-stu-id="689cd-173">See Also</span></span>  
<span data-ttu-id="689cd-174">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="689cd-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="689cd-175">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="689cd-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="689cd-176">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="689cd-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]