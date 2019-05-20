---
title: Definere lagerverdisetting og kostberegning | Microsoft-dokumentasjon
description: Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 184c7651fe8db60b55bd161bb5dc870df1ed01c5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241941"
---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="e23ec-103">Definere lagerverdisetting og kostberegning</span><span class="sxs-lookup"><span data-stu-id="e23ec-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="e23ec-104">For å sikre at lagerkost registreres riktig, må du definere ulike felt og sider før du begynner å opprette varetransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e23ec-104">To make sure that inventory costs are recorded correctly, you must set up various fields and pages before you begin to make item transactions.</span></span>

<span data-ttu-id="e23ec-105">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="e23ec-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="e23ec-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="e23ec-106">**To**</span></span>|<span data-ttu-id="e23ec-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="e23ec-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e23ec-108">Angi en lagermetode for hver vare for å styre hvordan innkommende kost brukes til å vurdere lagerverdi og solgte varers kost.</span><span class="sxs-lookup"><span data-stu-id="e23ec-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="e23ec-109">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="e23ec-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="e23ec-110">Sikre at kost automatisk bokføres mot Finans når en lagertransaksjons bokføres.</span><span class="sxs-lookup"><span data-stu-id="e23ec-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="e23ec-111">Feltet **Automatisk kostbokføring** på siden **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="e23ec-111">**Automatic Cost Posting** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e23ec-112">Sikre at forventet kost bokføres mot Finans for å se en beregning av skyldige beløp og solgte varers kost i midlertidige finanskonti før de faktisk faktureres.</span><span class="sxs-lookup"><span data-stu-id="e23ec-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="e23ec-113">Feltet **Bokf. av forventet kost i Finans** på siden **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="e23ec-113">**Expected Cost Posting to G/L** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e23ec-114">Definere at systemet skal justeres automatisk for eventuelle kostendringer hver gang du bokfører lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e23ec-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="e23ec-115">Justere varekost</span><span class="sxs-lookup"><span data-stu-id="e23ec-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="e23ec-116">Definere om gjennomsnittlig kost skal beregnes bare per vare, eller per vare for hver lagerføringsenhet og hver variant av varen.</span><span class="sxs-lookup"><span data-stu-id="e23ec-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="e23ec-117">Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="e23ec-117">**Average Cost Calc. Type** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e23ec-118">Velge hvilken tidsperiode du vil bruke til å beregne vektet gjennomsnittlig kost for varer som bruker lagermetoden Gjennomsnitt.</span><span class="sxs-lookup"><span data-stu-id="e23ec-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="e23ec-119">Feltet **Gjennomsnittskostperiode** på siden **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="e23ec-119">**Average Cost Period** field on the **Inventory Setup** page</span></span>|  
|<span data-ttu-id="e23ec-120">Definere lagerperioder for å kontrollere lagerverdi over tid ved å forby transaksjonsbokføring i lukkede lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="e23ec-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="e23ec-121">Arbeide med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="e23ec-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="e23ec-122">Sikre at salgsreturer utlignes mot den opprinnelige utgående transaksjonen for å opprettholde lagerverdi.</span><span class="sxs-lookup"><span data-stu-id="e23ec-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="e23ec-123">Feltet **Bruk opprinnelig kostpris** på siden **Salg**</span><span class="sxs-lookup"><span data-stu-id="e23ec-123">**Exact Cost Reversing Mandatory** field on the **Sales & Receivables** page</span></span>|  
|<span data-ttu-id="e23ec-124">Sikre at kjøpsreturer utlignes mot den opprinnelige inngående transaksjonen for å opprettholde lagerverdi.</span><span class="sxs-lookup"><span data-stu-id="e23ec-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="e23ec-125">Feltet **Bruk opprinnelig kostpris** på siden **Kjøp**</span><span class="sxs-lookup"><span data-stu-id="e23ec-125">**Exact Cost Reversing Mandatory** field on the **´Purchases & Payables** page</span></span>|
|<span data-ttu-id="e23ec-126">Definere avrundingsreglene som skal brukes ved justering av eller forslag om varepriser, og når standardkost skal justeres eller foreslås.</span><span class="sxs-lookup"><span data-stu-id="e23ec-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="e23ec-127">Siden **Avrundingsmetode**</span><span class="sxs-lookup"><span data-stu-id="e23ec-127">**Rounding Method** page</span></span>|  

## <a name="see-also"></a><span data-ttu-id="e23ec-128">Se også</span><span class="sxs-lookup"><span data-stu-id="e23ec-128">See Also</span></span>  
[<span data-ttu-id="e23ec-129">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="e23ec-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="e23ec-130">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="e23ec-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="e23ec-131">Finans</span><span class="sxs-lookup"><span data-stu-id="e23ec-131">Finance</span></span>](finance.md)  
