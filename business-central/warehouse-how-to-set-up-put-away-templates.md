---
title: Definere plasseringsmaler | Microsoft-dokumentasjon
description: Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller.
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
ms.openlocfilehash: 83ae54e61c5881cce9a58c6684bbf82c4b3ad750
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802869"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="94046-103">Definere plasseringsmaler</span><span class="sxs-lookup"><span data-stu-id="94046-103">Set Up Put-away Templates</span></span>
<span data-ttu-id="94046-104">Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller.</span><span class="sxs-lookup"><span data-stu-id="94046-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="94046-105">Du kan definere flere plasseringsmaler og velge én av dem som i hovedsak skal styre plasseringene i lageret.</span><span class="sxs-lookup"><span data-stu-id="94046-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="94046-106">Du kan også velge en plasseringsmal for en hvilken som helst vare eller lagerføringsenhet som kan ha spesielle plasseringskrav.</span><span class="sxs-lookup"><span data-stu-id="94046-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="94046-107">Slik setter du opp plasseringsmaler</span><span class="sxs-lookup"><span data-stu-id="94046-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="94046-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Plasseringsmaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="94046-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="94046-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="94046-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="94046-110">Angi en kode som er den unike identifikatoren for malen du er i ferd med å opprette.</span><span class="sxs-lookup"><span data-stu-id="94046-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="94046-111">Hvis du vil, kan du angi en kort beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="94046-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="94046-112">Fyll ut den første linjen med de hyllekravene du først og fremst vil skal oppfylles når en plassering foreslås.</span><span class="sxs-lookup"><span data-stu-id="94046-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="94046-113">Fyll ut den andre linjen med hyllekravene som skal være ditt andrevalg å oppfylle når en hylle blir funnet for plasseringen.</span><span class="sxs-lookup"><span data-stu-id="94046-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="94046-114">Den andre linjen brukes bare hvis det ikke blir funnet en hylle som oppfyller kravene på den første linjen.</span><span class="sxs-lookup"><span data-stu-id="94046-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="94046-115">Fortsett med å fylle ut linjene til du har beskrevet alle de akseptable hylleplasseringene du vil bruke i plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="94046-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="94046-116">På den siste linjen i plasseringsmalen merker du av for **Finn flytende hylle**.</span><span class="sxs-lookup"><span data-stu-id="94046-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="94046-117">Du kan opprette forskjellige plasseringsmaler og deretter bruke dem slik det passer.</span><span class="sxs-lookup"><span data-stu-id="94046-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="94046-118">Plasseringsmalen du har valgt for varen eller lagerføringsenheten, brukes først, hvis du har valgt en mal.</span><span class="sxs-lookup"><span data-stu-id="94046-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="94046-119">Hvis disse feltene ikke er utfylt, brukes plasseringsmalen du valgte for lageret på hurtigfanen **Hylleprinsipp** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="94046-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="94046-120">Se også</span><span class="sxs-lookup"><span data-stu-id="94046-120">See Also</span></span>  
[<span data-ttu-id="94046-121">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="94046-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="94046-122">Lager</span><span class="sxs-lookup"><span data-stu-id="94046-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="94046-123">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="94046-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="94046-124">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="94046-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="94046-125">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="94046-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="94046-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94046-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>