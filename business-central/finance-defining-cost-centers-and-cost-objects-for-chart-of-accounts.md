---
title: Definere kostsentre og kostobjekter for kontoplanen | Microsoft-dokumentasjon
description: Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel. Når du foretar overføringen, overfører systemet bare postene som allerede er koblet til et kostsenter eller et kostobjekt. Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 1a9178f80f6c16659509f1ae22b9225b1b6d2f70
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302431"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="8646b-105">Definere kostsentre og kostobjekter for kontoplanen</span><span class="sxs-lookup"><span data-stu-id="8646b-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="8646b-106">Du kan automatisk overføre utgifts- og inntektspostene fra finans til kostregnskap enten for hver finansbokføring eller sammen med en kjørsel.</span><span class="sxs-lookup"><span data-stu-id="8646b-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="8646b-107">Når du foretar overføringen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bare postene som allerede er koblet til et kostsenter eller et kostobjekt.</span><span class="sxs-lookup"><span data-stu-id="8646b-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="8646b-108">Hvis du vil opprette en meningsfull overføring, må du kontrollere at kostsentre og kostobjekter er riktig definert.</span><span class="sxs-lookup"><span data-stu-id="8646b-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="8646b-109">Definere standard dimensjonsverdier for finanskontoer</span><span class="sxs-lookup"><span data-stu-id="8646b-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="8646b-110">For hver finanskonto kan du definere standarddimensjonsverdier i **Standarddimensjon**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="8646b-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="8646b-111">Eksempelet nedenfor viser hvordan du definerer at det alltid skal finnes et kostsenter for AVDELING, men aldri et kostobjekt for PROSJEKT, ved bokføring til en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="8646b-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="8646b-112">**Dimensjonskode**</span><span class="sxs-lookup"><span data-stu-id="8646b-112">**Dimension Code**</span></span>|<span data-ttu-id="8646b-113">**Verdibokføring**</span><span class="sxs-lookup"><span data-stu-id="8646b-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="8646b-114">Avdeling</span><span class="sxs-lookup"><span data-stu-id="8646b-114">Department</span></span>|<span data-ttu-id="8646b-115">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8646b-115">Code Mandatory</span></span>|  
|<span data-ttu-id="8646b-116">Prosjekt</span><span class="sxs-lookup"><span data-stu-id="8646b-116">Project</span></span>|<span data-ttu-id="8646b-117">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8646b-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="8646b-118">Definere dimensjonsverdier for indirekte kostnader og direkte kostnader</span><span class="sxs-lookup"><span data-stu-id="8646b-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="8646b-119">Du kan overføre indirekte kostnader til et kostsenter og direkte kostnader til et kostobjekt.</span><span class="sxs-lookup"><span data-stu-id="8646b-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="8646b-120">Følgende tabell viser den optimale kombinasjonen av dimensjonsoppsettsverdier.</span><span class="sxs-lookup"><span data-stu-id="8646b-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="8646b-121">Overfør til</span><span class="sxs-lookup"><span data-stu-id="8646b-121">Transfer To</span></span>|<span data-ttu-id="8646b-122">Kostsenterbokføring</span><span class="sxs-lookup"><span data-stu-id="8646b-122">Cost Center Posting</span></span>|<span data-ttu-id="8646b-123">Bokføring av kostobjekt</span><span class="sxs-lookup"><span data-stu-id="8646b-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="8646b-124">Kostsenter</span><span class="sxs-lookup"><span data-stu-id="8646b-124">Cost Center</span></span>|<span data-ttu-id="8646b-125">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8646b-125">Code Mandatory</span></span>|<span data-ttu-id="8646b-126">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8646b-126">No Code</span></span>|  
|<span data-ttu-id="8646b-127">Kostobjekt</span><span class="sxs-lookup"><span data-stu-id="8646b-127">Cost Object</span></span>|<span data-ttu-id="8646b-128">Ingen kode</span><span class="sxs-lookup"><span data-stu-id="8646b-128">No Code</span></span>|<span data-ttu-id="8646b-129">Obligatorisk kode</span><span class="sxs-lookup"><span data-stu-id="8646b-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="8646b-130">For å sørge for at det forhåndsdefinerte kostsenteret og kostobjekt som du setter opp i finans, overføres automatisk til kostregnskapet, kan du merke av for **Kontroller finansbokføringer** på siden Kostregnskapsoppsett.</span><span class="sxs-lookup"><span data-stu-id="8646b-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8646b-131">Se også</span><span class="sxs-lookup"><span data-stu-id="8646b-131">See Also</span></span>  
[<span data-ttu-id="8646b-132">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="8646b-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="8646b-133">Definere kostregnskap</span><span class="sxs-lookup"><span data-stu-id="8646b-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="8646b-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8646b-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
