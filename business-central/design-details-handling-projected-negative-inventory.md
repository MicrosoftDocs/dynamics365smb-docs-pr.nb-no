---
title: "Designdetaljer – Håndtere forventet negativ lagerbeholdning | Microsoft-dokumentasjon"
description: "Gjenbestillingspunktet uttrykker forventet behov i løpet av leveringstiden for varen. Når gjenbestillingspunktet passeres, er det på tide å bestille mer. Det forventede beholdningsnivået må være stort nok til å dekke behovet til den nye ordren mottas. I mellomtiden håndterer sikkerhetslageret svingninger i behovet opptil et servicenivåmål."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: cfedced3a1e7ccf94294ebd36f4fb5311fd1933e
ms.contentlocale: nb-no
ms.lasthandoff: 11/20/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="527e9-106">Designdetaljer: Håndtere forventet negativ lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="527e9-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="527e9-107">Gjenbestillingspunktet uttrykker forventet behov i løpet av leveringstiden for varen.</span><span class="sxs-lookup"><span data-stu-id="527e9-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="527e9-108">Når gjenbestillingspunktet passeres, er det på tide å bestille mer.</span><span class="sxs-lookup"><span data-stu-id="527e9-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="527e9-109">Det forventede beholdningsnivået må være stort nok til å dekke behovet til den nye ordren mottas.</span><span class="sxs-lookup"><span data-stu-id="527e9-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="527e9-110">I mellomtiden håndterer sikkerhetslageret svingninger i behovet opptil et servicenivåmål.</span><span class="sxs-lookup"><span data-stu-id="527e9-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="527e9-111">Planleggingssystemet anser det derfor som en nødssituasjon hvis et fremtidig behov ikke kan betjenes fra den beregnede beholdningen, eller uttrykt i en annen måte, den beregnede beholdningen blir negativ.</span><span class="sxs-lookup"><span data-stu-id="527e9-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="527e9-112">Systemet håndterer et slikt unntak ved å foreslå en ny forsyningsordre som dekker en del av behovet som ikke kan dekkes av lageret eller annen forsyning.</span><span class="sxs-lookup"><span data-stu-id="527e9-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="527e9-113">Ordrestørrelsen på den nye forsyningsordren tar ikke maksimumsbeholdningen eller gjenbestillingsantallet med i betraktningen. Den tar heller ikke ordremodifikatorene Maks. bestillingsantall, Min. bestillingsantall og Bestillingsfaktor med i betraktningen.</span><span class="sxs-lookup"><span data-stu-id="527e9-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="527e9-114">I stedet gjenspeiles den nøyaktige mangelen.</span><span class="sxs-lookup"><span data-stu-id="527e9-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="527e9-115">Planleggingslinjen for denne typen forsyningsordre har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag for å informere brukeren om situasjonen.</span><span class="sxs-lookup"><span data-stu-id="527e9-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="527e9-116">I illustrasjonen nedenfor representerer forsyning D en kritisk bestilling for å justere for negativt lager.</span><span class="sxs-lookup"><span data-stu-id="527e9-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="527e9-117">![Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning](media/nav_app_supply_planning_2_negative_inventory.png "Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning")</span><span class="sxs-lookup"><span data-stu-id="527e9-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="527e9-118">Forsyning **A**, opprinnelig beregnet beholdning, er under gjenbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="527e9-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="527e9-119">Det opprettes en ny foroverplanlagt forsyning (**C**).</span><span class="sxs-lookup"><span data-stu-id="527e9-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="527e9-120">(Antall = Maks. beholdning – Forventet beholdningsnivå)</span><span class="sxs-lookup"><span data-stu-id="527e9-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="527e9-121">Forsyning **A** lukkes av behov **B**, som ikke er helt dekket.</span><span class="sxs-lookup"><span data-stu-id="527e9-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="527e9-122">(Behov **B** kan prøve å planlegge forsyning C i, men det vil ikke skje i henhold til tidsperiodekonseptet.)</span><span class="sxs-lookup"><span data-stu-id="527e9-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="527e9-123">Ny forsyning (**D**) blir opprettet for å dekke det gjenværende antallsbehovet **B**.</span><span class="sxs-lookup"><span data-stu-id="527e9-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="527e9-124">Behovet **B** er lukket (opprette en påminnelse til beregnet beholdning).</span><span class="sxs-lookup"><span data-stu-id="527e9-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="527e9-125">Den nye forsyningen **D** lukkes.</span><span class="sxs-lookup"><span data-stu-id="527e9-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="527e9-126">Beregnet beholdning er kontrollert. Gjenbestillingspunktet er ikke overskredet.</span><span class="sxs-lookup"><span data-stu-id="527e9-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="527e9-127">Forsyning **C** lukkes (det finnes ikke mer behov).</span><span class="sxs-lookup"><span data-stu-id="527e9-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="527e9-128">Sluttkontroll: Det finnes ingen utestående påminnelser for beholdningsnivå.</span><span class="sxs-lookup"><span data-stu-id="527e9-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="527e9-129">Trinn 4 viser hvordan systemet reagerer i versjoner før Microsoft Dynamics NAV 2009 SP1.</span><span class="sxs-lookup"><span data-stu-id="527e9-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="527e9-130">Med dette avsluttes beskrivelsen av sentrale prinsipper vedrørende lagerplanlegging basert på gjenbestillingsprinsipper.</span><span class="sxs-lookup"><span data-stu-id="527e9-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="527e9-131">Følgende del beskriver egenskapene til de fire gjenbestillingsprinsippene som støttes.</span><span class="sxs-lookup"><span data-stu-id="527e9-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="527e9-132">Se også</span><span class="sxs-lookup"><span data-stu-id="527e9-132">See Also</span></span>  
 <span data-ttu-id="527e9-133">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="527e9-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="527e9-134">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="527e9-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="527e9-135">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="527e9-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="527e9-136">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="527e9-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

