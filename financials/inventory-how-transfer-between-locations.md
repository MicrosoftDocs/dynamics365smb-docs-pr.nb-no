---
title: "Overføre varer mellom lagerlokasjoner | Microsoft-dokumentasjon"
description: "Beskriver hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8ee703865f86c0edcc5bff77d8bd04cc2bd107be
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="4bc78-103">Overføre beholdning mellom lokasjoner</span><span class="sxs-lookup"><span data-stu-id="4bc78-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="4bc78-104">Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="4bc78-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="4bc78-105">Du kan også bruke varereklassifiseringskladden.</span><span class="sxs-lookup"><span data-stu-id="4bc78-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="4bc78-106">Med overføringsordrer sender du den utgående overføringen fra én lokasjon og mottar den inngående overføring på den andre lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="4bc78-107">Dette lar deg administrere de involverte lageraktivitetene og gir større visshet om at lagerantallet oppdateres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="4bc78-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="4bc78-108">Med reklassifiseringskladden fyller du ganske enkelt ut feltene **Lokasjonskode** og **Ny Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="4bc78-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="4bc78-109">Når du bokfører kladden, justeres varepostene på de aktuelle lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="4bc78-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="4bc78-110">Med denne metoden styres ikke lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4bc78-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4bc78-111">Hvis du har varer som er registrert på lager uten en lokasjonskode, for eksempel fra en tid da du bare hadde ett lager, kan du ikke overføre disse varene ved å bruke overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="4bc78-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="4bc78-112">I stedet må du bruke reklassifiseringskladden til å klassifisere varer fra en tom lokasjonskode til en faktisk lokasjonskode.</span><span class="sxs-lookup"><span data-stu-id="4bc78-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="4bc78-113">Hvis du vil ha mer informasjon, kan du se trinn 3 i delen "Slik overfører du varer med varereklassifiseringskladden".</span><span class="sxs-lookup"><span data-stu-id="4bc78-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="4bc78-114">Hvis du vil overføre varer, må lokasjoner og overføringsruter defineres.</span><span class="sxs-lookup"><span data-stu-id="4bc78-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="4bc78-115">Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="4bc78-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="4bc78-116">Slik overfører du varer med en overføringsordre</span><span class="sxs-lookup"><span data-stu-id="4bc78-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="4bc78-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Overføringsordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="4bc78-118">I vinduet **Overføringsordrer** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4bc78-118">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="4bc78-119">Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** i vinduet **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="4bc78-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.** window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="4bc78-120">Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="4bc78-121">Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å levere varene.</span><span class="sxs-lookup"><span data-stu-id="4bc78-121">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="4bc78-122">Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-122">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="4bc78-123">Varene er nå i transitt mellom de angitte lokasjonene i henhold til den angitte overføringsruten.</span><span class="sxs-lookup"><span data-stu-id="4bc78-123">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="4bc78-124">Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene.</span><span class="sxs-lookup"><span data-stu-id="4bc78-124">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="4bc78-125">Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-125">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="4bc78-126">Slik overfører du varer med varereklassifiseringskladden</span><span class="sxs-lookup"><span data-stu-id="4bc78-126">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="4bc78-127">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Vareoverføringskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4bc78-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="4bc78-128">I vinduet **Vareoverføringskladder** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4bc78-128">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4bc78-129">I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.</span><span class="sxs-lookup"><span data-stu-id="4bc78-129">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="4bc78-130">Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="4bc78-130">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="4bc78-131">I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.</span><span class="sxs-lookup"><span data-stu-id="4bc78-131">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="4bc78-132">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="4bc78-132">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bc78-133">Se også</span><span class="sxs-lookup"><span data-stu-id="4bc78-133">See Also</span></span>
[<span data-ttu-id="4bc78-134">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="4bc78-134">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4bc78-135">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="4bc78-135">Set Up Locations</span></span>](inventory-how-setup-locations.md)  

<span data-ttu-id="4bc78-136">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4bc78-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="4bc78-137">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="4bc78-137">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="4bc78-138">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="4bc78-138">General Business Functionality</span></span>](ui-across-business-areas.md)

