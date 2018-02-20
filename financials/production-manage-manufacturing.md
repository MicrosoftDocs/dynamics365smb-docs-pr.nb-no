---
title: "Utføre produksjon | Microsoft-dokumentasjon"
description: "Når behov er planlagt og materialer er utstedt i henhold til produksjonsstykklistene, kan de faktiske produksjonsoperasjonene startes og kjøres i rekkefølgen definert i produksjonsordreruten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: e358e505977e2229ad7f7338fb22e0d8075b0aa9
ms.contentlocale: nb-no
ms.lasthandoff: 02/02/2018

---
# <a name="manufacturing"></a><span data-ttu-id="2e22e-103">Produksjon</span><span class="sxs-lookup"><span data-stu-id="2e22e-103">Manufacturing</span></span>
<span data-ttu-id="2e22e-104">Når behov er planlagt og materialer er utstedt i henhold til produksjonsstykklistene, kan de faktiske produksjonsoperasjonene startes og kjøres i rekkefølgen definert i produksjonsordreruten.</span><span class="sxs-lookup"><span data-stu-id="2e22e-104">When demand is planned for and the materials have been issued according to production BOMs, then the actual production operations can start and be executed in the sequence defined by the production order routing.</span></span>  

<span data-ttu-id="2e22e-105">En viktig del av produksjonsutførelsen, sett fra systemets side, er å bokføre produksjonsavgang i databasen for å rapportere fremdrift, og å oppdatere beholdningen med de ferdige varene.</span><span class="sxs-lookup"><span data-stu-id="2e22e-105">An important part of executing production, from a system point of view, is to post production output to the database to report progress and to update inventory with the finished items.</span></span> <span data-ttu-id="2e22e-106">Avgang kan bokføres manuelt ved å fylle ut og bokføre kladdelinjer etter produksjonsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="2e22e-106">Output posting can be done manually, by filling and posting journal lines after production operations.</span></span> <span data-ttu-id="2e22e-107">Det kan også gjøres automatisk ved å bruke lagertrekk fremover.</span><span class="sxs-lookup"><span data-stu-id="2e22e-107">Or, it can be done automatically with the use of backward flushing.</span></span> <span data-ttu-id="2e22e-108">Materialforbruk blir da bokført automatisk samtidig med avgang når produksjonsordren endres til Ferdig.</span><span class="sxs-lookup"><span data-stu-id="2e22e-108">In that case material consumption is automatically posted along with output when the production order changes to finished.</span></span>  

<span data-ttu-id="2e22e-109">Som et alternativ til kladden for massebokføring av avgang for flere produksjonsordrer, kan du bruke **Produksjonskladd**-vinduet til å bokføre forbruk og/eller avgang for én produksjonsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="2e22e-109">As an alternative to the batch journal for output posting for multiple production orders, you can use the **Production Journal** window to post consumption and/or output for one production order line.</span></span>

<span data-ttu-id="2e22e-110">Før du kan begynne å produsere varer, må du gjøre ulike oppsett, for eksempel arbeidssentre, ruter og produksjonsstykklister.</span><span class="sxs-lookup"><span data-stu-id="2e22e-110">Before you can begin to produce items, you must make various setup, such as work centers, routings, and production BOMs.</span></span> <span data-ttu-id="2e22e-111">Hvis du vil ha mer informasjon, kan du se [Definere produksjon](production-configure-production-processes.md).</span><span class="sxs-lookup"><span data-stu-id="2e22e-111">For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).</span></span>

<span data-ttu-id="2e22e-112">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="2e22e-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="2e22e-113">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="2e22e-113">**To**</span></span>|<span data-ttu-id="2e22e-114">**Se**</span><span class="sxs-lookup"><span data-stu-id="2e22e-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="2e22e-115">Forstå hvordan produksjonsordrer fungerer.</span><span class="sxs-lookup"><span data-stu-id="2e22e-115">Understand how production orders work.</span></span>|[<span data-ttu-id="2e22e-116">Om produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="2e22e-116">About Production Orders</span></span>](production-about-production-orders.md)|
|<span data-ttu-id="2e22e-117">Opprett produksjonsordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="2e22e-117">Create production orders manually.</span></span>|[<span data-ttu-id="2e22e-118">Opprette produksjonsordrer</span><span class="sxs-lookup"><span data-stu-id="2e22e-118">Create Production Orders</span></span>](production-how-to-create-production-orders.md)|
|<span data-ttu-id="2e22e-119">Sett ut alle eller utvalgte operasjoner i en produksjonsstykkliste til en underleverandør.</span><span class="sxs-lookup"><span data-stu-id="2e22e-119">Outsource all or selected operations in a production order to a subcontractor.</span></span>|[<span data-ttu-id="2e22e-120">Underleveranse av produksjon</span><span class="sxs-lookup"><span data-stu-id="2e22e-120">Subcontract Manufacturing</span></span>](production-how-to-subcontract-manufacturing.md)|
|<span data-ttu-id="2e22e-121">Registrere og bokføre produksjonsavgang, i tillegg til material- og tidsforbruk, for én enkelt frigitt produksjonsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="2e22e-121">Record and post production output along with material and time consumption for a single released production order line.</span></span>|[<span data-ttu-id="2e22e-122">Bokfør forbruk og avgang for en frigitt produksjonsordrelinje</span><span class="sxs-lookup"><span data-stu-id="2e22e-122">Post Consumption and Output for One Released Production Order Line</span></span>](production-how-to-register-consumption-and-output.md)|  
|<span data-ttu-id="2e22e-123">Massebokfør antall komponenter som brukes per operasjon i en kladd som kan behandle flere planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e22e-123">Batch post the quantity of components used per operation in a journal that can processes multiple planned production orders.</span></span>|[<span data-ttu-id="2e22e-124">Massebokføre forbruk</span><span class="sxs-lookup"><span data-stu-id="2e22e-124">Batch Post Consumption</span></span>](production-how-to-post-consumption.md)|
|<span data-ttu-id="2e22e-125">Bokfør antall ferdigstilte varer og tiden som brukes per operasjon i en kladd som kan behandle flere frigitte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e22e-125">Post the quantity of finished items and the time spent per operation in a journal that can processes multiple released production orders.</span></span>|[<span data-ttu-id="2e22e-126">Bokføre avgang og operasjonstid</span><span class="sxs-lookup"><span data-stu-id="2e22e-126">Batch Post Output and Run Times</span></span>](production-how-to-post-output-quantity.md)|  
|<span data-ttu-id="2e22e-127">Bokføre antallet varer som er produsert i hver fullført operasjon, og som ikke kvalifiserer som ferdigvare, men som vraket materiale.</span><span class="sxs-lookup"><span data-stu-id="2e22e-127">Post the number of items produced in each finished operation which do not qualify as finished output, but as scrapped material.</span></span>|[<span data-ttu-id="2e22e-128">Bokføre vrak</span><span class="sxs-lookup"><span data-stu-id="2e22e-128">Post Scrap</span></span>](production-how-to-post-scrap.md)|
|<span data-ttu-id="2e22e-129">Vise belastningen for produksjonen som et resultat av planlagte og frigitte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2e22e-129">View the shop floor load as a result of planned and released production orders.</span></span>|[<span data-ttu-id="2e22e-130">Vise belastning på arbeidssentre og produksjonsressurser</span><span class="sxs-lookup"><span data-stu-id="2e22e-130">View the Load in Work and Machine Centers</span></span>](production-how-to-view-the-load-on-work-centers.md)|      
|<span data-ttu-id="2e22e-131">Bruke **Kapasitetskladd**-vinduet til å bokføre brukt kapasitet som ikke er tilordnet til en produksjonsordre, for eksempel vedlikeholdsarbeid.</span><span class="sxs-lookup"><span data-stu-id="2e22e-131">Use the **Capacity Journal** window to post consumed capacities that are not assigned to a production order, such as maintenance work.</span></span>|[<span data-ttu-id="2e22e-132">Bokføre kapasiteter</span><span class="sxs-lookup"><span data-stu-id="2e22e-132">Post Capacities</span></span>](production-how-to-post-capacities.md)|  
|<span data-ttu-id="2e22e-133">Beregne og justere kost for ferdige produksjonsvarer og forbrukte komponenter for økonomisk avstemming.</span><span class="sxs-lookup"><span data-stu-id="2e22e-133">Calculate and adjust the cost of finished production items and consumed components for financial reconciliation.</span></span>|[<span data-ttu-id="2e22e-134">Om fullførte produksjonsordrekostnader</span><span class="sxs-lookup"><span data-stu-id="2e22e-134">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a><span data-ttu-id="2e22e-135">Se også</span><span class="sxs-lookup"><span data-stu-id="2e22e-135">See Also</span></span>  
[<span data-ttu-id="2e22e-136">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="2e22e-136">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2e22e-137">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="2e22e-137">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="2e22e-138">Lager</span><span class="sxs-lookup"><span data-stu-id="2e22e-138">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2e22e-139">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2e22e-139">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2e22e-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e22e-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

