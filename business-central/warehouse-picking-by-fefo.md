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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ae07bc4f1d9f348f08f591e5e4341938ec4b5f16
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382207"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="0d3f6-103">Aktivere plukking av varer etter FEFO</span><span class="sxs-lookup"><span data-stu-id="0d3f6-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="0d3f6-104">FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="0d3f6-105">Denne funksjonaliteten fungerer bare når følgende kriterier er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="0d3f6-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="0d3f6-106">Varen må ha et serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="0d3f6-107">På varens varesporingskodeoppsett må feltet **Lagers.nr. - sporing** eller feltet **Lagerparti - sporing** velges.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="0d3f6-108">Varen må bokføres til lager med en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="0d3f6-109">Det må merkes av for **Plukk nødv.** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="0d3f6-110">Det må merkes av for **Plukk i henhold til FEFO** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="0d3f6-111">Det må merkes av for **Hylle obligatorisk** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="0d3f6-112">Når alle kriteriene er oppfylt, sorteres serie-/partinummererte varer som skal plukkes, med de eldste først i alle plukk og flyttinger, unntatt for varer som bruker SN-spesifikk eller partispesifikk sporing.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="0d3f6-113">Hvis enkelte serie-/partinummererte varer bruker spesifikk sporing, har disse førsteprioritet, og under disse vises de gjenstående, ikke-spesifikke serie-/partinumrene i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="0d3f6-114">Hvis to serie-/partinummererte varer har samme utløpsdato, velges varen med lavest serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="0d3f6-115">Når du plukker serie-/partinummererte varer i lokasjoner definert for lagerstyring, blir bare antall i hyller av typen *Plukk* plukket i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="0d3f6-116">Når du skal aktivere flyttinger i henhold til FEFO, må du la **Fra hylle**-feltet stå tomt på siden **Lagerflytting** eller **Flytteforslag**.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="0d3f6-117">Hvis feltet **Bruk ikke etter utløpsdato** er valgt, inkluderes bare varer som ikke er utløpt, i plukkingen.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="0d3f6-118">Dette gjelder selv om du ikke bruker plukk i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d3f6-119">Se også</span><span class="sxs-lookup"><span data-stu-id="0d3f6-119">See Also</span></span>  
<span data-ttu-id="0d3f6-120">[Plukke varer](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="0d3f6-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="0d3f6-121">[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="0d3f6-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="0d3f6-122">[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="0d3f6-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="0d3f6-123">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="0d3f6-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="0d3f6-124">Lager</span><span class="sxs-lookup"><span data-stu-id="0d3f6-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0d3f6-125">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d3f6-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]