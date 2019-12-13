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
ms.date: 10/01/2019
ms.author: SorenGP
ms.openlocfilehash: 5554bb1576705cd1f3cbcddc7ef33da7b5db3796
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878320"
---
# <a name="set-up-locations"></a><span data-ttu-id="63621-103">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="63621-103">Set Up Locations</span></span>
<span data-ttu-id="63621-104">Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.</span><span class="sxs-lookup"><span data-stu-id="63621-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="63621-105">Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="63621-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="63621-106">Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="63621-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq]

## <a name="to-create-a-location-card"></a><span data-ttu-id="63621-107">Slik oppretter du et lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="63621-107">To create a location card</span></span>
1. <span data-ttu-id="63621-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="63621-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="63621-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="63621-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="63621-110">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="63621-110">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="63621-111">Gjenta trinn 2 og 3 for hver beholdninglokasjon.</span><span class="sxs-lookup"><span data-stu-id="63621-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="63621-112">Mange felt på lokasjonskortet refererer til håndteringen av varer i inngående og utgående lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="63621-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="63621-113">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="63621-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="63621-114">Slik oppretter du overføringsruter</span><span class="sxs-lookup"><span data-stu-id="63621-114">To create a transfer route</span></span>
1. <span data-ttu-id="63621-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overføringsruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="63621-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="63621-116">Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.</span><span class="sxs-lookup"><span data-stu-id="63621-116">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="63621-117">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="63621-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="63621-118">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="63621-118">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="63621-119">Nå kan du overføre lagervarer mellom to lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="63621-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="63621-120">Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="63621-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="63621-121">Se også</span><span class="sxs-lookup"><span data-stu-id="63621-121">See Also</span></span>
[<span data-ttu-id="63621-122">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="63621-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="63621-123">[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="63621-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="63621-124">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="63621-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="63621-125">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="63621-125">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="63621-126">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="63621-126">General Business Functionality</span></span>](ui-across-business-areas.md)
