---
title: Om planleggingsfunksjonalitet | Microsoft-dokumentasjon
description: "Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0910760881decc98ba1bfa6e8753566316386b2c
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="about-planning-functionality"></a><span data-ttu-id="5a2b3-103">Om planleggingsfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="5a2b3-103">About Planning Functionality</span></span>
<span data-ttu-id="5a2b3-104">Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="5a2b3-105">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="5a2b3-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="5a2b3-106">Les verktøytips for å forstå funksjon for alle feltene i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="5a2b3-107">Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="5a2b3-107">Demand and Supply</span></span>  
<span data-ttu-id="5a2b3-108">Planlegging har to elementer: behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="5a2b3-109">Disse må holdes i balanse for å sikre at behovet dekkes i rett tid og på en kosteffektiv måte.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="5a2b3-110">Behov er den vanlige betegnelsen som brukes om alle typer bruttobehov, for eksempel en ordre, serviceordre, komponentbehov fra monterings- eller produksjonsordrer, utgående overføring, rammeordre eller prognose.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="5a2b3-111">I tillegg til disse tillater programmet andre tekniske typer behov, for eksempel negativ produksjon eller bestilling, negativ beholdning og bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-111">In addition to these, the program allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="5a2b3-112">Forsyning er ordet som brukes om alle typer etterfylling, for eksempel beholdning, en bestilling, monteringsordre, produksjonsordre eller inngående overføring.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="5a2b3-113">På tilsvarende vis kan det finnes en negativ ordre eller serviceordre, negativt komponentbehov eller ordreretur, og alt dette representerer også på en måte forsyning.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="5a2b3-114">Et annet mål med planleggingssystemet er å sikre at beholdningen ikke vokser unødvendig.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="5a2b3-115">Hvis behovet avtar, foreslår systemet at du utsetter, reduserer antallet i eller annullerer eksisterende etterfyllingsordrer.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="5a2b3-116">Planleggingsberegning</span><span class="sxs-lookup"><span data-stu-id="5a2b3-116">Planning Calculation</span></span>  
<span data-ttu-id="5a2b3-117">Planleggingssystemet drives av forventet og faktisk kundebehov samt gjenbestillingsparametere for beholdning.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="5a2b3-118">Når du kjører planleggingsberegningen, foreslår programmet bestemte handlinger (handlingsmeldinger) som gjelder mulig etterfylling fra leverandører, overføringer mellom lagre eller produksjon.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-118">Running the planning calculation will result in the program suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="5a2b3-119">Hvis det allerede finnes etterfyllingsordrer, kan de foreslåtte handlingene være å øke eller påskynde ordrene for å dekke endringene i behovet.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="5a2b3-120">Grunnlaget for planleggingsrutinen er i beregningen av brutto til netto.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="5a2b3-121">Nettobehov driver planlagte ordrefrigivelser, som planlegges basert på ruteinformasjonen (produserte varer) eller leveringstiden for varekort (kjøpte varer).</span><span class="sxs-lookup"><span data-stu-id="5a2b3-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="5a2b3-122">Antall planlagte ordrefrigivelser er basert på planleggingsberegningen og påvirkes av parameterne som er angitt på de enkelte varekortene.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="5a2b3-123">Planlegge med manuelle overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="5a2b3-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="5a2b3-124">Som du ser i feltet **Etterfyllingssystem** på et LFE-kort, kan planleggingssystemet konfigureres slik at det opprettes overføringsordrer for å fordele forsyning og behov på tvers av lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="5a2b3-125">I tillegg til slike automatiske overføringsorder kan det av og til være behov for å foreta en generell flytting av lagerantall til en annen lokasjon, uansett eksisterende behov.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="5a2b3-126">Da kan du manuelt opprette en overføringsordre for antallet som skal flyttes.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="5a2b3-127">Du må angi Ingen som verdi for **Planleggingsfleksibilitet** på overføringslinjen(e) for å sikre at planleggingssystemet ikke prøver å manipulere denne manuelle overføringsordren.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="5a2b3-128">Hvis du derimot vil at planleggingssystemet skal justere overføringsordreantallene og datoene til eksisterende behov, må du angi standardverdien Ubegrenset i feltet **Planleggingsfleksibilitet**.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="5a2b3-129">Planleggingsparametere</span><span class="sxs-lookup"><span data-stu-id="5a2b3-129">Planning Parameters</span></span>  
<span data-ttu-id="5a2b3-130">Planleggingsparameterne kontrollerer når, hvor mye og hvordan etterfylling skal skje, basert på de ulike innstillingene på varekortet (eller lagerføringsenhet - LFE) og produksjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="5a2b3-131">Følgende planleggingsparametre finnes på vare- eller LFE-kortet:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="5a2b3-132">Avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="5a2b3-132">Dampener Period</span></span>  
-   <span data-ttu-id="5a2b3-133">Avdempingsantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="5a2b3-134">Gjenbestillingsprinsipp</span><span class="sxs-lookup"><span data-stu-id="5a2b3-134">Reordering Policy</span></span>  
-   <span data-ttu-id="5a2b3-135">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="5a2b3-135">Reorder Point</span></span>
-   <span data-ttu-id="5a2b3-136">Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="5a2b3-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="5a2b3-137">Overflytnivå</span><span class="sxs-lookup"><span data-stu-id="5a2b3-137">Overflow Level</span></span>  
-   <span data-ttu-id="5a2b3-138">Tidsperiode</span><span class="sxs-lookup"><span data-stu-id="5a2b3-138">Time Bucket</span></span>  
-   <span data-ttu-id="5a2b3-139">Akkumuleringsperiode for parti</span><span class="sxs-lookup"><span data-stu-id="5a2b3-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="5a2b3-140">Periode for ny planlegging</span><span class="sxs-lookup"><span data-stu-id="5a2b3-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="5a2b3-141">Gjenbestillingsantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="5a2b3-142">Sikkerhetsleveringstid</span><span class="sxs-lookup"><span data-stu-id="5a2b3-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="5a2b3-143">Sikkerhetslagerantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="5a2b3-144">Monteringsprinsipp</span><span class="sxs-lookup"><span data-stu-id="5a2b3-144">Assembly Policy</span></span>  
-   <span data-ttu-id="5a2b3-145">Produksjonsprinsipp</span><span class="sxs-lookup"><span data-stu-id="5a2b3-145">Manufacturing Policy</span></span>  

<span data-ttu-id="5a2b3-146">Følgende ordremodifikatorer finnes på vare- eller LFE-kortet:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="5a2b3-147">Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="5a2b3-148">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="5a2b3-149">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="5a2b3-149">Order Multiple</span></span>  

<span data-ttu-id="5a2b3-150">Oppsettsfeltene for global planlegging i **Produksjonsoppsett**-vinduet omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-150">Global planning setup fields on the **Manufacturing Setup** window include:</span></span>  

-   <span data-ttu-id="5a2b3-151">Dynamisk lavnivåkode]</span><span class="sxs-lookup"><span data-stu-id="5a2b3-151">Dynamic Low-Level Code]</span></span>  
-   <span data-ttu-id="5a2b3-152">Gjeldende produksjonsprognose</span><span class="sxs-lookup"><span data-stu-id="5a2b3-152">Current Production Forecast</span></span>  
-   <span data-ttu-id="5a2b3-153">Bruk prognose på lokasjoner</span><span class="sxs-lookup"><span data-stu-id="5a2b3-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="5a2b3-154">Standard sikkerhetstid</span><span class="sxs-lookup"><span data-stu-id="5a2b3-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="5a2b3-155">Tomt overflytnivå</span><span class="sxs-lookup"><span data-stu-id="5a2b3-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="5a2b3-156">Kombinert MPS/MRP-beregning</span><span class="sxs-lookup"><span data-stu-id="5a2b3-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="5a2b3-157">Komponenter ved lokasjon</span><span class="sxs-lookup"><span data-stu-id="5a2b3-157">Components at Location</span></span>  
-   <span data-ttu-id="5a2b3-158">Standard avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="5a2b3-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="5a2b3-159">Standard avdempingsantall</span><span class="sxs-lookup"><span data-stu-id="5a2b3-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="5a2b3-160">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: planleggingsparametere](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="5a2b3-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="5a2b3-161">Andre viktige felt for planlegging</span><span class="sxs-lookup"><span data-stu-id="5a2b3-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="5a2b3-162">Planleggingsfleksibilitet</span><span class="sxs-lookup"><span data-stu-id="5a2b3-162">Planning Flexibility</span></span>
<span data-ttu-id="5a2b3-163">I de fleste forsyningsordrer, for eksempel produksjonsordrer, kan du velge **Ubegrenset** eller **Ingen** i vinduet **Planleggingsfleksibilitet** på linjene.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="5a2b3-164">Dette angir om forsyningen som representeres av produksjonsordrelinjen, vurderes av planleggingssystemet ved beregning av handlingsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="5a2b3-165">Hvis feltet inneholder **Ubegrenset**, tar planleggingssystemet med linjen når handlingsmeldinger beregnes.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="5a2b3-166">Hvis feltet inneholder **Ingen**, er linjen fast og uforanderlig, og planleggingssystemet tar den ikke med når handlingsmeldinger beregnes.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="5a2b3-167">Advarsel</span><span class="sxs-lookup"><span data-stu-id="5a2b3-167">Warning</span></span>
<span data-ttu-id="5a2b3-168">Informasjonsfeltet **Advarsel**i vinduet **Planleggingsforslag** informerer deg om eventuelle planleggingslinjer som er opprettet for en uvanlig situasjon med en tekst som brukeren kan velge å få mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-168">The **Warning** information field in the **Planning Worksheet** window informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="5a2b3-169">Følgende typer advarsler finnes:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-169">The following warning types exist:</span></span>

- <span data-ttu-id="5a2b3-170">Kritisk</span><span class="sxs-lookup"><span data-stu-id="5a2b3-170">Emergency</span></span>
- <span data-ttu-id="5a2b3-171">Unntak</span><span class="sxs-lookup"><span data-stu-id="5a2b3-171">Exception</span></span>
- <span data-ttu-id="5a2b3-172">Viktig</span><span class="sxs-lookup"><span data-stu-id="5a2b3-172">Attention</span></span>
- <span data-ttu-id="5a2b3-173">Kritisk</span><span class="sxs-lookup"><span data-stu-id="5a2b3-173">Emergency</span></span>

<span data-ttu-id="5a2b3-174">Kritisk-advarselen vises i to situasjoner:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="5a2b3-175">Beholdningen er negativ på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="5a2b3-176">Det finnes tilbakedatert forsyning eller behov.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="5a2b3-177">Hvis beholdningen for en vare er negativ på den planlagte startdatoen, foreslår planleggingssystemet at det opprettes en kritisk ordre for det negative antallet, med ankomst på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="5a2b3-178">Advarselsteksten angir startdatoen og antallet på den kritiske ordren.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="5a2b3-179">Dokumentlinjer med forfallsdato før den planlagte startdatoen konsolideres til én kritisk ordre for varen, med ankomst på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="5a2b3-180">Unntak</span><span class="sxs-lookup"><span data-stu-id="5a2b3-180">Exception</span></span>
<span data-ttu-id="5a2b3-181">Unntak-advarselen vises hvis den beregnede disponible beholdningen faller under sikkerhetslagerantallet.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="5a2b3-182">Planleggingssystemet foreslår at det opprettes en forsyningsordre for å oppfylle behovet på forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="5a2b3-183">Advarselsteksten angir varens sikkerhetslagerantall og datoen da antallet ble for lavt.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="5a2b3-184">Et for lavt sikkerhetslagernivå anses for å være et unntak fordi det ikke skal forekomme hvis gjenbestillingspunktet er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="5a2b3-185">Forsyning på planleggingslinjer med unntaksadvarsler endres vanligvis ikke i henhold til planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="5a2b3-186">I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="5a2b3-187">Du kan imidlertid angi planleggingskjøringen for å respektere visse planleggingsparametre for planleggingslinjer med bestemte advarsler.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="5a2b3-188">Hvis du vil ha mer informasjon, kan du se "Respekter planleggingsparametre for unntaksadvarsler" i Beregn plan - planl.forslag.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="5a2b3-189">Wksh.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="5a2b3-190">Viktig</span><span class="sxs-lookup"><span data-stu-id="5a2b3-190">Attention</span></span>
<span data-ttu-id="5a2b3-191">Tilsyn-advarselen vises i to situasjoner:</span><span class="sxs-lookup"><span data-stu-id="5a2b3-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="5a2b3-192">Den planlagte startdatoen er tidligere enn arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="5a2b3-193">Planleggingslinjen foreslår at en frigitt bestilling eller produksjonsordre endres.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="5a2b3-194">På planleggingslinjer med advarsler er ikke feltet **Godta handlingsmelding** valgt, fordi planleggeren må undersøke disse linjene ytterligere før planen utføres.</span><span class="sxs-lookup"><span data-stu-id="5a2b3-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a2b3-195">Se også</span><span class="sxs-lookup"><span data-stu-id="5a2b3-195">See Also</span></span>  
[<span data-ttu-id="5a2b3-196">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="5a2b3-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="5a2b3-197">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="5a2b3-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="5a2b3-198">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="5a2b3-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5a2b3-199">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5a2b3-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5a2b3-200">Lager</span><span class="sxs-lookup"><span data-stu-id="5a2b3-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5a2b3-201">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="5a2b3-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="5a2b3-202">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="5a2b3-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="5a2b3-203">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a2b3-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

