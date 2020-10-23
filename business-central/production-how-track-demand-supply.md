---
title: Spore relasjoner mellom behov og forsyning | Microsoft-dokumentasjon
description: Fra ethvert forsynings- eller behovsdokument i det såkalte ordrenettverket kan du spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3d053de6193593256e404803d61b14f4681dc771
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921536"
---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="84df2-103">Spore relasjoner mellom behov og forsyning</span><span class="sxs-lookup"><span data-stu-id="84df2-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="84df2-104">Fra ethvert forsynings- eller behovsdokument i det såkalte ordrenettverket kan du spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen.</span><span class="sxs-lookup"><span data-stu-id="84df2-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="84df2-105">Planleggingsforslagene gir også støtteinformasjon for planlegging for ikke-ordreenheter for å hjelpe planleggeren med å opprette en optimal forsyningsplan.</span><span class="sxs-lookup"><span data-stu-id="84df2-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="84df2-106">Hvis du vil ha mer informasjon, kan du se [Ikke-sporet planleggingselement](production-how-track-demand-supply.md#untracked-planning-elements).</span><span class="sxs-lookup"><span data-stu-id="84df2-106">For more information, see [Untracked Planning Elements](production-how-track-demand-supply.md#untracked-planning-elements).</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="84df2-107">Spore tilknyttede varer</span><span class="sxs-lookup"><span data-stu-id="84df2-107">To track linked items</span></span>
<span data-ttu-id="84df2-108">Sporing viser hvordan ordrer, produksjonsordrer og bestillinger er knyttet til produksjonsordrer gjennom planleggings- og reservasjonssystemer.</span><span class="sxs-lookup"><span data-stu-id="84df2-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="84df2-109">Nedenfor beskrives hvordan du kan spore tilknyttede varer på en fast planlagt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="84df2-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="84df2-110">Fremgangsmåten er lik for alle andre ordretyper og fra planleggingsforslagslinjer.</span><span class="sxs-lookup"><span data-stu-id="84df2-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="84df2-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagt prod.ordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="84df2-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="84df2-112">Åpne den aktuelle fast planlagte produksjonsordren fra oversikten.</span><span class="sxs-lookup"><span data-stu-id="84df2-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="84df2-113">På hurtigfanen **Linjer** velger du **Funksjoner**-handlingen og deretter **Sporing**.</span><span class="sxs-lookup"><span data-stu-id="84df2-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="84df2-114">Linjene i **Sporing**-vinduet viser hvilke dokumenter som er knyttet til den aktuelle produksjonsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="84df2-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="84df2-115">Ikke-sporede planleggingselementer</span><span class="sxs-lookup"><span data-stu-id="84df2-115">Untracked Planning Elements</span></span>
<span data-ttu-id="84df2-116">Siden **Ikke-sporede planleggingselementer** åpnes når du velger feltet **Ikke-sporet antall** på siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="84df2-116">The **Untracked Planning Elements** page opens when you choose the **Untracked Qty.** field on the **order Planning** page.</span></span> <span data-ttu-id="84df2-117">Det har to formål:</span><span class="sxs-lookup"><span data-stu-id="84df2-117">It serves two purposes:</span></span>

1. <span data-ttu-id="84df2-118">Inneholde informasjon om ikke-sporede antall som vises når brukeren slår opp ikke-sporede antall fra Sporing-siden.</span><span class="sxs-lookup"><span data-stu-id="84df2-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking page to see untracked quantities.</span></span>
2. <span data-ttu-id="84df2-119">Inneholde advarsler som vises når brukeren klikker et **advarselsikon** på siden **Planleggingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="84df2-119">To hold warning messages displayed when the user chooses the **Warning** icon on the **Planning Worksheet** page.</span></span>

<span data-ttu-id="84df2-120">Siden inneholder poster som gjør rede for et ikke-sporet overskuddsantall i ordresporingsnettverket.</span><span class="sxs-lookup"><span data-stu-id="84df2-120">The page contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="84df2-121">Disse postene genereres under planleggingskjøringen og forklarer hvor det ikke-sporede overskuddsantallet på sporingslinjene kommer fra.</span><span class="sxs-lookup"><span data-stu-id="84df2-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="84df2-122">Dette ikke-sporede overskuddet kan komme fra:</span><span class="sxs-lookup"><span data-stu-id="84df2-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="84df2-123">Produksjonsprognose</span><span class="sxs-lookup"><span data-stu-id="84df2-123">Production forecast</span></span>
- <span data-ttu-id="84df2-124">Rammeordrer</span><span class="sxs-lookup"><span data-stu-id="84df2-124">Blanket orders</span></span>
- <span data-ttu-id="84df2-125">Sikkerhetslagerantall</span><span class="sxs-lookup"><span data-stu-id="84df2-125">Safety stock quantity</span></span>
- <span data-ttu-id="84df2-126">Gjenbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="84df2-126">Reorder point</span></span>
- <span data-ttu-id="84df2-127">Maks. beholdning</span><span class="sxs-lookup"><span data-stu-id="84df2-127">Maximum inventory</span></span>
- <span data-ttu-id="84df2-128">Gjenbestillingsantall</span><span class="sxs-lookup"><span data-stu-id="84df2-128">Reorder quantity</span></span>
- <span data-ttu-id="84df2-129">Maks. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="84df2-129">Maximum order quantity</span></span>
- <span data-ttu-id="84df2-130">Min. bestillingsantall</span><span class="sxs-lookup"><span data-stu-id="84df2-130">Minimum order quantity</span></span>
- <span data-ttu-id="84df2-131">Bestillingsfaktor</span><span class="sxs-lookup"><span data-stu-id="84df2-131">Order multiple</span></span>
- <span data-ttu-id="84df2-132">Avdemping (% av partistr.)</span><span class="sxs-lookup"><span data-stu-id="84df2-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="84df2-133">Se også</span><span class="sxs-lookup"><span data-stu-id="84df2-133">See Also</span></span>  
<span data-ttu-id="84df2-134">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="84df2-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="84df2-135">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="84df2-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="84df2-136">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="84df2-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="84df2-137">Lager</span><span class="sxs-lookup"><span data-stu-id="84df2-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="84df2-138">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="84df2-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="84df2-139">Designdetaljer: Reservasjon, sporing og handlingsmeldinger</span><span class="sxs-lookup"><span data-stu-id="84df2-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="84df2-140">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="84df2-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="84df2-141">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="84df2-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="84df2-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84df2-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
