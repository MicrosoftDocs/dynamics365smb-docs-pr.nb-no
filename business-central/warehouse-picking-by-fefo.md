---
title: Aktivere plukking etter FEFO | Microsoft-dokumentasjon
description: FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784070"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="39f76-103">Aktivere plukking av varer etter FEFO</span><span class="sxs-lookup"><span data-stu-id="39f76-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="39f76-104">FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.</span><span class="sxs-lookup"><span data-stu-id="39f76-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="39f76-105">Denne funksjonaliteten fungerer bare når følgende kriterier er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="39f76-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="39f76-106">Varen må ha et serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="39f76-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="39f76-107">På varens varesporingskodeoppsett må feltet **Lagers.nr. - sporing** eller feltet **Lagerparti - sporing** velges.</span><span class="sxs-lookup"><span data-stu-id="39f76-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="39f76-108">Varen må bokføres til lager med en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="39f76-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="39f76-109">På lokasjonen må valgene **Plukk nødv.**, **Plukk i henhold til FEFO** og **Hylle obligatorisk** være aktivert.</span><span class="sxs-lookup"><span data-stu-id="39f76-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="39f76-110">Når alle kriteriene er oppfylt, sorteres serie-/partinummererte varer som skal plukkes, med de eldste først i alle plukk og flyttinger, unntatt for varer som bruker SN-spesifikk eller partispesifikk sporing.</span><span class="sxs-lookup"><span data-stu-id="39f76-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="39f76-111">Hvis enkelte serie- eller partinummererte varer bruker spesifikk sporing, har disse førsteprioritet, og under disse vises de gjenstående, ikke-spesifikke serie-/partinumrene i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="39f76-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="39f76-112">Hvis to serie- eller partinummererte varer har samme utløpsdato, velges varen med lavest serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="39f76-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="39f76-113">Når du plukker serie- eller partinummererte varer i lokasjoner definert for lagerstyring, blir bare antall i hyller av typen *Plukk* plukket i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="39f76-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="39f76-114">Når du skal aktivere flyttinger i henhold til FEFO, må du la feltet **Fra hylle** stå tomt på siden **Lagerflytting** eller **Flytteforslag**.</span><span class="sxs-lookup"><span data-stu-id="39f76-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="39f76-115">Hvis feltet **Bruk ikke etter utløpsdato** er valgt på **kortet for varesporingskode**, blir bare varer som ikke er utgått, tatt med i plukkingen, og linjene sorteres i henhold til FEFO-prinsippet.</span><span class="sxs-lookup"><span data-stu-id="39f76-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="39f76-116">Se også</span><span class="sxs-lookup"><span data-stu-id="39f76-116">See Also</span></span>  
<span data-ttu-id="39f76-117">[Plukke varer](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="39f76-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="39f76-118">[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="39f76-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="39f76-119">[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="39f76-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="39f76-120">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="39f76-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="39f76-121">Lager</span><span class="sxs-lookup"><span data-stu-id="39f76-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="39f76-122">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39f76-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]