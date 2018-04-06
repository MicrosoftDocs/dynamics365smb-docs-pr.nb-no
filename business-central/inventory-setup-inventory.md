---
title: Definere lager| Microsoft-dokumentasjon
description: "Beskriver hvordan du definerer vare- og lagerprosesser, inkludert overføringsruter og lokasjoner, for eksempel lagre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 62eee7532e457721430cb31519b5acb23e95bfcb
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="388b4-103">Definere lager</span><span class="sxs-lookup"><span data-stu-id="388b4-103">Setting Up Inventory</span></span>
<span data-ttu-id="388b4-104">Før du kan håndtere lageraktiviteter og beholdning og kostberegning, må du konfigurere regler og verdier som definerer selskapets beholdningspolicyer.</span><span class="sxs-lookup"><span data-stu-id="388b4-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="388b4-105">Du kan gi bedre kundeservice og optimalisere forsyningskjeden ved å organisere beholdningen på forskjellige adresser.</span><span class="sxs-lookup"><span data-stu-id="388b4-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="388b4-106">Deretter kan du kjøpe, lagre eller selger varer på forskjellige lokasjoner og overføre beholdning mellom dem.</span><span class="sxs-lookup"><span data-stu-id="388b4-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="388b4-107">Når du har definert beholdningen, kan du administrere forskjellige prosesser relatert til varetransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="388b4-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="388b4-108">Hvis du vil ha mer informasjon, se [Håndtere lager](inventory-manage-inventory.md) og [Lagerstyring](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="388b4-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="388b4-109">Til</span><span class="sxs-lookup"><span data-stu-id="388b4-109">To</span></span> | <span data-ttu-id="388b4-110">Se</span><span class="sxs-lookup"><span data-stu-id="388b4-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="388b4-111">Definer det generelle lageroppsettet, for eksempel nummerserier og hvordan du bruker lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="388b4-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="388b4-112">Definere generell informasjon om lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="388b4-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="388b4-113">Konfigurer en effektiv distribusjonsmodell med en kombinasjon av ulike lokasjoner og ansvarssentre tilordnet til forretningspartnere eller ansatte.</span><span class="sxs-lookup"><span data-stu-id="388b4-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="388b4-114">Arbeide med ansvarssentre</span><span class="sxs-lookup"><span data-stu-id="388b4-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="388b4-115">Organiser beholdningen på flere lokasjoner, inkludert overføringsruter.</span><span class="sxs-lookup"><span data-stu-id="388b4-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="388b4-116">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="388b4-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="388b4-117">Opprett varekort for lagervarer som du handler med.</span><span class="sxs-lookup"><span data-stu-id="388b4-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="388b4-118">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="388b4-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="388b4-119">Definer flere enheter for en vare som kan brukes som alternative enheter, for eksempel for salgs-, kjøps- eller produksjonstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="388b4-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="388b4-120">Definere vareenheter</span><span class="sxs-lookup"><span data-stu-id="388b4-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="388b4-121">Som et supplement til varekort kan du registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="388b4-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="388b4-122">Definere lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="388b4-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="388b4-123">Tilordne varer til kategorier, og gi dem attributter for å hjelpe deg og kunder med å finne varer.</span><span class="sxs-lookup"><span data-stu-id="388b4-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="388b4-124">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="388b4-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="388b4-125">Se også</span><span class="sxs-lookup"><span data-stu-id="388b4-125">See Also</span></span>
[<span data-ttu-id="388b4-126">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="388b4-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="388b4-127">Håndtere kjøp</span><span class="sxs-lookup"><span data-stu-id="388b4-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="388b4-128">[Håndtere salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="388b4-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="388b4-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="388b4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="388b4-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="388b4-130">General Business Functionality</span></span>](ui-across-business-areas.md)

