---
title: Bruke vareserier i produksjon | Microsoft-dokumentasjon
description: Hovedoppgaven med å tilpasse en hovedkalender for selskapet, eller selskapets forretningspartner, er å angi eventuelle endringer i statusen for arbeids- eller fridager.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9d0b27a1bdcc2aa544c50cf9993d46405f519b0c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787605"
---
# <a name="work-with-production-families"></a><span data-ttu-id="99e5c-103">Arbeide med produksjonsfamilier</span><span class="sxs-lookup"><span data-stu-id="99e5c-103">Work with Production Families</span></span>
<span data-ttu-id="99e5c-104">En produksjonsfamilie er en gruppe individuelle varer der forbindelsen er basert på likheten i produksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="99e5c-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="99e5c-105">Ved hjelp av produksjonsfamilier kan noen varer produseres to eller flere ganger i én produksjon, noe som optimaliserer materialforbruket.</span><span class="sxs-lookup"><span data-stu-id="99e5c-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="99e5c-106">I **Antall**-feltet på **Familie**-siden angir du antallet som skal produseres når hele familien er produsert én gang.</span><span class="sxs-lookup"><span data-stu-id="99e5c-106">In the **Quantity** field on the **Family** page, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="99e5c-107">Eksempel</span><span class="sxs-lookup"><span data-stu-id="99e5c-107">Example</span></span>
<span data-ttu-id="99e5c-108">I utstansingsprosesser kan fire enheter av samme vare produseres fra ett ark, samtidig med 10 enheter av en annen, forskjellig vare.</span><span class="sxs-lookup"><span data-stu-id="99e5c-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="99e5c-109">Utstansingsmaskinen utstanser alle de 14 enhetene i én operasjon.</span><span class="sxs-lookup"><span data-stu-id="99e5c-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="99e5c-110">Når du definerer produksjonsfamilier, reduseres vrakantallet, fordi det som vanligvis ville blitt overflødig vrak ved produksjon av store enheter, i stedet brukes til å produsere små varer.</span><span class="sxs-lookup"><span data-stu-id="99e5c-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="99e5c-111">Slik konfigurerer du produksjonsfamilier</span><span class="sxs-lookup"><span data-stu-id="99e5c-111">To set up a production family</span></span>
1. <span data-ttu-id="99e5c-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Familier**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="99e5c-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="99e5c-113">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="99e5c-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a><span data-ttu-id="99e5c-114">Produsere basert på en produksjonsfamilie</span><span class="sxs-lookup"><span data-stu-id="99e5c-114">To produce based on a production family</span></span>
1. <span data-ttu-id="99e5c-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="99e5c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="99e5c-116">Opprett en ny produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="99e5c-116">Create a new production order.</span></span> <span data-ttu-id="99e5c-117">Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="99e5c-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="99e5c-118">Velg **Familie** i **Kildetype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="99e5c-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="99e5c-119">Velg den aktuelle produksjonsfamilien i **Kildenr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="99e5c-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="99e5c-120">Se også</span><span class="sxs-lookup"><span data-stu-id="99e5c-120">See Also</span></span>
[<span data-ttu-id="99e5c-121">Opprette produksjonsstykklister</span><span class="sxs-lookup"><span data-stu-id="99e5c-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="99e5c-122">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="99e5c-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="99e5c-123">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="99e5c-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="99e5c-124">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="99e5c-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="99e5c-125">Lager</span><span class="sxs-lookup"><span data-stu-id="99e5c-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="99e5c-126">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="99e5c-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="99e5c-127">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99e5c-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]