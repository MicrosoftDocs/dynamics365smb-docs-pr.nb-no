---
title: "Dimensjonssettposter – oversikt | Microsoft-dokumentasjon"
description: "Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 78e98bcbc88ffb38d5da3f5089d124d915585d91
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="2af16-103">Dimensjonssettposter – oversikt</span><span class="sxs-lookup"><span data-stu-id="2af16-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="2af16-104">Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2af16-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
## <a name="dimension-sets"></a><span data-ttu-id="2af16-105">Dimensjonssett</span><span class="sxs-lookup"><span data-stu-id="2af16-105">Dimension Sets</span></span>  
<span data-ttu-id="2af16-106">Et dimensjonssett er en unik kombinasjon av dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="2af16-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="2af16-107">Det lagres som dimensjonssettposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="2af16-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="2af16-108">Hver dimensjonssettpost representerer én enkelt dimensjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="2af16-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="2af16-109">Dimensjonssettet identifiseres av en felles dimensjonssett-ID som tilordnes hver dimensjonssettpost som tilhører dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="2af16-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  
  
<span data-ttu-id="2af16-110">Eksempelet nedenfor viser et dimensjonssett som har tre dimensjonssettposter.</span><span class="sxs-lookup"><span data-stu-id="2af16-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="2af16-111">Dimensjonssettet identifiseres av en dimensjonssett-ID, som er 108.</span><span class="sxs-lookup"><span data-stu-id="2af16-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  
  
|<span data-ttu-id="2af16-112">Dimensjonssett-ID</span><span class="sxs-lookup"><span data-stu-id="2af16-112">Dimension Set ID</span></span>|<span data-ttu-id="2af16-113">Dimensjonskode</span><span class="sxs-lookup"><span data-stu-id="2af16-113">Dimension Code</span></span>|<span data-ttu-id="2af16-114">Dimensjonsverdikode</span><span class="sxs-lookup"><span data-stu-id="2af16-114">Dimension Value Code</span></span>|<span data-ttu-id="2af16-115">Navn på dimensjonsverdi</span><span class="sxs-lookup"><span data-stu-id="2af16-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="2af16-116">108</span><span class="sxs-lookup"><span data-stu-id="2af16-116">108</span></span>|<span data-ttu-id="2af16-117">OMRÅDE</span><span class="sxs-lookup"><span data-stu-id="2af16-117">AREA</span></span>|<span data-ttu-id="2af16-118">70</span><span class="sxs-lookup"><span data-stu-id="2af16-118">70</span></span>|<span data-ttu-id="2af16-119">Amerika – nord</span><span class="sxs-lookup"><span data-stu-id="2af16-119">America North</span></span>|  
|<span data-ttu-id="2af16-120">108</span><span class="sxs-lookup"><span data-stu-id="2af16-120">108</span></span>|<span data-ttu-id="2af16-121">FIRMATYPE</span><span class="sxs-lookup"><span data-stu-id="2af16-121">BUSINESSGROUP</span></span>|<span data-ttu-id="2af16-122">HOME</span><span class="sxs-lookup"><span data-stu-id="2af16-122">HOME</span></span>|<span data-ttu-id="2af16-123">Hjem</span><span class="sxs-lookup"><span data-stu-id="2af16-123">Home</span></span>|  
|<span data-ttu-id="2af16-124">108</span><span class="sxs-lookup"><span data-stu-id="2af16-124">108</span></span>|<span data-ttu-id="2af16-125">AVDELING</span><span class="sxs-lookup"><span data-stu-id="2af16-125">DEPARTMENT</span></span>|<span data-ttu-id="2af16-126">SALG</span><span class="sxs-lookup"><span data-stu-id="2af16-126">SALES</span></span>|<span data-ttu-id="2af16-127">Salg</span><span class="sxs-lookup"><span data-stu-id="2af16-127">Sales</span></span>|  
  
## <a name="dimension-set-entries"></a><span data-ttu-id="2af16-128">Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="2af16-128">Dimension Set Entries</span></span>  
<span data-ttu-id="2af16-129">Dimensjonssett lagres i tabellen med **Dimensjonssettpost** som dimensjonssettposter med samme ID for dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="2af16-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  
  
<span data-ttu-id="2af16-130">![Oversikt over dimensjonspost](media/dimensionentrynav7.png "DimensionEntryNAV7")</span><span class="sxs-lookup"><span data-stu-id="2af16-130">![Dimension Entry overview](media/dimensionentrynav7.png "DimensionEntryNAV7")</span></span>  
  
<span data-ttu-id="2af16-131">Når du oppretter en ny kladdelinje, et nytt dokumenthode eller en ny dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="2af16-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="2af16-132">I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="2af16-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  
  
<span data-ttu-id="2af16-133">Når du redigerer og lukker vinduet **Rediger dimensjonssettposter**, blir det utført en kontroll for å se om kombinasjonen av dimensjonsverdier eksisterer som et dimensjonssett i tabellen.</span><span class="sxs-lookup"><span data-stu-id="2af16-133">When you edit and close the **Edit Dimension Set Entries** window, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="2af16-134">Hvis kombinasjonen forekommer i tabellen, tilordnes den tilsvarende dimensjonssett-IDen til kladdelinjen, dokumenthodet eller dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="2af16-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="2af16-135">Ellers legges et nytt dimensjonssett til i tabellen, og den nye dimensjonssett-IDen tilordnes til kladdelinjen, dokumenthodet eller dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="2af16-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>  
  
## <a name="performance-improvement"></a><span data-ttu-id="2af16-136">Ytelsesforbedring</span><span class="sxs-lookup"><span data-stu-id="2af16-136">Performance Improvement</span></span>  
<span data-ttu-id="2af16-137">Ved å lagre dimensjonssett én gang i databasen beholdes databaseplassen, og den generelle ytelsen blir forbedret.</span><span class="sxs-lookup"><span data-stu-id="2af16-137">By storing dimension sets once in the database, database space is preserved, and overall performance is improved.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2af16-138">Se også</span><span class="sxs-lookup"><span data-stu-id="2af16-138">See Also</span></span>  
<span data-ttu-id="2af16-139">[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="2af16-139">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="2af16-140">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="2af16-140">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
<span data-ttu-id="2af16-141">[Designdetaljer: Dimensjonsbehandling for kodeenhet 408](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="2af16-141">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
<span data-ttu-id="2af16-142">[Designdetaljer: Kodeeksempler på endrede mønstre i endringer](design-details-code-examples-of-changed-patterns-in-modifications.md) </span><span class="sxs-lookup"><span data-stu-id="2af16-142">[Design Details: Code Examples of Changed Patterns in Modifications](design-details-code-examples-of-changed-patterns-in-modifications.md) </span></span>  
[<span data-ttu-id="2af16-143">Designdetaljer: Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="2af16-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   

