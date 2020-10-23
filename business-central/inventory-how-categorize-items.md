---
title: Organisere varer i kategorier | Microsoft-dokumentasjon
description: For å gjøre det enklere å søke etter og finne varer kan du tilordne vareattributter og organisere varer i kategorier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a5698746fe52ff7ff6ca38e1207f09ded0742c96
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914109"
---
# <a name="categorize-items"></a><span data-ttu-id="70d11-103">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="70d11-103">Categorize Items</span></span>

<span data-ttu-id="70d11-104">For å holde oversikt over varene og hjelpe deg med å sortere og søke etter varer, er det nyttig å kunne organisere dem i varekategorier.</span><span class="sxs-lookup"><span data-stu-id="70d11-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="70d11-105">Hvis du vil søke etter varer etter egenskaper, kan du tilordne vareattributter til varer og også varekategorier.</span><span class="sxs-lookup"><span data-stu-id="70d11-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="70d11-106">Hvis du vil ha mer informasjon, kan du se [Arbeide med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="70d11-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="70d11-107">Slik oppretter du en varekategori:</span><span class="sxs-lookup"><span data-stu-id="70d11-107">To create an item category</span></span>
1. <span data-ttu-id="70d11-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekategorier**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="70d11-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="70d11-109">På siden **Varekategorier** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70d11-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="70d11-110">Fyll ut følgende felt på hurtigfanen **Generelt** på siden **Varekategorikort** etter behov.</span><span class="sxs-lookup"><span data-stu-id="70d11-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="70d11-111">I **Attributter**-hurtigfanen angir du hvilke som helst vareattributter for varekategorien.</span><span class="sxs-lookup"><span data-stu-id="70d11-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="70d11-112">Hvis du vil ha mer informasjon, kan du se [Slik tilordner du vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="70d11-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="70d11-113">Hvis varekategorien har en overordnet varekategori, som angitt av feltet **Overordnet kategori**, blir vareattributter som er tilordnet til denne overordnede varekategorien, forhåndsutfylt i hurtigfanen **Attributter**.</span><span class="sxs-lookup"><span data-stu-id="70d11-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="70d11-114">Vareattributter du tilordner til en varekategori, brukes automatisk på varen som varekategorien er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="70d11-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="70d11-115">Hvis du ombestemmer deg om en varekategori, kan du slette den.</span><span class="sxs-lookup"><span data-stu-id="70d11-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="70d11-116">Hvis den imidlertid allerede er tilordnet til en vare, må du fjerne denne tilordningen før du kan slette varekategorien.</span><span class="sxs-lookup"><span data-stu-id="70d11-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="70d11-117">Slik tilordner du en varekategori til en vare:</span><span class="sxs-lookup"><span data-stu-id="70d11-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="70d11-118">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="70d11-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="70d11-119">Åpne kortet for varen som du vil tilordne til en varekategori.</span><span class="sxs-lookup"><span data-stu-id="70d11-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="70d11-120">Velg oppslagsknappen i feltet **Varekategorikode** og velg en eksisterende varekategori.</span><span class="sxs-lookup"><span data-stu-id="70d11-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="70d11-121">Du kan også velge **Ny**-handlingen for å opprette en ny varekategori først, som forklart under [Slik oppretter du en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="70d11-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="70d11-122">Kategorier, attributter og varianter</span><span class="sxs-lookup"><span data-stu-id="70d11-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="70d11-123">Se også</span><span class="sxs-lookup"><span data-stu-id="70d11-123">See Also</span></span>

[<span data-ttu-id="70d11-124">Arbeide med vareattributter</span><span class="sxs-lookup"><span data-stu-id="70d11-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="70d11-125">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="70d11-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="70d11-126">Lager</span><span class="sxs-lookup"><span data-stu-id="70d11-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="70d11-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70d11-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
