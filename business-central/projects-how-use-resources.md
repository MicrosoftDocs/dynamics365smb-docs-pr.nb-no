---
title: Registrere og justere ressursforbruk og priser | Microsoft-dokumentasjon
description: Beskriver hvordan du kan registrere ressursforbruket eller forbruket som er knyttet til et prosjekt, for å holde rede på og håndtere kostnader, priser og arbeidstyper.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc51b47b71d37daaccc4133d648c90b84d5a3494
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251748"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="e92fd-103">Bruke ressurser for prosjekter</span><span class="sxs-lookup"><span data-stu-id="e92fd-103">Use Resources for Jobs</span></span>
<span data-ttu-id="e92fd-104">Du registrerer ressursforbruket i prosjektkladden for å holde oversikt over kostnader, priser og arbeidstypene som er knyttet til prosjekter.</span><span class="sxs-lookup"><span data-stu-id="e92fd-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="e92fd-105">Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="e92fd-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="e92fd-106">Du kan også bokføre ressursforbruket i en ressurskladd.</span><span class="sxs-lookup"><span data-stu-id="e92fd-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="e92fd-107">Poster som er bokført i en ressurskladd, har ingen innvirkning på Finans.</span><span class="sxs-lookup"><span data-stu-id="e92fd-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="e92fd-108">Slik tilordner du ressurser til prosjekter</span><span class="sxs-lookup"><span data-stu-id="e92fd-108">To assign resources to jobs</span></span>
<span data-ttu-id="e92fd-109">Du kan tilordne ressurser til prosjekter ved å opprette prosjektplanleggingslinjer for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e92fd-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="e92fd-110">Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="e92fd-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="e92fd-111">Slik registrerer du ressursforbruk for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="e92fd-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="e92fd-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e92fd-113">Åpne en relevant prosjektkladd, og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e92fd-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="e92fd-114">Når kladden er fullført, kan du velge handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="e92fd-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="e92fd-115">Slik justerer du ressurspriser</span><span class="sxs-lookup"><span data-stu-id="e92fd-115">To adjust resource prices</span></span>
<span data-ttu-id="e92fd-116">Hvis du vil endre kost- eller salgspriser for en rekke ressurser, kan du bruke en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="e92fd-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="e92fd-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **uster ressurskost/priser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="e92fd-118">Fyll ut feltene på en linje etter behov, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e92fd-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e92fd-119">Denne kjørselen verken oppretter eller justerer alternative kostnader eller priser for ressurser.</span><span class="sxs-lookup"><span data-stu-id="e92fd-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="e92fd-120">Den endrer bare innholdet i feltet på ressurskortet for **Juster felt**-feltet som du valgte i kjørselen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="e92fd-121">Justeringen vil tre i kraft umiddelbart for ressurser, så kontroller justeringsfaktorene før du kjører den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="e92fd-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="e92fd-122">Slik får du forslag til ressursprisendringer på bakgrunn av eksisterende alternative priser</span><span class="sxs-lookup"><span data-stu-id="e92fd-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="e92fd-123">Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.</span><span class="sxs-lookup"><span data-stu-id="e92fd-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="e92fd-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e92fd-125">Velg handlingen **Foreslå ress.prisendr. (pris)** og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e92fd-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e92fd-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e92fd-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e92fd-127">Når kjørselen er ferdig, viser siden **Ressursprisendringer** resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-127">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="e92fd-128">Slik får du forslag til ressursprisendringer på bakgrunn av standardpriser</span><span class="sxs-lookup"><span data-stu-id="e92fd-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="e92fd-129">Hvis du vil definere flere alternative ressurspriser på bakgrunn av standardprisene på ressurskortene, kan du bruke en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="e92fd-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="e92fd-130">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="e92fd-131">Velg handlingen **Foreslå ress.prisendr. (ress.)** og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e92fd-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="e92fd-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e92fd-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e92fd-133">Når kjørselen er ferdig, åpner du siden **Ressursprisendringer** for å se resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-133">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="e92fd-134">Slik får du forslag til ressursprisendringer på bakgrunn av alternative priser</span><span class="sxs-lookup"><span data-stu-id="e92fd-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="e92fd-135">Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.</span><span class="sxs-lookup"><span data-stu-id="e92fd-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="e92fd-136">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Foreslå ress.prisendr. (pris)**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e92fd-137">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e92fd-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e92fd-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e92fd-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="e92fd-139">Når kjørselen er ferdig, åpner du siden **Ressursprisendringer** for å se resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="e92fd-139">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="e92fd-140">Se også</span><span class="sxs-lookup"><span data-stu-id="e92fd-140">See Also</span></span>
[<span data-ttu-id="e92fd-141">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="e92fd-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="e92fd-142">Finans</span><span class="sxs-lookup"><span data-stu-id="e92fd-142">Finance</span></span>](finance.md)  
<span data-ttu-id="e92fd-143">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="e92fd-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="e92fd-144">[Salg](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="e92fd-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="e92fd-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e92fd-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
