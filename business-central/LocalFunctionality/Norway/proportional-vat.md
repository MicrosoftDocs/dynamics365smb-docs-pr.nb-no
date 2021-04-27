---
title: Forholdsmessig MVA
description: Forbedringer i den norske versjonen gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 53a3d8e196df9ede7413eeb0d85e8518f942b470
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775234"
---
# <a name="proportional-vat"></a><span data-ttu-id="b6789-103">Forholdsmessig MVA</span><span class="sxs-lookup"><span data-stu-id="b6789-103">Proportional VAT</span></span>
[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="b6789-104">gjør det mulig for deg å beregne MVA når både fradragsberettiget og ikke-fradragsberettiget MVA forekommer.</span><span class="sxs-lookup"><span data-stu-id="b6789-104">allows you to calculate VAT when there is both deductible and non-deductible VAT.</span></span> <span data-ttu-id="b6789-105">Siden det er vanskelig å vite hvor og hvordan varen blir brukt, må du ta kontakt med norske skattemyndigheter for å finne ut om en angitt prosentandel MVA kan gå til fradrag basert på historiske data.</span><span class="sxs-lookup"><span data-stu-id="b6789-105">Because it is difficult to know where and how an item is used, you will have to contact the Norwegian tax authorities to determine whether a specified percentage of the VAT is deductible based on historical data.</span></span>  

## <a name="example"></a><span data-ttu-id="b6789-106">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b6789-106">Example</span></span>  
<span data-ttu-id="b6789-107">Et busselskap eier både busser og lastebiler.</span><span class="sxs-lookup"><span data-stu-id="b6789-107">A bus company owns both buses and trucks.</span></span> <span data-ttu-id="b6789-108">Når det kjøpes inn bensin, blir denne lagret i én oppbevaringstank.</span><span class="sxs-lookup"><span data-stu-id="b6789-108">When gasoline is purchased, the gasoline is stored in one holding tank.</span></span> <span data-ttu-id="b6789-109">Når bensinen brukes i en buss som transporterer barn, er den ikke fradragsberettiget.</span><span class="sxs-lookup"><span data-stu-id="b6789-109">When the gasoline is used in a bus for transporting children, it is not deductible.</span></span> <span data-ttu-id="b6789-110">Når bensinen brukes i en lastebil, kan den være fradragsberettiget.</span><span class="sxs-lookup"><span data-stu-id="b6789-110">When the gasoline is used in a truck, the gasoline may be deductible.</span></span> <span data-ttu-id="b6789-111">Avtalen mellom selskapet og de norske skattemyndighetene kan for eksempel da være at 60 % av mva. går til fradrag.</span><span class="sxs-lookup"><span data-stu-id="b6789-111">The agreement between the bus company and the Norwegian tax authorities might be that 60 percent of the VAT is deductible.</span></span>  

<span data-ttu-id="b6789-112">Hvis du har en kjøpsfaktura på USD 12 500,00 basert på 25 prosent mva., og **Ja** er angitt i **Beregn forholdsmessig fradrag** på siden **Mva-bokføringsoppsett** og feltet **Forholdsmessig fradrags-%** er satt til **60 prosent**, går bare 60 prosent av mva. til fradrag i en kladd.</span><span class="sxs-lookup"><span data-stu-id="b6789-112">If you have a purchase invoice of $12,500 based on 25 percent VAT with the **Calc. Prop. Deduction VAT** field on the **VAT Posting Setup** page set to **Yes** and the **Proportional Deduction VAT %** field set to **60 percent**, only 60 percent of the VAT is deductible in a journal.</span></span> <span data-ttu-id="b6789-113">Når fakturaen er bokført, er posteringene som følger:</span><span class="sxs-lookup"><span data-stu-id="b6789-113">When the invoice is posted, the postings are as follows:</span></span>  

- <span data-ttu-id="b6789-114">Til leverandøren finanskonto - USD 12 500 (kredit)</span><span class="sxs-lookup"><span data-stu-id="b6789-114">To vendor general ledger account - $12,500 (credit)</span></span>  
- <span data-ttu-id="b6789-115">Til kostkonto 4010 - USD 11 000,00 (debet)</span><span class="sxs-lookup"><span data-stu-id="b6789-115">To cost account 4010 - $11,000 (debit)</span></span>  
- <span data-ttu-id="b6789-116">Til mva-konto 2720 - USD 1 500,00 (debet)</span><span class="sxs-lookup"><span data-stu-id="b6789-116">To VAT account 2720 - $1,500 (debit)</span></span>  

<span data-ttu-id="b6789-117">Vanligvis ville mva-beløpet bli USD 2 500, basert på 25 prosent mv.</span><span class="sxs-lookup"><span data-stu-id="b6789-117">Generally, based on 25 percent VAT, the VAT amount would be $2,500.</span></span> <span data-ttu-id="b6789-118">Imidlertid går bare 60 prosent til fradrag; mva-beløpet er derfor USD 2 500 x 60 % = USD 1 500.</span><span class="sxs-lookup"><span data-stu-id="b6789-118">However, only 60 percent is deductible; therefore the VAT amount is $2,500 x 60% = $1,500.</span></span> <span data-ttu-id="b6789-119">Beløpet på USD 1 000 som ikke er fradragsberettiget, legges til på kostkontoen.</span><span class="sxs-lookup"><span data-stu-id="b6789-119">The non-deductible amount of $1,000 is added to the cost account.</span></span> <span data-ttu-id="b6789-120">Mva-grunnlaget har tilsvarende verdier.</span><span class="sxs-lookup"><span data-stu-id="b6789-120">The VAT base has corresponding values.</span></span> <span data-ttu-id="b6789-121">Dette beløpet skulle ha vært USD 10 000,00, men siden bare 60 prosent går til fradrag, er grunnlaget USD 6000,00.</span><span class="sxs-lookup"><span data-stu-id="b6789-121">This amount should have been $10,000, but because only 60 percent is deductible, the base is $6,000.</span></span>  

<span data-ttu-id="b6789-122">Dette vil også fungere hvis transaksjonen med denne mva-kombinasjonen bokføres via en bestilling.</span><span class="sxs-lookup"><span data-stu-id="b6789-122">This also works if the transaction with this VAT combination is posted through a purchase order.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b6789-123">Hvis denne funksjonen brukes i en bestilling som brukes til innkjøp av varer til lager, har ikke funksjonen noen innvirkning på varekostnaden.</span><span class="sxs-lookup"><span data-stu-id="b6789-123">If this functionality is used on a purchase order that is used for buying items for inventory, the functionality will not influence the cost of the item.</span></span> <span data-ttu-id="b6789-124">Varekostnaden legges til gjennom ikke-fradragsberettiget mva.</span><span class="sxs-lookup"><span data-stu-id="b6789-124">The cost of the item will be added by using the non-deductible VAT.</span></span> <span data-ttu-id="b6789-125">Dette er bare tilfelle i forbindelse med finans.</span><span class="sxs-lookup"><span data-stu-id="b6789-125">This works on the general ledger level only.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6789-126">Se også</span><span class="sxs-lookup"><span data-stu-id="b6789-126">See Also</span></span>  
 <span data-ttu-id="b6789-127">[Beregne forholdsmessig MVA](how-to-calculate-proportional-vat.md) </span><span class="sxs-lookup"><span data-stu-id="b6789-127">[Calculate Proportional VAT](how-to-calculate-proportional-vat.md) </span></span>  
 [<span data-ttu-id="b6789-128">Norsk mva-rapportering</span><span class="sxs-lookup"><span data-stu-id="b6789-128">Norwegian VAT Reporting</span></span>](norwegian-vat-reporting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]