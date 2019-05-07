---
title: Definere lager| Microsoft-dokumentasjon
description: Beskriver hvordan du definerer vare- og lagerprosesser, inkludert overføringsruter og lokasjoner, for eksempel lagre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 038e3a9bfdb66a8d714f4f9452f0322623e6ddc4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "934330"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="c92eb-103">Definere lager</span><span class="sxs-lookup"><span data-stu-id="c92eb-103">Setting Up Inventory</span></span>
<span data-ttu-id="c92eb-104">Før du kan håndtere lageraktiviteter og beholdning og kostberegning, må du konfigurere regler og verdier som definerer selskapets beholdningspolicyer.</span><span class="sxs-lookup"><span data-stu-id="c92eb-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="c92eb-105">Du kan gi bedre kundeservice og optimalisere forsyningskjeden ved å organisere beholdningen på forskjellige adresser.</span><span class="sxs-lookup"><span data-stu-id="c92eb-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="c92eb-106">Deretter kan du kjøpe, lagre eller selger varer på forskjellige lokasjoner og overføre beholdning mellom dem.</span><span class="sxs-lookup"><span data-stu-id="c92eb-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="c92eb-107">Når du har definert beholdningen, kan du administrere forskjellige prosesser relatert til varetransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c92eb-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="c92eb-108">Hvis du vil ha mer informasjon, se [Håndtere lager](inventory-manage-inventory.md) og [Lagerstyring](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c92eb-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="c92eb-109">Til</span><span class="sxs-lookup"><span data-stu-id="c92eb-109">To</span></span> | <span data-ttu-id="c92eb-110">Se</span><span class="sxs-lookup"><span data-stu-id="c92eb-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="c92eb-111">Definer det generelle lageroppsettet, for eksempel nummerserier og hvordan du bruker lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="c92eb-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="c92eb-112">Definere generell informasjon om lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="c92eb-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="c92eb-113">Konfigurer en effektiv distribusjonsmodell med en kombinasjon av ulike lokasjoner og ansvarssentre tilordnet til forretningspartnere eller ansatte.</span><span class="sxs-lookup"><span data-stu-id="c92eb-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="c92eb-114">Arbeide med ansvarssentre</span><span class="sxs-lookup"><span data-stu-id="c92eb-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="c92eb-115">Organiser beholdningen på flere lokasjoner, inkludert overføringsruter.</span><span class="sxs-lookup"><span data-stu-id="c92eb-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="c92eb-116">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="c92eb-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="c92eb-117">Opprett varekort for lagervarer, ikke-lagervarer eller servicevarer som du handler med.</span><span class="sxs-lookup"><span data-stu-id="c92eb-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="c92eb-118">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="c92eb-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="c92eb-119">Lær hvordan du fyller ut feltet **Type** på varekortene i henhold til selskapsformålet.</span><span class="sxs-lookup"><span data-stu-id="c92eb-119">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="c92eb-120">Om varetyper</span><span class="sxs-lookup"><span data-stu-id="c92eb-120">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="c92eb-121">Definer flere enheter for en vare som kan brukes som alternative enheter, for eksempel for salgs-, kjøps- eller produksjonstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c92eb-121">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="c92eb-122">Definere vareenheter</span><span class="sxs-lookup"><span data-stu-id="c92eb-122">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="c92eb-123">Som et supplement til varekort kan du registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variantkode.</span><span class="sxs-lookup"><span data-stu-id="c92eb-123">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="c92eb-124">Definere lagerføringsenheter</span><span class="sxs-lookup"><span data-stu-id="c92eb-124">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="c92eb-125">Tilordne varer til kategorier, og gi dem attributter for å hjelpe deg og kunder med å finne varer.</span><span class="sxs-lookup"><span data-stu-id="c92eb-125">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="c92eb-126">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="c92eb-126">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="c92eb-127">Importer flere varebilder samtidig fra en zip-fil, der filene har fått navn i samsvar med varenumre.</span><span class="sxs-lookup"><span data-stu-id="c92eb-127">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="c92eb-128">Importere flere varebilder</span><span class="sxs-lookup"><span data-stu-id="c92eb-128">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|

## <a name="see-also"></a><span data-ttu-id="c92eb-129">Se også</span><span class="sxs-lookup"><span data-stu-id="c92eb-129">See Also</span></span>
[<span data-ttu-id="c92eb-130">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="c92eb-130">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c92eb-131">Håndtere kjøp</span><span class="sxs-lookup"><span data-stu-id="c92eb-131">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c92eb-132">[Håndtere salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="c92eb-132">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="c92eb-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c92eb-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="c92eb-134">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="c92eb-134">General Business Functionality</span></span>](ui-across-business-areas.md)
