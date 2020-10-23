---
title: Spore varesporede varer | Microsoft-dokumentasjon
description: Du kan vise hvor en varesporet vare er brukt, inkludert hvordan og når den ble mottatt eller produsert, overført, solgt, forbrukt eller returnert. Du kan også finne alle gjeldende forekomster av et bestemt serie- eller partinummer i databasen. Dette gjør du ved hjelp av funksjonene Varesporing og Naviger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9b9e77925a46f57b3c45a21f86ae583024146ff4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916096"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="2d460-105">Spore varesporede varer</span><span class="sxs-lookup"><span data-stu-id="2d460-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="2d460-106">Du kan vise hvor en varesporet vare er brukt, inkludert hvordan og når den ble mottatt eller produsert, overført, solgt, forbrukt eller returnert.</span><span class="sxs-lookup"><span data-stu-id="2d460-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="2d460-107">Du kan også finne alle gjeldende forekomster av et bestemt serie- eller partinummer i databasen.</span><span class="sxs-lookup"><span data-stu-id="2d460-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="2d460-108">Dette gjør du ved hjelp av funksjonene Varesporing og [Søk etter poster](ui-find-entries.md).</span><span class="sxs-lookup"><span data-stu-id="2d460-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="2d460-109">Disse funksjonene kan være spesielt nyttige i kvalitetskontroll når du må finne ut hvilke kunder som mottok produkter fra et bestemt partinummer, eller når du må finne ut hvilket parti en defekt komponent kom fra.</span><span class="sxs-lookup"><span data-stu-id="2d460-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="2d460-110">På siden **Varesporing** kan du spore fremover og bakover i en sekvens med bokførte lagertransaksjoner for serie- eller partinummeret.</span><span class="sxs-lookup"><span data-stu-id="2d460-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="2d460-111">Du kan ikke se transaksjonssekvensen på siden **Søk etter poster**, men du kan se alle postene for serie- eller partinummeret, både bokførte poster og åpne poster.</span><span class="sxs-lookup"><span data-stu-id="2d460-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="2d460-112">De to funksjonene kan brukes i kombinasjon ved å overføre et sporet serie- eller partinummer på siden **Søk etter poster** hvis du vil fullføre et fullstendig sporingsscenario.</span><span class="sxs-lookup"><span data-stu-id="2d460-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <span data-ttu-id="2d460-113">Hvis du vil ha mer informasjon, kan du se [Gjennomgang: spore serie-/partinumre](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="2d460-113">For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>  

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="2d460-114">Slik sporer du varesporede varer</span><span class="sxs-lookup"><span data-stu-id="2d460-114">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="2d460-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varesporing**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2d460-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2d460-116">Angi de bestemte varenumrene eller et filter på varenumrene du vil spore, i filterfeltene øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="2d460-116">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="2d460-117">Velg om du også vil vise hvor komponentene for varen kommer fra, i feltet **Vis komponenter**.</span><span class="sxs-lookup"><span data-stu-id="2d460-117">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="2d460-118">Alternativene i dette feltet er som følger.</span><span class="sxs-lookup"><span data-stu-id="2d460-118">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="2d460-119">Felt</span><span class="sxs-lookup"><span data-stu-id="2d460-119">Field</span></span>|<span data-ttu-id="2d460-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2d460-120">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="2d460-121">**Nei**</span><span class="sxs-lookup"><span data-stu-id="2d460-121">**No**</span></span>|<span data-ttu-id="2d460-122">Velg dette alternativet hvis du ikke vil vise noen komponenter.</span><span class="sxs-lookup"><span data-stu-id="2d460-122">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="2d460-123">**Bare varesporet**</span><span class="sxs-lookup"><span data-stu-id="2d460-123">**Item-tracked Only**</span></span>|<span data-ttu-id="2d460-124">Velg dette alternativet hvis du bare vil vise komponenter som har parti- eller serienumre.</span><span class="sxs-lookup"><span data-stu-id="2d460-124">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="2d460-125">**Alle**</span><span class="sxs-lookup"><span data-stu-id="2d460-125">**All**</span></span>|<span data-ttu-id="2d460-126">Velg dette alternativet hvis du vil vise alle komponentene.</span><span class="sxs-lookup"><span data-stu-id="2d460-126">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="2d460-127">Velg metoden du vil bruke til å spore varen, i feltet **Sporingsmetode**.</span><span class="sxs-lookup"><span data-stu-id="2d460-127">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="2d460-128">Du kan velge mellom følgende alternativer</span><span class="sxs-lookup"><span data-stu-id="2d460-128">The options are as follows</span></span>  

    |<span data-ttu-id="2d460-129">Felt</span><span class="sxs-lookup"><span data-stu-id="2d460-129">Field</span></span>|<span data-ttu-id="2d460-130">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2d460-130">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="2d460-131">**Forbruk->opprinnelse**</span><span class="sxs-lookup"><span data-stu-id="2d460-131">**Usage->Origin**</span></span>|<span data-ttu-id="2d460-132">Denne metoden sporer varen fra der den ble brukt, til der den kom fra.</span><span class="sxs-lookup"><span data-stu-id="2d460-132">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="2d460-133">Hvis en produsert vare for eksempel ble solgt til en kunde, vises dette på siden **Varesporing** med følgeseddellinjen først, som du deretter kan utvide for å vise hvilken produksjonsordre den kom fra.</span><span class="sxs-lookup"><span data-stu-id="2d460-133">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="2d460-134">**Opprinnelse->forbruk**</span><span class="sxs-lookup"><span data-stu-id="2d460-134">**Origin->Usage**</span></span>|<span data-ttu-id="2d460-135">Denne metoden sporer varen fra der den kom inn på lageret, til der den ble brukt.</span><span class="sxs-lookup"><span data-stu-id="2d460-135">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="2d460-136">Hvis en produsert vare ble solgt til en kunde, vises dette på siden **Varesporing** med den ferdige produksjonsordren først, som du deretter kan utvide for å vise følgeseddellinjer der varen ble brukt.</span><span class="sxs-lookup"><span data-stu-id="2d460-136">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="2d460-137">Velg **Spor** for å kjøre sporingen.</span><span class="sxs-lookup"><span data-stu-id="2d460-137">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d460-138">Hvis du har mottatt samme parti i flere transaksjoner, vises kanskje ikke alle transaksjonene på siden **Varesporing**.</span><span class="sxs-lookup"><span data-stu-id="2d460-138">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="2d460-139">Det vises bare utlignede transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="2d460-139">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d460-140">Hvis ytterligere transaksjonshistorikk under en varesporingslinje allerede er sporet av en annen linje ovenfor, er det merket av for **Allerede sporet**.</span><span class="sxs-lookup"><span data-stu-id="2d460-140">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="2d460-141">For en enklere visning vises ikke slike underliggende linjer.</span><span class="sxs-lookup"><span data-stu-id="2d460-141">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="2d460-142">Når du skal søke etter varesporingslinjer der transaksjonsloggen allerede er sporet, velger du knappen **Gå til allerede sporet**.</span><span class="sxs-lookup"><span data-stu-id="2d460-142">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="2d460-143">Den aktuelle varesporingslinjen velges, og alle underliggende linjer utvides.</span><span class="sxs-lookup"><span data-stu-id="2d460-143">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="2d460-144">Slik søker du etter varesporede varer med Søk etter poster:</span><span class="sxs-lookup"><span data-stu-id="2d460-144">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="2d460-145">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Søk etter poster**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2d460-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="2d460-146">Velg **Handlinger** > **Finn etter** > **Finn etter varereferanse**.</span><span class="sxs-lookup"><span data-stu-id="2d460-146">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="2d460-147">I feltene **Serienr.** og **Partinr.** angir du varesporingsnumrene du vil spore.</span><span class="sxs-lookup"><span data-stu-id="2d460-147">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="2d460-148">Velg **Søk** for å finne alle forekomster av serie- eller partinummeret i databasen.</span><span class="sxs-lookup"><span data-stu-id="2d460-148">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d460-149">Se også</span><span class="sxs-lookup"><span data-stu-id="2d460-149">See Also</span></span>  
[<span data-ttu-id="2d460-150">Lager</span><span class="sxs-lookup"><span data-stu-id="2d460-150">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2d460-151">[Designdetaljer: Varesporing](design-details-item-tracking.md)
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)</span><span class="sxs-lookup"><span data-stu-id="2d460-151">[Design Details: Item Tracking](design-details-item-tracking.md)
[Design Details - Item Tracking and Reservations](design-details-item-tracking-and-reservations.md)</span></span>  
[<span data-ttu-id="2d460-152">Reservere varer</span><span class="sxs-lookup"><span data-stu-id="2d460-152">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="2d460-153">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Gjennomgang: spore serie-/partinumre](walkthrough-tracing-serial-lot-numbers.md)</span><span class="sxs-lookup"><span data-stu-id="2d460-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)</span></span>  
[<span data-ttu-id="2d460-154">Søk etter poster</span><span class="sxs-lookup"><span data-stu-id="2d460-154">Find Entries</span></span>](ui-find-entries.md)  
