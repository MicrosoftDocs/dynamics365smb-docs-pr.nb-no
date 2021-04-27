---
title: Informasjon om Finans og kontoplan | Microsoft dokumenter
description: Beskriver Finans, kontoplanen og kontokategoriene.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f242bce26f55fe446ac8dc96335a8da835dd259c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774008"
---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="52d45-103">Forstå Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="52d45-103">Understanding the General Ledger and the COA</span></span>

<span data-ttu-id="52d45-104">Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som alle finansposter bokføres til.</span><span class="sxs-lookup"><span data-stu-id="52d45-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="52d45-105">inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.</span><span class="sxs-lookup"><span data-stu-id="52d45-105">includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="52d45-106">Finansoppsett og generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="52d45-106">General Ledger Setup and General Posting Setup</span></span>

<span data-ttu-id="52d45-107">Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data.</span><span class="sxs-lookup"><span data-stu-id="52d45-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="52d45-108">På siden **Finansoppsett** angir du hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:</span><span class="sxs-lookup"><span data-stu-id="52d45-108">On the **General Ledger Setup** page, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="52d45-109">Detaljopplysninger om fakturaavrunding</span><span class="sxs-lookup"><span data-stu-id="52d45-109">Invoice rounding details</span></span>  
* <span data-ttu-id="52d45-110">Adresseformater</span><span class="sxs-lookup"><span data-stu-id="52d45-110">Address formats</span></span>  
* <span data-ttu-id="52d45-111">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="52d45-111">Financial reporting</span></span>  

<span data-ttu-id="52d45-112">På siden **Generelt bokføringsoppsett** angir du hvordan du vil definere kombinasjoner av firma- og varebokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="52d45-112">Similarly, on the **General Posting Setup** page, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="52d45-113">Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="52d45-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="52d45-114">Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="52d45-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="52d45-115">Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="52d45-115">For more information, see [Posting Group Setups](finance-posting-groups.md).</span></span>  

> [!TIP]
> <span data-ttu-id="52d45-116">Siden **Finansoppsett** inneholder generelle felt og felt som er spesifikke for ditt land eller din region.</span><span class="sxs-lookup"><span data-stu-id="52d45-116">The **General Ledger Setup** page includes generic fields and fields that are particular to your country or region.</span></span> <span data-ttu-id="52d45-117">Hvis du ikke er sikker på betydningen av et felt, foreslår vi at du arbeider med regnskapsføreren for å finne ut om det er av relevans for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="52d45-117">If you are not sure of the meaning of a field, we suggest you work with your accountant to determine whether it is of relevance to your organization.</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="52d45-118">Kontoplanen</span><span class="sxs-lookup"><span data-stu-id="52d45-118">The Chart of Accounts</span></span>

<span data-ttu-id="52d45-119">Kontoplanen viser alle finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="52d45-119">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="52d45-120">Fra kontoplanen kan du gjøre ting som:</span><span class="sxs-lookup"><span data-stu-id="52d45-120">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="52d45-121">Vise rapporter som viser finansposter og saldoer.</span><span class="sxs-lookup"><span data-stu-id="52d45-121">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="52d45-122">Lukke resultatregnskapet.</span><span class="sxs-lookup"><span data-stu-id="52d45-122">Close your income statement.</span></span>  
* <span data-ttu-id="52d45-123">Åpne Finanskonto-kortet for å legge til eller endre innstillinger.</span><span class="sxs-lookup"><span data-stu-id="52d45-123">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="52d45-124">Vise en liste over bokføringsgrupper som du posterer til kontoen.</span><span class="sxs-lookup"><span data-stu-id="52d45-124">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="52d45-125">Vise separate debet- og kreditsaldoer for én konto</span><span class="sxs-lookup"><span data-stu-id="52d45-125">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="52d45-126">Du kan legge til, endre eller slette finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="52d45-126">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="52d45-127">For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="52d45-127">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="52d45-128">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="52d45-128">Account Categories</span></span>

<span data-ttu-id="52d45-129">Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.</span><span class="sxs-lookup"><span data-stu-id="52d45-129">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="52d45-130">Siden **Finanskontokategorier** viser dine kategorier og underkategorier og finanskonti som er tilordnet til dem.</span><span class="sxs-lookup"><span data-stu-id="52d45-130">The **G/L Account Categories** page shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="52d45-131">Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.</span><span class="sxs-lookup"><span data-stu-id="52d45-131">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="52d45-132">Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje på siden **Finanskontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="52d45-132">You create a category group by indenting other subcategories under a line on the **G/L Account Categories** page.</span></span> <span data-ttu-id="52d45-133">Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen.</span><span class="sxs-lookup"><span data-stu-id="52d45-133">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="52d45-134">Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.</span><span class="sxs-lookup"><span data-stu-id="52d45-134">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="52d45-135">Du kan angi om kontoene i hver underkategori må inkluderes i bestemte typer rapporter.</span><span class="sxs-lookup"><span data-stu-id="52d45-135">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="52d45-136">Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.</span><span class="sxs-lookup"><span data-stu-id="52d45-136">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="52d45-137">Standard saldoutdrag har for eksempel en underkategori for kontanter under gjeldende aktiva.</span><span class="sxs-lookup"><span data-stu-id="52d45-137">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="52d45-138">Hvis du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, kan du:</span><span class="sxs-lookup"><span data-stu-id="52d45-138">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="52d45-139">Legge til to nye underkategorier.</span><span class="sxs-lookup"><span data-stu-id="52d45-139">Add two new subcategories.</span></span> <span data-ttu-id="52d45-140">Én for håndkassen og én for sjekkontoen.</span><span class="sxs-lookup"><span data-stu-id="52d45-140">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="52d45-141">Angi den ekstra rapportdefinisjonen **Kontantkontoer** for disse underkategoriene.</span><span class="sxs-lookup"><span data-stu-id="52d45-141">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="52d45-142">Rykk inn dem under **Kontanter**-underkategori.</span><span class="sxs-lookup"><span data-stu-id="52d45-142">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="52d45-143">Neste gang du genererer kontoskjemaer, vil utdraget vise en total saldo for kontanter og to linjer med saldoer for håndkasse og sjekkontoen.</span><span class="sxs-lookup"><span data-stu-id="52d45-143">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="52d45-144">Se også</span><span class="sxs-lookup"><span data-stu-id="52d45-144">See Also</span></span>

[<span data-ttu-id="52d45-145">Finans</span><span class="sxs-lookup"><span data-stu-id="52d45-145">Finance</span></span>](finance.md)  
[<span data-ttu-id="52d45-146">Definere eller endre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="52d45-146">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="52d45-147">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="52d45-147">Business Intelligence</span></span>](bi.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]