---
title: Lageraktiviteter | Microsoft-dokumentasjon
description: "Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret, og organisere og vedlikeholde selskapet lagre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a><span data-ttu-id="ec4f8-103">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ec4f8-103">Warehouse Management</span></span>
<span data-ttu-id="ec4f8-104">Etter mottak av varer og før varene sendes, utføres det en rekke interne lageraktiviteter for å sørge for en effektiv strøm av varer gjennom lageret, og organisere og vedlikeholde selskapet lagre.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="ec4f8-105">Vanlige lageraktiviteter omfatter å plassere varer, flytte varer på lageret eller mellom ulike lager, og plukke varer til montering, produksjon eller for levering.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="ec4f8-106">Montering av varer for salg eller lager kan også regnes som lageraktiviteter, men disse dekkes andre steder.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="ec4f8-107">Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="ec4f8-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="ec4f8-108">På store lager kan de ulike håndteringsoppgavene legges til ulike avdelinger, mens integreringen administreres av en styrt arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="ec4f8-109">I enklere installasjoner er flyten mindre formalisert, og lageraktivitetene utføres med såkalte lagerplasseringer og lagerplukk.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="ec4f8-110">Hvis du vil ha mer informasjon om enkle kontra avanserte lageroppsett, kan du se [Designdetaljer: Lageroversikt](design-details-warehouse-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec4f8-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="ec4f8-111">Før du kan utføre lageraktiviteter, må du definere systemet for den aktuelle kompleksiteten for lagerbehandlingen.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="ec4f8-112">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ec4f8-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="ec4f8-113">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ec4f8-114">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="ec4f8-114">**To**</span></span>|<span data-ttu-id="ec4f8-115">**Se**</span><span class="sxs-lookup"><span data-stu-id="ec4f8-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ec4f8-116">Registrer mottaket av varer på lagerlokasjoner, enten bare med en bestilling, i enkle lokasjonsoppsett eller med et lagermottak i tilfelle halvautomatisert eller fullstendig automatisert lagerbehandling på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="ec4f8-117">Motta varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-117">How to: Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="ec4f8-118">Omgå plasseringen, og velg prosesser for å påskynde en vare rett fra mottak eller produksjon til levering.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="ec4f8-119">Kryssoverføre varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-119">How to: Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="ec4f8-120">Plassere varer som mottas etter kjøp, salgsreturer, overføringer eller produksjonsavgang i henhold til den konfigurerte lagerprosessen.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="ec4f8-121">Plassere varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="ec4f8-122">Flytte varer mellom hyller på lageret.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="ec4f8-123">Flytte varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="ec4f8-124">Plukke varer som skal leveres, overføres eller anvendes i monteringen eller produksjonen, i henhold til den konfigurerte lagerprosessen.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="ec4f8-125">Plukke varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="ec4f8-126">Registrer leveringen av varer fra lagerlokasjoner, enten bare med en ordre, i enkle lokasjonsoppsett eller med en lagerlevering i tilfelle halvautomatiserte eller fullstendig automatiserte lagerprosesser på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec4f8-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="ec4f8-127">Levere varer</span><span class="sxs-lookup"><span data-stu-id="ec4f8-127">How to: Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="ec4f8-128">Se også</span><span class="sxs-lookup"><span data-stu-id="ec4f8-128">See Also</span></span>  
 [<span data-ttu-id="ec4f8-129">Lager</span><span class="sxs-lookup"><span data-stu-id="ec4f8-129">Inventory</span></span>](inventory-manage-inventory.md)  
 <span data-ttu-id="ec4f8-130">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ec4f8-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
 <span data-ttu-id="ec4f8-131">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ec4f8-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ec4f8-132">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ec4f8-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
 <span data-ttu-id="ec4f8-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ec4f8-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

