---
title: Informasjon om Finans og kontoplan | Microsoft dokumenter
description: Beskriver Finans, kontoplanen og kontokategoriene.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9147b69f5fdc658358a387cd5e9d2834ec509d50
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="44646-103">Forstå Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="44646-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="44646-104">Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som alle finansposter bokføres til.</span><span class="sxs-lookup"><span data-stu-id="44646-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="44646-105">inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.</span><span class="sxs-lookup"><span data-stu-id="44646-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="44646-106">Finansoppsett og generelt bokføringsoppsett</span><span class="sxs-lookup"><span data-stu-id="44646-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="44646-107">Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data.</span><span class="sxs-lookup"><span data-stu-id="44646-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="44646-108">I vinduet **Finansoppsett** angir du hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:</span><span class="sxs-lookup"><span data-stu-id="44646-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="44646-109">Detaljopplysninger om fakturaavrunding</span><span class="sxs-lookup"><span data-stu-id="44646-109">Invoice rounding details</span></span>  
* <span data-ttu-id="44646-110">Adresseformater</span><span class="sxs-lookup"><span data-stu-id="44646-110">Address formats</span></span>  
* <span data-ttu-id="44646-111">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="44646-111">Financial reporting</span></span>  

<span data-ttu-id="44646-112">I vinduet **Generelt bokføringsoppsett** angir du hvordan du vil definere kombinasjoner av firma- og varebokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="44646-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="44646-113">Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="44646-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="44646-114">Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="44646-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="44646-115">Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="44646-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="44646-116">Kontoplanen</span><span class="sxs-lookup"><span data-stu-id="44646-116">The Chart of Accounts</span></span>
<span data-ttu-id="44646-117">Kontoplanen viser alle finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="44646-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="44646-118">Fra kontoplanen kan du gjøre ting som:</span><span class="sxs-lookup"><span data-stu-id="44646-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="44646-119">Vise rapporter som viser finansposter og saldoer.</span><span class="sxs-lookup"><span data-stu-id="44646-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="44646-120">Lukke resultatregnskapet.</span><span class="sxs-lookup"><span data-stu-id="44646-120">Close your income statement.</span></span>  
* <span data-ttu-id="44646-121">Åpne Finanskonto-kortet for å legge til eller endre innstillinger.</span><span class="sxs-lookup"><span data-stu-id="44646-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="44646-122">Vise en liste over bokføringsgrupper som du posterer til kontoen.</span><span class="sxs-lookup"><span data-stu-id="44646-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="44646-123">Vise separate debet- og kreditsaldoer for én konto</span><span class="sxs-lookup"><span data-stu-id="44646-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="44646-124">Du kan legge til, endre eller slette finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="44646-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="44646-125">For å unngå avvik kan du imidlertid ikke slette en finanskonto hvis dataene fra den er brukt i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="44646-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="44646-126">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="44646-126">Account Categories</span></span>
<span data-ttu-id="44646-127">Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.</span><span class="sxs-lookup"><span data-stu-id="44646-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="44646-128">Vinduet **Finanskontokategorier** viser dine kategorier og underkategorier og finanskonti som er tilordnet til dem.</span><span class="sxs-lookup"><span data-stu-id="44646-128">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="44646-129">Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.</span><span class="sxs-lookup"><span data-stu-id="44646-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="44646-130">Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje i vinduet **Finanskontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="44646-130">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="44646-131">Dette gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen.</span><span class="sxs-lookup"><span data-stu-id="44646-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="44646-132">Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.</span><span class="sxs-lookup"><span data-stu-id="44646-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="44646-133">Du kan angi om kontoene i hver underkategori må inkluderes i bestemte typer rapporter.</span><span class="sxs-lookup"><span data-stu-id="44646-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="44646-134">Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.</span><span class="sxs-lookup"><span data-stu-id="44646-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="44646-135">Standard saldoutdrag har for eksempel en underkategori for kontanter under gjeldende aktiva.</span><span class="sxs-lookup"><span data-stu-id="44646-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="44646-136">Hvis du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, kan du:</span><span class="sxs-lookup"><span data-stu-id="44646-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="44646-137">Legge til to nye underkategorier.</span><span class="sxs-lookup"><span data-stu-id="44646-137">Add two new subcategories.</span></span> <span data-ttu-id="44646-138">Én for håndkassen og én for sjekkontoen.</span><span class="sxs-lookup"><span data-stu-id="44646-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="44646-139">Angi den ekstra rapportdefinisjonen **Kontantkontoer** for disse underkategoriene.</span><span class="sxs-lookup"><span data-stu-id="44646-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="44646-140">Rykk inn dem under **Kontanter**-underkategori.</span><span class="sxs-lookup"><span data-stu-id="44646-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="44646-141">Neste gang du genererer kontoskjemaer, vil utdraget vise en total saldo for kontanter og to linjer med saldoer for håndkasse og sjekkontoen.</span><span class="sxs-lookup"><span data-stu-id="44646-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44646-142">Se også</span><span class="sxs-lookup"><span data-stu-id="44646-142">See Also</span></span>
[<span data-ttu-id="44646-143">Finans</span><span class="sxs-lookup"><span data-stu-id="44646-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="44646-144">Definere eller endre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="44646-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="44646-145">Forretningsintelligens</span><span class="sxs-lookup"><span data-stu-id="44646-145">Business Intelligence</span></span>](bi.md)  

