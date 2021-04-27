---
title: Massebokføre produksjonsavgang og operasjonstider
description: Avgangsantallet representerer arbeidsfremdriften i form av ferdig antall og brukt kapasitet for arbeidssenter eller produksjonsressurs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787880"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="73a02-103">Bokføre avgang og operasjonstid</span><span class="sxs-lookup"><span data-stu-id="73a02-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="73a02-104">Avgangsantallet representerer arbeidsfremdriften i form av ferdig antall og brukt kapasitet for arbeidssenter eller produksjonsressurs.</span><span class="sxs-lookup"><span data-stu-id="73a02-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="73a02-105">Du kan bruke ferdigmeldingskladden til å:</span><span class="sxs-lookup"><span data-stu-id="73a02-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="73a02-106">Justere lagerbeholdningen i forbindelse med avgang av ferdige varer fra produksjonen.</span><span class="sxs-lookup"><span data-stu-id="73a02-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="73a02-107">Registrere antall og vrak for hver operasjon i produksjonsrutingen.</span><span class="sxs-lookup"><span data-stu-id="73a02-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="73a02-108">Registrere oppsett og kjøretid for arbeidssentre og produksjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="73a02-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="73a02-109">Hvis produksjonsruting brukes, oppdateres lageret bare når du bokfører avgangsantall i den siste operasjonen.</span><span class="sxs-lookup"><span data-stu-id="73a02-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="73a02-110">I vinduet **Produksjonskladd** kan du utføre de samme oppgavene som i vinduet **Ferdigmeldingskladd**, og du kan utføre de relaterte forbruksbokføringsoppgavene samtidig.</span><span class="sxs-lookup"><span data-stu-id="73a02-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="73a02-111">Hvis du vil ha mer informasjon, kan du se [Registrere forbruk og avgang for én frigitt produksjonsordrelinje](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="73a02-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="73a02-112">Slik bokfører du avgangsantall og/eller registrerer kjøretider for en eller flere produksjonsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="73a02-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="73a02-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="73a02-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="73a02-114">Fyll ut feltene med produksjonsordre- og avgangsdata og/eller kjøretid.</span><span class="sxs-lookup"><span data-stu-id="73a02-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="73a02-115">Du kan bruke funksjonen **Utfold rute** til å generere kladdelinjer fra produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="73a02-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="73a02-116">Hvis operasjonen er fullført, velger du **Ferdig**-feltet.</span><span class="sxs-lookup"><span data-stu-id="73a02-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="73a02-117">Velg handlingen **Bokfør** for å bokføre operasjonene.</span><span class="sxs-lookup"><span data-stu-id="73a02-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="73a02-118">Kapasitetsposter oppdateres for det brukte arbeidssenteret eller produksjonsressursene med informasjon om tid og antall av avgang og vrak.</span><span class="sxs-lookup"><span data-stu-id="73a02-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="73a02-119">Hvis du bokførte den siste operasjonen, blir varen lagt til i lageret.</span><span class="sxs-lookup"><span data-stu-id="73a02-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="73a02-120">Se også</span><span class="sxs-lookup"><span data-stu-id="73a02-120">See Also</span></span>  
<span data-ttu-id="73a02-121">[Bokføre vrak manuelt](production-how-to-post-scrap.md)
[Tilbakeføre utgående bokføring](production-how-to-reverse-output-posting.md)
[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="73a02-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="73a02-122">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="73a02-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="73a02-123">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="73a02-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="73a02-124">Lager</span><span class="sxs-lookup"><span data-stu-id="73a02-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="73a02-125">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="73a02-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
