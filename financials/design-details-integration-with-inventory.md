---
title: "Designdetaljer – Integrasjon med lagerbeholdning | Microsoft-dokumentasjon"
description: Modulen Lagerstyring og modulen Lager samhandler med hverandre i vareopptelling og i lagerjustering.
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="36c1d-103">Designdetaljer: Integrasjon med lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="36c1d-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="36c1d-104">Modulen Lagerstyring og modulen Lager samhandler med hverandre i vareopptelling og i lagerjustering.</span><span class="sxs-lookup"><span data-stu-id="36c1d-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="36c1d-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="36c1d-105">Physical Inventory</span></span>  
 <span data-ttu-id="36c1d-106">Vinduet **Lagervareopptellingskladd** brukes med vinduet **Vareopptellingskladd** for alle avanserte lagerlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="36c1d-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="36c1d-107">Lageret beregnes på hyllenivå, og den lageransatte får en listeutskrift.</span><span class="sxs-lookup"><span data-stu-id="36c1d-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="36c1d-108">Listen viser hvilke varer som må telles i hvilke hyller.</span><span class="sxs-lookup"><span data-stu-id="36c1d-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="36c1d-109">Den lageransatte registrerer det opptalte antallet i vinduet **Lagervareopptellingskladd** og bokfører deretter kladden.</span><span class="sxs-lookup"><span data-stu-id="36c1d-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="36c1d-110">Hvis det opptalte antallet er større enn antallet på kladdelinjen, blir det bokført en bevegelse for denne forskjellen fra standard justeringshylle til hyllen som telles.</span><span class="sxs-lookup"><span data-stu-id="36c1d-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="36c1d-111">Dette øker antallet på den opptalte hyllen og reduserer antallet på standard justeringshylle.</span><span class="sxs-lookup"><span data-stu-id="36c1d-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="36c1d-112">Hvis det opptalte antallet er mindre enn antallet på kladdelinjen, blir det bokført en flytting for denne forskjellen fra den talte hyllen til standard justeringshylle.</span><span class="sxs-lookup"><span data-stu-id="36c1d-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="36c1d-113">Dette reduserer antallet på den opptalte hyllen og øker antallet på standard justeringshylle.</span><span class="sxs-lookup"><span data-stu-id="36c1d-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="36c1d-114">I avanserte lagerskonfigurasjoner blir verdien i feltet **Antall (beregnet)** hentet fra varepostene, og verdien i feltet **Antall (opptalt)** blir hentet fra lagerposter, unntatt justeringshylleinnholdet.</span><span class="sxs-lookup"><span data-stu-id="36c1d-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="36c1d-115">**Antall**-feltet angir forskjellen mellom de to første feltene, som skal være lik innholdet i justeringshyllen.</span><span class="sxs-lookup"><span data-stu-id="36c1d-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="36c1d-116">Når du bokfører vareopptellingskladden, oppdateres lageret og standard justeringshylle.</span><span class="sxs-lookup"><span data-stu-id="36c1d-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="36c1d-117">Lagerjusteringer i vareposten</span><span class="sxs-lookup"><span data-stu-id="36c1d-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="36c1d-118">Du bruker **Varekladd**-vinduet og funksjonen **Beregn lagerjustering** til å justere lagerbeholdningen i vareposten i samsvar med en justering som er gjort i vareantallet i en lagerhylle.</span><span class="sxs-lookup"><span data-stu-id="36c1d-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="36c1d-119">Hvis du vil opprette en kobling mellom beholdningen og lageret, må du definere en standard justeringshylle per lokasjon.</span><span class="sxs-lookup"><span data-stu-id="36c1d-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="36c1d-120">Standard justeringshylle registrerer varer på lageret når du bokfører en økning for lageret.</span><span class="sxs-lookup"><span data-stu-id="36c1d-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="36c1d-121">Hvis du bokfører en reduksjon, blir imidlertid antallet på standardhyllen også redusert.</span><span class="sxs-lookup"><span data-stu-id="36c1d-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="36c1d-122">I begge tilfeller blir det opprettet vareposter og lagerposter.</span><span class="sxs-lookup"><span data-stu-id="36c1d-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="36c1d-123">Justeringshyllen er ikke inkludert i tilgjengelighetsberegningen.</span><span class="sxs-lookup"><span data-stu-id="36c1d-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="36c1d-124">Hvis du vil justere hylleinnholdet, kan du bruke lagervarekladden der du kan angi varenummer, sonekode, hyllekode og antall som du vil justere.</span><span class="sxs-lookup"><span data-stu-id="36c1d-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="36c1d-125">Hvis du angir et positivt antall og bokfører linjen, økes beholdningen som er lagret på hyllen, og antallet i standard justeringshylle reduseres tilsvarende.</span><span class="sxs-lookup"><span data-stu-id="36c1d-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36c1d-126">Se også</span><span class="sxs-lookup"><span data-stu-id="36c1d-126">See Also</span></span>  
 <span data-ttu-id="36c1d-127">[Designdetaljer: Lagerstyring](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="36c1d-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="36c1d-128">Designdetaljer: Tilgjengelighet i lageret</span><span class="sxs-lookup"><span data-stu-id="36c1d-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
