---
title: "Designdetaljer – Håndtere ordrer før den planlagte startdatoen | Microsoft-dokumentasjon"
description: Dette emnet beskriver reglene som planlegging gjelder for bestillinger i den frosne sonen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5545fe1c2c8833eb1c97765f261777cbb1781098
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a><span data-ttu-id="210c4-103">Designdetaljer: Håndtere ordrer før den planlagte startdatoen</span><span class="sxs-lookup"><span data-stu-id="210c4-103">Design Details: Dealing with Orders Before the Planning Starting Date</span></span>
<span data-ttu-id="210c4-104">For å unngå at en leveringsplan viser umulige og dermed ubrukelige forslag, regner planleggingssystemet perioden frem til den planlagte startdatoen som en frossen sone der ingenting er planlagt.</span><span class="sxs-lookup"><span data-stu-id="210c4-104">To avoid that a supply plan shows impossible and therefore useless suggestions, the planning system regards the period up until the planning starting date a frozen zone where nothing is planned for.</span></span> <span data-ttu-id="210c4-105">Følgende regel gjelder den frosne sonen:</span><span class="sxs-lookup"><span data-stu-id="210c4-105">The following rule applies to the frozen zone:</span></span>  
  
<span data-ttu-id="210c4-106">Alle tilbud og etterspørsel før startdatoen for planleggingsperioden blir betraktet som en del av beholdningen eller levert.</span><span class="sxs-lookup"><span data-stu-id="210c4-106">All supply and demand before the starting date of the planning period will be considered a part of inventory or shipped.</span></span>  
  
<span data-ttu-id="210c4-107">Planleggingssystemet vil derfor ikke, med noen få unntak, foreslå endringer for forsyningsordrer i den frosne sonen, og ingen koblinger for ordresporing opprettes eller vedlikeholdes for denne perioden.</span><span class="sxs-lookup"><span data-stu-id="210c4-107">Accordingly, the planning system will not, with a few exceptions, suggest any changes to supply orders in the frozen zone, and no order tracking links are created or maintained for that period.</span></span>  
  
<span data-ttu-id="210c4-108">Unntakene fra denne regelen er som følger:</span><span class="sxs-lookup"><span data-stu-id="210c4-108">The exceptions to this rule are as follows:</span></span>  
  
* <span data-ttu-id="210c4-109">Hvis forventet disponibel beholdning, inkludert summen av forsyning og behov i den frosne sonen, er under null.</span><span class="sxs-lookup"><span data-stu-id="210c4-109">If the projected available inventory, including the sum of supply and demand in the frozen zone, is below zero.</span></span>  
* <span data-ttu-id="210c4-110">Hvis serie-/partinumre er nødvendige på tilbakedaterte ordre(r).</span><span class="sxs-lookup"><span data-stu-id="210c4-110">If serial/lot numbers are required on the backdated order(s).</span></span>  
* <span data-ttu-id="210c4-111">Hvis forsyningsbehovsettet er koblet til et ordre-til-ordre-prinsipp.</span><span class="sxs-lookup"><span data-stu-id="210c4-111">If the supply-demand set is linked by an order-to-order policy.</span></span>  
  
<span data-ttu-id="210c4-112">Hvis den første disponible beholdningen er under null, foreslår planleggingssystemet en kritisk ordre på dagen før planleggingsperioden, for å dekke antallet som mangler.</span><span class="sxs-lookup"><span data-stu-id="210c4-112">If the initial available inventory is below zero, the planning system suggests an emergency supply order on the day before the planning period to cover the missing quantity.</span></span> <span data-ttu-id="210c4-113">Forventet og tilgjengelige beholdning vil derfor alltid være minst null når planlegging for den fremtidige perioden begynner.</span><span class="sxs-lookup"><span data-stu-id="210c4-113">Consequently, the projected and available inventory will always be at least zero when planning for the future period begins.</span></span> <span data-ttu-id="210c4-114">Planleggingslinjen for denne forsyningsordren har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag.</span><span class="sxs-lookup"><span data-stu-id="210c4-114">The planning line for this supply order will display an Emergency warning icon and additional information is provided upon lookup.</span></span>  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a><span data-ttu-id="210c4-115">Serie-/partinumre og ordre-til-ordre-koblinger er fritatt fra den frosne sonen</span><span class="sxs-lookup"><span data-stu-id="210c4-115">Serial/Lot Numbers and Order-to-Order Links are Exempt from the Frozen Zone</span></span>  
<span data-ttu-id="210c4-116">Hvis serie-/partinumre er nødvendige eller det finnes en ordre-til-ordre-kobling, vil planleggingssystemet se bort fra den frosne sonen og inkludere slike antall som er tilbakedaterte fra startdatoen og potensielt foreslå korrigerende handlinger hvis behov og forsyning ikke er synkronisert.</span><span class="sxs-lookup"><span data-stu-id="210c4-116">If serial/lot numbers are required or an order-to-order link exists, the planning system will disregard the frozen zone and incorporate such quantities that are back-dated from the starting date and potentially suggest corrective actions if demand and supply is not synchronized.</span></span> <span data-ttu-id="210c4-117">Forretningsårsaken til dette prinsippet er at slike bestemte sett med behov/forsyning må samsvare for å sikre at dette bestemte behovet dekkes.</span><span class="sxs-lookup"><span data-stu-id="210c4-117">The business reason for this principle is that such specific demand-supply sets must match to ensure that this specific demand is fulfilled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="210c4-118">Se også</span><span class="sxs-lookup"><span data-stu-id="210c4-118">See Also</span></span>  
<span data-ttu-id="210c4-119">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="210c4-119">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="210c4-120">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="210c4-120">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="210c4-121">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="210c4-121">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
