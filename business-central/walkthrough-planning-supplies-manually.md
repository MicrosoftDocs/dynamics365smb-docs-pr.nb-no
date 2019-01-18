---
title: "Gjennomgang – Planlegge forsyninger manuelt | Microsoft-dokumentasjon"
description: "Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov. Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen."
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
ms.openlocfilehash: d0a7088e436def55b3c7ddc3115065c66686b7fb
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="33394-104">Gjennomgang: planlegge forsyninger manuelt</span><span class="sxs-lookup"><span data-stu-id="33394-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="33394-105">Denne gjennomgangen viser hvordan du planlegger forsyningsordrer for å dekke nytt behov.</span><span class="sxs-lookup"><span data-stu-id="33394-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="33394-106">Du kan sette i gang forsyningsplanlegging med jevne mellomrom, for eksempel hver morgen eller hver mandag, eller når du blir varslet av salg eller produksjon, avhengig av behovstypen.</span><span class="sxs-lookup"><span data-stu-id="33394-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="33394-107">I denne gjennomgangen skal du bruke siden **Ordreplanlegging**, som er et enkelt verktøy for forsyningsplanlegging som er basert på manuell beslutningstaking i stedet for parameterbasert automatisk planlegging.</span><span class="sxs-lookup"><span data-stu-id="33394-107">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="33394-108">Denne gjennomgangen</span><span class="sxs-lookup"><span data-stu-id="33394-108">About This Walkthrough</span></span>  
 <span data-ttu-id="33394-109">Denne gjennomgangen tar for seg følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="33394-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="33394-110">Planlegging av en bestilling for produksjonskomponenter</span><span class="sxs-lookup"><span data-stu-id="33394-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="33394-111">Planlegging av en overføringsordre for å dekke salgsbehov</span><span class="sxs-lookup"><span data-stu-id="33394-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="33394-112">Planlegging av en produksjonsordre for en vare med flere nivåer</span><span class="sxs-lookup"><span data-stu-id="33394-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="33394-113">Roller</span><span class="sxs-lookup"><span data-stu-id="33394-113">Roles</span></span>  
 <span data-ttu-id="33394-114">Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:</span><span class="sxs-lookup"><span data-stu-id="33394-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="33394-115">Produksjonsplanlegger</span><span class="sxs-lookup"><span data-stu-id="33394-115">Production Planner</span></span>  
-   <span data-ttu-id="33394-116">Innkjøper</span><span class="sxs-lookup"><span data-stu-id="33394-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="33394-117">Ordrebehandler</span><span class="sxs-lookup"><span data-stu-id="33394-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="33394-118">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="33394-118">Prerequisites</span></span>  
 <span data-ttu-id="33394-119">Før du begynner med denne gjennomgangen, må du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="33394-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="33394-120">Du må gjøre følgende endringer i databasen:</span><span class="sxs-lookup"><span data-stu-id="33394-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="33394-121">Slett alle eksisterende ordrer for sykler.</span><span class="sxs-lookup"><span data-stu-id="33394-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="33394-122">Opprett én ordre for ti sykler i OSLO.</span><span class="sxs-lookup"><span data-stu-id="33394-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="33394-123">Slett alle planlagte og fast planlagte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="33394-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="33394-124">Ikke slett påbegynte ordrer med poster som allerede er bokført.</span><span class="sxs-lookup"><span data-stu-id="33394-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="33394-125">Som en regel bruker du de foreslåtte dataene i denne gjennomgangen siden disse dataene har de nødvendige postene.</span><span class="sxs-lookup"><span data-stu-id="33394-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="33394-126">Hovedscenario</span><span class="sxs-lookup"><span data-stu-id="33394-126">Story</span></span>  
 <span data-ttu-id="33394-127">Martin, produksjonsplanleggeren i et lite produksjonsselskap, er i ferd med å planlegge produksjon og bestillinger for å dekke nytt salgsbehov.</span><span class="sxs-lookup"><span data-stu-id="33394-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="33394-128">Siden produktene har få stykklistenivåer og ordreflyten er relativt lav, bruker Martin siden **Ordreplanlegging** til å opprette forsyningsordrer manuelt, ett produktnivå om gangen.</span><span class="sxs-lookup"><span data-stu-id="33394-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="33394-129">I et mer sammensatt produksjonsmiljø brukes planleggingsforslaget til å planlegge forsyning basert på vareparametere, for eksempel periode for ny planlegging, sikkerhetsleveringstid, gjenbestillingspunkt og masseberegninger av konsolidert behov fra alle produktnivåer.</span><span class="sxs-lookup"><span data-stu-id="33394-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="33394-130">Konfigurere eksempeldataene</span><span class="sxs-lookup"><span data-stu-id="33394-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="33394-131">Det standard demonstrasjonsselskapet CRONUS har for tiden et stort behov som ikke er planlagt.</span><span class="sxs-lookup"><span data-stu-id="33394-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="33394-132">I løpet av de ulike planleggingsoppgavene i denne gjennomgangen må du avvike fra den realistiske forretningsflyten ved å ignorere behov med nære forfallsdatoer og i stedet bruke behov med senere forfall.</span><span class="sxs-lookup"><span data-stu-id="33394-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="33394-133">Bruke siden Ordreplanlegging</span><span class="sxs-lookup"><span data-stu-id="33394-133">Using the Order Planning Page</span></span>  

<!-- 
The **Order Planning** page can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this page for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="33394-134">Slik bruker du siden Ordreplanlegging:</span><span class="sxs-lookup"><span data-stu-id="33394-134">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="33394-135">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordreplanlegging**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="33394-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="33394-136">Når siden **Ordreplanlegging** åpnes for første gang, må en plan beregnes for å vise det nye behovet siden det sist ble beregnet.</span><span class="sxs-lookup"><span data-stu-id="33394-136">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="33394-137">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="33394-137">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="33394-138">Planleggingssystemet analyserer eventuelt nytt behov som er introdusert, for eksempel nye salg, endrede salg eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="33394-138">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="33394-139">Antallet som trengs for hver behovslinje, beregnes basert på totalt disponibelt antall.</span><span class="sxs-lookup"><span data-stu-id="33394-139">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="33394-140">Denne beregningen utføres ordre for ordre.</span><span class="sxs-lookup"><span data-stu-id="33394-140">This calculation is performed order-by-order.</span></span> <span data-ttu-id="33394-141">Dette betyr at ordren som inkluderer behovslinjen med den tidligste forfallsdatoen eller forsendelsesdatoen, beregnes først.</span><span class="sxs-lookup"><span data-stu-id="33394-141">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="33394-142">Etter dette beregnes ytterligere behovslinjer i den samme ordren, uavhengig av forfallsdatoen eller forsendelsesdatoen.</span><span class="sxs-lookup"><span data-stu-id="33394-142">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="33394-143">Kontroller at siden **Ordreplanlegging** er maksimert, og at størrelsen på kolonnefeltene er endret slik at alle standard feltnavn vises.</span><span class="sxs-lookup"><span data-stu-id="33394-143">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="33394-144">Når beregningen er fullført, vises alt udekket behov som sammenslåtte (skjulte) ordrehodelinjer sortert etter tidligste behovsdato.</span><span class="sxs-lookup"><span data-stu-id="33394-144">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="33394-145">Merk at CRONUS har flere ordrer med udekket behov.</span><span class="sxs-lookup"><span data-stu-id="33394-145">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="33394-146">Hver planleggingslinje i fet representerer en ordre eller produksjonsordre, inkludert minst én line med utilstrekkelig disponibelt antall.</span><span class="sxs-lookup"><span data-stu-id="33394-146">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="33394-147">Velg filteret **Alle behov** i feltet **Vis behov som**.</span><span class="sxs-lookup"><span data-stu-id="33394-147">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="33394-148">Du kan bruke **Behovstype**-feltet til å velge hvilke ordretyper du vil vise.</span><span class="sxs-lookup"><span data-stu-id="33394-148">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="33394-149">Ordrer uten disponibilitetsproblemer vises ikke.</span><span class="sxs-lookup"><span data-stu-id="33394-149">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="33394-150">Hvis det ikke finnes noen ordrer når en plan beregnes, får du en melding, og ingen planleggingslinjer vises.</span><span class="sxs-lookup"><span data-stu-id="33394-150">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="33394-151">Planlegge en bestilling for å dekke komponentbehov</span><span class="sxs-lookup"><span data-stu-id="33394-151">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="33394-152">I denne fremgangsmåten oppretter du en bestilling for produksjonskomponenter det er behov for.</span><span class="sxs-lookup"><span data-stu-id="33394-152">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="33394-153">Slik planlegger du en bestilling for å dekke et komponentbehov i produksjon:</span><span class="sxs-lookup"><span data-stu-id="33394-153">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="33394-154">Vis den første linjen (velg plussymbolet (+)).</span><span class="sxs-lookup"><span data-stu-id="33394-154">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="33394-155">Velg den første behovslinjen, med vare **LSU-15**, og velg deretter **Vis dokument**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="33394-155">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="33394-156">Lukk den åpnede produksjonsordren for å gå tilbake til siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-156">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="33394-157">Velg **Kjøp** i feltet **Etterfyllingssystem**.</span><span class="sxs-lookup"><span data-stu-id="33394-157">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="33394-158">Standardverdien er fra varekortet (eller LFE-kortet), men du kan endre den til ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="33394-158">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="33394-159">**Kjøp** – for å opprette en bestilling.</span><span class="sxs-lookup"><span data-stu-id="33394-159">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="33394-160">**Overfør** – opprette en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="33394-160">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="33394-161">**Prod.ordre** – for å opprette en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="33394-161">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="33394-162">Velg ett av følgende alternativer i henhold til det valgte etterfyllingssystemet, i **Forsyning fra**-feltet.</span><span class="sxs-lookup"><span data-stu-id="33394-162">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="33394-163">**Leverandør** – for kjøp</span><span class="sxs-lookup"><span data-stu-id="33394-163">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="33394-164">**Lokasjon** – For overføringer</span><span class="sxs-lookup"><span data-stu-id="33394-164">**Location** – For transfers</span></span>  

     <span data-ttu-id="33394-165">Hvis du ikke fyller ut feltet, vises en feilmelding når du prøver å opprette forsyningsordrene.</span><span class="sxs-lookup"><span data-stu-id="33394-165">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="33394-166">Hvis komponentene har et standard leverandørnummer angitt på varekortene, blir linjene forhåndsdefinert.</span><span class="sxs-lookup"><span data-stu-id="33394-166">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="33394-167">Velg feltet **Forsyning fra**.</span><span class="sxs-lookup"><span data-stu-id="33394-167">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="33394-168">Velg **Ny**-handlingen på siden **Vare/leverandør-katalog**, og velg deretter leverandør **30000**.</span><span class="sxs-lookup"><span data-stu-id="33394-168">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="33394-169">Velg **OK**-knappen for å gå tilbake til siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-169">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="33394-170">Kopier leverandør **30000** til de andre linjene for høyttalerkomponenter i denne produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="33394-170">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="33394-171">Du er nå klar til å opprette en bestilling.</span><span class="sxs-lookup"><span data-stu-id="33394-171">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="33394-172">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="33394-172">Choose the **Make Orders** action.</span></span> <span data-ttu-id="33394-173">Siden **Lag forsyningsordrer** åpnes.</span><span class="sxs-lookup"><span data-stu-id="33394-173">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="33394-174">På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **den aktive ordren**.</span><span class="sxs-lookup"><span data-stu-id="33394-174">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="33394-175">Velg alternativet **Lag bestilling** i feltet **Opprett bestilling** på hurtigfanen **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="33394-175">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="33394-176">Velg **OK**-knappen for å opprette en bestilling for alle komponentene i ordren.</span><span class="sxs-lookup"><span data-stu-id="33394-176">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="33394-177">Nå opprettes og lagres bestillingene som de siste bestillingene i bestillingsoversikten.</span><span class="sxs-lookup"><span data-stu-id="33394-177">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="33394-178">Planlegge en overføringsordre for å dekke salgsbehov</span><span class="sxs-lookup"><span data-stu-id="33394-178">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="33394-179">I denne fremgangsmåten skal du planlegge for behov fra en ordre.</span><span class="sxs-lookup"><span data-stu-id="33394-179">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="33394-180">Behovslinjer representerer salgslinjer, ikke komponentlinjer som i produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="33394-180">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="33394-181">Slik planlegger du en overføringsordre for å dekke salgsbehov:</span><span class="sxs-lookup"><span data-stu-id="33394-181">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="33394-182">Flytt pekeren til planleggingslinjen for ordrenummer **2008**.</span><span class="sxs-lookup"><span data-stu-id="33394-182">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="33394-183">Vis linjen, og flytt pekeren til behovslinjen.</span><span class="sxs-lookup"><span data-stu-id="33394-183">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="33394-184">Ordrenummer **2008** er for ti høyttalere, varen **LS-120**, som er bestilt av Pedersen Kontorutstyr AS.</span><span class="sxs-lookup"><span data-stu-id="33394-184">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="33394-185">Definert etterfyllingssystem og standardleverandør for varen vises.</span><span class="sxs-lookup"><span data-stu-id="33394-185">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="33394-186">Det er fire informasjonsfelt nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="33394-186">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="33394-187">I feltet **Tidligste tilgjengelige dato** blir de ti stykkene som trengs, tilgjengelige på en inngående forsyningsordre ni dager senere enn gjeldende forfallsdato.</span><span class="sxs-lookup"><span data-stu-id="33394-187">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="33394-188">Hvis dette blir for sent for kunden, viser feltet **Tilgjengelig for overføring** at 13 stykker av varen er tilgjengelig på en annen lokasjon.</span><span class="sxs-lookup"><span data-stu-id="33394-188">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="33394-189">Det er aktuelt å planlegge for denne varebeholdningen.</span><span class="sxs-lookup"><span data-stu-id="33394-189">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="33394-190">Velg feltet **Tilgjengelig for overføring** for å åpne siden **Hent alternativ forsyning**.</span><span class="sxs-lookup"><span data-stu-id="33394-190">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="33394-191">Velg **OK**-knappen for å bestille de ti varene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="33394-191">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="33394-192">På behovslinjen er det foreslåtte kjøpet erstattet med en en overføring fra lokasjonen GRØNN.</span><span class="sxs-lookup"><span data-stu-id="33394-192">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="33394-193">Funksjonen **Lag bestillinger** oppretter en overføringsordre fra GRØNN til den etterspurte lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="33394-193">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="33394-194">**Erstatning finnes**-feltet fungerer på samme måte.</span><span class="sxs-lookup"><span data-stu-id="33394-194">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="33394-195">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="33394-195">Choose the **Make Orders** action.</span></span> <span data-ttu-id="33394-196">Siden **Lag forsyningsordrer** åpnes.</span><span class="sxs-lookup"><span data-stu-id="33394-196">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="33394-197">På hurtigfanen **Ordreplanlegging**, i feltet **Lag ordrer for**, velger du alternativet **Den aktive ordren**.</span><span class="sxs-lookup"><span data-stu-id="33394-197">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="33394-198">Velg alternativet **Lag overføringsordrer** i feltet **Opprett overføringsordre** på hurtigfanen **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="33394-198">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="33394-199">Velg **OK**-knappen for å opprette overføringsordren som skal forsyne ordren.</span><span class="sxs-lookup"><span data-stu-id="33394-199">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="33394-200">Overføringsordren er nå opprettet og lagret i oversikten som den siste ordren i oversikten over åpne overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="33394-200">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="33394-201">Planlegge en produksjonsordre med flere nivåer for å dekke et salgsbehov</span><span class="sxs-lookup"><span data-stu-id="33394-201">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="33394-202">I denne fremgangsmåten skal du planlegge å dekke salgsbehov for en produsert vare med flere produktnivåer, der hvert nivå skaper et avhengig produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="33394-202">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="33394-203">Slik planlegger du produksjon med flere nivåer for å dekke salgsbehov:</span><span class="sxs-lookup"><span data-stu-id="33394-203">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="33394-204">Merk planleggingslinjen med salgsbehov for ordrenummer **1001**, opprettet tidligere som nødvendige data.</span><span class="sxs-lookup"><span data-stu-id="33394-204">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="33394-205">Denne behovslinjen er en salgslinje, men varen har **Prod.ordre** som definert etterfyllingssystem.</span><span class="sxs-lookup"><span data-stu-id="33394-205">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="33394-206">Begynn med å legge til en ekstra ringeklokke i komponentbehovet for hver sykkel.</span><span class="sxs-lookup"><span data-stu-id="33394-206">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="33394-207">Velg handlingen **Komponenter** for å åpne **Planleggingskomponenter**-siden.</span><span class="sxs-lookup"><span data-stu-id="33394-207">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="33394-208">På linjen med varen ringeklokke endrer du **Antall per**-feltet fra **1** til **2**.</span><span class="sxs-lookup"><span data-stu-id="33394-208">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="33394-209">Vurder planleggingsalternativene på siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-209">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="33394-210">I dette tilfellet har du ingen alternative forsyningsmuligheter, ingen overføring, erstatning eller senere levering.</span><span class="sxs-lookup"><span data-stu-id="33394-210">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="33394-211">Du må opprette den foreslåtte forsyningsordren – en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="33394-211">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="33394-212">Velg **Lag ordre**-handlingen for å opprette produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="33394-212">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="33394-213">Legg merke til at planleggingslinjen for ordre **1001** på siden **Ordreplanlegging** ikke lenger finnes, og at det opprinnelige salgsbehovet er dekket.</span><span class="sxs-lookup"><span data-stu-id="33394-213">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="33394-214">Lukk siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-214">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="33394-215">Nå kunne du ha valgt å fortsette i denne visningen og fylle ut alle planleggingsoppgavene.</span><span class="sxs-lookup"><span data-stu-id="33394-215">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="33394-216">I stedet skal du nå ta på deg rollen som produksjonsplanlegger ved å gå til produksjonsordren du nettopp opprettet, og åpne siden **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-216">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="33394-217">Som produksjonsplanlegger må du nå planlegge en bestemt produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="33394-217">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="33394-218">Slik planlegger du en bestemt produksjonsordre:</span><span class="sxs-lookup"><span data-stu-id="33394-218">To plan a specific production order</span></span>  

1.  <span data-ttu-id="33394-219">Åpne produksjonsordren **101001**, for ti sykler, som du nettopp opprettet med funksjonen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="33394-219">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="33394-220">Åpne siden **Prod.ordrekomponenter** for å kontrollere at den ekstra ringeklokken gjenspeiles på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="33394-220">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="33394-221">Velg handlingen **Planlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-221">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="33394-222">Siden **Ordreplanlegging** åpnes i en visning som alltid er filtrert etter bestemte produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="33394-222">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="33394-223">Salgsbehov vises ikke.</span><span class="sxs-lookup"><span data-stu-id="33394-223">Sales demand is not displayed.</span></span> <span data-ttu-id="33394-224">Du må beregne en plan før du kan vise ytterligere behov.</span><span class="sxs-lookup"><span data-stu-id="33394-224">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="33394-225">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="33394-225">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="33394-226">Legg merke til at fire nye produksjonsordrer vises som ikke-planlagt produksjonsbehov som er hentet fra ordre **101001**.</span><span class="sxs-lookup"><span data-stu-id="33394-226">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="33394-227">De nye linjene representerer produksjonsbehov fra delmonteringene som må opprettes for å produsere ordren.</span><span class="sxs-lookup"><span data-stu-id="33394-227">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="33394-228">Velg **Utvid alle**-handlingen for å få en oversikt over alt produksjonsbehov for de to produksjonsordrene.</span><span class="sxs-lookup"><span data-stu-id="33394-228">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="33394-229">For å gi tilleggsinformasjon om behovslinjene kan du legge til feltene **Behovsmengde** og **Disponibel behovsmengde** i visningen.</span><span class="sxs-lookup"><span data-stu-id="33394-229">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="33394-230">Nå må du forsyne ti av hver komponent.</span><span class="sxs-lookup"><span data-stu-id="33394-230">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="33394-231">Merk at fire av behovslinjene har Prod.ordre. fra etterfyllingssystemet.</span><span class="sxs-lookup"><span data-stu-id="33394-231">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="33394-232">Disse fire delmonteringene representerer sykkelens andre produktnivå.</span><span class="sxs-lookup"><span data-stu-id="33394-232">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="33394-233">Standardinnstillingene for etterfylling er allerede fylt ut, og du kan begynne å lage bestillinger.</span><span class="sxs-lookup"><span data-stu-id="33394-233">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="33394-234">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="33394-234">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="33394-235">Før du velger **OK**-knappen, må du legge merke til teksten i hurtigfanen **Ordreplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="33394-235">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="33394-236">Denne teksten er viktig fordi du vet at sykkelen har flere produserte komponenter, delmonteringer, som kan være etterspurt når du oppretter denne produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="33394-236">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="33394-237">Velg alternativet **Alle linjer** i feltet **Lag ordrer for** på siden **Lag forsyningsordrer**, og klikk deretter **OK** for å opprette produksjonsordrer for det andre produktnivået i ordren.</span><span class="sxs-lookup"><span data-stu-id="33394-237">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="33394-238">Merk at produksjonsbehovet på øverste nivå for produksjonsordren 101001 ikke lenger finnes.</span><span class="sxs-lookup"><span data-stu-id="33394-238">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="33394-239">Dette betyr at det er planlagt for det opprinnelige produksjonsbehovet for delmonteringer.</span><span class="sxs-lookup"><span data-stu-id="33394-239">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="33394-240">På siden **Ordreplanlegging** beregner du en plan på nytt for å planlegge sykkelstrukturen.</span><span class="sxs-lookup"><span data-stu-id="33394-240">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="33394-241">Velg **Beregn plan**-handlingen for å beregne planen på nytt i henhold til instruksjonene i den innebygde hjelpeteksten.</span><span class="sxs-lookup"><span data-stu-id="33394-241">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="33394-242">De to nye linjene representerer ytterligere produksjonsbehov hentet fra delmonteringene som ble planlagt i forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="33394-242">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="33394-243">Det blir foreslått at du lager to produksjonsordrer for å forsyne hjulnavene, én for ti fornav og én for ti baknav.</span><span class="sxs-lookup"><span data-stu-id="33394-243">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="33394-244">Velg **Utvid alle**-handlingen for å få en oversikt over alt behov for de to produksjonsordrene.</span><span class="sxs-lookup"><span data-stu-id="33394-244">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="33394-245">Den foreslåtte forsyningsplanen angir at i alt fire bestillinger blir opprettet for komponentene.</span><span class="sxs-lookup"><span data-stu-id="33394-245">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="33394-246">Du bestemmer deg for å lage de foreslåtte bestillingene.</span><span class="sxs-lookup"><span data-stu-id="33394-246">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="33394-247">Velg handlingen **Lag bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="33394-247">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="33394-248">Velg alternativet **Alle linjer** i feltet **Lag ordrer for**, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="33394-248">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="33394-249">Kontroller om det finnes ytterligere behov for produksjonen av den overordnede varen, sykkelen, som selges i ordre 1001.</span><span class="sxs-lookup"><span data-stu-id="33394-249">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="33394-250">Velg **Beregn plan**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="33394-250">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="33394-251">Meldingen angir at alle nødvendige varer nå er forsynt.</span><span class="sxs-lookup"><span data-stu-id="33394-251">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="33394-252">Kontroller de fast planlagte produksjonsordrene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="33394-252">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="33394-253">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Fast planlagte prod.ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="33394-253">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="33394-254">Se gjennom hvordan start- og sluttidspunkt for individuelle ordrer planlegges i henhold til produktstrukturen, på siden **Fast planlagte prod.ordrer**.</span><span class="sxs-lookup"><span data-stu-id="33394-254">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="33394-255">Komponentene på laveste nivå produseres først.</span><span class="sxs-lookup"><span data-stu-id="33394-255">The lowest-level components are produced first.</span></span> <span data-ttu-id="33394-256">Derfor må du planlegge ordrer med flere nivåer slik det er demonstrert i denne arbeidsflyten for planlegging.</span><span class="sxs-lookup"><span data-stu-id="33394-256">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33394-257">Se også</span><span class="sxs-lookup"><span data-stu-id="33394-257">See Also</span></span>  
 <span data-ttu-id="33394-258">[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="33394-258">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="33394-259">Gjennomgang: planlegge forsyninger automatisk</span><span class="sxs-lookup"><span data-stu-id="33394-259">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

