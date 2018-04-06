---
title: Definere kostsentre | Microsoft-dokumentasjon
description: Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter. Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 38b6ce01e48f1b32c28b1883875a566d19f02ea3
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="4ebe8-104">Definere kostsentre</span><span class="sxs-lookup"><span data-stu-id="4ebe8-104">Set Up Cost Centers</span></span>
<span data-ttu-id="4ebe8-105">Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="4ebe8-106">Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="4ebe8-107">Du kan definere diagrammet med kostsentre på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="4ebe8-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="4ebe8-108">Overfør dimensjonsverdier i finans til diagrammet med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="4ebe8-109">Du kan foreta alle nødvendige justeringer etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="4ebe8-110">Opprett et nytt kostsenterdiagram som er uavhengig av finans, eller legg til et nytt kostsenter i et eksisterende kostsenterdiagram.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="4ebe8-111">Du må opprette hvert enkelt kostsenter individuelt.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="4ebe8-112">Slik overfører du dimensjonsverdier i finans til diagrammet med kostsentre:</span><span class="sxs-lookup"><span data-stu-id="4ebe8-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="4ebe8-113">Angi en dimensjon som kostsenterdimensjon i vinduet **Oppdater kostregnskapsdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="4ebe8-114">Det er bare verdier fra denne dimensjonen som overføres.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="4ebe8-115">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Diagram med kostsentre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="4ebe8-116">I fanebladet **Handlinger**, under **Funksjoner** velger du **Hent kostsentre fra dimensjon** for å overføre dimensjonsverdier til kostsenterdiagrammet.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="4ebe8-117">Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="4ebe8-118">Du kan konfigurere feltet **Juster kostsenterdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="4ebe8-119">Du kan ikke definere en synkronisering av diagrammet med kostsentre til dimensjonsverdier fra finans.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="4ebe8-120">Diagrammet med kostsentre inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="4ebe8-121">Slik oppretter du nye kostsentre i vinduet Diagram med kostsentre:</span><span class="sxs-lookup"><span data-stu-id="4ebe8-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="4ebe8-122">Du kan definere og vedlikeholde kostsentre i kortet **Kostsenterkort** eller vinduet **Diagram med kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="4ebe8-123">I denne fremgangsmåten definerer sentre i vinduet **Diagram med kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="4ebe8-124">Åpne vinduet **Diagram med kostsentre** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="4ebe8-125">Angi kostsenterkoden i **Kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="4ebe8-126">Alle kostsentre må ha en kode.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="4ebe8-127">Skriv inn navnet på kostsenteret i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="4ebe8-128">Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="4ebe8-129">For kostsentre av typen **Sum** må du fylle ut feltet **Sammentelling**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="4ebe8-130">Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostsentre.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="4ebe8-131">Når det gjelder kostsentre av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="4ebe8-132">Fyll ut feltene **Sorteringsrekkefølge** og **Kostundertype**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="4ebe8-133">Velg den neste tomme linjen for å opprette et nytt kostsenter, og gjenta deretter trinn 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="4ebe8-134">Når du har definert alle kostsentrene, velger du **Rykk inn kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="4ebe8-135">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="4ebe8-136">Hvis du har angitt definisjoner i **Sammentelling**-feltene for **Til-sum**-kostsentre før du kjører innrykksfunksjonen, må du angi dem på nytt.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="4ebe8-137">Funksjonen overskriver verdiene i alle **Til-sum**-felt.</span><span class="sxs-lookup"><span data-stu-id="4ebe8-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ebe8-138">Se også</span><span class="sxs-lookup"><span data-stu-id="4ebe8-138">See Also</span></span>  
[<span data-ttu-id="4ebe8-139">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="4ebe8-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="4ebe8-140">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="4ebe8-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="4ebe8-141">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="4ebe8-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="4ebe8-142">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="4ebe8-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="4ebe8-143">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ebe8-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

