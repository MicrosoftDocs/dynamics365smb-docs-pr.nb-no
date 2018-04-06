---
title: "Designdetaljer – Rollen til gjenbestillingspunktet | Microsoft-dokumentasjon"
description: "Dette emnet belyser viktigheten av å angi et gjenbestillingspunkt, slik at du vet når du må bestille mer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="e8611-103">Designdetaljer: Rollen til gjenbestillingspunktet</span><span class="sxs-lookup"><span data-stu-id="e8611-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="e8611-104">I tillegg til generell balansering av tilbud og etterspørsel må systemet også overvåke lagernivåer for de berørte varene for å overholde angitte gjenbestillingsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="e8611-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="e8611-105">Et gjenbestillingspunkt representerer etterspørselen i løpet av leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="e8611-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="e8611-106">Når den beregnede beholdningen går under lagernivået som defineres av gjenbestillingspunktet, er det på tide å bestille mer.</span><span class="sxs-lookup"><span data-stu-id="e8611-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="e8611-107">I mellomtiden forventes det at beholdningen gradvis reduseres og kanskje blir null (eller sikkerhetslagernivået) til etterfyllingen kommer.</span><span class="sxs-lookup"><span data-stu-id="e8611-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="e8611-108">Planleggingssystemet vil foreslå en fremoverplanlagt forsyningsordre når den forventede beholdning blir lavere enn gjenbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="e8611-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="e8611-109">Gjenbestillingspunktet gjenspeiler et bestemt beholdningsnivå.</span><span class="sxs-lookup"><span data-stu-id="e8611-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="e8611-110">Lagernivåer kan imidlertid endre seg betydelig i tidsperioden, og planleggingssystemet må derfor konstant overvåke beregnet disponibel beholdning.</span><span class="sxs-lookup"><span data-stu-id="e8611-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8611-111">Se også</span><span class="sxs-lookup"><span data-stu-id="e8611-111">See Also</span></span>  
<span data-ttu-id="e8611-112">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="e8611-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="e8611-113">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="e8611-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="e8611-114">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="e8611-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="e8611-115">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="e8611-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
