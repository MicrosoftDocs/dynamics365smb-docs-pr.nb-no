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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4b0bb12f86a8984ca4a87d679bc22a0e34e51c88
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-capacities"></a><span data-ttu-id="4fc6f-104">Bokføre kapasiteter</span><span class="sxs-lookup"><span data-stu-id="4fc6f-104">How to: Post Capacities</span></span>
<span data-ttu-id="4fc6f-105">I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="4fc6f-106">Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="4fc6f-107">Slik bokfører du kapasiteter</span><span class="sxs-lookup"><span data-stu-id="4fc6f-107">To post capacities</span></span>  
1.  <span data-ttu-id="4fc6f-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kapasitetskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4fc6f-109">Fyll ut feltene **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="4fc6f-110">I feltet **Type** angir du kapasitetstypen, enten **Produksjonsressurs** eller **Arbeidssenter**, du bokfører.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="4fc6f-111">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4fc6f-111">In the **No.**</span></span> <span data-ttu-id="4fc6f-112">angir du nummeret på produksjonsressursen eller arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="4fc6f-113">Skriv inn relevante opplysninger i de andre feltene, for eksempel **Starttidspunkt**, **Sluttidspunkt**, **Antall** og **Vrak**.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="4fc6f-114">Velg handlingen **Bokfør** for å bokføre kapasitetene.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="4fc6f-115">Slik viser du arbeidssenterposter:</span><span class="sxs-lookup"><span data-stu-id="4fc6f-115">To view work center ledger entries</span></span>  
<span data-ttu-id="4fc6f-116">I vinduet **Arbeidssenterkort** og **Maskinsenterkort** kan du vise bokførte kapasiteter som et resultat av ferdige produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="4fc6f-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4fc6f-118">Åpne det aktuelle **Arbeidssenter**-kortet fra listen, og velg handlingen **Kapasitetsposter**.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="4fc6f-119">**Kapasitetsposter**-vinduet viser de bokførte postene fra arbeidssenteret i den rekkefølgen de ble bokført.</span><span class="sxs-lookup"><span data-stu-id="4fc6f-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="4fc6f-120">Se også</span><span class="sxs-lookup"><span data-stu-id="4fc6f-120">See Also</span></span>  
<span data-ttu-id="4fc6f-121">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4fc6f-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4fc6f-122">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="4fc6f-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4fc6f-123">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="4fc6f-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="4fc6f-124">Lager</span><span class="sxs-lookup"><span data-stu-id="4fc6f-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4fc6f-125">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4fc6f-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4fc6f-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4fc6f-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

