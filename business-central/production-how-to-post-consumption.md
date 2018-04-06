---
title: "Massebokføre forbruk | Microsoft-dokumentasjon"
description: "Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4058d16ee3bdfc10933e1f3a01c84fbc5d0b0ebb
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="2ee1d-103">Massebokføre produksjonsforbruk</span><span class="sxs-lookup"><span data-stu-id="2ee1d-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="2ee1d-104">Hvis trekkmetoden er **Manuell**, må du bokføre komponentene manuelt ved hjelp av forbrukskladdene.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="2ee1d-105">Du kan også definere at systemet automatisk skal bokføre (*utføre lagertrekk*) komponenter når du starter eller ferdigstiller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="2ee1d-106">Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="2ee1d-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="2ee1d-107">Slik bokfører du forbruk for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="2ee1d-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="2ee1d-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Forbrukskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ee1d-109">Fyll ut feltene med produksjonsordre- og forbruksinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="2ee1d-110">Hvis lagerlokasjonen der komponentene er lagret er definert for å bruke hyller, men ikke krever plukkbehandling, tildeler du en hyllekode til kladdelinjen for å vise hvor varene skal tas fra på lageret.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="2ee1d-111">Hvis du vil ha mer informasjon, kan du se [Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="2ee1d-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="2ee1d-112">Velg handlingen **Bokfør** for å bokføre forbruket.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="2ee1d-113">De relaterte varepostene reduseres.</span><span class="sxs-lookup"><span data-stu-id="2ee1d-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ee1d-114">Se også</span><span class="sxs-lookup"><span data-stu-id="2ee1d-114">See Also</span></span>  
<span data-ttu-id="2ee1d-115">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="2ee1d-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="2ee1d-116">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="2ee1d-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="2ee1d-117">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="2ee1d-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="2ee1d-118">Lager</span><span class="sxs-lookup"><span data-stu-id="2ee1d-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2ee1d-119">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="2ee1d-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="2ee1d-120">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ee1d-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

