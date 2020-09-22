---
title: Om planleggingsfunksjonalitet | Microsoft-dokumentasjon
description: Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: 541d3842977e7b139877d9a26fcc39b448ef9745
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786974"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="2b4f5-103">Om planleggingsfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="2b4f5-103">About Planning Functionality</span></span>

<span data-ttu-id="2b4f5-104">Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="2b4f5-105">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="2b4f5-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="2b4f5-106">Les verktøytips for å forstå funksjon for alle feltene i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="2b4f5-107">Behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="2b4f5-107">Demand and Supply</span></span>

<span data-ttu-id="2b4f5-108">Planlegging har to elementer: behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="2b4f5-109">Disse må holdes i balanse for å sikre at behovet dekkes i rett tid og på en kosteffektiv måte.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="2b4f5-110">Behov er den vanlige betegnelsen som brukes om alle typer bruttobehov, for eksempel en ordre, serviceordre, komponentbehov fra monterings- eller produksjonsordrer, utgående overføring, rammeordre eller prognose.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="2b4f5-111">I tillegg til disse tillater programmet andre tekniske typer behov, for eksempel negativ produksjon eller bestilling, negativ beholdning og bestillingsretur.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="2b4f5-112">Forsyning er ordet som brukes om alle typer etterfylling, for eksempel beholdning, en bestilling, monteringsordre, produksjonsordre eller inngående overføring.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="2b4f5-113">På tilsvarende vis kan det finnes en negativ ordre eller serviceordre, negativt komponentbehov eller ordreretur, og alt dette representerer også på en måte forsyning.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="2b4f5-114">Et annet mål med planleggingssystemet er å sikre at beholdningen ikke vokser unødvendig.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="2b4f5-115">Hvis behovet avtar, foreslår systemet at du utsetter, reduserer antallet i eller annullerer eksisterende etterfyllingsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="2b4f5-116">Planleggingsberegning</span><span class="sxs-lookup"><span data-stu-id="2b4f5-116">Planning Calculation</span></span>

<span data-ttu-id="2b4f5-117">Planleggingssystemet drives av forventet og faktisk kundebehov samt gjenbestillingsparametere for beholdning.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="2b4f5-118">Når du kjører planleggingsberegningen, foreslår programmet bestemte handlinger (handlingsmeldinger) som gjelder mulig etterfylling fra leverandører, overføringer mellom lagre eller produksjon.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="2b4f5-119">Hvis det allerede finnes etterfyllingsordrer, kan de foreslåtte handlingene være å øke eller påskynde ordrene for å dekke endringene i behovet.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="2b4f5-120">Grunnlaget for planleggingsrutinen er i beregningen av brutto til netto.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="2b4f5-121">Nettobehov driver planlagte ordrefrigivelser, som planlegges basert på ruteinformasjonen (produserte varer) eller leveringstiden for varekort (kjøpte varer).</span><span class="sxs-lookup"><span data-stu-id="2b4f5-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="2b4f5-122">Antall planlagte ordrefrigivelser er basert på planleggingsberegningen og påvirkes av parameterne som er angitt på de enkelte varekortene.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="2b4f5-123">Planlegge med manuelle overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="2b4f5-123">Planning with Manual Transfer Orders</span></span>

<span data-ttu-id="2b4f5-124">Som du ser i feltet **Etterfyllingssystem** på et LFE-kort, kan planleggingssystemet konfigureres slik at det opprettes overføringsordrer for å fordele forsyning og behov på tvers av lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="2b4f5-125">I tillegg til slike automatiske overføringsorder kan det av og til være behov for å foreta en generell flytting av lagerantall til en annen lokasjon, uansett eksisterende behov.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="2b4f5-126">Da kan du manuelt opprette en overføringsordre for antallet som skal flyttes.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="2b4f5-127">Du må angi Ingen som verdi for **Planleggingsfleksibilitet** på overføringslinjen(e) for å sikre at planleggingssystemet ikke prøver å manipulere denne manuelle overføringsordren.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="2b4f5-128">Hvis du derimot vil at planleggingssystemet skal justere overføringsordreantallene og datoene til eksisterende behov, må du angi standardverdien Ubegrenset i feltet **Planleggingsfleksibilitet**.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="2b4f5-129">Planleggingsparametere</span><span class="sxs-lookup"><span data-stu-id="2b4f5-129">Planning Parameters</span></span>

<span data-ttu-id="2b4f5-130">Planleggingsparameterne kontrollerer når, hvor mye og hvordan etterfylling skal skje, basert på de ulike innstillingene på varekortet (eller lagerføringsenhet - LFE) og produksjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="2b4f5-131">Følgende planleggingsparametre finnes på vare- eller LFE-kortet:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-131">The following planning parameters exist on the item or SKU card:</span></span>  

- <span data-ttu-id="2b4f5-132">Avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="2b4f5-132">Dampener Period</span></span>  
- <span data-ttu-id="2b4f5-133">Avdempingsantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-133">Dampener Quantity</span></span>  
- <span data-ttu-id="2b4f5-134">Gjenbestillingsprinsipp</span><span class="sxs-lookup"><span data-stu-id="2b4f5-134">Reordering Policy</span></span>  
- <span data-ttu-id="2b4f5-135">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="2b4f5-135">Reorder Point</span></span>
- <span data-ttu-id="2b4f5-136">Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="2b4f5-136">Maximum Inventory</span></span>  
- <span data-ttu-id="2b4f5-137">Overflytnivå</span><span class="sxs-lookup"><span data-stu-id="2b4f5-137">Overflow Level</span></span>  
- <span data-ttu-id="2b4f5-138">Tidsperiode</span><span class="sxs-lookup"><span data-stu-id="2b4f5-138">Time Bucket</span></span>  
- <span data-ttu-id="2b4f5-139">Akkumuleringsperiode for parti</span><span class="sxs-lookup"><span data-stu-id="2b4f5-139">Lot Accumulation Period</span></span>  
- <span data-ttu-id="2b4f5-140">Periode for ny planlegging</span><span class="sxs-lookup"><span data-stu-id="2b4f5-140">Rescheduling Period</span></span>  
- <span data-ttu-id="2b4f5-141">Gjenbestillingsantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-141">Reorder Quantity</span></span>  
- <span data-ttu-id="2b4f5-142">Sikkerhetsleveringstid</span><span class="sxs-lookup"><span data-stu-id="2b4f5-142">Safety Lead Time</span></span>  
- <span data-ttu-id="2b4f5-143">Sikkerhetslagerantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-143">Safety Stock Quantity</span></span>  
- <span data-ttu-id="2b4f5-144">Monteringsprinsipp</span><span class="sxs-lookup"><span data-stu-id="2b4f5-144">Assembly Policy</span></span>  
- <span data-ttu-id="2b4f5-145">Produksjonsprinsipp</span><span class="sxs-lookup"><span data-stu-id="2b4f5-145">Manufacturing Policy</span></span>  

<span data-ttu-id="2b4f5-146">Følgende ordremodifikatorer finnes på vare- eller LFE-kortet:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-146">The following order modifiers exist on the item or SKU card:</span></span>  

- <span data-ttu-id="2b4f5-147">Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-147">Minimum Order Quantity</span></span>  
- <span data-ttu-id="2b4f5-148">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-148">Maximum Order Quantity</span></span>  
- <span data-ttu-id="2b4f5-149">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="2b4f5-149">Order Multiple</span></span>  

<span data-ttu-id="2b4f5-150">Oppsettsfeltene for global planlegging på **Produksjonsoppsett**-siden omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

- <span data-ttu-id="2b4f5-151">Dynamisk lavnivåkode</span><span class="sxs-lookup"><span data-stu-id="2b4f5-151">Dynamic Low-Level Code</span></span>  
- <span data-ttu-id="2b4f5-152">Gjeldende behovsprognose</span><span class="sxs-lookup"><span data-stu-id="2b4f5-152">Current Demand Forecast</span></span>  
- <span data-ttu-id="2b4f5-153">Bruk prognose på lokasjoner</span><span class="sxs-lookup"><span data-stu-id="2b4f5-153">Use Forecast on Locations</span></span>  
- <span data-ttu-id="2b4f5-154">Standard sikkerhetstid</span><span class="sxs-lookup"><span data-stu-id="2b4f5-154">Default Safety Lead Time</span></span>  
- <span data-ttu-id="2b4f5-155">Tomt overflytnivå</span><span class="sxs-lookup"><span data-stu-id="2b4f5-155">Blank Overflow Level</span></span>  
- <span data-ttu-id="2b4f5-156">Kombinert MPS/MRP-beregning</span><span class="sxs-lookup"><span data-stu-id="2b4f5-156">Combined MPS/MRP Calculation</span></span>
- <span data-ttu-id="2b4f5-157">Komponenter ved lokasjon</span><span class="sxs-lookup"><span data-stu-id="2b4f5-157">Components at Location</span></span>  
- <span data-ttu-id="2b4f5-158">Standard avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="2b4f5-158">Default Dampener Period</span></span>  
- <span data-ttu-id="2b4f5-159">Standard avdempingsantall</span><span class="sxs-lookup"><span data-stu-id="2b4f5-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="2b4f5-160">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: planleggingsparametere](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="2b4f5-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="2b4f5-161">Andre viktige felt for planlegging</span><span class="sxs-lookup"><span data-stu-id="2b4f5-161">Other Important Planning Fields</span></span>

### <a name="planning-flexibility"></a><span data-ttu-id="2b4f5-162">Planleggingsfleksibilitet</span><span class="sxs-lookup"><span data-stu-id="2b4f5-162">Planning Flexibility</span></span>

<span data-ttu-id="2b4f5-163">I de fleste forsyningsordrer, for eksempel produksjonsordrer, kan du velge **Ubegrenset** eller **Ingen** i vinduet **Planleggingsfleksibilitet** på linjene.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="2b4f5-164">Dette angir om forsyningen som representeres av produksjonsordrelinjen, vurderes av planleggingssystemet ved beregning av handlingsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="2b4f5-165">Hvis feltet inneholder **Ubegrenset**, tar planleggingssystemet med linjen når handlingsmeldinger beregnes.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="2b4f5-166">Hvis feltet inneholder **Ingen**, er linjen fast og uforanderlig, og planleggingssystemet tar den ikke med når handlingsmeldinger beregnes.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="2b4f5-167">Advarsel</span><span class="sxs-lookup"><span data-stu-id="2b4f5-167">Warning</span></span>

<span data-ttu-id="2b4f5-168">Informasjonsfeltet **Advarsel** på siden **Planleggingsforslag** informerer deg om eventuelle planleggingslinjer som er opprettet for en uvanlig situasjon med en tekst som brukeren kan velge å få mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="2b4f5-169">Følgende typer advarsler finnes:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-169">The following warning types exist:</span></span>

- <span data-ttu-id="2b4f5-170">Kritisk</span><span class="sxs-lookup"><span data-stu-id="2b4f5-170">Emergency</span></span>
- <span data-ttu-id="2b4f5-171">Unntak</span><span class="sxs-lookup"><span data-stu-id="2b4f5-171">Exception</span></span>
- <span data-ttu-id="2b4f5-172">Viktig</span><span class="sxs-lookup"><span data-stu-id="2b4f5-172">Attention</span></span>
- <span data-ttu-id="2b4f5-173">Kritisk</span><span class="sxs-lookup"><span data-stu-id="2b4f5-173">Emergency</span></span>

<span data-ttu-id="2b4f5-174">Kritisk-advarselen vises i to situasjoner:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="2b4f5-175">Beholdningen er negativ på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="2b4f5-176">Det finnes tilbakedatert forsyning eller behov.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="2b4f5-177">Hvis beholdningen for en vare er negativ på den planlagte startdatoen, foreslår planleggingssystemet at det opprettes en kritisk ordre for det negative antallet, med ankomst på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-177">If an item's inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="2b4f5-178">Advarselsteksten angir startdatoen og antallet på den kritiske ordren.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="2b4f5-179">Dokumentlinjer med forfallsdato før den planlagte startdatoen konsolideres til én kritisk ordre for varen, med ankomst på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="2b4f5-180">Unntak</span><span class="sxs-lookup"><span data-stu-id="2b4f5-180">Exception</span></span>

<span data-ttu-id="2b4f5-181">Unntak-advarselen vises hvis den beregnede disponible beholdningen faller under sikkerhetslagerantallet.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="2b4f5-182">Planleggingssystemet foreslår at det opprettes en forsyningsordre for å oppfylle behovet på forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="2b4f5-183">Advarselsteksten angir varens sikkerhetslagerantall og datoen da antallet ble for lavt.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-183">The warning text states the item's safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="2b4f5-184">Et for lavt sikkerhetslagernivå anses for å være et unntak fordi det ikke skal forekomme hvis gjenbestillingspunktet er riktig angitt.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="2b4f5-185">Forsyning på planleggingslinjer med unntaksadvarsler endres vanligvis ikke i henhold til planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="2b4f5-186">I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="2b4f5-187">Du kan imidlertid angi planleggingskjøringen for å respektere visse planleggingsparametre for planleggingslinjer med bestemte advarsler.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="2b4f5-188">Hvis du vil ha mer informasjon, kan du se beskrivelsen for feltet **Respekter planleggingsparametre for unntaksadvarsler** i artikkelen [Kjøre full planlegging, MPS eller MRP](production-how-to-run-mps-and-mrp.md).</span><span class="sxs-lookup"><span data-stu-id="2b4f5-188">For more information, see the description for the **Respect Planning Parameters for Exception Warnings** field in the [Run Full Planning, MPS or MRP](production-how-to-run-mps-and-mrp.md) article.</span></span>

### <a name="attention"></a><span data-ttu-id="2b4f5-189">Viktig</span><span class="sxs-lookup"><span data-stu-id="2b4f5-189">Attention</span></span>

<span data-ttu-id="2b4f5-190">Tilsyn-advarselen vises i to situasjoner:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-190">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="2b4f5-191">Den planlagte startdatoen er tidligere enn arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-191">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="2b4f5-192">Planleggingslinjen foreslår at en frigitt bestilling eller produksjonsordre endres.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-192">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="2b4f5-193">På planleggingslinjer med advarsler er ikke feltet **Godta handlingsmelding** valgt, fordi planleggeren må undersøke disse linjene ytterligere før planen utføres.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-193">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="planning-worksheets-and-requisition-worksheets"></a><span data-ttu-id="2b4f5-194">Planleggingsforslag og bestillingsforslag</span><span class="sxs-lookup"><span data-stu-id="2b4f5-194">Planning worksheets and requisition worksheets</span></span>

<span data-ttu-id="2b4f5-195">Som beskrevet i [Planlegging](production-planning.md) kan du velge mellom to forslag for de fleste planleggingsaktivitetene, planleggingsforslaget og bestillingsforslaget.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-195">As described in [Planning](production-planning.md), you can choose between two worksheets for most planning activities, the planning worksheet and the requisition worksheet.</span></span> <span data-ttu-id="2b4f5-196">De fleste prosesser er beskrevet basert på planleggingsforslaget, men det finnes et par scenarier der bestillingsforslaget foretrekkes.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-196">Most processes are described based on the planning worksheet, but there are a couple of scenarios where the requisition worksheet is preferred.</span></span>

### <a name="requisition-worksheet"></a><span data-ttu-id="2b4f5-197">Bestillingsforslag</span><span class="sxs-lookup"><span data-stu-id="2b4f5-197">Requisition worksheet</span></span>

<span data-ttu-id="2b4f5-198">Siden **Bestillingsforslag** viser varer du vil bestille.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-198">The **Requisition Worksheet** page lists items that you want to order.</span></span> <span data-ttu-id="2b4f5-199">Du kan angi varer i forslaget på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="2b4f5-199">You can enter items in the worksheet in the following ways:</span></span>

- <span data-ttu-id="2b4f5-200">Angi varene manuelt i bestillingsforslaget, og fyll ut i de aktuelle feltene.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-200">Enter the items manually in the worksheet and fill in the relevant fields.</span></span>

- <span data-ttu-id="2b4f5-201">Bruk kjørselen **Beregn plan**.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-201">Use the **Calculate Plan** batch job.</span></span> <span data-ttu-id="2b4f5-202">Den beregner en etterfyllingsplan for varer og lagerføringsenheter som er satt opp med et etterfyllingssystem for **Kjøp** eller **Overføring**.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-202">This calculates a replenishment plan for items and stockkeeping units that have been set up with a replenishment system of **Purchase** or **Transfer**.</span></span> <span data-ttu-id="2b4f5-203">Når du bruker denne kjørselen, fyller programmet automatisk ut feltet **Handlingsmelding** med et forslag til handling for etterfylling av varen.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-203">When you use this batch job, the program automatically fills in the **Action Message** field with a suggestion for an action you can take to replenish the item.</span></span> <span data-ttu-id="2b4f5-204">Det kan for eksempel være å øke vareantallet i en eksisterende ordre, eller opprette en ny ordre.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-204">This could be increasing the item quantity on an existing order or creating a new order, for example.</span></span>

- <span data-ttu-id="2b4f5-205">Hvis du har brukt kjørselen **Beregn plan** på **Planleggingsforslag**-siden til å beregne en etterfyllingsplan, kan du bruke kjørselen **Utfør handlingsmelding** til å kopiere kjøps- og overføringsordreforslag fra planleggingsforslaget til bestillingsforslaget.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-205">If you have used the **Calculate Plan** batch job from the **Planning Worksheet** page to calculate a replenishment plan, you can use the **Carry Out Action Message** batch job to copy purchase and transfer order proposals from the planning worksheet to the requisition worksheet.</span></span> <span data-ttu-id="2b4f5-206">Dette er nyttig hvis forskjellige brukere har ansvaret for håndtering av produksjonsordrer og kjøps-/overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-206">This is practical if separate users are responsible for handling production orders and purchase/transfer orders.</span></span>

- <span data-ttu-id="2b4f5-207">Du kan bruke handlingen **Direkte levering** for å fylle ut bestillingsforslagslinjene.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-207">You can use the **Drop Shipment** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="2b4f5-208">Denne handlingen bruker kjørselen **Hent ordrer** til å finne ordrelinjene du vil angi for en direkte levering.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-208">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a drop shipment.</span></span>

- <span data-ttu-id="2b4f5-209">Du kan bruke handlingen **Spesialbestilling** for å fylle ut bestillingsforslagslinjene.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-209">You can use the **Special Order** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="2b4f5-210">Denne handlingen bruker kjørselen **Hent ordrer** til å finne ordrelinjene du vil angi for en spesialbestilling.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-210">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a special order.</span></span>

<span data-ttu-id="2b4f5-211">Bestillingsforslagslinjene inneholder detaljert informasjon om varene som må bestilles.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-211">Requisition worksheet lines contain detailed information about the items that need to be reordered.</span></span> <span data-ttu-id="2b4f5-212">Du kan redigere eller slette linjene for å endre etterfyllingsplanen, og du kan viderebehandle linjene med kjørselen **Utfør handlingsmelding**.</span><span class="sxs-lookup"><span data-stu-id="2b4f5-212">You can edit and delete the lines to adjust your replenishment plan, and you can further process the lines by using the **Carry Out Action Message** batch job.</span></span>

<span data-ttu-id="2b4f5-213">Hvis du vil ha detaljer om planlegging med lokasjoner og overføringer, se [Planlegge med/uten lokasjoner](production-planning-with-without-locations.md).</span><span class="sxs-lookup"><span data-stu-id="2b4f5-213">For details about planning with locations and transfers, see [Planning With or Without Locations](production-planning-with-without-locations.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b4f5-214">Se også</span><span class="sxs-lookup"><span data-stu-id="2b4f5-214">See Also</span></span>

[<span data-ttu-id="2b4f5-215">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="2b4f5-215">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
[<span data-ttu-id="2b4f5-216">Planlegging</span><span class="sxs-lookup"><span data-stu-id="2b4f5-216">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="2b4f5-217">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="2b4f5-217">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="2b4f5-218">Produksjon</span><span class="sxs-lookup"><span data-stu-id="2b4f5-218">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="2b4f5-219">Lager</span><span class="sxs-lookup"><span data-stu-id="2b4f5-219">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2b4f5-220">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2b4f5-220">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="2b4f5-221">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="2b4f5-221">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="2b4f5-222">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2b4f5-222">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
