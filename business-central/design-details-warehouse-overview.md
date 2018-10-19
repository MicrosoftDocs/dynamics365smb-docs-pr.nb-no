---
title: "Designdetaljer – Lageroversikt | Microsoft-dokumentasjon"
description: "For å støtte den fysiske håndteringen av varer på sone- og hyllenivå må all informasjon spores for hver transaksjon eller flytting på lageret. Dette håndteres i **Lagerpost**-tabellen. Hver transaksjon lagres i en lagerjournal."
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
ms.openlocfilehash: cea5bb76f8fdb8c9c52a5f341d29a34bcb8f0cdc
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="d1d11-105">Designdetaljer: Lageroversikt</span><span class="sxs-lookup"><span data-stu-id="d1d11-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="d1d11-106">For å støtte den fysiske håndteringen av varer på sone- og hyllenivå må all informasjon spores for hver transaksjon eller flytting på lageret.</span><span class="sxs-lookup"><span data-stu-id="d1d11-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="d1d11-107">Dette håndteres i **Lagerpost**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="d1d11-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="d1d11-108">Hver transaksjon lagres i en lagerjournal.</span><span class="sxs-lookup"><span data-stu-id="d1d11-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="d1d11-109">Lagerdokumenter og en lagerkladd brukes til å registrere flytting av varer på lageret.</span><span class="sxs-lookup"><span data-stu-id="d1d11-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="d1d11-110">Hver gang et element i lageret flyttes, mottas, plasseres, plukkes, leveres eller justeres, blir det registrert lagerposter for å lagre den fysiske informasjonen om sone, hylle og antall.</span><span class="sxs-lookup"><span data-stu-id="d1d11-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span> <span data-ttu-id="d1d11-111">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d1d11-111">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="d1d11-112">**Hylleinnhold**-tabellen brukes til å håndtere de ulike dimensjonene til innholdet i en hylle per vare, for eksempel enhet, maksimumsantall og minimumsantall.</span><span class="sxs-lookup"><span data-stu-id="d1d11-112">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="d1d11-113">**Hylleinnhold**-tabellen inneholder også flytfelt til lagerpostene, lagerinstruksjonene og lagerkladdelinjene, som sikrer at tilgjengeligheten til en vare per hylle og en hylle for en vare kan beregnes raskt.</span><span class="sxs-lookup"><span data-stu-id="d1d11-113">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="d1d11-114">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="d1d11-114">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="d1d11-115">Når varebokføringer skjer utenfor lagermodulen, brukes en standard justeringshylle per lokasjon til å synkronisere lagerposter med beholdningsposter.</span><span class="sxs-lookup"><span data-stu-id="d1d11-115">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="d1d11-116">Under vareopptelling for lageret registreres eventuelle forskjeller mellom beregnet og opptalt antall i justeringshyllen, og deretter posteres dette som korrigerende vareposter.</span><span class="sxs-lookup"><span data-stu-id="d1d11-116">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="d1d11-117">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Integrasjon med lagerbeholdning](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="d1d11-117">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="d1d11-118">Illustrasjonen nedenfor gir en oversikt over vanlig lagerflyter.</span><span class="sxs-lookup"><span data-stu-id="d1d11-118">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="d1d11-119">![Oversikt over lagerprosesser](media/design_details_warehouse_management_overview.png "Oversikt over lagerprosesser")</span><span class="sxs-lookup"><span data-stu-id="d1d11-119">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="d1d11-120">Grunnleggende eller avanserte lagerstyring</span><span class="sxs-lookup"><span data-stu-id="d1d11-120">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="d1d11-121">Lagerfunksjonaliteten i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan implementeres på ulike kompleksitetsnivåer, avhengig av rutiner og ordrevolum i et selskap.</span><span class="sxs-lookup"><span data-stu-id="d1d11-121">Warehouse functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="d1d11-122">Hovedforskjellen er at aktiviteter utføres ordre for ordre i grunnleggende lagerstyring, mens de konsolideres for flere ordrer i avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="d1d11-122">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="d1d11-123">For å skille mellom de ulike kompleksitetsnivåene henviser denne dokumentasjonen til to generelle betegnelser, grunnleggende og avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="d1d11-123">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="d1d11-124">Denne enkle differensieringen dekker flere ulike kompleksitetsnivåer, som defineres av produktgranuler og lokasjonsoppsettet, der hvert nivå støttes av ulike grensesnittdokumenter.</span><span class="sxs-lookup"><span data-stu-id="d1d11-124">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="d1d11-125">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerstyringsoppsett](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d1d11-125">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d1d11-126">De mest avanserte lagerstyringsnivået kalles "LA-installasjoner" i denne dokumentasjonen, siden dette nivået krever den mest avanserte granulen, Lagerstyringssystem.</span><span class="sxs-lookup"><span data-stu-id="d1d11-126">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="d1d11-127">De ulike grensesnittdokumentene nedenfor brukes i grunnleggende og avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="d1d11-127">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="d1d11-128">Dokumenter for grunnleggende brukergrensesnitt</span><span class="sxs-lookup"><span data-stu-id="d1d11-128">Basic UI Documents</span></span>  

-   <span data-ttu-id="d1d11-129">**Lagerplassering**</span><span class="sxs-lookup"><span data-stu-id="d1d11-129">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="d1d11-130">**Lagerplukk**</span><span class="sxs-lookup"><span data-stu-id="d1d11-130">**Inventory Pick**</span></span>  
-   <span data-ttu-id="d1d11-131">**Lagerflytting**</span><span class="sxs-lookup"><span data-stu-id="d1d11-131">**Inventory Movement**</span></span>  
-   <span data-ttu-id="d1d11-132">**Varekladd**</span><span class="sxs-lookup"><span data-stu-id="d1d11-132">**Item Journal**</span></span>  
-   <span data-ttu-id="d1d11-133">**Varereklassifiseringskladd**</span><span class="sxs-lookup"><span data-stu-id="d1d11-133">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="d1d11-134">(Forskjellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="d1d11-134">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="d1d11-135">Dokumenter for avanserte brukergrensesnitt</span><span class="sxs-lookup"><span data-stu-id="d1d11-135">Advanced UI Documents</span></span>  

-   <span data-ttu-id="d1d11-136">**Lagermottak**</span><span class="sxs-lookup"><span data-stu-id="d1d11-136">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="d1d11-137">**Plasseringsforslag**</span><span class="sxs-lookup"><span data-stu-id="d1d11-137">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="d1d11-138">**Plassering**</span><span class="sxs-lookup"><span data-stu-id="d1d11-138">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="d1d11-139">**Plukkforslag**</span><span class="sxs-lookup"><span data-stu-id="d1d11-139">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="d1d11-140">**Plukk**</span><span class="sxs-lookup"><span data-stu-id="d1d11-140">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="d1d11-141">**Flytteforslag**</span><span class="sxs-lookup"><span data-stu-id="d1d11-141">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="d1d11-142">**Lagerflytting**</span><span class="sxs-lookup"><span data-stu-id="d1d11-142">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="d1d11-143">**Intern plukk**</span><span class="sxs-lookup"><span data-stu-id="d1d11-143">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="d1d11-144">**Intern plassering**</span><span class="sxs-lookup"><span data-stu-id="d1d11-144">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="d1d11-145">**Hylleoppretting**</span><span class="sxs-lookup"><span data-stu-id="d1d11-145">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="d1d11-146">**Hylleinnholdopprett. - forslag**</span><span class="sxs-lookup"><span data-stu-id="d1d11-146">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="d1d11-147">**Lagervarekladd**</span><span class="sxs-lookup"><span data-stu-id="d1d11-147">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="d1d11-148">**Lagervarereklassif.kladd**</span><span class="sxs-lookup"><span data-stu-id="d1d11-148">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="d1d11-149">(Forskjellige rapporter)</span><span class="sxs-lookup"><span data-stu-id="d1d11-149">(Various reports)</span></span>  

<span data-ttu-id="d1d11-150">Hvis du vil ha mer informasjon om hvert dokument, kan du se de respektive emnene for vinduet.</span><span class="sxs-lookup"><span data-stu-id="d1d11-150">For more information about each document, see the respective window topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="d1d11-151">Terminologi</span><span class="sxs-lookup"><span data-stu-id="d1d11-151">Terminology</span></span>  
<span data-ttu-id="d1d11-152">Lagerdokumentasjonen for [!INCLUDE[d365fin](includes/d365fin_md.md)] henviser til følgende termer for vareflyt på lageret, slik at den passer med de økonomiske begrepene om kjøp og salg.</span><span class="sxs-lookup"><span data-stu-id="d1d11-152">To align with the financial concepts of purchases and sales, [!INCLUDE[d365fin](includes/d365fin_md.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="d1d11-153">Begrep</span><span class="sxs-lookup"><span data-stu-id="d1d11-153">Term</span></span>|<span data-ttu-id="d1d11-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d1d11-154">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="d1d11-155">Inngående flyt</span><span class="sxs-lookup"><span data-stu-id="d1d11-155">Inbound flow</span></span>|<span data-ttu-id="d1d11-156">Varer som flyttes på lagerlokasjonen, for eksempel innkjøp og inngående overføringer.</span><span class="sxs-lookup"><span data-stu-id="d1d11-156">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="d1d11-157">Intern flyt</span><span class="sxs-lookup"><span data-stu-id="d1d11-157">Internal flow</span></span>|<span data-ttu-id="d1d11-158">Varer som flyttes på lagerlokasjonen, for eksempel produksjonskomponenter og utligning.</span><span class="sxs-lookup"><span data-stu-id="d1d11-158">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="d1d11-159">Utgående flyt</span><span class="sxs-lookup"><span data-stu-id="d1d11-159">Outbound flow</span></span>|<span data-ttu-id="d1d11-160">Varer som flyttes ut av lagerlokasjonen, for eksempel salg og utgående overføringer.</span><span class="sxs-lookup"><span data-stu-id="d1d11-160">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="d1d11-161">Se også</span><span class="sxs-lookup"><span data-stu-id="d1d11-161">See Also</span></span>  
 [<span data-ttu-id="d1d11-162">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="d1d11-162">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

