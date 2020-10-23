---
title: Planlegge lagerflyttinger i forslaget | Microsoft-dokumentasjon
description: Planlegge flyttinger i forslaget ved hjelp av en funksjon for etterfylling av hyller eller ved manuell planlegging av linjene du vil opprette som flytteinstruksjoner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4b5293ace8fe0fc59b0e1f499574355397fb2d84
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923223"
---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="49043-103">Planlegge lagerflyttinger i forslag</span><span class="sxs-lookup"><span data-stu-id="49043-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="49043-104">Planlegge flyttinger i forslaget ved hjelp av en funksjon for etterfylling av hyller eller ved manuell planlegging av linjene du vil opprette som flytteinstruksjoner.</span><span class="sxs-lookup"><span data-stu-id="49043-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="49043-105">Slik beregner du en etterfyllingsflytting</span><span class="sxs-lookup"><span data-stu-id="49043-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="49043-106">Etter hvert som lageret leverer varer til kundene, vil hyllene med de høyeste hylleprioriteringene inneholde færre og færre varer.</span><span class="sxs-lookup"><span data-stu-id="49043-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="49043-107">For å fylle opp disse hyllene med varer fra andre hyller, kjører du funksjonen **Beregn etterfylling av hylle** på siden **Flytteforslag**.</span><span class="sxs-lookup"><span data-stu-id="49043-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function on the **Movement Worksheet** page</span></span>

1.  <span data-ttu-id="49043-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="49043-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="49043-109">Velg handlingen **Beregn etterfylling av hyller**.</span><span class="sxs-lookup"><span data-stu-id="49043-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="49043-110">oppretter linjer som angir nøyaktig hvordan du skal flytte varer fra hyller med lav prioritering til hyller med høy prioritering.</span><span class="sxs-lookup"><span data-stu-id="49043-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="49043-111">En flytting blir foreslått i henhold til FEFO når du aktiverer funksjonen **Opprett flytting**, hvis følgende betingelser er oppfylt for en vare:</span><span class="sxs-lookup"><span data-stu-id="49043-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="49043-112">Varen har en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="49043-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="49043-113">Avmerkingsboksen **Plukk i henhold til FEFO** på lokasjonskortet er merket av.</span><span class="sxs-lookup"><span data-stu-id="49043-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="49043-114">Avmerkingsboksen **Hylle obligatorisk** på lokasjonskortet er merket av.</span><span class="sxs-lookup"><span data-stu-id="49043-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="49043-115">Feltene **Fra sone** og **Fra hylle** er tomme.</span><span class="sxs-lookup"><span data-stu-id="49043-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="49043-116">Hvis du vil ha mer informasjon, kan du se [Plukking etter FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="49043-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="49043-117">Se gjennom linjene og endre dem hvis det er nødvendig, eller slett noen av dem hvis det ikke er nok tid til å utføre alle.</span><span class="sxs-lookup"><span data-stu-id="49043-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="49043-118">Velg handlingen **Opprett flytting** for å lage en lagerinstruksjon som de lageransatte kan bruke.</span><span class="sxs-lookup"><span data-stu-id="49043-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="49043-119">Slik flytter du hele innholdet i én eller flere hyller med funksjonen Hent hylleinnhold</span><span class="sxs-lookup"><span data-stu-id="49043-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="49043-120">Du kan også bruke flytteforslaget til å planlegge andre flyttinger av beholdning i lageret.</span><span class="sxs-lookup"><span data-stu-id="49043-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="49043-121">Du kan for eksempel bruke denne handlingen når du vil plassere varer i en hylle for kvalitetskontroll, og deretter opprette en flytting for å lage instruksjoner for en ansatt.</span><span class="sxs-lookup"><span data-stu-id="49043-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="49043-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytteforslag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="49043-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="49043-123">Velg **Hent hylleinnhold**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="49043-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="49043-124">Bruk forespørselssiden til å filtrere hyller og varer som du vil skal vises på flytteforslagslinjene.</span><span class="sxs-lookup"><span data-stu-id="49043-124">Use the request page to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="49043-125">Fyll ut de aktuelle feltene på siden for forespørsel om kjørsel.</span><span class="sxs-lookup"><span data-stu-id="49043-125">Fill in the relevant fields in the batch job request page.</span></span> <span data-ttu-id="49043-126">Hvis du for eksempel vil se hylleinnholdet i alle hyllene i en bestemt sone i lokasjonen, fyller du ut **Sonekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="49043-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="49043-127">Hvis du vil hente linjer for hver hylle som inneholder en bestemt vare, fyller du ut **Varenr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="49043-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="49043-128">Du kan ikke manuelt flytte varer til eller fra en hylle av hylletypen RECEIVE, fordi varer som er i en slik hylle må registreres som plassert før de blir en del av det tilgjengelige lageret.</span><span class="sxs-lookup"><span data-stu-id="49043-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="49043-129">Hvis du skal hente mange linjer, velger du **Sorter** for å velge en sorteringsmetode for å definere rekkefølgen av linjene i forslaget og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="49043-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="49043-130">Flyttingslinjer hentes i henhold til FEFO når du aktiverer funksjonen **Hent hylleinnhold**, hvis følgende betingelser er oppfylt for en vare:</span><span class="sxs-lookup"><span data-stu-id="49043-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="49043-131">Varen har en utløpsdato.</span><span class="sxs-lookup"><span data-stu-id="49043-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="49043-132">Avmerkingsboksen **Plukk i henhold til FEFO** på lokasjonskortet er merket av.</span><span class="sxs-lookup"><span data-stu-id="49043-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="49043-133">Avmerkingsboksen **Hylle obligatorisk** på lokasjonskortet er merket av.</span><span class="sxs-lookup"><span data-stu-id="49043-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="49043-134">Feltene **Fra sone** og **Fra hylle** er tomme.</span><span class="sxs-lookup"><span data-stu-id="49043-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="49043-135">Fyll ut noen av de hentede linjene for å utføre endringene du vil utføre.</span><span class="sxs-lookup"><span data-stu-id="49043-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="49043-136">For hver vare som skal flyttes, må du fylle ut feltene **Varenr.**, **Fra hylle-kode**, **Til hylle-kode** og **Antall**.</span><span class="sxs-lookup"><span data-stu-id="49043-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="49043-137">Slett de uferdige linjene som du brukte til informasjon.</span><span class="sxs-lookup"><span data-stu-id="49043-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="49043-138">Når flytteforslagslinjene nøyaktig gjenspeiler hvordan flyttehandlingen skal utføres av den lageransatte, velger du handlingen **Opprett flytting** for å opprette instruksjonene for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="49043-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="49043-139">Se også</span><span class="sxs-lookup"><span data-stu-id="49043-139">See Also</span></span>  
[<span data-ttu-id="49043-140">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="49043-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="49043-141">Lager</span><span class="sxs-lookup"><span data-stu-id="49043-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="49043-142">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="49043-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="49043-143">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="49043-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="49043-144">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="49043-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="49043-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="49043-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
