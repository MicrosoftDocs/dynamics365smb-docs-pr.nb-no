---
title: "Definere lagerføringsenheter | Microsoft-dokumentasjon"
description: "Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3c368af3347c72f2cf355876ed5574151095f993
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="ffaef-103">Definere lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="ffaef-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="ffaef-104">Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="ffaef-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="ffaef-105">Lagerføringsenheter er et tillegg til varekort.</span><span class="sxs-lookup"><span data-stu-id="ffaef-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="ffaef-106">De erstatter dem ikke, selv om de er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="ffaef-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="ffaef-107">Med lagerføringsenheter kan du skille mellom opplysninger om en vare for en bestemt lokasjon (for eksempel et lager eller et distribusjonssenter) eller en bestemt variant (for eksempel ulike hyllenumre og ulike opplysninger om etterfylling), for den samme varen.</span><span class="sxs-lookup"><span data-stu-id="ffaef-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="ffaef-108">Slik definerer du lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="ffaef-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="ffaef-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ffaef-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ffaef-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ffaef-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="ffaef-111">Fyll ut feltene på kortet.</span><span class="sxs-lookup"><span data-stu-id="ffaef-111">Fill in the fields on the card.</span></span> <span data-ttu-id="ffaef-112">Følgende felt er obligatoriske: **Varenr.**, **Lokasjonskode** og/eller **Variantkode**.</span><span class="sxs-lookup"><span data-stu-id="ffaef-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="ffaef-113">Når du har definert den første lagerføringsenheten for en vare, blir det merket av for **Lagerføringsenhet** på **vare** kortet.</span><span class="sxs-lookup"><span data-stu-id="ffaef-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="ffaef-114">Hvis du vil opprette flere lagerføringsenheter for en vare, bruker du kjørselen **Opprett lagerføringsenhet**.</span><span class="sxs-lookup"><span data-stu-id="ffaef-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ffaef-115">Opplysningene på **lagerføringsenhetskortet** har høyere prioritet enn opplysningene på **varekortet**.</span><span class="sxs-lookup"><span data-stu-id="ffaef-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ffaef-116">Se også</span><span class="sxs-lookup"><span data-stu-id="ffaef-116">See Also</span></span>  
[<span data-ttu-id="ffaef-117">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="ffaef-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="ffaef-118">Definere lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ffaef-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="ffaef-119">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ffaef-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ffaef-120">Lager</span><span class="sxs-lookup"><span data-stu-id="ffaef-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ffaef-121">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ffaef-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ffaef-122">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ffaef-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ffaef-123">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffaef-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

