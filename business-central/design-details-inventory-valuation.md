---
title: "Designdetaljer – Lagerverdisetting | Microsoft-dokumentasjon"
description: "Lagerverdisetting XE \"Lagerverdisetting\" er fastsettelse av kostnadene som er tilordnet en lagervare, som uttrykt med følgende ligning."
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
ms.openlocfilehash: 8d186d3f104f152a4ad121d32e14ad2bc1e33c5d
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="7240c-103">Designdetaljer: Lagerverdisetting</span><span class="sxs-lookup"><span data-stu-id="7240c-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="7240c-104">Lagerverdisetting XE "Lagerverdisetting" er fastsettelse av kostnadene som er tilordnet en lagervare, som uttrykt med følgende ligning.</span><span class="sxs-lookup"><span data-stu-id="7240c-104">Inventory valuation XE "Inventory Valuation"  is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="7240c-105">Sluttbeholdning = startbeholdning + nettokjøp – solgte varers kost</span><span class="sxs-lookup"><span data-stu-id="7240c-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="7240c-106">Beregningen av lagerverdien bruker feltet **Kostbeløp (faktisk)** i verdipostene for varen.</span><span class="sxs-lookup"><span data-stu-id="7240c-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="7240c-107">Postene klassifiseres i henhold til posttypen XE "Posttype" som svarer til kostnadskomponentene, direkte kostnad, indirekte kostnad, avvik, revaluering og avrunding.</span><span class="sxs-lookup"><span data-stu-id="7240c-107">The entries are classified according to the entry type XE "Entry Type"  that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="7240c-108">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostkomponenter](design-details-cost-components.md).</span><span class="sxs-lookup"><span data-stu-id="7240c-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="7240c-109">Poster utlignes mot hverandre ved fast utligning XE "Utligning; Fast" eller i henhold til generell kostflytforutsetning angitt av lagermetoden XE "Metode; Lager" XE "Lagermetode".</span><span class="sxs-lookup"><span data-stu-id="7240c-109">Entries are applied against each other, either by the fixed application XE "Application; Fixed" , or according to the general cost-flow assumption defined by the costing method XE "Method; Costing"  XE "Costing Method" .</span></span> <span data-ttu-id="7240c-110">Én lagerreduksjonspost kan brukes til flere enn én økningspost med ulike bokføringsdatoer og eventuell annen anskaffelseskost XE "Anskaffelseskost".</span><span class="sxs-lookup"><span data-stu-id="7240c-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition cost XE "Acquisition Cost" s.</span></span> <span data-ttu-id="7240c-111">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="7240c-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="7240c-112">Beregningen av lagerverdien XE "Lagerverdi" for en gitt dato er derfor basert på summering av positive og negative verdiposter.</span><span class="sxs-lookup"><span data-stu-id="7240c-112">Therefore, calculation of the inventory value XE "Inventory Value"  for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="7240c-113">Rapporten Lagerverdisetting</span><span class="sxs-lookup"><span data-stu-id="7240c-113">Inventory Valuation report</span></span>  
<span data-ttu-id="7240c-114">For å beregne lagerverdien i **Lagerverdisetting**-rapporten begynner den ved å beregne verdien til beholdningen for varen på en gitt startdato.</span><span class="sxs-lookup"><span data-stu-id="7240c-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="7240c-115">Deretter blir verdien av lagerøkningene lagt til, og verdien av lagerreduksjoner opptil en bestemt sluttdato, blir trukket fra.</span><span class="sxs-lookup"><span data-stu-id="7240c-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="7240c-116">Sluttresultatet er lagerverdien på sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="7240c-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="7240c-117">Rapporten beregner disse verdiene ved å summere verdiene i feltet **Kostbeløp (faktisk)** i verdipostene, og bruker bokføringsdatoene som filtre.</span><span class="sxs-lookup"><span data-stu-id="7240c-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="7240c-118">Utskriften av rapporten viser også faktiske beløp, det vil si kostnad for poster som er bokført som fakturerte poster.</span><span class="sxs-lookup"><span data-stu-id="7240c-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="7240c-119">Rapporten skriver også ut forventet kostnad for poster som er bokført som mottatt eller levert, hvis du velger feltet Ta med forventet kostnad på hurtigfanen Alternativer.</span><span class="sxs-lookup"><span data-stu-id="7240c-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="7240c-120">Verdier i rapporten **Lagerverdisetting** er avstemt med lagerkontoen i finans. Dette betyr at de aktuelle verdipostene er bokført i finans.</span><span class="sxs-lookup"><span data-stu-id="7240c-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="7240c-121">Beløp i **Verdi**-kolonnene i rapporten er basert på bokføringsdatoen for transaksjoner for en vare.</span><span class="sxs-lookup"><span data-stu-id="7240c-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="7240c-122">Rapporten Lagerverdisetting - VIA</span><span class="sxs-lookup"><span data-stu-id="7240c-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="7240c-123">Et produksjonsfirma må fastslå verdien av tre typer beholdning:</span><span class="sxs-lookup"><span data-stu-id="7240c-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="7240c-124">Råvarerbeholdning</span><span class="sxs-lookup"><span data-stu-id="7240c-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="7240c-125">VIA-beholdning</span><span class="sxs-lookup"><span data-stu-id="7240c-125">WIP inventory</span></span>  
* <span data-ttu-id="7240c-126">Ferdige varer på lager</span><span class="sxs-lookup"><span data-stu-id="7240c-126">Finished Goods inventory</span></span>  

<span data-ttu-id="7240c-127">Verdien til VIA-beholdning fastsettes med formelen nedenfor:</span><span class="sxs-lookup"><span data-stu-id="7240c-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="7240c-128">Slutt-VIA-beholdning = Start-VIA-beholdning + produksjonskost – kostnader for produserte varer</span><span class="sxs-lookup"><span data-stu-id="7240c-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="7240c-129">Verdipostene er grunnlaget for lagerverdien for kjøpt lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="7240c-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="7240c-130">Beregningen gjøres ved hjelp av verdiene i feltet **Kostbeløp (faktisk)** i verdipostene for vare og kapasitet som er knyttet til en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="7240c-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="7240c-131">Formålet med VIA-lagerverdisetting er å fastslå verdien til varer som ennå ikke er ferdigprodusert, på en gitt dato.</span><span class="sxs-lookup"><span data-stu-id="7240c-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="7240c-132">VIA-lagerverdien er derfor basert på verdipostene som er knyttet til forbruks- og kapasitetspostene.</span><span class="sxs-lookup"><span data-stu-id="7240c-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="7240c-133">Forbruksposter må faktureres fullstendig på datoen for verdisettingen.</span><span class="sxs-lookup"><span data-stu-id="7240c-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="7240c-134">Rapporten **Lagerverdisetting – VIA** viser derfor kostnadene som representerer VIA-lagerverdien, i to kategorier: forbruk og kapasitet.</span><span class="sxs-lookup"><span data-stu-id="7240c-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7240c-135">Se også</span><span class="sxs-lookup"><span data-stu-id="7240c-135">See Also</span></span>  
<span data-ttu-id="7240c-136">[Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="7240c-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="7240c-137">[Designdetaljer: Revaluering](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="7240c-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="7240c-138">[Designdetaljer: Bokføre produksjonsordre](design-details-production-order-posting.md)
[Administrere lagerkostnader](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="7240c-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="7240c-139">Finans</span><span class="sxs-lookup"><span data-stu-id="7240c-139">Finance</span></span>](finance.md)  
<span data-ttu-id="7240c-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7240c-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

