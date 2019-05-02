---
title: Beregne ordrebekreftelsesdatoer | Microsoft-dokumentasjon
description: Ordrebekreftelsesfunksjonen er et verktøy for beregning av når en vare tidligst kan leveres. Den oppretter i tillegg forslagslinjer for datoene du godtar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/23/2018
ms.author: sgroespe
ms.openlocfilehash: 2b1eae5f8562999f3fca227b6de6778ef1c5374e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802696"
---
# <a name="calculate-order-promising-dates"></a><span data-ttu-id="ca435-104">Beregne ordrebekreftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="ca435-104">Calculate Order Promising Dates</span></span>
<span data-ttu-id="ca435-105">Et firma må være i stand til å informere kundene om ordreleveringsdatoer.</span><span class="sxs-lookup"><span data-stu-id="ca435-105">A company must be able to inform their customers of order delivery dates.</span></span> <span data-ttu-id="ca435-106">På siden **Ordrebekreftelseslinjer** kan du gjøre dette fra en salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="ca435-106">The **Order Promising Lines** page enables you to do this from a sales order line.</span></span>  

<span data-ttu-id="ca435-107">Basert på en vares kjente og forventede tilgjengelighetsdatoer beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] forsendelses- og leveringsdato på et øyeblikk, som deretter kan loves kunden.</span><span class="sxs-lookup"><span data-stu-id="ca435-107">Based on an item’s known and expected availability dates, [!INCLUDE[d365fin](includes/d365fin_md.md)] instantly calculates shipment and delivery dates, which can then be promised to the customer.</span></span>  

<span data-ttu-id="ca435-108">Hvis du angir en ønsket leveringsdato på en ordrelinje, brukes denne datoen som utgangspunkt for følgende beregninger:</span><span class="sxs-lookup"><span data-stu-id="ca435-108">If you specify a requested delivery date on a sales order line, then that date is used as the starting point for the following calculations:</span></span>  

- <span data-ttu-id="ca435-109">ønsket leveringsdato - leveringstid = planlagt forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-109">requested delivery date - shipping time = planned shipment date</span></span>  
- <span data-ttu-id="ca435-110">planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-110">planned shipment date - outbound whse. handling time = shipment date</span></span>  

<span data-ttu-id="ca435-111">Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette.</span><span class="sxs-lookup"><span data-stu-id="ca435-111">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="ca435-112">Hvis ikke varene er tilgjengelige for plukking på forsendelsesdatoen, vises en advarsel om at det er tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="ca435-112">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>  

<span data-ttu-id="ca435-113">Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på.</span><span class="sxs-lookup"><span data-stu-id="ca435-113">If you do not specify a requested delivery date on a sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="ca435-114">Denne datoen angis deretter i feltet **Forsendelsesdato** på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="ca435-114">That date is then entered in the **Shipment Date** field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following calculations:</span></span>  

- <span data-ttu-id="ca435-115">forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-115">shipment date + outbound whse. handling time = planned shipment date</span></span>  
- <span data-ttu-id="ca435-116">planlagt forsendelsesdato + leveringstid = planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="ca435-116">planned shipment date + shipping time = planned delivery date</span></span>  

## <a name="about-order-promising"></a><span data-ttu-id="ca435-117">Om ordrebekreftelse</span><span class="sxs-lookup"><span data-stu-id="ca435-117">About Order Promising</span></span>
<span data-ttu-id="ca435-118">Med funksjonen for ordrebekreftelse kan du gi løfte om at en ordre skal leveres en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="ca435-118">The Order Promising functionality enables you to promise an order to be shipped or delivered on a specific date.</span></span> <span data-ttu-id="ca435-119">Datoen da en vare er tilgjengelig for ordre (ATP) eller varens første mulige forsendelsesdato (CTP) beregnes, og ordrelinjer opprettes for disse datoene som du godtar.</span><span class="sxs-lookup"><span data-stu-id="ca435-119">The date that an item is available to promise or capable to promise is calculated, and order lines are created for those dates that you accept.</span></span> <span data-ttu-id="ca435-120">Funksjonen beregner når en vare tidligst kan leveres.</span><span class="sxs-lookup"><span data-stu-id="ca435-120">The functionality calculates the earliest possible date that an item is available for shipment or delivery.</span></span> <span data-ttu-id="ca435-121">Den oppretter i tillegg forslagslinjer, i tilfelle varene først må kjøpes for datoene du godtar.</span><span class="sxs-lookup"><span data-stu-id="ca435-121">It also creates requisition lines, in case the items must first be purchases, for those dates that you accept.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ca435-122">bruker to grunnleggende begreper:</span><span class="sxs-lookup"><span data-stu-id="ca435-122">uses two fundamental concepts:</span></span>  

- <span data-ttu-id="ca435-123">Tilgjengelig for ordre (ATP)</span><span class="sxs-lookup"><span data-stu-id="ca435-123">Available to Promise (ATP)</span></span>  
- <span data-ttu-id="ca435-124">Første mulige forsendelsesdato (CTP)</span><span class="sxs-lookup"><span data-stu-id="ca435-124">Capable to Promise (CTP)</span></span>  

### <a name="available-to-promise"></a><span data-ttu-id="ca435-125">Tilgjengelig for ordre (ATP)</span><span class="sxs-lookup"><span data-stu-id="ca435-125">Available to Promise</span></span>  
<span data-ttu-id="ca435-126">Tilgjengelig for ordre (ATP) beregner datoer basert på reservasjonssystemet.</span><span class="sxs-lookup"><span data-stu-id="ca435-126">Available to promise (ATP) calculates dates based on the reservation system.</span></span> <span data-ttu-id="ca435-127">Den utfører en tilgjengelighetskontroll for de ureserverte antallene på lager i forhold til planlagt produksjon, kjøp, overføringer og ordrereturer.</span><span class="sxs-lookup"><span data-stu-id="ca435-127">It performs an availability check of the unreserved quantities in inventory with regard to planned production, purchases, transfers, and sales returns.</span></span> <span data-ttu-id="ca435-128">Basert på denne informasjonen beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk leveringsdatoen for kundens ordre fordi varene er tilgjengelige, enten på lager eller i planlagte mottak.</span><span class="sxs-lookup"><span data-stu-id="ca435-128">Based on this information, [!INCLUDE[d365fin](includes/d365fin_md.md)] automatically calculates the delivery date of the customer’s order because the items are available, either in inventory or on planned receipts.</span></span>  

### <a name="capable-to-promise"></a><span data-ttu-id="ca435-129">Første mulige forsendelsesdato (CTP)</span><span class="sxs-lookup"><span data-stu-id="ca435-129">Capable to Promise</span></span>  
<span data-ttu-id="ca435-130">Første mulige forsendelsesdato (CTP) forutsetter et "Hva om"-scenario som bare gjelder for vareantall som ikke er på lager eller på planlagte ordrer.</span><span class="sxs-lookup"><span data-stu-id="ca435-130">Capable to promise (CTP) assumes a “what if” scenario, which only applies to item quantities that are not in inventory or on scheduled orders.</span></span> <span data-ttu-id="ca435-131">Basert på dette scenariet beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] den tidligste datoen varen kan være tilgjengelig, hvis den skal produseres, kjøpes eller overføres.</span><span class="sxs-lookup"><span data-stu-id="ca435-131">Based on this scenario, [!INCLUDE[d365fin](includes/d365fin_md.md)] calculates the earliest date that the item can be available if it is to be produced, purchased, or transferred.</span></span>

#### <a name="example"></a><span data-ttu-id="ca435-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ca435-132">Example</span></span>
<span data-ttu-id="ca435-133">Hvis det er en bestilling på ti enheter og seks stykker er tilgjengelige på lageret eller i tidsplanlagte ordrer, baseres beregningen for første mulige forsendelsesdato på fire enheter.</span><span class="sxs-lookup"><span data-stu-id="ca435-133">If there is an order for 10 pieces, and 6 pieces are available in inventory or on scheduled orders, then the Capable-to-Promise calculation will be based on 4 pieces.</span></span>

### <a name="calculations"></a><span data-ttu-id="ca435-134">Beregninger</span><span class="sxs-lookup"><span data-stu-id="ca435-134">Calculations</span></span>  
<span data-ttu-id="ca435-135">Når [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner kundens leveringsdato, utføres to oppgaver:</span><span class="sxs-lookup"><span data-stu-id="ca435-135">When [!INCLUDE[d365fin](includes/d365fin_md.md)] calculates the customer’s delivery date, it performs two tasks:</span></span>  

- <span data-ttu-id="ca435-136">Beregner den tidligste leveringsdatoen når kunden ikke har bedt om en bestemt leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="ca435-136">Calculates the earliest delivery date when the customer has not requested a specific delivery date.</span></span>  
- <span data-ttu-id="ca435-137">Kontrollerer om leveringsdatoen som kunden har bedt om, eller som du har lovet kunden, er realistisk.</span><span class="sxs-lookup"><span data-stu-id="ca435-137">Verifies if the delivery date requested by the customer or promised to the customer is realistic.</span></span>  

<span data-ttu-id="ca435-138">Hvis kunden ikke ber om en bestemt leveringsdato, brukes arbeidsdatoen som leveringsdato, og tilgjengelighet baseres deretter på denne datoen.</span><span class="sxs-lookup"><span data-stu-id="ca435-138">If the customer does not request a specific delivery date, the shipment date is set to equal the work date, and availability is then based on that date.</span></span> <span data-ttu-id="ca435-139">Hvis varen er på lager, beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] fremover i tid for å fastsette når ordren kan leveres.</span><span class="sxs-lookup"><span data-stu-id="ca435-139">If the item is in inventory, [!INCLUDE[d365fin](includes/d365fin_md.md)] calculates forward in time to determine when the order can be delivered.</span></span> <span data-ttu-id="ca435-140">Dette kan gjøres med følgende formler:</span><span class="sxs-lookup"><span data-stu-id="ca435-140">This is accomplished by the following formulas:</span></span>  

- <span data-ttu-id="ca435-141">Forsendelsesdato + Utgående lagerhåndtering = Planlagt forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-141">Shipment Date + Outbound Warehouse Handling Time = Planned Shipment Date</span></span>  
- <span data-ttu-id="ca435-142">Planlagt forsendelsesdato + Leveringstid = Planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="ca435-142">Planned Shipment Date + Shipping Time = Planned Delivery Date</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ca435-143">kontrollerer deretter om beregnet leveringsdato er realistisk ved å beregne bakover i tid, for å bestemme når varen må være tilgjengelig for å overholde datoen som ble lovet.</span><span class="sxs-lookup"><span data-stu-id="ca435-143">then verifies if the calculated delivery date is realistic by calculating backward in time to determine when the item must be available to meet the promised date.</span></span> <span data-ttu-id="ca435-144">Dette kan gjøres med følgende formler:</span><span class="sxs-lookup"><span data-stu-id="ca435-144">This is accomplished by the following formulas:</span></span>  

- <span data-ttu-id="ca435-145">Planlagt forsendelsesdato - Leveringstid = Planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="ca435-145">Planned Delivery Date - Shipping Time = Planned Shipment Date</span></span>  
- <span data-ttu-id="ca435-146">Planlagt forsendelsesdato - Utgående lagerhåndteringstid = Forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-146">Planned Shipment Date - Outbound Warehouse Handling = Shipment Date</span></span>  

<span data-ttu-id="ca435-147">Leveringsdatoen brukes til å utføre tilgjengelighetskontrollen.</span><span class="sxs-lookup"><span data-stu-id="ca435-147">The shipment date is used to make the availability check.</span></span> <span data-ttu-id="ca435-148">Hvis varen er tilgjengelig på denne datoen, bekrefter [!INCLUDE[d365fin](includes/d365fin_md.md)] at forespurt/lovet levering kan innfris ved å angi at planlagt leveringsdato skal være lik forespurt/lovet leveringsdato.</span><span class="sxs-lookup"><span data-stu-id="ca435-148">If the item is available on this date, [!INCLUDE[d365fin](includes/d365fin_md.md)] confirms that therequested/promised delivery can be met by setting the planned delivery date to equal the requested/promised delivery date.</span></span> <span data-ttu-id="ca435-149">Hvis varen ikke er tilgjengelig, returneres en tom dato, og ordrebehandleren kan deretter bruke CTP-funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="ca435-149">If the item is unavailable, it returns a blank date and the order processor can then use the CTP functionality.</span></span>  

<span data-ttu-id="ca435-150">Basert på nye datoer og klokkeslett beregnes alle relaterte datoer i henhold til formlene som er oppført tidligere i denne delen.</span><span class="sxs-lookup"><span data-stu-id="ca435-150">Based on new dates and times, all related dates are calculated according to the formulas listed earlier in this section.</span></span> <span data-ttu-id="ca435-151">CTP-beregningen tar lengre tid, men den gir en nøyaktig dato for når kunden kan forvente å få varen levert.</span><span class="sxs-lookup"><span data-stu-id="ca435-151">The CTP calculation takes longer but it gives an accurate date when the customer can expect to have the item delivered.</span></span> <span data-ttu-id="ca435-152">Datoene som er beregnes fra CTP, vises i feltene **Planlagt lev.dato** og **Tidligste forsendelsesdato** på siden **Ordrebekreftelseslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ca435-152">The dates that are calculated from CTP are presented in the **Planned Delivery Date** and **Earliest Shipment Date** fields on the **Order Promising Lines** page.</span></span>  

<span data-ttu-id="ca435-153">Ordrebehandleren fullfører CTP-prosessen ved å godta datoene.</span><span class="sxs-lookup"><span data-stu-id="ca435-153">The order processor finishes the CTP process by accepting the dates.</span></span> <span data-ttu-id="ca435-154">Dette betyr at en planleggingslinje og en reservasjonspost opprettes for varen før de beregnede datoene for å sikre at ordren blir dekket.</span><span class="sxs-lookup"><span data-stu-id="ca435-154">This means that a planning line and a reservation entry are created for the item before the calculated dates to ensure that the order is fulfilled.</span></span>  

<span data-ttu-id="ca435-155">I tillegg til den eksterne ordrebekreftelsen som du kan utføre på siden **Ordrebekreftelseslinjer**, kan du også bekrefte interne eller eksterne leveringsdatoer for stykklistevarer.</span><span class="sxs-lookup"><span data-stu-id="ca435-155">In addition to the external order promising that you can perform on the **Order Promising Lines** page, you can also promise internal or external delivery dates for bill-of-material items.</span></span> <span data-ttu-id="ca435-156">Hvis du vil ha mer informasjon, kan du se [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ca435-156">For more information, see [View the Availability of Items](inventory-how-availability-overview.md).</span></span>

## <a name="to-set-up-order-promising"></a><span data-ttu-id="ca435-157">Slik angir du ordrebekreftelser</span><span class="sxs-lookup"><span data-stu-id="ca435-157">To set up order promising</span></span>  
1. <span data-ttu-id="ca435-158">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for ordrebekreftelse**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Promising Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ca435-159">Angi et nummer og en tidsenhetskode i feltet **Iverksett (tid)**.</span><span class="sxs-lookup"><span data-stu-id="ca435-159">Enter a number and time unit code in the **Offset(Time)** field.</span></span> <span data-ttu-id="ca435-160">Velg én av følgende koder.</span><span class="sxs-lookup"><span data-stu-id="ca435-160">Select one of the following codes.</span></span>  

    |<span data-ttu-id="ca435-161">Kode</span><span class="sxs-lookup"><span data-stu-id="ca435-161">Code</span></span>|<span data-ttu-id="ca435-162">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ca435-162">Description</span></span>|  
    |----------|-----------------|  
    |<span data-ttu-id="ca435-163">**d**</span><span class="sxs-lookup"><span data-stu-id="ca435-163">**d**</span></span>|<span data-ttu-id="ca435-164">Kalenderdag</span><span class="sxs-lookup"><span data-stu-id="ca435-164">Calendar day</span></span>|  
    |<span data-ttu-id="ca435-165">**a**</span><span class="sxs-lookup"><span data-stu-id="ca435-165">**w**</span></span>|<span data-ttu-id="ca435-166">Uke</span><span class="sxs-lookup"><span data-stu-id="ca435-166">Week</span></span>|  
    |<span data-ttu-id="ca435-167">**m**</span><span class="sxs-lookup"><span data-stu-id="ca435-167">**m**</span></span>|<span data-ttu-id="ca435-168">Måned</span><span class="sxs-lookup"><span data-stu-id="ca435-168">Month</span></span>|  
    |<span data-ttu-id="ca435-169">**k**</span><span class="sxs-lookup"><span data-stu-id="ca435-169">**q**</span></span>|<span data-ttu-id="ca435-170">Kvartal</span><span class="sxs-lookup"><span data-stu-id="ca435-170">Quarter</span></span>|  
    |<span data-ttu-id="ca435-171">**å**</span><span class="sxs-lookup"><span data-stu-id="ca435-171">**y**</span></span>|<span data-ttu-id="ca435-172">År</span><span class="sxs-lookup"><span data-stu-id="ca435-172">Year</span></span>|  

    <span data-ttu-id="ca435-173">"3u" betyr for eksempel at Iverksett (tid) er tre uker.</span><span class="sxs-lookup"><span data-stu-id="ca435-173">For example, "3w" indicates that the offset time is three weeks.</span></span> <span data-ttu-id="ca435-174">Bruk "n" som prefiks til en av disse kodene for å angi nåværende periode.</span><span class="sxs-lookup"><span data-stu-id="ca435-174">To indicate the current period, prefix to any of these codes with the letter “c”.</span></span> <span data-ttu-id="ca435-175">Hvis du for eksempel vil at Iverksett (tid) skal være nåværende måned, angir du **nm**.</span><span class="sxs-lookup"><span data-stu-id="ca435-175">For example, if you want the offset time to be the current month, enter **cm**.</span></span>  
3. <span data-ttu-id="ca435-176">Angi en nummerserie i feltet **Ordrebekreftelsesnr.** ved å velge en linje fra listen på siden **Nr. serie**.</span><span class="sxs-lookup"><span data-stu-id="ca435-176">Enter a number series in the **Order Promising Nos.** field by selecting a line from the list on the **No. Series** page.</span></span>  
4. <span data-ttu-id="ca435-177">Angi en ordrebekreftelsesmal i feltet **Ordrebekreftelsesmal** ved å velge en linje fra oversikten på siden **Best.forslagsmal - oversikt**.</span><span class="sxs-lookup"><span data-stu-id="ca435-177">Enter an order promising template in the **Order Promising Template** field by selecting a line from the list on the **Req. Worksheet Template List** page.</span></span>  
5. <span data-ttu-id="ca435-178">Angi et bestillingsforslag i feltet **Ordrebekreftelsesskjema** ved å velge en linje fra oversikten på siden **Best.forslagsnavn**.</span><span class="sxs-lookup"><span data-stu-id="ca435-178">Enter a requisition worksheet in the **Order Promising Worksheet** field by selecting a line from the list on the **Req. Wksh. Names** page.</span></span>

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-page"></a><span data-ttu-id="ca435-179">Slik angir du inngående lagerhåndteringstid i lageroppsettsiden</span><span class="sxs-lookup"><span data-stu-id="ca435-179">To enter inbound warehouse handling time in the inventory setup page</span></span>  
<span data-ttu-id="ca435-180">Hvis du vil at lagerhåndteringstid skal tas med i beregningen av ordrebekreftelse på bestillingslinjen, kan du definere den som standard for lageret og lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="ca435-180">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory and for your location.</span></span>    
1. <span data-ttu-id="ca435-181">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageroppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-181">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ca435-182">På hurtigfanen **Generelt** i feltet **Inngående lagerhåndteringstid** angir du hvor mange dager som skal tas med i beregningen av ordrebekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="ca435-182">On the **General** FastTab, in the **Inbound Whse. Handling Time** field, enter the number of days that you want to include in the order promising calculation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ca435-183">Hvis du har fylt ut feltet **Inngående lagerhåndteringstid** på **lokasjonskortet** for lokasjonen, brukes dette feltet som standard for inngående lagerhåndteringstid.</span><span class="sxs-lookup"><span data-stu-id="ca435-183">If you have filled in the **Inbound Whse. Handling Time** field on the **Location Card** for your location this field is used as the default inbound warehouse handling time.</span></span>  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a><span data-ttu-id="ca435-184">Slik angir du inngående lagerhåndteringstid på lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="ca435-184">To enter inbound warehouse handling time on location cards</span></span>  
1. <span data-ttu-id="ca435-185">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjon**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-185">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca435-186">Åpne det aktuelle lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="ca435-186">Open the relevant location card.</span></span>  
3.  <span data-ttu-id="ca435-187">På hurtigfanen **Lager** i feltet **Inngående lagerhåndteringstid** angir du hvor mange dager som skal tas med i beregningen av ordrebekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="ca435-187">On the **Warehouse** FastTab, in the **Inbound Whse. Handling Time** field, enter the number of days that you want to be included in the order promising calculation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ca435-188">Hvis du lar feltet **Inngående lagerhåndteringstid** stå tomt, brukes verdien på **Lageroppsett**-siden i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ca435-188">If you leave the **Inbound Whse. Handling Time** field blank, then the calculation uses the value in the **Inventory Setup**  page.</span></span>

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-page"></a><span data-ttu-id="ca435-189">Slik angir du utgående lagerhåndteringstid på lageroppsettsiden</span><span class="sxs-lookup"><span data-stu-id="ca435-189">To enter outbound warehouse handling time in the inventory setup page</span></span>  
<span data-ttu-id="ca435-190">Hvis du vil definere en utgående lagerhåndteringstid slik at den tas med i beregningen av ordrebekreftelsen på salgslinjen, kan du definere dette som standard for lageret.</span><span class="sxs-lookup"><span data-stu-id="ca435-190">If you want to set up an outbound warehouse handling time to be included in the order promising calculation on the sales line, you can set this up as a default for the inventory.</span></span>

1. <span data-ttu-id="ca435-191">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageroppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-191">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ca435-192">På hurtigfanen **Generelt** i feltet **Utgående lagerhåndteringstid** angir du hvor mange dager som skal tas med i beregningen av ordrebekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="ca435-192">On the **General** FastTab, in the **Outbound Whse. Handling Time** field, enter the number of days you want to include in the order promising calculation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ca435-193">Hvis du har fylt ut feltet **Utgående lagerhåndteringstid** på lokasjonskortet for lokasjonen, brukes dette feltet som standard for utgående lagerhåndteringstid.</span><span class="sxs-lookup"><span data-stu-id="ca435-193">If you have filled in the **Outbound Whse. Handling Time** field on the Location card for your location, this field is used as the default outbound warehouse handling time.</span></span>  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a><span data-ttu-id="ca435-194">Slik angir du utgående lagerhåndteringstid på lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="ca435-194">To enter outbound warehouse handling time on location cards</span></span>  
1.  <span data-ttu-id="ca435-195">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-195">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca435-196">Åpne det aktuelle lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="ca435-196">Open the relevant location card.</span></span>  
3.  <span data-ttu-id="ca435-197">På hurtigfanen **Lager** i feltet **Utgående lagerhåndteringstid** angir du hvor mange dager som skal tas med i beregningen av ordrebekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="ca435-197">On the **Warehouse** FastTab, in the **Outbound Whse. Handling Time** field, enter the number of days that you want to include in the order promising calculation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ca435-198">Hvis du lar feltet **Utgående lagerhåndteringstid** stå tomt, brukes verdien på **Lageroppsett**-siden i beregningen.</span><span class="sxs-lookup"><span data-stu-id="ca435-198">If you leave the **Outbound Whse. Handling Time** field blank, then the calculation uses the value in the **Inventory Setup**  page.</span></span>

## <a name="to-make-an-item-critical"></a><span data-ttu-id="ca435-199">Slik gjør du en vare kritisk</span><span class="sxs-lookup"><span data-stu-id="ca435-199">To make an item critical</span></span>  
<span data-ttu-id="ca435-200">Før en vare kan inkluderes i beregningen av ordrebekreftelsen, må den være merket som kritisk.</span><span class="sxs-lookup"><span data-stu-id="ca435-200">Before an item can be included in the order promising calculation, it must be marked as critical.</span></span> <span data-ttu-id="ca435-201">Dette oppsettet sikrer at ikke-kritiske varer ikke fører til uaktuell beregning av ordrebekreftelser.</span><span class="sxs-lookup"><span data-stu-id="ca435-201">This setup ensures that non-critical items do not cause irrelevant order promising calculations.</span></span>   
1.  <span data-ttu-id="ca435-202">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-202">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca435-203">Åpne det aktuelle varekortet.</span><span class="sxs-lookup"><span data-stu-id="ca435-203">Open the relevant item card.</span></span>  
3.  <span data-ttu-id="ca435-204">På hurtifganen **Planlegging** velger du **Kritisk**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ca435-204">On the **Planning** FastTab, select the **Critical** field.</span></span>  

## <a name="to-calculate-an-order-promising-date"></a><span data-ttu-id="ca435-205">Slik beregner du en ordrebekreftelsesdato</span><span class="sxs-lookup"><span data-stu-id="ca435-205">To calculate an order promising date</span></span>  
1.  <span data-ttu-id="ca435-206">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ca435-206">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca435-207">Åpne den aktuelle ordren, og velg ordrelinjene du vil at programmet skal beregne.</span><span class="sxs-lookup"><span data-stu-id="ca435-207">Open the relevant sales order and select the sales order lines that you want the program to calculate.</span></span>  
3.  <span data-ttu-id="ca435-208">Velg handlingen **Ordrebekreftelse** og deretter **Ordrebekreftelseslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ca435-208">Choose the **Order Promising** action, and then choose the **Order Promising Lines** action.</span></span>  
4.  <span data-ttu-id="ca435-209">Velg en linje, og velg deretter ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="ca435-209">Select a line, and then select one of the following options:</span></span>  

    - <span data-ttu-id="ca435-210">Velg **Tilgjengelig for ordre (ATP)** hvis du vil beregne når varen tidligst vil være tilgjengelig med hensyn til beholdning, tidsplanlagte mottak og bruttobehov.</span><span class="sxs-lookup"><span data-stu-id="ca435-210">Select **Available-to-Promise** if you want to calculate the earliest date that the item will be available with respect to inventory, scheduled receipts, and gross requirements.</span></span>  
    - <span data-ttu-id="ca435-211">Velg **Første mulige forsendelsesdato (CTP)** hvis du vet at varen er utsolgt fra lager og du vil beregne når varen tidligst vil være tilgjengelig når du utsteder nye etterfyllingsforslag.</span><span class="sxs-lookup"><span data-stu-id="ca435-211">Select **Capable-to-Promise** if you know that the item is presently out of stock and you want to calculate the earliest date that the item can be available by issuing new replenishment requisitions.</span></span>  
5.  <span data-ttu-id="ca435-212">Velg **Godta**-knappen for å godta den tidligste leveringsdatoen som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ca435-212">Choose the **Accept** button to accept the earliest shipment date available.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca435-213">Se også</span><span class="sxs-lookup"><span data-stu-id="ca435-213">See Also</span></span>  
[<span data-ttu-id="ca435-214">Salg</span><span class="sxs-lookup"><span data-stu-id="ca435-214">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="ca435-215">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="ca435-215">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
<span data-ttu-id="ca435-216">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca435-216">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>