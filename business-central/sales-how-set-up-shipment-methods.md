---
title: Sette opp leveringsmåter | Microsoft Docs
description: Du kan sette opp en kode for hver av leveringsmåtene du tilbyr, og angi informasjon om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: dc4864f27490a9cef7d3401f67c8ef177a5c7ef3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193889"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="11426-103">Sette opp leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="11426-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="11426-104">Leveringsmåter, også kalt "incoterms", avhenger ofte av varene, kundene og leverandørene.</span><span class="sxs-lookup"><span data-stu-id="11426-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="11426-105">Hvis kunden for eksempel bor på en øy, kan han/hun velge om varene skal sendes med fly eller båt.</span><span class="sxs-lookup"><span data-stu-id="11426-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="11426-106">Noen kunder kan be om levering neste dag.</span><span class="sxs-lookup"><span data-stu-id="11426-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="11426-107">Noen ønsker kanskje å hente ordren.</span><span class="sxs-lookup"><span data-stu-id="11426-107">Some may want to pick up the order.</span></span> <span data-ttu-id="11426-108">På kunde- og leverandørkortene kan du angi hvilken leveringsmåte du ønsker.</span><span class="sxs-lookup"><span data-stu-id="11426-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="11426-109">Du definerer beskrivelsen og koden for hver leveringsmåte på siden **Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="11426-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="11426-110">Du kan for eksempel sette opp koden FOB og skrive inn Fritt om bord i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="11426-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="11426-111">Deretter kan du angi koden i **Leveringsmåtekode**-feltet andre steder i systemet, for eksempel på et kundekort.</span><span class="sxs-lookup"><span data-stu-id="11426-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="11426-112">Når dette er gjort og du oppretter nye ordrer, fakturaer, kredittnotaer og så videre, angir systemet beskrivelsen representert av koden.</span><span class="sxs-lookup"><span data-stu-id="11426-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="11426-113">Du kan endre den i dokumentet etter behov.</span><span class="sxs-lookup"><span data-stu-id="11426-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="11426-114">Slik setter du opp en leveringskode</span><span class="sxs-lookup"><span data-stu-id="11426-114">To set up a shipment code</span></span>
1. <span data-ttu-id="11426-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leveringsmåter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="11426-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="11426-116">På siden **Leveringsmåter** velger du **Ny**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="11426-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="11426-117">Angi en kode og en beskrivelse for leveringsmåten på den nye linjen.</span><span class="sxs-lookup"><span data-stu-id="11426-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="11426-118">Se også</span><span class="sxs-lookup"><span data-stu-id="11426-118">See Also</span></span>
[<span data-ttu-id="11426-119">Incoterms</span><span class="sxs-lookup"><span data-stu-id="11426-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="11426-120">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="11426-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="11426-121">[Spore pakker](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="11426-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="11426-122">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="11426-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="11426-123">Lager</span><span class="sxs-lookup"><span data-stu-id="11426-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="11426-124">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="11426-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="11426-125">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="11426-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="11426-126">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="11426-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="11426-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="11426-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
