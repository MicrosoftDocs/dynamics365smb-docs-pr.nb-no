---
title: "Designdetaljer – Rollen til tidsperioden | Microsoft-dokumentasjon"
description: "Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre."
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
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="13104-103">Designdetaljer: Rollen til tidsperioden</span><span class="sxs-lookup"><span data-stu-id="13104-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="13104-104">Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre.</span><span class="sxs-lookup"><span data-stu-id="13104-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  
  
 <span data-ttu-id="13104-105">Du kan angi en tidsperiode for gjenbestillingsprinsipper som bruker et gjenbestillingspunkt.</span><span class="sxs-lookup"><span data-stu-id="13104-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="13104-106">Dette sikrer at behov i samme tidsperiode akkumuleres før virkningen på den beregnede beholdningen kontrolleres, og før det kontrolleres om gjenbestillingspunktet er overskredet.</span><span class="sxs-lookup"><span data-stu-id="13104-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="13104-107">Hvis gjenbestillingspunktet er overskredet, blir det planlagt en ny forsyningsordre fremover fra slutten av perioden som er angitt av tidsperioden.</span><span class="sxs-lookup"><span data-stu-id="13104-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="13104-108">Tidsperiodene begynner på den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="13104-108">The time buckets begin on the planning starting date.</span></span>  
  
 <span data-ttu-id="13104-109">Tidsperiodebegrepet gjenspeiler den manuelle fremgangsmåten for å kontrollere lagernivået hyppig i stedet for ved hver transaksjon.</span><span class="sxs-lookup"><span data-stu-id="13104-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="13104-110">Brukeren må angi frekvensen (tidsperioden).</span><span class="sxs-lookup"><span data-stu-id="13104-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="13104-111">Brukeren samler for eksempel inn alle behov fra én leverandør for å registrere en ukentlig ordre.</span><span class="sxs-lookup"><span data-stu-id="13104-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  
  
 <span data-ttu-id="13104-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span><span class="sxs-lookup"><span data-stu-id="13104-112">![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")</span></span>  
  
 <span data-ttu-id="13104-113">Tidsperioden brukes vanligvis til å unngå en kaskadeeffekt.</span><span class="sxs-lookup"><span data-stu-id="13104-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="13104-114">Det opprettes for eksempel en balansert rad av behov og forsyning der et tidlig behov blir avbrutt, eller det opprettes en ny.</span><span class="sxs-lookup"><span data-stu-id="13104-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="13104-115">Resultatet blir at hver forsyningsordre (unntatt den siste) tidsplanlegges på nytt.</span><span class="sxs-lookup"><span data-stu-id="13104-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13104-116">Se også</span><span class="sxs-lookup"><span data-stu-id="13104-116">See Also</span></span>  
 <span data-ttu-id="13104-117">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="13104-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="13104-118">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="13104-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="13104-119">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="13104-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="13104-120">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="13104-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
