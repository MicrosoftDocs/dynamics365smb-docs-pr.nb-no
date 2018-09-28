---
title: "Om fullførte produksjonsordrekostnader | Microsoft-dokumentasjon"
description: "Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f906be41274fa8c6f7be4a3db87cc0bc4ba7cdd0
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="9c44c-104">Om fullførte produksjonsordrekostnader</span><span class="sxs-lookup"><span data-stu-id="9c44c-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="9c44c-105">Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres.</span><span class="sxs-lookup"><span data-stu-id="9c44c-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="9c44c-106">De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**, som tillater økonomisk avstemming av kostbeløpene for vareproduksjon.</span><span class="sxs-lookup"><span data-stu-id="9c44c-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="9c44c-107">For at en produksjonsordre skal kunne behandles ved kostjustering, må statusen være **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="9c44c-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="9c44c-108">Derfor er det avgjørende at statusen til en produksjonsordre endres til **Ferdig** når ordren er fullført.</span><span class="sxs-lookup"><span data-stu-id="9c44c-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="9c44c-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9c44c-109">Example</span></span>  
 <span data-ttu-id="9c44c-110">Når du i et standardkostmiljø forbruker materiale for å produsere en vare, inngår varekostnaden pluss arbeid og indirekte kostnader i VIA.</span><span class="sxs-lookup"><span data-stu-id="9c44c-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="9c44c-111">Når varen er produsert, reduseres VIA med standardkostbeløpet for varen.</span><span class="sxs-lookup"><span data-stu-id="9c44c-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="9c44c-112">Disse kostbeløpene nettoføres vanligvis ikke til null.</span><span class="sxs-lookup"><span data-stu-id="9c44c-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="9c44c-113">For at disse kostnadene skal kunne nettoføres til null må du utføre kjørselen **Juster kostverdi - vareposter** og legge merke til at bare produksjonsordrer med status **Ferdig** vil tas med i beregningen ved justering.</span><span class="sxs-lookup"><span data-stu-id="9c44c-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9c44c-114">Se også</span><span class="sxs-lookup"><span data-stu-id="9c44c-114">See Also</span></span>  
[<span data-ttu-id="9c44c-115">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="9c44c-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="9c44c-116">Produksjon</span><span class="sxs-lookup"><span data-stu-id="9c44c-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="9c44c-117">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9c44c-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

