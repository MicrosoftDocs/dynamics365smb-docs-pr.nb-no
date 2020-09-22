---
title: Dimensjonssettposter – oversikt | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b9b69b539228e92776e1a7ee4c2fb491b20c1a15
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787999"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="addff-103">Dimensjonssettposter – oversikt</span><span class="sxs-lookup"><span data-stu-id="addff-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="addff-104">Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="addff-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="addff-105">Dimensjonssett</span><span class="sxs-lookup"><span data-stu-id="addff-105">Dimension Sets</span></span>  
<span data-ttu-id="addff-106">Et dimensjonssett er en unik kombinasjon av dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="addff-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="addff-107">Det lagres som dimensjonssettposter i databasen.</span><span class="sxs-lookup"><span data-stu-id="addff-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="addff-108">Hver dimensjonssettpost representerer én enkelt dimensjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="addff-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="addff-109">Dimensjonssettet identifiseres av en felles dimensjonssett-ID som tilordnes hver dimensjonssettpost som tilhører dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="addff-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="addff-110">Eksempelet nedenfor viser et dimensjonssett som har tre dimensjonssettposter.</span><span class="sxs-lookup"><span data-stu-id="addff-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="addff-111">Dimensjonssettet identifiseres av en dimensjonssett-ID, som er 108.</span><span class="sxs-lookup"><span data-stu-id="addff-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="addff-112">Dimensjonssett-ID</span><span class="sxs-lookup"><span data-stu-id="addff-112">Dimension Set ID</span></span>|<span data-ttu-id="addff-113">Dimensjonskode</span><span class="sxs-lookup"><span data-stu-id="addff-113">Dimension Code</span></span>|<span data-ttu-id="addff-114">Dimensjonsverdikode</span><span class="sxs-lookup"><span data-stu-id="addff-114">Dimension Value Code</span></span>|<span data-ttu-id="addff-115">Navn på dimensjonsverdi</span><span class="sxs-lookup"><span data-stu-id="addff-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="addff-116">108</span><span class="sxs-lookup"><span data-stu-id="addff-116">108</span></span>|<span data-ttu-id="addff-117">OMRÅDE</span><span class="sxs-lookup"><span data-stu-id="addff-117">AREA</span></span>|<span data-ttu-id="addff-118">70</span><span class="sxs-lookup"><span data-stu-id="addff-118">70</span></span>|<span data-ttu-id="addff-119">Amerika – nord</span><span class="sxs-lookup"><span data-stu-id="addff-119">America North</span></span>|  
|<span data-ttu-id="addff-120">108</span><span class="sxs-lookup"><span data-stu-id="addff-120">108</span></span>|<span data-ttu-id="addff-121">FIRMATYPE</span><span class="sxs-lookup"><span data-stu-id="addff-121">BUSINESSGROUP</span></span>|<span data-ttu-id="addff-122">HOME</span><span class="sxs-lookup"><span data-stu-id="addff-122">HOME</span></span>|<span data-ttu-id="addff-123">Hjem</span><span class="sxs-lookup"><span data-stu-id="addff-123">Home</span></span>|  
|<span data-ttu-id="addff-124">108</span><span class="sxs-lookup"><span data-stu-id="addff-124">108</span></span>|<span data-ttu-id="addff-125">AVDELING</span><span class="sxs-lookup"><span data-stu-id="addff-125">DEPARTMENT</span></span>|<span data-ttu-id="addff-126">SALG</span><span class="sxs-lookup"><span data-stu-id="addff-126">SALES</span></span>|<span data-ttu-id="addff-127">Salg</span><span class="sxs-lookup"><span data-stu-id="addff-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="addff-128">Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="addff-128">Dimension Set Entries</span></span>  
<span data-ttu-id="addff-129">Dimensjonssett lagres i tabellen med **Dimensjonssettpost** som dimensjonssettposter med samme ID for dimensjonssett.</span><span class="sxs-lookup"><span data-stu-id="addff-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="addff-130">![Flyt for dimensjonssettposter](media/dimensionentrynav7.png "Flyt for dimensjonssettposter")</span><span class="sxs-lookup"><span data-stu-id="addff-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="addff-131">Når du oppretter en ny kladdelinje, et nytt dokumenthode eller en ny dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="addff-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="addff-132">I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="addff-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="addff-133">Når du redigerer og lukker siden **Rediger dimensjonssettposter**, blir det utført en kontroll for å se om kombinasjonen av dimensjonsverdier eksisterer som et dimensjonssett i tabellen.</span><span class="sxs-lookup"><span data-stu-id="addff-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="addff-134">Hvis kombinasjonen forekommer i tabellen, tilordnes den tilsvarende dimensjonssett-IDen til kladdelinjen, dokumenthodet eller dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="addff-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="addff-135">Ellers legges et nytt dimensjonssett til i tabellen, og den nye dimensjonssett-IDen tilordnes til kladdelinjen, dokumenthodet eller dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="addff-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="addff-136">Dimensjonsbehandling for codeunit 408</span><span class="sxs-lookup"><span data-stu-id="addff-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="addff-137">Codeunit 408, dimensjonsbehandling, er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet.</span><span class="sxs-lookup"><span data-stu-id="addff-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="addff-138">Ytelsesforbedring</span><span class="sxs-lookup"><span data-stu-id="addff-138">Performance Improvement</span></span>  
<span data-ttu-id="addff-139">Ved å lagre dimensjonssett én gang i databasen beholdes databaseplassen, og den generelle ytelsen blir forbedret.</span><span class="sxs-lookup"><span data-stu-id="addff-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="addff-140">Se også</span><span class="sxs-lookup"><span data-stu-id="addff-140">See Also</span></span>  
<span data-ttu-id="addff-141">[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="addff-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="addff-142">[Designdetaljer: Tabellstruktur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="addff-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="addff-143">Designdetaljer: Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="addff-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   
