---
title: Aktivere plukking etter FEFO | Microsoft-dokumentasjon
description: FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 54857d668cdceb9cc1d4e035a496d621b1d9459b
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802610"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="5370a-103">Aktivere plukking av varer etter FEFO</span><span class="sxs-lookup"><span data-stu-id="5370a-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="5370a-104">FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.</span><span class="sxs-lookup"><span data-stu-id="5370a-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="5370a-105">Denne funksjonaliteten fungerer bare når følgende kriterier er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="5370a-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="5370a-106">Varen må ha et serie-/partinummer.</span><span class="sxs-lookup"><span data-stu-id="5370a-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="5370a-107">På varens varesporingskodeoppsett må feltet **Lagerporing basert på s.nr.** eller feltet **Lagersporing basert på parti** velges.</span><span class="sxs-lookup"><span data-stu-id="5370a-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="5370a-108">Varen må bokføres til lager med en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="5370a-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="5370a-109">Det må merkes av for **Plukk nødv.** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="5370a-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="5370a-110">Det må merkes av for **Plukk i henhold til FEFO** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="5370a-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="5370a-111">Det må merkes av for **Hylle obligatorisk** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="5370a-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="5370a-112">Når alle kriteriene er oppfylt, sorteres serie-/partinummererte varer som skal plukkes, med de eldste først i alle plukk og flyttinger, unntatt for varer som bruker SN-spesifikk eller partispesifikk sporing.</span><span class="sxs-lookup"><span data-stu-id="5370a-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5370a-113">Hvis enkelte serie-/partinummererte varer bruker spesifikk sporing, har disse førsteprioritet, og under disse vises de gjenstående, ikke-spesifikke serie-/partinumrene i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="5370a-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="5370a-114">Hvis to serie-/partinummererte varer har samme utløpsdato, velges varen med lavest serie- eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="5370a-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="5370a-115">Når du plukker serie-/partinummererte varer i lokasjoner definert for lagerstyring, blir bare antall i hyller av typen *Plukk* plukket i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="5370a-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="5370a-116">Når du skal aktivere flyttinger i henhold til FEFO, må du la **Fra hylle**-feltet stå tomt på siden **Lagerflytting** eller **Flytteforslag**.</span><span class="sxs-lookup"><span data-stu-id="5370a-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="5370a-117">Hvis feltet **Bruk ikke etter utløpsdato** er valgt, inkluderes bare varer som ikke er utløpt, i plukkingen.</span><span class="sxs-lookup"><span data-stu-id="5370a-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="5370a-118">Dette gjelder selv om du ikke bruker plukk i henhold til FEFO.</span><span class="sxs-lookup"><span data-stu-id="5370a-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="5370a-119">Se også</span><span class="sxs-lookup"><span data-stu-id="5370a-119">See Also</span></span>  
<span data-ttu-id="5370a-120">[Plukke varer](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="5370a-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="5370a-121">[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="5370a-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="5370a-122">[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="5370a-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="5370a-123">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="5370a-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="5370a-124">Lager</span><span class="sxs-lookup"><span data-stu-id="5370a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5370a-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5370a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
