---
title: Opprette et nytt selskap | Microsoft-dokumentasjon
description: Bruke RapidStart Services-tabeller og -sider som er opprettet, uten at det finnes data for dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c21d86c67c6020d1a32da4816246bc7aaf96c2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779885"
---
# <a name="create-a-new-company"></a><span data-ttu-id="66cac-103">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="66cac-103">Create a New Company</span></span>
<span data-ttu-id="66cac-104">Hvis du vil bruke RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], oppretter du først et nytt selskap du vil utføre en kundeimplementering for.</span><span class="sxs-lookup"><span data-stu-id="66cac-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="66cac-105">Når du oppretter et nytt selskap, opprettes standard [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og -sider, men de inneholder ingen data.</span><span class="sxs-lookup"><span data-stu-id="66cac-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="66cac-106">I tillegg kan du bruke bestemte oppsettsdata på selskapet etter at du har initialisert det.</span><span class="sxs-lookup"><span data-stu-id="66cac-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="66cac-107">Informasjonen leveres i en konfigurasjonspakke, en .rapidstart-fil, som leverer innhold i et komprimert format.</span><span class="sxs-lookup"><span data-stu-id="66cac-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="66cac-108">Eksempelkonfigurasjonspakker, inkludert lands-regionspesifikke filer, er inkludert i demoselskapet CRONUS.</span><span class="sxs-lookup"><span data-stu-id="66cac-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="66cac-109">Følg disse fremgangsmåtene for å bruke eksempelkonfigurasjonspakken med et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="66cac-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="66cac-110">Bruke eksempelkonfigurasjonspakken BASICCONFIG</span><span class="sxs-lookup"><span data-stu-id="66cac-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="66cac-111">Åpne demonstrasjonsselskapet CRONUS Norge AS.</span><span class="sxs-lookup"><span data-stu-id="66cac-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="66cac-112">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="66cac-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="66cac-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonspakker**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="66cac-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="66cac-114">Velg BASICCONFIG-pakken fra listen, og velg deretter handlingen **Eksporter pakke**.</span><span class="sxs-lookup"><span data-stu-id="66cac-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="66cac-115">Bruk følgende fremgangsmåte til å opprette et nytt selskap, og bruk BASICCONFIG-pakken som en del av prosessen.</span><span class="sxs-lookup"><span data-stu-id="66cac-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="66cac-116">Slik oppretter du et nytt selskap:</span><span class="sxs-lookup"><span data-stu-id="66cac-116">To create a new company</span></span>  
1. <span data-ttu-id="66cac-117">Opprett et nytt selskap.</span><span class="sxs-lookup"><span data-stu-id="66cac-117">Create a new company.</span></span> <span data-ttu-id="66cac-118">Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="66cac-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="66cac-119">Fra rollesenteret for RapidStart Services-implementereren kan du nå importere konfigurasjonspakken som du eksporterte fra selskapet CRONUS Norge AS.</span><span class="sxs-lookup"><span data-stu-id="66cac-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="66cac-120">Når du har opprettet et nytt selskap, blir enkelte tabeller fylt ut automatisk, selv om ingen selskapsmal er brukt.</span><span class="sxs-lookup"><span data-stu-id="66cac-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="66cac-121">Du kan for eksempel se gjennom standardkoder for bokføring og partitransaksjoner på **Kildekode**-siden.</span><span class="sxs-lookup"><span data-stu-id="66cac-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="66cac-122">Hvis du bruker en lokal versjon av [!INCLUDE[prod_short](includes/prod_short.md)], bør du se gjennom denne tabellen og vurdere eventuelle problemer på lokale språk.</span><span class="sxs-lookup"><span data-stu-id="66cac-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="66cac-123">Om datatabeller</span><span class="sxs-lookup"><span data-stu-id="66cac-123">About Data Tables</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="66cac-124">-datatabeller leveres i to hovedtyper: Hoved- og Oppsett.</span><span class="sxs-lookup"><span data-stu-id="66cac-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="66cac-125">Når du oppretter en firmakonfigurasjon, kan du bruke disse typene for å skape et fokus for konfigurasjonsstrategien.</span><span class="sxs-lookup"><span data-stu-id="66cac-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="66cac-126">Hoveddatatabeller</span><span class="sxs-lookup"><span data-stu-id="66cac-126">Master Data Tables</span></span>  
<span data-ttu-id="66cac-127">Tabellen nedenfor viser noen av hoveddatatabellene.</span><span class="sxs-lookup"><span data-stu-id="66cac-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="66cac-128">Når du initialiserer et nytt selskap, er disse tabellene tomme.</span><span class="sxs-lookup"><span data-stu-id="66cac-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="66cac-129">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="66cac-129">Table No.</span></span>|<span data-ttu-id="66cac-130">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="66cac-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="66cac-131">15</span><span class="sxs-lookup"><span data-stu-id="66cac-131">15</span></span>|<span data-ttu-id="66cac-132">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="66cac-132">G/L Account</span></span>|  
|<span data-ttu-id="66cac-133">18</span><span class="sxs-lookup"><span data-stu-id="66cac-133">18</span></span>|<span data-ttu-id="66cac-134">Kunde</span><span class="sxs-lookup"><span data-stu-id="66cac-134">Customer</span></span>|  
|<span data-ttu-id="66cac-135">23</span><span class="sxs-lookup"><span data-stu-id="66cac-135">23</span></span>|<span data-ttu-id="66cac-136">Leverandør</span><span class="sxs-lookup"><span data-stu-id="66cac-136">Vendor</span></span>|  
|<span data-ttu-id="66cac-137">27</span><span class="sxs-lookup"><span data-stu-id="66cac-137">27</span></span>|<span data-ttu-id="66cac-138">Element</span><span class="sxs-lookup"><span data-stu-id="66cac-138">Item</span></span>|  
|<span data-ttu-id="66cac-139">5050</span><span class="sxs-lookup"><span data-stu-id="66cac-139">5050</span></span>|<span data-ttu-id="66cac-140">Kontakt</span><span class="sxs-lookup"><span data-stu-id="66cac-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="66cac-141">Oppsettsdatatabeller</span><span class="sxs-lookup"><span data-stu-id="66cac-141">Setup Data Tables</span></span>  
<span data-ttu-id="66cac-142">Tabellen nedenfor viser noen av oppsettsdatatabellene, der du henter oppsettsinformasjon i konfigurasjonsspørreskjemaet.</span><span class="sxs-lookup"><span data-stu-id="66cac-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="66cac-143">Disse tabellene inneholder grunnlagsinformasjon når selskapet opprettes.</span><span class="sxs-lookup"><span data-stu-id="66cac-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="66cac-144">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="66cac-144">Table No.</span></span>|<span data-ttu-id="66cac-145">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="66cac-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="66cac-146">98</span><span class="sxs-lookup"><span data-stu-id="66cac-146">98</span></span>|<span data-ttu-id="66cac-147">Finansoppsett</span><span class="sxs-lookup"><span data-stu-id="66cac-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="66cac-148">311</span><span class="sxs-lookup"><span data-stu-id="66cac-148">311</span></span>|<span data-ttu-id="66cac-149">Salgsoppsett</span><span class="sxs-lookup"><span data-stu-id="66cac-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="66cac-150">312</span><span class="sxs-lookup"><span data-stu-id="66cac-150">312</span></span>|<span data-ttu-id="66cac-151">Kjøpsoppsett</span><span class="sxs-lookup"><span data-stu-id="66cac-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="66cac-152">313</span><span class="sxs-lookup"><span data-stu-id="66cac-152">313</span></span>|<span data-ttu-id="66cac-153">Lageroppsett</span><span class="sxs-lookup"><span data-stu-id="66cac-153">Inventory Setup</span></span>|  

<span data-ttu-id="66cac-154">I tillegg til oppsettsdatatabeller har [!INCLUDE[prod_short](includes/prod_short.md)] også oppsettsdatatabeller med kjerneinformasjon om selskapet og dets forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="66cac-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="66cac-155">Tabellen nedenfor viser noen av dem.</span><span class="sxs-lookup"><span data-stu-id="66cac-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="66cac-156">Tabellnr.</span><span class="sxs-lookup"><span data-stu-id="66cac-156">Table No.</span></span>|<span data-ttu-id="66cac-157">Tabellnavn</span><span class="sxs-lookup"><span data-stu-id="66cac-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="66cac-158">3</span><span class="sxs-lookup"><span data-stu-id="66cac-158">3</span></span>|<span data-ttu-id="66cac-159">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="66cac-159">Payment Terms</span></span>|  
|<span data-ttu-id="66cac-160">4</span><span class="sxs-lookup"><span data-stu-id="66cac-160">4</span></span>|<span data-ttu-id="66cac-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="66cac-161">Currency</span></span>|  
|<span data-ttu-id="66cac-162">6</span><span class="sxs-lookup"><span data-stu-id="66cac-162">6</span></span>|<span data-ttu-id="66cac-163">Kundeprisgrupper</span><span class="sxs-lookup"><span data-stu-id="66cac-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="66cac-164">5700</span><span class="sxs-lookup"><span data-stu-id="66cac-164">5700</span></span>|<span data-ttu-id="66cac-165">Lagerføringsenhet</span><span class="sxs-lookup"><span data-stu-id="66cac-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="66cac-166">Se også</span><span class="sxs-lookup"><span data-stu-id="66cac-166">See Also</span></span>  
[<span data-ttu-id="66cac-167">Bruke konfigurasjoner for nye selskaper</span><span class="sxs-lookup"><span data-stu-id="66cac-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="66cac-168">Konfigurere et selskap med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="66cac-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="66cac-169">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="66cac-169">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]