---
title: "Gjennomgang – Planlegge forsyninger manuelt | Microsoft-dokumentasjon"
description: "Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov. Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: de00ca393b5d2c28292ae3deba743ce3447b6145
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="adfba-104">Gjennomgang: planlegge forsyninger manuelt</span><span class="sxs-lookup"><span data-stu-id="adfba-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="adfba-105">Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov.</span><span class="sxs-lookup"><span data-stu-id="adfba-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="adfba-106">Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen.</span><span class="sxs-lookup"><span data-stu-id="adfba-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="adfba-107">I denne gjennomgangen skal du bruke vinduet **Ordreplanlegging**, som er et enkelt verktøy for forsyningsplanlegging som er basert på manuell beslutningstaking i stedet for parameterbasert automatisk planlegging.</span><span class="sxs-lookup"><span data-stu-id="adfba-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="adfba-108">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="adfba-108">About This Walkthrough</span></span>  
 <span data-ttu-id="adfba-109">Denne gjennomgangen tar for seg følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="adfba-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="adfba-110">Planlegging av en bestilling for produksjonskomponenter</span><span class="sxs-lookup"><span data-stu-id="adfba-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="adfba-111">Planlegging av en overføringsordre for å dekke salgsbehov</span><span class="sxs-lookup"><span data-stu-id="adfba-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="adfba-112">Planlegging av en produksjonsordre for en vare med flere nivåer</span><span class="sxs-lookup"><span data-stu-id="adfba-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="adfba-113">Roller</span><span class="sxs-lookup"><span data-stu-id="adfba-113">Roles</span></span>  
 <span data-ttu-id="adfba-114">Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:</span><span class="sxs-lookup"><span data-stu-id="adfba-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="adfba-115">Produksjonsplanlegger</span><span class="sxs-lookup"><span data-stu-id="adfba-115">Production Planner</span></span>  
-   <span data-ttu-id="adfba-116">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="adfba-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="adfba-117">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="adfba-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="adfba-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="adfba-118">Prerequisites</span></span>  
 <span data-ttu-id="adfba-119">Før du begynner med denne gjennomgangen, må du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="adfba-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="adfba-120">Du må gjøre følgende endringer i databasen:</span><span class="sxs-lookup"><span data-stu-id="adfba-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="adfba-121">Slett alle eksisterende ordrer for sykler.</span><span class="sxs-lookup"><span data-stu-id="adfba-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="adfba-122">Opprett én ordre for ti sykler i OSLO.</span><span class="sxs-lookup"><span data-stu-id="adfba-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="adfba-123">Slett alle planlagte og fast planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="adfba-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="adfba-124">Ikke slett påbegynte ordrer med poster som allerede er bokført.</span><span class="sxs-lookup"><span data-stu-id="adfba-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="adfba-125">Som en regel bruker du de foreslåtte dataene i denne gjennomgangen siden disse dataene har de nødvendige postene.</span><span class="sxs-lookup"><span data-stu-id="adfba-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="adfba-126">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="adfba-126">Story</span></span>  
 <span data-ttu-id="adfba-127">Martin, produksjonsplanleggeren i et lite produksjonsselskap, er i ferd med å planlegge produksjon og bestillinger for å dekke nytt salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="adfba-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="adfba-128">Siden produktene har få stykklistenivåer og ordreflyten er relativt lav, bruker Martin vinduet **Ordreplanlegging** til å opprette forsyningsordrer manuelt, ett produktnivå om gangen.</span><span class="sxs-lookup"><span data-stu-id="adfba-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="adfba-129">I et mer sammensatt produksjonsmiljø brukes planleggingsforslaget til å planlegge forsyning basert på vareparametere, for eksempel periode for ny planlegging, sikkerhetsleveringstid, gjenbestillingspunkt og masseberegninger av konsolidert behov fra alle produktnivåer.</span><span class="sxs-lookup"><span data-stu-id="adfba-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="adfba-130">Konfigurere eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="adfba-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="adfba-131">Det standard demonstrasjonsselskapet CRONUS har for tiden et stort behov som ikke er planlagt.</span><span class="sxs-lookup"><span data-stu-id="adfba-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="adfba-132">I løpet av de ulike planleggingsoppgavene i denne gjennomgangen må du avvike fra den realistiske forretningsflyten ved å ignorere behov med nære forfallsdatoer og i stedet bruke behov med senere forfall.</span><span class="sxs-lookup"><span data-stu-id="adfba-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="adfba-133">Bruke vinduet Ordreplanlegging eller Bestillingsplanlegging</span><span class="sxs-lookup"><span data-stu-id="adfba-133">Using the Order Planning Window</span></span>  
 <span data-ttu-id="adfba-134">Du kan få tilgang til vinduet **Ordreplanlegging** eller Bestillingsplanlegging fra mange ulike steder på **Avdelinger**-menyen i navigasjonsruten:</span><span class="sxs-lookup"><span data-stu-id="adfba-134">The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:</span></span>  

-   <span data-ttu-id="adfba-135">Produksjon, Planlegging</span><span class="sxs-lookup"><span data-stu-id="adfba-135">Manufacturing, Planning</span></span>  
-   <span data-ttu-id="adfba-136">Salg og markedsføring, Ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="adfba-136">Sales & Marketing, Order Processing</span></span>  
-   <span data-ttu-id="adfba-137">Kjøp, Planlegging</span><span class="sxs-lookup"><span data-stu-id="adfba-137">Purchase, Planning</span></span>  
-   <span data-ttu-id="adfba-138">I fanenn du åpne dette vinduet for en bestemt produksjonsordre ved å velge **Planlegging** under **Ordre** i fanen **Naviger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-138">In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.</span></span>  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="adfba-139">Slik bruker du vinduet Ordreplanlegging:</span><span class="sxs-lookup"><span data-stu-id="adfba-139">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="adfba-140">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordreplanlegging**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-140">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="adfba-141">Når vinduet **Ordreplanlegging** åpnes for første gang, må en plan beregnes for å vise det nye behovet siden det sist ble beregnet.</span><span class="sxs-lookup"><span data-stu-id="adfba-141">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="adfba-142">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-142">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="adfba-143">Planleggingssystemet analyserer eventuelt nytt behov som er introdusert, for eksempel nye salg, endrede salg eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="adfba-143">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="adfba-144">Antallet som trengs for hver behovslinje, beregnes basert på totalt disponibelt antall.</span><span class="sxs-lookup"><span data-stu-id="adfba-144">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="adfba-145">Denne beregningen utføres ordre for ordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-145">This calculation is performed order-by-order.</span></span> <span data-ttu-id="adfba-146">Dette betyr at ordren som inkluderer behovslinjen med den tidligste forfallsdatoen eller forsendelsesdatoen, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="adfba-146">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="adfba-147">Etter dette beregnes ytterligere behovslinjer i den samme ordren, uavhengig av forfallsdatoen eller forsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="adfba-147">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="adfba-148">Kontroller at vinduet **Ordreplanlegging** er maksimert, og at størrelsen på kolonnefeltene er endret slik at alle standard feltnavn vises.</span><span class="sxs-lookup"><span data-stu-id="adfba-148">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="adfba-149">Når beregningen er fullført, vises alt udekket behov som sammenslåtte (skjulte) ordrehodelinjer sortert etter tidligste behovsdato.</span><span class="sxs-lookup"><span data-stu-id="adfba-149">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="adfba-150">Merk at CRONUS har flere ordrer med udekket behov.</span><span class="sxs-lookup"><span data-stu-id="adfba-150">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="adfba-151">Hver planleggingslinje i fet representerer en ordre eller produksjonsordre, inkludert minst én line med utilstrekkelig disponibelt antall.</span><span class="sxs-lookup"><span data-stu-id="adfba-151">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="adfba-152">Velg filteret **Alle behov** i feltet **Vis behov som**.</span><span class="sxs-lookup"><span data-stu-id="adfba-152">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="adfba-153">Du kan bruke **Behovstype**-feltet til å velge hvilke ordretyper du vil vise.</span><span class="sxs-lookup"><span data-stu-id="adfba-153">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="adfba-154">Ordrer uten disponibilitetsproblemer vises ikke.</span><span class="sxs-lookup"><span data-stu-id="adfba-154">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="adfba-155">Hvis det ikke finnes noen ordrer når en plan beregnes, får du en melding, og ingen planleggingslinjer vises.</span><span class="sxs-lookup"><span data-stu-id="adfba-155">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="adfba-156">Planlegge en bestilling for å dekke komponentbehov</span><span class="sxs-lookup"><span data-stu-id="adfba-156">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="adfba-157">I denne fremgangsmåten oppretter du en bestilling for produksjonskomponenter det er behov for.</span><span class="sxs-lookup"><span data-stu-id="adfba-157">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="adfba-158">Slik planlegger du en bestilling for å dekke et komponentbehov i produksjon:</span><span class="sxs-lookup"><span data-stu-id="adfba-158">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="adfba-159">Vis den første linjen (velg plussymbolet (+)).</span><span class="sxs-lookup"><span data-stu-id="adfba-159">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="adfba-160">Velg den første behovslinjen, med vare **LSU-15**, og velg deretter **Vis dokument**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-160">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="adfba-161">Lukk den åpnede produksjonsordren for å gå tilbake til vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-161">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="adfba-162">Velg **Kjøp** i feltet **Etterfyllingssystem**.</span><span class="sxs-lookup"><span data-stu-id="adfba-162">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="adfba-163">Standardverdien er fra varekortet (eller LFE-kortet), men du kan endre den til ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="adfba-163">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="adfba-164">**Kjøp** – for å opprette en bestilling.</span><span class="sxs-lookup"><span data-stu-id="adfba-164">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="adfba-165">**Overfør** – opprette en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-165">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="adfba-166">**Prod.ordre** – for å opprette en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-166">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="adfba-167">Velg ett av følgende alternativer i henhold til det valgte etterfyllingssystemet, i **Forsyning fra**-feltet.</span><span class="sxs-lookup"><span data-stu-id="adfba-167">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="adfba-168">**Leverandør** – for kjøp</span><span class="sxs-lookup"><span data-stu-id="adfba-168">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="adfba-169">**Lokasjon** – For overføringer</span><span class="sxs-lookup"><span data-stu-id="adfba-169">**Location** – For transfers</span></span>  

     <span data-ttu-id="adfba-170">Hvis du ikke fyller ut feltet, vises en feilmelding når du prøver å opprette forsyningsordrene.</span><span class="sxs-lookup"><span data-stu-id="adfba-170">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="adfba-171">Hvis komponentene har et standard leverandørnummer angitt på varekortene, blir linjene forhåndsdefinert.</span><span class="sxs-lookup"><span data-stu-id="adfba-171">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="adfba-172">Velg feltet **Forsyning fra**.</span><span class="sxs-lookup"><span data-stu-id="adfba-172">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="adfba-173">Velg **Ny**-handlingen i vinduet **Vare/leverandør-katalog**, og velg deretter leverandør **30000**.</span><span class="sxs-lookup"><span data-stu-id="adfba-173">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="adfba-174">Velg **OK**-knappen for å gå tilbake til vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-174">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="adfba-175">Kopier leverandør **30000** til de andre linjene for høyttalerkomponenter i denne produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-175">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="adfba-176">Du er nå klar til å opprette en bestilling.</span><span class="sxs-lookup"><span data-stu-id="adfba-176">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="adfba-177">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-177">Choose the **Make Orders** action.</span></span> <span data-ttu-id="adfba-178">Vinduet **Lag forsyningsordrer** åpnes.</span><span class="sxs-lookup"><span data-stu-id="adfba-178">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="adfba-179">På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **den aktive ordren**.</span><span class="sxs-lookup"><span data-stu-id="adfba-179">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="adfba-180">Velg alternativet **Lag bestilling** i feltet **Opprett bestilling** på hurtigfanen **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="adfba-180">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="adfba-181">Velg **OK**-knappen for å opprette en bestilling for alle komponentene i ordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-181">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="adfba-182">Nå opprettes og lagres bestillingene som de siste bestillingene i bestillingsoversikten.</span><span class="sxs-lookup"><span data-stu-id="adfba-182">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="adfba-183">Planlegge en overføringsordre for å dekke salgsbehov</span><span class="sxs-lookup"><span data-stu-id="adfba-183">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="adfba-184">I denne fremgangsmåten skal du planlegge for behov fra en ordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-184">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="adfba-185">Behovslinjer representerer salgslinjer, ikke komponentlinjer som i produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="adfba-185">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="adfba-186">Slik planlegger du en overføringsordre for å dekke salgsbehov:</span><span class="sxs-lookup"><span data-stu-id="adfba-186">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="adfba-187">Flytt pekeren til planleggingslinjen for ordrenummer **2008**.</span><span class="sxs-lookup"><span data-stu-id="adfba-187">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="adfba-188">Vis linjen, og flytt pekeren til behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="adfba-188">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="adfba-189">Ordrenummer **2008** er for ti høyttalere, varen **LS-120**, som er bestilt av Pedersen Kontorutstyr AS.</span><span class="sxs-lookup"><span data-stu-id="adfba-189">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="adfba-190">Definert etterfyllingssystem og standardleverandør for varen vises.</span><span class="sxs-lookup"><span data-stu-id="adfba-190">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="adfba-191">Det er fire informasjonsfelt nederst i vinduet.</span><span class="sxs-lookup"><span data-stu-id="adfba-191">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="adfba-192">I feltet **Tidligste tilgjengelige dato** blir de ti stykkene som trengs, tilgjengelige på en inngående forsyningsordre ni dager senere enn gjeldende forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="adfba-192">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="adfba-193">Hvis dette blir for sent for kunden, viser feltet **Tilgjengelig for overføring** at 13 stykker av varen er tilgjengelig på en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="adfba-193">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="adfba-194">Det er aktuelt å planlegge for denne varebeholdningen.</span><span class="sxs-lookup"><span data-stu-id="adfba-194">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="adfba-195">Velg feltet **Tilgjengelig for overføring** for å åpne vinduet **Hent alternativ forsyning**.</span><span class="sxs-lookup"><span data-stu-id="adfba-195">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="adfba-196">Velg **OK**-knappen for å bestille de ti varene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="adfba-196">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="adfba-197">På behovslinjen er det foreslåtte kjøpet erstattet med en en overføring fra lokasjonen GRØNN.</span><span class="sxs-lookup"><span data-stu-id="adfba-197">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="adfba-198">Funksjonen **Lag bestillinger** oppretter en overføringsordre fra GRØNN til den etterspurte lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="adfba-198">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="adfba-199">**Erstatning finnes**-feltet fungerer på samme måte.</span><span class="sxs-lookup"><span data-stu-id="adfba-199">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="adfba-200">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-200">Choose the **Make Orders** action.</span></span> <span data-ttu-id="adfba-201">Vinduet **Lag forsyningsordrer** åpnes.</span><span class="sxs-lookup"><span data-stu-id="adfba-201">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="adfba-202">På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **Den aktive ordren**.</span><span class="sxs-lookup"><span data-stu-id="adfba-202">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="adfba-203">Velg alternativet **Lag overføringsordrer** i feltet **Opprett overføringsordre** på hurtigfanen **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="adfba-203">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="adfba-204">Velg **OK**-knappen for å opprette overføringsordren som skal forsyne ordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-204">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="adfba-205">Overføringsordren er nå opprettet og lagret i oversikten som den siste ordren i oversikten over åpne overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="adfba-205">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="adfba-206">Planlegge en produksjonsordre med flere nivåer for å dekke et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="adfba-206">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="adfba-207">I denne fremgangsmåten skal du planlegge å dekke salgsbehov for en produsert vare med flere produktnivåer, der hvert nivå skaper et avhengig produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="adfba-207">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="adfba-208">Slik planlegger du produksjon med flere nivåer for å dekke salgsbehov:</span><span class="sxs-lookup"><span data-stu-id="adfba-208">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="adfba-209">Merk planleggingslinjen med salgsbehov for ordrenummer **1001**, opprettet tidligere som nødvendige data.</span><span class="sxs-lookup"><span data-stu-id="adfba-209">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="adfba-210">Denne behovslinjen er en salgslinje, men varen har **Prod.ordre** som definert etterfyllingssystem.</span><span class="sxs-lookup"><span data-stu-id="adfba-210">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="adfba-211">Begynn med å legge til en ekstra ringeklokke i komponentbehovet for hver sykkel.</span><span class="sxs-lookup"><span data-stu-id="adfba-211">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="adfba-212">Velg handlingen **Komponenter** for å åpne **Planleggingskomponenter**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="adfba-212">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="adfba-213">På linjen med varen ringeklokke endrer du **Antall per**-feltet fra **1** til **2**.</span><span class="sxs-lookup"><span data-stu-id="adfba-213">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="adfba-214">Vurder planleggingsalternativene i vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-214">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="adfba-215">I dette tilfellet har du ingen alternative forsyningsmuligheter, ingen overføring, erstatning eller senere levering.</span><span class="sxs-lookup"><span data-stu-id="adfba-215">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="adfba-216">Du må opprette den foreslåtte forsyningsordren – en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-216">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="adfba-217">Velg **Lag ordre**-handlingen for å opprette produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-217">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="adfba-218">Legg merke til at planleggingslinjen for ordre **1001** i vinduet **Ordreplanlegging** ikke lenger finnes, og at det opprinnelige salgsbehovet er dekket.</span><span class="sxs-lookup"><span data-stu-id="adfba-218">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="adfba-219">Lukk vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-219">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="adfba-220">Nå kunne du ha valgt å fortsette i denne visningen og fylle ut alle planleggingsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="adfba-220">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="adfba-221">I stedet skal du nå ta på deg rollen som produksjonsplanlegger ved å gå til produksjonsordren du nettopp opprettet, og åpne vinduet **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-221">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="adfba-222">Som produksjonsplanlegger må du nå planlegge en bestemt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="adfba-222">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="adfba-223">Slik planlegger du en bestemt produksjonsordre:</span><span class="sxs-lookup"><span data-stu-id="adfba-223">To plan a specific production order</span></span>  

1.  <span data-ttu-id="adfba-224">Åpne produksjonsordren **101001**, for ti sykler, som du nettopp opprettet med funksjonen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-224">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="adfba-225">Åpne vinduet **Prod.ordrekomponenter** for å kontrollere at den ekstra ringeklokken gjenspeiles på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-225">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="adfba-226">Velg handlingen **Planlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-226">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="adfba-227">Vinduet **Ordreplanlegging** åpnes i en visning som alltid er filtrert etter bestemte produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="adfba-227">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="adfba-228">Salgsbehov vises ikke.</span><span class="sxs-lookup"><span data-stu-id="adfba-228">Sales demand is not displayed.</span></span> <span data-ttu-id="adfba-229">Du må beregne en plan før du kan vise ytterligere behov.</span><span class="sxs-lookup"><span data-stu-id="adfba-229">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="adfba-230">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-230">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="adfba-231">Legg merke til at fire nye produksjonsordrer vises som ikke-planlagt produksjonsbehov som er hentet fra ordre **101001**.</span><span class="sxs-lookup"><span data-stu-id="adfba-231">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="adfba-232">De nye linjene representerer produksjonsbehov fra delmonteringene som må opprettes for å produsere ordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-232">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="adfba-233">Velg **Utvid alle**-handlingen for å få en oversikt over alt produksjonsbehov for de to produksjonsordrene.</span><span class="sxs-lookup"><span data-stu-id="adfba-233">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="adfba-234">For å gi tilleggsinformasjon om behovslinjene kan du legge til feltene **Behovsmengde** og **Disponibel behovsmengde** i visningen.</span><span class="sxs-lookup"><span data-stu-id="adfba-234">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="adfba-235">Nå må du forsyne ti av hver komponent.</span><span class="sxs-lookup"><span data-stu-id="adfba-235">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="adfba-236">Merk at fire av behovslinjene har Prod.ordre. fra etterfyllingssystemet.</span><span class="sxs-lookup"><span data-stu-id="adfba-236">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="adfba-237">Disse fire delmonteringene representerer sykkelens andre produktnivå.</span><span class="sxs-lookup"><span data-stu-id="adfba-237">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="adfba-238">Standardinnstillingene for etterfylling er allerede fylt ut, og du kan begynne å lage bestillinger.</span><span class="sxs-lookup"><span data-stu-id="adfba-238">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="adfba-239">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-239">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="adfba-240">Før du velger **OK**-knappen, må du legge merke til teksten i hurtigfanen **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="adfba-240">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="adfba-241">Denne teksten er viktig fordi du vet at sykkelen har flere produserte komponenter, delmonteringer, som kan være etterspurt når du oppretter denne produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-241">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="adfba-242">Velg alternativet **Alle linjer** i feltet **Lag ordrer for** i vinduet **Lag forsyningsordrer**, og klikk deretter **OK** for å opprette produksjonsordrer for det andre produktnivået i ordren.</span><span class="sxs-lookup"><span data-stu-id="adfba-242">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="adfba-243">Merk at produksjonsbehovet på øverste nivå for produksjonsordren 101001 ikke lenger finnes.</span><span class="sxs-lookup"><span data-stu-id="adfba-243">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="adfba-244">Dette betyr at det er planlagt for det opprinnelige produksjonsbehovet for delmonteringer.</span><span class="sxs-lookup"><span data-stu-id="adfba-244">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="adfba-245">I vinduet **Ordreplanlegging** beregner du en plan på nytt for å planlegge sykkelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="adfba-245">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="adfba-246">Velg **Beregn plan**-handlingen for å beregne planen på nytt i henhold til instruksjonene i den innebygde hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="adfba-246">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="adfba-247">De to nye linjene representerer ytterligere produksjonsbehov hentet fra delmonteringene som ble planlagt i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="adfba-247">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="adfba-248">Det blir foreslått at du lager to produksjonsordrer for å forsyne hjulnavene, én for ti fornav og én for ti baknav.</span><span class="sxs-lookup"><span data-stu-id="adfba-248">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="adfba-249">Velg **Utvid alle**-handlingen for å få en oversikt over alt behov for de to produksjonsordrene.</span><span class="sxs-lookup"><span data-stu-id="adfba-249">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="adfba-250">Den foreslåtte forsyningsplanen angir at i alt fire bestillinger blir opprettet for komponentene.</span><span class="sxs-lookup"><span data-stu-id="adfba-250">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="adfba-251">Du bestemmer deg for å lage de foreslåtte bestillingene.</span><span class="sxs-lookup"><span data-stu-id="adfba-251">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="adfba-252">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="adfba-252">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="adfba-253">Velg alternativet **Alle linjer** i feltet **Lag ordrer for**, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="adfba-253">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="adfba-254">Kontroller om det finnes ytterligere behov for produksjonen av den overordnede varen, sykkelen, som selges i ordre 1001.</span><span class="sxs-lookup"><span data-stu-id="adfba-254">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="adfba-255">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-255">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="adfba-256">Meldingen angir at alle nødvendige varer nå er forsynt.</span><span class="sxs-lookup"><span data-stu-id="adfba-256">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="adfba-257">Kontroller de fast planlagte produksjonsordrene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="adfba-257">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="adfba-258">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="adfba-258">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="adfba-259">Se gjennom hvordan start- og sluttidspunkt for individuelle ordrer planlegges i henhold til produktstrukturen, i vinduet **Fast planlagte prod.ordrer**.</span><span class="sxs-lookup"><span data-stu-id="adfba-259">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="adfba-260">Komponentene på laveste nivå produseres først.</span><span class="sxs-lookup"><span data-stu-id="adfba-260">The lowest-level components are produced first.</span></span> <span data-ttu-id="adfba-261">Derfor må du planlegge ordrer med flere nivåer slik det er demonstrert i denne arbeidsflyten for planlegging.</span><span class="sxs-lookup"><span data-stu-id="adfba-261">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="adfba-262">Se også</span><span class="sxs-lookup"><span data-stu-id="adfba-262">See Also</span></span>  
 <span data-ttu-id="adfba-263">[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="adfba-263">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="adfba-264">Gjennomgang: planlegge forsyninger automatisk</span><span class="sxs-lookup"><span data-stu-id="adfba-264">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

