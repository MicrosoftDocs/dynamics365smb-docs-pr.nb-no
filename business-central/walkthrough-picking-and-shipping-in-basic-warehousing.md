---
title: Plukking og levering i enkle lageroppsett
description: I Business Central kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214656"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="b53de-103">Gjennomgang: Plukking og levering i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="b53de-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="b53de-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.</span><span class="sxs-lookup"><span data-stu-id="b53de-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="b53de-105">Prinsipp</span><span class="sxs-lookup"><span data-stu-id="b53de-105">Method</span></span>|<span data-ttu-id="b53de-106">Inngående prosess</span><span class="sxs-lookup"><span data-stu-id="b53de-106">Inbound process</span></span>|<span data-ttu-id="b53de-107">Hyller</span><span class="sxs-lookup"><span data-stu-id="b53de-107">Bins</span></span>|<span data-ttu-id="b53de-108">Plukking</span><span class="sxs-lookup"><span data-stu-id="b53de-108">Picks</span></span>|<span data-ttu-id="b53de-109">Følgesedler</span><span class="sxs-lookup"><span data-stu-id="b53de-109">Shipments</span></span>|<span data-ttu-id="b53de-110">Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="b53de-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="b53de-111">A</span><span class="sxs-lookup"><span data-stu-id="b53de-111">A</span></span>|<span data-ttu-id="b53de-112">Bokføre plukking og levering fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="b53de-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="b53de-113">X</span><span class="sxs-lookup"><span data-stu-id="b53de-113">X</span></span>|||<span data-ttu-id="b53de-114">2</span><span class="sxs-lookup"><span data-stu-id="b53de-114">2</span></span>|  
|<span data-ttu-id="b53de-115">B</span><span class="sxs-lookup"><span data-stu-id="b53de-115">B</span></span>|<span data-ttu-id="b53de-116">Bokføre plukking og levering fra et lagerplukkdokument</span><span class="sxs-lookup"><span data-stu-id="b53de-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="b53de-117">X</span><span class="sxs-lookup"><span data-stu-id="b53de-117">X</span></span>||<span data-ttu-id="b53de-118">3</span><span class="sxs-lookup"><span data-stu-id="b53de-118">3</span></span>|  
|<span data-ttu-id="b53de-119">L</span><span class="sxs-lookup"><span data-stu-id="b53de-119">C</span></span>|<span data-ttu-id="b53de-120">Bokføre plukking og levering fra en lagerfølgeseddel</span><span class="sxs-lookup"><span data-stu-id="b53de-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="b53de-121">X</span><span class="sxs-lookup"><span data-stu-id="b53de-121">X</span></span>|<span data-ttu-id="b53de-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="b53de-122">4/5/6</span></span>|  
|<span data-ttu-id="b53de-123">D</span><span class="sxs-lookup"><span data-stu-id="b53de-123">D</span></span>|<span data-ttu-id="b53de-124">Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel</span><span class="sxs-lookup"><span data-stu-id="b53de-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="b53de-125">X</span><span class="sxs-lookup"><span data-stu-id="b53de-125">X</span></span>|<span data-ttu-id="b53de-126">X</span><span class="sxs-lookup"><span data-stu-id="b53de-126">X</span></span>|<span data-ttu-id="b53de-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="b53de-127">4/5/6</span></span>|  

<span data-ttu-id="b53de-128">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="b53de-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="b53de-129">Følgende gjennomgangen demonstrerer metoden B i forrige tabell.</span><span class="sxs-lookup"><span data-stu-id="b53de-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="b53de-130">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="b53de-130">About This Walkthrough</span></span>

<span data-ttu-id="b53de-131">I grunnleggende lageroppsett hvor lokasjonen er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du siden **Lagerplukk** til å registrere og bokføre plukkings- og leveringsopplysninger for de utgående kildedokumentene.</span><span class="sxs-lookup"><span data-stu-id="b53de-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="b53de-132">Det utgående kildedokumentet kan være en ordre, en bestillingsretur, en utgående overføringsordre eller en produksjonsordre med komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="b53de-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="b53de-133">Denne gjennomgangen viser følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="b53de-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="b53de-134">Definere SØR-plassering for lagerplukkinger.</span><span class="sxs-lookup"><span data-stu-id="b53de-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="b53de-135">Opprette en ordre for kunde 10000 for 30 Amsterdam-lamper.</span><span class="sxs-lookup"><span data-stu-id="b53de-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="b53de-136">Frigir ordren for lagerhåndtering.</span><span class="sxs-lookup"><span data-stu-id="b53de-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="b53de-137">Opprette et lagerplukk basert på et frigitt kildedokument.</span><span class="sxs-lookup"><span data-stu-id="b53de-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="b53de-138">Registrerer lagerflyttingen fra lageret og bokfører samtidig følgeseddelen for salgsordrekilden.</span><span class="sxs-lookup"><span data-stu-id="b53de-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="b53de-139">Roller</span><span class="sxs-lookup"><span data-stu-id="b53de-139">Roles</span></span>

<span data-ttu-id="b53de-140">Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:</span><span class="sxs-lookup"><span data-stu-id="b53de-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="b53de-141">Lagerleder</span><span class="sxs-lookup"><span data-stu-id="b53de-141">Warehouse Manager</span></span>  
- <span data-ttu-id="b53de-142">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="b53de-142">Order Processor</span></span>  
- <span data-ttu-id="b53de-143">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="b53de-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="b53de-144">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="b53de-144">Story</span></span>

<span data-ttu-id="b53de-145">Ellen, lagersjefen på CRONUS, setter opp SØR-lageret for grunnleggende plukkhåndtering der lagermedarbeidere behandler utgående ordrer individuelt.</span><span class="sxs-lookup"><span data-stu-id="b53de-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="b53de-146">Ordrebehandleren Heidi oppretter en ordre for 30 enheter av varen 1928-S som skal leveres til kunde 10000 fra SØR-lageret.</span><span class="sxs-lookup"><span data-stu-id="b53de-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="b53de-147">John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="b53de-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="b53de-148">John behandler alle involverte oppgaver på siden **Lagerplukk**, som peker automatisk til hyllene der 1928-S er lagret.</span><span class="sxs-lookup"><span data-stu-id="b53de-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="b53de-149">Definere hyllekodene</span><span class="sxs-lookup"><span data-stu-id="b53de-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="b53de-150">Når lokasjonen er definert, må du legge til to hyller.</span><span class="sxs-lookup"><span data-stu-id="b53de-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="b53de-151">Slik definerer du hyllekodene</span><span class="sxs-lookup"><span data-stu-id="b53de-151">To setup the bin codes</span></span>

1. <span data-ttu-id="b53de-152">Velg handlingen **Hyller**.</span><span class="sxs-lookup"><span data-stu-id="b53de-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="b53de-153">Opprett to hyller med kodene *S-01-0001* og *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="b53de-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="b53de-154">Opprette deg selv som en lageransatt på lokasjon SØR</span><span class="sxs-lookup"><span data-stu-id="b53de-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="b53de-155">For å kunne bruke denne funksjonaliteten må du legge deg selv til på lokasjonen som en lagerarbeider.</span><span class="sxs-lookup"><span data-stu-id="b53de-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="b53de-156">Slik oppretter du deg selv som en lageransatt</span><span class="sxs-lookup"><span data-stu-id="b53de-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="b53de-157">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen første](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageransatte**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b53de-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="b53de-158">Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Lageransatte**.</span><span class="sxs-lookup"><span data-stu-id="b53de-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="b53de-159">Velg SØR i feltet **Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="b53de-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="b53de-160">Velg feltet **Standard**, og velg deretter **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b53de-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="b53de-161">Gjøre vare 1928-S tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="b53de-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="b53de-162">For å gjøre varen 1928-S tilgjengelig på SØR-plasseringen følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="b53de-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="b53de-163">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen andre](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b53de-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="b53de-164">Åpne standardkladden, og opprett deretter to varekladdelinjer med følgende informasjon om arbeidsdatoen (23. januar).</span><span class="sxs-lookup"><span data-stu-id="b53de-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="b53de-165">Posttype</span><span class="sxs-lookup"><span data-stu-id="b53de-165">Entry Type</span></span>|<span data-ttu-id="b53de-166">Varenummer</span><span class="sxs-lookup"><span data-stu-id="b53de-166">Item Number</span></span>|<span data-ttu-id="b53de-167">Lokasjonskode</span><span class="sxs-lookup"><span data-stu-id="b53de-167">Location Code</span></span>|<span data-ttu-id="b53de-168">Hyllekode</span><span class="sxs-lookup"><span data-stu-id="b53de-168">Bin Code</span></span>|<span data-ttu-id="b53de-169">Antall</span><span class="sxs-lookup"><span data-stu-id="b53de-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="b53de-170">Oppjustering</span><span class="sxs-lookup"><span data-stu-id="b53de-170">Positive Adjmt.</span></span>|<span data-ttu-id="b53de-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="b53de-171">1928-S</span></span>|<span data-ttu-id="b53de-172">SØR</span><span class="sxs-lookup"><span data-stu-id="b53de-172">SOUTH</span></span>|<span data-ttu-id="b53de-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="b53de-173">S-01-0001</span></span>|<span data-ttu-id="b53de-174">20</span><span class="sxs-lookup"><span data-stu-id="b53de-174">20</span></span>|  
        |<span data-ttu-id="b53de-175">Oppjustering</span><span class="sxs-lookup"><span data-stu-id="b53de-175">Positive Adjmt.</span></span>|<span data-ttu-id="b53de-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="b53de-176">1928-S</span></span>|<span data-ttu-id="b53de-177">SØR</span><span class="sxs-lookup"><span data-stu-id="b53de-177">SOUTH</span></span>|<span data-ttu-id="b53de-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="b53de-178">S-01-0002</span></span>|<span data-ttu-id="b53de-179">20</span><span class="sxs-lookup"><span data-stu-id="b53de-179">20</span></span>|  

        <span data-ttu-id="b53de-180">Som standard er feltet **Hyllekode** på salgslinjen skjult, så du må vise den.</span><span class="sxs-lookup"><span data-stu-id="b53de-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="b53de-181">Du må tilpasse siden for å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="b53de-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="b53de-182">Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="b53de-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="b53de-183">Velg **Handlinger**, **Bokføring** og deretter **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="b53de-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="b53de-184">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b53de-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="b53de-185">Opprette ordren</span><span class="sxs-lookup"><span data-stu-id="b53de-185">Creating the Sales Order</span></span>

<span data-ttu-id="b53de-186">Salgsordrer er den vanligste typen av utgående kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="b53de-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="b53de-187">Slik oppretter du ordren</span><span class="sxs-lookup"><span data-stu-id="b53de-187">To create the sales order</span></span>

1. <span data-ttu-id="b53de-188">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen tredje](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b53de-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b53de-189">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b53de-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="b53de-190">Opprett en ordre for kunde 10000 på arbeidsdatoen (23. januar) med følgende ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="b53de-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="b53de-191">Vare</span><span class="sxs-lookup"><span data-stu-id="b53de-191">Item</span></span>|<span data-ttu-id="b53de-192">Lokasjonskode</span><span class="sxs-lookup"><span data-stu-id="b53de-192">Location Code</span></span>|<span data-ttu-id="b53de-193">Antall</span><span class="sxs-lookup"><span data-stu-id="b53de-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="b53de-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="b53de-194">1928-S</span></span>|<span data-ttu-id="b53de-195">SØR</span><span class="sxs-lookup"><span data-stu-id="b53de-195">SOUTH</span></span>|<span data-ttu-id="b53de-196">30</span><span class="sxs-lookup"><span data-stu-id="b53de-196">30</span></span>|  

     <span data-ttu-id="b53de-197">Fortsett med å informere lageret om at ordren er klar for lagerhåndtering.</span><span class="sxs-lookup"><span data-stu-id="b53de-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="b53de-198">Velg handlingen **Frigi**.</span><span class="sxs-lookup"><span data-stu-id="b53de-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="b53de-199">John fortsetter å plukke og leverer solgte varer.</span><span class="sxs-lookup"><span data-stu-id="b53de-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="b53de-200">Plukke og levere varer</span><span class="sxs-lookup"><span data-stu-id="b53de-200">Picking and Shipping Items</span></span>

<span data-ttu-id="b53de-201">På siden **Lagerplukk** kan du håndtere alle utgående lageraktiviteter for et bestemt kildedokument, for eksempel en ordre.</span><span class="sxs-lookup"><span data-stu-id="b53de-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="b53de-202">Slik plukker og leverer du varer:</span><span class="sxs-lookup"><span data-stu-id="b53de-202">To pick and ship items</span></span>

1. <span data-ttu-id="b53de-203">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen fjerde](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b53de-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b53de-204">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b53de-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="b53de-205">Pass på at **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b53de-205">Make sure that the **No.**</span></span> <span data-ttu-id="b53de-206">-feltet i hurtigfanen **Generelt** er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="b53de-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="b53de-207">Velg feltet **Kildedokument**, og velg deretter **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="b53de-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="b53de-208">Velg feltet **Kildenr.**, velg linjen for salg til kunde 10000, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b53de-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="b53de-209">Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter ordren.</span><span class="sxs-lookup"><span data-stu-id="b53de-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="b53de-210">Velg handlingen **Autoutfyll ant som skal håndt**.</span><span class="sxs-lookup"><span data-stu-id="b53de-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="b53de-211">Du kan også skrive inn 10 og 20 i de to lagerplukklinjene i feltet **Ant. som skal håndt.**.</span><span class="sxs-lookup"><span data-stu-id="b53de-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="b53de-212">Velg **Bokfør**-handlingen, velg **Lever**, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="b53de-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="b53de-213">30 Amsterdam-lamper er nå registrert som plukket fra hyllene S-01-0001 og S-01-0002, og det opprettes en negativ varepost som gjenspeiler den bokførte følgeseddelen.</span><span class="sxs-lookup"><span data-stu-id="b53de-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b53de-214">Se også</span><span class="sxs-lookup"><span data-stu-id="b53de-214">See Also</span></span>

[<span data-ttu-id="b53de-215">Plukke varer med lagerplukk</span><span class="sxs-lookup"><span data-stu-id="b53de-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="b53de-216">Plukke varer for lagerlevering</span><span class="sxs-lookup"><span data-stu-id="b53de-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="b53de-217">Opprette grunnleggende lagre med operasjonsområder</span><span class="sxs-lookup"><span data-stu-id="b53de-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="b53de-218">Flytte komponenter til et operasjonsområde i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="b53de-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="b53de-219">Plukke for produksjon eller montering</span><span class="sxs-lookup"><span data-stu-id="b53de-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="b53de-220">Flytte varer ad hoc i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="b53de-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="b53de-221">Designdetaljer: Utgående lagerflyt</span><span class="sxs-lookup"><span data-stu-id="b53de-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="b53de-222">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="b53de-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="b53de-223">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b53de-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
