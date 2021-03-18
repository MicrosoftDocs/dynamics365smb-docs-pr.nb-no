---
title: Definere spor for revisjonsspor | Microsoft Docs
description: Finn ut mer om oppgavene for å konfigurere kildespor og årsaksspor som du kan bruke til å spore revisjonsspor.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dab74a6a8debd20de781890c3b391457c6034e3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386902"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="55890-103">Definere kildespor og årsaksspor for revisjonsspor</span><span class="sxs-lookup"><span data-stu-id="55890-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="55890-104">Alle bokførte poster tilordnes automatisk til et kildespor, slik at transaksjoner kan spores til utgangspunktet.</span><span class="sxs-lookup"><span data-stu-id="55890-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="55890-105">Hvis du vil gi poster et ekstra kildespor, kan du bruke årsaksspor.</span><span class="sxs-lookup"><span data-stu-id="55890-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="55890-106">Årsaksspor brukes til å vise hvorfor en post ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="55890-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="55890-107">Når du definerer årsaksspor, kan du tilordne dem til hele kladdemaler og kladder, og du kan også tilordne dem til individuelle kladdelinjer og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="55890-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="55890-108">For både kildespor og årsaksspor bruker du spor som er lette å huske, og som er beskrivende.</span><span class="sxs-lookup"><span data-stu-id="55890-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="55890-109">Sporet må være unikt, og du kan definere så mange spor du vil.</span><span class="sxs-lookup"><span data-stu-id="55890-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="55890-110">Definere kildespor</span><span class="sxs-lookup"><span data-stu-id="55890-110">Define source codes</span></span>

<span data-ttu-id="55890-111">Noen ganger kan du ha behov for å se hvordan en spesiell post oppstod, for eksempel om den kom fra bokføring av en finanskladd eller en kjøpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="55890-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="55890-112">Et kildespor angir hvor en post ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="55890-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="55890-113">Postene opprettes når kladder og fakturaer bokføres og når visse kjørsler startes.</span><span class="sxs-lookup"><span data-stu-id="55890-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="55890-114">Hver bokføringstype har et bestemt kildespor som tilordnes når posten opprettes.</span><span class="sxs-lookup"><span data-stu-id="55890-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="55890-115">Bokføring av kladder, bestillinger, faktura eller kreditnota, og kjøring av ulike kjørsler oppretter poster i regnskapet.</span><span class="sxs-lookup"><span data-stu-id="55890-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="55890-116">Siden **Kildespordefinisjon** inneholder én hurtigfane for hver modul.</span><span class="sxs-lookup"><span data-stu-id="55890-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="55890-117">Hver hurtigfane inneholder kildesporene som kan brukes i den aktuelle modulen.</span><span class="sxs-lookup"><span data-stu-id="55890-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="55890-118">Når du bokfører eller starter en kjørsel, knyttes det riktige kildesporet til posten automatisk.</span><span class="sxs-lookup"><span data-stu-id="55890-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="55890-119">Når du for eksempel bokfører fra en finanskladd, kodes posten som *FINKLD*.</span><span class="sxs-lookup"><span data-stu-id="55890-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="55890-120">Du kan deretter filtrere **Finansposter**-siden for å vise hvilke poster som er bokført fra finanskladder eller salgsdokumenter, for eksempel</span><span class="sxs-lookup"><span data-stu-id="55890-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="55890-121">Slik definerer du kildespor</span><span class="sxs-lookup"><span data-stu-id="55890-121">To define source codes</span></span>

1. <span data-ttu-id="55890-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kildespordefinisjon**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="55890-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="55890-123">I vinduet **Kildespordefinisjon** angir du det aktuelle kildesporet for hver enkelt bokføringstype og kjørsel.</span><span class="sxs-lookup"><span data-stu-id="55890-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="55890-124">Du kan endre innholdet i et felt senere, og denne endringen vil deretter påvirke fremtidige bokføringer.</span><span class="sxs-lookup"><span data-stu-id="55890-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="55890-125">Endre kildespor</span><span class="sxs-lookup"><span data-stu-id="55890-125">Change source codes</span></span>

<span data-ttu-id="55890-126">Noen ganger kan det være nødvendig å endre et kildespor.</span><span class="sxs-lookup"><span data-stu-id="55890-126">You may want to change a source code.</span></span> <span data-ttu-id="55890-127">Du vil for eksempel endre kildesporet *FINKLD* til *FNK*.</span><span class="sxs-lookup"><span data-stu-id="55890-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="55890-128">Slik endrer du kildespor</span><span class="sxs-lookup"><span data-stu-id="55890-128">To change source codes</span></span>

1. <span data-ttu-id="55890-129">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kildespor**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="55890-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="55890-130">På linjen med kildesporet som skal endres, velger du et spor i feltet **Spor**.</span><span class="sxs-lookup"><span data-stu-id="55890-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="55890-131">Angi den nye koden, og velg deretter **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="55890-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="55890-132">Du kan også endre innholdet i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="55890-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="55890-133">Alle nye poster som bokføres fra finanskladden får det nye kildesporet.</span><span class="sxs-lookup"><span data-stu-id="55890-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="55890-134">Definere årsaksspor</span><span class="sxs-lookup"><span data-stu-id="55890-134">Define reason codes</span></span>

<span data-ttu-id="55890-135">Årsaksspor er et tillegg til kildesporene og brukes til å vise hvorfor en post ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="55890-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="55890-136">Du kan tildele årsaksspor på enkeltposter, og du kan overføre dem til poster og tilordne permanente koder til bestemte kladdemaler og kladder.</span><span class="sxs-lookup"><span data-stu-id="55890-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="55890-137">Når et årsaksspor er tilknyttet en kladdelinje eller et salgs- og bestillingshode, merkes alle poster med årsakssporet når de bokføres.</span><span class="sxs-lookup"><span data-stu-id="55890-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="55890-138">Slik setter du opp årsaksspor</span><span class="sxs-lookup"><span data-stu-id="55890-138">To set up reason codes</span></span>

1. <span data-ttu-id="55890-139">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Årsaksspor**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="55890-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="55890-140">Angi den første koden i **Spor**-feltet i **Årsaksspor**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="55890-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="55890-141">I feltet **Beskrivelse** skriver du inn en forklarende tekst.</span><span class="sxs-lookup"><span data-stu-id="55890-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="55890-142">Gjenta dette for hvert årsaksspor du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="55890-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="55890-143">Du kan opprette så mange årsaksspor du vil.</span><span class="sxs-lookup"><span data-stu-id="55890-143">You can set up any number of codes.</span></span>

<span data-ttu-id="55890-144">Følgende fremgangsmåte viser hvordan du legger til et årsaksspor i en kladdemal, men med lignende trinn gjelder det å legge til et årsaksspor i en kladdelinje eller varekladd.</span><span class="sxs-lookup"><span data-stu-id="55890-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="55890-145">Slik tilordner du årsaksspor til kladdemaler</span><span class="sxs-lookup"><span data-stu-id="55890-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="55890-146">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladdemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="55890-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="55890-147">På linjen med den valgte kladdemalen setter du inn ønsket spor i **Årsaksspor**-feltet.</span><span class="sxs-lookup"><span data-stu-id="55890-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="55890-148">Lukk kladdemalen.</span><span class="sxs-lookup"><span data-stu-id="55890-148">Close the journal template.</span></span>

<span data-ttu-id="55890-149">Årsakssporet som er valgt overføres til nye kladder som opprettes med denne kladdemalen.</span><span class="sxs-lookup"><span data-stu-id="55890-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="55890-150">Årsaksspor tilordnes kladdemaler i de andre modulene på samme måte.</span><span class="sxs-lookup"><span data-stu-id="55890-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="55890-151">Slik bruker du årsaksspor i salgs- og kjøpsdokumenter</span><span class="sxs-lookup"><span data-stu-id="55890-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="55890-152">Åpne det relevante salgs- eller kjøpsdokumentet.</span><span class="sxs-lookup"><span data-stu-id="55890-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="55890-153">Angi sporet i **Årsaksspor**-feltet i salgs- eller bestillingshodet.</span><span class="sxs-lookup"><span data-stu-id="55890-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="55890-154">Når fakturaen er bokført, overføres årsakssporet til hver finans-, kunde- og leverandørpost.</span><span class="sxs-lookup"><span data-stu-id="55890-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="55890-155">Du kan ikke tilordne forskjellige årsaksspor til hver enkelt kjøps- og salgslinje, fordi alle linjene bokføres som én post.</span><span class="sxs-lookup"><span data-stu-id="55890-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="55890-156">Se relatert opplæring på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="55890-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="55890-157">Se også</span><span class="sxs-lookup"><span data-stu-id="55890-157">See Also</span></span>

[<span data-ttu-id="55890-158">Finans</span><span class="sxs-lookup"><span data-stu-id="55890-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="55890-159">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="55890-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="55890-160">Arbeide med dimensjoner</span><span class="sxs-lookup"><span data-stu-id="55890-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="55890-161">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="55890-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="55890-162">Analysere kontantstrømmen i firmaet</span><span class="sxs-lookup"><span data-stu-id="55890-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="55890-163">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55890-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]