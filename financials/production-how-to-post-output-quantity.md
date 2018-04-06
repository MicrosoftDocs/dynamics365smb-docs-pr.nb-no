---
title: "Slik massebokfører du produksjonsavgang og operasjonstider | Microsoft-dokumentasjon"
description: Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="83fc2-103">Bokføre avgang og operasjonstid</span><span class="sxs-lookup"><span data-stu-id="83fc2-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="83fc2-104">Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.</span><span class="sxs-lookup"><span data-stu-id="83fc2-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="83fc2-105">Bare når du bokfører avgangsantall i den siste operasjonen, oppdateres beholdningen automatisk.</span><span class="sxs-lookup"><span data-stu-id="83fc2-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="83fc2-106">Slik bokfører du avgangsantall for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="83fc2-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="83fc2-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="83fc2-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="83fc2-108">Fyll ut feltene med produksjonsordre- og avgangsdata.</span><span class="sxs-lookup"><span data-stu-id="83fc2-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="83fc2-109">Hvis operasjonen er fullført, velger du **Ferdig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="83fc2-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="83fc2-110">Hvis lagerlokasjonen der varene skal plasseres bruker hyller, men ikke krever plasseringsbehandling,  tildeler du en hyllekode til kladdelinjen for å angi hvor varene skal lagres på lageret</span><span class="sxs-lookup"><span data-stu-id="83fc2-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="83fc2-111">Hvis du vil ha mer informasjon, kan du se [Plassere produksjonsavgang eller monteringsavgang](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="83fc2-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="83fc2-112">Velg **Bokfør** for å bokføre operasjonene.</span><span class="sxs-lookup"><span data-stu-id="83fc2-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="83fc2-113">Avgangsantallet bokføres.</span><span class="sxs-lookup"><span data-stu-id="83fc2-113">The output quantity will be posted.</span></span> <span data-ttu-id="83fc2-114">Varen kan nå leveres.</span><span class="sxs-lookup"><span data-stu-id="83fc2-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="83fc2-115">Slik bokfører du kjøretid for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="83fc2-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="83fc2-116">Operasjonstiden representerer arbeidsframdrift i form av nødvendig arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="83fc2-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="83fc2-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="83fc2-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="83fc2-118">Fyll ut feltene med produksjonsordre- og avgangsdata.</span><span class="sxs-lookup"><span data-stu-id="83fc2-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="83fc2-119">Hvis operasjonen er fullført, velger du **Ferdig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="83fc2-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="83fc2-120">Velg **Bokfør**-handlingen for å bokføre tiden som brukes per operasjon.</span><span class="sxs-lookup"><span data-stu-id="83fc2-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="83fc2-121">Kapasitetsposter oppdateres for brukte arbeids- eller produksjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="83fc2-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="83fc2-122">Se også</span><span class="sxs-lookup"><span data-stu-id="83fc2-122">See Also</span></span>  
<span data-ttu-id="83fc2-123">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="83fc2-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="83fc2-124">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="83fc2-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="83fc2-125">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="83fc2-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="83fc2-126">Lager</span><span class="sxs-lookup"><span data-stu-id="83fc2-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="83fc2-127">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="83fc2-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="83fc2-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="83fc2-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

