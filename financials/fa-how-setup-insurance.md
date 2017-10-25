---
title: Definere aktivaforsikring | Microsoft-dokumentasjon
description: "Du definerer et forsikringskort og generell informasjon om forsikringspolise for å behandle forsikringsdekning for aktiva."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8e88002c920e392cd61f2a899811fd0434d8cb4b
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-insurance"></a><span data-ttu-id="4fdcc-103">Definere aktivaforsikring</span><span class="sxs-lookup"><span data-stu-id="4fdcc-103">How to: Set Up Fixed Asset Insurance</span></span>
<span data-ttu-id="4fdcc-104">Hvis du vil behandle forsikringsdekning for aktiva, må du først sette opp noen generelle forsikringsopplysninger og et forsikringskort per polise.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-104">To manage fixed asset insurance coverage, you must first set up some general insurance information and an insurance card per policy.</span></span>

## <a name="to-set-up-general-insurance-information"></a><span data-ttu-id="4fdcc-105">Slik definerer du generelle forsikringsopplysninger</span><span class="sxs-lookup"><span data-stu-id="4fdcc-105">To set up general insurance information</span></span>
<span data-ttu-id="4fdcc-106">Hvis du vil bruke forsikringsfunksjoner i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi noen generelle forsikringsopplysninger.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-106">To use the insurance features in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set up some general insurance information.</span></span>  

1. <span data-ttu-id="4fdcc-107">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Aktivaoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Setups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fdcc-108">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-108">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a><span data-ttu-id="4fdcc-109">Slik definerer du forsikringstyper</span><span class="sxs-lookup"><span data-stu-id="4fdcc-109">To set up insurance types</span></span>
<span data-ttu-id="4fdcc-110">Du kan gruppere forsikringspoliser i kategorier, for eksempel tyveriforsikring og brannforsikring.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-110">You can group your insurance policies into categories, such as insurance against theft or fire insurance.</span></span> <span data-ttu-id="4fdcc-111">Forsikringstypene brukes på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-111">The insurance types are used on the insurance card.</span></span>

1. <span data-ttu-id="4fdcc-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringstyper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Types**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fdcc-113">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-113">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-cards"></a><span data-ttu-id="4fdcc-114">Slik definerer du forsikringskort</span><span class="sxs-lookup"><span data-stu-id="4fdcc-114">To set up insurance cards</span></span>
<span data-ttu-id="4fdcc-115">Du kan samle opplysninger om hver enkelt forsikringspolise på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-115">You may accumulate information about each insurance policy on the insurance card.</span></span>  

1. <span data-ttu-id="4fdcc-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikring**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fdcc-117">Velg **Ny** for å opprette et nytt forsikringskort i **Forsikring**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-117">In the **Insurance** window, choose the **New** action to create a  new insurance card.</span></span>  
3. <span data-ttu-id="4fdcc-118">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-118">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-templates"></a><span data-ttu-id="4fdcc-119">Slik definerer du forsikringskladdemaler</span><span class="sxs-lookup"><span data-stu-id="4fdcc-119">To set up insurance journal templates</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="4fdcc-120"> oppretter automatisk en forsikringskladdemal første gang du åpner **Forsikringskladd**-vinduet, men du kan definere flere kladdemaler.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-120"> automatically creates an insurance journal template the first time that you open the **Insurance Journal** window, but you can set up additional journal templates.</span></span> <span data-ttu-id="4fdcc-121">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="4fdcc-121">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  

1. <span data-ttu-id="4fdcc-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fdcc-123">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-123">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-batches"></a><span data-ttu-id="4fdcc-124">Slik definerer du forsikringskladder</span><span class="sxs-lookup"><span data-stu-id="4fdcc-124">To set up insurance journal batches</span></span>
<span data-ttu-id="4fdcc-125">Du kan definere kladder i en forsikringskladdemal.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-125">You can set up batches in an insurance journal template.</span></span> <span data-ttu-id="4fdcc-126">Verdiene i kladden brukes som standardverdier hvis ikke feltene på kladdelinjene er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-126">The values in the journal batch are used as default values if the fields are not filled in on the journal lines.</span></span> <span data-ttu-id="4fdcc-127">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-127">For more information, see [Work with General Journals](ui-work-general-journals.md)</span></span>  

1. <span data-ttu-id="4fdcc-128">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fdcc-129">Velg en forsikringskladdemal, og velg deretter **Kladder**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-129">Select an insurance journal template, and then choose the **Batches** action.</span></span>
3. <span data-ttu-id="4fdcc-130">I vinduet **Forsikringskladder** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-130">In the **Insurance Journal Batches** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4fdcc-131">Tall har en bestemt funksjon i kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-131">Numbers have a special function in journal names.</span></span> <span data-ttu-id="4fdcc-132">Hvis en kladdemal eller et kladdenavn inneholder et tall, øker tallet automatisk med én hver gang du bokfører en kladd.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-132">If a journal template name or journal batch name contains a number, the number automatically advances by one every time that the journal is posted.</span></span> <span data-ttu-id="4fdcc-133">Hvis for eksempel HH1 er angitt i feltet **Navn**, endres kladdenavnet til HH2 etter at kladden HH1 er bokført.</span><span class="sxs-lookup"><span data-stu-id="4fdcc-133">For example, if HH1 is entered in the **Name** field, the journal name will change to HH2 after the journal named HH1 has been posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="4fdcc-134">Se også</span><span class="sxs-lookup"><span data-stu-id="4fdcc-134">See Also</span></span>
[<span data-ttu-id="4fdcc-135">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="4fdcc-135">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="4fdcc-136">Aktiva</span><span class="sxs-lookup"><span data-stu-id="4fdcc-136">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="4fdcc-137">Finans</span><span class="sxs-lookup"><span data-stu-id="4fdcc-137">Finance</span></span>](finance.md)  
<span data-ttu-id="4fdcc-138">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-138">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="4fdcc-139">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

