---
title: Opprette et nytt selskap | Microsoft-dokumentasjon
description: Bruke RapidStart Services-tabeller og -sider som er opprettet, uten at det finnes data for dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8b534af530a7ce6d91a71ca7802938fe3573c2c2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240795"
---
# <a name="create-a-new-company"></a><span data-ttu-id="086a0-103">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="086a0-103">Create a New Company</span></span>
<span data-ttu-id="086a0-104">Hvis du vil bruke RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], oppretter du først et nytt selskap du vil utføre en kundeimplementering for.</span><span class="sxs-lookup"><span data-stu-id="086a0-104">To use RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="086a0-105">Når du oppretter et nytt selskap, opprettes standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og -sider, men de inneholder ingen data.</span><span class="sxs-lookup"><span data-stu-id="086a0-105">When you create a new company, the standard [!INCLUDE[d365fin](includes/d365fin_md.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="086a0-106">I tillegg kan du bruke bestemte oppsettsdata på selskapet etter at du har initialisert det.</span><span class="sxs-lookup"><span data-stu-id="086a0-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="086a0-107">Informasjonen leveres i en konfigurasjonspakke, en .rapidstart-fil, som leverer innhold i et komprimert format.</span><span class="sxs-lookup"><span data-stu-id="086a0-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="086a0-108">Eksempelkonfigurasjonspakker, inkludert lands-regionspesifikke filer, er inkludert i demoselskapet CRONUS.</span><span class="sxs-lookup"><span data-stu-id="086a0-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="086a0-109">Følg disse fremgangsmåtene for å bruke eksempelkonfigurasjonspakken med et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="086a0-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="086a0-110">Bruke eksempelkonfigurasjonspakken BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="086a0-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="086a0-111">Åpne demonstrasjonsselskapet CRONUS Norge AS.</span><span class="sxs-lookup"><span data-stu-id="086a0-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="086a0-112">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="086a0-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="086a0-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="086a0-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="086a0-114">Velg BASICCONFIG-pakken fra listen, og velg deretter handlingen **Eksporter pakke**.</span><span class="sxs-lookup"><span data-stu-id="086a0-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="086a0-115">Bruk følgende fremgangsmåte til å opprette et nytt selskap, og bruk BASICCONFIG-pakken som en del av prosessen.</span><span class="sxs-lookup"><span data-stu-id="086a0-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="086a0-116">Slik oppretter du et nytt selskap:</span><span class="sxs-lookup"><span data-stu-id="086a0-116">To create a new company</span></span>  
1. <span data-ttu-id="086a0-117">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="086a0-117">Create a new company.</span></span> <span data-ttu-id="086a0-118">Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="086a0-118">For more information, see [Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="086a0-119">Fra rollesenteret for RapidStart Services-implementereren kan du nå importere konfigurasjonspakken som du eksporterte fra selskapet CRONUS Norge AS.</span><span class="sxs-lookup"><span data-stu-id="086a0-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="086a0-120">Når du har opprettet et nytt selskap, blir enkelte tabeller fylt ut automatisk, selv om ingen selskapsmal er brukt.</span><span class="sxs-lookup"><span data-stu-id="086a0-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="086a0-121">Du kan for eksempel se gjennom standardkoder for bokføring og partitransaksjoner på **Kildekode**-siden.</span><span class="sxs-lookup"><span data-stu-id="086a0-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="086a0-122">Hvis du bruker en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], bør du se gjennom denne tabellen og vurdere eventuelle problemer på lokale språk.</span><span class="sxs-lookup"><span data-stu-id="086a0-122">If you provide a local version of [!INCLUDE[d365fin](includes/d365fin_md.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="086a0-123">Om datatabeller</span><span class="sxs-lookup"><span data-stu-id="086a0-123">About Data Tables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="086a0-124">-datatabeller leveres i to hovedtyper: Hoved- og Oppsett.</span><span class="sxs-lookup"><span data-stu-id="086a0-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="086a0-125">Når du oppretter en firmakonfigurasjon, kan du bruke disse typene for å skape et fokus for konfigurasjonsstrategien.</span><span class="sxs-lookup"><span data-stu-id="086a0-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="086a0-126">Hoveddatatabeller</span><span class="sxs-lookup"><span data-stu-id="086a0-126">Master Data Tables</span></span>  
<span data-ttu-id="086a0-127">Tabellen nedenfor viser noen av hoveddatatabellene.</span><span class="sxs-lookup"><span data-stu-id="086a0-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="086a0-128">Når du initialiserer et nytt selskap, er disse tabellene tomme.</span><span class="sxs-lookup"><span data-stu-id="086a0-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="086a0-129">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="086a0-129">Table No.</span></span>|<span data-ttu-id="086a0-130">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="086a0-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="086a0-131">15</span><span class="sxs-lookup"><span data-stu-id="086a0-131">15</span></span>|<span data-ttu-id="086a0-132">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="086a0-132">G/L Account</span></span>|  
|<span data-ttu-id="086a0-133">18</span><span class="sxs-lookup"><span data-stu-id="086a0-133">18</span></span>|<span data-ttu-id="086a0-134">Kunde</span><span class="sxs-lookup"><span data-stu-id="086a0-134">Customer</span></span>|  
|<span data-ttu-id="086a0-135">23</span><span class="sxs-lookup"><span data-stu-id="086a0-135">23</span></span>|<span data-ttu-id="086a0-136">Leverandør</span><span class="sxs-lookup"><span data-stu-id="086a0-136">Vendor</span></span>|  
|<span data-ttu-id="086a0-137">27</span><span class="sxs-lookup"><span data-stu-id="086a0-137">27</span></span>|<span data-ttu-id="086a0-138">Element</span><span class="sxs-lookup"><span data-stu-id="086a0-138">Item</span></span>|  
|<span data-ttu-id="086a0-139">5050</span><span class="sxs-lookup"><span data-stu-id="086a0-139">5050</span></span>|<span data-ttu-id="086a0-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="086a0-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="086a0-141">Oppsettsdatatabeller</span><span class="sxs-lookup"><span data-stu-id="086a0-141">Setup Data Tables</span></span>  
<span data-ttu-id="086a0-142">Tabellen nedenfor viser noen av oppsettsdatatabellene, der du henter oppsettsinformasjon i konfigurasjonsspørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="086a0-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="086a0-143">Disse tabellene inneholder grunnlagsinformasjon når selskapet opprettes.</span><span class="sxs-lookup"><span data-stu-id="086a0-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="086a0-144">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="086a0-144">Table No.</span></span>|<span data-ttu-id="086a0-145">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="086a0-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="086a0-146">98</span><span class="sxs-lookup"><span data-stu-id="086a0-146">98</span></span>|<span data-ttu-id="086a0-147">Finansoppsett</span><span class="sxs-lookup"><span data-stu-id="086a0-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="086a0-148">311</span><span class="sxs-lookup"><span data-stu-id="086a0-148">311</span></span>|<span data-ttu-id="086a0-149">Salgsoppsett</span><span class="sxs-lookup"><span data-stu-id="086a0-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="086a0-150">312</span><span class="sxs-lookup"><span data-stu-id="086a0-150">312</span></span>|<span data-ttu-id="086a0-151">Kjøpsoppsett</span><span class="sxs-lookup"><span data-stu-id="086a0-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="086a0-152">313</span><span class="sxs-lookup"><span data-stu-id="086a0-152">313</span></span>|<span data-ttu-id="086a0-153">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="086a0-153">Inventory Setup</span></span>|  

<span data-ttu-id="086a0-154">I tillegg til oppsettsdatatabeller har [!INCLUDE[d365fin](includes/d365fin_md.md)] også oppsettsdatatabeller med kjerneinformasjon om selskapet og dets forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="086a0-154">In addition to setup data tables, [!INCLUDE[d365fin](includes/d365fin_md.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="086a0-155">Tabellen nedenfor viser noen av dem.</span><span class="sxs-lookup"><span data-stu-id="086a0-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="086a0-156">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="086a0-156">Table No.</span></span>|<span data-ttu-id="086a0-157">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="086a0-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="086a0-158">3</span><span class="sxs-lookup"><span data-stu-id="086a0-158">3</span></span>|<span data-ttu-id="086a0-159">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="086a0-159">Payment Terms</span></span>|  
|<span data-ttu-id="086a0-160">4</span><span class="sxs-lookup"><span data-stu-id="086a0-160">4</span></span>|<span data-ttu-id="086a0-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="086a0-161">Currency</span></span>|  
|<span data-ttu-id="086a0-162">6</span><span class="sxs-lookup"><span data-stu-id="086a0-162">6</span></span>|<span data-ttu-id="086a0-163">Kundeprisgrupper</span><span class="sxs-lookup"><span data-stu-id="086a0-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="086a0-164">5700</span><span class="sxs-lookup"><span data-stu-id="086a0-164">5700</span></span>|<span data-ttu-id="086a0-165">Lagerføringsenhet</span><span class="sxs-lookup"><span data-stu-id="086a0-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="086a0-166">Se også</span><span class="sxs-lookup"><span data-stu-id="086a0-166">See Also</span></span>  
[<span data-ttu-id="086a0-167">Bruke konfigurasjoner for nye selskaper</span><span class="sxs-lookup"><span data-stu-id="086a0-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="086a0-168">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="086a0-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="086a0-169">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="086a0-169">Administration</span></span>](admin-setup-and-administration.md)
