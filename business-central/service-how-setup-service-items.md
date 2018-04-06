---
title: Oppsett av servicevarer og servicevarekomponenter | Microsoft-dokumentasjon
description: "Finn ut mer om ting du må definere før du kan bruke servicevarer, inkludert standardverdier som responstid, kontraktrabattprosent og serviceprisgruppe."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 050456758a2bf4f3489ed382103d5fed99e8fada
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="b6bc8-103">Definere servicevarer og servicevarekomponenter</span><span class="sxs-lookup"><span data-stu-id="b6bc8-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="b6bc8-104">Hvis du vil arbeide med servicevarer, må du definere følgende</span><span class="sxs-lookup"><span data-stu-id="b6bc8-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="b6bc8-105">Servicevaregrupper.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-105">Service item groups.</span></span>
* <span data-ttu-id="b6bc8-106">Valgfritt</span><span class="sxs-lookup"><span data-stu-id="b6bc8-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="b6bc8-107">Definere servicevaregrupper</span><span class="sxs-lookup"><span data-stu-id="b6bc8-107">To set up service item groups</span></span>
<span data-ttu-id="b6bc8-108">Du kan angi grupper av varer som er relaterte med hensyn til reparasjon og vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="b6bc8-109">Du kan definere standardverdier for servicevarer i en servicevaregruppe, for eksempel responstid, kontraktrabattprosent og serviceprisgruppe.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="b6bc8-110">For varer i en servicevaregruppe kan du velge om du vil at de skal registreres automatisk som servicevarer når de selges.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="b6bc8-111">Du tilordner servicevaregrupper til varer **Vare**-kortet og servicevarer på **Servicevare**-kortet.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="b6bc8-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b6bc8-113">Opprett en ny servicevaregruppe.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="b6bc8-114">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="b6bc8-115">I feltet **Standard kontraktrabatt-%** angir du den standard kontraktrabattprosenten som du vil at servicevarene i gruppen skal ha.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="b6bc8-116">I feltet **Standard serv.prisgruppekode** angir du den standard serviceprisgruppekoden som du vil at servicevarene i gruppen skal ha.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="b6bc8-117">I feltet **Standard responstid (timer)** angir du den standard responstiden i timer som du vil at servicevarene i gruppen skal ha.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="b6bc8-118">Hvis du vil registrere varene i gruppen som servicevarer når de selges, velger du feltet **Opprett servicevare**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="b6bc8-119">Slik definerer du servicevarekomponenter</span><span class="sxs-lookup"><span data-stu-id="b6bc8-119">To set up service item components</span></span>
<span data-ttu-id="b6bc8-120">En servicevare kan bestå av flere komponenter, som kan erstattes med reservedeler når varen vedlikeholdes.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="b6bc8-121">Disse komponentene defineres på siden **Oversikt over servicevarekomponenter**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="b6bc8-122">Hvis du vil definere komponenter for servicevarer som er stykklister, kan du også kopiere stykklistevarene, og deretter opprette dem som servicevarekomponenter.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="b6bc8-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicevarer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="b6bc8-124">Åpne servicevaren du vil definere komponenter for.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="b6bc8-125">Velg handlingen **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-125">Choose the **Components** action.</span></span> <span data-ttu-id="b6bc8-126">Cinduet **Oversikt over servicevarekomponenter** åpnes.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-126">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="b6bc8-127">Legg til en ny komponent.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-127">Add a new component.</span></span>  
5. <span data-ttu-id="b6bc8-128">I **Type**-feltet velger du **Servicevare** hvis selve komponenten er en registrert servicevare.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="b6bc8-129">Ellers velger du **Vare**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="b6bc8-130">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="b6bc8-130">In the **No.**</span></span> <span data-ttu-id="b6bc8-131">-feltet velger du varen eller servicevaren som er en komponent i servicevaren.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="b6bc8-132">Slik definerer du servicevarekomponenter fra stykklister</span><span class="sxs-lookup"><span data-stu-id="b6bc8-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="b6bc8-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicevarer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b6bc8-134">Åpne servicevaren du vil definere komponenter fra en stykkliste for.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="b6bc8-135">Velg handlingen **Komponenter**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-135">Choose the **Components** action.</span></span> <span data-ttu-id="b6bc8-136">Vinduet **Oversikt over servicevarekomponenter** åpnes.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-136">The **Service Item Component List** window opens.</span></span>  
4. <span data-ttu-id="b6bc8-137">Velg handlingen **Kopier fra stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="b6bc8-138">Hvis varen som servicevaren er knyttet til, er en stykkliste, opprettes komponentene for alle varene i stykklisten automatisk.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="b6bc8-139">Slik definerer du servicehyller</span><span class="sxs-lookup"><span data-stu-id="b6bc8-139">To set up a service shelf</span></span>
<span data-ttu-id="b6bc8-140">Du kan definere servicehyller som identifiserer hvor du lagrer servicevarene.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="b6bc8-141">Du tilordner servicehyller til servicevarer på sidene **Serviceordre** og **Servicevareskjema**.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="b6bc8-142">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicehyller**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-142">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="b6bc8-143">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6bc8-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6bc8-144">Se også</span><span class="sxs-lookup"><span data-stu-id="b6bc8-144">See Also</span></span>
<span data-ttu-id="b6bc8-145">[Definere koder for standardservicer](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="b6bc8-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="b6bc8-146">Definere feilsøking</span><span class="sxs-lookup"><span data-stu-id="b6bc8-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)

