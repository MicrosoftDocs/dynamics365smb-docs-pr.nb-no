---
title: Definere plasseringsmaler | Microsoft-dokumentasjon
description: "Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7fecd72242d30291d3741ee99fcb3ee5bc09af9f
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="e27b5-103">Definere plasseringsmaler</span><span class="sxs-lookup"><span data-stu-id="e27b5-103">Set Up Put-away Templates</span></span>
<span data-ttu-id="e27b5-104">Med funksjonaliteten for lagerstyring foreslås den hyllen som passer best til varene på et hvilket som helst tidspunkt, i henhold til den plasseringsmalen du har definert for lageret, de hylleprioriteringene du har gitt til hyllene, og de minimums- og maksimumsantallene du har definert for faste hyller.</span><span class="sxs-lookup"><span data-stu-id="e27b5-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="e27b5-105">Du kan definere flere plasseringsmaler og velge én av dem som i hovedsak skal styre plasseringene i lageret.</span><span class="sxs-lookup"><span data-stu-id="e27b5-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="e27b5-106">Du kan også velge en plasseringsmal for en hvilken som helst vare eller lagerføringsenhet som kan ha spesielle plasseringskrav.</span><span class="sxs-lookup"><span data-stu-id="e27b5-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="e27b5-107">Slik setter du opp plasseringsmaler</span><span class="sxs-lookup"><span data-stu-id="e27b5-107">To set up put-away templates</span></span>  
1.  <span data-ttu-id="e27b5-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plasseringsmaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e27b5-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e27b5-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e27b5-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e27b5-110">Angi en kode som er den unike identifikatoren for malen du er i ferd med å opprette.</span><span class="sxs-lookup"><span data-stu-id="e27b5-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4.  <span data-ttu-id="e27b5-111">Hvis du vil, kan du angi en kort beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e27b5-111">Enter a short description, if you wish.</span></span>  
5.  <span data-ttu-id="e27b5-112">Fyll ut den første linjen med de hyllekravene du først og fremst vil skal oppfylles når en plassering foreslås.</span><span class="sxs-lookup"><span data-stu-id="e27b5-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>  
6.  <span data-ttu-id="e27b5-113">Fyll ut den andre linjen med hyllekravene som skal være ditt andrevalg å oppfylle når en hylle blir funnet for plasseringen.</span><span class="sxs-lookup"><span data-stu-id="e27b5-113">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="e27b5-114">Den andre linjen brukes bare hvis det ikke blir funnet en hylle som oppfyller kravene på den første linjen.</span><span class="sxs-lookup"><span data-stu-id="e27b5-114">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7.  <span data-ttu-id="e27b5-115">Fortsett med å fylle ut linjene til du har beskrevet alle de akseptable hylleplasseringene du vil bruke i plasseringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="e27b5-115">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8.  <span data-ttu-id="e27b5-116">På den siste linjen i plasseringsmalen merker du av for **Finn flytende hylle**.</span><span class="sxs-lookup"><span data-stu-id="e27b5-116">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="e27b5-117">Du kan opprette forskjellige plasseringsmaler og deretter bruke dem slik det passer.</span><span class="sxs-lookup"><span data-stu-id="e27b5-117">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="e27b5-118">Plasseringsmalen du har valgt for varen eller lagerføringsenheten, brukes først, hvis du har valgt en mal.</span><span class="sxs-lookup"><span data-stu-id="e27b5-118">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="e27b5-119">Hvis disse feltene ikke er utfylt, brukes plasseringsmalen du valgte for lageret på hurtigfanen **Hylleprinsipp** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="e27b5-119">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e27b5-120">Se også</span><span class="sxs-lookup"><span data-stu-id="e27b5-120">See Also</span></span>  
[<span data-ttu-id="e27b5-121">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="e27b5-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="e27b5-122">Lager</span><span class="sxs-lookup"><span data-stu-id="e27b5-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="e27b5-123">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="e27b5-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="e27b5-124">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="e27b5-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="e27b5-125">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="e27b5-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="e27b5-126">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e27b5-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

