---
title: Bokføre kapasiteter | Microsoft-dokumentasjon
description: I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 58005b8b4d401f5eab8a934d7b00b610b64b4281
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "928303"
---
# <a name="post-capacities"></a><span data-ttu-id="4782c-104">Bokføre kapasiteter</span><span class="sxs-lookup"><span data-stu-id="4782c-104">Post Capacities</span></span>
<span data-ttu-id="4782c-105">I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="4782c-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="4782c-106">Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="4782c-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="4782c-107">Slik bokfører du kapasiteter</span><span class="sxs-lookup"><span data-stu-id="4782c-107">To post capacities</span></span>  
1.  <span data-ttu-id="4782c-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kapasitetskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4782c-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4782c-109">Fyll ut feltene **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="4782c-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="4782c-110">I feltet **Type** angir du kapasitetstypen, enten **Produksjonsressurs** eller **Arbeidssenter**, du bokfører.</span><span class="sxs-lookup"><span data-stu-id="4782c-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="4782c-111">I feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="4782c-111">In the **No.**</span></span> <span data-ttu-id="4782c-112">angir du nummeret på produksjonsressursen eller arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="4782c-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="4782c-113">Skriv inn relevante opplysninger i de andre feltene, for eksempel **Starttidspunkt**, **Sluttidspunkt**, **Antall** og **Vrak**.</span><span class="sxs-lookup"><span data-stu-id="4782c-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="4782c-114">Velg handlingen **Bokfør** for å bokføre kapasitetene.</span><span class="sxs-lookup"><span data-stu-id="4782c-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="4782c-115">Slik viser du arbeidssenterposter:</span><span class="sxs-lookup"><span data-stu-id="4782c-115">To view work center ledger entries</span></span>  
<span data-ttu-id="4782c-116">På sidene **Arbeidssenterkort** og **Maskinsenterkort** kan du vise bokførte kapasiteter som et resultat av ferdige produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="4782c-116">In the **Work Center Card** and **Machine Center Card** pages, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="4782c-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidssentre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4782c-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4782c-118">Åpne det aktuelle **Arbeidssenter**-kortet fra listen, og velg handlingen **Kapasitetsposter**.</span><span class="sxs-lookup"><span data-stu-id="4782c-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="4782c-119">**Kapasitetsposter**-siden viser de bokførte postene fra arbeidssenteret i den rekkefølgen de ble bokført.</span><span class="sxs-lookup"><span data-stu-id="4782c-119">The **Capacity Ledger Entries** page displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="4782c-120">Se også</span><span class="sxs-lookup"><span data-stu-id="4782c-120">See Also</span></span>  
<span data-ttu-id="4782c-121">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="4782c-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="4782c-122">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="4782c-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="4782c-123">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="4782c-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="4782c-124">Lager</span><span class="sxs-lookup"><span data-stu-id="4782c-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4782c-125">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4782c-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="4782c-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4782c-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
