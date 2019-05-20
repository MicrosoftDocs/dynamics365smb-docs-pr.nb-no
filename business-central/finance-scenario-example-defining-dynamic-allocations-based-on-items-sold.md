---
title: Eksempelscenario - Definere dynamiske fordelinger basert på solgte varer | Microsoft-dokumentasjon
description: Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling.
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
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 7219e1d56129da66e802aa0b4ea5df946dc34e04
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239593"
---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="51fe9-103">Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer</span><span class="sxs-lookup"><span data-stu-id="51fe9-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="51fe9-104">Dette emnet viser et eksempel på hvordan du kan definere fordelinger ved hjelp av metoden dynamisk tildeling.</span><span class="sxs-lookup"><span data-stu-id="51fe9-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="51fe9-105">I eksemplet endrer du dynamisk fordeling av kostnadene for SALG-kostsenteret slik at det støtter det nye kostobjektet IT-UTSTYR.</span><span class="sxs-lookup"><span data-stu-id="51fe9-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="51fe9-106">IT-UTSTYR-pakker har varenumre i området fra 8904-W til 8924-W.</span><span class="sxs-lookup"><span data-stu-id="51fe9-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="51fe9-107">Du kan bruke salgstall for fjoråret til å beregne andelen.</span><span class="sxs-lookup"><span data-stu-id="51fe9-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="51fe9-108">Tildelingen er bokført til hjelpekosttype 9903.</span><span class="sxs-lookup"><span data-stu-id="51fe9-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="51fe9-109">I eksempelet brukes demodataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="51fe9-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="51fe9-110">Slik definerer du dynamisk fordelinger basert på varer solgt i fjoråret:</span><span class="sxs-lookup"><span data-stu-id="51fe9-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="51fe9-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostfordelinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="51fe9-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="51fe9-112">På siden **Kostfordeling** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-112">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="51fe9-113">Trykk på Enter eller angi en ID i **ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="51fe9-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="51fe9-114">I feltet **Grad** angir du **1**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="51fe9-115">I feltene **Gyldig fra** og **Gyldig til** angir du datoene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="51fe9-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="51fe9-116">Angi **SALG** i feltet **Kostsenterkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="51fe9-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="51fe9-117">I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="51fe9-118">I feltet **Krediter til kosttype** skriver du inn kosttypen **9903**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="51fe9-119">Velg **Ny** i feltet **Målkostobjekt** for å opprette det nye kostobjektet IT-UTSTYR, og fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="51fe9-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="51fe9-120">Velg **IT-UTSTYR**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="51fe9-121">La **Målkostsenter**-feltet være tomt.</span><span class="sxs-lookup"><span data-stu-id="51fe9-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="51fe9-122">I feltet **Fordelingsmåltype**, velger du **All kost** for å definere hvordan alle akkumulerte kostnader fordeles.</span><span class="sxs-lookup"><span data-stu-id="51fe9-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="51fe9-123">Velg fordelingsgrunnlaget **Solgte varer (beløp)** i **Grunnlag**-feltet.</span><span class="sxs-lookup"><span data-stu-id="51fe9-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="51fe9-124">I feltet **Nr.filter** skriver du inn **8904-W..8924-W**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="51fe9-125">I feltet **Datofilterkode** skriver du inn **I fjor**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="51fe9-126">Hvis du vil beregne delen, velger du handlingen **Beregn fordelingsnøkkel**.</span><span class="sxs-lookup"><span data-stu-id="51fe9-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="51fe9-127">bruker forrige års salgstall til å beregne en andel av 1596,50 NOK med 100 prosent for IT-UTSTYR-pakker.</span><span class="sxs-lookup"><span data-stu-id="51fe9-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="51fe9-128">Dette betyr at alle varene som er solgt det siste året vil bli fordelt til kostobjektet IT-UTSTYR.</span><span class="sxs-lookup"><span data-stu-id="51fe9-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="51fe9-129">Se også</span><span class="sxs-lookup"><span data-stu-id="51fe9-129">See Also</span></span>  
[<span data-ttu-id="51fe9-130">Definere og fordele kostnader</span><span class="sxs-lookup"><span data-stu-id="51fe9-130">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="51fe9-131">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="51fe9-131">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="51fe9-132">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="51fe9-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)
