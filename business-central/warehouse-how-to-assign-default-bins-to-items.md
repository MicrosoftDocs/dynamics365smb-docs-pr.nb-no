---
title: Tilordne standardhyller til varer | Microsoft-dokumentasjon
description: Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere. Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8c8cca84e7ace9eb25f3e1366a5beefa954edbc4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911899"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="b3e7f-104">Tilordne standardhyller til varer</span><span class="sxs-lookup"><span data-stu-id="b3e7f-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="b3e7f-105">Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="b3e7f-106">Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="b3e7f-107">Standardhyller defineres på siden **Hylleinnhold**.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="b3e7f-108">Tilordne en standardhylle til en vare</span><span class="sxs-lookup"><span data-stu-id="b3e7f-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="b3e7f-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Hylleinnholdopprett. – forslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="b3e7f-110">Fyll ut hyllekoden og opplysninger om varen for hver hylle du vil definere som standard for en vare.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="b3e7f-111">Pass på å velge **Standard**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="b3e7f-112">Velg **Opprett hylleinnhold**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="b3e7f-113">Standardhyllene tilordnes for varen.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b3e7f-114">Hvis en vare ikke er tilordnet en standardhylle når den plasseres, vil hyllen der varen plasseres, tilordnes som standardhylle.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="b3e7f-115">Slik endrer du standardhyllen for en vare</span><span class="sxs-lookup"><span data-stu-id="b3e7f-115">To change the default bin for an item</span></span>  
<span data-ttu-id="b3e7f-116">Det kan hende du må endre tilordningen av standardhylle for en vare eller tilordne en standardhylle til en ny vare.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="b3e7f-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Hylleinnhold**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b3e7f-118">I feltet **Lokasjonsfilter** velger du den riktige lokasjonskoden.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="b3e7f-119">Finn den gjeldende posten med standard hylleinnhold for varen, og fjern avmerkingen for **Standardhylle**.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="b3e7f-120">Finn hylleinnholdslinjen for hyllen som du vil bruke som ny standardhylle.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="b3e7f-121">Merk av for **Standardhylle**.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b3e7f-122">Hvis en vare ikke er tilordnet en standardhylle når den plasseres første gang, vil systemet tilordne hyllen der varen plasseres, som standardhylle.</span><span class="sxs-lookup"><span data-stu-id="b3e7f-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3e7f-123">Se også</span><span class="sxs-lookup"><span data-stu-id="b3e7f-123">See Also</span></span>  
[<span data-ttu-id="b3e7f-124">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="b3e7f-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b3e7f-125">Lager</span><span class="sxs-lookup"><span data-stu-id="b3e7f-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b3e7f-126">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b3e7f-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b3e7f-127">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b3e7f-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b3e7f-128">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="b3e7f-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b3e7f-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b3e7f-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
