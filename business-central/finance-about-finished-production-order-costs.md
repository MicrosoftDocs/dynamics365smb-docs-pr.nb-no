---
title: Om fullførte produksjonsordrekostnader | Microsoft-dokumentasjon
description: Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen Juster kostverdi - vareposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e1116d99a2893c3fef8fd2306b79cb2252c04d77
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389427"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="e5464-104">Om fullførte produksjonsordrekostnader</span><span class="sxs-lookup"><span data-stu-id="e5464-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="e5464-105">Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres.</span><span class="sxs-lookup"><span data-stu-id="e5464-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="e5464-106">De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**, som tillater økonomisk avstemming av kostbeløpene for vareproduksjon.</span><span class="sxs-lookup"><span data-stu-id="e5464-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="e5464-107">For at en produksjonsordre skal kunne behandles ved kostjustering, må statusen være **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="e5464-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="e5464-108">Derfor er det avgjørende at statusen til en produksjonsordre endres til **Ferdig** når ordren er fullført.</span><span class="sxs-lookup"><span data-stu-id="e5464-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="e5464-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e5464-109">Example</span></span>  
 <span data-ttu-id="e5464-110">Når du i et standardkostmiljø forbruker materiale for å produsere en vare, inngår varekostnaden pluss arbeid og indirekte kostnader i VIA.</span><span class="sxs-lookup"><span data-stu-id="e5464-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="e5464-111">Når varen er produsert, reduseres VIA med standardkostbeløpet for varen.</span><span class="sxs-lookup"><span data-stu-id="e5464-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="e5464-112">Disse kostbeløpene nettoføres vanligvis ikke til null.</span><span class="sxs-lookup"><span data-stu-id="e5464-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="e5464-113">For at disse kostnadene skal kunne nettoføres til null må du utføre kjørselen **Juster kostverdi - vareposter** og legge merke til at bare produksjonsordrer med status **Ferdig** vil tas med i beregningen ved justering.</span><span class="sxs-lookup"><span data-stu-id="e5464-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5464-114">Se også</span><span class="sxs-lookup"><span data-stu-id="e5464-114">See Also</span></span>  
[<span data-ttu-id="e5464-115">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="e5464-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="e5464-116">Produksjon</span><span class="sxs-lookup"><span data-stu-id="e5464-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="e5464-117">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5464-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]