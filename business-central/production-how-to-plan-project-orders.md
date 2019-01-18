---
title: Planlegge prosjektordrer | Microsoft-dokumentasjon
description: "Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-siden. Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-siden."
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4cb63a7dc26e13c7947ba2ae071c3dff87c53e9d
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="plan-project-orders"></a><span data-ttu-id="f52a6-104">Planlegge prosjektordrer</span><span class="sxs-lookup"><span data-stu-id="f52a6-104">Plan Project Orders</span></span>
<span data-ttu-id="f52a6-105">Denne planleggingsoppgaven starter fra en ordre og bruker **Ordreplanlegging**-siden.</span><span class="sxs-lookup"><span data-stu-id="f52a6-105">This planning task starts from a sales order and uses the **Sales Order Planning** page.</span></span> <span data-ttu-id="f52a6-106">Når du har opprettet en prosjektproduksjonsordre, kan du planlegge den videre ved hjelp av **Ordreplanlegging**-siden.</span><span class="sxs-lookup"><span data-stu-id="f52a6-106">Once you have created a project production order, you can plan it further by using the **Order Planning** page.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="f52a6-107">Slik oppretter du en prosjektproduksjonsordre</span><span class="sxs-lookup"><span data-stu-id="f52a6-107">To create a project production order</span></span>  

1.  <span data-ttu-id="f52a6-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f52a6-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f52a6-109">Velg ordren som representerer produksjonsprosjektet, og velg deretter **Planlegging**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="f52a6-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="f52a6-110">På **Ordreplanlegging**-siden velger du handlingen **Opprett prod.ordre**.</span><span class="sxs-lookup"><span data-stu-id="f52a6-110">On the **Sales Order Planning** page, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="f52a6-111">På siden **Opprett ordre fra salg** velger du **Prosjektordre** i **Ordretype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f52a6-111">On the **Create Order from Sales** page, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="f52a6-112">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f52a6-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="f52a6-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f52a6-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="f52a6-114">Åpne produksjonsordren som ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="f52a6-114">Open the production order just created.</span></span>  

    <span data-ttu-id="f52a6-115">Merk at **Kildetype**-feltet i produksjonsordren inneholder **Salgshode**, og ordren har flere linjer, en for hver salgslinjevare som må produseres.</span><span class="sxs-lookup"><span data-stu-id="f52a6-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="f52a6-116">Velg handlingen **Planlegging**.</span><span class="sxs-lookup"><span data-stu-id="f52a6-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="f52a6-117">På siden **Ordreplanlegging** velger du handlingen **Forny** for å beregne nytt behov.</span><span class="sxs-lookup"><span data-stu-id="f52a6-117">On the **Order Planning** page, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="f52a6-118">Ordrehodelinjen for prosjektordren vises med alle behovslinjer som ikke er oppfylt, utvidet under hodelinjen.</span><span class="sxs-lookup"><span data-stu-id="f52a6-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="f52a6-119">Selv om produksjonsordren inneholder linjer for flere produserte varer, er det totale behovet for alle produksjonsordrelinjer ført opp under én ordrehodelinje på **Ordreplanlegging**-siden, og det opprinnelige kundenavnet vises.</span><span class="sxs-lookup"><span data-stu-id="f52a6-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line on the **Order Planning** page, and the original customer name is displayed.</span></span> <span data-ttu-id="f52a6-120">Du kan deretter fortsette med å planlegge behovet som beskrevet i [Planlegge for nytt behov bestilling for bestilling](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="f52a6-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f52a6-121">Behovslinjer i prosjektproduksjonsordren som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="f52a6-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="f52a6-122">Når du har generert disse produksjonsordrene, må du på nytt beregne en plan på siden **Ordreplanlegging** for å identifisere eventuelle komponentbehov som ikke er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="f52a6-122">After you have generated these production orders, you must again calculate a plan on the **Order Planning** page to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="f52a6-123">I det tilfellet vises forsyningsordrene som behovslinjer under en vanlig produksjonsordrehodelinje. Dette betyr at prosjektforbindelsen ikke lenger vises på siden.</span><span class="sxs-lookup"><span data-stu-id="f52a6-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible on the page.</span></span> <span data-ttu-id="f52a6-124">Hvis du imidlertid bruker sporingsfunksjonen, kan du lete frem og tilbake i alle forsyningsordrer som er laget under den opprinnelige ordren.</span><span class="sxs-lookup"><span data-stu-id="f52a6-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f52a6-125">Se også</span><span class="sxs-lookup"><span data-stu-id="f52a6-125">See Also</span></span>
<span data-ttu-id="f52a6-126">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f52a6-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="f52a6-127">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="f52a6-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f52a6-128">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f52a6-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f52a6-129">Lager</span><span class="sxs-lookup"><span data-stu-id="f52a6-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f52a6-130">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="f52a6-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f52a6-131">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f52a6-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="f52a6-132">Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="f52a6-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="f52a6-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f52a6-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

