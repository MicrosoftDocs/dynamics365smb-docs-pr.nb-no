---
title: Underleveranse av produksjon | Microsoft-dokumentasjon
description: Når bestillingen er opprettet fra underleverandørforslaget, kan den bokføres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: bdb9d8c0d47fe53e9e5ea310a83854e69f545d9e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802695"
---
# <a name="subcontract-manufacturing"></a><span data-ttu-id="b8275-103">Underleveranse av produksjon</span><span class="sxs-lookup"><span data-stu-id="b8275-103">Subcontract Manufacturing</span></span>
<span data-ttu-id="b8275-104">Underleveranse av valgte operasjoner til leverandør er vanlig i mange produksjonsselskaper.</span><span class="sxs-lookup"><span data-stu-id="b8275-104">Subcontracting selected operations to vendor is common in many manufacturing companies.</span></span> <span data-ttu-id="b8275-105">Underleveranse kan skje en sjelden gang eller være en vesentlig del av alle produksjonsprosesser.</span><span class="sxs-lookup"><span data-stu-id="b8275-105">Subcontracting can be a rare occurrence or can be an integral part of all production processes.</span></span>

<span data-ttu-id="b8275-106">Programmet har mange verktøy for håndtering av underleveransearbeid:</span><span class="sxs-lookup"><span data-stu-id="b8275-106">The program provides several tools for managing subcontract work:</span></span>  

- <span data-ttu-id="b8275-107">Arbeidssentre med tilordnet leverandør: Du kan bruke denne funksjonen til å definere et arbeidssenter som er tilknyttet en leverandør (underleverandør).</span><span class="sxs-lookup"><span data-stu-id="b8275-107">Work Centers with assigned vendor: This feature enables you to set up a work center that is associated with a vendor (subcontractor).</span></span> <span data-ttu-id="b8275-108">Dette kalles et arbeidssenter for underleveranse.</span><span class="sxs-lookup"><span data-stu-id="b8275-108">This is called a subcontract work center.</span></span> <span data-ttu-id="b8275-109">Du kan angi et arbeidssenter for underleveranse i en ruteoperasjon, slik at du enkelt kan behandle underleveranseaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="b8275-109">You can specify a subcontract work center on a routing operation, which allows you to easily process the subcontracted activity.</span></span> <span data-ttu-id="b8275-110">I tillegg kan operasjonskostbeløpet tildeles på rute- eller arbeidssenternivået.</span><span class="sxs-lookup"><span data-stu-id="b8275-110">In addition, the cost of the operation can be designated at the routing or the work center level.</span></span>  
- <span data-ttu-id="b8275-111">Arbeidssenterkost basert på enheter eller tid: Du kan bruke denne funksjonen til å angi om kost som er knyttet til arbeidssenteret, er basert på produksjonstiden eller på en ensartet pris per enhet.</span><span class="sxs-lookup"><span data-stu-id="b8275-111">Work Center cost based on units or time: This feature enables you to specify whether costs associated with the work center are based on the production time or a flat charge per unit.</span></span> <span data-ttu-id="b8275-112">Selv om underleverandører vanligvis bruker en ensartet pris per enhet som betaling for tjenester, kan programmet håndtere begge alternativene (produksjonstid og ensartet pris per enhet).</span><span class="sxs-lookup"><span data-stu-id="b8275-112">Although subcontractors commonly use a flat charge per unit to charge for their services, the program can handle both options (production time and flat charge per unit).</span></span>  
- <span data-ttu-id="b8275-113">Underleveranseforslag: Du kan bruke denne funksjonen til å finne produksjonsordrene med materiale som er klare til å bli sendt til en underleverandør, og til å opprette bestillinger for underleveranseoperasjoner fra produksjonsordreruter automatisk.</span><span class="sxs-lookup"><span data-stu-id="b8275-113">Subcontracting Worksheet: This feature allows you to find the production orders with material ready to send to a subcontractor and to automatically create purchase orders for subcontract operations from production order routings.</span></span> <span data-ttu-id="b8275-114">Deretter bokføres bestillingsgebyrene automatisk i produksjonsordren under bokføringen av bestillingen.</span><span class="sxs-lookup"><span data-stu-id="b8275-114">Then the program automatically posts the purchase order charges to the production order during the posting of the purchase order.</span></span> <span data-ttu-id="b8275-115">Du kan bare få tilgang til og bruke produksjonsordrer med statusen frigitt fra et underleveranseforslag.</span><span class="sxs-lookup"><span data-stu-id="b8275-115">Only production orders with a status of released can be accessed and used from a subcontracting worksheet.</span></span>  

## <a name="subcontract-work-centers"></a><span data-ttu-id="b8275-116">Arbeidssentre for underleveranse</span><span class="sxs-lookup"><span data-stu-id="b8275-116">Subcontract Work Centers</span></span>  
<span data-ttu-id="b8275-117">Arbeidssentre for underleveranse defineres på samme måte som vanlige arbeidssentre med tilleggsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="b8275-117">Subcontract Work Centers are set up the same as regular work centers with additional information.</span></span> <span data-ttu-id="b8275-118">De tilordnes ruter på samme måte som andre arbeidssentre.</span><span class="sxs-lookup"><span data-stu-id="b8275-118">They are assigned to routings in the same manner as other work centers.</span></span>  

### <a name="subcontract-work-center-fields"></a><span data-ttu-id="b8275-119">Felt i arbeidssentre for underleveranse</span><span class="sxs-lookup"><span data-stu-id="b8275-119">Subcontract Work Center Fields</span></span>  
<span data-ttu-id="b8275-120">Feltet **Underleverandørnr.** angir arbeidssenteret som et arbeidssenter for underleveranse.</span><span class="sxs-lookup"><span data-stu-id="b8275-120">This **Subcontractor No.** field designates the work center as a subcontract work center.</span></span> <span data-ttu-id="b8275-121">Du kan angi nummeret på en underleverandør som forsyner arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="b8275-121">You can enter the number of a subcontractor who supplies the work center.</span></span> <span data-ttu-id="b8275-122">Feltet kan brukes til å administrere eksterne arbeidssentre som arbeider på kontrakt.</span><span class="sxs-lookup"><span data-stu-id="b8275-122">This field can be used to administer work centers, which are not in-house but perform processing under contract.</span></span>  

<span data-ttu-id="b8275-123">Hvis du avtaler underleveranser med leverandøren med en ulik sats for hver prosess, velger du feltet **Bestemt enhetskost**.</span><span class="sxs-lookup"><span data-stu-id="b8275-123">If you subcontract with the vendor for a different rate for each process, then select the **Specific Unit Cost** field.</span></span> <span data-ttu-id="b8275-124">Dermed kan du definere en kost på hver rutelinje og sparer tiden det tar å angi hver bestilling.</span><span class="sxs-lookup"><span data-stu-id="b8275-124">This lets you set up a cost on each routing line and saves the time of re-entering each purchase order.</span></span> <span data-ttu-id="b8275-125">Kosten på rutelinjen brukes i behandling i stedet for kosten i kostfeltene i arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="b8275-125">The cost on the routing line is used in processing instead of the cost on the work center cost fields.</span></span> <span data-ttu-id="b8275-126">Når du velger feltet **Bestemt enhetskost**, beregnes kost for leverandøren i henhold til ruteoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="b8275-126">Selecting the **Specific Unit Cost** field calculates costs for the vendor by the routing operation.</span></span>  

<span data-ttu-id="b8275-127">Hvis du avtaler underleveranser med én enkelt sats per leverandør, lar du feltet **Bestemt enhetskost** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="b8275-127">If you subcontract at a single rate per vendor, leave the **Specific Unit Cost** field blank.</span></span> <span data-ttu-id="b8275-128">Kostbeløpene defineres ved å fylle ut feltene **Direkte enhetskost**, **Indirekte kost-%** og **Sats for indirekte kostnader**.</span><span class="sxs-lookup"><span data-stu-id="b8275-128">The costs will be set up by filling in **Direct Unit Cost**, **Indirect Cost %**, and **Overhead Rate** fields.</span></span>  

### <a name="routings-that-use-subcontract-work-centers"></a><span data-ttu-id="b8275-129">Ruter som bruker arbeidssentre for underleveranse</span><span class="sxs-lookup"><span data-stu-id="b8275-129">Routings that use Subcontract Work Centers</span></span>  
<span data-ttu-id="b8275-130">Arbeidssentre for underleveranse kan brukes til operasjoner i ruter på samme måte som vanlige arbeidssentre.</span><span class="sxs-lookup"><span data-stu-id="b8275-130">Subcontract work centers can be used for operations on routings in the same way as regular work centers.</span></span>  

<span data-ttu-id="b8275-131">Du kan definere en rute som bruker et eksternt arbeidssenter, som et standard operasjonstrinn.</span><span class="sxs-lookup"><span data-stu-id="b8275-131">You can set up a routing that uses an outside work center as a standard operational step.</span></span> <span data-ttu-id="b8275-132">Alternativt kan du endre ruten for en bestemt produksjonsordre for å inkludere en ekstern operasjon.</span><span class="sxs-lookup"><span data-stu-id="b8275-132">Alternatively, you can modify the routing for a particular production order to include an outside operation.</span></span> <span data-ttu-id="b8275-133">Dette kan bli nødvendig i en nødssituasjon, for eksempel hvis en server ikke fungerer riktig, eller i en midlertidig periode med høyere etterspørsel, der arbeid som vanligvis gjøres internt, må sendes til en underleverandør.</span><span class="sxs-lookup"><span data-stu-id="b8275-133">This might be needed in an emergency such as a server not working correctly, or during a temporary period of higher demand, where the work generally performed in-house must be sent to a subcontractor.</span></span>  

<span data-ttu-id="b8275-134">Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).</span><span class="sxs-lookup"><span data-stu-id="b8275-134">For more information, see [Create Routings](production-how-to-create-routings.md).</span></span>  

## <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a><span data-ttu-id="b8275-135">Beregne underleveranseforslag og opprette underleverandørbestillinger</span><span class="sxs-lookup"><span data-stu-id="b8275-135">Calculate Subcontracting Worksheets and Create Subcontract Purchase Orders</span></span>  
<span data-ttu-id="b8275-136">Når du har beregnet underleveranseforslaget, opprettes det aktuelle dokumentet, i dette tilfellet en bestilling.</span><span class="sxs-lookup"><span data-stu-id="b8275-136">Once you have calculated the subcontracting worksheet, the relevant document, in this case a purchase order, is created.</span></span>  

<span data-ttu-id="b8275-137">Siden **Underleveranseforslag** fungerer som **Planleggingsforslag** ved å beregne den nødvendige forsyningen, i dette tilfellet bestillinger, som du ser gjennom i forslaget og deretter oppretter med funksjonen **Utfør handlingsmelding**.</span><span class="sxs-lookup"><span data-stu-id="b8275-137">The **Subcontracting Worksheet** page functions like the **Planning Worksheet** by calculating the needed supply, in this case purchase orders, which you review in the worksheet and then create with the **Carry Out Action Message** function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b8275-138">Du kan bare få tilgang til og bruke produksjonsordrer med statusen **Frigitt** fra et underleveranseforslag.</span><span class="sxs-lookup"><span data-stu-id="b8275-138">Only production orders with status **Released** can be accessed and used from a subcontracting worksheet.</span></span>  

### <a name="to-calculate-the-subcontracting-worksheet"></a><span data-ttu-id="b8275-139">Slik beregner du underleveranseforslaget</span><span class="sxs-lookup"><span data-stu-id="b8275-139">To calculate the subcontracting worksheet</span></span>  
1.  <span data-ttu-id="b8275-140">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Underleveranseforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8275-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Subcontracting Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b8275-141">Hvis du vil beregne forslaget, velger du handlingen **Beregn underleveranser**.</span><span class="sxs-lookup"><span data-stu-id="b8275-141">To calculate the worksheet, choose the **Calculate Subcontracts** action.</span></span>  
3.  <span data-ttu-id="b8275-142">På siden **Beregn underleveranser** angir du filtre for underleveranseoperasjonene, eller arbeidssentrene der de utføres, for å beregne bare de relevante produksjonsordrene.</span><span class="sxs-lookup"><span data-stu-id="b8275-142">On the **Calculate Subcontracts** page, set filters for the subcontracted operations, or the work centers where they are performed, to calculate only the relevant production orders.</span></span>  
4.  <span data-ttu-id="b8275-143">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8275-143">Choose the **OK** button.</span></span>  

    <span data-ttu-id="b8275-144">Gå gjennom linjene på siden **Underleveranseforslag**.</span><span class="sxs-lookup"><span data-stu-id="b8275-144">Review the lines on the **Subcontracting Worksheet** page.</span></span> <span data-ttu-id="b8275-145">Informasjonen i dette forslaget kommer fra produksjonsordren og produksjonsordrerutelinjene og sendes til bestillingen når bestillingsdokumentet opprettes.</span><span class="sxs-lookup"><span data-stu-id="b8275-145">The information in this worksheet comes from the production order and production order routing lines and flows to the purchase order when that document is created.</span></span> <span data-ttu-id="b8275-146">Som i de andre forslagene, kan du slette en rad fra dette forslaget uten at det påvirker den opprinnelige informasjonen.</span><span class="sxs-lookup"><span data-stu-id="b8275-146">You can delete a row from the worksheet without affecting the original information, just as you can with the other worksheets.</span></span> <span data-ttu-id="b8275-147">Informasjonen vises igjen neste gang du kjører funksjonen **Beregn underleveranser**.</span><span class="sxs-lookup"><span data-stu-id="b8275-147">The information will reappear the next time you run the **Calculate Subcontracts** function.</span></span>  

### <a name="to-create-the-subcontract-purchase-order"></a><span data-ttu-id="b8275-148">Slik oppretter du underleverandørbestillingen</span><span class="sxs-lookup"><span data-stu-id="b8275-148">To create the subcontract purchase order</span></span>  
1.  <span data-ttu-id="b8275-149">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Underleveranseforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8275-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Subcontracting Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b8275-150">I fanebladet **Handlinger**, under **Prosess** velger du **Utfør handlingsmelding**.</span><span class="sxs-lookup"><span data-stu-id="b8275-150">On the **Actions** tab, in the **Process** group, choose **Carry Out Action Message**.</span></span>  
3.  <span data-ttu-id="b8275-151">Velg feltet **Skriv ut bestillinger** hvis du vil skrive ut bestillingen når den opprettes.</span><span class="sxs-lookup"><span data-stu-id="b8275-151">Select the **Print Orders** field to print the purchase order as it is created.</span></span>  
4.  <span data-ttu-id="b8275-152">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8275-152">Choose the **OK** button.</span></span>  

<span data-ttu-id="b8275-153">Hvis alle underleveranseoperasjoner sendes til samme leverandørlokasjon, opprettes bare én bestilling.</span><span class="sxs-lookup"><span data-stu-id="b8275-153">If all subcontracted operations are sent to the same vendor location, then only one purchase order is created.</span></span>  

<span data-ttu-id="b8275-154">Forslagslinjen som ble gjort om til en bestilling, slettes fra forslaget.</span><span class="sxs-lookup"><span data-stu-id="b8275-154">The worksheet line that was turned into a purchase order is deleted from the worksheet.</span></span> <span data-ttu-id="b8275-155">Når en bestilling er opprettet vises den ikke på nytt i forslaget.</span><span class="sxs-lookup"><span data-stu-id="b8275-155">Once a purchase order is created, it will not appear in the worksheet again.</span></span>  

## <a name="posting-subcontract-purchase-orders"></a><span data-ttu-id="b8275-156">Bokføre underleverandørbestillinger</span><span class="sxs-lookup"><span data-stu-id="b8275-156">Posting Subcontract Purchase Orders</span></span>  
<span data-ttu-id="b8275-157">Når underleverandørbestillingene er opprettet kan de bli bokført.</span><span class="sxs-lookup"><span data-stu-id="b8275-157">Once the Subcontractor Purchase Orders have been created, they can be posted.</span></span> <span data-ttu-id="b8275-158">Når bestillingen mottas bokføres en kapasitetspost i produksjonsordren, og når den faktureres, bokføres den direkte kostnaden i produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="b8275-158">Receiving the order posts a Capacity Ledger Entry to the production order and invoicing the order posts the direct cost of the purchase order to the production order.</span></span>  

<span data-ttu-id="b8275-159">Det bokføres automatisk en ferdigmeldingskladdelinjepost for produksjonsordren når kjøpet er bokført som mottatt.</span><span class="sxs-lookup"><span data-stu-id="b8275-159">When the purchase is posted as received, then an output journal entry is automatically posted for the production order.</span></span> <span data-ttu-id="b8275-160">Dette gjelder bare hvis underleveranseoperasjonen er den siste operasjonen på produksjonsordreruten.</span><span class="sxs-lookup"><span data-stu-id="b8275-160">This only applies if the subcontract operation is the last operation on the production order routing.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="b8275-161">Det kan være at det ikke er ønskelig å bokføre utdata for en pågående produksjonsordre automatisk når underleveransevarer mottas.</span><span class="sxs-lookup"><span data-stu-id="b8275-161">Posting output automatically for an ongoing production order when subcontracted items are received may not be desired.</span></span> <span data-ttu-id="b8275-162">Årsaker til dette kan være at det forventede avgangsantallet som er bokført, kan være forskjellig fra det faktiske antallet og at bokføringsdatoen for de automatiske utdataene er misvisende.</span><span class="sxs-lookup"><span data-stu-id="b8275-162">Reasons for this could be that the expected output quantity that is posted may be different from the actual quantity and that the posting date of the automatic output is misleading.</span></span>  
>   
>  <span data-ttu-id="b8275-163">For å unngå at den forventede avgangen for en produksjonsordre bokføres når kjøp fra underleverandører mottas, må du passe på at underleveranseoperasjonen ikke er den siste.</span><span class="sxs-lookup"><span data-stu-id="b8275-163">To avoid that the expected output of a production order is posted when subcontract purchases are received, make sure the subcontracted operation is not the last one.</span></span> <span data-ttu-id="b8275-164">Du kan også sette inn en ny siste operasjon for endelig avgangsantall.</span><span class="sxs-lookup"><span data-stu-id="b8275-164">Alternatively, insert a new last operation for the final output quantity.</span></span>

## <a name="to-post-a-subcontract-purchase-order"></a><span data-ttu-id="b8275-165">Slik bokfører du en underleverandørbestilling</span><span class="sxs-lookup"><span data-stu-id="b8275-165">To post a subcontract purchase order</span></span>  
1.  <span data-ttu-id="b8275-166">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b8275-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then select the related link.</span></span>  
2.  <span data-ttu-id="b8275-167">Åpne en bestilling som er opprettet fra underleveranseforslaget.</span><span class="sxs-lookup"><span data-stu-id="b8275-167">Open a purchase order that is created from the subcontracting worksheet.</span></span>  

    <span data-ttu-id="b8275-168">På bestillingslinjene ser du den samme informasjonen som far i forslaget.</span><span class="sxs-lookup"><span data-stu-id="b8275-168">On the purchase order lines, you see the same information that was in the worksheet.</span></span> <span data-ttu-id="b8275-169">Feltene **Prod.ordrenr.**, **Prod.ordrelinjenr.**, **Operasjonsnr.**, og **Arbeidssenternr.**</span><span class="sxs-lookup"><span data-stu-id="b8275-169">The **Prod. Order No.**, **Prod. Order Line No.**, **Operation No.**, and **Work Center No.**</span></span> <span data-ttu-id="b8275-170">er fylt med informasjon fra kildeproduksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="b8275-170">fields are filled in with the information from the source production order.</span></span>  

3.  <span data-ttu-id="b8275-171">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="b8275-171">Choose the **Post** action.</span></span>  

<span data-ttu-id="b8275-172">Det bokføres automatisk en ferdigmeldingskladdelinjepost for produksjonsordren når kjøpet er bokført som mottatt.</span><span class="sxs-lookup"><span data-stu-id="b8275-172">When the purchase is posted as received, then an output journal entry is automatically posted for the production order.</span></span> <span data-ttu-id="b8275-173">Dette gjelder bare hvis underleveranseoperasjonen er den siste operasjonen på produksjonsordreruten.</span><span class="sxs-lookup"><span data-stu-id="b8275-173">This only applies if the subcontract operation is the last operation on the production order routing.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="b8275-174">Det kan være at det ikke er ønskelig å bokføre utdata for en pågående produksjonsordre automatisk når underleveransevarer mottas.</span><span class="sxs-lookup"><span data-stu-id="b8275-174">Posting output automatically for an ongoing production order when subcontracted items are received may not be desired.</span></span> <span data-ttu-id="b8275-175">Årsaker til dette kan være at det forventede avgangsantallet som er bokført, kan være forskjellig fra det faktiske antallet og at bokføringsdatoen for de automatiske utdataene er misvisende.</span><span class="sxs-lookup"><span data-stu-id="b8275-175">Reasons for this could be that the expected output quantity that is posted may be different from the actual quantity and that the posting date of the automatic output is misleading.</span></span>  
>   
>  <span data-ttu-id="b8275-176">For å unngå at den forventede avgangen for en produksjonsordre bokføres når kjøp fra underleverandører mottas, må du passe på at underleveranseoperasjonen ikke er den siste.</span><span class="sxs-lookup"><span data-stu-id="b8275-176">To avoid that the expected output of a production order is posted when subcontract purchases are received, make sure the subcontracted operation is not the last one.</span></span> <span data-ttu-id="b8275-177">Du kan også sette inn en ny siste operasjon for endelig avgangsantall.</span><span class="sxs-lookup"><span data-stu-id="b8275-177">Alternatively, insert a new last operation for the final output quantity.</span></span>  

<span data-ttu-id="b8275-178">Direkte kost for bestillingen bokføres til bestillingen når bestillingen er bokført som fakturert.</span><span class="sxs-lookup"><span data-stu-id="b8275-178">When the purchase order is posted as invoiced, then the direct cost of the purchase order is posted to the production.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8275-179">Se også</span><span class="sxs-lookup"><span data-stu-id="b8275-179">See Also</span></span>  
<span data-ttu-id="b8275-180">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="b8275-180">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="b8275-181">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="b8275-181">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="b8275-182">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="b8275-182">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="b8275-183">Lager</span><span class="sxs-lookup"><span data-stu-id="b8275-183">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="b8275-184">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="b8275-184">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="b8275-185">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8275-185">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>