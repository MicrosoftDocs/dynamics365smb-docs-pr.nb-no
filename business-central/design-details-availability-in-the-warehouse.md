---
title: "Designdetaljer – Tilgjengelighet i lageret | Microsoft-dokumentasjon"
description: "Systemet må holde konstant kontroll over varedisposisjon på lageret, slik at utgående ordrer kan flyte effektivt og gi optimale leveringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 698404dab1b3888d073eb3c23268d3b009a4f577
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-availability-in-the-warehouse"></a><span data-ttu-id="3429c-103">Designdetaljer: Tilgjengelighet i lageret</span><span class="sxs-lookup"><span data-stu-id="3429c-103">Design Details: Availability in the Warehouse</span></span>
<span data-ttu-id="3429c-104">Systemet må holde konstant kontroll over varedisposisjon på lageret, slik at utgående ordrer kan flyte effektivt og gi optimale leveringer.</span><span class="sxs-lookup"><span data-stu-id="3429c-104">The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.</span></span>  

 <span data-ttu-id="3429c-105">Tilgjengelighet varierer avhengig av tildelinger på hyllenivå når det oppstår lageraktiviteter som plukking og flytting, og når lagerreservasjonssystemet bruker begrensninger som må overholdes.</span><span class="sxs-lookup"><span data-stu-id="3429c-105">Availability varies depending on allocations at the bin level when warehouse activities such as picks and movements occur and when the inventory reservation system imposes restrictions to comply with.</span></span> <span data-ttu-id="3429c-106">En ganske komplisert algoritme bekrefter at alle betingelsene er oppfylt før tildeling av antall i plukk for utgående flyter.</span><span class="sxs-lookup"><span data-stu-id="3429c-106">A rather complex algorithm verifies that all conditions are met before allocating quantities to picks for outbound flows.</span></span>  

## <a name="bin-content-and-reservations"></a><span data-ttu-id="3429c-107">Hylleinnhold og reservasjoner</span><span class="sxs-lookup"><span data-stu-id="3429c-107">Bin Content and Reservations</span></span>  
 <span data-ttu-id="3429c-108">I en installasjon av lagerstyring finnes vareantall både som lagerposter i modulen Lager og som varepostene i modulen Beholdning.</span><span class="sxs-lookup"><span data-stu-id="3429c-108">In any installation of warehouse management, item quantities exist both as warehouse entries, in the Warehouse application area, and as item ledger entries, in the Inventory application area.</span></span> <span data-ttu-id="3429c-109">Disse to posttypene inneholder forskjellig informasjon om hvor varene er, og om de er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="3429c-109">These two entry types contain different information about where items exist and whether they are available.</span></span> <span data-ttu-id="3429c-110">Lagerposter angir disposisjonen til en vare etter hylle og hylletype, som kalles hylleinnhold.</span><span class="sxs-lookup"><span data-stu-id="3429c-110">Warehouse entries define an item’s availability by bin and bin type, which is called bin content.</span></span> <span data-ttu-id="3429c-111">Vareposter angir varens tilgjengelighet ved reservasjon til utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3429c-111">Item ledger entries define an item’s availability by its reservation to outbound documents.</span></span>  

 <span data-ttu-id="3429c-112">I plukkealgoritmen er det spesialfunksjonalitet som brukes til å beregne antallet som er disponibelt for plukking når hylleinnhold er knyttet til reservasjoner.</span><span class="sxs-lookup"><span data-stu-id="3429c-112">Special functionality in the picking algorithm exists to calculate the quantity that is available to pick when bin content is coupled with reservations.</span></span>  

## <a name="quantity-available-to-pick"></a><span data-ttu-id="3429c-113">Antall tilgjengelig for plukk</span><span class="sxs-lookup"><span data-stu-id="3429c-113">Quantity Available to Pick</span></span>  
 <span data-ttu-id="3429c-114">Hvis for eksempel plukkalgoritmen tar hensyn til vareantall som er reservert for en ventende ordrelevering, kan disse varene plukkes for en annen ordre som er sendt tidligere, noe som hindrer at det første salget fullføres.</span><span class="sxs-lookup"><span data-stu-id="3429c-114">If, for example, the picking algorithm does not consider item quantities that are reserved for a pending sales order shipment, then those items might be picked for another sales order that is shipped earlier, which prevents the first sales from being fulfilled.</span></span> <span data-ttu-id="3429c-115">For å unngå denne situasjonen trekker plukkealgoritmen fra antall som er reservert for andre utgående dokumenter, antall i eksisterende plukkdokumenter og antall som er plukket, men ennå ikke er levert eller forbrukt.</span><span class="sxs-lookup"><span data-stu-id="3429c-115">To avoid this situation, the picking algorithm subtracts quantities that are reserved for other outbound documents, quantities on existing pick documents, and quantities that are picked but not yet shipped or consumed.</span></span>  

 <span data-ttu-id="3429c-116">Resultatet vises i feltet **Disp. antall som kan plukkes** i vinduet **Plukkforslag**, der feltet beregnes dynamisk.</span><span class="sxs-lookup"><span data-stu-id="3429c-116">The result is displayed in the **Available Qty. to Pick** field in the **Pick Worksheet** window, where the field is calculated dynamically.</span></span> <span data-ttu-id="3429c-117">Verdien beregnes også når brukere oppretter plukkinger direkte for utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3429c-117">The value is also calculated when users create warehouse picks directly for outbound documents.</span></span> <span data-ttu-id="3429c-118">Slike utgående dokumenter kan være ordrer, produksjonsforbruk eller utgående overføringer, der resultatet gjenspeiles i de tilknyttede antallsfeltene, for eksempel **Ant. som skal håndt.**.</span><span class="sxs-lookup"><span data-stu-id="3429c-118">Such outbound documents could be sales orders, production consumption, or outbound transfers, where the result is reflected in the related quantity fields, such as **Qty. to Handle**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3429c-119">Når det gjelder reservasjonsprioriteter, blir antallet som skal reserveres trukket fra antallet som er tilgjengelige for plukk.</span><span class="sxs-lookup"><span data-stu-id="3429c-119">Concerning the priority of reservations, the quantity to reserve is subtracted from the quantity available to pick.</span></span> <span data-ttu-id="3429c-120">Hvis for eksempel antallet som er tilgjengelig i plukkhyller er 5 enheter, men 100 enheter er i plasseringshyller, vil det vises en feilmelding når du prøver å reservere flere enn 5 enheter for en annen ordre, fordi resten av antallet må være tilgjengelig i plukkhyller.</span><span class="sxs-lookup"><span data-stu-id="3429c-120">For example, if the quantity available in pick bins is 5 units, but 100 units are in put-away bins, then when you try to reserve more than 5 units for another order, an error message is displayed because the additional quantity must be available in pick bins.</span></span>  

### <a name="calculating-the-quantity-available-to-pick"></a><span data-ttu-id="3429c-121">Beregne antall tilgjengelig for plukk</span><span class="sxs-lookup"><span data-stu-id="3429c-121">Calculating the Quantity Available to Pick</span></span>  
 <span data-ttu-id="3429c-122">Antallet som er disponibelt for plukking, beregnes som følger:</span><span class="sxs-lookup"><span data-stu-id="3429c-122">The quantity available to pick is calculated as follows:</span></span>  

 <span data-ttu-id="3429c-123">Antall tilgjengelige for plukk = Antallet i plukkhyller - Antallet i plukk og flyttinger – (Reservert antall i plukkhyller + Reservert antall i plukk og flyttinger)</span><span class="sxs-lookup"><span data-stu-id="3429c-123">quantity available to pick = quantity in pick bins - quantity on picks and movements – (reserved quantity in pick bins + reserved quantity on picks and movements)</span></span>  

 <span data-ttu-id="3429c-124">Diagrammet nedenfor viser de ulike elementene i beregningen.</span><span class="sxs-lookup"><span data-stu-id="3429c-124">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="3429c-125">![Disponibelt for plukking, med reservasjonsoverlapping](media/design_details_warehouse_management_availability_2.png "design_details_warehouse_management_availability_2")</span><span class="sxs-lookup"><span data-stu-id="3429c-125">![Available to pick, with reservation overlap](media/design_details_warehouse_management_availability_2.png "design_details_warehouse_management_availability_2")</span></span>  

## <a name="quantity-available-to-reserve"></a><span data-ttu-id="3429c-126">Antall tilgjengelig for reservasjon</span><span class="sxs-lookup"><span data-stu-id="3429c-126">Quantity Available to Reserve</span></span>  
 <span data-ttu-id="3429c-127">Siden konsepter for hylleinnhold og reservasjon sameksisterer, må antall varer som er tilgjengelige for reservasjon, justeres etter tildelinger til utgående lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="3429c-127">Because the concepts of bin content and reservation co-exist, the quantity of items that are available to reserve must be aligned with allocations to outbound warehouse documents.</span></span>  

 <span data-ttu-id="3429c-128">Det skal være mulig å reservere alle varene i beholdningen, unntatt de som har startet utgående behandling.</span><span class="sxs-lookup"><span data-stu-id="3429c-128">It should be possible to reserve all items in inventory, except those that have started outbound processing.</span></span> <span data-ttu-id="3429c-129">Antallet som er tilgjengelig for å reservere blir derfor definert som antallet på alle dokumenter og alle hylletyper, unntatt følgende utgående antall:</span><span class="sxs-lookup"><span data-stu-id="3429c-129">Accordingly, the quantity that is available to reserve is defined as the quantity on all documents and all bin types, except the following outbound quantities:</span></span>  

-   <span data-ttu-id="3429c-130">Antall på uregistrerte plukkdokumenter</span><span class="sxs-lookup"><span data-stu-id="3429c-130">Quantity on unregistered pick documents</span></span>  
-   <span data-ttu-id="3429c-131">Antall i leveringshyller</span><span class="sxs-lookup"><span data-stu-id="3429c-131">Quantity in shipment bins</span></span>  
-   <span data-ttu-id="3429c-132">Antall i til produksjon-hyller</span><span class="sxs-lookup"><span data-stu-id="3429c-132">Quantity in to-production bins</span></span>  
-   <span data-ttu-id="3429c-133">Antall i åpne produksjonshyller</span><span class="sxs-lookup"><span data-stu-id="3429c-133">Quantity in open shop floor bins</span></span>  
-   <span data-ttu-id="3429c-134">Antall i til montering-hyller</span><span class="sxs-lookup"><span data-stu-id="3429c-134">Quantity in to-assembly bins</span></span>  
-   <span data-ttu-id="3429c-135">Antall i justeringshyller</span><span class="sxs-lookup"><span data-stu-id="3429c-135">Quantity in adjustment bins</span></span>  

 <span data-ttu-id="3429c-136">Resultatet vises i feltet **Totalt disp. antall** i **Reservasjon**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="3429c-136">The result is displayed in the **Total Available Quantity** field in the **Reservation** window.</span></span>  

 <span data-ttu-id="3429c-137">Antallet som ikke kan reserveres på en reservasjonslinje fordi det er tildelt i lageret, vises i feltet **Tildelt antall på lager** i **Reservasjon**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="3429c-137">On a reservation line, the quantity that cannot be reserved, because it is allocated in the warehouse, is displayed in the **Qty. Allocated in Warehouse** field in the **Reservation** window.</span></span>  

### <a name="calculating-the-quantity-available-to-reserve"></a><span data-ttu-id="3429c-138">Beregne antall tilgjengelig for reservasjon</span><span class="sxs-lookup"><span data-stu-id="3429c-138">Calculating the Quantity Available to Reserve</span></span>  
 <span data-ttu-id="3429c-139">Antallet som er disponibelt for reservasjon, beregnes som følger:</span><span class="sxs-lookup"><span data-stu-id="3429c-139">The quantity available to reserve is calculated as follows:</span></span>  

 <span data-ttu-id="3429c-140">Antall tilgjengelige for reservasjon = Totalt antall på lager - Antallet i plukk og flyttinger for kildedokumenter - Reservert antall - Antall i utgående hyller</span><span class="sxs-lookup"><span data-stu-id="3429c-140">quantity available to reserve = total quantity in inventory - quantity on picks and movements for source documents - reserved quantity - quantity in outbound bins</span></span>  

 <span data-ttu-id="3429c-141">Diagrammet nedenfor viser de ulike elementene i beregningen.</span><span class="sxs-lookup"><span data-stu-id="3429c-141">The following diagram shows the different elements of the calculation.</span></span>  

 <span data-ttu-id="3429c-142">![Disponibelt for reservering, per lagerlokasjon](media/design_details_warehouse_management_availability_3.png "design_details_warehouse_management_availability_3")</span><span class="sxs-lookup"><span data-stu-id="3429c-142">![Avaliable to reserve, per warehouse allocations](media/design_details_warehouse_management_availability_3.png "design_details_warehouse_management_availability_3")</span></span>  

## <a name="see-also"></a><span data-ttu-id="3429c-143">Se også</span><span class="sxs-lookup"><span data-stu-id="3429c-143">See Also</span></span>  
 [<span data-ttu-id="3429c-144">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="3429c-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)

