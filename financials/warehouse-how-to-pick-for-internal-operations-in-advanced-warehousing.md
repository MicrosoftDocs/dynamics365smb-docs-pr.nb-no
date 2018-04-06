---
title: Plukke for interne operasjoner i avansert lageroppsett | Microsoft-dokumentasjon
description: "I avansert lageroppsett der lokasjonen er definert slik at plukking og levering brukes, kan du plukke komponenter for produksjons- og monteringsaktiviteter ved å bruke **Plukk**-vinduet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0a18e88ae9bb34b3cf5aa9d4a28e1d087ba9aa40
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a><span data-ttu-id="8e7e0-103">Plukke for montering eller produksjon i avanserte lageroppsett</span><span class="sxs-lookup"><span data-stu-id="8e7e0-103">Pick for Assembly or Production in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="8e7e0-104">I avansert lageroppsett der lokasjonen er definert slik at plukking og levering brukes, kan du plukke komponenter for produksjons- og monteringsaktiviteter ved å bruke **Plukk**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-104">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** window.</span></span>  

<span data-ttu-id="8e7e0-105">Du kan også bruke vinduet **Flytteforslag** til å flytte varer mellom hyller ad hoc, noe som betyr uten referanse til et kildedokument.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-105">Alternatively, you can use the **Movement Worksheet** window to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="8e7e0-106">Hvis du vil ha mer informasjon, kan du se [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="8e7e0-106">For more information, see [Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="8e7e0-107">Hvis du vil ha mer informasjon om plukking av varer for interne operasjoner i grunnleggende lagerlokasjoner som er definert for bare plukking, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="8e7e0-107">For information about picking items for internal operations in basic warehouse locations that are set up for picking only, see [Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>  

<span data-ttu-id="8e7e0-108">Du kan ikke opprette et lagerplukkdokument fra grunnen av fordi en plukkaktivitet alltid er en del av en arbeidsflyt, enten i et pull- eller push-scenario.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-108">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="8e7e0-109">Du kan opprette lagerplukkdokumentet på en push-måte ved å velge **Opprett plukk** i kildedokumentet, for eksempel en frigitt monteringsordre eller lagerlevering.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-109">You can create the warehouse pick document in a push fashion by selecting **Create Whse. Pick** on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="8e7e0-110">Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="8e7e0-110">For more information, see [Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="8e7e0-111">Du kan også opprette plukkdokumentet på en hentemåte ved å bruke vinduet **Plukkforslag** til å oppdage plukkforespørsler, både for levering og interne operasjoner, og deretter opprette de nødvendige plukkdokumentene.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-111">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** window to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="8e7e0-112">Fremgangsmåten nedenfor forklarer et plukkescenario der du plukker komponenter for en frigitt produksjonsordre via vinduet **Plukkforslag**.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-112">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** window.</span></span> <span data-ttu-id="8e7e0-113">Fremgangsmåten gjelder også for en monteringsordre.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-113">The procedure also applies for an assembly order.</span></span>  

<span data-ttu-id="8e7e0-114">Hvis du vil opprette plukkforespørsler, må de aktuelle kildedokumentene frigis både for plukk- og skyvscenarier.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-114">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="8e7e0-115">Frigi kildedokumenter for interne operasjoner på følgende måter.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-115">Release source documents for internal operations in the following ways.</span></span>  

|<span data-ttu-id="8e7e0-116">Kildedokument</span><span class="sxs-lookup"><span data-stu-id="8e7e0-116">Source Document</span></span>|<span data-ttu-id="8e7e0-117">Frigivelsesmetode</span><span class="sxs-lookup"><span data-stu-id="8e7e0-117">Release Method</span></span>|  
|---------------------|--------------------|  
|<span data-ttu-id="8e7e0-118">Produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="8e7e0-118">Production Order</span></span>|<span data-ttu-id="8e7e0-119">Endre ordretypen til frigitt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-119">Change order type to released production order.</span></span>|  
|<span data-ttu-id="8e7e0-120">Monteringsordre</span><span class="sxs-lookup"><span data-stu-id="8e7e0-120">Assembly Order</span></span>|<span data-ttu-id="8e7e0-121">Endre status til Frigitt.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-121">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="8e7e0-122">Slik plukker du komponenter ved hjelp av plukkforslaget</span><span class="sxs-lookup"><span data-stu-id="8e7e0-122">To pick components using the pick worksheet</span></span>  
1.  <span data-ttu-id="8e7e0-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukkforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8e7e0-124">Velg handlingen **Hent lagerdokumenter**, og velg deretter komponentlinjene fra den frigitte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-124">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="8e7e0-125">Inspiser linjene, sorter dem for å sikre en effektiv plukkrunde, og slå dem sammen med andre forslagslinjer om nødvendig for å utnytte arbeidstiden best mulig.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-125">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="8e7e0-126">Velg handlingen **Opprett plukk**.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-126">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="8e7e0-127">Definer hvordan lagerplukkdokumenter skal opprettes og hvordan plukklinjer skal sorteres, ved å fylle ut felt i vinduet **Opprett plukk**.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-127">Define how to create the warehouse pick documents and how to sort pick lines by filling fields in the **Create Pick** window.</span></span>  
6.  <span data-ttu-id="8e7e0-128">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-128">Choose the **OK** button.</span></span> <span data-ttu-id="8e7e0-129">Lagerplukkdokumenter opprettes med plukklinjer for hver komponent som kreves i den interne operasjonen.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-129">Warehouse pick documents are created with pick lines for each component that is required in the internal operation.</span></span>  

<span data-ttu-id="8e7e0-130">Hvis det interne operasjonsområdet, for eksempel en produksjon, er opprettet med en standardhylle for plassering av komponenter som skal brukes i operasjonen, settes denne hyllekoden inn på Plasser-linjene i plukkdokumentet for å gi lagermedarbeidere beskjed om hvor de skal plassere varene.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-130">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="8e7e0-131">Hvis du vil ha mer informasjon, se feltet **Til-Hyllekode for produksjon** eller **Til-Hyllekode for montering**.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-131">For more information, see the **To-Production Bin Code** or the **To-Assembly Bin Code** field.</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="8e7e0-132">Fylle forbrukshyllen</span><span class="sxs-lookup"><span data-stu-id="8e7e0-132">Filling the Consumption Bin</span></span>
<span data-ttu-id="8e7e0-133">Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="8e7e0-133">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="8e7e0-134">![Flytskjema for hylle](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="8e7e0-134">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e7e0-135">Se også</span><span class="sxs-lookup"><span data-stu-id="8e7e0-135">See Also</span></span>
[<span data-ttu-id="8e7e0-136">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="8e7e0-136">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="8e7e0-137">Lager</span><span class="sxs-lookup"><span data-stu-id="8e7e0-137">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="8e7e0-138">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="8e7e0-138">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="8e7e0-139">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="8e7e0-139">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="8e7e0-140">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="8e7e0-140">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="8e7e0-141">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8e7e0-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

