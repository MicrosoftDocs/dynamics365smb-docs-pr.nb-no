---
title: Gjennomgang – Mottak og plassering i enkle lageroppsett | Microsoft-dokumentasjon
description: I Business Central kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 597f14f07f7e8ac690dce8a5473d01ec68d1669a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314748"
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a><span data-ttu-id="cac9c-103">Gjennomgang: Mottak og plassering i grunnleggende lageroppsett</span><span class="sxs-lookup"><span data-stu-id="cac9c-103">Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations</span></span>

<span data-ttu-id="cac9c-104">**Merk**: Denne gjennomgangen må utføres i et demoselskap med alternativet **Full evaluering - Fullfør eksempeldata**, som er tilgjengelig i Sandbox-miljøet.</span><span class="sxs-lookup"><span data-stu-id="cac9c-104">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="cac9c-105">Hvis du vil ha mer informasjon, kan du se [Opprette et sandkassemiljø](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cac9c-105">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="cac9c-106">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de inngående prosessene for mottak og plassering utføres på fire måter ved hjelp av forskjellige funksjoner avhengig av kompleksitetsnivået til lageret.</span><span class="sxs-lookup"><span data-stu-id="cac9c-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="cac9c-107">Prinsipp</span><span class="sxs-lookup"><span data-stu-id="cac9c-107">Method</span></span>|<span data-ttu-id="cac9c-108">Inngående prosess</span><span class="sxs-lookup"><span data-stu-id="cac9c-108">Inbound process</span></span>|<span data-ttu-id="cac9c-109">Hyller</span><span class="sxs-lookup"><span data-stu-id="cac9c-109">Bins</span></span>|<span data-ttu-id="cac9c-110">Mottak</span><span class="sxs-lookup"><span data-stu-id="cac9c-110">Receipts</span></span>|<span data-ttu-id="cac9c-111">Plassering</span><span class="sxs-lookup"><span data-stu-id="cac9c-111">Put-aways</span></span>|<span data-ttu-id="cac9c-112">Kompleksitetsnivå (se [Designdetaljer: Lageroppsett](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="cac9c-112">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="cac9c-113">A</span><span class="sxs-lookup"><span data-stu-id="cac9c-113">A</span></span>|<span data-ttu-id="cac9c-114">Bokføre mottak og plassering fra ordrelinjen</span><span class="sxs-lookup"><span data-stu-id="cac9c-114">Post receipt and put-away from the order line</span></span>|<span data-ttu-id="cac9c-115">X</span><span class="sxs-lookup"><span data-stu-id="cac9c-115">X</span></span>|||<span data-ttu-id="cac9c-116">2</span><span class="sxs-lookup"><span data-stu-id="cac9c-116">2</span></span>|  
|<span data-ttu-id="cac9c-117">B</span><span class="sxs-lookup"><span data-stu-id="cac9c-117">B</span></span>|<span data-ttu-id="cac9c-118">Bokføre mottak og plassering fra et lagerplasseringsdokument</span><span class="sxs-lookup"><span data-stu-id="cac9c-118">Post receipt and put-away from an inventory put-away document</span></span>|||<span data-ttu-id="cac9c-119">X</span><span class="sxs-lookup"><span data-stu-id="cac9c-119">X</span></span>|<span data-ttu-id="cac9c-120">3</span><span class="sxs-lookup"><span data-stu-id="cac9c-120">3</span></span>|  
|<span data-ttu-id="cac9c-121">L</span><span class="sxs-lookup"><span data-stu-id="cac9c-121">C</span></span>|<span data-ttu-id="cac9c-122">Bokføre mottak og plassering fra et lagermottaksdokument</span><span class="sxs-lookup"><span data-stu-id="cac9c-122">Post receipt and put-away from a warehouse receipt document</span></span>||<span data-ttu-id="cac9c-123">X</span><span class="sxs-lookup"><span data-stu-id="cac9c-123">X</span></span>||<span data-ttu-id="cac9c-124">4/5/6</span><span class="sxs-lookup"><span data-stu-id="cac9c-124">4/5/6</span></span>|  
|<span data-ttu-id="cac9c-125">D</span><span class="sxs-lookup"><span data-stu-id="cac9c-125">D</span></span>|<span data-ttu-id="cac9c-126">Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument</span><span class="sxs-lookup"><span data-stu-id="cac9c-126">Post receipt from a warehouse receipt document and post put-away from a warehouse put-away document</span></span>||<span data-ttu-id="cac9c-127">X</span><span class="sxs-lookup"><span data-stu-id="cac9c-127">X</span></span>|<span data-ttu-id="cac9c-128">X</span><span class="sxs-lookup"><span data-stu-id="cac9c-128">X</span></span>|<span data-ttu-id="cac9c-129">4/5/6</span><span class="sxs-lookup"><span data-stu-id="cac9c-129">4/5/6</span></span>|  

<span data-ttu-id="cac9c-130">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="cac9c-130">For more information, see [Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="cac9c-131">Følgende gjennomgangen demonstrerer metoden B i forrige tabell.</span><span class="sxs-lookup"><span data-stu-id="cac9c-131">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="cac9c-132">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="cac9c-132">About This Walkthrough</span></span>  
<span data-ttu-id="cac9c-133">I genkle lageroppsett hvor lokasjonen er definert til å kreve plasseringsbehandling, men ikke mottaksbehandling, bruker du siden **Lagerplassering** til å registrere og bokføre plasserings- og mottaksopplysninger for de inngående kildedokumentene.</span><span class="sxs-lookup"><span data-stu-id="cac9c-133">In basic warehouse configurations where your location is set up to require put-away processing but not receive processing, you use the **Inventory Put-away** page to record and post put-away and receipt information for your inbound source documents.</span></span> <span data-ttu-id="cac9c-134">Det inngående kildedokument kan være en bestilling, en ordreretur, en inngående overføringsordre eller en produksjonsordre med avgang som er klar til plassering.</span><span class="sxs-lookup"><span data-stu-id="cac9c-134">The inbound source document can be a purchase order, sales return order, inbound transfer order, or production order with output that is ready to be put away.</span></span>

> [!NOTE]
> <span data-ttu-id="cac9c-135">Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter for firma på lokasjoner der du velger disse avmerkingsboksene.</span><span class="sxs-lookup"><span data-stu-id="cac9c-135">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="cac9c-136">Denne gjennomgangen viser følgende oppgaver.</span><span class="sxs-lookup"><span data-stu-id="cac9c-136">This walkthrough demonstrates the following tasks.</span></span>  

-   <span data-ttu-id="cac9c-137">Definere SØLV-plassering for lagerplasseringer.</span><span class="sxs-lookup"><span data-stu-id="cac9c-137">Setting up SILVER location for inventory put aways.</span></span>  
-   <span data-ttu-id="cac9c-138">Definere SØLV-plassering for hyllehåndtering.</span><span class="sxs-lookup"><span data-stu-id="cac9c-138">Setting up SILVER location for bin handling.</span></span>  
-   <span data-ttu-id="cac9c-139">Definere en standardhylle for varen LS-81.</span><span class="sxs-lookup"><span data-stu-id="cac9c-139">Defining a default bin for item LS-81.</span></span> <span data-ttu-id="cac9c-140">(LS-75 er allerede er satt opp i CRONUS.)</span><span class="sxs-lookup"><span data-stu-id="cac9c-140">(LS-75 is already set up in CRONUS.)</span></span>  
-   <span data-ttu-id="cac9c-141">Opprette en bestilling for leverandør 10000 for 40 høyttalere.</span><span class="sxs-lookup"><span data-stu-id="cac9c-141">Creating a purchase order for vendor 10000 for 40 loudspeakers.</span></span>  
-   <span data-ttu-id="cac9c-142">Verifiserer at plasseringshyllene er forhåndsinnstilt i oppsettet.</span><span class="sxs-lookup"><span data-stu-id="cac9c-142">Verifying that the put-away bins are preset by setup.</span></span>  
-   <span data-ttu-id="cac9c-143">Frigir bestillingen for lagerhåndtering.</span><span class="sxs-lookup"><span data-stu-id="cac9c-143">Releasing the purchase order for warehouse handling.</span></span>  
-   <span data-ttu-id="cac9c-144">Opprette en lagerplassering basert på et frigitt kildedokument.</span><span class="sxs-lookup"><span data-stu-id="cac9c-144">Creating an inventory put-away based on a released source document.</span></span>  
-   <span data-ttu-id="cac9c-145">Verifiserer at plasseringshyllene er arvet fra bestillingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-145">Verifying that the put-away bins are inherited from the purchase order.</span></span>  
-   <span data-ttu-id="cac9c-146">Registrerer lagerflyttingen til lageret og bokfører samtidig mottaket for kildebestillingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-146">Registering the warehouse movement into the warehouse and at the same time posting the purchase receipt for the source purchase order.</span></span>  

## <a name="roles"></a><span data-ttu-id="cac9c-147">Roller</span><span class="sxs-lookup"><span data-stu-id="cac9c-147">Roles</span></span>  
<span data-ttu-id="cac9c-148">Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:</span><span class="sxs-lookup"><span data-stu-id="cac9c-148">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

-   <span data-ttu-id="cac9c-149">Lagerleder</span><span class="sxs-lookup"><span data-stu-id="cac9c-149">Warehouse Manager</span></span>  
-   <span data-ttu-id="cac9c-150">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="cac9c-150">Purchasing Agent</span></span>  
-   <span data-ttu-id="cac9c-151">Lagermedarbeider</span><span class="sxs-lookup"><span data-stu-id="cac9c-151">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="cac9c-152">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="cac9c-152">Prerequisites</span></span>  
<span data-ttu-id="cac9c-153">For å fullføre denne gjennomgangen må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="cac9c-153">To complete this walkthrough, you will need:</span></span>  

-   <span data-ttu-id="cac9c-154">CRONUS Norge AS installert.</span><span class="sxs-lookup"><span data-stu-id="cac9c-154">CRONUS International Ltd. installed.</span></span>  
-   <span data-ttu-id="cac9c-155">Gjør deg til lageransatt på lokasjonen SØLV ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="cac9c-155">To make yourself a warehouse employee at SILVER location by following these steps:</span></span>  

    1.  <span data-ttu-id="cac9c-156">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageransatte**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-156">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
    2.  <span data-ttu-id="cac9c-157">Velg feltet **Bruker-ID**, og velg din egen brukerkonto på siden **Brukere**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-157">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
    3.  <span data-ttu-id="cac9c-158">Skriv inn SØLV i feltet **Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-158">In the **Location Code** field, enter SILVER.</span></span>  
    4.  <span data-ttu-id="cac9c-159">Velg **Standard**-feltet.</span><span class="sxs-lookup"><span data-stu-id="cac9c-159">Select the **Default** field.</span></span>  

## <a name="story"></a><span data-ttu-id="cac9c-160">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="cac9c-160">Story</span></span>  
<span data-ttu-id="cac9c-161">Ellen, lagerlederen hos CRONUS Norge AS, oppretter en bestilling for 10 enheter av varen LS-75 og 30 enheter av varen LS-81 fra leverandør 10000 som skal leveres til SØLV-lageret.</span><span class="sxs-lookup"><span data-stu-id="cac9c-161">Ellen, the warehouse manager at CRONUS International Ltd., creates a purchase order for 10 units of item LS-75 and 30 units of item LS-81 from vendor 10000 to be delivered to SILVER Warehouse.</span></span> <span data-ttu-id="cac9c-162">Når leveringen ankommer til lageret, plasserer lagermedarbeideren John varene i standardhyller definert for varene.</span><span class="sxs-lookup"><span data-stu-id="cac9c-162">When the delivery arrives at the warehouse, John, the warehouse worker, puts the items away in default bins defined for the items.</span></span> <span data-ttu-id="cac9c-163">Når John bokfører plasseringen, bokføres varene som mottatt på lageret og tilgjengelig for salg eller andre behov.</span><span class="sxs-lookup"><span data-stu-id="cac9c-163">When John posts the put-away, the items are posted as received into inventory and available for sale or other demand.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="cac9c-164">Definere plassering</span><span class="sxs-lookup"><span data-stu-id="cac9c-164">Setting up the Location</span></span>  
 <span data-ttu-id="cac9c-165">Oppsettet av siden **Lokasjonskort** definerer selskapets lagerflyter.</span><span class="sxs-lookup"><span data-stu-id="cac9c-165">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="cac9c-166">Slik definerer du lokasjonen:</span><span class="sxs-lookup"><span data-stu-id="cac9c-166">To set up the location</span></span>  

1.  <span data-ttu-id="cac9c-167">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-167">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cac9c-168">Åpne lokasjonskortet SØLV.</span><span class="sxs-lookup"><span data-stu-id="cac9c-168">Open the SILVER location card.</span></span>  
3.  <span data-ttu-id="cac9c-169">Merk av for **Plassering nødv.**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-169">Select the **Require Put-away** check box.</span></span>  

    <span data-ttu-id="cac9c-170">Fortsett med å sette opp en standardhylle for de to varenumrene for å kontrollere hvor de er plassert.</span><span class="sxs-lookup"><span data-stu-id="cac9c-170">Proceed to set up a default bin for the two item numbers to control where they are put away.</span></span>  

4.  <span data-ttu-id="cac9c-171">Velg handlingen **Hyller**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-171">Choose the **Bins** action.</span></span>  
5.  <span data-ttu-id="cac9c-172">Merk den første raden, hylle S-01-0001, og velg **Innhold**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-172">Select the first row, for bin S-01-0001, and then choose the **Contents** action.</span></span>  

    <span data-ttu-id="cac9c-173">Legg merke til at på siden **Hylleinnhold** er varen LS-75 allerede definert som innhold i hyllen S-01-0001.</span><span class="sxs-lookup"><span data-stu-id="cac9c-173">Notice on the **Bin Content** page that item LS-75 is already set up as content in bin S-01-0001.</span></span>  

6.  <span data-ttu-id="cac9c-174">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-174">Choose the **New** action.</span></span>  
7.  <span data-ttu-id="cac9c-175">Velg feltene **Fast** og **Standard**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-175">Select the **Fixed** and the **Default** fields.</span></span>  
8.  <span data-ttu-id="cac9c-176">Angi LS-81 i feltet **Varenr.**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-176">In the **Item No.** field, enter LS-81.</span></span>  

## <a name="creating-the-purchase-order"></a><span data-ttu-id="cac9c-177">Opprette bestillingen</span><span class="sxs-lookup"><span data-stu-id="cac9c-177">Creating the Purchase Order</span></span>  
<span data-ttu-id="cac9c-178">Bestillinger er den vanligste typen inngående kildedokument.</span><span class="sxs-lookup"><span data-stu-id="cac9c-178">Purchase orders are the most common type of inbound source document.</span></span>  

### <a name="to-create-the-purchase-order"></a><span data-ttu-id="cac9c-179">Slik oppretter du bestillingen:</span><span class="sxs-lookup"><span data-stu-id="cac9c-179">To create the purchase order</span></span>  

1.  <span data-ttu-id="cac9c-180">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cac9c-181">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-181">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="cac9c-182">Opprett en bestilling for leverandør 10000 på arbeidsdatoen (23. januar) med følgende bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="cac9c-182">Create a purchase order for vendor 10000 on the work date (January 23) with the following purchase order lines.</span></span>  

    |<span data-ttu-id="cac9c-183">Vare</span><span class="sxs-lookup"><span data-stu-id="cac9c-183">Item</span></span>|<span data-ttu-id="cac9c-184">Lokasjonskode</span><span class="sxs-lookup"><span data-stu-id="cac9c-184">Location code</span></span>|<span data-ttu-id="cac9c-185">Hyllekode</span><span class="sxs-lookup"><span data-stu-id="cac9c-185">Bin code</span></span>|<span data-ttu-id="cac9c-186">Antall</span><span class="sxs-lookup"><span data-stu-id="cac9c-186">Quantity</span></span>|  
    |----------|-------------------|--------------|--------------|  
    |<span data-ttu-id="cac9c-187">LS_75</span><span class="sxs-lookup"><span data-stu-id="cac9c-187">LS_75</span></span>|<span data-ttu-id="cac9c-188">SØLV</span><span class="sxs-lookup"><span data-stu-id="cac9c-188">SILVER</span></span>|<span data-ttu-id="cac9c-189">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="cac9c-189">S-01-0001</span></span>|<span data-ttu-id="cac9c-190">10</span><span class="sxs-lookup"><span data-stu-id="cac9c-190">10</span></span>|  
    |<span data-ttu-id="cac9c-191">LS-81</span><span class="sxs-lookup"><span data-stu-id="cac9c-191">LS-81</span></span>|<span data-ttu-id="cac9c-192">SØLV</span><span class="sxs-lookup"><span data-stu-id="cac9c-192">SILVER</span></span>|<span data-ttu-id="cac9c-193">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="cac9c-193">S-01-0001</span></span>|<span data-ttu-id="cac9c-194">30</span><span class="sxs-lookup"><span data-stu-id="cac9c-194">30</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="cac9c-195">Hyllekoden angis automatisk i samsvar med oppsettet du utførte i delen Definere plassering.</span><span class="sxs-lookup"><span data-stu-id="cac9c-195">The bin code is entered automatically according to the setup that you performed in the “Setting up the Location” section.</span></span>  

    <span data-ttu-id="cac9c-196">Fortsett med å varsle lageret om at bestillingen er klar for håndtering av lageret når leveringen ankommer.</span><span class="sxs-lookup"><span data-stu-id="cac9c-196">Proceed to notify the warehouse that the purchase order is ready for warehouse handling when the delivery arrives.</span></span>  

4.  <span data-ttu-id="cac9c-197">Velg handlingen **Frigi**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-197">Choose the **Release** action.</span></span>  

    <span data-ttu-id="cac9c-198">Leveringen av høyttalere fra leverandør 10000 er ankommet på SØLV-lageret, og John fortsetter med å plassere dem.</span><span class="sxs-lookup"><span data-stu-id="cac9c-198">The delivery of loudspeakers from vendor 10000 has arrived at SILVER warehouse, and John proceeds to put them away.</span></span>  

## <a name="receiving-and-putting-the-items-away"></a><span data-ttu-id="cac9c-199">Mottak og plassering av varer</span><span class="sxs-lookup"><span data-stu-id="cac9c-199">Receiving and Putting the Items Away</span></span>  
<span data-ttu-id="cac9c-200">På siden **Lagerplassering** kan du håndtere alle inngående lageraktiviteter for et bestemt kildedokument, for eksempel en bestilling.</span><span class="sxs-lookup"><span data-stu-id="cac9c-200">On the **Inventory Put-away** page, you can manage all inbound warehouse activities for a specific source document, such as a purchase order.</span></span>  

### <a name="to-receive-and-put-the-items-away"></a><span data-ttu-id="cac9c-201">Slik mottar og plasserer du varene:</span><span class="sxs-lookup"><span data-stu-id="cac9c-201">To receive and put the items away</span></span>  

1.  <span data-ttu-id="cac9c-202">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lagerplasseringer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-202">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-aways**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cac9c-203">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-203">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="cac9c-204">Velg feltet **Kildedokument**, og velg deretter **Bestilling**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-204">Select the **Source Document** field, and then select **Purchase Order**.</span></span>  
4.  <span data-ttu-id="cac9c-205">Velg feltet **Kildenr.**, velg linjen for kjøp fra leverandør 10000, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-205">Select the **Source No.** field, select the line for the purchase from vendor 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="cac9c-206">På fanebladet **Handlinger** i gruppen **Funksjoner** velger du eventuelt **Hent kildedokument**, og deretter velger du bestillingen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-206">Alternatively, on the **Actions** tab, in the **Functions** group, choose **Get Source Document**, and then select the purchase order.</span></span>  

5.  <span data-ttu-id="cac9c-207">Velg handlingen **Autoutfyll ant som skal håndt**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-207">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="cac9c-208">Du kan også skrive inn 10 og 30 i de to lagerplasseringslinjene i feltet **Ant. som skal håndt.**.</span><span class="sxs-lookup"><span data-stu-id="cac9c-208">Alternatively, in the **Qty. to Handle** field, enter 10 and 30 respectively on the two inventory put-away lines.</span></span>  

6.  <span data-ttu-id="cac9c-209">Velg **Bokfør**-handlingen, velg **Motta og fakturer**, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="cac9c-209">Choose the **Post** action, select the **Receive** action, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="cac9c-210">40 høyttalere er nå registrert som plassert i hyllen S-01-0001, og det opprettes en positiv varepost som gjenspeiler det bokførte kjøpsmottaket.</span><span class="sxs-lookup"><span data-stu-id="cac9c-210">The 40 loudspeakers are now registered as put away in bin S-01-0001, and a positive item ledger entry is created reflecting the posted purchase receipt.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cac9c-211">Se også</span><span class="sxs-lookup"><span data-stu-id="cac9c-211">See Also</span></span>  
 <span data-ttu-id="cac9c-212">[Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-212">[Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md) </span></span>  
 <span data-ttu-id="cac9c-213">[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-213">[Set Up Basic Warehouses with Operations Areas](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) </span></span>  
 <span data-ttu-id="cac9c-214">[Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-214">[Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="cac9c-215">[Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-215">[Pick for Production or Assembly](warehouse-how-to-pick-for-production.md) </span></span>  
 <span data-ttu-id="cac9c-216">[Flytte varer ad hoc i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-216">[Move Items Ad Hoc in Basic Warehouse Configurations](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) </span></span>  
 <span data-ttu-id="cac9c-217">[Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md) </span><span class="sxs-lookup"><span data-stu-id="cac9c-217">[Design Details: Inbound Warehouse Flow](design-details-inbound-warehouse-flow.md) </span></span>  
 [<span data-ttu-id="cac9c-218">Gjennomgang av forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="cac9c-218">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="cac9c-219">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cac9c-219">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
