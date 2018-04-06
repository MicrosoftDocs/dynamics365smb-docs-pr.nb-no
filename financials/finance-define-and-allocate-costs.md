---
title: Definere og fordele kostnader | Microsoft-dokumentasjon
description: "Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Du kan definere så mange fordelinger som du trenger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a><span data-ttu-id="53bf2-104">Definere og fordele kostnader</span><span class="sxs-lookup"><span data-stu-id="53bf2-104">Defining and Allocating Costs</span></span>
<span data-ttu-id="53bf2-105">Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter.</span><span class="sxs-lookup"><span data-stu-id="53bf2-105">Cost allocations move costs and revenues between cost types, cost centers, and cost objects.</span></span> <span data-ttu-id="53bf2-106">Du kan definere så mange fordelinger som du trenger.</span><span class="sxs-lookup"><span data-stu-id="53bf2-106">You can define as many allocations as you need.</span></span> <span data-ttu-id="53bf2-107">Hver fordeling består av:</span><span class="sxs-lookup"><span data-stu-id="53bf2-107">Each allocation consists of:</span></span>  

-   <span data-ttu-id="53bf2-108">En fordelingskilde.</span><span class="sxs-lookup"><span data-stu-id="53bf2-108">An allocation source.</span></span>  
-   <span data-ttu-id="53bf2-109">Ett eller flere tildelingsmål.</span><span class="sxs-lookup"><span data-stu-id="53bf2-109">One or more allocation targets.</span></span>  

<span data-ttu-id="53bf2-110">Fordelingskilde fastsetter hvilke kostnader må fordeles, og fordelingsmålene avgjør hvor kostnadene må fordeles.</span><span class="sxs-lookup"><span data-stu-id="53bf2-110">The allocation source establishes which costs must be allocated, and the allocation targets determine where the costs must be allocated.</span></span> <span data-ttu-id="53bf2-111">En fordelingskilde kan for eksempel være kostnadene for kostnadstypen Elektrisitet og oppvarming.</span><span class="sxs-lookup"><span data-stu-id="53bf2-111">For example, an allocation source can be the costs for the Electricity and Heating cost type.</span></span> <span data-ttu-id="53bf2-112">Du tilordner alle elektrisitets- og oppvarmingskostnader til tre kostsentre: Workshop, Produksjon og Salg.</span><span class="sxs-lookup"><span data-stu-id="53bf2-112">You allocate all electricity and heating costs to three cost centers: Workshop, Production, and Sales.</span></span> <span data-ttu-id="53bf2-113">Disse kostsentrene er fordelingsmålene dine.</span><span class="sxs-lookup"><span data-stu-id="53bf2-113">These cost centers are your allocation targets.</span></span>  

<span data-ttu-id="53bf2-114">For hver fordelingskilde kan du definere du et fordelingsnivå, en gyldighetsperiode og en variant som grupperingsidentifikator.</span><span class="sxs-lookup"><span data-stu-id="53bf2-114">For each allocation source, you define an allocation level, a validity period, and a variant as grouping identifier.</span></span> <span data-ttu-id="53bf2-115">Du kan bruke en kjørsel til å definere filtre for å velge fordelingsdefinisjoner, og deretter kjøre kostfordelinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="53bf2-115">You can use a batch job to set filters to select allocation definitions and then run cost allocations automatically.</span></span>  

<span data-ttu-id="53bf2-116">For hvert fordelingsmål kan du definere et fordelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="53bf2-116">For each allocation target, you define an allocation base.</span></span> <span data-ttu-id="53bf2-117">Fordelingsgrunnlaget kan være statisk eller dynamisk.</span><span class="sxs-lookup"><span data-stu-id="53bf2-117">The allocation base can be either static or dynamic.</span></span>  

-   <span data-ttu-id="53bf2-118">Statiske fordelingsgrunnlag er basert på en bestemt verdi, for eksempel kvadratmeter eller et fastsatt fordelingsforhold, for eksempel 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="53bf2-118">Static allocation bases are based on a definite value, such as square footage or an established allocation ratio, such as 5:2:4.</span></span>  
-   <span data-ttu-id="53bf2-119">Grunnlaget for dynamisk fordeling avhenger av verdier som kan endres, for eksempel antall ansatte i et kostsenter eller salgsinntekten av et kostobjekt i løpet av en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="53bf2-119">Dynamic allocation bases depend on changeable values, such as the number of employees in a cost center or sales revenue of a cost object throughout a certain time period.</span></span>  

<span data-ttu-id="53bf2-120">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="53bf2-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="53bf2-121">Til</span><span class="sxs-lookup"><span data-stu-id="53bf2-121">To</span></span>|<span data-ttu-id="53bf2-122">Se</span><span class="sxs-lookup"><span data-stu-id="53bf2-122">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="53bf2-123">Definere fordelingskilde og kildens mål.</span><span class="sxs-lookup"><span data-stu-id="53bf2-123">Set up allocation source and its targets.</span></span>|[<span data-ttu-id="53bf2-124">Definere fordelingskilde og -mål</span><span class="sxs-lookup"><span data-stu-id="53bf2-124">Set Up Allocation Source and Targets</span></span>](finance-how-to-set-up-allocation-source-and-targets.md)|  
|<span data-ttu-id="53bf2-125">Definere ulike filtre for dynamiske fordelingsgrunnlag.</span><span class="sxs-lookup"><span data-stu-id="53bf2-125">Set up various filters for dynamic allocation bases.</span></span>|[<span data-ttu-id="53bf2-126">Angi filtre for dynamisk fordelingsgrunnlag</span><span class="sxs-lookup"><span data-stu-id="53bf2-126">Setting Filters for Dynamic Allocation Bases</span></span>](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|<span data-ttu-id="53bf2-127">Se et eksempel på hvordan du definerer en statisk fordeling.</span><span class="sxs-lookup"><span data-stu-id="53bf2-127">See an example of how to define a static allocation.</span></span>|[<span data-ttu-id="53bf2-128">Eksempelscenario: Definere statiske fordelinger basert på fordelingsgrad</span><span class="sxs-lookup"><span data-stu-id="53bf2-128">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|<span data-ttu-id="53bf2-129">Se et eksempel på hvordan du definerer en dynamisk fordeling.</span><span class="sxs-lookup"><span data-stu-id="53bf2-129">See an example of how to define a dynamic allocation.</span></span>|[<span data-ttu-id="53bf2-130">Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer</span><span class="sxs-lookup"><span data-stu-id="53bf2-130">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a><span data-ttu-id="53bf2-131">Se også</span><span class="sxs-lookup"><span data-stu-id="53bf2-131">See Also</span></span>  
 <span data-ttu-id="53bf2-132">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="53bf2-132">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
 <span data-ttu-id="53bf2-133">[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="53bf2-133">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="53bf2-134">[Gjøre rede for kostnader](finance-manage-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="53bf2-134">[Accounting for Costs](finance-manage-cost-accounting.md) </span></span>  
 <span data-ttu-id="53bf2-135">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="53bf2-135">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="53bf2-136">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="53bf2-136">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

