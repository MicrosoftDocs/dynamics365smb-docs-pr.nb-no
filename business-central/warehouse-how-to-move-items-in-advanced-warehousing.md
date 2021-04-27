---
title: Flytte varer i avanserte lageroppsett | Microsoft-dokumentasjon
description: I avanserte lageroppsett, det vil si lokasjoner med lagerstyring, utføres lagerflyttinger mellom hyller av en overordnet ansatt som klargjør lagerflyttinger i flytteforslaget, og deretter oppretter lagerflyttingene som ansatte på lageret utfører.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e843b048c117539d077dc4a8ecba33f265a2e826
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782637"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a><span data-ttu-id="b22ab-103">Flytte varer i avanserte lageroppsett</span><span class="sxs-lookup"><span data-stu-id="b22ab-103">Move Items in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="b22ab-104">I avanserte lageroppsett, det vil si lokasjoner med lagerstyring, utføres lagerflyttinger mellom hyller av en overordnet ansatt som klargjør lagerflyttinger i flytteforslaget, og deretter oppretter lagerflyttingene som ansatte på lageret utfører.</span><span class="sxs-lookup"><span data-stu-id="b22ab-104">In advanced warehouse configurations, that is, locations with directed put-away and pick, warehouse movements between bins are performed by a senior employee preparing warehouse movements in the movement worksheet and then creating the warehouse movements for warehouse employees to perform.</span></span>  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a><span data-ttu-id="b22ab-105">Flytte varer med lagerflytteforslaget</span><span class="sxs-lookup"><span data-stu-id="b22ab-105">To move items with the warehouse movement worksheet</span></span>
<span data-ttu-id="b22ab-106">**Flytteforslag**-siden har to funksjoner som kan hjelpe til med automatisk utfylling på linjene.</span><span class="sxs-lookup"><span data-stu-id="b22ab-106">The **Movement Worksheet** page has two functions that can assist in automatically filling in the lines.</span></span> <span data-ttu-id="b22ab-107">Den første er funksjonen **Beregn etterfylling av hylle**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-107">The first is the **Calculate Bin Replenishment** function.</span></span> <span data-ttu-id="b22ab-108">Denne funksjonen bruker hylleprioriteringene til å foreslå etterfylling til høyt prioriterte hyller fra hyller med lav prioritering. Den andre er funksjonen **Hent hylleinnhold**, som fyller ut forslagslinjene med hele hylleinnholdet i hyllen eller hyllene du angir.</span><span class="sxs-lookup"><span data-stu-id="b22ab-108">This function uses the bin rankings to suggest replenishment for high-ranking bins from low-ranking bins. The second is the **Get Bin Content** function, which fills in the worksheet lines with the entire bin contents of the bin or bins you specify.</span></span>

1.  <span data-ttu-id="b22ab-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b22ab-110">Skriv inn aktuelle opplysninger om lagerflyttingen på forslagslinjene.</span><span class="sxs-lookup"><span data-stu-id="b22ab-110">Enter the warehouse movement information on the worksheet lines as appropriate.</span></span>  
3. <span data-ttu-id="b22ab-111">Velg handlingen **Opprett flytting** for å opprette et lagerflyttingsdokument som deretter kan registreres når lagerflyttingen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="b22ab-111">Choose the **Create Movement** action to create a warehouse movement document which can then be registered when the warehouse movement is completed.</span></span>  

### <a name="to-register-the-warehouse-movement"></a><span data-ttu-id="b22ab-112">Slik registrerer du lagerflyttingen</span><span class="sxs-lookup"><span data-stu-id="b22ab-112">To register the warehouse movement</span></span>  
1.  <span data-ttu-id="b22ab-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flyttinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movements**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b22ab-114">Åpne lagerflyttingen du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="b22ab-114">Open the warehouse movement that you want to process.</span></span>  
3.  <span data-ttu-id="b22ab-115">På linjer av handlingstype **Plasser** angir du hvor, hvilke, og når den aktuelle varen skal flyttes ved å redigere feltene **Sonekode**, **Hyllekode**, **Ant. som skal håndt.** eller **Forfallsdato**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-115">On lines of action type **Place**, specify where, which, and when to move the item in question by editing the **Zone Code**, **Bin Code**, **Qty. to Handle**, or **Due Date** fields.</span></span>  

    <span data-ttu-id="b22ab-116">Hvis lageret er definert slik at hyllekodene følger strukturen i lageret, kan du ta flere varer fra påfølgende hyller med store enheter, og plassere dem i hyller for forhåndsplukking, som også kan være plassert nær hverandre.</span><span class="sxs-lookup"><span data-stu-id="b22ab-116">If your warehouse has been set up so the bin codes follow the physical structure of the warehouse, you can take quantities of several items from successive bulk bins and then place them in forward picking bins, which also might be close to one another.</span></span>  
4.  <span data-ttu-id="b22ab-117">På linjer av handlingstype **Hent** angir du i feltet **Ant. som skal håndt.** et delantall av hylleinnholdet som du vil flytte.</span><span class="sxs-lookup"><span data-stu-id="b22ab-117">On lines of action type **Take**, specify in the **Qty. to Handle** field a part quantity of the bin content that you want to move.</span></span> <span data-ttu-id="b22ab-118">Alle andre felt på linjer for handlingstypen **Hent** er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="b22ab-118">All other fields on lines of action type **Take** are read-only.</span></span>  
5.  <span data-ttu-id="b22ab-119">Hvis du vil flytte alle foreslåtte antall som er angitt i **Antall**-feltet, velger du handlingen **Autoutfyll ant som skal håndt**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-119">To move all suggested quantities as specified in the **Quantity** field, choose the **Autofill Qty. to Handle** action.</span></span>  
6. <span data-ttu-id="b22ab-120">Velg handlingen **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-120">Choose the **Register** action.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b22ab-121">Hvis lokasjonen bruker lagerstyring, kan du ikke manuelt flytte varer til eller fra hyller av hylletypen MOTTA, fordi varer som er i slike hyller må registreres som plassert før de blir en del av det tilgjengelige lageret.</span><span class="sxs-lookup"><span data-stu-id="b22ab-121">If the location uses directed put-away and pick, then you cannot manually move items in or out of bins of bin type RECEIVE, because items in such bins must be registered as being put away before they are part of available inventory.</span></span>

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a><span data-ttu-id="b22ab-122">Slik registrerer du vareflytting som allerede har funnet sted</span><span class="sxs-lookup"><span data-stu-id="b22ab-122">To register the movement of an item that has already occurred</span></span>  
<span data-ttu-id="b22ab-123">Hvis lokasjonen bruker lagerstyring og du trenger å flytte varer til andre hyller uten at det finnes en eksisterende plassering, plukking eller flytting, kan du registrere den riktige plasseringen av varene i lageret ved hjelp av **Lagerreklassifiseringskladd**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-123">If your location uses directed put-away and pick, and you need to move items to other bins without a pre-existing warehouse put-away, pick, or movement, you can register the correct placement of the items in the warehouse using the **Whse. Reclassification Journal**.</span></span>

1.  <span data-ttu-id="b22ab-124">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerreklassifiseringskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b22ab-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Whse. Reclassification Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b22ab-125">Fyll ut feltene **Varenr.**, **Fra sone-kode**, **Fra hylle-kode**, **Til sone-kode**, **Til hylle-kode**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-125">Fill in the **Item No.**, **From Zone Code**, **From Bin Code**, **To Zone Code**, and **To Bin Code** fields.</span></span>  
3.  <span data-ttu-id="b22ab-126">Velg handlingen **Registrer**.</span><span class="sxs-lookup"><span data-stu-id="b22ab-126">Choose the **Register** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b22ab-127">Se også</span><span class="sxs-lookup"><span data-stu-id="b22ab-127">See Also</span></span>  
[<span data-ttu-id="b22ab-128">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="b22ab-128">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b22ab-129">Lager</span><span class="sxs-lookup"><span data-stu-id="b22ab-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b22ab-130">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b22ab-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b22ab-131">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b22ab-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b22ab-132">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="b22ab-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b22ab-133">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b22ab-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]