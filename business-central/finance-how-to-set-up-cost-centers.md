---
title: Definere kostsentre | Microsoft-dokumentasjon
description: Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter. Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 48c1b9800c1e89246ba84122b4af56d75fdf6f9f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243529"
---
# <a name="set-up-cost-centers"></a><span data-ttu-id="962f7-104">Definere kostsentre</span><span class="sxs-lookup"><span data-stu-id="962f7-104">Set Up Cost Centers</span></span>
<span data-ttu-id="962f7-105">Kostsentre er avdelinger som er ansvarlig for kostnader og inntekter.</span><span class="sxs-lookup"><span data-stu-id="962f7-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="962f7-106">Diagrammet med kostsentre ligner dimensjonsinformasjonen for finans.</span><span class="sxs-lookup"><span data-stu-id="962f7-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="962f7-107">Du kan definere diagrammet med kostsentre på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="962f7-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="962f7-108">Overfør dimensjonsverdier i finans til diagrammet med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="962f7-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="962f7-109">Du kan foreta alle nødvendige justeringer etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="962f7-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="962f7-110">Opprett et nytt kostsenterdiagram som er uavhengig av finans, eller legg til et nytt kostsenter i et eksisterende kostsenterdiagram.</span><span class="sxs-lookup"><span data-stu-id="962f7-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="962f7-111">Du må opprette hvert enkelt kostsenter individuelt.</span><span class="sxs-lookup"><span data-stu-id="962f7-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="962f7-112">Slik overfører du dimensjonsverdier i finans til diagrammet med kostsentre:</span><span class="sxs-lookup"><span data-stu-id="962f7-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="962f7-113">Angi en dimensjon som kostsenterdimensjon på siden **Oppdater kostregnskapsdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="962f7-113">Set up a dimension to be the cost center dimension on the **Update Cost Acctg. Dimensions** page.</span></span> <span data-ttu-id="962f7-114">Det er bare verdier fra denne dimensjonen som overføres.</span><span class="sxs-lookup"><span data-stu-id="962f7-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="962f7-115">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostsentre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="962f7-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="962f7-116">I fanebladet **Handlinger**, under **Funksjoner** velger du **Hent kostsentre fra dimensjon** for å overføre dimensjonsverdier til kostsenterdiagrammet.</span><span class="sxs-lookup"><span data-stu-id="962f7-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="962f7-117">Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="962f7-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="962f7-118">Du kan konfigurere feltet **Juster kostsenterdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostsentre.</span><span class="sxs-lookup"><span data-stu-id="962f7-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="962f7-119">Du kan ikke definere en synkronisering av diagrammet med kostsentre til dimensjonsverdier fra finans.</span><span class="sxs-lookup"><span data-stu-id="962f7-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="962f7-120">Diagrammet med kostsentre inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.</span><span class="sxs-lookup"><span data-stu-id="962f7-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a><span data-ttu-id="962f7-121">Slik oppretter du nye kostsentre på siden Diagram med kostsentre:</span><span class="sxs-lookup"><span data-stu-id="962f7-121">To create new cost centers in the Chart of Cost Centers page</span></span>  
<span data-ttu-id="962f7-122">Du kan definere og vedlikeholde kostsentre i kortet **Kostsenterkort** eller på siden **Diagram med kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="962f7-122">You can set up and maintain cost centers in either the **Cost Center Card** card or on the **Chart of Cost Centers** page.</span></span> <span data-ttu-id="962f7-123">I denne fremgangsmåten definerer sentre på siden **Diagram med kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="962f7-123">In this procedure, you set up cost centers on the **Chart of Cost Centers** page.</span></span>  

1. <span data-ttu-id="962f7-124">Åpne siden **Diagram med kostsentre** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="962f7-124">Open the **Chart of Cost Centers** page in edit mode.</span></span>  
2. <span data-ttu-id="962f7-125">Angi kostsenterkoden i **Kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="962f7-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="962f7-126">Alle kostsentre må ha en kode.</span><span class="sxs-lookup"><span data-stu-id="962f7-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="962f7-127">Skriv inn navnet på kostsenteret i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="962f7-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="962f7-128">Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostsenteret.</span><span class="sxs-lookup"><span data-stu-id="962f7-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="962f7-129">For kostsentre av typen **Sum** må du fylle ut feltet **Sammentelling**.</span><span class="sxs-lookup"><span data-stu-id="962f7-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="962f7-130">Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostsentre.</span><span class="sxs-lookup"><span data-stu-id="962f7-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="962f7-131">Når det gjelder kostsentre av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="962f7-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="962f7-132">Fyll ut feltene **Sorteringsrekkefølge** og **Kostundertype**.</span><span class="sxs-lookup"><span data-stu-id="962f7-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="962f7-133">Velg den neste tomme linjen for å opprette et nytt kostsenter, og gjenta deretter trinn 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="962f7-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="962f7-134">Når du har definert alle kostsentrene, velger du **Rykk inn kostsentre**.</span><span class="sxs-lookup"><span data-stu-id="962f7-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="962f7-135">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="962f7-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="962f7-136">Hvis du har angitt definisjoner i **Sammentelling**-feltene for **Til-sum**-kostsentre før du kjører innrykksfunksjonen, må du angi dem på nytt.</span><span class="sxs-lookup"><span data-stu-id="962f7-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="962f7-137">Funksjonen overskriver verdiene i alle **Til-sum**-felt.</span><span class="sxs-lookup"><span data-stu-id="962f7-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="962f7-138">Se også</span><span class="sxs-lookup"><span data-stu-id="962f7-138">See Also</span></span>  
[<span data-ttu-id="962f7-139">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="962f7-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="962f7-140">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="962f7-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="962f7-141">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="962f7-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="962f7-142">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="962f7-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="962f7-143">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="962f7-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
