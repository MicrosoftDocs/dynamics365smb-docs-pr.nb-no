---
title: Definere lagerføringsenheter | Microsoft-dokumentasjon
description: Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4f5a1933e803322367b241e772d796f1365f9d11
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915463"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="4073a-103">Definere lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="4073a-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="4073a-104">Du kan bruke lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="4073a-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="4073a-105">Lagerføringsenheter er et tillegg til varekort.</span><span class="sxs-lookup"><span data-stu-id="4073a-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="4073a-106">De erstatter dem ikke, selv om de er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="4073a-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="4073a-107">Med lagerføringsenheter kan du skille mellom opplysninger om en vare for en bestemt lokasjon (for eksempel et lager eller et distribusjonssenter) eller en bestemt variant (for eksempel ulike hyllenumre og ulike opplysninger om etterfylling), for den samme varen.</span><span class="sxs-lookup"><span data-stu-id="4073a-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="4073a-108">Slik definerer du lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="4073a-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="4073a-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4073a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4073a-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4073a-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="4073a-111">Fyll ut feltene på kortet.</span><span class="sxs-lookup"><span data-stu-id="4073a-111">Fill in the fields on the card.</span></span> <span data-ttu-id="4073a-112">Følgende felt er obligatoriske: **Varenr.**, **Lokasjonskode** og/eller **Variantkode**.</span><span class="sxs-lookup"><span data-stu-id="4073a-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="4073a-113">Når du har definert den første lagerføringsenheten for en vare, blir det merket av for **Lagerføringsenhet** på **vare** kortet.</span><span class="sxs-lookup"><span data-stu-id="4073a-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="4073a-114">Hvis du vil opprette flere lagerføringsenheter for en vare, bruker du kjørselen **Opprett lagerføringsenhet**.</span><span class="sxs-lookup"><span data-stu-id="4073a-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="4073a-115">Opplysningene på **lagerføringsenhetskortet** har høyere prioritet enn opplysningene på **varekortet**.</span><span class="sxs-lookup"><span data-stu-id="4073a-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="4073a-116">Hvis LFE angis via produksjon, brukes ikke **Kostpris (standard)**-feltet når faktisk kost for den produserte varen faktureres og justeres.</span><span class="sxs-lookup"><span data-stu-id="4073a-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="4073a-117">I stedet brukes **Kostpris (standard)**-feltet på det underliggende varekortet, og eventuelle avvik beregnes mot kostandelene for denne varen.</span><span class="sxs-lookup"><span data-stu-id="4073a-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="4073a-118">Siden produksjonsstykklister og ruting ikke kan tilordnes til LFEer, er heller ikke opprulling av enhetskost og den relaterte beregningen av kostandeler tilgjengelig på LFEer.</span><span class="sxs-lookup"><span data-stu-id="4073a-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="4073a-119">Hvis du vil ha mer informasjon, kan du se [Om beregning av standardkost](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="4073a-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="4073a-120">Se også</span><span class="sxs-lookup"><span data-stu-id="4073a-120">See Also</span></span>  
[<span data-ttu-id="4073a-121">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="4073a-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="4073a-122">Definere lagerstyring</span><span class="sxs-lookup"><span data-stu-id="4073a-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="4073a-123">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="4073a-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="4073a-124">Lager</span><span class="sxs-lookup"><span data-stu-id="4073a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="4073a-125">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="4073a-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="4073a-126">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="4073a-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="4073a-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4073a-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
