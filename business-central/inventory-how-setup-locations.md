---
title: Definer et lokasjonskort og definere overføringsruter
description: Du oppretter et lokasjonskort for hvert sted der du oppbevarer lagervarer, for eksempel et lager eller distribusjonssenter, og definerer ruter for å overføre varer mellom lokasjoner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184327"
---
# <a name="set-up-locations"></a><span data-ttu-id="3928f-103">Definer lokasjoner</span><span class="sxs-lookup"><span data-stu-id="3928f-103">Set Up Locations</span></span>

<span data-ttu-id="3928f-104">Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.</span><span class="sxs-lookup"><span data-stu-id="3928f-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="3928f-105">[!INCLUDE [prod_short](includes/prod_short.md)] bruker lokasjoner til å holde oversikt over lageret både i enklere tilfeller og de mer sammensatte lagerprosessene.</span><span class="sxs-lookup"><span data-stu-id="3928f-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="3928f-106">Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="3928f-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="3928f-107">Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="3928f-108">Lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="3928f-108">Location cards</span></span>

<span data-ttu-id="3928f-109">Lokasjonskortet angir opplysninger om en lokasjon, for eksempel et lager eller distribusjonssenter.</span><span class="sxs-lookup"><span data-stu-id="3928f-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="3928f-110">Du gir hver lokasjon et navn og en kode som representerer lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3928f-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="3928f-111">Deretter kan du angi lokasjonskoden i andre deler av programmet når du vil registrere transaksjoner for en gitt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="3928f-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="3928f-112">Du kan angi opplysninger om hyller og lagerprinsipper for hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="3928f-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="3928f-113">Basert på lagerprinsippet du velger, kan du bruke alternativene i hurtigfanen **Hyller** til å definere hyllene som skal brukes som standardhyller når du foretar transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="3928f-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="3928f-114">Hvis du bruker lagerstyring, bruker du de fleste av disse alternativene i hurtigfanen **Hylleprinsipp** til å definere hvordan du vil bruke de forskjellige avanserte lagerfunksjonene.</span><span class="sxs-lookup"><span data-stu-id="3928f-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="3928f-115">Noen alternativfelt er nedtonet og deaktivert av andre innstillinger på siden **Lokasjonskort** for å begrense oppsettskombinasjoner som ikke støttes.</span><span class="sxs-lookup"><span data-stu-id="3928f-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="3928f-116">Velg handlingen **Soner** eller **Hyller** for å vise informasjon om soner og hyller som kan være definert for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="3928f-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="3928f-117">Slik oppretter du et lokasjonskort</span><span class="sxs-lookup"><span data-stu-id="3928f-117">To create a location card</span></span>

1. <span data-ttu-id="3928f-118">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3928f-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="3928f-119">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3928f-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="3928f-120">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="3928f-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="3928f-121">Gjenta trinn 2 og 3 for hver beholdninglokasjon.</span><span class="sxs-lookup"><span data-stu-id="3928f-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="3928f-122">Mange felt på lokasjonskortet refererer til håndteringen av varer i inngående og utgående lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="3928f-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="3928f-123">Feltene er ikke relevante for selskaper som ikke trenger den mer komplekse lagerfunksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="3928f-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="3928f-124">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="3928f-125">Du kan endre konfigurasjonen for en lokasjon senere, men du kan ikke redigere oppsettet av lokasjoner som har vareposter.</span><span class="sxs-lookup"><span data-stu-id="3928f-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="3928f-126">Hvis du har flere lokasjoner, kan du definere overføringsruter mellom lokasjonene.</span><span class="sxs-lookup"><span data-stu-id="3928f-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="3928f-127">Slik oppretter du overføringsruter</span><span class="sxs-lookup"><span data-stu-id="3928f-127">To create a transfer route</span></span>

1. <span data-ttu-id="3928f-128">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overføringsruter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3928f-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="3928f-129">Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.</span><span class="sxs-lookup"><span data-stu-id="3928f-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="3928f-130">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="3928f-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="3928f-131">På siden **Lokasjonskort** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="3928f-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="3928f-132">Nå kan du overføre lagervarer mellom to lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="3928f-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="3928f-133">Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="3928f-134">Hyller</span><span class="sxs-lookup"><span data-stu-id="3928f-134">Bins</span></span>

<span data-ttu-id="3928f-135">Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer.</span><span class="sxs-lookup"><span data-stu-id="3928f-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="3928f-136">Når du har opprettet hyllene, kan du definere nøyaktig det innholdet du vil plassere i hver hylle, eller hyllen kan fungere som en mobil hylle uten angitt innhold.</span><span class="sxs-lookup"><span data-stu-id="3928f-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="3928f-137">Hyller brukes for øyeblikket i enkle og avanserte lageroperasjoner.</span><span class="sxs-lookup"><span data-stu-id="3928f-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="3928f-138">Hvis du administrerer lagerbeholdningen i et mer enkelt oppsett, trenger du sannsynligvis ikke hyller.</span><span class="sxs-lookup"><span data-stu-id="3928f-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="3928f-139">Hvis du vil bruke hyllefunksjonaliteten i en lokasjon, må du først aktivere funksjonaliteten på kortet **Lokasjon** ved å velge feltet **Hylle obligatorisk** på hurtigfanen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="3928f-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="3928f-140">Du utformer deretter vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.</span><span class="sxs-lookup"><span data-stu-id="3928f-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="3928f-141">Før du kan angi hyllekoder på lokasjonskortet, må hyllekodene være opprettet.</span><span class="sxs-lookup"><span data-stu-id="3928f-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="3928f-142">Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="3928f-143">Soner</span><span class="sxs-lookup"><span data-stu-id="3928f-143">Zones</span></span>

<span data-ttu-id="3928f-144">Hvis du vil strukturere hyllene under soner, kan du gjøre det på siden **Soner**.</span><span class="sxs-lookup"><span data-stu-id="3928f-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="3928f-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopierer feltene som du definerer for en bestemt sone, til hyllene som hører til den.</span><span class="sxs-lookup"><span data-stu-id="3928f-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="3928f-146">På denne måten kan du tilordne en sone til en hylle eller en hyllemal (hyllefilter), og flere andre felter fylles ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="3928f-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="3928f-147">Du kan også velge å definere bare en sone og organisere lageret bare ut fra hyllene.</span><span class="sxs-lookup"><span data-stu-id="3928f-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="3928f-148">Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3928f-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="3928f-149">Se også</span><span class="sxs-lookup"><span data-stu-id="3928f-149">See Also</span></span>

[<span data-ttu-id="3928f-150">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="3928f-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3928f-151">Overføre beholdning mellom lokasjoner</span><span class="sxs-lookup"><span data-stu-id="3928f-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="3928f-152">Opprette hyller</span><span class="sxs-lookup"><span data-stu-id="3928f-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="3928f-153">Definere hylletyper</span><span class="sxs-lookup"><span data-stu-id="3928f-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="3928f-154">Definere lagerstyring</span><span class="sxs-lookup"><span data-stu-id="3928f-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="3928f-155">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3928f-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3928f-156">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="3928f-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="3928f-157">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="3928f-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]