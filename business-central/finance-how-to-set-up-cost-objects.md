---
title: Definere kostobjekter | Microsoft-dokumentasjon
description: Lær hvordan du definerer kostobjekter, som ligner på dimensjonene i Finans.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: ae2ca5b4c6f63a004d42c2ae1ef9f0efa95dd02c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306031"
---
# <a name="set-up-cost-objects"></a><span data-ttu-id="27978-103">Definere kostobjekter</span><span class="sxs-lookup"><span data-stu-id="27978-103">Set Up Cost Objects</span></span>
<span data-ttu-id="27978-104">Kostobjekter er et selskaps prosjekter, produkter eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="27978-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="27978-105">Diagrammet med kostobjekter ligner dimensjonsinformasjonen for finans.</span><span class="sxs-lookup"><span data-stu-id="27978-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="27978-106">Du kan definere diagrammet med kostobjekter på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="27978-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="27978-107">Overfør dimensjonsverdier i finans til diagrammet med kostobjekter.</span><span class="sxs-lookup"><span data-stu-id="27978-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="27978-108">Du kan foreta alle nødvendige justeringer etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="27978-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="27978-109">Opprett et nytt kostobjektdiagram som er uavhengig av finans, eller legg til et nytt kostobjekt i et eksisterende kostobjektdiagram.</span><span class="sxs-lookup"><span data-stu-id="27978-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="27978-110">Du må opprette hvert enkelt kostobjekt individuelt.</span><span class="sxs-lookup"><span data-stu-id="27978-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="27978-111">Slik overfører du dimensjonsverdier fra finans til diagrammet med kostobjekter:</span><span class="sxs-lookup"><span data-stu-id="27978-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="27978-112">Angi en dimensjon som kostobjektdimensjon på siden **Oppdatere KR-dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="27978-112">Set a dimension to be the cost object dimension on the **Update CA Dimensions** page.</span></span> <span data-ttu-id="27978-113">Det er bare verdier fra denne dimensjonen som overføres.</span><span class="sxs-lookup"><span data-stu-id="27978-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="27978-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kostobjekter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="27978-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="27978-115">Velg **Hent kostobjekter fra dimensjon** for å overføre dimensjonsverdier til kostobjektdiagrammet.</span><span class="sxs-lookup"><span data-stu-id="27978-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="27978-116">Funksjonen overfører dimensjonsverdiene som du definerte i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="27978-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="27978-117">Du kan konfigurere feltet **Juster kostobjektdimensjon** slik at det definerer en enveissynkronisering av dimensjonsverdier fra finans til diagrammet med kostobjekter.</span><span class="sxs-lookup"><span data-stu-id="27978-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="27978-118">Du kan ikke definere en synkronisering av diagrammet med kostobjekter til dimensjonsverdier fra finans.</span><span class="sxs-lookup"><span data-stu-id="27978-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="27978-119">Diagrammet med kostobjektene inneholder nå alle angitte dimensjonsverdier fra finans og inkluderer titler og delsummer.</span><span class="sxs-lookup"><span data-stu-id="27978-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a><span data-ttu-id="27978-120">Slik oppretter du nye kostobjekter på siden Diagram med kostobjekter:</span><span class="sxs-lookup"><span data-stu-id="27978-120">To create new cost objects in the Chart of Cost Objects page</span></span>  
<span data-ttu-id="27978-121">Du kan definere og vedlikeholde kostobjekter i kortet **Kostobjektkort** eller siden **Diagram med kostobjekter**.</span><span class="sxs-lookup"><span data-stu-id="27978-121">You can set up and maintain cost objects in either the **Cost Object Card** card or on the **Chart of Cost Objects** page.</span></span> <span data-ttu-id="27978-122">I denne fremgangsmåten definerer objekter på siden **Diagram med kostobjekter**.</span><span class="sxs-lookup"><span data-stu-id="27978-122">In this procedure, you set up cost objects on the **Chart of Cost Objects** page.</span></span>  

1.  <span data-ttu-id="27978-123">Åpne siden **Diagram med kostobjekter** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="27978-123">Open the **Chart of Cost Objects** page in edit mode.</span></span>  
2.  <span data-ttu-id="27978-124">Angi kostobjektkoden i **Kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27978-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="27978-125">Alle kostobjekter må ha en kode.</span><span class="sxs-lookup"><span data-stu-id="27978-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="27978-126">Skriv inn kostobjektnavnet i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="27978-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="27978-127">Velg rullegardinpilen i feltet **Linjetype** for å angi formålet med kostobjektet.</span><span class="sxs-lookup"><span data-stu-id="27978-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="27978-128">Når det gjelder kostobjekter av linjetypen **Sum**, må du fylle ut feltet **Total fra/til**.</span><span class="sxs-lookup"><span data-stu-id="27978-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="27978-129">Bruk **eller**-operatoren, som er en loddrett linje (**&#124;**), til å angi områder for kostobjekter.</span><span class="sxs-lookup"><span data-stu-id="27978-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="27978-130">Når det gjelder kostobjekter av linjetypen **Til-sum**, fylles dette feltet ut automatisk når du bruker innrykksfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="27978-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="27978-131">Fyll ut feltet **Sorteringsrekkefølge**.</span><span class="sxs-lookup"><span data-stu-id="27978-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="27978-132">Velg den neste tomme linjen for å opprette et nytt kostobjekt, og gjenta deretter trinn 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="27978-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="27978-133">Når du har definert alle kostsentrene, velger du **Rykk inn kostobjekter**.</span><span class="sxs-lookup"><span data-stu-id="27978-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="27978-134">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="27978-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="27978-135">Hvis du har angitt definisjoner i feltene **Total fra/til** for **Til-sum**-kostobjekter før du kjører innrykksfunksjonen, må du angi dem på nytt.</span><span class="sxs-lookup"><span data-stu-id="27978-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="27978-136">Funksjonen overskriver verdiene i alle **Til-sum**-felt.</span><span class="sxs-lookup"><span data-stu-id="27978-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27978-137">Se også</span><span class="sxs-lookup"><span data-stu-id="27978-137">See Also</span></span>  
[<span data-ttu-id="27978-138">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="27978-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="27978-139">[Definere kostsentre og kostobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="27978-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="27978-140">[Balanser mellom kosttype, kostsenter og kostobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="27978-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="27978-141">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="27978-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="27978-142">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="27978-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="27978-143">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="27978-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="27978-144">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="27978-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
