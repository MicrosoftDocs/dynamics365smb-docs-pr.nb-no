---
title: "Bokføre kapasiteter | Microsoft-dokumentasjon"
description: "I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre."
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
ms.openlocfilehash: a30e62bf2bf62c547398d733fcfe80b0204805cf
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="post-capacities"></a><span data-ttu-id="5f85b-104">Bokføre kapasiteter</span><span class="sxs-lookup"><span data-stu-id="5f85b-104">Post Capacities</span></span>
<span data-ttu-id="5f85b-105">I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="5f85b-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="5f85b-106">Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="5f85b-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="5f85b-107">Slik bokfører du kapasiteter</span><span class="sxs-lookup"><span data-stu-id="5f85b-107">To post capacities</span></span>  
1.  <span data-ttu-id="5f85b-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kapasitetskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5f85b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f85b-109">Fyll ut feltene **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="5f85b-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="5f85b-110">I feltet **Type** angir du kapasitetstypen, enten **Produksjonsressurs** eller **Arbeidssenter**, du bokfører.</span><span class="sxs-lookup"><span data-stu-id="5f85b-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="5f85b-111">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="5f85b-111">In the **No.**</span></span> <span data-ttu-id="5f85b-112">angir du nummeret på produksjonsressursen eller arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="5f85b-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="5f85b-113">Skriv inn relevante opplysninger i de andre feltene, for eksempel **Starttidspunkt**, **Sluttidspunkt**, **Antall** og **Vrak**.</span><span class="sxs-lookup"><span data-stu-id="5f85b-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="5f85b-114">Velg handlingen **Bokfør** for å bokføre kapasitetene.</span><span class="sxs-lookup"><span data-stu-id="5f85b-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="5f85b-115">Slik viser du arbeidssenterposter:</span><span class="sxs-lookup"><span data-stu-id="5f85b-115">To view work center ledger entries</span></span>  
<span data-ttu-id="5f85b-116">I vinduet **Arbeidssenterkort** og **Maskinsenterkort** kan du vise bokførte kapasiteter som et resultat av ferdige produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f85b-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="5f85b-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="5f85b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5f85b-118">Åpne det aktuelle **Arbeidssenter**-kortet fra listen, og velg handlingen **Kapasitetsposter**.</span><span class="sxs-lookup"><span data-stu-id="5f85b-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="5f85b-119">**Kapasitetsposter**-vinduet viser de bokførte postene fra arbeidssenteret i den rekkefølgen de ble bokført.</span><span class="sxs-lookup"><span data-stu-id="5f85b-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="5f85b-120">Se også</span><span class="sxs-lookup"><span data-stu-id="5f85b-120">See Also</span></span>  
<span data-ttu-id="5f85b-121">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="5f85b-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="5f85b-122">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="5f85b-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="5f85b-123">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="5f85b-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="5f85b-124">Lager</span><span class="sxs-lookup"><span data-stu-id="5f85b-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="5f85b-125">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="5f85b-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5f85b-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f85b-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

