---
title: "Designdetaljer – Håndtere gjenbestillingsprinsipper | Microsoft-dokumentasjon"
description: "Oversikt over oppgaver for å definere en gjenbestillingspolicy ved forsyningsplanlegging."
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
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="6a11f-103">Designdetaljer: Håndtere gjenbestillingsprinsipper</span><span class="sxs-lookup"><span data-stu-id="6a11f-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="6a11f-104">Det må angis et gjenbestillingsprinsipp for at en vare skal kunne delta i forsyningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="6a11f-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="6a11f-105">Det finnes fire gjenbestillingsprinsipper:</span><span class="sxs-lookup"><span data-stu-id="6a11f-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="6a11f-106">Fast gjenbest.ant.</span><span class="sxs-lookup"><span data-stu-id="6a11f-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="6a11f-107">Maks.ant.</span><span class="sxs-lookup"><span data-stu-id="6a11f-107">Maximum Qty.</span></span>  
* <span data-ttu-id="6a11f-108">Bestilling</span><span class="sxs-lookup"><span data-stu-id="6a11f-108">Order</span></span>  
* <span data-ttu-id="6a11f-109">Parti for parti</span><span class="sxs-lookup"><span data-stu-id="6a11f-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="6a11f-110">Prinsippene Fast gjenbest.ant., og Maks.ant. som er relatert til lagerplanlegging.</span><span class="sxs-lookup"><span data-stu-id="6a11f-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="6a11f-111">Selv om lagerplanlegging teknisk sett er enklere enn fremgangsmåten for balansering, må disse policyene eksistere sammen med trinnvise balansering av forsynings- og ordresporing.</span><span class="sxs-lookup"><span data-stu-id="6a11f-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="6a11f-112">For å styre integrasjonen mellom dem og gi innsikt i planleggingslogikken som er involvert, finnes det strenge regler som bestemmer hvordan gjenbestillingsprinsipper skal håndteres.</span><span class="sxs-lookup"><span data-stu-id="6a11f-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6a11f-113">I denne delen</span><span class="sxs-lookup"><span data-stu-id="6a11f-113">In This Section</span></span>  
[<span data-ttu-id="6a11f-114">Designdetaljer: Rollen til gjenbestillingspunktet</span><span class="sxs-lookup"><span data-stu-id="6a11f-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="6a11f-115">Designdetaljer: Overvåke forventet lagernivå og gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="6a11f-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="6a11f-116">Designdetaljer: Rollen til tidsperioden</span><span class="sxs-lookup"><span data-stu-id="6a11f-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="6a11f-117">Designdetaljer: Holde seg under overflytnivået</span><span class="sxs-lookup"><span data-stu-id="6a11f-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="6a11f-118">Designdetaljer: Håndtere forventet negativ lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="6a11f-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="6a11f-119">Designdetaljer: Gjenbestillingsprinsipper</span><span class="sxs-lookup"><span data-stu-id="6a11f-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="6a11f-120">Se også</span><span class="sxs-lookup"><span data-stu-id="6a11f-120">See Also</span></span>  
<span data-ttu-id="6a11f-121">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="6a11f-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="6a11f-122">[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="6a11f-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="6a11f-123">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="6a11f-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="6a11f-124">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="6a11f-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="6a11f-125">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="6a11f-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
