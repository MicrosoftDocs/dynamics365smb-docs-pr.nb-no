---
title: Sette opp et diagram med kosttyper | Microsoft-dokumentasjon
description: Diagrammet med kosttyper ligner på kontoplanen i finans.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: d9a2c6efcee13564edbe9b108c831a1e9fbb7d93
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301988"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="b45ed-103">Definere kosttyper</span><span class="sxs-lookup"><span data-stu-id="b45ed-103">Set Up Cost Types</span></span>
<span data-ttu-id="b45ed-104">Diagrammet med kosttyper ligner på kontoplanen i finans.</span><span class="sxs-lookup"><span data-stu-id="b45ed-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="b45ed-105">Du kan definere diagrammet med kosttyper på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="b45ed-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="b45ed-106">Strukturen i oversikten over kosttyper ligner på resultatregnskapskontiene i finanskontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="b45ed-107">Du kan deretter overføre finanskontoplanen til diagrammet med kosttyper.</span><span class="sxs-lookup"><span data-stu-id="b45ed-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="b45ed-108">Du kan foreta alle nødvendige justeringer etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="b45ed-109">Opprett et nytt kosttypediagram, eller legg til nye kosttyper i det eksisterende kosttypediagrammet.</span><span class="sxs-lookup"><span data-stu-id="b45ed-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="b45ed-110">Du må opprette hver enkelt nye kosttype individuelt.</span><span class="sxs-lookup"><span data-stu-id="b45ed-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="b45ed-111">Slik overfører du finanskontoplanen til diagrammet med kosttyper:</span><span class="sxs-lookup"><span data-stu-id="b45ed-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="b45ed-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b45ed-113">Velg handlingen **Hent kosttyper fra kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="b45ed-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="b45ed-114">Klikk **Ja**-knappen i dialogboksen for å bekrefte overføringen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="b45ed-115">Funksjonen bruker kontoplanen til å opprette et diagram med kosttyper.</span><span class="sxs-lookup"><span data-stu-id="b45ed-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="b45ed-116">Diagrammet over kostnadstypene inneholder nå alle resultatkontiene i finans og inkluderer overskrifter og delsummer.</span><span class="sxs-lookup"><span data-stu-id="b45ed-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="b45ed-117">Du kan endre diagrammet med kosttyper etter behov.</span><span class="sxs-lookup"><span data-stu-id="b45ed-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="b45ed-118">Du kan for eksempel slette eksisterende kosttypeduplikater.</span><span class="sxs-lookup"><span data-stu-id="b45ed-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="b45ed-119">Funksjonen **Registrer kosttyper i kontoplan** oppdaterer forholdet mellom kontoplanen og oversikten over kosttyper.</span><span class="sxs-lookup"><span data-stu-id="b45ed-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="b45ed-120">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="b45ed-120">The **No.**</span></span> <span data-ttu-id="b45ed-121">-feltet er fylt ut og bekreftet for å forsikre at hver finanskonto er relatert til bare én kostnadstype.</span><span class="sxs-lookup"><span data-stu-id="b45ed-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="b45ed-122">Funksjonen kjøres automatisk før overføring av finansposter til kostregnskap.</span><span class="sxs-lookup"><span data-stu-id="b45ed-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="b45ed-123">Slik definerer du nye kosttyper på siden Diagram med kosttyper:</span><span class="sxs-lookup"><span data-stu-id="b45ed-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="b45ed-124">Åpne siden **Diagram med kosttyper** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="b45ed-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="b45ed-125">Fyll ut feltene som beskrevet etter behov.</span><span class="sxs-lookup"><span data-stu-id="b45ed-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="b45ed-126">Du kan definere og vedlikeholde kostnadstyper på siden **Kosttypekort** eller **Diagram med kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="b45ed-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="b45ed-127">I denne fremgangsmåten definerer du nye kosttyper på siden **Diagram med kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="b45ed-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="b45ed-128">Når du har opprettet alle kosttyper, velger du **Rykk inn kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="b45ed-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="b45ed-129">Klikk **Ja**-knappen i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="b45ed-130">Koble nye kosttypen til den tilsvarende kontoen i finans.</span><span class="sxs-lookup"><span data-stu-id="b45ed-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="b45ed-131">Hvis du har angitt definisjoner i feltene **Sammentelling** for linjetypen **Til-sum** før du kjører funksjonen **Rykk inn kosttyper**, må du angi definisjonene på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-felt.</span><span class="sxs-lookup"><span data-stu-id="b45ed-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="b45ed-132">Slik oppdaterer du kosttyper:</span><span class="sxs-lookup"><span data-stu-id="b45ed-132">To update cost types</span></span>  
1.  <span data-ttu-id="b45ed-133">Velg på siden **Kostregnskapsoppsett** hvis du vil at diagrammet med kosttypene skal oppdateres automatisk når kontoplanen endres.</span><span class="sxs-lookup"><span data-stu-id="b45ed-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="b45ed-134">I feltet **Juster finanskonto** kan du velge blant følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="b45ed-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="b45ed-135">**Ingen justering** – Det gjøres ingen tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="b45ed-136">**Automatisk** – en tilsvarende endring blir utført i diagrammet for kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="b45ed-137">**Spør** - Det vises en melding med spørsmål om du vil gjøre tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="b45ed-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b45ed-138">Se også</span><span class="sxs-lookup"><span data-stu-id="b45ed-138">See Also</span></span>  
[<span data-ttu-id="b45ed-139">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="b45ed-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="b45ed-140">[Definere kostsentre og kostobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="b45ed-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="b45ed-141">[Balanser mellom kosttype, kostsenter og kostobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="b45ed-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="b45ed-142">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="b45ed-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="b45ed-143">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="b45ed-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="b45ed-144">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="b45ed-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="b45ed-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b45ed-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
