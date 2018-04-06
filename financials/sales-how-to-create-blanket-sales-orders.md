---
title: Opprette rammeordrer | Microsoft-dokumentasjon
description: "Bruk rammeordrer når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 89db93227222d79e535f2d18400330aa30566f2f
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-blanket-sales-orders"></a><span data-ttu-id="cc47f-103">Arbeide med rammeordrer</span><span class="sxs-lookup"><span data-stu-id="cc47f-103">Work with Blanket Sales Orders</span></span>
<span data-ttu-id="cc47f-104">En rammeordre utgjør rammene for en langsiktig avtale mellom deg og kunden.</span><span class="sxs-lookup"><span data-stu-id="cc47f-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="cc47f-105">En rammeordre opprettes som regel når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="cc47f-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="cc47f-106">Rammeordrer dekker ofte bare én vare med forhåndsbestemte leveringsdatoer.</span><span class="sxs-lookup"><span data-stu-id="cc47f-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="cc47f-107">Hovedgrunnen til å bruke en rammeordre i stedet for en salgsordre er at antallene som angis på en rammeordre ikke påvirker tilgjengeligheten for varene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="cc47f-108">På rammeordren kan hver enkelt levering settes opp som en ordrelinje som deretter kan konverteres til en salgsordre på leveringstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="cc47f-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="cc47f-109">Et eksempel på et tilfelle hvor en rammeordre kan brukes er når en kunde ringer og bestiller 1000 enheter av en vare, og de vil at det skal leveres 250 enheter per uke over den neste måneden.</span><span class="sxs-lookup"><span data-stu-id="cc47f-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="cc47f-110">Rammebestillinger fungerer på lignende måte som rammeordrer.</span><span class="sxs-lookup"><span data-stu-id="cc47f-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="cc47f-111">Denne dokumentasjonen dekker ikke rammebestillinger.</span><span class="sxs-lookup"><span data-stu-id="cc47f-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="cc47f-112">Slik oppretter du en rammeordre</span><span class="sxs-lookup"><span data-stu-id="cc47f-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="cc47f-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="cc47f-114">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="cc47f-115">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="cc47f-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="cc47f-116">La **Ordredato**-feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc47f-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="cc47f-117">Når egne ordrer opprettes fra rammeordren, settes ordredatoen for salgsordren til faktisk arbeidsdato.</span><span class="sxs-lookup"><span data-stu-id="cc47f-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="cc47f-118">På hurtigfanen **Linjer** oppretter du egne linjer for hver levering.</span><span class="sxs-lookup"><span data-stu-id="cc47f-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="cc47f-119">Hvis kunden for eksempel vil ha 1&#160;000 enheter fordelt jevnt på fire uker, angir du fire linjer på 250 enheter hver.</span><span class="sxs-lookup"><span data-stu-id="cc47f-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="cc47f-120">Slik oppretter du en ordre fra en rammeordre</span><span class="sxs-lookup"><span data-stu-id="cc47f-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="cc47f-121">Hvis du vil opprette en ordre fra noen av linjene i rammemonteringsordren, fjerner du antallet i **Levere (antall)**-feltet på alle linjene som du IKKE vil levere på dette tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="cc47f-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="cc47f-122">Når du er klar til å opprette bestillinger, velger du handlingen **Lag ordre** og velger deretter **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="cc47f-123">Det vises en melding om at rammebestillingen er tilordnet et bestillingsnummer.</span><span class="sxs-lookup"><span data-stu-id="cc47f-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="cc47f-124">Vær oppmerksom på at rammebestillingen ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="cc47f-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="cc47f-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="cc47f-126">Hvis du vil se resultatene av de foregående trinnene, velger du **Linje**-handlingen velger handlingen **Ikke-bokførte linjer** og deretter handlingen **Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="cc47f-127">I vinduet **Salgslinjer** velger du ønsket ordre, velger **Linje**-handlingen og deretter **Vis dokument**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="cc47f-128">Følgende gjelder for ordrer når de har blitt opprettet fra rammeordrer:</span><span class="sxs-lookup"><span data-stu-id="cc47f-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="cc47f-129">Når rammeordren konverteres til en ordre, inneholder ordren alle linjene fra rammeordren.</span><span class="sxs-lookup"><span data-stu-id="cc47f-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="cc47f-130">Linjene der antallet i **Levere (antall)**-feltet ble slettet, vises, men med tomme **Antall**-felt.</span><span class="sxs-lookup"><span data-stu-id="cc47f-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="cc47f-131">Du kan velge å la linjene stå, redigere dem eller slette dem.</span><span class="sxs-lookup"><span data-stu-id="cc47f-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="cc47f-132">Det er viktig å huske at antallet på ordrelinjen ikke må overstige antallet på den tilordnede rammeordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="cc47f-133">Ellers vil det ikke være mulig å bokføre ordren.</span><span class="sxs-lookup"><span data-stu-id="cc47f-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="cc47f-134">Når ordren er bokført som levert og/eller fakturert, oppdateres **Levert (antall)**- og **Fakturert (antall)**-feltene på den tilknyttede rammebestillingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="cc47f-135">Rammeordrenummeret og linjenummeret registreres som egenskaper for salgslinjene ved oppretting fra en rammeordre.</span><span class="sxs-lookup"><span data-stu-id="cc47f-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="cc47f-136">Når ordrer ikke er opprettet direkte fra rammeordren, men er relatert til den, kan en kobling mellom en ordre og en rammeordre opprettes ved at rammeordrenummeret i **Rammeordrenr**-feltet</span><span class="sxs-lookup"><span data-stu-id="cc47f-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="cc47f-137">på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-137">field on the sales order line.</span></span>  
- <span data-ttu-id="cc47f-138">Når ordren er opprettet for det totale antallet på en rammebestillingslinje, kan ingen andre ordrer opprettes for den samme linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="cc47f-139">Brukere kan ikke angi et antall i feltet **Levere (antall)**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="cc47f-140">Hvis det imidlertid er behov for å angi flere antall i en rammebestilling, kan verdien i **Antall**-feltet økes, og flere bestillinger kan da opprettes.</span><span class="sxs-lookup"><span data-stu-id="cc47f-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="cc47f-141">Den fakturerte rammeordren blir i systemet til den slettes, enten ved å slette individuelle rammeordrer, eller ved å bruke kjørselen **Slett fakturerte rammeordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="cc47f-142">Hvis en kunde også er registrert som kontakt i modulen Markedsføring, og hvis du har angitt en kode for samhandlingsmal for rammeordre i vinduet **Markedsføringsoppsett**, registreres en samhandling i tabellen Samhandlingspost når du velger **Skriv ut** for å skrive ut rammeordren.</span><span class="sxs-lookup"><span data-stu-id="cc47f-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="cc47f-143">Slik viser du statusen for rammebestillinger</span><span class="sxs-lookup"><span data-stu-id="cc47f-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="cc47f-144">Du kan vise statusen for en rammeordre i vinduet **Bestillingsstatistikk**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="cc47f-145">Dette kan være relevant når du begynner å fakturere ordren som opprettes fra rammebestillingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="cc47f-146">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="cc47f-147">Velg en rammebestilling, og velg deretter **Statistikk**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="cc47f-148">På hurtigfanen **Generelt** i **Bestillingsstatistikk**-vinduet vises en informasjonsoversikt over hele bestillingen, basert på det totale antallet i **Antall**-feltene på bestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="cc47f-149">På hurtigfanen **Fakturering** vises en informasjonsoversikt basert på det totale antallet i **Fakturer (antall)**-feltene på rammebestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="cc47f-150">På hurtigfanen **Levering** vises en informasjonsoversikt basert på det totale antallet i **Motta (antall)**-feltene på rammebestillingslinjene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="cc47f-151">På hurtigfanen **Forskudd** vises en informasjonsoversikt over eventuelle forhåndsbetalte beløp.</span><span class="sxs-lookup"><span data-stu-id="cc47f-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="cc47f-152">På hurtigfanen **Leverandør** vises bestemte grunnleggende opplysninger om leverandøren.</span><span class="sxs-lookup"><span data-stu-id="cc47f-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="cc47f-153">Vise ikke-bokførte og bokførte rammeordrelinjer</span><span class="sxs-lookup"><span data-stu-id="cc47f-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="cc47f-154">Koblingen mellom rammeordren og den opprinnelige salgsordren, og eventuelle andre salgsdokumenter, beholdes etter bokføring som en liste over bokførte og ikke-bokførte salgsordrefakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="cc47f-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="cc47f-155">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="cc47f-156">Åpne rammeordren du vil vise.</span><span class="sxs-lookup"><span data-stu-id="cc47f-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="cc47f-157">Hvis du vil vise ikke-bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Ikke-bokførte linjer**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="cc47f-158">Velg ett av følgende alternativene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="cc47f-159">Alternativ</span><span class="sxs-lookup"><span data-stu-id="cc47f-159">Option</span></span></th>
    <th><span data-ttu-id="cc47f-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc47f-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-161">**Bestillinger**</span><span class="sxs-lookup"><span data-stu-id="cc47f-161">**Orders**</span></span></td>
    <td><span data-ttu-id="cc47f-162">Angir åpne ordrer knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-163">**Fakturaer**</span><span class="sxs-lookup"><span data-stu-id="cc47f-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="cc47f-164">Angir åpne fakturaer som har blitt knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="cc47f-165">Åpne fakturaer knyttes vanligvis til en rammeordre ved at rammeordrenummeret angis på salgsfakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-166">**Ordreretur**</span><span class="sxs-lookup"><span data-stu-id="cc47f-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="cc47f-167">Angir åpne ordrereturer som har blitt knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-168">**Kreditnotaer**</span><span class="sxs-lookup"><span data-stu-id="cc47f-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="cc47f-169">Angir åpne kreditnotaer som har blitt knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="cc47f-170">
4.Hvis du vil vise bokførte poster, velger du den aktuelle linjen, velger **Linje**-handlingen og deretter **Bokførte linjer**.</span><span class="sxs-lookup"><span data-stu-id="cc47f-170">
4. To view posted entries, select the line in question, choose the **Line** action, and then choose the **Posted Lines** action.</span></span> <span data-ttu-id="cc47f-171">Velg ett av følgende alternativene.</span><span class="sxs-lookup"><span data-stu-id="cc47f-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="cc47f-172">Alternativ</span><span class="sxs-lookup"><span data-stu-id="cc47f-172">Option</span></span></th>
    <th><span data-ttu-id="cc47f-173">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc47f-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-174">**Følgesedler**</span><span class="sxs-lookup"><span data-stu-id="cc47f-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="cc47f-175">Bokførte følgesedler knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-176">**Fakturaer**</span><span class="sxs-lookup"><span data-stu-id="cc47f-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="cc47f-177">Bokførte fakturaer knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-178">**Retursedler**</span><span class="sxs-lookup"><span data-stu-id="cc47f-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="cc47f-179">Åpne retursedler som har blitt knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="cc47f-180">**Kreditnotaer**</span><span class="sxs-lookup"><span data-stu-id="cc47f-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="cc47f-181">Bokførte kreditnotaer som har blitt knyttet til den valgte linjen.</span><span class="sxs-lookup"><span data-stu-id="cc47f-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="cc47f-182">
5.I **Salgslinjer**-vinduet velger du handlingen **Vis dokument** for å vise posten.</span><span class="sxs-lookup"><span data-stu-id="cc47f-182">
5. In the **Sales Lines** window, choose the **Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc47f-183">Se også</span><span class="sxs-lookup"><span data-stu-id="cc47f-183">See Also</span></span>
[<span data-ttu-id="cc47f-184">Salg</span><span class="sxs-lookup"><span data-stu-id="cc47f-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="cc47f-185">Sette opp salg</span><span class="sxs-lookup"><span data-stu-id="cc47f-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="cc47f-186">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cc47f-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

