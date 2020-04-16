---
title: Opprette nye verdiposter for varer på lageret | Microsoft-dokumentasjon
description: Beskriver hvordan du foretar oppskrivning eller avskrivning av verdiposter for én eller flere varer på lageret, ved å bokføre den gjeldende, beregnede verdien.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c961d15d04da5fcad18a460adc269f3099962f6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182135"
---
# <a name="revalue-inventory"></a><span data-ttu-id="c2dc1-103">Revaluere beholdning</span><span class="sxs-lookup"><span data-stu-id="c2dc1-103">Revalue Inventory</span></span>
<span data-ttu-id="c2dc1-104">Hvis du vil endre lagerverdien for en vare eller en bestemt varepost, må du bruke revalueringskladden.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="c2dc1-105">Slik revaluerer du beholdning</span><span class="sxs-lookup"><span data-stu-id="c2dc1-105">To revalue inventory</span></span>
1. <span data-ttu-id="c2dc1-106">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Revalueringskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2dc1-107">Velg handlingen **Beregn lagerverdi**.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="c2dc1-108">På siden **Beregn lagerverdi** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="c2dc1-109">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="c2dc1-110">På hver linje på siden **Revalueringskladd** i feltet **Enhetskost (revaluert)** angir du den nye enhetskosten.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="c2dc1-111">Du kan eventuelt angi det nye totalbeløpet i feltet **Lagerverdi (revaluert)**.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="c2dc1-112">De relevante feltene oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="c2dc1-113">Merk deg at feltet **Beløp** viser den faktiske endringen i lagerverdien for den vareposten du har valgt.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="c2dc1-114">I dette feltet beregnes differansen mellom feltene **Lagerverdi (beregnet)** og **Lagerverdi (revaluert)**.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="c2dc1-115">Når du har fullført alle linjene i revalueringskladden, kan du velge handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="c2dc1-116">Nye verdiposter opprettes nå for å gjenspeile revalueringer som du har bokført.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="c2dc1-117">Du kan se de nye verdiene på de respektive varekortene.</span><span class="sxs-lookup"><span data-stu-id="c2dc1-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2dc1-118">Se også</span><span class="sxs-lookup"><span data-stu-id="c2dc1-118">See Also</span></span>
[<span data-ttu-id="c2dc1-119">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="c2dc1-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="c2dc1-120">Lager</span><span class="sxs-lookup"><span data-stu-id="c2dc1-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c2dc1-121">Salg</span><span class="sxs-lookup"><span data-stu-id="c2dc1-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="c2dc1-122">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="c2dc1-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="c2dc1-123">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2dc1-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
