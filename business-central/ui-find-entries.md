---
title: Søke etter poster | Microsoft Docs
description: Denne artikkelen beskriver hvordan du finner dokumenter og poster som er relatert
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a29cea15cba15da1bc68816e07f76de59f43958b
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216131"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="6f5a7-103">Søke etter relaterte poster for bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="6f5a7-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="6f5a7-104">I denne artikkelen lærer du hvordan du finner dokumenter og poster som er knyttet til hverandre basert på en felles informasjon, for eksempel:</span><span class="sxs-lookup"><span data-stu-id="6f5a7-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="6f5a7-105">Bilagsnummer eller bokføringsdato</span><span class="sxs-lookup"><span data-stu-id="6f5a7-105">Document number or posting date</span></span>
- <span data-ttu-id="6f5a7-106">Forretningskontakttype, nummer eller eksternt dokumentnummer</span><span class="sxs-lookup"><span data-stu-id="6f5a7-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="6f5a7-107">Vareserienummer eller partinummer</span><span class="sxs-lookup"><span data-stu-id="6f5a7-107">Item serial number or lot number</span></span>

<span data-ttu-id="6f5a7-108">Denne funksjonen er svært nyttig for å finne postene som resulterer fra bestemte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="6f5a7-109">Når du søker ved hjelp av bilagsnummer, kan du skrive ut oversikten fra Bilagsposter-rapporten.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="6f5a7-110">Kom i gang</span><span class="sxs-lookup"><span data-stu-id="6f5a7-110">Get started</span></span>

<span data-ttu-id="6f5a7-111">Funksjonen for å finne poster er lett tilgjengelig på de fleste sider som viser bokførte dokumenter eller bokførte dokumentposter, for både lister og kort.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="6f5a7-112">Det første trinnet er derfor å åpne én av disse sidene.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="6f5a7-113">Velg deretter handlingen **Søk etter poster**, eller trykk på Alt+G.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="6f5a7-114">Siden **Søk etter poster** inkluderer alle relaterte dokumenter og poster basert på bilagsnr. og bokføringsdato.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="6f5a7-115">Siden er delt inn i tre deler:</span><span class="sxs-lookup"><span data-stu-id="6f5a7-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="6f5a7-116">Den øverste delen viser felt og handlinger som du bruker til å filtrere søket.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="6f5a7-117">Den midterste delen viser relaterte dokumenter basert på søket.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="6f5a7-118">Den nederste delen viser informasjon om kildedokumentet som ble funnet ved å søke.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="6f5a7-119">Søke etter poster</span><span class="sxs-lookup"><span data-stu-id="6f5a7-119">Search for entries</span></span>

<span data-ttu-id="6f5a7-120">Du kan søke etter oppføringer basert på informasjon om enten dokumentet, forretningskontakten eller varereferansen.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="6f5a7-121">Du kan endre søket ved å velge **Handlinger**, **Finn etter**, og deretter én av følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="6f5a7-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="6f5a7-122">Handling</span><span class="sxs-lookup"><span data-stu-id="6f5a7-122">Action</span></span>|<span data-ttu-id="6f5a7-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6f5a7-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="6f5a7-124">Finn etter dokument</span><span class="sxs-lookup"><span data-stu-id="6f5a7-124">Find by Document</span></span>|<span data-ttu-id="6f5a7-125">Vis poster basert på et bestemt bilagsnummer eller en bestemt bokføringsdato.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="6f5a7-126">Forretningskontakt</span><span class="sxs-lookup"><span data-stu-id="6f5a7-126">Business Contact</span></span> |<span data-ttu-id="6f5a7-127">Vis poster basert på en bestemt kontakttype, kontaktnummer og/eller eksternt dokumentnummer.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="6f5a7-128">Du kan skrive inn dokumentinformasjon som ble tilordnet av en leverandør eller en kunde.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="6f5a7-129">Bruk de tilgjengelige feltene til å søke etter leverandørs bilagsnummer ved hjelp av numrene som leverandøren har knyttet til dokumentene.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="6f5a7-130">Varereferanse</span><span class="sxs-lookup"><span data-stu-id="6f5a7-130">Item reference</span></span>|<span data-ttu-id="6f5a7-131">Vis poster basert på serienummer eller partinummer.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="6f5a7-132">Du kan angi partinummeret eller serienummeret, eller filtrere på partinummeret eller serienummeret du vil søke etter.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="6f5a7-133">Denne handlingen er nyttig hvis du vil se hvor et bestemt varesporingsnummer er brukt, hvilken leverandør det kom fra, eller hvilken kunde det ble solgt til.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="6f5a7-134">Når du har gjort et valg, angir du relevant søkeinformasjon i feltene øverst.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="6f5a7-135">Bruk verktøytipsene i feltene som hjelp.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="6f5a7-136">Når du er ferdig, velger du **Søk** for å starte søket.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="6f5a7-137">Hvis du endrer noen av filtrene, må du velge **Søk** på nytt.</span><span class="sxs-lookup"><span data-stu-id="6f5a7-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="6f5a7-138">Hvis du vil se noen eksempler på hvordan du bruker **Søk etter poster**, kan du se [Spor varesporede varer](inventory-how-to-trace-item-tracked-items.md)</span><span class="sxs-lookup"><span data-stu-id="6f5a7-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md)</span></span> <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="6f5a7-139">Se relatert opplæring på [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="6f5a7-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="6f5a7-140">Se også</span><span class="sxs-lookup"><span data-stu-id="6f5a7-140">See Also</span></span>

[<span data-ttu-id="6f5a7-141">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="6f5a7-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="6f5a7-142">Legge til en sidehandling i rollesenteret</span><span class="sxs-lookup"><span data-stu-id="6f5a7-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="6f5a7-143">Spore varesporede varer</span><span class="sxs-lookup"><span data-stu-id="6f5a7-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
