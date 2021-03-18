---
title: Oversikt over komponent og arkitektur for Power BI-integrering for Business Central | Microsoft Docs
description: Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Business Central-apper for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d6c01d95dfaebe6682c4c5e20bc85bdebb0c9b54
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377926"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="d4197-103">Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="d4197-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="d4197-104">I denne artikkelen får du informasjon om de forskjellige aspektene ved Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)] for å gjøre det enklere å forstå hvordan du implementerer og bruker den.</span><span class="sxs-lookup"><span data-stu-id="d4197-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="d4197-105">Komponenter</span><span class="sxs-lookup"><span data-stu-id="d4197-105">Components</span></span>

<span data-ttu-id="d4197-106">Tabellen nedenfor beskriver de hovedkomponentene som er involvert i Power BI-integrering.</span><span class="sxs-lookup"><span data-stu-id="d4197-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="d4197-107">Komponent</span><span class="sxs-lookup"><span data-stu-id="d4197-107">Component</span></span>|<span data-ttu-id="d4197-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d4197-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="d4197-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="d4197-109">Power BI</span></span>|<span data-ttu-id="d4197-110">En skybasert tjeneste for drifting og administrasjon av rapporter.</span><span class="sxs-lookup"><span data-stu-id="d4197-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="d4197-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d4197-111">Power BI Desktop</span></span>|<span data-ttu-id="d4197-112">Et redigeringsverktøy du bruker til å bygge rapporter og instrumentbord, og gjør at du kan kjøre rapporter.</span><span class="sxs-lookup"><span data-stu-id="d4197-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="d4197-113">Det er tilgjengelig som en gratis nedlasting i Microsoft Store og installeres lokalt.</span><span class="sxs-lookup"><span data-stu-id="d4197-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="d4197-114">Online eller lokal løsning med koblinger som er eksponert for Power BI, og kan bygge inn en Power BI-del.</span><span class="sxs-lookup"><span data-stu-id="d4197-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="d4197-115">Hva som er tilgjengelig fra begynnelsen</span><span class="sxs-lookup"><span data-stu-id="d4197-115">What's available from the start</span></span>

<span data-ttu-id="d4197-116">Tabellen nedenfor beskriver tilgjengelige funksjoner.</span><span class="sxs-lookup"><span data-stu-id="d4197-116">The following table describes available features.</span></span>

|<span data-ttu-id="d4197-117">Funksjon</span><span class="sxs-lookup"><span data-stu-id="d4197-117">Feature</span></span>|<span data-ttu-id="d4197-118">Støtte for [!INCLUDE[prod_short](includes/prod_short.md)] Online eller lokalt</span><span class="sxs-lookup"><span data-stu-id="d4197-118">[!INCLUDE[prod_short](includes/prod_short.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="d4197-119">Power BI-koblinger</span><span class="sxs-lookup"><span data-stu-id="d4197-119">Power BI connectors</span></span>|<span data-ttu-id="d4197-120">Begge deler.</span><span class="sxs-lookup"><span data-stu-id="d4197-120">Both.</span></span> <span data-ttu-id="d4197-121">Ulike koblinger for Online og lokalt.</span><span class="sxs-lookup"><span data-stu-id="d4197-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="d4197-122">Samme kobling brukes for Power BI Desktop og Power BI-tjeneste.</span><span class="sxs-lookup"><span data-stu-id="d4197-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="d4197-123">Innebygd opplevelse for visning av en gitt rapport i en faktaboks i [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="d4197-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="d4197-124">Begge deler.</span><span class="sxs-lookup"><span data-stu-id="d4197-124">Both.</span></span> <span data-ttu-id="d4197-125">Må konfigureres for å kunne vise rapporter for den lokale versjonen.</span><span class="sxs-lookup"><span data-stu-id="d4197-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="d4197-126">Power BI-rapportadministrasjon fra [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="d4197-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="d4197-127">Online</span><span class="sxs-lookup"><span data-stu-id="d4197-127">Online</span></span>|
|<span data-ttu-id="d4197-128">Standard Power BI-rapporter for rollesentre distribueres til Power BI</span><span class="sxs-lookup"><span data-stu-id="d4197-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="d4197-129">Online</span><span class="sxs-lookup"><span data-stu-id="d4197-129">Online</span></span>|
|<span data-ttu-id="d4197-130">Power BI-apper i Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="d4197-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="d4197-131">Online</span><span class="sxs-lookup"><span data-stu-id="d4197-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="d4197-132">Arkitektur</span><span class="sxs-lookup"><span data-stu-id="d4197-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d4197-133">integreres med Power BI via en kobling som bruker OData.</span><span class="sxs-lookup"><span data-stu-id="d4197-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="d4197-134">Datakilden for Power BI-rapporter eksponeres som OData-nettjenester.</span><span class="sxs-lookup"><span data-stu-id="d4197-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-arkitektur for integrering med Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="d4197-136">Generell flyt</span><span class="sxs-lookup"><span data-stu-id="d4197-136">General Flow</span></span>

<span data-ttu-id="d4197-137">Diagrammet nedenfor viser den grunnleggende arbeidsflyten for brukere når du kobler [!INCLUDE[prod_short](includes/prod_short.md)] til Power BI.</span><span class="sxs-lookup"><span data-stu-id="d4197-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Power BI-arbeidsflyt for integrering med Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="d4197-139">Brukeren registrerer seg for en Power BI-konto.</span><span class="sxs-lookup"><span data-stu-id="d4197-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="d4197-140">Brukeren kobler seg til Power BI fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d4197-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d4197-141">kontrollerer lisensen.</span><span class="sxs-lookup"><span data-stu-id="d4197-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d4197-142">distribuerer standardrapporter til Power BI-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d4197-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="d4197-143">Dette trinnet skjer bare for [!INCLUDE[prod_short](includes/prod_short.md)] Online.</span><span class="sxs-lookup"><span data-stu-id="d4197-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d4197-144">gjør rapporter i Power BI tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d4197-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d4197-145">Standardrapporter vises automatisk i Power BI-deler.</span><span class="sxs-lookup"><span data-stu-id="d4197-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="d4197-146">Brukeren oppretter en rapport i Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d4197-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="d4197-147">Brukeren publiserer rapporten til Power BI-tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d4197-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="d4197-148">Rapportene blir deretter tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d4197-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d4197-149">Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="d4197-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="d4197-150">Se også</span><span class="sxs-lookup"><span data-stu-id="d4197-150">See Also</span></span>

[<span data-ttu-id="d4197-151">Business Central og Power BI</span><span class="sxs-lookup"><span data-stu-id="d4197-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="d4197-152">Power BI for forbrukere</span><span class="sxs-lookup"><span data-stu-id="d4197-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="d4197-153">Nytt utseende på Power BI-tjenesten</span><span class="sxs-lookup"><span data-stu-id="d4197-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="d4197-154">Hurtigstart: Koble til data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d4197-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="d4197-155">Power BI-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="d4197-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="d4197-156">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="d4197-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="d4197-157">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="d4197-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="d4197-158">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="d4197-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="d4197-159">[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d4197-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="d4197-160">[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="d4197-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="d4197-161">[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="d4197-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="d4197-162">[Ved hjelp av [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="d4197-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]