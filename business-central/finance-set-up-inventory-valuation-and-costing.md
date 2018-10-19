---
title: Definere lagerverdisetting og kostberegning | Microsoft-dokumentasjon
description: Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="b4f20-103">Definere lagerverdisetting og kostberegning</span><span class="sxs-lookup"><span data-stu-id="b4f20-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="b4f20-104">For å sikre at lagerkost registreres riktig, må du definere ulike felt og vinduer før du begynner å opprette varetransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b4f20-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="b4f20-105">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="b4f20-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="b4f20-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="b4f20-106">**To**</span></span>|<span data-ttu-id="b4f20-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="b4f20-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="b4f20-108">Angi en lagermetode for hver vare for å styre hvordan innkommende kost brukes til å vurdere lagerverdi og solgte varers kost.</span><span class="sxs-lookup"><span data-stu-id="b4f20-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="b4f20-109">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="b4f20-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="b4f20-110">Sikre at kost automatisk bokføres mot Finans når en lagertransaksjons bokføres.</span><span class="sxs-lookup"><span data-stu-id="b4f20-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="b4f20-111">Feltet **Automatisk kostbokføring** i vinduet **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="b4f20-111">**Automatic Cost Posting** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="b4f20-112">Sikre at forventet kost bokføres mot Finans for å se en beregning av skyldige beløp og solgte varers kost i midlertidige finanskonti før de faktisk faktureres.</span><span class="sxs-lookup"><span data-stu-id="b4f20-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="b4f20-113">Feltet **Bokf. av forventet kost i Finans** i vinduet **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="b4f20-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="b4f20-114">Definere at systemet skal justeres automatisk for eventuelle kostendringer hver gang du bokfører lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b4f20-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="b4f20-115">Justere varekost</span><span class="sxs-lookup"><span data-stu-id="b4f20-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="b4f20-116">Definere om gjennomsnittlig kost skal beregnes bare per vare, eller per vare for hver lagerføringsenhet og hver variant av varen.</span><span class="sxs-lookup"><span data-stu-id="b4f20-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="b4f20-117">Feltet **Beregn.type for gj.snittskost** i vinduet **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="b4f20-117">**Average Cost Calc. Type** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="b4f20-118">Velge hvilken tidsperiode du vil bruke til å beregne vektet gjennomsnittlig kost for varer som bruker lagermetoden Gjennomsnitt.</span><span class="sxs-lookup"><span data-stu-id="b4f20-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="b4f20-119">Feltet **Gjennomsnittskostperiode** i vinduet **Lageroppsett**</span><span class="sxs-lookup"><span data-stu-id="b4f20-119">**Average Cost Period** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="b4f20-120">Definere lagerperioder for å kontrollere lagerverdi over tid ved å forby transaksjonsbokføring i lukkede lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="b4f20-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="b4f20-121">Arbeide med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="b4f20-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="b4f20-122">Sikre at salgsreturer utlignes mot den opprinnelige utgående transaksjonen for å opprettholde lagerverdi.</span><span class="sxs-lookup"><span data-stu-id="b4f20-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="b4f20-123">Feltet **Bruk opprinnelig kostpris** i vinduet **Salg**</span><span class="sxs-lookup"><span data-stu-id="b4f20-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** window</span></span>|  
|<span data-ttu-id="b4f20-124">Sikre at kjøpsreturer utlignes mot den opprinnelige inngående transaksjonen for å opprettholde lagerverdi.</span><span class="sxs-lookup"><span data-stu-id="b4f20-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="b4f20-125">Feltet **Bruk opprinnelig kostpris** i vinduet **Kjøp**</span><span class="sxs-lookup"><span data-stu-id="b4f20-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** window</span></span>|
|<span data-ttu-id="b4f20-126">Definere avrundingsreglene som skal brukes ved justering av eller forslag om varepriser, og når standardkost skal justeres eller foreslås.</span><span class="sxs-lookup"><span data-stu-id="b4f20-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="b4f20-127">Vinduet **Avrundingsmetode**</span><span class="sxs-lookup"><span data-stu-id="b4f20-127">**Rounding Method** window</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b4f20-128">Se også</span><span class="sxs-lookup"><span data-stu-id="b4f20-128">See Also</span></span>  
[<span data-ttu-id="b4f20-129">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="b4f20-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="b4f20-130">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="b4f20-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="b4f20-131">Finans</span><span class="sxs-lookup"><span data-stu-id="b4f20-131">Finance</span></span>](finance.md)  

