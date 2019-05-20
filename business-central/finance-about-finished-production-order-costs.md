---
title: Om fullførte produksjonsordrekostnader | Microsoft-dokumentasjon
description: Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen Juster kostverdi - vareposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96cf025bbac137f61f41a65cbd2f9520f2c5e787
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242793"
---
# <a name="about-finished-production-order-costs"></a><span data-ttu-id="71bbd-104">Om fullførte produksjonsordrekostnader</span><span class="sxs-lookup"><span data-stu-id="71bbd-104">About Finished Production Order Costs</span></span>
<span data-ttu-id="71bbd-105">Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres.</span><span class="sxs-lookup"><span data-stu-id="71bbd-105">Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced.</span></span> <span data-ttu-id="71bbd-106">De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**, som tillater økonomisk avstemming av kostbeløpene for vareproduksjon.</span><span class="sxs-lookup"><span data-stu-id="71bbd-106">Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the **Adjust Cost - Item Entries** batch job, which allows for financial reconciliation of the costs of item production.</span></span> <span data-ttu-id="71bbd-107">For at en produksjonsordre skal kunne behandles ved kostjustering, må statusen være **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="71bbd-107">For a production order to be considered for cost adjustment, the status must be **Finished**.</span></span> <span data-ttu-id="71bbd-108">Derfor er det avgjørende at statusen til en produksjonsordre endres til **Ferdig** når ordren er fullført.</span><span class="sxs-lookup"><span data-stu-id="71bbd-108">It is therefore critical that upon completion, the status of a production order is changed to **Finished**.</span></span>  

## <a name="example"></a><span data-ttu-id="71bbd-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="71bbd-109">Example</span></span>  
 <span data-ttu-id="71bbd-110">Når du i et standardkostmiljø forbruker materiale for å produsere en vare, inngår varekostnaden pluss arbeid og indirekte kostnader i VIA.</span><span class="sxs-lookup"><span data-stu-id="71bbd-110">In a standard cost environment, when you consume material to produce an item, stated simply, the cost of the item plus labor and overhead go into WIP.</span></span> <span data-ttu-id="71bbd-111">Når varen er produsert, reduseres VIA med standardkostbeløpet for varen.</span><span class="sxs-lookup"><span data-stu-id="71bbd-111">When the item is produced, WIP is reduced by the amount of the standard cost of the item.</span></span> <span data-ttu-id="71bbd-112">Disse kostbeløpene nettoføres vanligvis ikke til null.</span><span class="sxs-lookup"><span data-stu-id="71bbd-112">Typically, these costs do not net to zero.</span></span> <span data-ttu-id="71bbd-113">For at disse kostnadene skal kunne nettoføres til null må du utføre kjørselen **Juster kostverdi - vareposter** og legge merke til at bare produksjonsordrer med status **Ferdig** vil tas med i beregningen ved justering.</span><span class="sxs-lookup"><span data-stu-id="71bbd-113">So that these costs can net to zero, you must run the **Adjust Cost - Item Entries** batch job, noting that only production orders with the status of **Finished** will be considered for adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="71bbd-114">Se også</span><span class="sxs-lookup"><span data-stu-id="71bbd-114">See Also</span></span>  
[<span data-ttu-id="71bbd-115">Administrere lagerkostnader</span><span class="sxs-lookup"><span data-stu-id="71bbd-115">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="71bbd-116">Produksjon</span><span class="sxs-lookup"><span data-stu-id="71bbd-116">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="71bbd-117">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71bbd-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
