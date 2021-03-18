---
title: Sette opp leveringsmåter
description: Du kan sette opp en kode for hver av leveringsmåtene du tilbyr, og angi informasjon om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: 096b609d26ad24785f90634d725d751ac57b346e
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573304"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="5a147-103">Sette opp leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="5a147-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="5a147-104">Leveringsmåter avhenger ofte av varene, kundene og leverandørene.</span><span class="sxs-lookup"><span data-stu-id="5a147-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="5a147-105">Hvis kunden for eksempel bor på en øy, kan han/hun velge om varene skal sendes med fly eller båt.</span><span class="sxs-lookup"><span data-stu-id="5a147-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="5a147-106">Noen kunder kan be om levering neste dag.</span><span class="sxs-lookup"><span data-stu-id="5a147-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="5a147-107">Noen ønsker kanskje å hente ordren.</span><span class="sxs-lookup"><span data-stu-id="5a147-107">Some may want to pick up the order.</span></span> <span data-ttu-id="5a147-108">På kunde- og leverandørkortene kan du angi hvilken leveringsmåte du ønsker.</span><span class="sxs-lookup"><span data-stu-id="5a147-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="5a147-109">Du definerer beskrivelsen og koden for hver leveringsmåte på siden **Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="5a147-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="5a147-110">Du kan for eksempel sette opp koden FOB og skrive inn Fritt om bord i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="5a147-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="5a147-111">Deretter kan du angi koden i **Leveringsmåtekode**-feltet andre steder i systemet, for eksempel på et kundekort.</span><span class="sxs-lookup"><span data-stu-id="5a147-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="5a147-112">Når dette er gjort og du oppretter nye ordrer, fakturaer, kredittnotaer og så videre, angir systemet beskrivelsen representert av koden.</span><span class="sxs-lookup"><span data-stu-id="5a147-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="5a147-113">Du kan endre den i dokumentet etter behov.</span><span class="sxs-lookup"><span data-stu-id="5a147-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="5a147-114">Slik definerer du leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="5a147-114">To set up a shipment method</span></span>

1. <span data-ttu-id="5a147-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leveringsmåter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5a147-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="5a147-116">På siden **Leveringsmåter** velger du **Ny**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="5a147-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="5a147-117">Angi en kode og en beskrivelse for leveringsmåten på den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="5a147-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="5a147-118">Hvis du bruker Incoterms, må du definere leveringsmåter for å representere de aktuelle Incoterms-reglene.</span><span class="sxs-lookup"><span data-stu-id="5a147-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a147-119">Se også</span><span class="sxs-lookup"><span data-stu-id="5a147-119">See Also</span></span>

[<span data-ttu-id="5a147-120">Sett opp transportører</span><span class="sxs-lookup"><span data-stu-id="5a147-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="5a147-121">Spore pakker</span><span class="sxs-lookup"><span data-stu-id="5a147-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="5a147-122">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="5a147-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5a147-123">Lager</span><span class="sxs-lookup"><span data-stu-id="5a147-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5a147-124">Definere lagerstyring</span><span class="sxs-lookup"><span data-stu-id="5a147-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="5a147-125">Monteringsstyring</span><span class="sxs-lookup"><span data-stu-id="5a147-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="5a147-126">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="5a147-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5a147-127">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a147-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5a147-128">Incoterms på iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="5a147-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]