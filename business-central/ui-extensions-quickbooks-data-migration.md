---
title: Utvidelsen QuickBooks-migrering | Microsoft Docs
description: Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 34acbbf383048c6ef411797dfb1afcb51f7f6b40
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912274"
---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="eb62e-103">Utvidelsen QuickBooks Datamigrering</span><span class="sxs-lookup"><span data-stu-id="eb62e-103">The QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="eb62e-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eb62e-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="eb62e-105">Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eb62e-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="eb62e-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).</span><span class="sxs-lookup"><span data-stu-id="eb62e-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="data-from-quickbooks-desktop"></a><span data-ttu-id="eb62e-107">Data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="eb62e-107">Data from QuickBooks Desktop</span></span>

<span data-ttu-id="eb62e-108">Du kan importere følgende data fra QuickBooks Online til Business Central:</span><span class="sxs-lookup"><span data-stu-id="eb62e-108">You can import the following data from QuickBooks Online to Business Central:</span></span>

- <span data-ttu-id="eb62e-109">Kunder</span><span class="sxs-lookup"><span data-stu-id="eb62e-109">Customers</span></span>  
- <span data-ttu-id="eb62e-110">Leverandører</span><span class="sxs-lookup"><span data-stu-id="eb62e-110">Vendors</span></span>  
- <span data-ttu-id="eb62e-111">Varer</span><span class="sxs-lookup"><span data-stu-id="eb62e-111">Items</span></span>  
- <span data-ttu-id="eb62e-112">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="eb62e-112">Chart of Accounts</span></span>  
- <span data-ttu-id="eb62e-113">Starte saldotransaksjoner i Finans</span><span class="sxs-lookup"><span data-stu-id="eb62e-113">Beginning Balance transactions in General Ledger</span></span>  
- <span data-ttu-id="eb62e-114">Beholdningsantall for lagervarer</span><span class="sxs-lookup"><span data-stu-id="eb62e-114">On-hand Quantities for Inventory Items</span></span>  
- <span data-ttu-id="eb62e-115">Åpne dokumenter for kunder og leverandører, for eksempel fakturaer, kreditnotaer og betalinger</span><span class="sxs-lookup"><span data-stu-id="eb62e-115">Open documents for customers and vendors, such as invoices, credit memos and payments</span></span>  

<span data-ttu-id="eb62e-116">Vi overfører bare hele beløp på salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="eb62e-116">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="eb62e-117">Vi oppdaterer ikke delvis betalte beløp.</span><span class="sxs-lookup"><span data-stu-id="eb62e-117">We do not update partially paid amounts.</span></span> <span data-ttu-id="eb62e-118">Hvis en kunde for eksempel har betalt 300 av totalt 500 kroner på en salgsfaktura, overfører vi hele beløpet på 500.</span><span class="sxs-lookup"><span data-stu-id="eb62e-118">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="eb62e-119">Hvis du har mottatt delbetalinger, må du oppdatere disse manuelt før eller etter at du har overført data.</span><span class="sxs-lookup"><span data-stu-id="eb62e-119">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="eb62e-120">Vi anbefaler at du utligner utestående transaksjoner før du overfører, bare for å gjøre ting enklere senere.</span><span class="sxs-lookup"><span data-stu-id="eb62e-120">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]
> <span data-ttu-id="eb62e-121">Vi overfører ikke bestillinger eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="eb62e-121">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="eb62e-122">Før du begynner</span><span class="sxs-lookup"><span data-stu-id="eb62e-122">Before You Start</span></span>

<span data-ttu-id="eb62e-123">En viktig del av overføringen er å angi kontiene som transaksjonene skal overføres til.</span><span class="sxs-lookup"><span data-stu-id="eb62e-123">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="eb62e-124">Det er lurt å planlegge denne tilordningen før du overfører data.</span><span class="sxs-lookup"><span data-stu-id="eb62e-124">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="eb62e-125">Kontiene der du for eksempel bokfører transaksjoner for følgende:</span><span class="sxs-lookup"><span data-stu-id="eb62e-125">For example, the accounts where you post transactions for:</span></span>

- <span data-ttu-id="eb62e-126">Salg av varer eller tjenestene til kunder</span><span class="sxs-lookup"><span data-stu-id="eb62e-126">The sale of items or services to customers</span></span>  
- <span data-ttu-id="eb62e-127">Kjøp av varer eller tjenester fra leverandører</span><span class="sxs-lookup"><span data-stu-id="eb62e-127">The purchase of items or services from vendors</span></span>  
- <span data-ttu-id="eb62e-128">Justeringer i Finans</span><span class="sxs-lookup"><span data-stu-id="eb62e-128">Adjustments in the general ledger</span></span>  

<span data-ttu-id="eb62e-129">Business Central krever at det er tilordnet kontonumre til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="eb62e-129">Business Central requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="eb62e-130">Kontroller at kontonumre er tilordnet til kontiene i QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="eb62e-130">Make sure that account numbers are assigned to your accounts in QuickBooks.</span></span>
<span data-ttu-id="eb62e-131">Hvis transaksjoner i QuickBooks har mva-beløp, må du definere en mva-konto for mva-jurisdiksjonene i Business Central før du kan bokføre transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="eb62e-131">If transactions in QuickBooks have tax amounts, you must set up a tax account for your tax jurisdictions in Business Central before you can post transactions.</span></span>

<span data-ttu-id="eb62e-132">Du må laste ned Microsofts verktøy for dataeksport for å få dataene dine ut av QuickBooks Desktop-programmet.</span><span class="sxs-lookup"><span data-stu-id="eb62e-132">In order to get your data out of the QuickBooks desktop application you will need to download the Microsoft Data Exporter Tool.</span></span>  <span data-ttu-id="eb62e-133">Instruksjonene for verktøyet finnes i veiviseren for datamigrering i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eb62e-133">The instructions for the tool are in the Data Migration Wizard in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="eb62e-134">Verktøyet vil koble til QuickBooks-programmet ditt og eksportere de aktuelle dataene til en ZIP-fil.</span><span class="sxs-lookup"><span data-stu-id="eb62e-134">The tool will connect to your QuickBooks application and export the applicable data to a .zip file.</span></span>  

> [!NOTE]
> <span data-ttu-id="eb62e-135">For tiden fungerer bare dataeksportverktøyet med QuickBooks 2017 og 2018.</span><span class="sxs-lookup"><span data-stu-id="eb62e-135">Currently the data exporter tool only works with QuickBooks 2017 and 2018.</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="eb62e-136">Finne QuickBooks-utvidelse for dataoverføring</span><span class="sxs-lookup"><span data-stu-id="eb62e-136">Finding the QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="eb62e-137">Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering.</span><span class="sxs-lookup"><span data-stu-id="eb62e-137">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="eb62e-138">Hvis du er klar til å starte nå og har eksportert dataene dine fra QuickBooks, kan du velge ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Assistert oppsett**, og deretter velge den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="eb62e-138">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="eb62e-139">Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="eb62e-139">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="eb62e-140">Hva gjør jeg etter at jeg har overført dataene?</span><span class="sxs-lookup"><span data-stu-id="eb62e-140">What do I do after I migrate Data?</span></span>

<span data-ttu-id="eb62e-141">Etter at du har overført dataene, har transaksjoner statusen Ikke bokført, slik at du kan se gjennom dem og foreta justeringer.</span><span class="sxs-lookup"><span data-stu-id="eb62e-141">After you migrate data, transactions have the status Unposted, so you can review them and make adjustments.</span></span> <span data-ttu-id="eb62e-142">Hvis du vil se gjennom transaksjonene, går du til siden der de vanligvis er.</span><span class="sxs-lookup"><span data-stu-id="eb62e-142">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="eb62e-143">Hvis du for eksempel vil se gjennom ikke-bokførte salgsfakturaer, går du til siden Salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="eb62e-143">For example, to review unposted sales invoices, go to the Sales Invoices page.</span></span> <span data-ttu-id="eb62e-144">Hvis du vil se gjennom utbetalingskladder, går du til siden Utbetalingskladder.</span><span class="sxs-lookup"><span data-stu-id="eb62e-144">To review payment journals, go to the Payment Journals page.</span></span>
<span data-ttu-id="eb62e-145">Det finnes et par spesifikke ting du bør gjøre: Hvis transaksjonene i QuickBooks inneholder påslagsbeløp eller rabattbeløp, må du manuelt legge beløpene til de relaterte transaksjonene i Business Central før du bokfører dem.</span><span class="sxs-lookup"><span data-stu-id="eb62e-145">There are a few things in particular that you should do: If the transactions in QuickBooks had markup or discount amounts, you must manually add the amounts to the related transactions in Business Central before you post them.</span></span>
<span data-ttu-id="eb62e-146">Hvis du bruker merverdiavgift (mva), må du kanskje legge til en bokføringsgruppe for firma og en varebokføringsgruppe i bokføringsoppsettet, slik at du kan bokføre mva-beløp.</span><span class="sxs-lookup"><span data-stu-id="eb62e-146">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
<span data-ttu-id="eb62e-147">Kontroller startsaldoene for konti i Finans.</span><span class="sxs-lookup"><span data-stu-id="eb62e-147">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="eb62e-148">QuickBooks lagrer ikke gjeldende saldo for alle konti, så du må kanskje rette startsaldoer.</span><span class="sxs-lookup"><span data-stu-id="eb62e-148">QuickBooks does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb62e-149">Se også</span><span class="sxs-lookup"><span data-stu-id="eb62e-149">See Also</span></span>

[<span data-ttu-id="eb62e-150">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="eb62e-150">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="eb62e-151">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="eb62e-151">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
