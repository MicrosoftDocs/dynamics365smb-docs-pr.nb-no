---
title: "Oversikt over oppgaver for å fordele kostnader og inntekter | Microsoft-dokumentasjon"
description: "Skisserer oppgavene for å fordele en post i en finanskladd på flere forskjellige konti når du bokfører kladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2291f45cda61f72cbabc8a39b2463903c641ad97
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="52d8a-103">Fordele kostnader og inntekter</span><span class="sxs-lookup"><span data-stu-id="52d8a-103">Allocate Costs and Income</span></span>
<span data-ttu-id="52d8a-104">Du kan fordele en post i en finanskladd på flere forskjellige konti når du bokfører kladden.</span><span class="sxs-lookup"><span data-stu-id="52d8a-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="52d8a-105">Fordelingen kan gjøres med tre ulike metoder:</span><span class="sxs-lookup"><span data-stu-id="52d8a-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="52d8a-106">Antall</span><span class="sxs-lookup"><span data-stu-id="52d8a-106">Quantity</span></span>
* <span data-ttu-id="52d8a-107">Prosent (%)</span><span class="sxs-lookup"><span data-stu-id="52d8a-107">Percentage (%)</span></span>
* <span data-ttu-id="52d8a-108">Beløp</span><span class="sxs-lookup"><span data-stu-id="52d8a-108">Amount</span></span>

<span data-ttu-id="52d8a-109">Fordelingsfunksjonen kan brukes i forbindelse med gjentakende finanskladder og i aktivakladder.</span><span class="sxs-lookup"><span data-stu-id="52d8a-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="52d8a-110">De følgende fremgangsmåtene viser hvordan du forbereder deg på å fordele kost i en gjentakende finanskladd ved å definere fordelingsnøkler.</span><span class="sxs-lookup"><span data-stu-id="52d8a-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="52d8a-111">Når fordelingsnøkler er definert, fyller du ut og bokfører kladden som en hvilken som helst annen gjentakende finanskladd.</span><span class="sxs-lookup"><span data-stu-id="52d8a-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="52d8a-112">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="52d8a-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="52d8a-113">Definere fordelingsnøkler</span><span class="sxs-lookup"><span data-stu-id="52d8a-113">To set up allocation keys</span></span>
<span data-ttu-id="52d8a-114">Du kan fordele en post i en gjentakende finanskladd på flere forskjellige konti når du bokfører kladden.</span><span class="sxs-lookup"><span data-stu-id="52d8a-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="52d8a-115">Fordelingen kan gjøres etter antall, prosent eller beløp.</span><span class="sxs-lookup"><span data-stu-id="52d8a-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="52d8a-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Gjentakende finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52d8a-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="52d8a-117">Velg feltet **Bunkenavn** for å åpne vinduet **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="52d8a-118">Du kan endre fordelinger på en eksisterende bunke i listen, eller du kan opprette en ny bunke med tildelinger.</span><span class="sxs-lookup"><span data-stu-id="52d8a-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="52d8a-119">Hvis du vil opprette en ny bunke, velger du handlingen **Ny** og går til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="52d8a-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="52d8a-120">Hvis du vil endre fordelinger for en eksisterende kladd, velger du kladden og går til trinn 7.</span><span class="sxs-lookup"><span data-stu-id="52d8a-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="52d8a-121">I feltet **Navn** skriver du inn et navn på kladden, for eksempel RENGJØRING.</span><span class="sxs-lookup"><span data-stu-id="52d8a-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="52d8a-122">I feltet **Beskrivelse** angir du en beskrivelse som for eksempel Kladd for rengjøringsutgifter.</span><span class="sxs-lookup"><span data-stu-id="52d8a-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="52d8a-123">Når du er ferdig, lukker du vinduet.</span><span class="sxs-lookup"><span data-stu-id="52d8a-123">When you are done, close the window.</span></span> <span data-ttu-id="52d8a-124">En ny, tom gjentakende kladd åpnes.</span><span class="sxs-lookup"><span data-stu-id="52d8a-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="52d8a-125">Fyll ut feltene på linjen.</span><span class="sxs-lookup"><span data-stu-id="52d8a-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="52d8a-126">Velg handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="52d8a-127">Legg til en linje for hver fordeling.</span><span class="sxs-lookup"><span data-stu-id="52d8a-127">Add a line for each allocation.</span></span> <span data-ttu-id="52d8a-128">Du må fylle ut enten feltet **Andel i pst.**, **Andel i antall** eller **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="52d8a-129">Du må også fylle ut feltet **Kontonr.** og, hvis du fordeler transaksjonen på globale dimensjoner, feltene for globale dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="52d8a-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="52d8a-130">Hvis du angir en prosentsats på en linje, beregnes beløpet i feltet **Beløp** automatisk.</span><span class="sxs-lookup"><span data-stu-id="52d8a-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="52d8a-131">Disse beløpene har motsatt fortegn av det totale beløpet i feltet **Beløp** i den gjentakende kladden.</span><span class="sxs-lookup"><span data-stu-id="52d8a-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="52d8a-132">Når du har angitt fordelingslinjene, velger du **OK** for å gå tilbake til vinduet **Gjentakende finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="52d8a-133">Feltet **Fordelt beløp (USD)** fylles ut og samsvarer med **Beløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="52d8a-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="52d8a-134">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="52d8a-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="52d8a-135">Endre en fordelingsnøkkel som allerede er definert</span><span class="sxs-lookup"><span data-stu-id="52d8a-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="52d8a-136">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Gjentakende finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52d8a-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="52d8a-137">Velg kladden med fordelingen, i vinduet **Finansgjentak.kladd**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-137">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="52d8a-138">Velg linjen med fordelingen, og velg deretter handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="52d8a-139">Endre de relevante feltene, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="52d8a-140">Se også</span><span class="sxs-lookup"><span data-stu-id="52d8a-140">See Also</span></span>
[<span data-ttu-id="52d8a-141">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="52d8a-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="52d8a-142">[Arbeide med finanskladder](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="52d8a-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="52d8a-143">[Bokføre dokumenter og kladder](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="52d8a-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="52d8a-144">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52d8a-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

