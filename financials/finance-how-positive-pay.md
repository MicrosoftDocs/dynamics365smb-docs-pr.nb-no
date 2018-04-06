---
title: Eksportere Positive Pay-filer | Microsoft-dokumentasjon
description: "Du kan sikre at banken bare innfrir validerte sjekker og beløp, ved å eksportere en Positive Pay-fil som inneholder leverandør-og betalingsinformasjon."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57580354c2ea5b63162e1539cf2f97eb9770c50b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="fd388-103">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="fd388-103">Export a Positive Pay file</span></span>
<span data-ttu-id="fd388-104">For å sørge for at banken bare innfrir validerte sjekker og beløp, kan du eksportere en Positive Pay-fil med relevant leverandørinformasjon, sjekknummer og betalingskonto, som du deretter sender til banken for referanse når du behandler betalinger.</span><span class="sxs-lookup"><span data-stu-id="fd388-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fd388-105"> er forhåndskonfigurert til å støtte Positive Pay-filer for Bank of America og City Bank.</span><span class="sxs-lookup"><span data-stu-id="fd388-105"> is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="fd388-106">Slik definerer du en bankkonto for Positive Pay</span><span class="sxs-lookup"><span data-stu-id="fd388-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="fd388-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fd388-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fd388-108">Åpne kortet for bank du vil bruke Positive Pay for.</span><span class="sxs-lookup"><span data-stu-id="fd388-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="fd388-109">Angi POSPAYBANK i feltet **Kode for eksport for Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="fd388-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="fd388-110">Lukk vinduet.</span><span class="sxs-lookup"><span data-stu-id="fd388-110">Close the window.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="fd388-111">Slik eksporterer du en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="fd388-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="fd388-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fd388-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fd388-113">Velg bankkontoen som du vil eksportere en Positive Pay-fil for.</span><span class="sxs-lookup"><span data-stu-id="fd388-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="fd388-114">Velg **Eksport for Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="fd388-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="fd388-115">Vinduet **Eksport for Positive Pay** åpnes med betalinger som er gjort for bankkontoen siden den forrige datoen for opplasting, som vist i feltene **Dato for siste oppdatering** og **Klokkeslett for siste oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="fd388-115">The **Positive Pay Export** window opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="fd388-116">I feltet **Dato for frist for oppdatering** field angir du en dato, og betalinger blir ikke inkludert i den eksporterte filen før denne datoen.</span><span class="sxs-lookup"><span data-stu-id="fd388-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="fd388-117">Velg handlingen **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="fd388-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="fd388-118">I **Eksporter fil**-vinduet velger du **Lagre**-knappen, og deretter lagrer du filen på en passende plassering.</span><span class="sxs-lookup"><span data-stu-id="fd388-118">In the **Export File** window, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="fd388-119">Last opp filen til det elektroniske bankområdet.</span><span class="sxs-lookup"><span data-stu-id="fd388-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="fd388-120">Skriv ned eller kopier bekreftelsesnummeret som vises når filopplastingen er vellykket.</span><span class="sxs-lookup"><span data-stu-id="fd388-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="fd388-121">Vise eksporterte Positive Pay-poster</span><span class="sxs-lookup"><span data-stu-id="fd388-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="fd388-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fd388-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fd388-123">Velg bankkontoen som du vil vise Positive Pay-eksportposter for.</span><span class="sxs-lookup"><span data-stu-id="fd388-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="fd388-124">Velg **Poster for Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="fd388-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="fd388-125">I vinduet **Poster for Positive Pay** kan du se alle Positive Pay-eksportpostene for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="fd388-125">In the **Positive Pay Entries** window, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="fd388-126">I feltet **Bekreftelsesnummer** angir du bekreftelsesnummeret som du får når opplastingen av filen til banken er vellykket, for hver post for eksport.</span><span class="sxs-lookup"><span data-stu-id="fd388-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="fd388-127">For å vise de relaterte betalingslinjene, velger du **Detaljer for poster for Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="fd388-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="fd388-128">Eksportere Positive Pay-filer på nytt</span><span class="sxs-lookup"><span data-stu-id="fd388-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="fd388-129">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fd388-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="fd388-130">Velg bankkontoen som du vil eksportere Positive Pay-filer på nytt for.</span><span class="sxs-lookup"><span data-stu-id="fd388-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="fd388-131">Velg **Poster for Positive Pay**.</span><span class="sxs-lookup"><span data-stu-id="fd388-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="fd388-132">Velg linjen for Positive Pay-eksportfilen som du vil eksportere på nytt.</span><span class="sxs-lookup"><span data-stu-id="fd388-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="fd388-133">I vinduet **Poster for Positive Pay** velger du **Eksporter Positive Pay til fil på nytt**.</span><span class="sxs-lookup"><span data-stu-id="fd388-133">In the **Positive Pay Entries** window, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd388-134">Se også</span><span class="sxs-lookup"><span data-stu-id="fd388-134">See Also</span></span>
[<span data-ttu-id="fd388-135">Finans</span><span class="sxs-lookup"><span data-stu-id="fd388-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="fd388-136">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="fd388-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="fd388-137">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="fd388-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="fd388-138">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd388-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

