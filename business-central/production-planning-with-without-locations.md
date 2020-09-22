---
title: Planlegge med/uten lokasjoner | Microsoft-dokumentasjon
description: Det er viktig å forstå planlegging med eller uten lokasjonskoder på behovslinjer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d9afd30c3b81912797ad95871256207d135b673
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783985"
---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="b81eb-103">Se Planlegge med/uten lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="b81eb-103">Planning With or Without Locations</span></span>
<span data-ttu-id="b81eb-104">Når det gjelder planlegging med eller uten lokasjonskoder på behovslinjer, fungerer planleggingssystemet på ordinær måte når:</span><span class="sxs-lookup"><span data-stu-id="b81eb-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="b81eb-105">behovslinjene alltid inneholder lokasjonskoder og systemet fullt ut bruker lagerføringsenheter, inkludert det relevante lokasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="b81eb-106">behovslinjene aldri inneholder lokasjonskoder og systemet ikke bruker lagerføringsenheter eller lokasjonsoppsett (se siste scenario nedenfor).</span><span class="sxs-lookup"><span data-stu-id="b81eb-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="b81eb-107">Hvis imidlertid behovslinjene noen ganger har lokasjonskoder og andre ganger ikke, følger planleggingssystemet visse regler avhengig av oppsettet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="b81eb-108">Behov i lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-108">Demand at Location</span></span>  
<span data-ttu-id="b81eb-109">Når planleggingssystemet oppdager behov i en lokasjon (en linje med en lokasjonskode), fungerer det på ulike måter avhengig av 3 viktige oppsettsverdier.</span><span class="sxs-lookup"><span data-stu-id="b81eb-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="b81eb-110">Under en kjørsel kontrolleres de 3 oppsettsverdiene etter tur, og planleggingen utføres i tråd med dette:</span><span class="sxs-lookup"><span data-stu-id="b81eb-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="b81eb-111">Er det merket av i feltet **Lokasjon obligatorisk**?</span><span class="sxs-lookup"><span data-stu-id="b81eb-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="b81eb-112">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="b81eb-112">If yes, then:</span></span>  

2.  <span data-ttu-id="b81eb-113">Finnes det lagerføringsenhet for varen?</span><span class="sxs-lookup"><span data-stu-id="b81eb-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="b81eb-114">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="b81eb-114">If yes, then:</span></span>  

    <span data-ttu-id="b81eb-115">Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="b81eb-116">Hvis nei:</span><span class="sxs-lookup"><span data-stu-id="b81eb-116">If no, then:</span></span>  

3.  <span data-ttu-id="b81eb-117">Inneholder feltet **Komponenter ved lokasjon** den nødvendige lokasjonskoden?</span><span class="sxs-lookup"><span data-stu-id="b81eb-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="b81eb-118">Hvis ja:</span><span class="sxs-lookup"><span data-stu-id="b81eb-118">If yes, then:</span></span>  

    <span data-ttu-id="b81eb-119">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="b81eb-120">Hvis nei:</span><span class="sxs-lookup"><span data-stu-id="b81eb-120">If no, then:</span></span>  

    <span data-ttu-id="b81eb-121">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti*, Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="b81eb-122">(Varer som bruker gjenbestillingsprinsippet  *Ordre*, fortsetter med å bruke  *Ordre* samt de andre innstillingene.)</span><span class="sxs-lookup"><span data-stu-id="b81eb-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b81eb-123">Dette minimumsalternativet dekker bare eksakt behov.</span><span class="sxs-lookup"><span data-stu-id="b81eb-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="b81eb-124">Eventuelle planleggingsparametre som er definert, ignoreres.</span><span class="sxs-lookup"><span data-stu-id="b81eb-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="b81eb-125">Se variasjoner i scenariene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b81eb-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="b81eb-126">Behov i "tom lokasjon"</span><span class="sxs-lookup"><span data-stu-id="b81eb-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="b81eb-127">Selv om det er merket av i feltet **Lokasjon obligatorisk**, tillater systemet at det opprettes behovslinjer uten en lokasjonskode – også kalt *TOM* lokasjon.</span><span class="sxs-lookup"><span data-stu-id="b81eb-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="b81eb-128">Dette er et systemavvik fordi ulike oppsettsverdier er rettet mot lokasjoner (se ovenfor), og planleggingsmotoren vil derfor ikke opprette en planleggingslinje for en slik behovslinje.</span><span class="sxs-lookup"><span data-stu-id="b81eb-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="b81eb-129">Hvis det ikke er merket av i feltet **Lokasjon obligatorisk**, men noen av lokasjonsoppsettsverdiene finnes, regnes dette også som et avvik, og planleggingssystemet vil reagere med å benytte "minimumsalternativet":</span><span class="sxs-lookup"><span data-stu-id="b81eb-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="b81eb-130">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir *Ordre)*, Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="b81eb-131">Se variasjoner i oppsettsscenariene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b81eb-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="b81eb-132">Oppsett 1:</span><span class="sxs-lookup"><span data-stu-id="b81eb-132">Setup 1:</span></span>  

-   <span data-ttu-id="b81eb-133">Lokasjon obligatorisk = *Ja*</span><span class="sxs-lookup"><span data-stu-id="b81eb-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="b81eb-134">LFE defineres for  *RØD*</span><span class="sxs-lookup"><span data-stu-id="b81eb-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="b81eb-135">Komponenter ved lokasjon =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="b81eb-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="b81eb-136">Eksempel 1.1: Behovet er i  *RØD* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="b81eb-137">Varen planlegges i henhold til planleggingsparametrene på LFE-kortet (inkludert mulig overføring).</span><span class="sxs-lookup"><span data-stu-id="b81eb-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="b81eb-138">Eksempel 1.2: Behovet er i  *BLÅ* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="b81eb-139">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="b81eb-140">Eksempel 1.3: Behovet er i  *GRØNN* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="b81eb-141">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="b81eb-142">Eksempel 1.4: Behovet er i  *TOM* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="b81eb-143">Varen planlegges ikke fordi ingen lokasjon er definert på behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="b81eb-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="b81eb-144">Oppsett 2:</span><span class="sxs-lookup"><span data-stu-id="b81eb-144">Setup 2:</span></span>  

-   <span data-ttu-id="b81eb-145">Lokasjon obligatorisk = *Ja*</span><span class="sxs-lookup"><span data-stu-id="b81eb-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="b81eb-146">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="b81eb-146">No SKU exists</span></span>  
-   <span data-ttu-id="b81eb-147">Komponenter ved lokasjon =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="b81eb-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="b81eb-148">Eksempel 2.1: Behovet er i  *RØD* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="b81eb-149">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="b81eb-150">Eksempel 2.2: Behovet er i  *BLÅ* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="b81eb-151">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="b81eb-152">Oppsett 3:</span><span class="sxs-lookup"><span data-stu-id="b81eb-152">Setup 3:</span></span>  

-   <span data-ttu-id="b81eb-153">Lokasjon obligatorisk = *Nei*</span><span class="sxs-lookup"><span data-stu-id="b81eb-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="b81eb-154">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="b81eb-154">No SKU exists</span></span>  
-   <span data-ttu-id="b81eb-155">Komponenter ved lokasjon =  *BLÅ*</span><span class="sxs-lookup"><span data-stu-id="b81eb-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="b81eb-156">Eksempel 3.1: Behovet er i  *RØD* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="b81eb-157">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="b81eb-158">Eksempel 3.2: Behovet er i  *BLÅ* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="b81eb-159">Varen planlegges i henhold til planleggingsparametrene på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="b81eb-160">Eksempel 3.3: Behovet er i  *TOM* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="b81eb-161">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="b81eb-162">Oppsett 4:</span><span class="sxs-lookup"><span data-stu-id="b81eb-162">Setup 4:</span></span>  

-   <span data-ttu-id="b81eb-163">Lokasjon obligatorisk = *Nei*</span><span class="sxs-lookup"><span data-stu-id="b81eb-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="b81eb-164">LFE finnes ikke</span><span class="sxs-lookup"><span data-stu-id="b81eb-164">No SKU exists</span></span>  
-   <span data-ttu-id="b81eb-165">Komponenter ved lokasjon =  *TOM*</span><span class="sxs-lookup"><span data-stu-id="b81eb-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="b81eb-166">Eksempel 4.1: Behovet er i  *BLÅ* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="b81eb-167">Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.</span><span class="sxs-lookup"><span data-stu-id="b81eb-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="b81eb-168">Eksempel 4.2: Behovet er i  *TOM* lokasjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="b81eb-169">Varen planlegges i henhold til planleggingsparameterne på varekortet.</span><span class="sxs-lookup"><span data-stu-id="b81eb-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="b81eb-170">Som du ser i det siste scenariet, kan du bare få et riktig resultat for en behovslinje uten lokasjonskode ved å deaktivere alle oppsettsverdier som gjelder lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="b81eb-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="b81eb-171">På samme måte kan du bare få stabile planleggingsresultater for behov i lokasjoner ved å bruke lagerføringsenheter.</span><span class="sxs-lookup"><span data-stu-id="b81eb-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="b81eb-172">Hvis du ofte planlegger for behov i lokasjoner, anbefaler vi derfor på det sterkeste å bruke funksjonen Lagerføringsenheter.</span><span class="sxs-lookup"><span data-stu-id="b81eb-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b81eb-173">Se også</span><span class="sxs-lookup"><span data-stu-id="b81eb-173">See Also</span></span>
<span data-ttu-id="b81eb-174">[Planlegging](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="b81eb-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="b81eb-175">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="b81eb-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b81eb-176">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b81eb-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b81eb-177">Lager</span><span class="sxs-lookup"><span data-stu-id="b81eb-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b81eb-178">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="b81eb-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b81eb-179">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b81eb-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="b81eb-180">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="b81eb-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="b81eb-181">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b81eb-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
