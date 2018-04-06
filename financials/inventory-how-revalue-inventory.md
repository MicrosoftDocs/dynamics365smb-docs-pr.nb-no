---
title: "Opprette nye verdiposter for varer på lageret | Microsoft-dokumentasjon"
description: "Beskriver hvordan du foretar oppskrivning eller avskrivning av verdiposter for én eller flere varer på lageret, ved å bokføre den gjeldende, beregnede verdien."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8460dac8478fa101a255d93110578fa9ea20516f
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-inventory"></a><span data-ttu-id="d7960-103">Revaluere beholdning</span><span class="sxs-lookup"><span data-stu-id="d7960-103">Revalue Inventory</span></span>
<span data-ttu-id="d7960-104">Hvis du vil endre lagerverdien for en vare eller en bestemt varepost, må du bruke revalueringskladden.</span><span class="sxs-lookup"><span data-stu-id="d7960-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="d7960-105">Slik revaluerer du beholdning</span><span class="sxs-lookup"><span data-stu-id="d7960-105">To revalue inventory</span></span>
1. <span data-ttu-id="d7960-106">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Revalueringskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d7960-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d7960-107">Velg handlingen **Beregn lagerverdi**.</span><span class="sxs-lookup"><span data-stu-id="d7960-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="d7960-108">I vinduet **Beregn lagerverdi** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d7960-108">In the **Calculate Inventory Value** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d7960-109">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7960-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="d7960-110">På hver linje i vinduet **Revalueringskladd** i feltet **Enhetskost (revaluert)** angir du den nye enhetskosten.</span><span class="sxs-lookup"><span data-stu-id="d7960-110">On each line in the **Revaluation Journal** window, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="d7960-111">Du kan eventuelt angi det nye totalbeløpet i feltet **Lagerverdi (revaluert)**.</span><span class="sxs-lookup"><span data-stu-id="d7960-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="d7960-112">De relevante feltene oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="d7960-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="d7960-113">Merk deg at feltet **Beløp** viser den faktiske endringen i lagerverdien for den vareposten du har valgt.</span><span class="sxs-lookup"><span data-stu-id="d7960-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="d7960-114">I dette feltet beregnes differansen mellom feltene **Lagerverdi (beregnet)** og **Lagerverdi (revaluert)**.</span><span class="sxs-lookup"><span data-stu-id="d7960-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="d7960-115">Når du har fullført alle linjene i revalueringskladden, kan du velge handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="d7960-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="d7960-116">Nye verdiposter opprettes nå for å gjenspeile revalueringer som du har bokført.</span><span class="sxs-lookup"><span data-stu-id="d7960-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="d7960-117">Du kan se de nye verdiene på de respektive varekortene.</span><span class="sxs-lookup"><span data-stu-id="d7960-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7960-118">Se også</span><span class="sxs-lookup"><span data-stu-id="d7960-118">See Also</span></span>
[<span data-ttu-id="d7960-119">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="d7960-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="d7960-120">Lager</span><span class="sxs-lookup"><span data-stu-id="d7960-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d7960-121">Salg</span><span class="sxs-lookup"><span data-stu-id="d7960-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d7960-122">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d7960-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d7960-123">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7960-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

