---
title: Designdetaljer – Inngående lagerflyt | Microsoft-dokumentasjon
description: Den inngående flyten på et lager begynner når varene ankommer på lageret på selskapslokasjonen, enten de mottas fra eksterne kilder eller fra en annen selskapslokasjon. En ansatt registrerer varene, vanligvis ved å skanne en strekkode. Fra mottaksområdene utførers lageraktiviteter på ulike kompleksitetsnivåer for å hente varer til lagringsområdet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9e7990c907360a1ba7fb445e3eeefeb026315f9e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802600"
---
# <a name="design-details-inbound-warehouse-flow"></a><span data-ttu-id="1d547-105">Designdetaljer: Inngående lagerflyt</span><span class="sxs-lookup"><span data-stu-id="1d547-105">Design Details: Inbound Warehouse Flow</span></span>
<span data-ttu-id="1d547-106">Den inngående flyten på et lager begynner når varene ankommer på lageret på selskapslokasjonen, enten de mottas fra eksterne kilder eller fra en annen selskapslokasjon.</span><span class="sxs-lookup"><span data-stu-id="1d547-106">The inbound flow in a warehouse begins when items arrive in the warehouse of the company location, either received from external sources or from another company location.</span></span> <span data-ttu-id="1d547-107">En ansatt registrerer varene, vanligvis ved å skanne en strekkode.</span><span class="sxs-lookup"><span data-stu-id="1d547-107">An employee registers the items, typically by scanning a bar code.</span></span> <span data-ttu-id="1d547-108">Fra mottaksområdene utførers lageraktiviteter på ulike kompleksitetsnivåer for å hente varer til lagringsområdet.</span><span class="sxs-lookup"><span data-stu-id="1d547-108">From the receiving dock, warehouse activities are performed at different complexity levels to bring the items into the storage area.</span></span>  

 <span data-ttu-id="1d547-109">Hvert element identifiseres og samsvares med en tilsvarende inngående kildedokument.</span><span class="sxs-lookup"><span data-stu-id="1d547-109">Each item is identified and matched to a corresponding inbound source document.</span></span> <span data-ttu-id="1d547-110">Følgende inngående kildedokumenter finnes:</span><span class="sxs-lookup"><span data-stu-id="1d547-110">The following inbound source documents exist:</span></span>  

- <span data-ttu-id="1d547-111">Bestilling</span><span class="sxs-lookup"><span data-stu-id="1d547-111">Purchase order</span></span>  
- <span data-ttu-id="1d547-112">Inngående overføringsordre</span><span class="sxs-lookup"><span data-stu-id="1d547-112">Inbound transfer order</span></span>  
- <span data-ttu-id="1d547-113">Ordreretur</span><span class="sxs-lookup"><span data-stu-id="1d547-113">Sales return order</span></span>  

<span data-ttu-id="1d547-114">I tillegg finnes følgende interne kildedokumenter som fungerer som innkommende kilder:</span><span class="sxs-lookup"><span data-stu-id="1d547-114">In addition, the following internal source documents exist that function like inbound sources:</span></span>  

- <span data-ttu-id="1d547-115">Produksjonsordre med avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="1d547-115">Production order with output posting</span></span>  
- <span data-ttu-id="1d547-116">Monteringsordre med avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="1d547-116">Assembly order with output posting</span></span>  

<span data-ttu-id="1d547-117">De to siste representerer inngående flyter til lageret fra interne operasjonsområder.</span><span class="sxs-lookup"><span data-stu-id="1d547-117">The last two represent inbound flows to the warehouse from internal operation areas.</span></span> <span data-ttu-id="1d547-118">Hvis du vil ha mer informasjon om lagerhåndtering for interne innkommende og utgående prosesser, kan du se [Designdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md).</span><span class="sxs-lookup"><span data-stu-id="1d547-118">For more information about warehouse handling for internal inbound and outbound processes, see [Design Details: Internal Warehouse Flows](design-details-internal-warehouse-flows.md).</span></span>  

<span data-ttu-id="1d547-119">Prosesser og dokumenter for brukergrensesnitt i inngående lagerflyter er forskjellige for grunnleggende og avanserte lagerkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="1d547-119">Processes and UI documents in inbound warehouse flows are different for basic and advanced warehouse configurations.</span></span> <span data-ttu-id="1d547-120">Hovedforskjellen er at aktiviteter utføres ordre for ordre i grunnleggende lagerkonfigurasjoner, og de konsolideres for flere ordrer i avanserte lagerkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="1d547-120">The main difference is that activities are performed order-by-order in basic warehouse configurations, and they are consolidated for multiple orders in advanced warehouse configurations.</span></span> <span data-ttu-id="1d547-121">Hvis du vil ha mer informasjon om ulike kompleksitetsnivåer for lageret, kan du se [Designdetaljer: Lageroversikt](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="1d547-121">For more information about different warehouse complexity levels, see [Design Details: Warehouse Overview](design-details-warehouse-setup.md).</span></span>  

<span data-ttu-id="1d547-122">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner, avhengig av kompleksitetsnivået til lageret.</span><span class="sxs-lookup"><span data-stu-id="1d547-122">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes of receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="1d547-123">Metode</span><span class="sxs-lookup"><span data-stu-id="1d547-123">Method</span></span>|<span data-ttu-id="1d547-124">Inngående prosess</span><span class="sxs-lookup"><span data-stu-id="1d547-124">Inbound Process</span></span>|<span data-ttu-id="1d547-125">Hyller</span><span class="sxs-lookup"><span data-stu-id="1d547-125">Bins</span></span>|<span data-ttu-id="1d547-126">Mottak</span><span class="sxs-lookup"><span data-stu-id="1d547-126">Receipts</span></span>|<span data-ttu-id="1d547-127">Plassering</span><span class="sxs-lookup"><span data-stu-id="1d547-127">Put-aways</span></span>|<span data-ttu-id="1d547-128">Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="1d547-128">Complexity Level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="1d547-129">A</span><span class="sxs-lookup"><span data-stu-id="1d547-129">A</span></span>|<span data-ttu-id="1d547-130">Bokføre mottak og plassering fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="1d547-130">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="1d547-131">X</span><span class="sxs-lookup"><span data-stu-id="1d547-131">X</span></span>|||<span data-ttu-id="1d547-132">2</span><span class="sxs-lookup"><span data-stu-id="1d547-132">2</span></span>|  
|<span data-ttu-id="1d547-133">B</span><span class="sxs-lookup"><span data-stu-id="1d547-133">B</span></span>|<span data-ttu-id="1d547-134">Bokføre mottak og plassering fra et lagerplasseringsdokument</span><span class="sxs-lookup"><span data-stu-id="1d547-134">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="1d547-135">X</span><span class="sxs-lookup"><span data-stu-id="1d547-135">X</span></span>|<span data-ttu-id="1d547-136">3</span><span class="sxs-lookup"><span data-stu-id="1d547-136">3</span></span>|  
|<span data-ttu-id="1d547-137">L</span><span class="sxs-lookup"><span data-stu-id="1d547-137">C</span></span>|<span data-ttu-id="1d547-138">Bokføre mottak og plassering fra et lagermottaksdokument</span><span class="sxs-lookup"><span data-stu-id="1d547-138">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="1d547-139">X</span><span class="sxs-lookup"><span data-stu-id="1d547-139">X</span></span>||<span data-ttu-id="1d547-140">4/5/6</span><span class="sxs-lookup"><span data-stu-id="1d547-140">4/5/6</span></span>|  
|<span data-ttu-id="1d547-141">D</span><span class="sxs-lookup"><span data-stu-id="1d547-141">D</span></span>|<span data-ttu-id="1d547-142">Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument</span><span class="sxs-lookup"><span data-stu-id="1d547-142">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="1d547-143">X</span><span class="sxs-lookup"><span data-stu-id="1d547-143">X</span></span>|<span data-ttu-id="1d547-144">X</span><span class="sxs-lookup"><span data-stu-id="1d547-144">X</span></span>|<span data-ttu-id="1d547-145">4/5/6</span><span class="sxs-lookup"><span data-stu-id="1d547-145">4/5/6</span></span>|  

<span data-ttu-id="1d547-146">Hvilken metode som er aktuell å velge, avhenger av selskapets vanlige praksis og organisasjonens kompleksitetsnivå.</span><span class="sxs-lookup"><span data-stu-id="1d547-146">Selecting an approach depends on the company's accepted practices and the level of their organizational complexity.</span></span> <span data-ttu-id="1d547-147">I et ordre for ordre-lagermiljø, der de fleste ansatte på lageret arbeider direkte med ordredokumenter, kan et selskap for eksempel bruke metode A. Et ordre for ordre-lager som har en mer kompleks plasseringsprosess eller der det ikke er egne lageransatte til å utføre lageraktiviteter, kan skille plasseringsfunksjonene fra ordredokumentet (metode B). Selskaper som må planlegge behandling av flere ordrer kan i tillegg dra nytte av å bruke bekreftelse lagermottaks (metode C og D).</span><span class="sxs-lookup"><span data-stu-id="1d547-147">In an order-by-order warehouse environment, where most of the warehouse staff works directly with order documents, a company might decide to use method A. An order-by-order warehouse that has a more complex put-away process, or where there are dedicated warehouse staff to perform warehousing functions, might decide to separate their put-away functions from the order document, method B. Additionally, companies that need to plan the handling of multiple orders may find it helpful to use warehouse receipt documents, methods C and D.</span></span>  

<span data-ttu-id="1d547-148">I metode A, B og C kombineres mottaks- og plasseringshandlingen i ett trinn når tilsvarende dokumenter bokføres som mottatt.</span><span class="sxs-lookup"><span data-stu-id="1d547-148">In methods A, B, and C, the actions of receiving and putting away are combined in one step when posting the corresponding documents as received.</span></span> <span data-ttu-id="1d547-149">I metode D blir mottaket bokført først for å gjenkjenne lagerøkningen og at varer er tilgjengelige for salg.</span><span class="sxs-lookup"><span data-stu-id="1d547-149">In method D, the receipt is posted first to recognize the increase of inventory and that items are available for sale.</span></span> <span data-ttu-id="1d547-150">Lagermedarbeideren registrerer deretter plasseringen for å gjøre varene tilgjengelige for plukking.</span><span class="sxs-lookup"><span data-stu-id="1d547-150">The warehouse worker then registers the put-away to make items available to pick.</span></span>  

## <a name="basic-warehouse-configurations"></a><span data-ttu-id="1d547-151">Enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="1d547-151">Basic Warehouse Configurations</span></span>  
<span data-ttu-id="1d547-152">Diagrammet nedenfor illustrerer inngående lagerflyter etter dokumenttype i grunnleggende lagerkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="1d547-152">The following diagram illustrates the inbound warehouse flows by document type in basic warehouse configurations.</span></span> <span data-ttu-id="1d547-153">Tallene i diagrammet svarer til trinnene nedenfor diagrammet.</span><span class="sxs-lookup"><span data-stu-id="1d547-153">The numbers in the diagram correspond with the steps in the sections following the diagram.</span></span>  

<span data-ttu-id="1d547-154">![Inngående flyt i grunnleggende lageroppsett](media/design_details_warehouse_management_inbound_basic_flow.png "Inngående flyt i grunnleggende lageroppsett")</span><span class="sxs-lookup"><span data-stu-id="1d547-154">![Inbound flow in basic warehouse configurations](media/design_details_warehouse_management_inbound_basic_flow.png "Inbound flow in basic warehouse configurations")</span></span>  

### <a name="1-release-source-document--create-inventory-put-away"></a><span data-ttu-id="1d547-155">1: Frigi kildedokument / opprett lagerplassering</span><span class="sxs-lookup"><span data-stu-id="1d547-155">1: Release Source Document / Create Inventory Put-Away</span></span>  
<span data-ttu-id="1d547-156">Når varer mottas på lageret, frigir brukeren som er ansvarlig for mottak, kildedokumentet, for eksempel en bestilling eller inngående overføringsordre, for å signalisere til lagermedarbeidere at de mottatte varene kan plasseres på lager.</span><span class="sxs-lookup"><span data-stu-id="1d547-156">When items are received in the warehouse, the user who is responsible for receiving releases the source document, such as a purchase order or an inbound transfer order, to signal to warehouse workers that the received items can be put away in inventory.</span></span> <span data-ttu-id="1d547-157">Brukeren kan også opprette lagerplasseringsdokumenter for enkelte ordrelinjene med en push-metode, basert på angitte hyller og antall som skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="1d547-157">Alternatively, the user creates inventory put-away documents for individual order lines, in a push fashion, based on specified bins and quantities to handle.</span></span>  

### <a name="2-create-inbound-request"></a><span data-ttu-id="1d547-158">2: Opprett inngående forespørsel</span><span class="sxs-lookup"><span data-stu-id="1d547-158">2: Create Inbound Request</span></span>  
<span data-ttu-id="1d547-159">Når det inngående kildedokumentet frigis, opprettes en inngående lagerforespørsel automatisk.</span><span class="sxs-lookup"><span data-stu-id="1d547-159">When the inbound source document is released, an inbound warehouse request is created automatically.</span></span> <span data-ttu-id="1d547-160">Den inneholder referanser til kildedokumenttype og /nummer, og er ikke synlige for brukeren.</span><span class="sxs-lookup"><span data-stu-id="1d547-160">It contains references to the source document type and number and is not visible to the user.</span></span>  

### <a name="3-create-inventory-put-away"></a><span data-ttu-id="1d547-161">3: Opprett lagerplassering</span><span class="sxs-lookup"><span data-stu-id="1d547-161">3: Create Inventory Put-Away</span></span>  
<span data-ttu-id="1d547-162">På siden **Lagerplassering** henter brukeren som er ansvarlig, de ventende kildedokumentlinjene basert på inngående lagerforespørsler.</span><span class="sxs-lookup"><span data-stu-id="1d547-162">On the **Inventory Put-away** page, the warehouse worker retrieves, in a pull fashion, the pending source document lines based on inbound warehouse requests.</span></span> <span data-ttu-id="1d547-163">Det kan også hende at lagerplasseringslinjene allerede er opprettet med en push-metode, av brukeren som er ansvarlig for kildedokumentet.</span><span class="sxs-lookup"><span data-stu-id="1d547-163">Alternatively, the inventory put-away lines are already created, in a push fashion, by the user who is responsible for the source document.</span></span>  

### <a name="4-post-inventory-put-away"></a><span data-ttu-id="1d547-164">4: Bokfør lagerplassering</span><span class="sxs-lookup"><span data-stu-id="1d547-164">4: Post Inventory Put-Away</span></span>  
<span data-ttu-id="1d547-165">På hver linje for varer som er plassert, helt eller delvis, fyller lagermedarbeideren ut feltet **Antall** og bokfører deretter lagerplasseringen.</span><span class="sxs-lookup"><span data-stu-id="1d547-165">On each line for items that have been put away, partially or fully, the warehouse worker fills in the **Quantity** field, and then posts the inventory put-away.</span></span> <span data-ttu-id="1d547-166">Kildedokumenter som er knyttet til lagerplasseringen, bokføres som mottatt.</span><span class="sxs-lookup"><span data-stu-id="1d547-166">Source documents that are related to the inventory put-away are posted as received.</span></span>  

<span data-ttu-id="1d547-167">Det blir opprettet positive vareposter og lagerposter, og plasseringsforespørselen slettes hvis ferdigbehandlet.</span><span class="sxs-lookup"><span data-stu-id="1d547-167">Positive item ledger entries are created, warehouse entries are created, and the put-away request is deleted, if fully handled.</span></span> <span data-ttu-id="1d547-168">Eksempel: Feltet **Mottatt (antall)** i den inngående kildedokumentlinjen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="1d547-168">For example, the **Quantity Received** field on the inbound source document line is updated.</span></span> <span data-ttu-id="1d547-169">Det opprettes et postert mottaksdokument som for eksempel gjenspeiler bestillingen og de mottatte varene.</span><span class="sxs-lookup"><span data-stu-id="1d547-169">A posted receipt document is created that reflects the purchase order, for example, and the received items.</span></span>  

## <a name="advanced-warehouse-configurations"></a><span data-ttu-id="1d547-170">Avanserte lageroppsett</span><span class="sxs-lookup"><span data-stu-id="1d547-170">Advanced warehouse configurations</span></span>  
<span data-ttu-id="1d547-171">Diagrammet nedenfor illustrerer inngående lagerflyter etter dokumenttype i avanserte lagerkonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="1d547-171">The following diagram illustrates the inbound warehouse flow by document type in advanced warehouse configurations.</span></span> <span data-ttu-id="1d547-172">Tallene i diagrammet svarer til trinnene nedenfor diagrammet.</span><span class="sxs-lookup"><span data-stu-id="1d547-172">The numbers in the diagram correspond with the steps in the sections following the diagram.</span></span>  

<span data-ttu-id="1d547-173">![Inngående flyt i avanserte lageroppsett](media/design_details_warehouse_management_inbound_advanced_flow.png "Inngående flyt i avanserte lageroppsett")</span><span class="sxs-lookup"><span data-stu-id="1d547-173">![Inbound flow in advanced warehouse configurations](media/design_details_warehouse_management_inbound_advanced_flow.png "Inbound flow in advanced warehouse configurations")</span></span>  

### <a name="1-release-source-document"></a><span data-ttu-id="1d547-174">1: Frigi kildedokument</span><span class="sxs-lookup"><span data-stu-id="1d547-174">1: Release Source Document</span></span>  
<span data-ttu-id="1d547-175">Når varer mottas på lageret, frigir brukeren som er ansvarlig for mottak, kildedokumentet, for eksempel en bestilling eller inngående overføringsordre, for å signalisere til lagermedarbeidere at de mottatte varene kan plasseres på lager.</span><span class="sxs-lookup"><span data-stu-id="1d547-175">When items are received in the warehouse, the user who is responsible for receiving releases the source document, such as a purchase order or an inbound transfer order, to signal to warehouse workers that the received items can be put away in inventory.</span></span>  

### <a name="2-create-inbound-request"></a><span data-ttu-id="1d547-176">2: Opprett inngående forespørsel</span><span class="sxs-lookup"><span data-stu-id="1d547-176">2: Create Inbound Request</span></span>  
<span data-ttu-id="1d547-177">Når det inngående kildedokumentet frigis, opprettes en inngående lagerforespørsel automatisk.</span><span class="sxs-lookup"><span data-stu-id="1d547-177">When the inbound source document is released, an inbound warehouse request is created automatically.</span></span> <span data-ttu-id="1d547-178">Den inneholder referanser til kildedokumenttype og /nummer, og er ikke synlige for brukeren.</span><span class="sxs-lookup"><span data-stu-id="1d547-178">It contains references to the source document type and number and is not visible to the user.</span></span>  

### <a name="3-create-warehouse-receipt"></a><span data-ttu-id="1d547-179">3: Opprett lagermottak</span><span class="sxs-lookup"><span data-stu-id="1d547-179">3: Create Warehouse Receipt</span></span>  
<span data-ttu-id="1d547-180">På siden **Lagermottak** henter brukeren som er ansvarlig for mottak av varer, de ventende kildedokumentlinjene basert på inngående lagerforespørsel.</span><span class="sxs-lookup"><span data-stu-id="1d547-180">On the **Warehouse Receipt** page, the user who is responsible for receiving items retrieves the pending source document lines based on the inbound warehouse request.</span></span> <span data-ttu-id="1d547-181">Flere kildedokumentlinjer kan kombineres i ett lagermottaksdokument.</span><span class="sxs-lookup"><span data-stu-id="1d547-181">Several source document lines can be combined in one warehouse receipt document.</span></span>  

<span data-ttu-id="1d547-182">Brukeren fyller ut feltet **Ant. som skal håndt.** og velger om nødvendig mottakssonen og hyllen.</span><span class="sxs-lookup"><span data-stu-id="1d547-182">The user fills in the **Qty. to Handle** field and selects the receiving zone and bin, if required.</span></span>  

### <a name="4-post-warehouse-receipt"></a><span data-ttu-id="1d547-183">4: Bokfør lagermottak</span><span class="sxs-lookup"><span data-stu-id="1d547-183">4: Post Warehouse Receipt</span></span>  
<span data-ttu-id="1d547-184">Brukeren bokfører lagermottaket.</span><span class="sxs-lookup"><span data-stu-id="1d547-184">The user posts the warehouse receipt.</span></span> <span data-ttu-id="1d547-185">Det blir opprettet positive vareposter.</span><span class="sxs-lookup"><span data-stu-id="1d547-185">Positive item ledger entries are created.</span></span> <span data-ttu-id="1d547-186">Eksempel: Feltet **Mottatt (antall)** i den inngående kildedokumentlinjen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="1d547-186">For example, the **Quantity Received** field on the inbound source document line is updated.</span></span>  

### <a name="5-create-warehouse-internal-put-away"></a><span data-ttu-id="1d547-187">5: Opprett intern lagerplassering</span><span class="sxs-lookup"><span data-stu-id="1d547-187">5: Create Warehouse Internal Put-Away</span></span>  
<span data-ttu-id="1d547-188">Brukeren som er ansvarlig for å plassere fra interne operasjoner, oppretter en intern plassering for varer som må plasseres på lageret, for eksempel produksjons- eller monteringsavgang.</span><span class="sxs-lookup"><span data-stu-id="1d547-188">The user who is responsible for putting away from internal operations creates a warehouse internal put-away for items that have to be put away in the warehouse, such as production or assembly output.</span></span> <span data-ttu-id="1d547-189">Brukeren angir antall, sone og hylle som varer skal plasseres fra, eventuelt med funksjonen **Hent hylleinnhold**.</span><span class="sxs-lookup"><span data-stu-id="1d547-189">The user specifies quantity, zone, and bin from where the items should be put away, potentially with the **Get Bin Content** function.</span></span> <span data-ttu-id="1d547-190">Brukeren frigir den interne plasseringen på lageret, som gjør at en inngående lagerforespørsel opprettes, slik at oppgaven kan hentes i lagerplasseringsdokumenter eller i plasseringsforslaget.</span><span class="sxs-lookup"><span data-stu-id="1d547-190">The user releases the warehouse internal put-away, which creates an inbound warehouse request so that the task can be retrieved in warehouse put-away documents or in the put-away worksheet.</span></span>  

### <a name="6-create-put-away-request"></a><span data-ttu-id="1d547-191">6: Opprett plasseringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="1d547-191">6: Create Put-away Request</span></span>  
<span data-ttu-id="1d547-192">Når det inngående kildedokumentet bokføres, opprettes en lagerplasseringsforespørsel automatisk.</span><span class="sxs-lookup"><span data-stu-id="1d547-192">When the inbound source document is posted, a warehouse put-away request is created automatically.</span></span> <span data-ttu-id="1d547-193">Den inneholder referanser til kildedokumenttype og /nummer, og er ikke synlige for brukeren.</span><span class="sxs-lookup"><span data-stu-id="1d547-193">It contains references to the source document type and number and is not visible to the user.</span></span> <span data-ttu-id="1d547-194">Avhengig av oppsettet vil utdata fra en produksjonsordre også opprette en plasseringsforespørsel om å plassere de ferdige varene på lageret.</span><span class="sxs-lookup"><span data-stu-id="1d547-194">Depending on the setup, output from a production order also creates a put-away request to put the finished items away in inventory.</span></span>  

### <a name="7-generate-put-away-worksheet-lines-optional"></a><span data-ttu-id="1d547-195">7: Generer plasseringsforslagslinjer (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="1d547-195">7: Generate Put-away Worksheet Lines (Optional)</span></span>  
<span data-ttu-id="1d547-196">Brukeren som er ansvarlig for å koordinere plassering, henter plasseringslinjer i **Plasseringsforslag** basert på bokførte lagermottak eller interne operasjoner med komponentforbruk.</span><span class="sxs-lookup"><span data-stu-id="1d547-196">The user who is responsible for coordinating put-aways retrieves warehouse put-away lines in the **Put-away Worksheet** based on posted warehouse receipts or internal operations with output.</span></span> <span data-ttu-id="1d547-197">Brukeren velger linjene som skal plasseres, og klargjør plasseringene ved å angi hvilke hyller det skal tas fra, hvilke det skal plasseres i, og hvor mange enheter som skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="1d547-197">The user selects the lines to be put-away and prepares the put-aways by specifying which bins to take from, which bins to place in, and how many units to handle.</span></span> <span data-ttu-id="1d547-198">Hyllene kan være forhåndsdefinert av definisjonen av lagerlokasjonen eller operasjonsressursen.</span><span class="sxs-lookup"><span data-stu-id="1d547-198">The bins may be predefined by the setup of the warehouse location or operation resource.</span></span>  

<span data-ttu-id="1d547-199">Når alle plasseringer er planlagt og tilordnet til lagermedarbeidere, genererer brukeren lagerplasseringsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="1d547-199">When all put-aways are planned and assigned to warehouse workers, the user generates the warehouse put-away documents.</span></span> <span data-ttu-id="1d547-200">Fullstendig tildelte plasseringslinjer blir slettet fra **plasseringsforslaget**.</span><span class="sxs-lookup"><span data-stu-id="1d547-200">Fully assigned put-aways lines are deleted from the **Put-away Worksheet**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1d547-201">Hvis feltet **Bruk plasseringsforslag** ikke er valgt på lokasjonskortet, blir lagerplasseringsdokumenter opprettet direkte basert på bokførte lagermottak.</span><span class="sxs-lookup"><span data-stu-id="1d547-201">If the **Use Put-away Worksheet** field is not selected on the location card, then warehouse put-away documents are created directly based on posted warehouse receipts.</span></span> <span data-ttu-id="1d547-202">I slike tilfeller utelates trinn 7.</span><span class="sxs-lookup"><span data-stu-id="1d547-202">In that case, step 7 is omitted.</span></span>  

### <a name="8-create-warehouse-put-away-document"></a><span data-ttu-id="1d547-203">8: Opprett plasseringsdokument</span><span class="sxs-lookup"><span data-stu-id="1d547-203">8: Create Warehouse Put-away Document</span></span>  
<span data-ttu-id="1d547-204">Lagermedarbeideren som utfører plasseringer, oppretter et lagerplasseringsdokument på en hentemåte, basert på det bokførte lagermottaket.</span><span class="sxs-lookup"><span data-stu-id="1d547-204">The warehouse worker who performs put-aways creates a warehouse put-away document in a pull fashion, based on the posted warehouse receipt.</span></span> <span data-ttu-id="1d547-205">Lagerplasseringsdokumentet kan også opprettes og tilordnes lagermedarbeidere med en push-metode.</span><span class="sxs-lookup"><span data-stu-id="1d547-205">Alternatively, the warehouse put-away document is created and assigned to a warehouse worker in a push fashion.</span></span>  

### <a name="9-register-warehouse-put-away"></a><span data-ttu-id="1d547-206">9: Registrer plassering</span><span class="sxs-lookup"><span data-stu-id="1d547-206">9: Register Warehouse Put-Away</span></span>  
<span data-ttu-id="1d547-207">På hver linje for varer som er plassert, helt eller delvis, fyller lagermedarbeider ut feltet **Antall** på siden **Plassering**, og registrerer deretter plasseringen.</span><span class="sxs-lookup"><span data-stu-id="1d547-207">On each line for items that have been put away, partially or fully, the warehouse worker fills in the **Quantity** field on the **Warehouse Put-away** page, and then registers the warehouse put-away.</span></span>  

<span data-ttu-id="1d547-208">Lagerposter opprettes, og lagerplasseringslinjene slettes hvis de er helt ferdigbehandlet.</span><span class="sxs-lookup"><span data-stu-id="1d547-208">Warehouse entries are created, and the warehouse put-away lines are deleted, if fully handled.</span></span> <span data-ttu-id="1d547-209">Lagerplasseringsdokumentet holdes åpent til hele antallet for det tilknyttede bokførte lagermottaket er registrert.</span><span class="sxs-lookup"><span data-stu-id="1d547-209">The warehouse put-away document remains open until the full quantity of the related posted warehouse receipt is registered.</span></span> <span data-ttu-id="1d547-210">Feltet **Plassert ant.** på bestillingslinjene for lagermottak oppdateres.</span><span class="sxs-lookup"><span data-stu-id="1d547-210">The **Qty. Put Away** field on the warehouse receipt order lines is updated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d547-211">Se også</span><span class="sxs-lookup"><span data-stu-id="1d547-211">See Also</span></span>  
[<span data-ttu-id="1d547-212">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="1d547-212">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)