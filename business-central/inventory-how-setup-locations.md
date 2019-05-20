---
title: Definere et lokasjonskort og definere overføringsruter | Microsoft-dokumentasjon
description: Du oppretter et lokasjonskort for hvert sted der du oppbevarer lagervarer, for eksempel et lager eller distribusjonssenter, og definerer ruter for å overføre varer mellom lokasjoner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: d94f1bb2fe45263f013119954622b995e902b30f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244285"
---
# <a name="set-up-locations"></a><span data-ttu-id="54d2a-103">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="54d2a-103">Set Up Locations</span></span>
<span data-ttu-id="54d2a-104">Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.</span><span class="sxs-lookup"><span data-stu-id="54d2a-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="54d2a-105">Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="54d2a-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="54d2a-106">Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="54d2a-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="54d2a-107">Slik oppretter du et lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="54d2a-107">To create a location card</span></span>
1. <span data-ttu-id="54d2a-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="54d2a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="54d2a-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54d2a-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="54d2a-110">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="54d2a-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="54d2a-111">Gjenta trinn 2 og 3 for hver beholdninglokasjon.</span><span class="sxs-lookup"><span data-stu-id="54d2a-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="54d2a-112">Mange felt på lokasjonskortet refererer til håndteringen av varer i inngående og utgående lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="54d2a-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="54d2a-113">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="54d2a-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="54d2a-114">Slik oppretter du overføringsruter</span><span class="sxs-lookup"><span data-stu-id="54d2a-114">To create a transfer route</span></span>
1. <span data-ttu-id="54d2a-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overføringsruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="54d2a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="54d2a-116">Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.</span><span class="sxs-lookup"><span data-stu-id="54d2a-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="54d2a-117">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54d2a-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="54d2a-118">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="54d2a-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="54d2a-119">Nå kan du overføre lagervarer mellom to lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="54d2a-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="54d2a-120">Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="54d2a-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="54d2a-121">Se også</span><span class="sxs-lookup"><span data-stu-id="54d2a-121">See Also</span></span>
[<span data-ttu-id="54d2a-122">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="54d2a-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="54d2a-123">[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="54d2a-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="54d2a-124">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54d2a-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="54d2a-125">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="54d2a-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="54d2a-126">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="54d2a-126">General Business Functionality</span></span>](ui-across-business-areas.md)
