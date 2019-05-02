---
title: Opprette ruter | Microsoft-dokumentasjon
description: En rute inneholder hoveddata som gjenspeiler prosesskravene for en gitt produsert vare. Når en produksjonsordre opprettes for denne varen, styrer varens rute planleggingen av operasjonen(e) som vist på siden **Prod.ordrerute** under produksjonsordren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 6eb16bd42357646a9e88c4799a3f110be0e294eb
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803660"
---
# <a name="create-routings"></a><span data-ttu-id="52705-104">Opprette ruter</span><span class="sxs-lookup"><span data-stu-id="52705-104">Create Routings</span></span>
<span data-ttu-id="52705-105">Produksjonsselskaper bruker ruter til å visualisere og dirigere produksjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="52705-105">Manufacturing companies use routings to visualize and direct the manufacturing process.</span></span>

<span data-ttu-id="52705-106">Ruten danner grunnlaget for prosessplanlegging, kapasitetsplaner, planlage tildelinger av materialbehov og diverse produksjonsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="52705-106">The routing is the basis of process scheduling, capacity scheduling, scheduled assignment of material needs, and manufacturing documents.</span></span>  

<span data-ttu-id="52705-107">Som for produksjonsstykklister tilordnes rutene til den ferdige produksjonsvaren.</span><span class="sxs-lookup"><span data-stu-id="52705-107">As for production BOMs, the routings are assigned to the manufacturing end item.</span></span> <span data-ttu-id="52705-108">En rute inneholder hoveddata som gjenspeiler prosesskravene for en gitt produsert vare.</span><span class="sxs-lookup"><span data-stu-id="52705-108">A routing holds master data that captures the process requirements of a given produced item.</span></span> <span data-ttu-id="52705-109">Når en produksjonsordre opprettes for denne varen, styrer varens rute planleggingen av operasjonen(e) som vist på siden **Prod.ordrerute** under produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="52705-109">Once a production order is created for that item, its routing will govern the scheduling of operations as represented on the **Prod. Order Routing** page under the production order.</span></span>  

<span data-ttu-id="52705-110">Før du kan definere en rute, må følgende være på plass:</span><span class="sxs-lookup"><span data-stu-id="52705-110">Before you can set up a routing, the following must be in place:</span></span>  

- <span data-ttu-id="52705-111">Varekort er opprettet for overordnede varer som inngår i produksjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-111">Item cards are created for parent items that take part in manufacturing.</span></span> <span data-ttu-id="52705-112">Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="52705-112">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>
- <span data-ttu-id="52705-113">Produksjonsressurser er definert.</span><span class="sxs-lookup"><span data-stu-id="52705-113">Production resources are set up.</span></span> <span data-ttu-id="52705-114">Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidssentre og produksjonsressurser](production-how-to-set-up-work-and-machine-centers.md).</span><span class="sxs-lookup"><span data-stu-id="52705-114">For more information, see [Set Up Work Centers and Machine Centers](production-how-to-set-up-work-and-machine-centers.md).</span></span>

## <a name="to-create-a-routing"></a><span data-ttu-id="52705-115">Slik oppretter du en rute</span><span class="sxs-lookup"><span data-stu-id="52705-115">To create a routing</span></span>  
1.  <span data-ttu-id="52705-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52705-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52705-117">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52705-117">Choose the **New** action.</span></span>  
3. <span data-ttu-id="52705-118">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="52705-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="52705-119">Velg **Seriell** i **Type**-feltet for å beregne produksjonsruten i henhold til verdien i **Operasjonsnr.**-feltet</span><span class="sxs-lookup"><span data-stu-id="52705-119">In the **Type** field, select **Serial** to calculate the production routing according to the value in the **Operation No.**</span></span> <span data-ttu-id="52705-120">.</span><span class="sxs-lookup"><span data-stu-id="52705-120">field.</span></span>   
    <span data-ttu-id="52705-121">Velg **Parallell** for å beregne operasjonene i henhold til verdien i feltet **Neste operasjonsnr.**</span><span class="sxs-lookup"><span data-stu-id="52705-121">Select **Parallel** to calculate the operations according to the value in the **Next Operation No.**</span></span> <span data-ttu-id="52705-122">.</span><span class="sxs-lookup"><span data-stu-id="52705-122">field.</span></span>  
5.  <span data-ttu-id="52705-123">Hvis du vil kunne redigere ruten, setter du **Status**-feltet til **Ny** eller **Under utvikling**.</span><span class="sxs-lookup"><span data-stu-id="52705-123">To edit the routing, set the **Status** field to **New** or **Under Development**.</span></span> <span data-ttu-id="52705-124">Hvis du vil aktivere den, setter du **Status**-feltet til **Sertifisert**.</span><span class="sxs-lookup"><span data-stu-id="52705-124">To activate it, set the **Status** field to **Certified**.</span></span>  

    <span data-ttu-id="52705-125">Fortsett med å fylle ut rutelinjene.</span><span class="sxs-lookup"><span data-stu-id="52705-125">Proceed to fill in the routing lines.</span></span>
6.  <span data-ttu-id="52705-126">I feltet **Operasjonsnr.**</span><span class="sxs-lookup"><span data-stu-id="52705-126">In the **Operation No.**</span></span> <span data-ttu-id="52705-127">registrerer du nummeret for den første operasjonen, for eksempel  **10**.</span><span class="sxs-lookup"><span data-stu-id="52705-127">field, enter the number of the first operation, for example,  **10**.</span></span>  
7.  <span data-ttu-id="52705-128">Angi hvilken ressurstype som brukes, i **Type**-feltet, for eksempel **Arbeidssenter**.</span><span class="sxs-lookup"><span data-stu-id="52705-128">In the **Type** field, specify which kind of resource is used, for example, **Work Center**.</span></span>  
8.  <span data-ttu-id="52705-129">I **Nr.**</span><span class="sxs-lookup"><span data-stu-id="52705-129">In the **No.**</span></span> <span data-ttu-id="52705-130">-feltet velger du ressursen som skal brukes, eller skriv den inn i feltet.</span><span class="sxs-lookup"><span data-stu-id="52705-130">field, select the resource to be used, or type it in the field.</span></span>  
9.  <span data-ttu-id="52705-131">I feltet **Rutekoblingskode** registrerer du en kode for å koble komponenten til en bestemt operasjon.</span><span class="sxs-lookup"><span data-stu-id="52705-131">In the **Routing Link Code** field, enter a code to connect the component to a specific operation.</span></span> <span data-ttu-id="52705-132">Hvis du vil ha mer informasjon, kan du se [Slik oppretter du rutekoblinger](production-how-to-create-routings.md#to-create-routing-links).</span><span class="sxs-lookup"><span data-stu-id="52705-132">For more information, see [To create routing links](production-how-to-create-routings.md#to-create-routing-links).</span></span>
10.  <span data-ttu-id="52705-133">I feltene **Operasjonstid** og **Oppstillingstid** registrerer du tiden det tar å utføre operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-133">In the **Run Time** and **Setup Time** fields, enter the process times needed to perform the operation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52705-134">Oppstillingstiden beregnes per produksjonsordre, mens operasjonstiden beregnes per produserte vare.</span><span class="sxs-lookup"><span data-stu-id="52705-134">Setup time is calculated per production order, whereas run time is calculated per produced item.</span></span>  

11.  <span data-ttu-id="52705-135">Angi hvor mange enheter av den valgte ressursen skal brukes til å utføre operasjonen, i feltet **Samtidige kapasiteter**.</span><span class="sxs-lookup"><span data-stu-id="52705-135">In the **Concurrent Capacities** field, specify how many units of the selected resource are used to perform the operation.</span></span> <span data-ttu-id="52705-136">To personer som for eksempel er tildelt til én pakkeoperasjon, halverer operasjonstiden.</span><span class="sxs-lookup"><span data-stu-id="52705-136">For example, two people allocated to one packing operation will halve the run time.</span></span>  
12.  <span data-ttu-id="52705-137">Fortsett med å fylle ut linjer for alle operasjonene som kreves for å produsere den aktuelle varen.</span><span class="sxs-lookup"><span data-stu-id="52705-137">Continue to fill in lines for all operations involved in producing the item in question.</span></span>  
13.  <span data-ttu-id="52705-138">Hvis du vil kopiere linjer fra en eksisterende rute, velger du **Kopier rute** for å velge eksisterende linjer.</span><span class="sxs-lookup"><span data-stu-id="52705-138">To copy lines from an existing routing, choose the **Copy Routing** action to select existing lines.</span></span>  
14. <span data-ttu-id="52705-139">Godkjenn ruten.</span><span class="sxs-lookup"><span data-stu-id="52705-139">Certify the routing.</span></span>  
15. <span data-ttu-id="52705-140">Nå kan du knytte den nye ruten til kortet for den aktuelle produksjonsvaren ved å fylle ut feltet **Rutenr.**</span><span class="sxs-lookup"><span data-stu-id="52705-140">You can now attach the new routing to the card of the production item in question, by filling in the **Routing No.** field.</span></span> <span data-ttu-id="52705-141">Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="52705-141">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="52705-142">Husk også å beregne varens standardkost fra **Vare**-kortet: Velg **Produksjon**, velg **Beregn standardkost**, og velg deretter **Alle nivåer**.</span><span class="sxs-lookup"><span data-stu-id="52705-142">Remember also to recalculate the item’s standard cost from the **Item** card: Choose the **Manufacturing** action, select the **Calc. Standard Cost** action, and then select the **All Levels** action.</span></span>  

## <a name="to-create-routing-links"></a><span data-ttu-id="52705-143">Slik oppretter du rutekoblinger</span><span class="sxs-lookup"><span data-stu-id="52705-143">To create routing links</span></span>
<span data-ttu-id="52705-144">Du kan opprette rutekoblinger til å koble komponenter til bestemte operasjoner for å kunne beholde forbindelsen selv om produksjonsstykklisten eller ruten endres.</span><span class="sxs-lookup"><span data-stu-id="52705-144">You can create routing links to connect components to specific operations in order to retain their relationship even though the production BOM or routing is modified.</span></span> <span data-ttu-id="52705-145">Det blir også enklere med trekk av komponenter i siste liten, nærmere bestemt når den spesifikke koblingsoperasjonen starter, og ikke når hele produksjonsordren frigis.</span><span class="sxs-lookup"><span data-stu-id="52705-145">It also facilitates just-in-time flushing of components, namely when the specific linked operation starts, not when the complete production order is released.</span></span> <span data-ttu-id="52705-146">Hvis du vil ha mer informasjon, kan du se [Lagertrekke komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="52705-146">For more information see [Flush Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>  

<span data-ttu-id="52705-147">En annen viktig fordel er at koblede komponenter og operasjoner vises i en logisk prosesstruktur når du bruker **Produksjonskladd**-siden til bokføring av avgang og forbruk.</span><span class="sxs-lookup"><span data-stu-id="52705-147">Another important benefit is that linked components and operations are displayed in a logical process structure when you use the **Production Journal** page for output and consumption posting.</span></span>  

1.  <span data-ttu-id="52705-148">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52705-148">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52705-149">Åpne ruten som inneholder operasjonene du vil koble.</span><span class="sxs-lookup"><span data-stu-id="52705-149">Open the routing that contains the operations that you want to link.</span></span>  

    <span data-ttu-id="52705-150">Kontroller at rutestatus er **Under utvikling**.</span><span class="sxs-lookup"><span data-stu-id="52705-150">Make sure the routing status is **Under Development**.</span></span>  

3.  <span data-ttu-id="52705-151">På den aktuelle rutelinjen, i **Rutekoblingskode**-feltet, velger du en kode.</span><span class="sxs-lookup"><span data-stu-id="52705-151">On the relevant routing line, in the **Routing Link Code** field, select a code.</span></span>  
4.  <span data-ttu-id="52705-152">Legg deretter til forskjellige rutekoblingskoder i andre operasjoner i ruten, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="52705-152">Proceed to add different routing link codes to other operations in the routing, if relevant.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="52705-153">Du bør ikke bruke samme rutekoblingskode i forskjellige operasjoner i en rute fordi du kan komme til å koble en komponent til to forskjellige operasjoner ved en feil, slik at den blir brukt to ganger.</span><span class="sxs-lookup"><span data-stu-id="52705-153">You should not use the same routing link code in different operations on a routing because you may incorrectly link a component to two different operations, so that it is consumed two times.</span></span>  
    >   
    >  <span data-ttu-id="52705-154">Det kan være hensiktsmessig å navngi rutekoblingskoden etter operasjonen for å sikre at rutekoblingen er operasjonsspesifikk.</span><span class="sxs-lookup"><span data-stu-id="52705-154">It is a good idea to name the routing link code after the operation in order to ensure operation-specific routing links.</span></span>

5.  <span data-ttu-id="52705-155">Sett rutestatusen til **Sertifisert**.</span><span class="sxs-lookup"><span data-stu-id="52705-155">Set the routing status to **Certified**.</span></span>  

    <span data-ttu-id="52705-156">Rutekoblingskoder tilordnes nå til operasjoner.</span><span class="sxs-lookup"><span data-stu-id="52705-156">Routing link codes are now assigned to operations.</span></span> <span data-ttu-id="52705-157">Deretter må du opprette den faktiske koblingen ved å tilordne de samme kodene til bestemte komponenter i den aktuelle produksjonsstykklisten.</span><span class="sxs-lookup"><span data-stu-id="52705-157">Next, you must create the actual link by assigning the same codes to specific components in the relevant production BOM.</span></span>  

6.  <span data-ttu-id="52705-158">Åpne **produksjonsstykklisten** som inneholder komponentene du vil koble til operasjonene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="52705-158">Open the **Production BOM** that contains the components that you want to link to the above operations.</span></span> <span data-ttu-id="52705-159">Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsstykklister](production-how-to-create-production-boms.md).</span><span class="sxs-lookup"><span data-stu-id="52705-159">For more information, see [Create Production BOMs](production-how-to-create-production-boms.md).</span></span>
7.  <span data-ttu-id="52705-160">Kontroller at stykklistestatus er **Under utvikling**.</span><span class="sxs-lookup"><span data-stu-id="52705-160">Make sure the BOM status is **Under Development**.</span></span>  
8.  <span data-ttu-id="52705-161">På den aktuelle produksjonsstykklistelinjen, i **Rutekoblingskode**-feltet, velger du koden du nettopp har tilordnet til den aktuelle operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-161">On the relevant production BOM line, in the **Routing Link Code** field, select the code that you have just assigned to the relevant operation.</span></span>  
9. <span data-ttu-id="52705-162">Legg deretter til rutekoblingskoder i andre komponenter i henhold til de unike operasjonene de brukes i.</span><span class="sxs-lookup"><span data-stu-id="52705-162">Proceed to add routing link codes to other components according to the unique operations where they are used.</span></span>  
10. <span data-ttu-id="52705-163">Sett statusen for produksjonsstykklisten til **Sertifisert**.</span><span class="sxs-lookup"><span data-stu-id="52705-163">Set the production BOM status to **Certified**.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="52705-164">Hvis du vil aktivere rutekoblingene for en eksisterende produksjonsordre, må du først fornye produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="52705-164">To enable the routing links on an existing production order, you must refresh the productio1n order.</span></span> <span data-ttu-id="52705-165">Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="52705-165">For more information, see [Create Production Orders](production-how-to-create-production-orders.md).</span></span>  

<span data-ttu-id="52705-166">De valgte komponentene kobles nå til de valgte operasjonene når du oppretter eller fornyer produksjonsordren ved hjelp av den aktuelle produksjonsstykklisten og ruten.</span><span class="sxs-lookup"><span data-stu-id="52705-166">The selected components will now be linked to the selected operations when you create or refresh a production order using the production BOM and routing in question.</span></span> <span data-ttu-id="52705-167">Dette vises på siden **Prod.ordrekomponenter** under produksjonsordren, og her kan du også fjerne og legge til de definerte rutekoblingskodene når som helst.</span><span class="sxs-lookup"><span data-stu-id="52705-167">This is visible on the **Prod. Order Components** page under the production order, and here you can also remove and add the defined routing link codes at any time.</span></span>

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a><span data-ttu-id="52705-168">Slik tilordner du personellet, verktøyene og kvalitetsmålene til ruteoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="52705-168">To assign personnel, tools, and quality measures to routing operations.</span></span>
<span data-ttu-id="52705-169">Hvis du trenger personell med kvalifikasjoner, spesialkunnskap eller spesiell godkjenning for en operasjon, kan du tilordne dette personellet til operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-169">If you require personnel with qualifications, special knowledge, or special authorization for an operation, you can assign these personnel to the operation.</span></span> <span data-ttu-id="52705-170">Du kan dessuten tilordne verktøy og kvalitetskrav til operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-170">In addition, you can assign tools and quality requirements to the operation.</span></span> <span data-ttu-id="52705-171">Denne fremgangsmåten beskriver hvordan du tilordner personell.</span><span class="sxs-lookup"><span data-stu-id="52705-171">This procedure describes how to assign personnel.</span></span> <span data-ttu-id="52705-172">Fremgangsmåten er de samme som for andre typer informasjon om operasjoner.</span><span class="sxs-lookup"><span data-stu-id="52705-172">The steps are similar for other types of operation information.</span></span>

1.  <span data-ttu-id="52705-173">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52705-173">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52705-174">Åpne den aktuelle ruten.</span><span class="sxs-lookup"><span data-stu-id="52705-174">Open the relevant routing.</span></span>  
3.  <span data-ttu-id="52705-175">På hurtigfanen **Linjer** velger du linjen du vil behandle, og velg deretter **Personell**.</span><span class="sxs-lookup"><span data-stu-id="52705-175">On the **Lines** FastTab, select the line that you want to process, and then choose the **Personnel** action.</span></span>  
4.  <span data-ttu-id="52705-176">Fyll ut feltene på **Rutepersonell**-siden.</span><span class="sxs-lookup"><span data-stu-id="52705-176">Fill in the fields on the **Routing Personnel** page.</span></span>  
5.  <span data-ttu-id="52705-177">Velg **OK**-knappen for å lukke siden.</span><span class="sxs-lookup"><span data-stu-id="52705-177">Choose the **OK** button to exit the page.</span></span> <span data-ttu-id="52705-178">De angitte verdiene kopieres og tilordnes operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-178">The entered values are copied and assigned to the operation.</span></span>    

## <a name="to-create-a-new-versions-of-a-routing"></a><span data-ttu-id="52705-179">Slik oppretter du en ny versjon av en rute</span><span class="sxs-lookup"><span data-stu-id="52705-179">To create a new versions of a routing</span></span>  
<span data-ttu-id="52705-180">Med versjonsprinsippet kan du håndtere flere versjoner av en rute.</span><span class="sxs-lookup"><span data-stu-id="52705-180">The version principle enables you to manage several versions of a routing.</span></span> <span data-ttu-id="52705-181">Strukturen i ruteversjonen tilsvarer strukturen i ruten som består av ruteversjonshodet og ruteversjonslinjene.</span><span class="sxs-lookup"><span data-stu-id="52705-181">The structure of the routing version corresponds to the structure of the routing consisting of the routing version header and the routing version lines.</span></span> <span data-ttu-id="52705-182">Hovedforskjellen defineres av startdatoen.</span><span class="sxs-lookup"><span data-stu-id="52705-182">The basic difference is defined by the starting date.</span></span>  

1.  <span data-ttu-id="52705-183">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52705-183">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Routings**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="52705-184">Velg ruten som skal kopieres, og velg deretter **Versjoner**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="52705-184">Select the routing to be copied, and then choose the **Versions** action.</span></span>  
3. <span data-ttu-id="52705-185">På siden **Ruteversjoner** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52705-185">On the **Routing Versions** page, choose the **New** action.</span></span>
4. <span data-ttu-id="52705-186">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="52705-186">Fill in the fields as necessary.</span></span>
5.  <span data-ttu-id="52705-187">I feltet **Versjonskode** angir du versjonens unike identifikasjon.</span><span class="sxs-lookup"><span data-stu-id="52705-187">In the **Version Code** field, enter the unique identification of the version.</span></span> <span data-ttu-id="52705-188">Alle kombinasjoner av tall og bokstaver er tillatt.</span><span class="sxs-lookup"><span data-stu-id="52705-188">Any combination of numbers and letters is permitted.</span></span>  

    <span data-ttu-id="52705-189">Den nye versjonen får automatisk statusen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="52705-189">The newly created version is automatically assigned the status **New**.</span></span>  
6.  <span data-ttu-id="52705-190">Hvis du vil opprette operasjonslinjene, velger du den første tomme linjen, og deretter fyller du ut feltet **Operasjonsnr.**</span><span class="sxs-lookup"><span data-stu-id="52705-190">To create operation lines, select the first blank line, and then fill in the **Operation No.**</span></span> <span data-ttu-id="52705-191">i henhold til rekkefølgen på operasjonene.</span><span class="sxs-lookup"><span data-stu-id="52705-191">field according to the sequence of operations.</span></span>

    <span data-ttu-id="52705-192">Operasjonslinjene sorteres i stigende rekkefølge etter operasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="52705-192">The operation lines are sorted in ascending order by operation numbers.</span></span> <span data-ttu-id="52705-193">Vi anbefaler at du velger passende trinnbredde slik at du kan gjøre endringer senere.</span><span class="sxs-lookup"><span data-stu-id="52705-193">To be able to make changes later, we recommend you to select adequate step widths.</span></span> <span data-ttu-id="52705-194">Feltet **Neste operasjonsnr.**</span><span class="sxs-lookup"><span data-stu-id="52705-194">The **Next Operation No.**</span></span> <span data-ttu-id="52705-195">refererer til den etterfølgende operasjonen.</span><span class="sxs-lookup"><span data-stu-id="52705-195">field refers to the following operation.</span></span> <span data-ttu-id="52705-196">Nummeret på operasjonen kan angis direkte.</span><span class="sxs-lookup"><span data-stu-id="52705-196">The number of the operation can be entered directly.</span></span>

7. <span data-ttu-id="52705-197">Når ruteversjonen er fullført, kan du angi **Status**-feltet til **Sertifisert**.</span><span class="sxs-lookup"><span data-stu-id="52705-197">When the routing version is completed, setting the **Status** field to **Certified**.</span></span>

<span data-ttu-id="52705-198">Tidsgyldigheten for versjonen angis i feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="52705-198">The time validity of the version is specified by the **Starting Date** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52705-199">Se også</span><span class="sxs-lookup"><span data-stu-id="52705-199">See Also</span></span>  
[<span data-ttu-id="52705-200">Opprette produksjonsstykklister</span><span class="sxs-lookup"><span data-stu-id="52705-200">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="52705-201">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="52705-201">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="52705-202">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="52705-202">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="52705-203">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="52705-203">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="52705-204">Lager</span><span class="sxs-lookup"><span data-stu-id="52705-204">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="52705-205">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="52705-205">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="52705-206">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52705-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>