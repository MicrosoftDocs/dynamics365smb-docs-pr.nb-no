---
title: Opprette OCR-betalinger
description: "Du kan behandle elektroniske betalinger fra kunder i henhold til en forhåndsdefinert betalings-ID. Dette blir ofte referert til som en OCR-betaling (optisk tegngjenkjenning)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: 330570f356d923dadfc3128e79d8dad91ddf5fcb
ms.contentlocale: nb-no
ms.lasthandoff: 10/15/2018

---
# <a name="set-up-ocr-payments"></a><span data-ttu-id="a61a6-104">Opprette OCR-betalinger</span><span class="sxs-lookup"><span data-stu-id="a61a6-104">Set Up OCR Payments</span></span>
<span data-ttu-id="a61a6-105">Du kan behandle elektroniske betalinger fra kunder i henhold til en forhåndsdefinert betalings-ID.</span><span class="sxs-lookup"><span data-stu-id="a61a6-105">You can process electronic payments from customers according to a predefined payment ID.</span></span> <span data-ttu-id="a61a6-106">Dette blir ofte referert til som en OCR-betaling (optisk tegngjenkjenning).</span><span class="sxs-lookup"><span data-stu-id="a61a6-106">This is often referred to as an optical character recognition (OCR) payment.</span></span> <span data-ttu-id="a61a6-107">Betalings-ID-en brukes med elektroniske betalingstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a61a6-107">The payment ID is used with electronic payment transactions.</span></span> <span data-ttu-id="a61a6-108">Kunder kan vise til denne ID-en når de foretar betalinger.</span><span class="sxs-lookup"><span data-stu-id="a61a6-108">Customers can refer to this ID when they make payments.</span></span> <span data-ttu-id="a61a6-109">Betalings-IDen brukes også til å identifisere importerte betalingstransaksjoner og anvende importerte betalingsdata automatisk.</span><span class="sxs-lookup"><span data-stu-id="a61a6-109">The payment ID is also used to identify imported payment transactions and automatically apply imported payment data.</span></span>  

## <a name="to-set-up-ocr-payments"></a><span data-ttu-id="a61a6-110">Slik oppretter du OCR-betalinger</span><span class="sxs-lookup"><span data-stu-id="a61a6-110">To set up OCR payments</span></span>  

1.  <span data-ttu-id="a61a6-111">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **OCR-oppsett**, og angi deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a61a6-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a61a6-112">I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a61a6-112">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a61a6-113">Felt</span><span class="sxs-lookup"><span data-stu-id="a61a6-113">Field</span></span>|<span data-ttu-id="a61a6-114">Description</span><span class="sxs-lookup"><span data-stu-id="a61a6-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a61a6-115">**Format**</span><span class="sxs-lookup"><span data-stu-id="a61a6-115">**Format**</span></span>|<span data-ttu-id="a61a6-116">Velg et OCR-betalingsfilformat.</span><span class="sxs-lookup"><span data-stu-id="a61a6-116">Select an OCR payment file format.</span></span> <span data-ttu-id="a61a6-117">Formater inkluderer **BBS** og **Datadialog**.</span><span class="sxs-lookup"><span data-stu-id="a61a6-117">Formats include **BBS** and **Data Dialog**.</span></span>|  
    |<span data-ttu-id="a61a6-118">**Filnavn**</span><span class="sxs-lookup"><span data-stu-id="a61a6-118">**FileName**</span></span>|<span data-ttu-id="a61a6-119">Skriv inn hele banen til OCR-betalingsfilen.</span><span class="sxs-lookup"><span data-stu-id="a61a6-119">Enter the full path of the OCR payment file.</span></span>|  
    |<span data-ttu-id="a61a6-120">**Slett returfil**</span><span class="sxs-lookup"><span data-stu-id="a61a6-120">**Delete Return File**</span></span>|<span data-ttu-id="a61a6-121">Velg dette alternativet for å gi filen nytt navn etter import og forhindre at filen importeres mer enn én gang.</span><span class="sxs-lookup"><span data-stu-id="a61a6-121">Select to rename the file after import and prevent the file from being imported more than one time.</span></span>|  

3.  <span data-ttu-id="a61a6-122">I hurtigfanen **Finans** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a61a6-122">On the **Gen. Ledger** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a61a6-123">Felt</span><span class="sxs-lookup"><span data-stu-id="a61a6-123">Field</span></span>|<span data-ttu-id="a61a6-124">Description</span><span class="sxs-lookup"><span data-stu-id="a61a6-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a61a6-125">**Motkontotype**</span><span class="sxs-lookup"><span data-stu-id="a61a6-125">**Bal. Account Type**</span></span>|<span data-ttu-id="a61a6-126">Velg en motkontotype.</span><span class="sxs-lookup"><span data-stu-id="a61a6-126">Select a balance account type.</span></span> <span data-ttu-id="a61a6-127">Motkontotyper inkluderer **Finanskonto** og **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="a61a6-127">Balance account types include **Gen. Ledg. Account** and **Bank Account**.</span></span>|  
    |<span data-ttu-id="a61a6-128">**Motkontonr.**</span><span class="sxs-lookup"><span data-stu-id="a61a6-128">**Bal. Account No.**</span></span>|<span data-ttu-id="a61a6-129">Velg et motkontonummer.</span><span class="sxs-lookup"><span data-stu-id="a61a6-129">Select a balance account number.</span></span>|  
    |<span data-ttu-id="a61a6-130">**Maks. differanse**</span><span class="sxs-lookup"><span data-stu-id="a61a6-130">**Max. Divergence**</span></span>|<span data-ttu-id="a61a6-131">Angi høyeste differanseverdi.</span><span class="sxs-lookup"><span data-stu-id="a61a6-131">Enter a maximum divergence value.</span></span> <span data-ttu-id="a61a6-132">Hvis differansen i en betaling er mindre enn eller lik den angitte verdien, bokføres differansebeløpet automatisk.</span><span class="sxs-lookup"><span data-stu-id="a61a6-132">If the divergence on a payment is less than or equal to the value entered, the divergence amount is automatically posted.</span></span> <span data-ttu-id="a61a6-133">Hvis ikke, blir beløpet ikke bokført automatisk.</span><span class="sxs-lookup"><span data-stu-id="a61a6-133">Otherwise, the divergence is not automatically posted.</span></span> <span data-ttu-id="a61a6-134">I begge tilfeller vises en advarsel i innbetalingskladden ved import av OCR-girobetalinger.</span><span class="sxs-lookup"><span data-stu-id="a61a6-134">In both situations, a warning is displayed in the cash receipt journal when importing OCR Giro payments.</span></span>|  
    |<span data-ttu-id="a61a6-135">**Kontonr. differanse**</span><span class="sxs-lookup"><span data-stu-id="a61a6-135">**Divergence Account No.**</span></span>|<span data-ttu-id="a61a6-136">Angi avvikkontonummeret det skal bokføres på.</span><span class="sxs-lookup"><span data-stu-id="a61a6-136">Enter the divergence account number that will receive posting.</span></span>|  
    |<span data-ttu-id="a61a6-137">**Kladdemalnavn**</span><span class="sxs-lookup"><span data-stu-id="a61a6-137">**Journal Template Name**</span></span>|<span data-ttu-id="a61a6-138">Velg navnet på kladdemalen som skal motta de importerte OCR-girobetalingene.</span><span class="sxs-lookup"><span data-stu-id="a61a6-138">Select the name of the journal template that should receive the imported OCR Giro payments.</span></span>|  
    |<span data-ttu-id="a61a6-139">**Kladdenavn**</span><span class="sxs-lookup"><span data-stu-id="a61a6-139">**Journal Name**</span></span>|<span data-ttu-id="a61a6-140">Velg navnet på kladden som skal motta de importerte OCR-girobetalingene.</span><span class="sxs-lookup"><span data-stu-id="a61a6-140">Select the name of the journal that should receive the imported OCR Giro payments.</span></span><br /><br /> <span data-ttu-id="a61a6-141">Hvis feltene **Kladdemalnavn** og **Kladdenavn** er tomme, kan du importere OCR-girobetalinger til en hvilken som helst kladd.</span><span class="sxs-lookup"><span data-stu-id="a61a6-141">If the **Journal Template Name** and **Journal Name** fields are blank, you can import OCR Giro payments in any journal.</span></span> <span data-ttu-id="a61a6-142">Ellers må du importere OCR-girobetalingene til den angitte kladden.</span><span class="sxs-lookup"><span data-stu-id="a61a6-142">Otherwise, you must import OCR Giro payments in the journal that is specified.</span></span>|  

4.  <span data-ttu-id="a61a6-143">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a61a6-143">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a61a6-144">OCR-betalinger kan bare bokføres i innbetalingskladder når feltet **Avstem per bilag** er tomt i tabellen **Finanskladdemal**.</span><span class="sxs-lookup"><span data-stu-id="a61a6-144">OCR payments can only be posted to cash receipt journals when the **Force Doc. Balance** field has been cleared in the **Gen. Journal Template** table.</span></span> <span data-ttu-id="a61a6-145">Hvis du vil ha mer informasjon, kan du se Finanskladdemal.</span><span class="sxs-lookup"><span data-stu-id="a61a6-145">For more information, see Gen. Journal Template.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a61a6-146">Se også</span><span class="sxs-lookup"><span data-stu-id="a61a6-146">See Also</span></span>  
 <span data-ttu-id="a61a6-147">[Elektroniske banktjenester i Norge](electronic-banking-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="a61a6-147">[Electronic Banking in Norway](electronic-banking-in-norway.md) </span></span>  
 <span data-ttu-id="a61a6-148">[Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md) </span><span class="sxs-lookup"><span data-stu-id="a61a6-148">[Set Up KID Numbers on Sales Documents](how-to-set-up-kid-numbers-on-sales-documents.md) </span></span>  
 <span data-ttu-id="a61a6-149">[Importere og bokføre OCR-betalinger](how-to-import-and-post-ocr-payments.md) </span><span class="sxs-lookup"><span data-stu-id="a61a6-149">[Import and Post OCR Payments](how-to-import-and-post-ocr-payments.md) </span></span>  
 [<span data-ttu-id="a61a6-150">Skrive ut rapporten OCR-kladd - test</span><span class="sxs-lookup"><span data-stu-id="a61a6-150">Print the OCR Journal - Test Report</span></span>](how-to-print-the-ocr-journal-test-report.md)   
 

