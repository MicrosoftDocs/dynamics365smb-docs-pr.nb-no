---
title: Designdetaljer – Rollen til gjenbestillingspunktet | Microsoft-dokumentasjon
description: Dette emnet belyser viktigheten av å angi et gjenbestillingspunkt, slik at du vet når du må bestille mer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "924190"
---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="fb372-103">Designdetaljer: Rollen til gjenbestillingspunktet</span><span class="sxs-lookup"><span data-stu-id="fb372-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="fb372-104">I tillegg til generell balansering av tilbud og etterspørsel må systemet også overvåke lagernivåer for de berørte varene for å overholde angitte gjenbestillingsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="fb372-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  

<span data-ttu-id="fb372-105">Et gjenbestillingspunkt representerer etterspørselen i løpet av leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="fb372-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="fb372-106">Når den beregnede beholdningen går under lagernivået som defineres av gjenbestillingspunktet, er det på tide å bestille mer.</span><span class="sxs-lookup"><span data-stu-id="fb372-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="fb372-107">I mellomtiden forventes det at beholdningen gradvis reduseres og kanskje blir null (eller sikkerhetslagernivået) til etterfyllingen kommer.</span><span class="sxs-lookup"><span data-stu-id="fb372-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  

<span data-ttu-id="fb372-108">Planleggingssystemet vil foreslå en fremoverplanlagt forsyningsordre når den forventede beholdning blir lavere enn gjenbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="fb372-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  

<span data-ttu-id="fb372-109">Gjenbestillingspunktet gjenspeiler et bestemt beholdningsnivå.</span><span class="sxs-lookup"><span data-stu-id="fb372-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="fb372-110">Lagernivåer kan imidlertid endre seg betydelig i tidsperioden, og planleggingssystemet må derfor konstant overvåke beregnet disponibel beholdning.</span><span class="sxs-lookup"><span data-stu-id="fb372-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb372-111">Se også</span><span class="sxs-lookup"><span data-stu-id="fb372-111">See Also</span></span>  
<span data-ttu-id="fb372-112">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fb372-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="fb372-113">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="fb372-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="fb372-114">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fb372-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="fb372-115">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="fb372-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
