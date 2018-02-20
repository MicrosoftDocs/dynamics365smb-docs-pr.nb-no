---
title: Beregne etterfylling av hylle | Microsoft-dokumentasjon
description: "Når lokasjonen er definert til å bruke lagerstyring, tas det hensyn til prioriteringene av plasseringsmalene for lokasjonen ved plassering av mottak."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e667ca56aa22fafc7fe6d0a4880c419a4272db26
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="fa718-103">Beregn etterfylling av hylle</span><span class="sxs-lookup"><span data-stu-id="fa718-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="fa718-104">Når lokasjonen er definert til å bruke lagerstyring, tas det hensyn til prioriteringene av plasseringsmalene for lokasjonen ved plassering av mottak.</span><span class="sxs-lookup"><span data-stu-id="fa718-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="fa718-105">Prioriteter inkluderer minimums- og maksimumsantall for hylleinnhold som er fastsatt for en bestemt hylle, og hylleprioriteringene.</span><span class="sxs-lookup"><span data-stu-id="fa718-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="fa718-106">Hvis varene ankommer jevnlig, vil de mest brukte plukkhyllene derfor bli fylt opp etter hvert som de blir tømt.</span><span class="sxs-lookup"><span data-stu-id="fa718-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="fa718-107">Lagerbeholdningen ankommer imidlertid ikke alltid jevnt.</span><span class="sxs-lookup"><span data-stu-id="fa718-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="fa718-108">Noen ganger kjøpes varer i store antall slik at selskapet kan få en rabatt, eller produksjonsenheten kan produsere en stor mengde av én vare for å oppnå en lav enhetskostnad.</span><span class="sxs-lookup"><span data-stu-id="fa718-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="fa718-109">Varene vil deretter ikke bli mottatt i lageret igjen på en stund, og lageret må jevnlig flytte varer til plukkhyller fra masselagringsområder.</span><span class="sxs-lookup"><span data-stu-id="fa718-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="fa718-110">Det kan også være at lageret forventer at en lagervare skal ankomme snart, og ønsker å tømme masselagringsområdet for varer før de nye varene ankommer.</span><span class="sxs-lookup"><span data-stu-id="fa718-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="fa718-111">Og endelig, hvis du har definert masselagringshyllene med bare hylletypehandlingen **Plassering**, som betyr at **Plukk**-handlingen ikke er valg for hylletypen, må du alltid sørge for etterfylling av plukkhyllene, fordi en plukking av beholdning ikke foreslås for hyller av typen Plassering.</span><span class="sxs-lookup"><span data-stu-id="fa718-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="fa718-112">Slik etterfyller du plukkhyller</span><span class="sxs-lookup"><span data-stu-id="fa718-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="fa718-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fa718-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fa718-114">Velg handlingen **Beregn etterfylling av hylle** for åpne rapportforespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="fa718-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="fa718-115">Fyll ut kjørselvinduet for å begrense omfanget av etterfyllingsforslaget som skal beregnes.</span><span class="sxs-lookup"><span data-stu-id="fa718-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="fa718-116">Du kan for eksempel ønske å begrense deg til bestemte varer, soner eller hyller.</span><span class="sxs-lookup"><span data-stu-id="fa718-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="fa718-117">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="fa718-117">Choose the **OK** button.</span></span> <span data-ttu-id="fa718-118">Det opprettes linjer for etterfyllingsflyttingene som må utføres, i henhold til reglene som er definert for hyllene og hylleinnholdet, det vil si varer i hyller.</span><span class="sxs-lookup"><span data-stu-id="fa718-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="fa718-119">Hvis du ønsker å utføre alle de foreslåtte etterfyllingene, velger du **Opprett flytting**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="fa718-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="fa718-120">De ansatte kan nå finne instruksjoner på menyelementet **Flyttinger**, utføre dem og registrere dem.</span><span class="sxs-lookup"><span data-stu-id="fa718-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="fa718-121">Hvis du bare vil at noen av forslagene skal utføres, sletter du de linjene som er mindre viktige, og deretter oppretter du en flytting.</span><span class="sxs-lookup"><span data-stu-id="fa718-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="fa718-122">Neste gang du beregner etterfylling av en hylle, vil forslagene du har slettet, bli opprettet på nytt hvis de fremdeles er gyldige på det tidspunktet.</span><span class="sxs-lookup"><span data-stu-id="fa718-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="fa718-123">Hvis følgende betingelser er oppfylt for en vare:</span><span class="sxs-lookup"><span data-stu-id="fa718-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="fa718-124">varen har en utløpsdato</span><span class="sxs-lookup"><span data-stu-id="fa718-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="fa718-125">Feltet **Plukk i henhold til FEFO** er merket av på lokasjonskortet, og</span><span class="sxs-lookup"><span data-stu-id="fa718-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="fa718-126">Du bruker funksjonaliteten **Beregn etterfylling av hyller**</span><span class="sxs-lookup"><span data-stu-id="fa718-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="fa718-127">vil feltene **Fra sone** og **Fra hylle** være tomme fordi algoritmen for å beregne hvor varene skal flyttes fra, bare utløses når du aktiverer funksjonen **Opprett flytting**.</span><span class="sxs-lookup"><span data-stu-id="fa718-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa718-128">Se også</span><span class="sxs-lookup"><span data-stu-id="fa718-128">See Also</span></span>  
[<span data-ttu-id="fa718-129">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="fa718-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="fa718-130">Plukking etter FEFO</span><span class="sxs-lookup"><span data-stu-id="fa718-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="fa718-131">Lager</span><span class="sxs-lookup"><span data-stu-id="fa718-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="fa718-132">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="fa718-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="fa718-133">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="fa718-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="fa718-134">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="fa718-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="fa718-135">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fa718-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

