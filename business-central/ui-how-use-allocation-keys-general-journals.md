---
title: Bruke fordelingsnøkler i finanskladder | Microsoft-dokumentasjon
description: Lær hvordan du kan bruke fordelingsnøkler i kladder.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 84ea436a7e7edc6851b97b718b66195edddd2da2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760495"
---
# <a name="use-allocation-keys-in-general-journals"></a><span data-ttu-id="990f3-103">Bruke fordelingsnøkler i finanskladder</span><span class="sxs-lookup"><span data-stu-id="990f3-103">Use Allocation Keys in General Journals</span></span>
<span data-ttu-id="990f3-104">Du kan fordele en post i en finanskladd på flere forskjellige konti når du bokfører kladden.</span><span class="sxs-lookup"><span data-stu-id="990f3-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="990f3-105">Fordelingen kan gjøres etter antall, prosent eller beløp.</span><span class="sxs-lookup"><span data-stu-id="990f3-105">The allocation can be made by quantity, percentage, or amount.</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="990f3-106">Definere fordelingsnøkler</span><span class="sxs-lookup"><span data-stu-id="990f3-106">To set up allocation keys</span></span>
1. <span data-ttu-id="990f3-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Gjentakende finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="990f3-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="990f3-108">Velg feltet **Bunkenavn** for å åpne siden **Finanskladder**.</span><span class="sxs-lookup"><span data-stu-id="990f3-108">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="990f3-109">Du kan endre fordelinger på en eksisterende bunke i listen, eller du kan opprette en ny bunke med tildelinger.</span><span class="sxs-lookup"><span data-stu-id="990f3-109">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="990f3-110">Hvis du vil opprette en ny bunke, velger du handlingen **Ny** og går til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="990f3-110">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="990f3-111">Hvis du vil endre fordelinger for en eksisterende kladd, velger du kladden og går til trinn 7.</span><span class="sxs-lookup"><span data-stu-id="990f3-111">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="990f3-112">I feltet **Navn** skriver du inn et navn på kladden, for eksempel RENGJØRING.</span><span class="sxs-lookup"><span data-stu-id="990f3-112">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="990f3-113">I feltet **Beskrivelse** angir du en beskrivelse som for eksempel Kladd for rengjøringsutgifter.</span><span class="sxs-lookup"><span data-stu-id="990f3-113">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="990f3-114">Når du er ferdig, lukker du siden.</span><span class="sxs-lookup"><span data-stu-id="990f3-114">When you are done, close the page.</span></span> <span data-ttu-id="990f3-115">En ny, tom gjentakende kladd åpnes.</span><span class="sxs-lookup"><span data-stu-id="990f3-115">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="990f3-116">Fyll ut feltene på linjen.</span><span class="sxs-lookup"><span data-stu-id="990f3-116">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="990f3-117">Velg handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="990f3-117">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="990f3-118">Legg til en linje for hver fordeling.</span><span class="sxs-lookup"><span data-stu-id="990f3-118">Add a line for each allocation.</span></span> <span data-ttu-id="990f3-119">Du må fylle ut enten feltet **Andel i pst.**, **Andel i antall** eller **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="990f3-119">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="990f3-120">Du må også fylle ut feltet **Kontonr.** og, hvis du fordeler transaksjonen på globale dimensjoner, feltene for globale dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="990f3-120">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="990f3-121">Hvis du angir en prosentsats på en linje, beregnes beløpet i feltet **Beløp** automatisk.</span><span class="sxs-lookup"><span data-stu-id="990f3-121">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="990f3-122">Disse beløpene har motsatt fortegn av det totale beløpet i feltet **Beløp** i den gjentakende kladden.</span><span class="sxs-lookup"><span data-stu-id="990f3-122">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="990f3-123">Når du har angitt fordelingslinjene, velger du **OK** for å gå tilbake til siden **Gjentakende finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="990f3-123">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="990f3-124">Feltet **Fordelt beløp (USD)** fylles ut og samsvarer med **Beløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="990f3-124">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="990f3-125">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="990f3-125">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="990f3-126">Slik endrer du en fordelingsnøkkel som allerede er definert</span><span class="sxs-lookup"><span data-stu-id="990f3-126">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="990f3-127">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Gjentakende finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="990f3-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="990f3-128">Velg kladden med fordelingen, på siden **Finansgjentak.kladd**.</span><span class="sxs-lookup"><span data-stu-id="990f3-128">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="990f3-129">Velg linjen med fordelingen, og velg deretter handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="990f3-129">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="990f3-130">Endre de relevante feltene, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="990f3-130">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="990f3-131">Se også</span><span class="sxs-lookup"><span data-stu-id="990f3-131">See Also</span></span>
[<span data-ttu-id="990f3-132">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="990f3-132">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="990f3-133">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="990f3-133">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="990f3-134">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="990f3-134">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
