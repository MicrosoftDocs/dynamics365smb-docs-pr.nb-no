---
title: Organisere varer i kategorier | Microsoft-dokumentasjon
description: "For å gjøre det enklere å søke etter og finne varer kan du tilordne vareattributter og organisere varer i kategorier."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: da87c427033d58d92a6a5222bc323c68c4bc3f4e
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-categorize-items"></a><span data-ttu-id="20291-103">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="20291-103">How to: Categorize Items</span></span>
<span data-ttu-id="20291-104">For å holde oversikt over varene og hjelpe deg med å sortere og søke etter varer, er det nyttig å kunne organisere dem i varekategorier.</span><span class="sxs-lookup"><span data-stu-id="20291-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="20291-105">Hvis du vil søke etter varer etter egenskaper, kan du tilordne vareattributter til varer og også varekategorier.</span><span class="sxs-lookup"><span data-stu-id="20291-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="20291-106">Hvis du vil ha mer informasjon, kan du se [Arbeide med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="20291-106">For more information, see [How to: Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

## <a name="to-create-an-item-category"></a><span data-ttu-id="20291-107">Slik oppretter du en varekategori:</span><span class="sxs-lookup"><span data-stu-id="20291-107">To create an item category</span></span>
1. <span data-ttu-id="20291-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varekategorier**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="20291-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Categories**, and then choose the related link.</span></span>
2. <span data-ttu-id="20291-109">I vinduet **Varekategorier** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="20291-109">In the **Item Categories** window, choose the **New** action.</span></span>
3. <span data-ttu-id="20291-110">Fyll ut følgende felt på hurtigfanen **Generelt** i vinduet **Varekategorikort** etter behov.</span><span class="sxs-lookup"><span data-stu-id="20291-110">In the **Item Category Card** window, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="20291-111">I **Attributter**-hurtigfanen angir du hvilke som helst vareattributter for varekategorien.</span><span class="sxs-lookup"><span data-stu-id="20291-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="20291-112">Hvis du vil ha mer informasjon, kan du se "Slik tilordner du vareattributter til en varekategori" i [Arbeide med vareattributter](inventory-how-work-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="20291-112">For more information, see the "To assign item attributes to an item category" section in [How to: Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="20291-113">Hvis varekategorien har en overordnet varekategori, som angitt av feltet **Overordnet kategori**, blir vareattributter som er tilordnet til denne overordnede varekategorien, forhåndsutfylt i hurtigfanen **Attributter**.</span><span class="sxs-lookup"><span data-stu-id="20291-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
>   <span data-ttu-id="20291-114">Vareattributter du tilordner til en varekategori, brukes automatisk på varen som varekategorien er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="20291-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="20291-115">Slik tilordner du en varekategori til en vare:</span><span class="sxs-lookup"><span data-stu-id="20291-115">To assign an item category to an item</span></span>
1. <span data-ttu-id="20291-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="20291-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="20291-117">Åpne kortet for varen som du vil tilordne til en varekategori.</span><span class="sxs-lookup"><span data-stu-id="20291-117">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="20291-118">Velg oppslagsknappen i feltet **Varekategorikode** og velg en eksisterende varekategori.</span><span class="sxs-lookup"><span data-stu-id="20291-118">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="20291-119">Du kan også velge **Ny**-handlingen for å opprette en ny varekategori først, som forklart under "Slik oppretter du en varekategori".</span><span class="sxs-lookup"><span data-stu-id="20291-119">Alternatively, choose the **New** action to first create a new item category as explained in the "To create an item category" section.</span></span>

## <a name="see-also"></a><span data-ttu-id="20291-120">Se også</span><span class="sxs-lookup"><span data-stu-id="20291-120">See Also</span></span>
[<span data-ttu-id="20291-121">Arbeide med vareattributter</span><span class="sxs-lookup"><span data-stu-id="20291-121">How to: Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="20291-122">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="20291-122">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="20291-123">Lager</span><span class="sxs-lookup"><span data-stu-id="20291-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="20291-124">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20291-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

