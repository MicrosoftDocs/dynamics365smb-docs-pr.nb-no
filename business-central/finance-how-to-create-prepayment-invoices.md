---
title: Opprette forskuddsfakturaer | Microsoft-dokumentasjon
description: Lær hvordan du vil håndtere situasjoner der du eller leverandøren krever forskuddsbetaling.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f227cc73531111ae15f69d6fba5ac541e28560c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746869"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="254ee-103">Opprette forskuddsfakturaer</span><span class="sxs-lookup"><span data-stu-id="254ee-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="254ee-104">Hvis du krever at kundene skal betale før du leverer en ordre til dem, kan du bruke funksjonen for forskudd.</span><span class="sxs-lookup"><span data-stu-id="254ee-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="254ee-105">Det samme gjelder hvis leverandøren krever at du sender betaling før de leverer en ordre til deg.</span><span class="sxs-lookup"><span data-stu-id="254ee-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="254ee-106">Du kan starte betalingsprosessen når du oppretter en ordre eller bestilling.</span><span class="sxs-lookup"><span data-stu-id="254ee-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="254ee-107">Hvis du har en standard forskuddsprosent for denne kunden eller leverandøren, vil det automatisk bli inkludert i den resulterende forskuddsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="254ee-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="254ee-108">Du kan også angi en forskuddsprosent for hele dokumentet.</span><span class="sxs-lookup"><span data-stu-id="254ee-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="254ee-109">Når du har opprettet en ordre eller bestilling, kan du opprette en forskuddsfaktura.</span><span class="sxs-lookup"><span data-stu-id="254ee-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="254ee-110">Du kan bruke standardprosentene for hver salgslinje eller bestillingslinje, eller du kan justere beløpet etter behov.</span><span class="sxs-lookup"><span data-stu-id="254ee-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="254ee-111">Du kan for eksempel angi et totalbeløp for hele ordren.</span><span class="sxs-lookup"><span data-stu-id="254ee-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="254ee-112">Fremgangsmåten nedenfor beskriver hvordan du fakturerer et forskudd for en ordre.</span><span class="sxs-lookup"><span data-stu-id="254ee-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="254ee-113">Trinnene er de samme for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="254ee-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="254ee-114">Slik oppretter du en forskuddsfaktura:</span><span class="sxs-lookup"><span data-stu-id="254ee-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="254ee-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="254ee-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="254ee-116">Opprett en ny ordre for den aktuelle kunden.</span><span class="sxs-lookup"><span data-stu-id="254ee-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="254ee-117">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="254ee-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="254ee-118">I hurtigfanen **Forskudd** angir feltet **Forskuddsprosent** prosenten som skal brukes til å beregne forskuddsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="254ee-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="254ee-119">Hvis det er angitt en standard forskuddsprosent på kundekortet, fylles feltet ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="254ee-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="254ee-120">Du kan endre prosenten.</span><span class="sxs-lookup"><span data-stu-id="254ee-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="254ee-121">Velg feltet **Komprimer forskudd** hvis du vil opprette linjer på forskuddsfakturaen som kombinerer linjer fra ordren, hvis:</span><span class="sxs-lookup"><span data-stu-id="254ee-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="254ee-122">De har samme finanskonto for forskudd, som definert i det generelle bokføringsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="254ee-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="254ee-123">De har samme dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="254ee-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="254ee-124">Hvis du vil definere en forskuddsfaktura med én linje for hver ordrelinje som har en forskuddsprosent, velger du ikke feltet **Komprimer forskudd**.</span><span class="sxs-lookup"><span data-stu-id="254ee-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="254ee-125">Forskuddsdatoen for forskuddet beregnes automatisk basert på verdien i feltet **Kode for betalingsbetingelser for forskudd**.</span><span class="sxs-lookup"><span data-stu-id="254ee-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="254ee-126">Fyll ut salgslinjene.</span><span class="sxs-lookup"><span data-stu-id="254ee-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="254ee-127">Hvis du har angitt en standard forskuddsprosent for kunden eller i hurtigfanen **Forskudd** for dette dokumentet, blir denne verdien kopiert til hver linje.</span><span class="sxs-lookup"><span data-stu-id="254ee-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="254ee-128">Du kan endre verdien i **Forskuddsprosent**-feltet på linjen.</span><span class="sxs-lookup"><span data-stu-id="254ee-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="254ee-129">Du kan vise det totale forskuddsbeløpet ved å velge **Statistikk**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="254ee-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="254ee-130">Hvis du vil justere det totale forskuddsbeløpet for ordren, kan du endre verdien i **Forskuddsbeløp**-feltet på **Ordrestatistikk**-siden.</span><span class="sxs-lookup"><span data-stu-id="254ee-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="254ee-131">Hvis feltet **Priser inkl. mva.** er valgt, kan du redigere feltet **Forskuddsbeløp inkl. mva**.</span><span class="sxs-lookup"><span data-stu-id="254ee-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="254ee-132">Hvis du endrer verdien i **Forskuddsbeløp**-feltet, blir beløpet fordelt proporsjonalt mellom alle linjene, unntatt de som har **0** i **Forskuddsprosent**-feltet.</span><span class="sxs-lookup"><span data-stu-id="254ee-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="254ee-133">Hvis du vil skrive ut en testrapport før du bokfører forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Testrapport for forskudd**.</span><span class="sxs-lookup"><span data-stu-id="254ee-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="254ee-134">Hvis du vil bokføre forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Bokfør forskuddsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="254ee-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="254ee-135">Hvis du vil bokføre og skrive ut forskuddsfakturaen, velger du handlingen **Bokfør og skriv ut forskuddsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="254ee-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="254ee-136">Du kan utstede flere forskuddsfakturaer for ordren.</span><span class="sxs-lookup"><span data-stu-id="254ee-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="254ee-137">Dette gjør du ved å øke forskuddsbeløpet på én eller flere linjer, justere dokumentdatoen om nødvendig, og bokføre forskuddsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="254ee-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="254ee-138">Det opprettes en ny faktura for differansen mellom forskuddsbeløpene som er fakturert hittil, og det nye forskuddsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="254ee-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="254ee-139">Hvis du befinner deg i Nord-Amerika, kan du ikke endre forskuddsprosenten når den forskuddsbetalte fakturaen er bokført.</span><span class="sxs-lookup"><span data-stu-id="254ee-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="254ee-140">Dette er ikke tillatt i Nord-Amerika-versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] fordi beregningen av merverdiavgift ellers blir feil.</span><span class="sxs-lookup"><span data-stu-id="254ee-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="254ee-141">Når du er klar til å bokføre resten av fakturaen, bokfører du den som en hvilken som helst annen faktura, og forskuddsbeløpet blir automatisk trukket fra forfallsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="254ee-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="254ee-142">Se også</span><span class="sxs-lookup"><span data-stu-id="254ee-142">See Also</span></span>

[<span data-ttu-id="254ee-143">Fakturere forskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="254ee-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="254ee-144">Gjennomgang: konfigurere og fakturere salgsforskudd</span><span class="sxs-lookup"><span data-stu-id="254ee-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="254ee-145">Finans</span><span class="sxs-lookup"><span data-stu-id="254ee-145">Finance</span></span>](finance.md)  
<span data-ttu-id="254ee-146">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="254ee-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
