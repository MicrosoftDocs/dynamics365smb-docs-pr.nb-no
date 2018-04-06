---
title: Definere kostsentre og kostobjekter for kontoplanen | Microsoft-dokumentasjon
description: "Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel. Når du foretar overføringen, overfører systemet bare postene som allerede er koblet til et kostsenter eller et kostobjekt. Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert."
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
ms.openlocfilehash: 92ad393733c758304743ec0b63c98c1612e7240b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="8847a-105">Definere kostsentre og kostobjekter for kontoplanen</span><span class="sxs-lookup"><span data-stu-id="8847a-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="8847a-106">Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="8847a-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="8847a-107">Når du foretar overføringen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bare postene som allerede er koblet til et kostsenter eller et kostobjekt.</span><span class="sxs-lookup"><span data-stu-id="8847a-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="8847a-108">Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert.</span><span class="sxs-lookup"><span data-stu-id="8847a-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="8847a-109">Definere standard dimensjonsverdier for finanskontoer</span><span class="sxs-lookup"><span data-stu-id="8847a-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="8847a-110">For hver finanskonto kan du definere standarddimensjonsverdier i **Standarddimensjon**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="8847a-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="8847a-111">Eksempelet nedenfor viser hvordan du definerer at det alltid skal finnes et kostsenter for AVDELING, men aldri et kostobjekt for PROSJEKT, ved bokføring til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="8847a-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="8847a-112">**Dimensjonskode**</span><span class="sxs-lookup"><span data-stu-id="8847a-112">**Dimension Code**</span></span>|<span data-ttu-id="8847a-113">**Verdibokføring**</span><span class="sxs-lookup"><span data-stu-id="8847a-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="8847a-114">Avdeling</span><span class="sxs-lookup"><span data-stu-id="8847a-114">Department</span></span>|<span data-ttu-id="8847a-115">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8847a-115">Code Mandatory</span></span>|  
|<span data-ttu-id="8847a-116">Prosjekt</span><span class="sxs-lookup"><span data-stu-id="8847a-116">Project</span></span>|<span data-ttu-id="8847a-117">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8847a-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="8847a-118">Definere dimensjonsverdier for indirekte kostnader og direkte kostnader</span><span class="sxs-lookup"><span data-stu-id="8847a-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="8847a-119">Du kan overføre indirekte kostnader til et kostsenter og direkte kostnader til et kostobjekt.</span><span class="sxs-lookup"><span data-stu-id="8847a-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="8847a-120">Følgende tabell viser den optimale kombinasjonen av dimensjonsoppsettsverdier.</span><span class="sxs-lookup"><span data-stu-id="8847a-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="8847a-121">Overfør til</span><span class="sxs-lookup"><span data-stu-id="8847a-121">Transfer To</span></span>|<span data-ttu-id="8847a-122">Kostsenterbokføring</span><span class="sxs-lookup"><span data-stu-id="8847a-122">Cost Center Posting</span></span>|<span data-ttu-id="8847a-123">Bokføring av kostobjekt</span><span class="sxs-lookup"><span data-stu-id="8847a-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="8847a-124">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="8847a-124">Cost Center</span></span>|<span data-ttu-id="8847a-125">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8847a-125">Code Mandatory</span></span>|<span data-ttu-id="8847a-126">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8847a-126">No Code</span></span>|  
|<span data-ttu-id="8847a-127">Kostobjekt</span><span class="sxs-lookup"><span data-stu-id="8847a-127">Cost Object</span></span>|<span data-ttu-id="8847a-128">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8847a-128">No Code</span></span>|<span data-ttu-id="8847a-129">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8847a-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="8847a-130">For å sørge for at det forhåndsdefinerte kostsenteret og kostobjekt som du setter opp i finans, overføres automatisk til kostregnskapet, kan du merke av for **Kontroller finansbokføringer** i vinduet Kostregnskapsoppsett.</span><span class="sxs-lookup"><span data-stu-id="8847a-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8847a-131">Se også</span><span class="sxs-lookup"><span data-stu-id="8847a-131">See Also</span></span>  
[<span data-ttu-id="8847a-132">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="8847a-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="8847a-133">[Definere kostsentre](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="8847a-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="8847a-134">Definere kostobjekter</span><span class="sxs-lookup"><span data-stu-id="8847a-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="8847a-135">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8847a-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

