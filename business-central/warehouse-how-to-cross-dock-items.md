---
title: Kryssoverføre varer| Microsoft-dokumentasjon
description: Kryssoverføringsfunksjonalitet er tilgjengelig hvis du har definert lokasjonen slik at den krever lagermottaksbehandling og plasseringsbehandling.
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
ms.openlocfilehash: 8cf67f83434f135226eaa677cd64d86090a0ab0f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803093"
---
# <a name="cross-dock-items"></a><span data-ttu-id="ac0c0-103">Kryssoverføringsvarer</span><span class="sxs-lookup"><span data-stu-id="ac0c0-103">Cross-Dock Items</span></span>
<span data-ttu-id="ac0c0-104">Kryssoverføringsfunksjonalitet er tilgjengelig hvis du har definert lokasjonen slik at den krever lagermottaksbehandling og plasseringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-104">Cross-docking functionality is available to you if you have set up your location to require warehouse receive and put-away processing.</span></span>  

<span data-ttu-id="ac0c0-105">Når du kryssoverfører varer, behandler du varer i mottak og levering uten å plassere dem på lager, og derved ekspederer du varen ved hjelp av plasserings- og plukkprosesser, og begrenser den fysiske håndteringen av varer.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-105">When you cross-dock items, you process items in receiving and shipping without ever placing them in storage, thereby expediting the item through the put-away and pick processes and limiting the physical handling of items.</span></span> <span data-ttu-id="ac0c0-106">Du kan kryssoverføre varer for både leveringer og produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-106">You can cross-dock items for both shipments and for production orders.</span></span> <span data-ttu-id="ac0c0-107">Når du forbereder en levering eller plukker varer for produksjon og bruker hyller, plukkes varen automatisk fra en kryssoverføringshylle før noen annen hylle.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-107">When you prepare a shipment or pick items for production and you are using bins, the item is automatically picked from a cross-dock bin before any other bin.</span></span> <span data-ttu-id="ac0c0-108">Du må se i kryssoverføringsområdet for å finne ut om de varene du trenger, er tilgjengelig der før du henter varene fra det vanlige lagringsområdet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-108">You must look in the cross-dock area to see if the items you need are available there before you get the items in their usual storage area.</span></span>  

<span data-ttu-id="ac0c0-109">Hvis du har beregnet kryssoverføringsantall, opprettes plasseringslinjer til kryssoverføringshyllen for kryssoverføringsberegning når du bokfører mottaket.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-109">If you have calculated cross-dock quantities, put-away lines to the cross-dock bin for cross-dock calculations are created when you post the receipt.</span></span> <span data-ttu-id="ac0c0-110">Andre plasseringslinjer blir opprettet som vanlig.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-110">Other put-away lines are created as usual.</span></span>  

<span data-ttu-id="ac0c0-111">Hvis du vil bokføre de kryssoverførte varene med en gang slik at de blir tilgjengelig for plukking, må du også registrere en plassering for de andre varene som kom fra mottakslinjen, nemlig de som må lagres.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-111">If you want to post the cross-dock items right away to make them available for picking, you must also register a put-away for the other items originating from the receipt line, namely those that need to be stored.</span></span> <span data-ttu-id="ac0c0-112">Hvis bare noen av varene på en mottakslinje blir kryssoverført, må du derfor sørge for å plassere resten av varene så snart som mulig.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-112">If only some items on a receipt line are being cross-docked, you must therefore make an effort to put away the remaining items as quickly as possible.</span></span> <span data-ttu-id="ac0c0-113">Lageret kan også ha regler som sier at kryssoverføring av hele mottakslinjer skal utføres så sant det er mulig.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-113">Alternatively, your warehouse policy could be to encourage cross-docking of entire receipt lines whenever possible.</span></span>  

<span data-ttu-id="ac0c0-114">I plasseringsinstruksjonen kan du med fordel slette både Hent- og Plasser-instuksjonslinjer for hver mottakslinje som gjelder mottak som helt skal plasseres på lager.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-114">In the put-away instruction, you can to your advantage delete both Take and Place instruction lines for each receipt line that concern receipts that are to be fully put away in storage.</span></span> <span data-ttu-id="ac0c0-115">Disse linjene kan senere opprettes som plasseringslinjer fra plasseringsforslaget eller det bokførte mottaket.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-115">These lines can later be created as put-away lines from the put-away worksheet or the posted receipt.</span></span> <span data-ttu-id="ac0c0-116">Når de er slettet, kan du plassere og registrere linjene som dreier seg om kryssoverførte varer.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-116">When they are deleted, you can then put away and register the lines that concern cross-dock items.</span></span>  

<span data-ttu-id="ac0c0-117">Hvis du har valgt feltet **Bruk plasseringsforslag** på lokasjonskortet og har bokført mottaket med beregnede kryssoverføringer, blir alle mottakslinjene tilgjengelig i forslaget.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-117">If you have selected the **Use Put-away Worksheet** field on the location card and have posted your receipt with calculated cross-docks, all the receipt lines become available in the worksheet.</span></span> <span data-ttu-id="ac0c0-118">Informasjonen om kryssoverføringen går tapt, og den kan ikke gjenopprettes.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-118">The cross-dock information is lost and cannot be recreated.</span></span> <span data-ttu-id="ac0c0-119">Hvis du ønsker å bruke kryssoverføringsfunksjonaliteten, bør du derfor overføre linjer til plasseringsforslaget ved å slette plasseringsinstruksjoner i stedet for å bruke den automatiske overføringsfunksjonen i feltet **Bruk plasseringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-119">Therefore, if you wish to use cross-dock functionality, you should relay lines to the put-away worksheet by deleting put-away instructions rather than using the automatic relay function provided in the **Use Put-away Worksheet** field.</span></span>  

<span data-ttu-id="ac0c0-120">Hvis du bokfører lagermottaket og du ikke har valgt feltet **Bruk plasseringsforslag**, vises varene som skal kryssoverføres som separate linjer i plasseringsinstruksen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-120">If you post the warehouse receipt and you do not have the **Use Put-away Worksheet** field selected, the items to be cross-docked appear as separate lines on the put-away instruction.</span></span> <span data-ttu-id="ac0c0-121">Feltet **Kryssoverføringsinformasjon** på hver plasseringslinje viser om linjen inneholder kryssoverførte varer, varer fra samme mottak som alle må lagres, eller varer som må lagres som kommer fra en mottakslinje der noen av varene skal kryssoverføres.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-121">The **Cross-Dock Information** field on each put-away line shows whether the line contains cross-dock items, items from the same receipt that all need to be stored, or items that need to be stored originating from a receipt line where some of the items are to be cross-docked.</span></span> <span data-ttu-id="ac0c0-122">Med dette feltet kan de ansatte enkelt se hvorfor hele mottaksantallet ikke blir plassert på lager.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-122">With this field, employees can easily see why the full receipt quantity is not being placed in storage.</span></span>  

<span data-ttu-id="ac0c0-123">Programmet har ikke separate poster om varer som er kryssoverført, men det registrerer dem som vanlige plasseringsinstruksjoner.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-123">The program does not keep separate records about items that have been cross-docked, but registers them as ordinary put-away instructions.</span></span>  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a><span data-ttu-id="ac0c0-124">Slik definerer du lageret for kryssoverføring</span><span class="sxs-lookup"><span data-stu-id="ac0c0-124">To set up the warehouse for cross-docking</span></span>  
1.  <span data-ttu-id="ac0c0-125">Definer minst én kryssoverføringshylle hvis du bruker hyller. Definer en kryssoverføringssone hvis du bruker lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-125">Set up at least one cross-dock bin, if you are using bins. Set up a cross-dock zone, if you are using directed put-away and pick.</span></span>  

    <span data-ttu-id="ac0c0-126">Det er merket av for **Kryssoverføringshylle** for en kryssoverføringshylle, og både hylletypen **Motta** og **Plukke** må være valgt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-126">A cross-dock bin has the **Cross-Dock Bin** field selected and must have both **Receive** and **Pick** bin types selected.</span></span> <span data-ttu-id="ac0c0-127">Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c0-127">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

    <span data-ttu-id="ac0c0-128">Hvis du bruker soner, oppretter du en sone for kryssoverføringshyllene og velger feltet **Kryssoverføringshyllesone**.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-128">If you are using zones, create a zone for your cross-dock bins, and select the **Cross-Dock Bin Zone** field.</span></span> <span data-ttu-id="ac0c0-129">Hvis du vil ha mer informasjon, kan du se [Definere lokasjoner slik at de bruker hyller](warehouse-how-to-set-up-locations-to-use-bins.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c0-129">For more information, see [Set Up Locations to Use Bins](warehouse-how-to-set-up-locations-to-use-bins.md).</span></span>  

2.  <span data-ttu-id="ac0c0-130">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjon**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Location**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="ac0c0-131">Velg lokasjonen der du vil definere lageret for kryssoverføring, på siden **Lokasjon**, og velg deretter **Rediger**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-131">On the **Location** page, select the location that you want to set up the warehouse for cross-docking, and then choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="ac0c0-132">På hurtigfanen **Lager**, merker du av for **Bruk kryssoverføring** og fyller ut feltet **Kryssoverføring forfallsdatoberegn.** med tidspunktet for å søke etter kryssoverføringsmuligheter.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-132">On the **Warehouse** FastTab, select the **Use Cross-Docking** check box and fill in the **Cross-Dock Due Date Calc.** field with the time to search for cross-dock opportunities.</span></span>

    <span data-ttu-id="ac0c0-133">Alternativet **Bruk kryssoverføring** er bare tilgjengelig hvis feltene **Mottak nødv.**, **Levering nødv.**, **Plukk nødv.** og **Plassering nødv.** er valgt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-133">The **Use Cross-Docking** option is only available if the **Require Receive**, **Require Shipment**, **Require Pick**, and **Require Put-away** fields are selected.</span></span>  

5.  <span data-ttu-id="ac0c0-134">Hvis du bruker hyller, fyller du ut feltet **Hyllekode for kryssoverføring** på hurtigfanen **Hyller** med koden for hyllen du vil bruke som standard kryssoverføringshylle.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-134">If you are using bins, on the **Bins** FastTab, fill in the **Cross-Dock Bin Code** field with the code of the bin you would like to use as the default cross-dock bin.</span></span>  
6.  <span data-ttu-id="ac0c0-135">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerføringsenhet**, og velg den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Unit**, and select the related link.</span></span>  
7.  <span data-ttu-id="ac0c0-136">For hver vare eller lagerføringsenhet du ønsker å kunne kryssoverføre, velger du varen og deretter **Rediger**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-136">For each item or stockkeeping unit that you want to be able to cross-dock, select the item, and then choose the **Edit** action.</span></span>
8. <span data-ttu-id="ac0c0-137">På siden **Lagerføringsenhetskort** merker du av for **Bruk kryssoverføring**.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-137">On the **Stockkeeping Unit Card** page, select the **Use Cross-Docking** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ac0c0-138">Kryssoverføring er mulig bare hvis du har definert lokasjonen til å kreve lagermottaksbehandling og plasseringsbehandling.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-138">Cross-docking is only possible if your location is set up to require warehouse receive and put-away processing.</span></span>  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a><span data-ttu-id="ac0c0-139">Slik kryssoverfører du varer uten å vise mulighetene</span><span class="sxs-lookup"><span data-stu-id="ac0c0-139">To cross-dock items without viewing the opportunities</span></span>  
1.  <span data-ttu-id="ac0c0-140">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagermottak**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ac0c0-141">Opprett et lagermottak for en vare som er ankommet, og som kanskje kan kryssoverføres.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-141">Create a warehouse receipts for an item that has arrived and can perhaps be cross-docked.</span></span> <span data-ttu-id="ac0c0-142">Hvis du vil ha mer informasjon, kan du se [Motta varer](warehouse-how-receive-items.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c0-142">For more information, see [Receive Items](warehouse-how-receive-items.md).</span></span>  
3.  <span data-ttu-id="ac0c0-143">Fyll ut feltet **Motta (antall)**, og velg deretter **Beregn kryssoverføring**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-143">Fill in the **Qty. to Receive** field, and then choose the **Calculate Cross-Dock** action.</span></span>  

    <span data-ttu-id="ac0c0-144">Utgående kildedokumenter som ber om varene som er planlagt å skulle forlate lageret innefor datoformelens tidsperiode, identifiseres.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-144">Outbound source documents requesting the items that are scheduled to leave the warehouse within the date formula time period are identified.</span></span>  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ac0c0-145">beregner antall slik at du kan kryssoverføre så mye som mulig og unngå å plassere varene, uten å samle opp for mange varer i kryssoverføringsområdet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-145">calculates quantities so that you can cross-dock as much as possible and avoid having to put items away, without piling up too many items in the cross-dock area.</span></span> <span data-ttu-id="ac0c0-146">Verdien i feltet **Ant. som skal kryssoverf** blir derved den minste av enten summen av alle de utgående linjene som ber om varen innenfor beregningstiden minus det antallet varer som allerede er plassert i kryssoverføringsområdet, eller verdien i feltet **Motta (antall)** på mottakslinjen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-146">The value in the **Qty. to Cross-Dock** field is thus the sum of all the outbound lines requesting the item within the look-ahead period minus the quantity of the items that have already been placed in the cross-dock area, or it is the value in the **Qty. to Receive** field on the receipt line, whichever is smaller.</span></span> <span data-ttu-id="ac0c0-147">Du kan ikke kryssoverføre mer enn du har mottatt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-147">You cannot cross-dock more than you have received.</span></span>  

4.  <span data-ttu-id="ac0c0-148">Hvis du vil kryssoverføre det antallet som blir foreslått, bokfører du mottaket.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-148">If you want to cross-dock the quantity as suggested, post the receipt.</span></span> <span data-ttu-id="ac0c0-149">Du kan også bestemme deg for å endre antallet som skal kryssoverføres til en høyere eller lavere verdi, og deretter bokføre mottaket.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-149">You can also decide to change the quantity to cross-dock to a higher or lower value and then post the receipt.</span></span>  

    <span data-ttu-id="ac0c0-150">Antallene som skal kryssoverføres, blir nå vist som linjer i plasseringsinstruksjonen, forutsatt at feltet **Bruk plasseringsforslag** er tomt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-150">The amounts to be cross-docked now appear as lines in the put-away instruction, assuming the **Use Put-away Worksheet** field is cleared.</span></span> <span data-ttu-id="ac0c0-151">Antallene som ikke er kryssoverført, blir til linjer i plasseringsinstruksjonen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-151">The quantities not cross-docked also become lines in the put-away instruction.</span></span>  

    <span data-ttu-id="ac0c0-152">Hvis du har hyller, har de kryssoverførte varene blitt tilordnet til standard kryssoverføringshylle på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-152">If you have bins, the cross-docked items have been assigned to the default cross-dock bin defined on the location card.</span></span>  

5.  <span data-ttu-id="ac0c0-153">Slett **Hent**- og **Plasser**-linjene for varer som ikke skal kryssoverføres i det hele tatt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-153">Delete the **Take** and **Place** lines for items that are not going to be cross-docked at all.</span></span>  
6.  <span data-ttu-id="ac0c0-154">Skriv ut plasseringsinstruksjonen for de resterende linjene, og plasser de antallene av mottaket som skal lagres i de passende hyllene eller i det passende området av lageret.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-154">Print the put-away instruction for the remaining lines, and place the quantities of the receipt that need to be stored in the appropriate bins or in the appropriate area of the warehouse.</span></span> <span data-ttu-id="ac0c0-155">Plasser de kryssoverførte varene i området eller hyllen som er definert for dem av lagerets prinsipper.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-155">Place the cross-dock items in the area or bin designated for them by warehouse policy.</span></span> <span data-ttu-id="ac0c0-156">Enkelte ganger kan lagerets retningslinjer kreve at du lar dem ligge i mottaksområdet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-156">Sometimes, warehouse policy might require that you to just leave them in the receiving area.</span></span>  
7.  <span data-ttu-id="ac0c0-157">Velg **Registrer**-handlingen for å registrere de kryssoverførte varene som plassert og tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-157">To register the cross-docked items as being put-away and available for picking, choose the **Register** action.</span></span>  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a><span data-ttu-id="ac0c0-158">Slik kryssoverfører du varer etter å ha vist mulighetene</span><span class="sxs-lookup"><span data-stu-id="ac0c0-158">To cross-dock items after viewing the opportunities</span></span>  
1.  <span data-ttu-id="ac0c0-159">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagermottak**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-159">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ac0c0-160">Opprett et lagermottak for en vare som er ankommet, og som kanskje kan kryssoverføres.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-160">Create a warehouse receipts for an item that has arrived and can perhaps be cross-docked.</span></span> <span data-ttu-id="ac0c0-161">Hvis du vil ha mer informasjon, kan du se [Motta varer](warehouse-how-receive-items.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c0-161">For more information, see [Receive Items](warehouse-how-receive-items.md).</span></span>  

    <span data-ttu-id="ac0c0-162">Du vil vise kildedokumentlinjer som ber om varen, før du bokfører mottaket.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-162">You want to view the source document lines that are requesting the item before you post the receipt.</span></span>  
3.  <span data-ttu-id="ac0c0-163">Velg handlingen **Beregn kryssoverføring**.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-163">Choose the **Calculate Cross-Dock** action.</span></span>  

    <span data-ttu-id="ac0c0-164">På siden **Kryssoverføringsmuligheter** kan du se de viktigste opplysningene om linjene som ber om varen, for eksempel dokumenttype, forespurt antall og forfallsdatoen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-164">On the **Cross-Dock Opportunities** page you can see the most important details about the lines requesting the item, such as type of document, quantity requested, and due date.</span></span> <span data-ttu-id="ac0c0-165">Disse opplysningene kan hjelpe det med å bestemme hvor mye som skal kryssoverføres, hvor varene skal passeres i kryssoverføringsområdet, og hvordan de skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-165">This information might help you to decide how much to cross-dock, where to place the items in the cross-dock area, or how to group them.</span></span>  

4.  <span data-ttu-id="ac0c0-166">Velg handlingen **Autoutfyll antall for kryssoverføring** for å se hvordan antallene på mottakslinjene beregnes.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-166">Choose **Autofill Qty. to Cross-Dock** action to see how the quantities on the receipt lines are calculated.</span></span> <span data-ttu-id="ac0c0-167">Når du endrer antall varer i feltet **Ant. som skal kryssoverf.** på hver linje, oppdateres beregningen etter hvert som du gjør endringer.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-167">When you change the number of items in the **Qty. to Cross-Dock** field on each line, the calculation is updated as you make changes.</span></span> <span data-ttu-id="ac0c0-168">Dette betyr ikke at den bestemte leveringen eller produksjonen faktisk skal motta varene som er foreslått for kryssoverføring, fordi disse endringene bare blir gjort for testing.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-168">This does not mean that the particular shipment or production order will actually receive the items being suggested for cross-docking, because these manipulations are for testing purposes only.</span></span> <span data-ttu-id="ac0c0-169">Prosessen kan imidlertid være informativ, hvis det blir brukt mer enn én enhet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-169">The process can be informative, however, if more than one unit of measure is involved.</span></span>  
5.  <span data-ttu-id="ac0c0-170">Hvis du vil reservere et antall av varen for en bestemt ordrelinje, plasserer du markøren på denne linjen og velger deretter handlingen **Reserver**.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-170">If you want to reserve a quantity of the item for a particular order line, place your cursor on that line, and then choose the **Reserve** action.</span></span> <span data-ttu-id="ac0c0-171">På siden **Reservasjon** kan du nå reservere eventuelt disponibelt antall av varen for denne bestemte ordren.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-171">On the **Reservation** page, you can now reserve any available quantity of the item for this specific order.</span></span> <span data-ttu-id="ac0c0-172">Denne reservasjonen er som andre reservasjoner og har ikke høyere prioritet fordi den ble opprettet i forbindelse med kryssoverføring.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-172">This reservation is like any other reservation and does not have higher priority because it was created in connection with cross-docking.</span></span> <span data-ttu-id="ac0c0-173">Hvis du vil ha mer informasjon, kan du se [Reservere varer](inventory-how-to-reserve-items.md).</span><span class="sxs-lookup"><span data-stu-id="ac0c0-173">For more information, see [Reserve Items](inventory-how-to-reserve-items.md).</span></span>   
6.  <span data-ttu-id="ac0c0-174">Når du er ferdig med å beregne på nytt eller med å reservere, velger du **OK**-knappen for å hente den beregningen du har revidert, inn i feltet **Ant. som skal kryssoverf.** på mottakslinjen, eller så velger du **Avbryt**-knappen hvis du vil gå tilbake til lagermottaket, der du eventuelt kan beregne kryssoverføringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-174">When you are finished recalculating or reserving, choose the **OK** button to bring the calculation as you have revised it into the **Qty. to Cross-Dock** field on the receipt line, or choose the **Cancel** button if you want to return to the warehouse receipt, where you can calculate the cross-dock again if you wish.</span></span>  
7.  <span data-ttu-id="ac0c0-175">Bokfør deretter mottaket, og du kan fortsette i plasseringsinstruksjonen slik det er beskrevet i trinn 3 til 7 i delen "Slik kryssoverfører varer uten å vise salgsmulighetene".</span><span class="sxs-lookup"><span data-stu-id="ac0c0-175">Now post the receipt, and you can continue in the put-away instruction as described in steps 3 through 7 in the “To cross-dock items without viewing the opportunities” section.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ac0c0-176">I plasseringen kan du fortsette å endre antallene som blir plassert på lager eller kryssoverført, slik det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-176">In the warehouse put-away, you can continue to change the quantities that are being put away in storage or cross-docked, as necessary.</span></span> <span data-ttu-id="ac0c0-177">Du kan for eksempel bestemme deg for å kryssoverføre et ekstra antall for å få registreringen av kryssoverføringen til å gå raskere.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-177">For example, you might decide to cross-dock an extra quantity to expedite the cross-dock registration.</span></span>  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a><span data-ttu-id="ac0c0-178">Slik viser du kryssoverførte varer i en følgeseddel eller et plukkforslag</span><span class="sxs-lookup"><span data-stu-id="ac0c0-178">To view cross-docked items in a shipment or pick worksheet</span></span>  
<span data-ttu-id="ac0c0-179">Hvis du bruker hyller, kan du, hver gang du åpner en følgeseddel eller plukkforslaget, se en oppdatert beregning av antallet for hver vare i kryssoverføringshyllene. Dette er verdifull informasjon hvis du venter på at en vare skal komme inn.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-179">If you are using bins, you can see, each time you open a shipment or the pick worksheet, an updated calculation of the quantity of each item in the cross-dock bins. This is valuable information if you are waiting for an item to come in.</span></span> <span data-ttu-id="ac0c0-180">Når du ser at varen er tilgjengelig i kryssoverføringshyllen, kan du raskt opprette en plukking for alle varene i leveringen.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-180">When you see that the item is available in the cross-dock bin, you can then quickly create a pick for all the items on the shipment.</span></span> <span data-ttu-id="ac0c0-181">I plukkforslaget kan du endre linjene slik det passer, og deretter opprette en plukking.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-181">In the pick worksheet, you can modify the lines as appropriate and then create a pick.</span></span>  

<span data-ttu-id="ac0c0-182">Du må se etter varer i kryssoverføringsområdet før du plukker varer for levering.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-182">You have to look for items in the cross-dock area first when you pick items for shipment.</span></span> <span data-ttu-id="ac0c0-183">Hvis du under mottaksprosessen har merket deg hvilke kildedokumenter som var grunnlaget for kryssoverføringen, vil du ha en bedre forståelse av om varen finnes i kryssoverføringsområdet eller ikke.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-183">If you have noted during the receipt process the source documents that were the basis for cross-docking, you have a better idea of whether the item can be found in the cross-dock area or not.</span></span>  

<span data-ttu-id="ac0c0-184">Når en produksjonsordre er frigitt, er linjene tilgjengelig i plukkforslaget, og du kan se i feltet **Ant. i kryssoverføringshylle** om de varene du venter på, er ankommet og plassert i kryssoverføringshyllene. Når du oppretter en plukkinstruksjon, foreslår programmet at du først plukker de kryssoverførte varene, og vil senere søke etter varen i lagringshyllene.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-184">When a production order has been released, the lines are available in the pick worksheet, and you can see in the **Qty. on Cross-Dock Bin** field whether the items you are waiting for have arrived and been placed in the cross-dock bins. When you create a pick instruction, the program suggests that you first pick the cross-docked items and will only later search for the item in storage bins.</span></span>  

<span data-ttu-id="ac0c0-185">Hvis du ikke bruker hyller, må du huske å kontrollere kryssoverføringsområdet jevnlig. Hvis ikke, må du stole på varsler fra mottak om at varene for produksjon er ankommet.</span><span class="sxs-lookup"><span data-stu-id="ac0c0-185">If you are not using bins, you must remember to check the cross-dock area from time to time, or rely on notifications from receipts that items for production have arrived.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac0c0-186">Se også</span><span class="sxs-lookup"><span data-stu-id="ac0c0-186">See Also</span></span>  
[<span data-ttu-id="ac0c0-187">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ac0c0-187">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ac0c0-188">Lager</span><span class="sxs-lookup"><span data-stu-id="ac0c0-188">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ac0c0-189">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ac0c0-189">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ac0c0-190">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ac0c0-190">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ac0c0-191">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="ac0c0-191">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ac0c0-192">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac0c0-192">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  