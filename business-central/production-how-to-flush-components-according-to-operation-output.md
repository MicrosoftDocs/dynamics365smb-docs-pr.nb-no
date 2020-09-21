---
title: Lagertrekke komponenter i henhold til operasjonsavgang | Microsoft-dokumentasjon
description: For varer som er definert med trekkmetoden Bakover, er standard virkemåte å beregne og bokføre komponentforbruk når du endrer statusen for en frigitt produksjonsordre til **Ferdig**. Hvis du vil ha mer informasjon, kan du se Trekkmetode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d895ede7ec603b1f4892b1aacb2683f6ace11233
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779765"
---
# <a name="flush-components-according-to-operation-output"></a><span data-ttu-id="bf595-104">Lagertrekke komponenter i henhold til operasjonsavgang</span><span class="sxs-lookup"><span data-stu-id="bf595-104">Flush Components According to Operation Output</span></span>
<span data-ttu-id="bf595-105">For varer som er definert med trekkmetoden Bakover, er standard virkemåte å beregne og bokføre komponentforbruk når du endrer statusen for en frigitt produksjonsordre til **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="bf595-105">For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**.</span></span>  

<span data-ttu-id="bf595-106">Hvis du også definerer rutekoblingskoder, skjer beregning og bokføring når hver operasjon er fullført, og antallet som faktisk ble forbrukt i operasjonen, bokføres.</span><span class="sxs-lookup"><span data-stu-id="bf595-106">If you also define routing link codes, then calculation and posting occurs when each operation is finished, and the quantity that was actually consumed in the operation is posted.</span></span> <span data-ttu-id="bf595-107">Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="bf595-107">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

<span data-ttu-id="bf595-108">Hvis en produksjonsordre om å produsere 800 meter for eksempel krever 8 kg av en komponent, bokføres 2 kg automatisk som forbruk når du bokfører 200 meter som avgang.</span><span class="sxs-lookup"><span data-stu-id="bf595-108">For example, if a production order to produce 800 meters requires 8 kg of a component, then when you post 200 meters as output, 2 kg are automatically posted as consumption.</span></span>  

<span data-ttu-id="bf595-109">Denne funksjonaliteten er nyttig av følgende årsaker:</span><span class="sxs-lookup"><span data-stu-id="bf595-109">This functionality is useful for the following reasons:</span></span>  

-   <span data-ttu-id="bf595-110">**Lagerverdisetting** -Verdipostene for avgang og forbruk opprettes parallelt ettersom produksjonsordren går fremover.</span><span class="sxs-lookup"><span data-stu-id="bf595-110">**Inventory Valuation** - Value entries for output and consumption are created in parallel as the production order progresses.</span></span> <span data-ttu-id="bf595-111">Uten rutekoblingskoder vil lagerverdien øke etter hvert som avgangen bokføres og deretter reduseres på et senere tidspunkt når verdien for komponentforbruk bokføres sammen med den ferdige produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="bf595-111">Without routing link codes, the inventory value will increase as output is posted and then decrease at a later point in time when the value of component consumption is posted together with the finished production order.</span></span>  
-   <span data-ttu-id="bf595-112">**Lagertilgjengelighet** - Med gradvis forbruksbokføring er komponentvarenes tilgjengelighet mer oppdatert, noe som er viktig for å opprettholde den interne balansen mellom behov og forsyning.</span><span class="sxs-lookup"><span data-stu-id="bf595-112">**Inventory Availability** - With gradual consumption posting, the availability of component items is more up-to-date, which is important to maintain the internal balance between demand and supply.</span></span> <span data-ttu-id="bf595-113">Uten rutekoblingskoder kan andre behov for komponenten tro at den er tilgjengelig så lenge den venter på en forsinket forbruksbokføring.</span><span class="sxs-lookup"><span data-stu-id="bf595-113">Without routing link codes, other demands for the component may believe that it is available as long as it is pending a delayed consumption posting.</span></span>  
-   <span data-ttu-id="bf595-114">**Til rett tid** – Med evnen til å tilpasse produktene til kundens ønsker kan du minimere svinn ved å kontrollere at arbeids- og systemendringer bare forekommer når det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="bf595-114">**Just-in-Time** – With the ability to customize products to customer requests, you can minimize waste by making sure that work and system changes only occur when it is necessary.</span></span>  

<span data-ttu-id="bf595-115">Følgende fremgangsmåte viser hvordan du kombinerer lagertrekk bakover og rutekoblingskoder slik at lagertrekksantallet for hver operasjon er proporsjonalt med den faktiske avgangen for den fullførte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="bf595-115">The following procedure shows how to combine backward flushing and routing link codes so that the quantity that is flushed for each operation is proportional to the actual output of the finished operation.</span></span>  

## <a name="to-flush-components-according-to-operation-output"></a><span data-ttu-id="bf595-116">Slik utfører du lagertrekk i henhold til operasjonsavgang:</span><span class="sxs-lookup"><span data-stu-id="bf595-116">To flush components according to operation output</span></span>  
1.  <span data-ttu-id="bf595-117">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf595-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bf595-118">Velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="bf595-118">Choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="bf595-119">På hurtigfanen **Etterfylling**, i **Trekkmetode**- feltet, velger du **Fremover**.</span><span class="sxs-lookup"><span data-stu-id="bf595-119">On the **Replenishment** FastTab, in the **Flushing Method** field, select **Forward**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="bf595-120">Velg **Plukk + Fremover** hvis komponenten er brukt på en lokasjon som er konfigurert for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="bf595-120">Select **Pick+ Forward** if the component is used in a location that is set up for directed put-away and pick.</span></span>  

4.  <span data-ttu-id="bf595-121">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf595-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
5.  <span data-ttu-id="bf595-122">Definer rutekoblingskoder for hver operasjon som forbruker komponenten.</span><span class="sxs-lookup"><span data-stu-id="bf595-122">Define routing link codes for every operation that consumes the component.</span></span> <span data-ttu-id="bf595-123">Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="bf595-123">For more information, see [Create Routings ](production-how-to-create-routings.md).</span></span>  
6.  <span data-ttu-id="bf595-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="bf595-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production BOM**, and then choose the related link.</span></span>  
7.  <span data-ttu-id="bf595-125">Definer rutekoblingskoder fra hver forekomst av komponenten til operasjonen der den er brukt.</span><span class="sxs-lookup"><span data-stu-id="bf595-125">Define routing link codes from each instance of the component to the operation where it is consumed.</span></span>

    > [!IMPORTANT]  
    >  <span data-ttu-id="bf595-126">Komponenten må ha en rutekobling til den siste operasjonen i ruten.</span><span class="sxs-lookup"><span data-stu-id="bf595-126">The component must have a routing link to the last operation in the routing.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bf595-127">Se også</span><span class="sxs-lookup"><span data-stu-id="bf595-127">See Also</span></span>  
[<span data-ttu-id="bf595-128">Opprette produksjonsstykklister</span><span class="sxs-lookup"><span data-stu-id="bf595-128">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="bf595-129">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="bf595-129">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="bf595-130">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="bf595-130">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="bf595-131">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="bf595-131">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="bf595-132">Lager</span><span class="sxs-lookup"><span data-stu-id="bf595-132">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="bf595-133">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="bf595-133">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="bf595-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf595-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
