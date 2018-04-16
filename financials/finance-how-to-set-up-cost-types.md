---
title: Sette opp et diagram med kosttyper | Microsoft-dokumentasjon
description: "Diagrammet med kosttyper ligner på kontoplanen i finans."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: c89170fd159428d771df105ca16a1d91d29651e4
ms.contentlocale: nb-no
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-cost-types"></a><span data-ttu-id="ff826-103">Definere kosttyper</span><span class="sxs-lookup"><span data-stu-id="ff826-103">Set Up Cost Types</span></span>
<span data-ttu-id="ff826-104">Diagrammet med kosttyper ligner på kontoplanen i finans.</span><span class="sxs-lookup"><span data-stu-id="ff826-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="ff826-105">Du kan definere diagrammet med kosttyper på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="ff826-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="ff826-106">Strukturen i oversikten over kosttyper ligner på resultatregnskapskontiene i finanskontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ff826-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="ff826-107">Du kan deretter overføre finanskontoplanen til diagrammet med kosttyper.</span><span class="sxs-lookup"><span data-stu-id="ff826-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="ff826-108">Du kan foreta alle nødvendige justeringer etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="ff826-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="ff826-109">Opprett et nytt kosttypediagram, eller legg til nye kosttyper i det eksisterende kosttypediagrammet.</span><span class="sxs-lookup"><span data-stu-id="ff826-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="ff826-110">Du må opprette hver enkelt nye kosttype individuelt.</span><span class="sxs-lookup"><span data-stu-id="ff826-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="ff826-111">Slik overfører du finanskontoplanen til diagrammet med kosttyper:</span><span class="sxs-lookup"><span data-stu-id="ff826-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="ff826-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ff826-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ff826-113">Velg handlingen **Hent kosttyper fra kontoplan**.</span><span class="sxs-lookup"><span data-stu-id="ff826-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="ff826-114">Klikk **Ja**-knappen i dialogboksen for å bekrefte overføringen.</span><span class="sxs-lookup"><span data-stu-id="ff826-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="ff826-115">Funksjonen bruker kontoplanen til å opprette et diagram med kosttyper.</span><span class="sxs-lookup"><span data-stu-id="ff826-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="ff826-116">Diagrammet over kostnadstypene inneholder nå alle resultatkontiene i finans og inkluderer overskrifter og delsummer.</span><span class="sxs-lookup"><span data-stu-id="ff826-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="ff826-117">Du kan endre diagrammet med kosttyper etter behov.</span><span class="sxs-lookup"><span data-stu-id="ff826-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="ff826-118">Du kan for eksempel slette eksisterende kosttypeduplikater.</span><span class="sxs-lookup"><span data-stu-id="ff826-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="ff826-119">Funksjonen **Registrer kosttyper i kontoplan** oppdaterer forholdet mellom kontoplanen og oversikten over kosttyper.</span><span class="sxs-lookup"><span data-stu-id="ff826-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="ff826-120">**Nr.**</span><span class="sxs-lookup"><span data-stu-id="ff826-120">The **No.**</span></span> <span data-ttu-id="ff826-121">-feltet er fylt ut og bekreftet for å forsikre at hver finanskonto er relatert til bare én kostnadstype.</span><span class="sxs-lookup"><span data-stu-id="ff826-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="ff826-122">Funksjonen kjøres automatisk før overføring av finansposter til kostregnskap.</span><span class="sxs-lookup"><span data-stu-id="ff826-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a><span data-ttu-id="ff826-123">Slik definerer du nye kosttyper i vinduet Diagram med kosttyper:</span><span class="sxs-lookup"><span data-stu-id="ff826-123">To set up new cost types in the Chart of Cost Types window</span></span>  
1. <span data-ttu-id="ff826-124">Åpne vinduet **Diagram med kosttyper** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="ff826-124">Open the **Chart of Cost Types** window in edit mode.</span></span>  
2. <span data-ttu-id="ff826-125">Fyll ut feltene som beskrevet etter behov.</span><span class="sxs-lookup"><span data-stu-id="ff826-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]  
   >  <span data-ttu-id="ff826-126">Du kan definere og vedlikeholde kostnadstyper i vinduet **Kosttypekort** eller **Diagram med kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="ff826-126">You can set up and maintain cost types in either the **Cost Type Card** window or in the **Chart of Cost Types** window.</span></span> <span data-ttu-id="ff826-127">I denne fremgangsmåten definerer du nye kosttyper i vinduet **Diagram med kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="ff826-127">In this procedure, you set up cost types in the **Chart of Cost Types** window.</span></span>

3. <span data-ttu-id="ff826-128">Når du har opprettet alle kosttyper, velger du **Rykk inn kosttyper**.</span><span class="sxs-lookup"><span data-stu-id="ff826-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="ff826-129">Klikk **Ja**-knappen i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ff826-129">In the dialog box, choose the **Yes** button.</span></span>  
4. <span data-ttu-id="ff826-130">Koble nye kosttypen til den tilsvarende kontoen i finans.</span><span class="sxs-lookup"><span data-stu-id="ff826-130">Link the new cost type to the corresponding general ledger account.</span></span>  

   > [!IMPORTANT]  
   >  <span data-ttu-id="ff826-131">Hvis du har angitt definisjoner i feltene **Sammentelling** for linjetypen **Til-sum** før du kjører funksjonen **Rykk inn kosttyper**, må du angi definisjonene på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-felt.</span><span class="sxs-lookup"><span data-stu-id="ff826-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="ff826-132">Slik oppdaterer du kosttyper:</span><span class="sxs-lookup"><span data-stu-id="ff826-132">To update cost types</span></span>  
1.  <span data-ttu-id="ff826-133">Velg i vinduet **Kostregnskapsoppsett** hvis du vil at diagrammet med kosttypene skal oppdateres automatisk når kontoplanen endres.</span><span class="sxs-lookup"><span data-stu-id="ff826-133">In the **Cost Accounting Setup** window, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="ff826-134">I feltet **Juster finanskonto** kan du velge blant følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="ff826-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="ff826-135">**Ingen justering** – Det gjøres ingen tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ff826-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="ff826-136">**Automatisk** – en tilsvarende endring blir utført i diagrammet for kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ff826-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="ff826-137">**Spør** - Det vises en melding med spørsmål om du vil gjøre tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="ff826-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff826-138">Se også</span><span class="sxs-lookup"><span data-stu-id="ff826-138">See Also</span></span>  
[<span data-ttu-id="ff826-139">Gjøre rede for kostnader</span><span class="sxs-lookup"><span data-stu-id="ff826-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="ff826-140">[Definere forholdet mellom kostnadstyper og finanskontoer](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ff826-140">[Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md) </span></span>  
<span data-ttu-id="ff826-141">[Definere kostsentre og kostobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ff826-141">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="ff826-142">[Balanser mellom kosttype, kostsenter og kostobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="ff826-142">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="ff826-143">[Definere kost.regnskap](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="ff826-143">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="ff826-144">[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="ff826-144">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="ff826-145">Om kostregnskap</span><span class="sxs-lookup"><span data-stu-id="ff826-145">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="ff826-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff826-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

