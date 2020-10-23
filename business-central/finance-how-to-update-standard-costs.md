---
title: Oppdatere standardkost | Microsoft-dokumentasjon
description: Du må regelmessig oppdatere standardkostnadene for komponenter og opprullere de nye kostnadene til den overordnede varen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8343a4169c127abdcee18a0a2e15cbc5f6b2b7c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924106"
---
# <a name="update-standard-costs"></a><span data-ttu-id="36e54-103">Oppdatere standardkost</span><span class="sxs-lookup"><span data-stu-id="36e54-103">Update Standard Costs</span></span>
<span data-ttu-id="36e54-104">Du må regelmessig oppdatere standardkostnadene for komponenter og opprullere de nye kostnadene til den overordnede varen.</span><span class="sxs-lookup"><span data-stu-id="36e54-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="36e54-105">Prosessen består vanligvis av følgende fire trinn:</span><span class="sxs-lookup"><span data-stu-id="36e54-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="36e54-106">Oppdatere kost på komponent- og kapasitetsnivået.</span><span class="sxs-lookup"><span data-stu-id="36e54-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="36e54-107">Hvis du vil ha mer informasjon, se kjørselen **Foreslå standardkost for vare**.</span><span class="sxs-lookup"><span data-stu-id="36e54-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="36e54-108">Konsolider og rull opp komponent- og kapasitetskost for å beregne samlet produksjons- eller monteringskost for varene.</span><span class="sxs-lookup"><span data-stu-id="36e54-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="36e54-109">Implementere standardkostnadene som angis når du kjører de forrige kjørslene.</span><span class="sxs-lookup"><span data-stu-id="36e54-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="36e54-110">Standardkostnadene trer ikke i kraft før de blir implementert.</span><span class="sxs-lookup"><span data-stu-id="36e54-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="36e54-111">Hvis du vil ha mer informasjon, se Implementer endringer i standardkost.</span><span class="sxs-lookup"><span data-stu-id="36e54-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="36e54-112">Implementere endringene for å oppdatere **Enhetskost**-feltet på varekortet og utføre revaluering av lager.</span><span class="sxs-lookup"><span data-stu-id="36e54-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="36e54-113">Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="36e54-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="36e54-114">Hvis du vil ha mer informasjon, kan du se [Om beregning av standardkost](finance-about-calculating-standard-cost.md).</span><span class="sxs-lookup"><span data-stu-id="36e54-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="36e54-115">Slik oppdaterer du standardkost</span><span class="sxs-lookup"><span data-stu-id="36e54-115">To update standard costs</span></span>  
1.  <span data-ttu-id="36e54-116">Kjør kjørselen **Juster kostverdi - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="36e54-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="36e54-117">Kjør kjørselen **Bokfør lagerkost i Finans**.</span><span class="sxs-lookup"><span data-stu-id="36e54-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="36e54-118">Åpne **Standardkost - forslag**, og bruk én eller flere av følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="36e54-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="36e54-119">Kjør kjørselen **Foreslå standardkost for vare**.</span><span class="sxs-lookup"><span data-stu-id="36e54-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="36e54-120">Gå gjennom resultatene, og foreta nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="36e54-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="36e54-121">Kjør kjørselen **Foreslå standardkost for kapasitet**.</span><span class="sxs-lookup"><span data-stu-id="36e54-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="36e54-122">Gå gjennom resultatene, og foreta nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="36e54-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="36e54-123">Kjør kjørselen **Oppruller standardkost**.</span><span class="sxs-lookup"><span data-stu-id="36e54-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="36e54-124">Gå gjennom resultatene, og foreta nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="36e54-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="36e54-125">Kjør kjørselen **Implementer endringer i standardkost**.</span><span class="sxs-lookup"><span data-stu-id="36e54-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="36e54-126">Gå gjennom og bokfør siden **Revalueringskladd**, som er fylt ut med poster fra tidligere trinn i denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="36e54-126">Review and post the **Revaluation Journal** page, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="36e54-127">Se også</span><span class="sxs-lookup"><span data-stu-id="36e54-127">See Also</span></span>  
 <span data-ttu-id="36e54-128">[Om beregning av standardkost](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="36e54-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="36e54-129">[Administrere lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="36e54-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="36e54-130">[Designdetaljer: Kostmetoder](design-details-costing-methods.md) [Finans](finance.md)</span><span class="sxs-lookup"><span data-stu-id="36e54-130">[Design Details: Costing Methods](design-details-costing-methods.md) [Finance](finance.md)</span></span>  
 <span data-ttu-id="36e54-131">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="36e54-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
