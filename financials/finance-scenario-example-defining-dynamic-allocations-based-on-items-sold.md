---
title: "Eksempelscenario - Definere dynamiske fordelinger basert på solgte varer | Microsoft-dokumentasjon"
description: "Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling."
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
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="dfaba-103">Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer</span><span class="sxs-lookup"><span data-stu-id="dfaba-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="dfaba-104">Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling.</span><span class="sxs-lookup"><span data-stu-id="dfaba-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="dfaba-105">I eksemplet endrer du dynamisk fordeling av kostnadene for SALG-kostsenteret slik at det støtter det nye kostobjektet IT-UTSTYR.</span><span class="sxs-lookup"><span data-stu-id="dfaba-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="dfaba-106">IT-UTSTYR-pakker har varenumre i området fra 8904-W til 8924-W.</span><span class="sxs-lookup"><span data-stu-id="dfaba-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="dfaba-107">Du kan bruke salgstall for fjoråret til å beregne andelen.</span><span class="sxs-lookup"><span data-stu-id="dfaba-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="dfaba-108">Tildelingen er bokført til hjelpekosttype 9903.</span><span class="sxs-lookup"><span data-stu-id="dfaba-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="dfaba-109">I eksempelet brukes demodataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="dfaba-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="dfaba-110">Slik definerer du dynamisk fordelinger basert på varer solgt i fjoråret:</span><span class="sxs-lookup"><span data-stu-id="dfaba-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="dfaba-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kostfordelinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="dfaba-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="dfaba-112">I vinduet **Kostfordeling** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="dfaba-113">Trykk på Enter eller angi en ID i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfaba-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="dfaba-114">I feltet **Grad** angir du **1**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="dfaba-115">I feltene **Gyldig fra** og **Gyldig til** angir du datoene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="dfaba-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="dfaba-116">Angi **SALG** i feltet **Kostsenterkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfaba-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="dfaba-117">I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="dfaba-118">I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="dfaba-119">Velg **Ny** i feltet **Målkostobjekt** for å opprette det nye kostobjektet IT-UTSTYR, og fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="dfaba-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="dfaba-120">Velg **IT-UTSTYR**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="dfaba-121">La **Målkostsenter**-feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="dfaba-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="dfaba-122">I feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle akkumulerte kostnader fordeles.</span><span class="sxs-lookup"><span data-stu-id="dfaba-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="dfaba-123">Velg fordelingsgrunnlaget **Solgte varer (beløp)** i **Grunnlag**-feltet.</span><span class="sxs-lookup"><span data-stu-id="dfaba-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="dfaba-124">I feltet **Nr.filter** skriver du inn **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="dfaba-125">I feltet **Datofilterkode** skriver du inn **I fjor**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="dfaba-126">Hvis du vil beregne delen, velger du handlingen **Beregn fordelingsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="dfaba-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="dfaba-127"> bruker forrige års salgstall til å beregne en andel av 1596,50 NOK med 100 prosent for IT-UTSTYR-pakker.</span><span class="sxs-lookup"><span data-stu-id="dfaba-127"> uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="dfaba-128">Dette betyr at alle varene som er solgt det siste året vil bli fordelt til kostobjektet IT-UTSTYR.</span><span class="sxs-lookup"><span data-stu-id="dfaba-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="dfaba-129">Se også</span><span class="sxs-lookup"><span data-stu-id="dfaba-129">See Also</span></span>  
 <span data-ttu-id="dfaba-130">[Angi filtre for dynamisk fordelingsgrunnlag](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="dfaba-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="dfaba-131">[Definere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="dfaba-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="dfaba-132">[Definere og fordele kostnader](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="dfaba-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="dfaba-133">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="dfaba-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="dfaba-134">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="dfaba-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

