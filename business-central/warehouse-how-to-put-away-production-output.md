---
title: Plassere produksjonsavgang | Microsoft-dokumentasjon
description: Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon.
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
ms.openlocfilehash: 9092100816c58fe2882c61214a5008e27591d4f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802566"
---
# <a name="put-away-production-or-assembly-output"></a><span data-ttu-id="c4a32-103">Plassere produksjonsavgang eller monteringsavgang</span><span class="sxs-lookup"><span data-stu-id="c4a32-103">Put Away Production or Assembly Output</span></span>
<span data-ttu-id="c4a32-104">Hvordan du plasserer avgang fra produksjon, avhenger av hvordan lageret er definert som lokasjon.</span><span class="sxs-lookup"><span data-stu-id="c4a32-104">How you put away your output from production depends on how your warehouse is set up as a location.</span></span> <span data-ttu-id="c4a32-105">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c4a32-105">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

<span data-ttu-id="c4a32-106">I grunnleggende lageroppsett hvor lokasjonen krever plasseringsbehandling, men ikke mottaksbehandling, bruker du dokumentet **Lagerplassering** til å organisere og registrere plasseringen av avgang.</span><span class="sxs-lookup"><span data-stu-id="c4a32-106">In basic warehouse configurations where the location requires put-away processing, but not receive processing, you use the **Inventory Put-away** document to organize and record the put-away of output.</span></span>  

<span data-ttu-id="c4a32-107">I avanserte lageroppsett hvor lokasjonen krever både plasserings- og mottaksbehandling, kan du opprette enten et internt plasseringsdokument eller et flyttedokument for å plassere avgangen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-107">In advanced warehouse configurations where the location requires both put-away and receive processing, you create either an internal put-away document or a movement document to put away the output.</span></span>  

<span data-ttu-id="c4a32-108">Det første trinnet ved opprettelse av plasseringsavgang, er å opprette den inngående lagerforespørselen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-108">The first step in creating putting output away is to create the inbound warehouse request.</span></span> <span data-ttu-id="c4a32-109">Denne forespørselen informerer lageret om at produksjons- eller monteringsordreavgangen er klar til å plasseres.</span><span class="sxs-lookup"><span data-stu-id="c4a32-109">This request informs the warehouse that the production or assembly order output is ready to be put away.</span></span>

## <a name="to-create-the-inbound-warehouse-request"></a><span data-ttu-id="c4a32-110">Slik oppretter du den inngående lagerforespørselen</span><span class="sxs-lookup"><span data-stu-id="c4a32-110">To create the inbound warehouse request</span></span>  
1.  <span data-ttu-id="c4a32-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Released Production Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4a32-112">På produksjonsordren som er klar til plassering, velger du handlingen **Opprett inngående lagerforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-112">On the production order that is ready for put-away, choose the **Create Inbound Whse. Request** action.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c4a32-113">Du kan også opprette den inngående lagerforespørselen ved å merke av for **Opprett inngående foresp.** når du fornyer produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="c4a32-113">You can also create the inbound warehouse request by selecting the **Create Inbound Request** check box when you refresh the production order.</span></span> <span data-ttu-id="c4a32-114">Hvis du vil ha mer informasjon, se [Fornye eller planlegge produksjonsordrer på nytt](production-how-to-replan-refresh-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="c4a32-114">For more information, see [Refresh or Replan Production Orders](production-how-to-replan-refresh-production-orders.md).</span></span>  

## <a name="to-put-output-away-with-an-inventory-put-away"></a><span data-ttu-id="c4a32-115">Slik plasseres varer med lagerplassering</span><span class="sxs-lookup"><span data-stu-id="c4a32-115">To put output away with an inventory put-away</span></span>  
1.  <span data-ttu-id="c4a32-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplassering**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Put-away**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4a32-117">Opprett en ny lagerplassering.</span><span class="sxs-lookup"><span data-stu-id="c4a32-117">Create a new inventory put-away.</span></span> <span data-ttu-id="c4a32-118">Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).</span><span class="sxs-lookup"><span data-stu-id="c4a32-118">For more information, see [Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md).</span></span>
3.  <span data-ttu-id="c4a32-119">Du får tilgang til produksjonsordreavgang ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="c4a32-119">To access the production order output, choose the **Get Source Documents** action, and then select the released production order.</span></span>  
4.  <span data-ttu-id="c4a32-120">Fyll ut plasseringslinjene.</span><span class="sxs-lookup"><span data-stu-id="c4a32-120">Fill in the put-away lines as appropriate.</span></span>
5.  <span data-ttu-id="c4a32-121">Når linjene er klare for bokføring, velger du handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-121">When the lines are ready for posting, choose the **Post** action.</span></span> <span data-ttu-id="c4a32-122">Bokføringen vil opprette de nødvendige lagerpostene og bokføre avgangen av varene.</span><span class="sxs-lookup"><span data-stu-id="c4a32-122">The posting will create the necessary warehouse entries and post the output of the items.</span></span>  

<span data-ttu-id="c4a32-123">Du kan også opprette en **Lagerplassering** direkte fra den frigitte produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="c4a32-123">You can also create an **Inventory Put-away** directly from the released production order.</span></span> <span data-ttu-id="c4a32-124">Hvis du vil ha mer informasjon, kan du se [Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md).</span><span class="sxs-lookup"><span data-stu-id="c4a32-124">For more information, see [Put Items Away with Inventory Put-aways](warehouse-how-to-put-items-away-with-inventory-put-aways.md).</span></span>  

<span data-ttu-id="c4a32-125">Når du bokfører en lagerplassering, antas det at alle operasjonene bokføres i henhold til standardruten, det vil si at avgangsantall bokføres i henhold til den siste operasjonen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-125">When you post an inventory put-away, it is assumed that all the operations are posted according to the standard routing, that is, output quantity is posted according to the last operation.</span></span> <span data-ttu-id="c4a32-126">Du kan bruke ferdigmeldingskladden til å bokføre avvik i avgangsantall og oppstillingstid og operasjonstid.</span><span class="sxs-lookup"><span data-stu-id="c4a32-126">You can use the output journal to post variances in output quantity and the setup and run times.</span></span> <span data-ttu-id="c4a32-127">Hvis det er nødvendig å bokføre delvis etter at du har opprettet lagerplasseringen, kan du gjøre dette for oppstillingstider og antall for alle operasjoner bortsett fra den siste.</span><span class="sxs-lookup"><span data-stu-id="c4a32-127">If it is required to post partially after you have created the inventory put-away, you can do so on setup times and quantities for all operations except the last one.</span></span> <span data-ttu-id="c4a32-128">I dette tilfellet styres den siste operasjonen av lagerplasseringen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-128">In that case, the last operation is controlled by the inventory put-away.</span></span>  

<span data-ttu-id="c4a32-129">Hvis du bare trenger å bokføre oppsett eller kjøretid i den siste operasjonen, kan du sette avgangsantallet i den siste operasjonen til 0.</span><span class="sxs-lookup"><span data-stu-id="c4a32-129">If you only need to post setup or run time on the last operation, then set the output quantity on the last operation to 0.</span></span> <span data-ttu-id="c4a32-130">Du kan også velge ikke å bokføre den siste linjen i det hele tatt ved å slette den.</span><span class="sxs-lookup"><span data-stu-id="c4a32-130">Alternatively, you can choose not to post the last line at all by simply deleting it</span></span>  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a><span data-ttu-id="c4a32-131">Slik plasserer du avgang med intern plassering eller flytting</span><span class="sxs-lookup"><span data-stu-id="c4a32-131">To put output away with a warehouse internal put-away</span></span>
1.  <span data-ttu-id="c4a32-132">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Intern plassering**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Whse. Internal Put-away**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c4a32-133">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-133">Choose the **New** action.</span></span>
3. <span data-ttu-id="c4a32-134">Fyll ut hodet til den nye interne plasseringen med minst feltet **Lokasjonskode**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-134">Fill in the header of a new internal put-away with at least the **Location Code**.</span></span>  
4. <span data-ttu-id="c4a32-135">Fyll ut en linje for hver vare du vil flytte til lageret.</span><span class="sxs-lookup"><span data-stu-id="c4a32-135">Fill in a line for each item you wish to move to the warehouse.</span></span> <span data-ttu-id="c4a32-136">Du trenger bare å fylle ut feltene **Varenr.** og **Antall**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-136">You only have to fill in the **Item No.** and the **Quantity** fields.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c4a32-137">Når du velger feltet **Varenr.**, åpnes **Hylleinnholdsoversikt** i stedet for **Vareoversikt**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-137">When you select the **Item No.** field, the **Bin Contents List** opens instead of the **Item List**.</span></span> <span data-ttu-id="c4a32-138">Det kommer av at du ønsker å plassere varer som er i en bestemt hylle (et hylleinnhold), ikke bare en vare, og du vet allerede hvilken hylle varen skal tas fra.</span><span class="sxs-lookup"><span data-stu-id="c4a32-138">This is because you want to put away an item that is in a particular bin - a Bin Content - not just an item, and you already know the bin the item should be taken from.</span></span>  

4.  <span data-ttu-id="c4a32-139">Hvis du vil fylle ut forslagslinjene med hele hylleinnholdet eller det filtrerte hylleinnholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-139">To fill the worksheet lines with the entire bin content or the filtered bin content of bins in the location, choose the **Get Bin Content** action.</span></span>  
5.  <span data-ttu-id="c4a32-140">Velg handlingen **Opprett plassering**. Varene du vil flytte ut av produksjon, er nå i plasseringsinstruksjoner og venter på å bli lagret i lageret.</span><span class="sxs-lookup"><span data-stu-id="c4a32-140">Choose the **Create Put-away** action, and the items you want to move out of production are now on put-away instructions waiting to be stored in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c4a32-141">Når lagerlokasjonen er definert til å bruke lagerstyring, er lageret koblet til produksjonsfunksjonen gjennom standardproduksjonshyllene: Dette er de inngående, utgående og åpne produksjonshyllene, som alle defineres på hurtigfanen **Hyller** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="c4a32-141">When your warehouse location is set up to use directed put-away and pick, the warehouse is linked to your manufacturing facility through the default production bins: the inbound and outbound production bins and the open shop bin, all of which you define on the **Bins** FastTab of the location card.</span></span> <span data-ttu-id="c4a32-142">Når du bokfører avgangen til en produksjonsordre, plasseres avgangen i den **utgående produksjonshyllen**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-142">When you post the output of a production order, the output is placed in the **Outbound Production Bin**.</span></span> <span data-ttu-id="c4a32-143">Du følger samme fremgangsmåte som den beskrevet ovenfor, til å plassere produksjonsavgangen, bortsett fra at i stedet for å bruke varens standardhylle vil du flytte eller plassere varene fra den **utgående produksjonshyllen** til varens standardhylle.</span><span class="sxs-lookup"><span data-stu-id="c4a32-143">You follow the same procedure as described above to put-away the production output, except that instead of using the item's default bin, you will move or put-away the items from the **Outbound Production Bin** to the item's default bin.</span></span>  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a><span data-ttu-id="c4a32-144">Angi en hylle for plassering av varer fra produksjonsavgang manuelt</span><span class="sxs-lookup"><span data-stu-id="c4a32-144">To manually specify a bin to store items from production output</span></span>  
1.  <span data-ttu-id="c4a32-145">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c4a32-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c4a32-146">Fyll ut hodet, og opprett en linje for hver vare du vil flytte til lageret.</span><span class="sxs-lookup"><span data-stu-id="c4a32-146">Fill in the header, and create a line for each item you wish to move to the warehouse.</span></span>  
3.  <span data-ttu-id="c4a32-147">Fyll ut både feltet **Fra hylle-kode** og feltet **Til hylle-kode**, og angi antallet i feltet **Antall**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-147">Fill in both the **From Bin Code** and the **To Bin Code** fields, and enter the quantity in the **Quantity** field.</span></span>  
4.  <span data-ttu-id="c4a32-148">Hvis du vil fylle ut forslagslinjene med hele hylleinnholdet eller det filtrerte hylleinnholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-148">To fill the worksheet lines with the entire bin content or the filtered bin content of bins in the location, choose the **Get Bin Content** action.</span></span>  
5. <span data-ttu-id="c4a32-149">Velg handlingen **Opprett flytting**.</span><span class="sxs-lookup"><span data-stu-id="c4a32-149">Choose the **Create Movement** action.</span></span> <span data-ttu-id="c4a32-150">Lagerflyttingsinstruksjonene opprettes med Hent- og Plasser-linjer som de lageransatte skal utføre.</span><span class="sxs-lookup"><span data-stu-id="c4a32-150">The warehouse movement instructions are created with Take and Place lines for warehouse employees to perform.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c4a32-151">Du kan ikke angi kildedokumentnummeret, for eksempel produksjonsordrenummeret, i dokumentene for intern plassering, plukking eller plassering for noen av disse prosedyrene.</span><span class="sxs-lookup"><span data-stu-id="c4a32-151">You cannot enter the source document number, such as the Production Order No., in the internal put-away, put-away, or movement documents for either of these procedures.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c4a32-152">Se også</span><span class="sxs-lookup"><span data-stu-id="c4a32-152">See Also</span></span>  
[<span data-ttu-id="c4a32-153">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="c4a32-153">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="c4a32-154">Lager</span><span class="sxs-lookup"><span data-stu-id="c4a32-154">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c4a32-155">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="c4a32-155">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="c4a32-156">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="c4a32-156">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="c4a32-157">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="c4a32-157">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="c4a32-158">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c4a32-158">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>