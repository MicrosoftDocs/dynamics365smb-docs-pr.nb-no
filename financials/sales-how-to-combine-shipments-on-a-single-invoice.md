---
title: "Kombinere leveringer på én faktura | Microsoft-dokumentasjon"
description: "Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="75adf-103">Kombinere leveringer på én faktura</span><span class="sxs-lookup"><span data-stu-id="75adf-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="75adf-104">Hvis du vil fakturere mer enn én følgeseddel av gangen, kan du bruke funksjonen for samling av følgesedler.</span><span class="sxs-lookup"><span data-stu-id="75adf-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="75adf-105">Før du kan opprette samlefakturaer, må du bokføre mer enn én følgeseddel for den samme kunden i én og samme valuta.</span><span class="sxs-lookup"><span data-stu-id="75adf-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="75adf-106">Du må med andre ord ha fylt ut minst to ordrer og bokført disse ordrene som levert, men ikke fakturert.</span><span class="sxs-lookup"><span data-stu-id="75adf-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="75adf-107">Du kombinerer forsendelser ved å merke av for **Opprett samlefaktura** på hurtigfanen **Levering** på **kundekortet**.</span><span class="sxs-lookup"><span data-stu-id="75adf-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="75adf-108">Kombinere leveringer på én faktura manuelt</span><span class="sxs-lookup"><span data-stu-id="75adf-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="75adf-109">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="75adf-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="75adf-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="75adf-110">Choose the **New** action.</span></span> <span data-ttu-id="75adf-111">Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="75adf-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="75adf-112">I feltet **Salg til-kundenr.**</span><span class="sxs-lookup"><span data-stu-id="75adf-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="75adf-113">angir du kunden som skal motta fakturaen for de leverte varene.</span><span class="sxs-lookup"><span data-stu-id="75adf-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="75adf-114">På hurtigfanen **Linjer** velger du handlingen **Hent leveringslinjer**.</span><span class="sxs-lookup"><span data-stu-id="75adf-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="75adf-115">Velg følgeseddellinjen du vil inkludere i fakturaen:</span><span class="sxs-lookup"><span data-stu-id="75adf-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="75adf-116">Du setter inn alle linjene ved å merke dem og velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="75adf-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="75adf-117">Du setter inn bestemte linjer ved å merke dem og velge **OK**.</span><span class="sxs-lookup"><span data-stu-id="75adf-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="75adf-118">Du kan bruke CTRL-tasten for å velge flere linjer som ikke ligger inntil hverandre.</span><span class="sxs-lookup"><span data-stu-id="75adf-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="75adf-119">Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på fakturaen og kjøre funksjonen **Hent følgeseddellinjer** på nytt.</span><span class="sxs-lookup"><span data-stu-id="75adf-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="75adf-120">Velg handlingen **Bokfør** for å bokføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="75adf-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="75adf-121">Slik kombinerer du leveringer på én enkelt faktura automatisk:</span><span class="sxs-lookup"><span data-stu-id="75adf-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="75adf-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Opprett samlefaktura**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="75adf-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="75adf-123">Vinduet for kjørselforespørsel åpnes.</span><span class="sxs-lookup"><span data-stu-id="75adf-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="75adf-124">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="75adf-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="75adf-125">Merk av for **Bokfør fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="75adf-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="75adf-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="75adf-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="75adf-127">Du må bokføre fakturaene manuelt hvis det ikke var merket av for alternativet **Bokfør fakturaer** for kjørselen.</span><span class="sxs-lookup"><span data-stu-id="75adf-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="75adf-128">Fjerne åpne ordrer etter kombinert leveringsbokføring</span><span class="sxs-lookup"><span data-stu-id="75adf-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="75adf-129">Når du oppretter og bokfører en samlefaktura, opprettes en bokført salgsfaktura for fakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="75adf-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="75adf-130">**Fakturert (antall)**-feltet på den opprinnelige rammeordren eller ordren oppdateres ut fra det fakturerte antallet.</span><span class="sxs-lookup"><span data-stu-id="75adf-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="75adf-131">Når du fakturerer følgesedler på denne måten, eksisterer fortsatt ordrene som følgesedlene ble bokført fra, selv om de er fullstendig levert og fakturert.</span><span class="sxs-lookup"><span data-stu-id="75adf-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="75adf-132">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Slett fakturerte ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="75adf-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="75adf-133">Angi hvilke ordrer som skal slettes, i **Nr.**</span><span class="sxs-lookup"><span data-stu-id="75adf-133">Specify in the **No.**</span></span> <span data-ttu-id="75adf-134">-filterfeltet.</span><span class="sxs-lookup"><span data-stu-id="75adf-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="75adf-135">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="75adf-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="75adf-136">Du kan også slette individuelle ordrer manuelt.</span><span class="sxs-lookup"><span data-stu-id="75adf-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="75adf-137">Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel ordrer.</span><span class="sxs-lookup"><span data-stu-id="75adf-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="75adf-138">Se også</span><span class="sxs-lookup"><span data-stu-id="75adf-138">See Also</span></span>  
[<span data-ttu-id="75adf-139">Salg</span><span class="sxs-lookup"><span data-stu-id="75adf-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="75adf-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75adf-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

