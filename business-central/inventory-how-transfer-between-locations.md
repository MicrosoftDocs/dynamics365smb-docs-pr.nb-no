---
title: Overføre varer mellom lagerlokasjoner | Microsoft-dokumentasjon
description: Beskriver hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 26ce0f4661a44c1f478b38a2709015ea6ff1f602
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309703"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="22f15-103">Overføre beholdning mellom lokasjoner</span><span class="sxs-lookup"><span data-stu-id="22f15-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="22f15-104">Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="22f15-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="22f15-105">Du kan også bruke varereklassifiseringskladden.</span><span class="sxs-lookup"><span data-stu-id="22f15-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="22f15-106">Med overføringsordrer sender du den utgående overføringen fra én lokasjon og mottar den inngående overføring på den andre lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="22f15-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="22f15-107">Dette lar deg administrere de involverte lageraktivitetene og gir større visshet om at lagerantallet oppdateres på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="22f15-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="22f15-108">Med reklassifiseringskladden fyller du ganske enkelt ut feltene **Lokasjonskode** og **Ny Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="22f15-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="22f15-109">Når du bokfører kladden, justeres varepostene på de aktuelle lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="22f15-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="22f15-110">Med denne metoden styres ikke lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="22f15-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="22f15-111">Hvis du har varer som er registrert på lager uten en lokasjonskode, for eksempel fra en tid da du bare hadde ett lager, kan du ikke overføre disse varene ved å bruke overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="22f15-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="22f15-112">I stedet må du bruke reklassifiseringskladden til å klassifisere varer fra en tom lokasjonskode til en faktisk lokasjonskode.</span><span class="sxs-lookup"><span data-stu-id="22f15-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="22f15-113">Hvis du vil ha mer informasjon, kan du se trinn 3 i [Slik overfører du varer med varereklassifiseringskladden](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span><span class="sxs-lookup"><span data-stu-id="22f15-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="22f15-114">Hvis du vil overføre varer, må lokasjoner og overføringsruter defineres.</span><span class="sxs-lookup"><span data-stu-id="22f15-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="22f15-115">Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="22f15-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="22f15-116">Slik overfører du varer med en overføringsordre</span><span class="sxs-lookup"><span data-stu-id="22f15-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="22f15-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overføringsordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="22f15-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="22f15-118">I hodet på siden **Overføringsordre** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="22f15-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="22f15-119">Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** på siden **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="22f15-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="22f15-120">Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="22f15-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="22f15-121">Når du skal fylle ut linjene, kan du angi dem manuelt eller velge ett av følgende alternativer under **Funksjoner**-handlingen:</span><span class="sxs-lookup"><span data-stu-id="22f15-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="22f15-122">Velg handlingen **Hent hylleinnhold** for å velge eksisterende varer fra en bestemt hylle på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="22f15-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="22f15-123">Velg **Hent mottakslinjer** for å velge varer som du nettopp har mottatt på overfør fra-lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="22f15-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="22f15-124">Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å levere varene.</span><span class="sxs-lookup"><span data-stu-id="22f15-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="22f15-125">Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="22f15-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="22f15-126">Varene er nå i transitt mellom de angitte lokasjonene i henhold til den angitte overføringsruten.</span><span class="sxs-lookup"><span data-stu-id="22f15-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="22f15-127">Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene.</span><span class="sxs-lookup"><span data-stu-id="22f15-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="22f15-128">Overføringsordrelinjene er de samme som når de sendes, og kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="22f15-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="22f15-129">Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="22f15-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="22f15-130">Slik overfører du varer med varereklassifiseringskladden</span><span class="sxs-lookup"><span data-stu-id="22f15-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="22f15-131">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareoverføringskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="22f15-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="22f15-132">På siden **Vareoverføringskladder** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="22f15-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="22f15-133">I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.</span><span class="sxs-lookup"><span data-stu-id="22f15-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="22f15-134">Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="22f15-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="22f15-135">I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.</span><span class="sxs-lookup"><span data-stu-id="22f15-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="22f15-136">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="22f15-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="22f15-137">Se også</span><span class="sxs-lookup"><span data-stu-id="22f15-137">See Also</span></span>
[<span data-ttu-id="22f15-138">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="22f15-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="22f15-139">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="22f15-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="22f15-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="22f15-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="22f15-141">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="22f15-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="22f15-142">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="22f15-142">General Business Functionality</span></span>](ui-across-business-areas.md)
