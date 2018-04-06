---
title: "Definere statiske fordelinger basert på fordelingsgrad | Microsoft-dokumentasjon"
description: "Statisk fordelingsmetode er basert på en bestemt verdi, for eksempel kvadratmeteren som brukes, eller et fastsatt fordelingsforhold, for eksempel 5:2:4."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9b58c3889196cba3a6ddbeb50249a6ae962c4ea1
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="d3d7e-103">Eksempelscenario: Definere statiske fordelinger basert på fordelingsgrad</span><span class="sxs-lookup"><span data-stu-id="d3d7e-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="d3d7e-104">Statisk fordelingsmetode er basert på en bestemt verdi, for eksempel kvadratmeteren som brukes, eller et fastsatt fordelingsforhold, for eksempel 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="d3d7e-105">Dette emnet beskriver hvordan du definerer tre nye kostobjekter for fordelingsmål for PROD-kostsenteret for fordelingskilden ved hjelp av det fastsatte fordelingsforholdet på 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="d3d7e-106">De tre målkostobjektene er TILBEHØR, MALING og ARMATUR.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d3d7e-107">I eksempelet brukes demodataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d3d7e-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="d3d7e-108">Slik definerer du PROD-kostsenteret for fordelingskilden i hurtigfanen Generelt:</span><span class="sxs-lookup"><span data-stu-id="d3d7e-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="d3d7e-109">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kostfordeling**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d3d7e-110">I vinduet **Kostfordeling** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-110">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="d3d7e-111">Trykk på Enter eller angi en ID i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="d3d7e-112">I feltet **Grad** angir du **1**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="d3d7e-113">I feltene **Gyldig fra** og **Gyldig til** angir du datoene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="d3d7e-114">Angi **PROD** i feltet **Kostsenterkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="d3d7e-115">I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="d3d7e-116">Slik definerer du kostobjekter for fordelingsmålene i hurtigfanen Linjer:</span><span class="sxs-lookup"><span data-stu-id="d3d7e-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="d3d7e-117">På den første fakturalinjen i feltet **Målkosttype** angir du **9903**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="d3d7e-118">På den første fakturalinjen i feltet **Målkostobjekt** angir du **TILBEHØR**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="d3d7e-119">På den første linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="d3d7e-120">På den første linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="d3d7e-121">På den første linjen, i feltet **Del**, angir du fordelingsforholdet **5**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="d3d7e-122">På den andre fakturalinjen i feltet **Målkosttype** angir du **9903**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="d3d7e-123">På den andre fakturalinjen i feltet **Målkostobjekt** angir du **MALING**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="d3d7e-124">På den andre linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="d3d7e-125">På den andre linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="d3d7e-126">På den andre linjen, i feltet **Del**, angir du fordelingsforholdet **2**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="d3d7e-127">På den tredje fakturalinjen i feltet **Målkosttype** angir du **9903**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="d3d7e-128">På den tredje fakturalinjen i feltet **Målkostobjekt** angir du **ARMATUR**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="d3d7e-129">På den tredje linjen, i feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle påløpte kostnader fordeles.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="d3d7e-130">På den tredje linjen i **Grunnlag**-feltet velger du **Statisk** for å bruke den statiske fordelingsmetoden.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="d3d7e-131">På den tredje linjen, i feltet **Del**, angir du fordelingsforholdet **4**.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="d3d7e-132"> beregner automatisk **Prosent**-feltet ved å bruke en prosentsats som er avhengige av alle de tre fordelingsforholdene som er angitt i **Del**-feltet for alle de tre linjene.</span><span class="sxs-lookup"><span data-stu-id="d3d7e-132"> automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3d7e-133">Se også</span><span class="sxs-lookup"><span data-stu-id="d3d7e-133">See Also</span></span>  
<span data-ttu-id="d3d7e-134">[Definere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="d3d7e-134">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
<span data-ttu-id="d3d7e-135">[Definere og fordele kostnader](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="d3d7e-135">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
<span data-ttu-id="d3d7e-136">[Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span><span class="sxs-lookup"><span data-stu-id="d3d7e-136">[Scenario Example: Defining Dynamic Allocations Based on Items Sold](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md) </span></span>  
[<span data-ttu-id="d3d7e-137">Definere og fordele kostnader</span><span class="sxs-lookup"><span data-stu-id="d3d7e-137">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)

