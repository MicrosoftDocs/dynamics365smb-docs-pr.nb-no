---
title: Massebokføre forbruk
description: Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787905"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="95b80-103">Massebokføre produksjonsforbruk</span><span class="sxs-lookup"><span data-stu-id="95b80-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="95b80-104">Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.</span><span class="sxs-lookup"><span data-stu-id="95b80-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="95b80-105">Hvis du satte en hake i feltet **Plukk nødv.** på lokasjonskortet for å vise at lokasjonen krever legerplukkbehandling, trenger du ikke å bruke denne kjørselen.</span><span class="sxs-lookup"><span data-stu-id="95b80-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="95b80-106">skal håndtere forbruk når du bokfører lagerplukkingen.</span><span class="sxs-lookup"><span data-stu-id="95b80-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="95b80-107">Hvis du vil ha mer informasjon, kan du se [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span><span class="sxs-lookup"><span data-stu-id="95b80-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="95b80-108">Du kan også konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk å bokføre (*lagertrekke*) komponenter når du starter eller ferdigstiller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="95b80-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="95b80-109">Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="95b80-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="95b80-110">Slik bokfører du forbruk for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="95b80-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="95b80-111">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forbrukskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="95b80-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95b80-112">Fyll ut feltene med produksjonsordre- og forbruksinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="95b80-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="95b80-113">Bruk handlingen **Beregn forbruk** til å generere journallinjer fra produksjonsordrer basert på den faktiske avgangen (antall ferdigvarer du har rapportert) eller den forventede avgangen (antall ferdigvarer du forventer å produsere).</span><span class="sxs-lookup"><span data-stu-id="95b80-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="95b80-114">Hvis du konfigurerte lokasjonskortet til å kreve lagerplukkbehandling, kan du bare angi antall varer som allerede er plukket via en lageraktivitet, i feltet **Antall** på siden **Forbrukskladd**, og ikke beregnet antall.</span><span class="sxs-lookup"><span data-stu-id="95b80-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="95b80-115">Hvis du vil ha mer informasjon, kan du se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="95b80-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="95b80-116">Velg handlingen **Bokfør** for å bokføre forbruket.</span><span class="sxs-lookup"><span data-stu-id="95b80-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="95b80-117">De relaterte beholdningene reduseres.</span><span class="sxs-lookup"><span data-stu-id="95b80-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="95b80-118">Se også</span><span class="sxs-lookup"><span data-stu-id="95b80-118">See Also</span></span>

<span data-ttu-id="95b80-119">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="95b80-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="95b80-120">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="95b80-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="95b80-121">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="95b80-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="95b80-122">Lager</span><span class="sxs-lookup"><span data-stu-id="95b80-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="95b80-123">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="95b80-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="95b80-124">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95b80-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
