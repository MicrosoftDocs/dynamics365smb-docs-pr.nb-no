---
title: Definere transportører | Microsoft-dokumentasjon
description: Du kan definere en kode for hver enkelt transportør og angi opplysninger om dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 49ed631f56730bce647dfe9fc75be2c2fc6b9359
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803604"
---
# <a name="set-up-shipping-agents"></a><span data-ttu-id="626e7-103">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="626e7-103">Set Up Shipping Agents</span></span>
<span data-ttu-id="626e7-104">Du kan definere en kode for hver enkelt transportør og angi opplysninger om dem.</span><span class="sxs-lookup"><span data-stu-id="626e7-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="626e7-105">Hvis du oppgir en internettadresse til transportøren, og vedkommende tilbyr pakkesporingsservice på Internett, kan du bruke funksjonen for automatisk sporing av pakker.</span><span class="sxs-lookup"><span data-stu-id="626e7-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="626e7-106">Hvis du vil ha mer informasjon, kan du se [Spore pakker](sales-how-track-packages.md).</span><span class="sxs-lookup"><span data-stu-id="626e7-106">For more information, see [Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="626e7-107">Når du definerer transportører i ordrene, kan du også angi hvilken service den enkelte transportør tilbyr.</span><span class="sxs-lookup"><span data-stu-id="626e7-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="626e7-108">Du kan definere et ubegrenset serviceantall for hver transportør, og angi en leveringstid for den enkelte service som utføres.</span><span class="sxs-lookup"><span data-stu-id="626e7-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="626e7-109">Når du har tilordnet en transportørservice til en ordrelinje, tas leveringstiden for servicen med i beregningen av ordrebekreftelsen for denne linjen.</span><span class="sxs-lookup"><span data-stu-id="626e7-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="626e7-110">Hvis du vil ha mer informasjon, kan du se [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="626e7-110">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="626e7-111">Slik definerer du transportører</span><span class="sxs-lookup"><span data-stu-id="626e7-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="626e7-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Transportører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="626e7-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="626e7-113">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="626e7-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="626e7-114">.</span><span class="sxs-lookup"><span data-stu-id="626e7-114">.</span></span>  
3.  <span data-ttu-id="626e7-115">Velg handlingen **Transportørservice**.</span><span class="sxs-lookup"><span data-stu-id="626e7-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="626e7-116">I vinduet **Transportørservice** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="626e7-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="626e7-117">Hvis du sletter transportøren på ordrelinjen, slettes også transportørservicekoden.</span><span class="sxs-lookup"><span data-stu-id="626e7-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="626e7-118">Innholdet i feltene som var delvis basert på transportørservice, beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="626e7-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="626e7-119">Se også</span><span class="sxs-lookup"><span data-stu-id="626e7-119">See Also</span></span>
<span data-ttu-id="626e7-120">[Spore pakker](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="626e7-120">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="626e7-121">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="626e7-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="626e7-122">Lager</span><span class="sxs-lookup"><span data-stu-id="626e7-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="626e7-123">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="626e7-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="626e7-124">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="626e7-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="626e7-125">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="626e7-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="626e7-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="626e7-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  