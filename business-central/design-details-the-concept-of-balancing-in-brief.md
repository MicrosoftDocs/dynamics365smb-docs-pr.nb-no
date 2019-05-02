---
title: Designdetaljer – Kort om begrepet balansering | Microsoft-dokumentasjon
description: Behovet er gitt av selskapets kunder. Forsyning er det selskapet kan opprette og fjerne for å skape balanse. Planleggingssystemet starter med det uavhengige behovet og sporer deretter bakover til forsyningen.
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
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: ccf9857752fffd873e171880274a5a039c69bdec
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802932"
---
# <a name="design-details-the-concept-of-balancing-in-brief"></a><span data-ttu-id="f0068-105">Designdetaljer: Kort om begrepet balansering</span><span class="sxs-lookup"><span data-stu-id="f0068-105">Design Details: The Concept of Balancing in Brief</span></span>
<span data-ttu-id="f0068-106">Behovet er gitt av selskapets kunder.</span><span class="sxs-lookup"><span data-stu-id="f0068-106">Demand is given by a company’s customers.</span></span> <span data-ttu-id="f0068-107">Forsyning er det selskapet kan opprette og fjerne for å skape balanse.</span><span class="sxs-lookup"><span data-stu-id="f0068-107">Supply is what the company can create and remove to establish balance.</span></span> <span data-ttu-id="f0068-108">Planleggingssystemet starter med det uavhengige behovet og sporer deretter bakover til forsyningen.</span><span class="sxs-lookup"><span data-stu-id="f0068-108">The planning system starts with the independent demand and then tracks backwards to the supply.</span></span>  

 <span data-ttu-id="f0068-109">Beholdningsprofilene brukes til å lagre informasjon om behov og forsyninger, antall og tidsberegning.</span><span class="sxs-lookup"><span data-stu-id="f0068-109">The inventory profiles are used to contain information about the demands and supplies, quantities, and timing.</span></span> <span data-ttu-id="f0068-110">Disse profilene utgjør i hovedsak de to sidene av balanseringsskalaen.</span><span class="sxs-lookup"><span data-stu-id="f0068-110">These profiles essentially make up the two sides of the balancing scale.</span></span>  

 <span data-ttu-id="f0068-111">Formålet med planleggingsmekanismen er å utligne behovet for og forsyningen av en vare for å sikre at forsyningen samsvarer med behovet, og å gjøre dette på en passende måte som defineres av planleggingsparameterne og -reglene.</span><span class="sxs-lookup"><span data-stu-id="f0068-111">The objective of the planning mechanism is to counterbalance the demand and supply of an item to ensure that supply will match demand in a feasible way as defined by the planning parameters and rules.</span></span>  

 <span data-ttu-id="f0068-112">![Oversikt over balansering mellom forsyningen og behov](media/nav_app_supply_planning_2_balancing.png "Oversikt over balansering mellom forsyningen og behov")</span><span class="sxs-lookup"><span data-stu-id="f0068-112">![Overview of supply-demand balancing](media/nav_app_supply_planning_2_balancing.png "Overview of supply-demand balancing")</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0068-113">Se også</span><span class="sxs-lookup"><span data-stu-id="f0068-113">See Also</span></span>  
 <span data-ttu-id="f0068-114">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="f0068-114">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="f0068-115">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="f0068-115">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="f0068-116">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="f0068-116">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)