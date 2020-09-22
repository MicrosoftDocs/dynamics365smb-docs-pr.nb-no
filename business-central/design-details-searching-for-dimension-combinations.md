---
title: Designdetaljer – Søke etter dimensjonskombinasjoner | Microsoft-dokumentasjon
description: Når du lukker en side etter å ha redigert et sett med dimensjoner, undersøker Business Central om det redigerte settet med dimensjoner finnes. Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 962f7762db6cae08b2ac7080898df629015d79e7
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787188"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="3e102-104">Designdetaljer: Søke etter dimensjonskombinasjoner</span><span class="sxs-lookup"><span data-stu-id="3e102-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="3e102-105">Når du lukker en side etter å ha redigert et sett med dimensjoner, undersøker [!INCLUDE[d365fin](includes/d365fin_md.md)] om det redigerte settet med dimensjoner finnes.</span><span class="sxs-lookup"><span data-stu-id="3e102-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="3e102-106">Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert.</span><span class="sxs-lookup"><span data-stu-id="3e102-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="3e102-107">Bygge søketre</span><span class="sxs-lookup"><span data-stu-id="3e102-107">Building Search Tree</span></span>  
 <span data-ttu-id="3e102-108">Tabell 481 **Trenode for dimensjonssett** brukes når [!INCLUDE[d365fin](includes/d365fin_md.md)] vurderer om et sett med dimensjoner allerede finnes i tabell 480 **Dimensjonssettpost**.</span><span class="sxs-lookup"><span data-stu-id="3e102-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="3e102-109">Evalueringen utføres ved å traversere søketreet rekursivt fra det øverste nivået, som har fått nummeret 0.</span><span class="sxs-lookup"><span data-stu-id="3e102-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="3e102-110">Det øverste nivået 0 representerer et dimensjonssett uten dimensjonssettposter.</span><span class="sxs-lookup"><span data-stu-id="3e102-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="3e102-111">De underordnede elementene for dette dimensjonssettet representerer dimensjonssett med bare én dimensjonssettpost.</span><span class="sxs-lookup"><span data-stu-id="3e102-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="3e102-112">De underordnede elementene for disse dimensjonssettene representerer dimensjonssett med to underordnede elementer og så videre.</span><span class="sxs-lookup"><span data-stu-id="3e102-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="3e102-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="3e102-113">Example 1</span></span>  
 <span data-ttu-id="3e102-114">Diagrammet nedenfor representerer et søketre med seks dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="3e102-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="3e102-115">Bare den spesielle dimensjonssettposten vises i diagrammet.</span><span class="sxs-lookup"><span data-stu-id="3e102-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="3e102-116">![Eksempel på dimensjonstrestruktur](media/nav2013_dimension_tree.png "Eksempel på dimensjonstrestruktur")</span><span class="sxs-lookup"><span data-stu-id="3e102-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="3e102-117">Tabellen nedenfor beskriver en fullstendig liste over dimensjonssettpostene som utgjør hvert dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="3e102-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="3e102-118">Dimensjonssett</span><span class="sxs-lookup"><span data-stu-id="3e102-118">Dimension Sets</span></span>|<span data-ttu-id="3e102-119">Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="3e102-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="3e102-120">Sett 0</span><span class="sxs-lookup"><span data-stu-id="3e102-120">Set 0</span></span>|<span data-ttu-id="3e102-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e102-121">None</span></span>|  
|<span data-ttu-id="3e102-122">Sett 1</span><span class="sxs-lookup"><span data-stu-id="3e102-122">Set 1</span></span>|<span data-ttu-id="3e102-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="3e102-123">AREA 30</span></span>|  
|<span data-ttu-id="3e102-124">Sett 2</span><span class="sxs-lookup"><span data-stu-id="3e102-124">Set 2</span></span>|<span data-ttu-id="3e102-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="3e102-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="3e102-126">Sett 3</span><span class="sxs-lookup"><span data-stu-id="3e102-126">Set 3</span></span>|<span data-ttu-id="3e102-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="3e102-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="3e102-128">Sett 4</span><span class="sxs-lookup"><span data-stu-id="3e102-128">Set 4</span></span>|<span data-ttu-id="3e102-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="3e102-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="3e102-130">Sett 5</span><span class="sxs-lookup"><span data-stu-id="3e102-130">Set 5</span></span>|<span data-ttu-id="3e102-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="3e102-131">AREA 40</span></span>|  
|<span data-ttu-id="3e102-132">Sett 6</span><span class="sxs-lookup"><span data-stu-id="3e102-132">Set 6</span></span>|<span data-ttu-id="3e102-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="3e102-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="3e102-134">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="3e102-134">Example 2</span></span>  
 <span data-ttu-id="3e102-135">Dette eksemplet viser hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] vurderer om det finnes et dimensjonssett som består av dimensjonssettpostene AREA 40, DEPT PROD.</span><span class="sxs-lookup"><span data-stu-id="3e102-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="3e102-136">Først oppdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] også tabellen **Trenode for dimensjonssett** for å sikre at søketreet ser ut som diagrammet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3e102-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="3e102-137">Dimensjonssett 7 blir dermed underordnet dimensjonssett 5.</span><span class="sxs-lookup"><span data-stu-id="3e102-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="3e102-138">![Eksempel på dimensjonstrestruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Eksempel på dimensjonstrestruktur i NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="3e102-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="3e102-139">Finne dimensjonssett-ID</span><span class="sxs-lookup"><span data-stu-id="3e102-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="3e102-140">På et grunnleggende nivå vil **Overordnet ID**, **Dimensjon** og **Dimensjonsverdi** i søketreet, kombineres og brukes som primærnøkkel fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] går gjennom treet i samme rekkefølge som dimensjonspostene.</span><span class="sxs-lookup"><span data-stu-id="3e102-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="3e102-141">GET-funksjonen (post) brukes til å søke etter dimensjonssett-ID.</span><span class="sxs-lookup"><span data-stu-id="3e102-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="3e102-142">Følgende kodeeksempel viser hvordan du finner dimensjonssett-IDen når det finnes tre dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="3e102-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="3e102-143">For å beholde muligheten for [!INCLUDE[d365fin](includes/d365fin_md.md)] til å gi nytt navn til både en dimensjon og en dimensjonsverdi, utvides imidlertid tabell 349, **Dimensjonsverdi**, med et heltallsfelt, **Dimensjonsverdi-ID**.</span><span class="sxs-lookup"><span data-stu-id="3e102-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="3e102-144">Denne tabellen konverterer feltparet, **Dimensjon** og **Dimensjonsverdi**, til en heltallsverdi.</span><span class="sxs-lookup"><span data-stu-id="3e102-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="3e102-145">Når du gir dimensjonen og dimensjonsverdien nytt navn, endres ikke heltallsverdien.</span><span class="sxs-lookup"><span data-stu-id="3e102-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="3e102-146">Se også</span><span class="sxs-lookup"><span data-stu-id="3e102-146">See Also</span></span>  
 <span data-ttu-id="3e102-147">[GET-funksjonen (post)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="3e102-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="3e102-148">[Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="3e102-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="3e102-149">[Dimensjonssettposter – oversikt](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="3e102-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="3e102-150">Designdetaljer: Tabellstruktur</span><span class="sxs-lookup"><span data-stu-id="3e102-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
