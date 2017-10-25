---
title: Spore relasjoner mellom behov og forsyning | Microsoft-dokumentasjon
description: "Fra ethvert forsynings- eller behovsdokument i det såkalte ordrenettverket kan du spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 511381e4f6d469ff16714a30fde60d3e238ad975
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-track-relations-between-demand-and-supply"></a><span data-ttu-id="7ed15-103">Spore relasjoner mellom behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="7ed15-103">How to: Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="7ed15-104">Fra ethvert forsynings- eller behovsdokument i det såkalte ordrenettverket kan du spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="7ed15-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="7ed15-105">Planleggingsforslagene gir også støtteinformasjon for planlegging for ikke-ordreenheter for å hjelpe planleggeren med å opprette en optimal forsyningsplan.</span><span class="sxs-lookup"><span data-stu-id="7ed15-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="7ed15-106">Hvis du vil ha mer informasjon, kan du se delen Ikke-sporet planleggingselement.</span><span class="sxs-lookup"><span data-stu-id="7ed15-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="7ed15-107">Spore tilknyttede varer</span><span class="sxs-lookup"><span data-stu-id="7ed15-107">To track linked items</span></span>
<span data-ttu-id="7ed15-108">Sporing viser hvordan ordrer, produksjonsordrer og bestillinger er knyttet til produksjonsordrer gjennom planleggings- og reservasjonssystemer.</span><span class="sxs-lookup"><span data-stu-id="7ed15-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="7ed15-109">Nedenfor beskrives hvordan du kan spore tilknyttede varer på en fast planlagt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="7ed15-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="7ed15-110">Fremgangsmåten er lik for alle andre ordretyper og fra planleggingsforslagslinjer.</span><span class="sxs-lookup"><span data-stu-id="7ed15-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="7ed15-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Fast planlagte prod.ordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="7ed15-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="7ed15-112">Åpne den aktuelle fast planlagte produksjonsordren fra oversikten.</span><span class="sxs-lookup"><span data-stu-id="7ed15-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="7ed15-113">På hurtigfanen **Linjer** velger du **Funksjoner**-handlingen og deretter **Sporing**.</span><span class="sxs-lookup"><span data-stu-id="7ed15-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="7ed15-114">Linjene i **Sporing**-vinduet viser hvilke dokumenter som er knyttet til den aktuelle produksjonsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="7ed15-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="7ed15-115">Ikke-sporede planleggingselementer</span><span class="sxs-lookup"><span data-stu-id="7ed15-115">Untracked Planning Elements</span></span>
<span data-ttu-id="7ed15-116">Vinduet **Ikke-sporede planleggingselementer** åpnes når du velger feltet **Ikke-sporet antall** i vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="7ed15-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="7ed15-117">Det har to formål:</span><span class="sxs-lookup"><span data-stu-id="7ed15-117">It serves two purposes:</span></span>

1. <span data-ttu-id="7ed15-118">Inneholde informasjon om ikke-sporede antall som vises når brukeren slår opp ikke-sporede antall fra Sporing-vinduet.</span><span class="sxs-lookup"><span data-stu-id="7ed15-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="7ed15-119">Inneholde advarsler som vises når brukeren klikker et **advarselsikon** i vinduet **Planleggingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="7ed15-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="7ed15-120">Vinduet inneholder poster som gjør rede for et ikke-sporet overskuddsantall i ordresporingsnettverket.</span><span class="sxs-lookup"><span data-stu-id="7ed15-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="7ed15-121">Disse postene genereres under planleggingskjøringen og forklarer hvor det ikke-sporede overskuddsantallet på sporingslinjene kommer fra.</span><span class="sxs-lookup"><span data-stu-id="7ed15-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="7ed15-122">Dette ikke-sporede overskuddet kan komme fra:</span><span class="sxs-lookup"><span data-stu-id="7ed15-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="7ed15-123">Produksjonsprognose</span><span class="sxs-lookup"><span data-stu-id="7ed15-123">Production forecast</span></span>
- <span data-ttu-id="7ed15-124">Rammeordrer</span><span class="sxs-lookup"><span data-stu-id="7ed15-124">Blanket orders</span></span>
- <span data-ttu-id="7ed15-125">Sikkerhetslagerantall</span><span class="sxs-lookup"><span data-stu-id="7ed15-125">Safety stock quantity</span></span>
- <span data-ttu-id="7ed15-126">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="7ed15-126">Reorder point</span></span>
- <span data-ttu-id="7ed15-127">Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="7ed15-127">Maximum inventory</span></span>
- <span data-ttu-id="7ed15-128">Gjenbestillingsantall</span><span class="sxs-lookup"><span data-stu-id="7ed15-128">Reorder quantity</span></span>
- <span data-ttu-id="7ed15-129">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="7ed15-129">Maximum order quantity</span></span>
- <span data-ttu-id="7ed15-130">Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="7ed15-130">Minimum order quantity</span></span>
- <span data-ttu-id="7ed15-131">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="7ed15-131">Order multiple</span></span>
- <span data-ttu-id="7ed15-132">Avdemping (% av partistr.)</span><span class="sxs-lookup"><span data-stu-id="7ed15-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="7ed15-133">Se også</span><span class="sxs-lookup"><span data-stu-id="7ed15-133">See Also</span></span>  
<span data-ttu-id="7ed15-134">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7ed15-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="7ed15-135">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="7ed15-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="7ed15-136">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="7ed15-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="7ed15-137">Lager</span><span class="sxs-lookup"><span data-stu-id="7ed15-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="7ed15-138">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="7ed15-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="7ed15-139">Designdetaljer: Reservasjon, sporing og handlingsmeldinger</span><span class="sxs-lookup"><span data-stu-id="7ed15-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="7ed15-140">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="7ed15-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="7ed15-141">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="7ed15-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="7ed15-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7ed15-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

