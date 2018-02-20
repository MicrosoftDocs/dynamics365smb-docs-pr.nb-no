---
title: Rapportere kostnader og avstemme med Finans | Microsoft-dokumentasjon
description: "Ved slutten av en regnskapsperiode, enten månedlig, årlig eller annet, må en sekvens med oppgaver innen kostkontroll og sporing utføres for å rapportere en korrekt og balansert lagerverdi til finansavdelingen. I tillegg til bokføringsrutinen som overfører de enkeltstående vareverdipostene til dedikerte finanskonti, er flere rapporter, sporingsfunksjoner og et spesielt avstemmingsverktøy tilgjengelig for revisoren eller kontrolleren som er ansvarlig for dette forretningskritiske arbeidet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45afc7249e921b483d9fcb6860401528746f554a
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="reporting-costs-and-reconciling-with-the-general-ledger"></a><span data-ttu-id="28a95-104">Rapportere kostnader og avstemme med Finans</span><span class="sxs-lookup"><span data-stu-id="28a95-104">Reporting Costs and Reconciling with the General Ledger</span></span>
<span data-ttu-id="28a95-105">Ved slutten av en regnskapsperiode, enten månedlig, årlig eller annet, må en sekvens med oppgaver innen kostkontroll og sporing utføres for å rapportere en korrekt og balansert lagerverdi til finansavdelingen.</span><span class="sxs-lookup"><span data-stu-id="28a95-105">At the end of accounting periods, monthly, yearly or other, a sequence of cost control and auditing tasks must be performed to report a correct and balanced inventory value to the finance department.</span></span> <span data-ttu-id="28a95-106">I tillegg til bokføringsrutinen som overfører de enkeltstående vareverdipostene til dedikerte finanskonti, er flere rapporter, sporingsfunksjoner og et spesielt avstemmingsverktøy tilgjengelig for revisoren eller kontrolleren som er ansvarlig for dette forretningskritiske arbeidet.</span><span class="sxs-lookup"><span data-stu-id="28a95-106">Apart from the posting routine that transfers the individual item value entries to dedicated general ledger accounts, several reports, tracing functions, and a special reconciliation tool are available to the auditor or controller responsible for this business-critical work.</span></span>  

 <span data-ttu-id="28a95-107">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="28a95-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="28a95-108">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="28a95-108">**To**</span></span>|<span data-ttu-id="28a95-109">**Se**</span><span class="sxs-lookup"><span data-stu-id="28a95-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="28a95-110">Vise lagerverdien for utvalgte varer, inkludert informasjon om antall og verdier for økninger eller reduksjoner i lageret i løpet av en utvalgt periode.</span><span class="sxs-lookup"><span data-stu-id="28a95-110">View the inventory value of selected items, including information about the quantities and values of increases and decreases in inventory over a selected period.</span></span>|<span data-ttu-id="28a95-111">Rapporten **Lagerverdisetting**</span><span class="sxs-lookup"><span data-stu-id="28a95-111">**Inventory Valuation** report</span></span>|  
|<span data-ttu-id="28a95-112">Vise lagerverdien for utvalgte produksjonsordrer i VIA-beholdningen (varer i arbeid), for eksempel antall og verdier for forbruk, kapasitetsbruk og produksjon fra produksjonsordrer som pågår.</span><span class="sxs-lookup"><span data-stu-id="28a95-112">View the inventory value of selected production orders in your WIP (work in process) inventory, such as the quantities and values of consumption, capacity usage, and output in ongoing production orders.</span></span>|<span data-ttu-id="28a95-113">Rapporten **Lagerverdisetting - VIA**</span><span class="sxs-lookup"><span data-stu-id="28a95-113">**Inventory Valuation - WIP** report</span></span>|  
|<span data-ttu-id="28a95-114">Vise lagerverdien for utvalgte varer, inkludert faktisk og forventet kost på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="28a95-114">View the inventory value of selected items, including their actual and expected cost on the date specified.</span></span>|<span data-ttu-id="28a95-115">Rappporten **Lagerverdisetting - kostspesifikasjon**</span><span class="sxs-lookup"><span data-stu-id="28a95-115">**Invt. Valuation - Cost Spec.** report</span></span>|  
|<span data-ttu-id="28a95-116">Bruke en rapport til å analysere årsakene til prisavvik eller få innsikt i kostandelen for solgte varer (vareforbruk).</span><span class="sxs-lookup"><span data-stu-id="28a95-116">Use a report to analyze the reasons for cost variances or to gain insight into the cost shares of sold items (COGS).</span></span>|<span data-ttu-id="28a95-117">Rapporten **Spesifikasjon av kostandeler**</span><span class="sxs-lookup"><span data-stu-id="28a95-117">**Cost Shares Breakdown** report</span></span>|  
|<span data-ttu-id="28a95-118">Jevnlig bokføre verdipostene for varetransaksjoner fra vareposten til de relaterte finanskontiene for å avstemme de to postene.</span><span class="sxs-lookup"><span data-stu-id="28a95-118">Periodically post the value entries of item transactions from the inventory ledger to the related G/L accounts to reconcile the two ledgers.</span></span>|[<span data-ttu-id="28a95-119">Avstemme lagerkost med finans</span><span class="sxs-lookup"><span data-stu-id="28a95-119">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="28a95-120">Bruke ett vindu til å spore avstemmingen mellom lagerposten og Finans.</span><span class="sxs-lookup"><span data-stu-id="28a95-120">Use one window to audit the reconciliation between the inventory ledger and the general ledger.</span></span>|[<span data-ttu-id="28a95-121">Avstemme lagerkost med finans</span><span class="sxs-lookup"><span data-stu-id="28a95-121">Reconcile Inventory Costs with the General Ledger</span></span>](finance-how-to-post-inventory-costs-to-the-general-ledger.md)|  
|<span data-ttu-id="28a95-122">Fastsette VIA-beløpet som må bokføres på balansekonti for rapportering ved periodeslutt.</span><span class="sxs-lookup"><span data-stu-id="28a95-122">Determine the WIP amount that needs to be posted to balance sheet accounts for period-end reporting.</span></span>|[<span data-ttu-id="28a95-123">Overvåke prosjektfremdrift og -ytelse</span><span class="sxs-lookup"><span data-stu-id="28a95-123">Monitor Job Progress and Performance</span></span>](projects-how-monitor-progress-performance.md)|

## <a name="see-also"></a><span data-ttu-id="28a95-124">Se også</span><span class="sxs-lookup"><span data-stu-id="28a95-124">See Also</span></span>  
[<span data-ttu-id="28a95-125">Definere lagerverdisetting og kostberegning</span><span class="sxs-lookup"><span data-stu-id="28a95-125">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="28a95-126">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="28a95-126">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="28a95-127">Finans</span><span class="sxs-lookup"><span data-stu-id="28a95-127">Finance</span></span>](finance.md)  
<span data-ttu-id="28a95-128">[Lager](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="28a95-128">[Inventory](inventory-manage-inventory.md) </span></span>  
<span data-ttu-id="28a95-129">[Salg](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="28a95-129">[Sales](sales-manage-sales.md) </span></span>  
[<span data-ttu-id="28a95-130">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="28a95-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="28a95-131">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28a95-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

