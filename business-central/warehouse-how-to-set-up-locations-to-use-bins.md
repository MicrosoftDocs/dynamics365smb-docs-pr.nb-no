---
title: Definere lokasjoner slik at de bruker hyller | Microsoft-dokumentasjon
description: Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer. Når du har opprettet hyllene, kan du definere det innholdet du vil plassere i hver hylle, svært spesifikt, eller hyllen kan fungere som en mobil hylle uten angitt innhold.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 26f6898cbcb63f19ea3b89d5cd1e5df254bc33af
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382380"
---
# <a name="set-up-locations-to-use-bins"></a><span data-ttu-id="134ad-104">Definere lokasjoner slik at de bruker hyller</span><span class="sxs-lookup"><span data-stu-id="134ad-104">Set Up Locations to Use Bins</span></span>
<span data-ttu-id="134ad-105">Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer.</span><span class="sxs-lookup"><span data-stu-id="134ad-105">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="134ad-106">Når du har opprettet hyllene, kan du definere det innholdet du vil plassere i hver hylle, svært spesifikt, eller hyllen kan fungere som en mobil hylle uten angitt innhold.</span><span class="sxs-lookup"><span data-stu-id="134ad-106">When you have created your bins, you can define very specifically the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span>  

<span data-ttu-id="134ad-107">Når du skal bruke hyllen funksjonelt på en lokasjon, må du først aktivere funksjonaliteten på **Lokasjon**-kortet.</span><span class="sxs-lookup"><span data-stu-id="134ad-107">To use the bin functionality at a location, you first activate the functionality on the **Location** card.</span></span> <span data-ttu-id="134ad-108">Du utformer deretter vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.</span><span class="sxs-lookup"><span data-stu-id="134ad-108">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="134ad-109">Før du kan angi hyllekoder på lokasjonskortet, må hyllekodene være opprettet.</span><span class="sxs-lookup"><span data-stu-id="134ad-109">Before you can specify bin codes on the location card, the bin codes must be created.</span></span> <span data-ttu-id="134ad-110">Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="134ad-110">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  

## <a name="to-set-up-a-location-to-use-bins"></a><span data-ttu-id="134ad-111">Sette opp en lokasjon til å bruke hyller</span><span class="sxs-lookup"><span data-stu-id="134ad-111">To set up a location to use bins</span></span>  
1.  <span data-ttu-id="134ad-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="134ad-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="134ad-113">Velg lokajonen der du vil bruke hyller.</span><span class="sxs-lookup"><span data-stu-id="134ad-113">Select the location where you want to use bins.</span></span>  
3.  <span data-ttu-id="134ad-114">Velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="134ad-114">Choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="134ad-115">På hurtigfanen **Lager** merker du av for **Hylle obligatorisk**.</span><span class="sxs-lookup"><span data-stu-id="134ad-115">On the **Warehouse** FastTab, select the **Bin Mandatory** check box.</span></span>  
5.  <span data-ttu-id="134ad-116">Hvis du ikke bruker lagerstyring for lokasjonen, fyller du ut feltet **Standard hyllevalg** med metoden systemet skal bruke til å tilordne en standardhylle til en vare.</span><span class="sxs-lookup"><span data-stu-id="134ad-116">If you are not using directed put-away and pick for the location, fill in the **Default Bin Selection** field with the method the system should use when assigning a default bin to an item.</span></span>  
6.  <span data-ttu-id="134ad-117">Åpne kortet for lokasjonen du vil konfigurere hyller for.</span><span class="sxs-lookup"><span data-stu-id="134ad-117">Open the card for the location that you want to set up bins for.</span></span>
7.  <span data-ttu-id="134ad-118">På hurtigfanen **Hyller** velger du de hyllene du vil bruke som standard for mottak og leveringer og inngående, utgående og åpne produksjonshyller.</span><span class="sxs-lookup"><span data-stu-id="134ad-118">On the **Bins** FastTab, select the bins that you want to use as the default for receipts, shipments, inbound, outbound, and open shop floor bins.</span></span>  
8.  <span data-ttu-id="134ad-119">De hyllekodene du angir her, vil bli vist automatisk i hodene og på linjene i ulike lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="134ad-119">The bin codes you fill in here will appear automatically on the headers and on the lines of various warehouse documents.</span></span> <span data-ttu-id="134ad-120">Standardhyllene definerer alle start- og sluttplasseringer for varene i lageret.</span><span class="sxs-lookup"><span data-stu-id="134ad-120">The default bins define all starting or ending placements of items in the warehouse.</span></span>  
9.  <span data-ttu-id="134ad-121">Hvis du bruker lagerstyring, velger du en hylle til lagerjusteringer.</span><span class="sxs-lookup"><span data-stu-id="134ad-121">If you are using directed put-away and pick, select a bin for your warehouse adjustments.</span></span> <span data-ttu-id="134ad-122">Hyllekoden i feltet **Hyllekode for justering** definerer den virtuelle hyllen som skal registrere avvik i beholdning når du registrerer enten observerte forskjeller som er registrert i lagerets varekladd, eller forskjeller som beregnes når du registrerer en lageropptelling.</span><span class="sxs-lookup"><span data-stu-id="134ad-122">The bin code in the **Adjustment Bin Code** field defines the virtual bin in which to record discrepancies in inventory when you register either observed differences registered in the warehouse item journal, or differences calculated when you register a warehouse physical inventory.</span></span>  
10. <span data-ttu-id="134ad-123">Fyll ut feltene i hurtigfane **Hylleprinsipp** hvis de er relevante for lageret.</span><span class="sxs-lookup"><span data-stu-id="134ad-123">Fill in the fields on the **Bin Policies** FastTab if they are relevant to your warehouse.</span></span> <span data-ttu-id="134ad-124">De viktigste feltene er **Hyllekapasitetsprinsipp**, **Tillat anbrekk** og **Plasseringsmal - kode**.</span><span class="sxs-lookup"><span data-stu-id="134ad-124">The most important fields are **Bin Capacity Policy**, **Allow Breakbulk**, and **Put-away Template Code** fields.</span></span>  
11. <span data-ttu-id="134ad-125">På hurtigfanen **Lager** fyller du ut feltene **Utgående lagerhåndteringstid**, **Inngående lagerhåndteringstid** og **Hovedkalenderkode**.</span><span class="sxs-lookup"><span data-stu-id="134ad-125">On the **Warehouse** FastTab, fill in the **Outbound Whse. Handling Time**, **Inbound Whse. Handling Time**, and the **Base Calendar Code** fields.</span></span> <span data-ttu-id="134ad-126">Hvis du vil ha mer informasjon, kan du se [Definere hovedkalendere](across-how-to-assign-base-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="134ad-126">For more information, see [Set Up Base Calendars](across-how-to-assign-base-calendars.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="134ad-127">Fylle forbrukshyllen</span><span class="sxs-lookup"><span data-stu-id="134ad-127">Filling the Consumption Bin</span></span>
<span data-ttu-id="134ad-128">Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="134ad-128">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="134ad-129">![Flytskjema for hylle](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="134ad-129">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="134ad-130">Se også</span><span class="sxs-lookup"><span data-stu-id="134ad-130">See Also</span></span>
[<span data-ttu-id="134ad-131">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="134ad-131">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="134ad-132">Lager</span><span class="sxs-lookup"><span data-stu-id="134ad-132">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="134ad-133">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="134ad-133">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="134ad-134">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="134ad-134">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="134ad-135">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="134ad-135">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="134ad-136">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="134ad-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]