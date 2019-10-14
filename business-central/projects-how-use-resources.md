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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8d637a21a795db46554a45c688bf7ad081533e4a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312703"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="d0b65-103">Bruke ressurser for prosjekter</span><span class="sxs-lookup"><span data-stu-id="d0b65-103">Use Resources for Jobs</span></span>
<span data-ttu-id="d0b65-104">Du registrerer ressursforbruket i prosjektkladden for å holde oversikt over kostnader, priser og arbeidstypene som er knyttet til prosjekter.</span><span class="sxs-lookup"><span data-stu-id="d0b65-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="d0b65-105">Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="d0b65-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="d0b65-106">Du kan også bokføre ressursforbruket i en ressurskladd.</span><span class="sxs-lookup"><span data-stu-id="d0b65-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="d0b65-107">Poster som er bokført i en ressurskladd, har ingen innvirkning på Finans.</span><span class="sxs-lookup"><span data-stu-id="d0b65-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="d0b65-108">Slik tilordner du ressurser til prosjekter</span><span class="sxs-lookup"><span data-stu-id="d0b65-108">To assign resources to jobs</span></span>
<span data-ttu-id="d0b65-109">Du kan tilordne ressurser til prosjekter ved å opprette prosjektplanleggingslinjer for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d0b65-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="d0b65-110">Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="d0b65-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="d0b65-111">Slik registrerer du ressursforbruk for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="d0b65-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="d0b65-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0b65-113">Åpne en relevant prosjektkladd, og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d0b65-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d0b65-114">Når kladden er fullført, kan du velge handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="d0b65-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="d0b65-115">Slik justerer du ressurspriser</span><span class="sxs-lookup"><span data-stu-id="d0b65-115">To adjust resource prices</span></span>
<span data-ttu-id="d0b65-116">Hvis du vil endre kost- eller salgspriser for en rekke ressurser, kan du bruke en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="d0b65-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="d0b65-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **uster ressurskost/priser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0b65-118">Fyll ut feltene på en linje etter behov, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0b65-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d0b65-119">Denne kjørselen verken oppretter eller justerer alternative kostnader eller priser for ressurser.</span><span class="sxs-lookup"><span data-stu-id="d0b65-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="d0b65-120">Den endrer bare innholdet i feltet på ressurskortet for **Juster felt**-feltet som du valgte i kjørselen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="d0b65-121">Justeringen vil tre i kraft umiddelbart for ressurser, så kontroller justeringsfaktorene før du kjører den satsvise jobben.</span><span class="sxs-lookup"><span data-stu-id="d0b65-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="d0b65-122">Slik får du forslag til ressursprisendringer på bakgrunn av eksisterende alternative priser</span><span class="sxs-lookup"><span data-stu-id="d0b65-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="d0b65-123">Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.</span><span class="sxs-lookup"><span data-stu-id="d0b65-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="d0b65-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0b65-125">Velg handlingen **Foreslå ress.prisendr. (pris)** og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d0b65-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="d0b65-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0b65-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="d0b65-127">Når kjørselen er ferdig, viser siden **Ressursprisendringer** resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-127">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="d0b65-128">Slik får du forslag til ressursprisendringer på bakgrunn av standardpriser</span><span class="sxs-lookup"><span data-stu-id="d0b65-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="d0b65-129">Hvis du vil definere flere alternative ressurspriser på bakgrunn av standardprisene på ressurskortene, kan du bruke en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="d0b65-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="d0b65-130">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0b65-131">Velg handlingen **Foreslå ress.prisendr. (ress.)** og fyll deretter ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d0b65-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="d0b65-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0b65-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="d0b65-133">Når kjørselen er ferdig, åpner du siden **Ressursprisendringer** for å se resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-133">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="d0b65-134">Slik får du forslag til ressursprisendringer på bakgrunn av alternative priser</span><span class="sxs-lookup"><span data-stu-id="d0b65-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="d0b65-135">Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.</span><span class="sxs-lookup"><span data-stu-id="d0b65-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="d0b65-136">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Foreslå ress.prisendr. (pris)**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d0b65-137">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d0b65-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="d0b65-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0b65-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="d0b65-139">Når kjørselen er ferdig, åpner du siden **Ressursprisendringer** for å se resultatene av kjørselen.</span><span class="sxs-lookup"><span data-stu-id="d0b65-139">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0b65-140">Se også</span><span class="sxs-lookup"><span data-stu-id="d0b65-140">See Also</span></span>
[<span data-ttu-id="d0b65-141">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="d0b65-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d0b65-142">Finans</span><span class="sxs-lookup"><span data-stu-id="d0b65-142">Finance</span></span>](finance.md)  
<span data-ttu-id="d0b65-143">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d0b65-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d0b65-144">[Salg](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="d0b65-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="d0b65-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0b65-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
