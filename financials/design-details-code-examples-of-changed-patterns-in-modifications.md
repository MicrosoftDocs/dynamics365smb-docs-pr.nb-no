---
title: "Designdetaljer – Lukke behov og forsyning | Microsoft-dokumentasjon"
description: "Når balanseringsprosessene for forsyning er utført, er det tre mulige sluttsituasjoner."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f682e2fdaa5be20ae8e6f3ff6ee2ff4769b48545
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-closing-demand-and-supply"></a><span data-ttu-id="4c2f9-103">Designdetaljer: Lukke behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="4c2f9-103">Design Details: Closing Demand and Supply</span></span>
<span data-ttu-id="4c2f9-104">Når balanseringsprosessene for forsyning er utført, er det tre mulige sluttsituasjoner:</span><span class="sxs-lookup"><span data-stu-id="4c2f9-104">When the supply balancing procedures have been performed, there are three possible end situations:</span></span>  

-   <span data-ttu-id="4c2f9-105">Nødvendig antall og dato for behovshendelsene er dekket, og planleggingen for dem kan lukkes.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-105">The required quantity and date of the demand events have been met and the planning for them can be closed.</span></span> <span data-ttu-id="4c2f9-106">Forsyningshendelsen er fortsatt åpen og kan kanskje dekke neste behov, slik at balanseringsprosessen kan starte på nytt med den gjeldende forsyningshendelsen og neste behov.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-106">The supply event is still open and may be able to cover the next demand, so the balancing procedure can start over with the current supply event and the next demand.</span></span>  

-   <span data-ttu-id="4c2f9-107">Forsyningsordren kan ikke endres slik at den dekker alle behov.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-107">The supply order cannot be modified to cover all of the demand.</span></span> <span data-ttu-id="4c2f9-108">Behovshendelsen er fortsatt åpen, med et ikke-dekket antall som kan dekkes av neste forsyningshendelse.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-108">The demand event is still open, with some uncovered quantity that may be covered by the next supply event.</span></span> <span data-ttu-id="4c2f9-109">Gjeldende forsyningshendelse blir dermed lukket, slik at balanseringen kan starte på nytt med det gjeldende behovet og neste forsyningshendelse.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-109">Thus the current supply event is closed, so the balancing act can start over with the current demand and the next supply event.</span></span>  

-   <span data-ttu-id="4c2f9-110">All etterspørsel er dekket. Det er ingen etterfølgende etterspørsel (eller det er ingen etterspørsel i det hele tatt).</span><span class="sxs-lookup"><span data-stu-id="4c2f9-110">All of the demand has been covered; there is no subsequent demand (or there has been no demand at all).</span></span> <span data-ttu-id="4c2f9-111">Hvis det finnes overskuddsforsyning, kan den reduseres (eller avbrytes) og deretter lukkes.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-111">If there is any surplus supply, it may be decreased (or canceled) and then closed.</span></span> <span data-ttu-id="4c2f9-112">Det kan hende det finnes flere forsyningshendelser videre i kjeden, og de må også avbrytes.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-112">It is possible that additional supply events exist further along in the chain, and they should also be canceled.</span></span>  

 <span data-ttu-id="4c2f9-113">Til slutt oppretter planleggingssystemet en ordresporingskoblingen mellom forsyning og behov.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-113">Last, the planning system will create an order tracking link between the supply and the demand.</span></span>  

## <a name="creating-the-planning-line-suggested-action"></a><span data-ttu-id="4c2f9-114">Opprette planleggingslinjen (foreslått handling)</span><span class="sxs-lookup"><span data-stu-id="4c2f9-114">Creating the Planning Line (Suggested Action)</span></span>  
 <span data-ttu-id="4c2f9-115">Hvis det foreslås en handling, Ny, Endre antall, Tidsplanlegg på nytt, Tidsplanlegg på nytt og endre antallet eller Avbryt, for å endre forsyningsordren, oppretter planleggingssystemet en planleggingslinje i planleggingsforslaget.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-115">If any action – New, Change Quantity, Reschedule, Reschedule and Change Quantity, or Cancel – is suggested to revise the supply order, the planning system creates a planning line in the planning worksheet.</span></span> <span data-ttu-id="4c2f9-116">Planleggingslinjen opprettes på grunn av ordresporing, ikke bare når forsyningshendelsen lukkes, men også hvis behovshendelsen lukkes, selv om forsyningshendelsen fremdeles er åpen og kan endres når neste behovshendelse behandles.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-116">Due to order tracking, the planning line is created not only when the supply event is closed, but also if the demand event is closed, even though the supply event is still open and may be subject to additional changes when the next demand event is processed.</span></span> <span data-ttu-id="4c2f9-117">Dette betyr at når planleggingslinjen først opprettes, kan den endres på nytt.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-117">This means that when first created, the planning line may be changed again.</span></span>  

 <span data-ttu-id="4c2f9-118">Du kan minimere databasetilgang ved håndtering av produksjonsordrer ved å vedlikeholde planleggingslinjen på tre nivåer og samtidig prøve å utføre det minst krevende vedlikeholdsnivået:</span><span class="sxs-lookup"><span data-stu-id="4c2f9-118">To minimize database access when handling production orders, the planning line can be maintained in three levels, while aiming to perform the least demanding maintenance level:</span></span>  

-   <span data-ttu-id="4c2f9-119">Opprett bare planleggingslinjen med gjeldende forfallsdato og antall, men uten ruting og komponenter.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-119">Create only the planning line with the current due date and quantity but without the routing and components.</span></span>  

-   <span data-ttu-id="4c2f9-120">Inkluder ruting: Den planlagte ruten settes opp, herunder beregning av start- og sluttdatoer og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-120">Include routing: the planned routing is laid out including calculation of starting and ending dates and times.</span></span> <span data-ttu-id="4c2f9-121">Dette er krevende når det gjelder databasetilgang.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-121">This is demanding in terms of database accesses.</span></span> <span data-ttu-id="4c2f9-122">For å fastslå slutt- og forfallsdatoene blir det kanskje nødvendig å beregne dette selv om forsyningshendelsen ikke er lukket (når det gjelder planlegging fremover).</span><span class="sxs-lookup"><span data-stu-id="4c2f9-122">To determine the ending and due dates, it may be necessary to calculate this even if the supply event has not been closed (in the case of forward scheduling).</span></span>  

-   <span data-ttu-id="4c2f9-123">Ta med stykklisteutfoldelse: Dette kan vente til like før forsyningshendelsen lukkes.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-123">Include BOM explosion: this can wait until just before the supply event is closed.</span></span>  

 <span data-ttu-id="4c2f9-124">Med dette avsluttes beskrivelsene av hvordan behov og forsyning lastes, prioriteres og balanseres av planleggingssystemet.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-124">This concludes the descriptions of how demand and supply is loaded, prioritized, and balanced by the planning system.</span></span> <span data-ttu-id="4c2f9-125">I integrering med denne aktiviteten for forsyningsplanlegging, må systemet sikre at nødvendig lagernivå opprettholdes for hver planlagt vare i henhold til sine gjenbestillingsprinsippene.</span><span class="sxs-lookup"><span data-stu-id="4c2f9-125">In integration with this supply planning activity, the system must ensure that the required inventory level of each planned item is maintained according to its reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c2f9-126">Se også</span><span class="sxs-lookup"><span data-stu-id="4c2f9-126">See Also</span></span>  
 <span data-ttu-id="4c2f9-127">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="4c2f9-127">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="4c2f9-128">[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="4c2f9-128">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="4c2f9-129">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="4c2f9-129">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

