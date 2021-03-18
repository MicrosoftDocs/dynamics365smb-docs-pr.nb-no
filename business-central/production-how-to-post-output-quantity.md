---
title: Slik massebokfører du produksjonsavgang og operasjonstider | Microsoft-dokumentasjon
description: Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83354217bac3b27457303083163cf5eae4494e79
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380459"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="fee1a-103">Bokføre avgang og operasjonstid</span><span class="sxs-lookup"><span data-stu-id="fee1a-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="fee1a-104">Avgangsantallet representerer arbeidsframdriften i form av det ferdige antallet.</span><span class="sxs-lookup"><span data-stu-id="fee1a-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="fee1a-105">Bare når du bokfører avgangsantall i den siste operasjonen, oppdateres beholdningen automatisk.</span><span class="sxs-lookup"><span data-stu-id="fee1a-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="fee1a-106">Slik bokfører du avgangsantall for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="fee1a-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="fee1a-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fee1a-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fee1a-108">Fyll ut feltene med produksjonsordre- og avgangsdata.</span><span class="sxs-lookup"><span data-stu-id="fee1a-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="fee1a-109">Hvis operasjonen er fullført, velger du **Ferdig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fee1a-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="fee1a-110">Hvis lagerlokasjonen der varene skal plasseres bruker hyller, men ikke krever plasseringsbehandling, tildeler du en hyllekode til kladdelinjen for å angi hvor varene skal lagres på lageret</span><span class="sxs-lookup"><span data-stu-id="fee1a-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="fee1a-111">Hvis du vil ha mer informasjon, kan du se [Plassere produksjonsavgang eller monteringsavgang](warehouse-how-to-put-away-production-output.md).</span><span class="sxs-lookup"><span data-stu-id="fee1a-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="fee1a-112">Velg **Bokfør** for å bokføre operasjonene.</span><span class="sxs-lookup"><span data-stu-id="fee1a-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="fee1a-113">Avgangsantallet bokføres.</span><span class="sxs-lookup"><span data-stu-id="fee1a-113">The output quantity will be posted.</span></span> <span data-ttu-id="fee1a-114">Varen kan nå leveres.</span><span class="sxs-lookup"><span data-stu-id="fee1a-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="fee1a-115">Slik bokfører du kjøretid for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="fee1a-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="fee1a-116">Operasjonstiden representerer arbeidsframdrift i form av nødvendig arbeidstid.</span><span class="sxs-lookup"><span data-stu-id="fee1a-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="fee1a-117">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fee1a-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fee1a-118">Fyll ut feltene med produksjonsordre- og avgangsdata.</span><span class="sxs-lookup"><span data-stu-id="fee1a-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="fee1a-119">Hvis operasjonen er fullført, velger du **Ferdig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fee1a-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="fee1a-120">Velg **Bokfør**-handlingen for å bokføre tiden som brukes per operasjon.</span><span class="sxs-lookup"><span data-stu-id="fee1a-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="fee1a-121">Kapasitetsposter oppdateres for brukte arbeids- eller produksjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="fee1a-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="fee1a-122">Se også</span><span class="sxs-lookup"><span data-stu-id="fee1a-122">See Also</span></span>  
<span data-ttu-id="fee1a-123">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="fee1a-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="fee1a-124">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="fee1a-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="fee1a-125">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="fee1a-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="fee1a-126">Lager</span><span class="sxs-lookup"><span data-stu-id="fee1a-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="fee1a-127">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="fee1a-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="fee1a-128">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fee1a-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]