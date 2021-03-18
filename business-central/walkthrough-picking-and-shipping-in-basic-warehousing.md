---
title: Plukking og levering i enkle lageroppsett | Microsoft-dokumentasjon
description: I Business Central kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 96a837eaded2cf9be5e1fabb4d7f81415a171f96
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393452"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="37445-103">Gjennomgang: Plukking og levering i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="37445-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="37445-104">I [!INCLUDE[prod_short](includes/prod_short.md)] kan de utgående prosessene for plukking og levering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.</span><span class="sxs-lookup"><span data-stu-id="37445-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="37445-105">Prinsipp</span><span class="sxs-lookup"><span data-stu-id="37445-105">Method</span></span>|<span data-ttu-id="37445-106">Inngående prosess</span><span class="sxs-lookup"><span data-stu-id="37445-106">Inbound process</span></span>|<span data-ttu-id="37445-107">Hyller</span><span class="sxs-lookup"><span data-stu-id="37445-107">Bins</span></span>|<span data-ttu-id="37445-108">Plukking</span><span class="sxs-lookup"><span data-stu-id="37445-108">Picks</span></span>|<span data-ttu-id="37445-109">Følgesedler</span><span class="sxs-lookup"><span data-stu-id="37445-109">Shipments</span></span>|<span data-ttu-id="37445-110">Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="37445-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="37445-111">A</span><span class="sxs-lookup"><span data-stu-id="37445-111">A</span></span>|<span data-ttu-id="37445-112">Bokføre plukking og levering fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="37445-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="37445-113">X</span><span class="sxs-lookup"><span data-stu-id="37445-113">X</span></span>|||<span data-ttu-id="37445-114">2</span><span class="sxs-lookup"><span data-stu-id="37445-114">2</span></span>|  
|<span data-ttu-id="37445-115">B</span><span class="sxs-lookup"><span data-stu-id="37445-115">B</span></span>|<span data-ttu-id="37445-116">Bokføre plukking og levering fra et lagerplukkdokument</span><span class="sxs-lookup"><span data-stu-id="37445-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="37445-117">X</span><span class="sxs-lookup"><span data-stu-id="37445-117">X</span></span>||<span data-ttu-id="37445-118">3</span><span class="sxs-lookup"><span data-stu-id="37445-118">3</span></span>|  
|<span data-ttu-id="37445-119">L</span><span class="sxs-lookup"><span data-stu-id="37445-119">C</span></span>|<span data-ttu-id="37445-120">Bokføre plukking og levering fra en lagerfølgeseddel</span><span class="sxs-lookup"><span data-stu-id="37445-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="37445-121">X</span><span class="sxs-lookup"><span data-stu-id="37445-121">X</span></span>|<span data-ttu-id="37445-122">4/5/6</span><span class="sxs-lookup"><span data-stu-id="37445-122">4/5/6</span></span>|  
|<span data-ttu-id="37445-123">D</span><span class="sxs-lookup"><span data-stu-id="37445-123">D</span></span>|<span data-ttu-id="37445-124">Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel</span><span class="sxs-lookup"><span data-stu-id="37445-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="37445-125">X</span><span class="sxs-lookup"><span data-stu-id="37445-125">X</span></span>|<span data-ttu-id="37445-126">X</span><span class="sxs-lookup"><span data-stu-id="37445-126">X</span></span>|<span data-ttu-id="37445-127">4/5/6</span><span class="sxs-lookup"><span data-stu-id="37445-127">4/5/6</span></span>|  

<span data-ttu-id="37445-128">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="37445-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="37445-129">Følgende gjennomgangen demonstrerer metoden B i forrige tabell.</span><span class="sxs-lookup"><span data-stu-id="37445-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="about-this-walkthrough"></a><span data-ttu-id="37445-130">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="37445-130">About This Walkthrough</span></span>

<span data-ttu-id="37445-131">I grunnleggende lageroppsett hvor lokasjonen er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du siden **Lagerplukk** til å registrere og bokføre plukkings- og leveringsopplysninger for de utgående kildedokumentene.</span><span class="sxs-lookup"><span data-stu-id="37445-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="37445-132">Det utgående kildedokumentet kan være en ordre, en bestillingsretur, en utgående overføringsordre eller en produksjonsordre med komponentbehov.</span><span class="sxs-lookup"><span data-stu-id="37445-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="37445-133">Denne gjennomgangen viser følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="37445-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="37445-134">Definere SØLV-plassering for lagerplukkinger.</span><span class="sxs-lookup"><span data-stu-id="37445-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="37445-135">Opprette en ordre for kunde 10000 for 30 høyttalere.</span><span class="sxs-lookup"><span data-stu-id="37445-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="37445-136">Frigir ordren for lagerhåndtering.</span><span class="sxs-lookup"><span data-stu-id="37445-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="37445-137">Opprette et lagerplukk basert på et frigitt kildedokument.</span><span class="sxs-lookup"><span data-stu-id="37445-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="37445-138">Registrerer lagerflyttingen fra lageret og bokfører samtidig følgeseddelen for salgsordrekilden.</span><span class="sxs-lookup"><span data-stu-id="37445-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles"></a><span data-ttu-id="37445-139">Roller</span><span class="sxs-lookup"><span data-stu-id="37445-139">Roles</span></span>

<span data-ttu-id="37445-140">Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:</span><span class="sxs-lookup"><span data-stu-id="37445-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="37445-141">Lagerleder</span><span class="sxs-lookup"><span data-stu-id="37445-141">Warehouse Manager</span></span>  
- <span data-ttu-id="37445-142">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="37445-142">Order Processor</span></span>  
- <span data-ttu-id="37445-143">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="37445-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="37445-144">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="37445-144">Prerequisites</span></span>

<span data-ttu-id="37445-145">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="37445-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="37445-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online bruker du et selskap basert på det alternativet **Avansert evaluering - Fullfør eksempeldata** i et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="37445-146">For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="37445-147">For lokal [!INCLUDE[prod_short](includes/prod_short.md)] installeres CRONUS International Ltd..</span><span class="sxs-lookup"><span data-stu-id="37445-147">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="37445-148">Gjør deg til lageransatt på lokasjonen SØLV ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="37445-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="37445-149">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageransatte**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="37445-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="37445-150">Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="37445-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="37445-151">Skriv inn SØLV i feltet **Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="37445-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="37445-152">Velg **Standard**- feltet.</span><span class="sxs-lookup"><span data-stu-id="37445-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="37445-153">Gjør elementet LS-81 tilgjengelig på SØLV-plasseringen ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="37445-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="37445-154">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="37445-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="37445-155">Åpne standardkladden, og opprett deretter to varekladdelinjer med følgende informasjon om arbeidsdatoen (23. januar).</span><span class="sxs-lookup"><span data-stu-id="37445-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="37445-156">Posttype</span><span class="sxs-lookup"><span data-stu-id="37445-156">Entry Type</span></span>|<span data-ttu-id="37445-157">Varenummer</span><span class="sxs-lookup"><span data-stu-id="37445-157">Item Number</span></span>|<span data-ttu-id="37445-158">Lokasjonskode</span><span class="sxs-lookup"><span data-stu-id="37445-158">Location Code</span></span>|<span data-ttu-id="37445-159">Hyllekode</span><span class="sxs-lookup"><span data-stu-id="37445-159">Bin Code</span></span>|<span data-ttu-id="37445-160">Antall</span><span class="sxs-lookup"><span data-stu-id="37445-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="37445-161">Oppjustering</span><span class="sxs-lookup"><span data-stu-id="37445-161">Positive Adjmt.</span></span>|<span data-ttu-id="37445-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="37445-162">LS-81</span></span>|<span data-ttu-id="37445-163">SØLV</span><span class="sxs-lookup"><span data-stu-id="37445-163">SILVER</span></span>|<span data-ttu-id="37445-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="37445-164">S-01-0001</span></span>|<span data-ttu-id="37445-165">20</span><span class="sxs-lookup"><span data-stu-id="37445-165">20</span></span>|  
        |<span data-ttu-id="37445-166">Oppjustering</span><span class="sxs-lookup"><span data-stu-id="37445-166">Positive Adjmt.</span></span>|<span data-ttu-id="37445-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="37445-167">LS-81</span></span>|<span data-ttu-id="37445-168">SØLV</span><span class="sxs-lookup"><span data-stu-id="37445-168">SILVER</span></span>|<span data-ttu-id="37445-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="37445-169">S-01-0002</span></span>|<span data-ttu-id="37445-170">20</span><span class="sxs-lookup"><span data-stu-id="37445-170">20</span></span>|  

  3. <span data-ttu-id="37445-171">Velg **Bokfør**-handlingen, og velg deretter **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="37445-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="37445-172">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="37445-172">Story</span></span>

<span data-ttu-id="37445-173">Ellen, lagersjefen på CRONUS, setter opp SØLV-lageret for grunnleggende plukkhåndtering der lagermedarbeidere behandler utgående ordrer individuelt.</span><span class="sxs-lookup"><span data-stu-id="37445-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="37445-174">Ordrebehandleren Heidi oppretter en ordre for 30 enheter av varen LS-81 som skal leveres til kunde 10000 fra SØLV-lageret.</span><span class="sxs-lookup"><span data-stu-id="37445-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="37445-175">John, lagermedarbeideren, må kontrollere at forsendelsen klargjøres og leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="37445-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="37445-176">John behandler alle involverte oppgaver på siden **Lagerplukk**, som peker automatisk til hyllene der LS-81 er lagret.</span><span class="sxs-lookup"><span data-stu-id="37445-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="37445-177">Definere plassering</span><span class="sxs-lookup"><span data-stu-id="37445-177">Setting Up the Location</span></span>

<span data-ttu-id="37445-178">Oppsettet av siden **Lokasjonskort** definerer selskapets lagerflyter.</span><span class="sxs-lookup"><span data-stu-id="37445-178">The setup of the **Location Card** page defines the company's warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="37445-179">Slik definerer du lokasjonen</span><span class="sxs-lookup"><span data-stu-id="37445-179">To set up the location</span></span>

1. <span data-ttu-id="37445-180">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="37445-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37445-181">Åpne lokasjonskortet SØLV.</span><span class="sxs-lookup"><span data-stu-id="37445-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="37445-182">I hurtigfanen **Lager** merker du av for **Plukk nødv.**.</span><span class="sxs-lookup"><span data-stu-id="37445-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="37445-183">Opprette ordren</span><span class="sxs-lookup"><span data-stu-id="37445-183">Creating the Sales Order</span></span>

<span data-ttu-id="37445-184">Salgsordrer er den vanligste typen av utgående kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="37445-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="37445-185">Slik oppretter du ordren</span><span class="sxs-lookup"><span data-stu-id="37445-185">To create the sales order</span></span>

1. <span data-ttu-id="37445-186">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="37445-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37445-187">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="37445-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="37445-188">Opprett en ordre for kunde 10000 på arbeidsdatoen (23. januar) med følgende ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="37445-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="37445-189">Vare</span><span class="sxs-lookup"><span data-stu-id="37445-189">Item</span></span>|<span data-ttu-id="37445-190">Lokasjonskode</span><span class="sxs-lookup"><span data-stu-id="37445-190">Location Code</span></span>|<span data-ttu-id="37445-191">Antall</span><span class="sxs-lookup"><span data-stu-id="37445-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="37445-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="37445-192">LS_81</span></span>|<span data-ttu-id="37445-193">SØLV</span><span class="sxs-lookup"><span data-stu-id="37445-193">SILVER</span></span>|<span data-ttu-id="37445-194">30</span><span class="sxs-lookup"><span data-stu-id="37445-194">30</span></span>|  

     <span data-ttu-id="37445-195">Fortsett med å informere lageret om at ordren er klar for lagerhåndtering.</span><span class="sxs-lookup"><span data-stu-id="37445-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="37445-196">Velg handlingen **Frigi**.</span><span class="sxs-lookup"><span data-stu-id="37445-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="37445-197">John fortsetter å plukke og leverer solgte varer.</span><span class="sxs-lookup"><span data-stu-id="37445-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="37445-198">Plukke og levere varer</span><span class="sxs-lookup"><span data-stu-id="37445-198">Picking and Shipping Items</span></span>

<span data-ttu-id="37445-199">På siden **Lagerplukk** kan du håndtere alle utgående lageraktiviteter for et bestemt kildedokument, for eksempel en ordre.</span><span class="sxs-lookup"><span data-stu-id="37445-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="37445-200">Slik plukker og leverer du varer:</span><span class="sxs-lookup"><span data-stu-id="37445-200">To pick and ship items</span></span>

1. <span data-ttu-id="37445-201">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="37445-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="37445-202">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="37445-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="37445-203">Pass på at **Nr.**</span><span class="sxs-lookup"><span data-stu-id="37445-203">Make sure that the **No.**</span></span> <span data-ttu-id="37445-204">-feltet i hurtigfanen **Generelt** er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="37445-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="37445-205">Velg feltet **Kildedokument**, og velg deretter **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="37445-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="37445-206">Velg feltet **Kildenr.**, velg linjen for salg til kunde 10000, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="37445-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="37445-207">Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter ordren.</span><span class="sxs-lookup"><span data-stu-id="37445-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="37445-208">Velg handlingen **Autoutfyll ant som skal håndt**.</span><span class="sxs-lookup"><span data-stu-id="37445-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="37445-209">Du kan også skrive inn 10 og 20 i de to lagerplukklinjene i feltet **Ant. som skal håndt.**.</span><span class="sxs-lookup"><span data-stu-id="37445-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="37445-210">Velg **Bokfør**-handlingen, velg **Lever**, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="37445-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="37445-211">30 høyttalere er nå registrert som plukket fra hyllene S-01-0001 og S-01-0002, og det opprettes en negativ varepost som gjenspeiler den bokførte følgeseddelen.</span><span class="sxs-lookup"><span data-stu-id="37445-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="37445-212">Se også</span><span class="sxs-lookup"><span data-stu-id="37445-212">See Also</span></span>

[<span data-ttu-id="37445-213">Plukke varer med lagerplukk</span><span class="sxs-lookup"><span data-stu-id="37445-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="37445-214">Plukke varer for lagerlevering</span><span class="sxs-lookup"><span data-stu-id="37445-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="37445-215">Opprette grunnleggende lagre med operasjonsområder</span><span class="sxs-lookup"><span data-stu-id="37445-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="37445-216">Flytte komponenter til et operasjonsområde i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="37445-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="37445-217">Plukke for produksjon eller montering</span><span class="sxs-lookup"><span data-stu-id="37445-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="37445-218">Flytte varer ad hoc i enkle lageroppsett</span><span class="sxs-lookup"><span data-stu-id="37445-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="37445-219">Designdetaljer: Utgående lagerflyt</span><span class="sxs-lookup"><span data-stu-id="37445-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="37445-220">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="37445-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="37445-221">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37445-221">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]