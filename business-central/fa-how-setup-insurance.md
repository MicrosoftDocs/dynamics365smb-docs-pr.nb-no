---
title: Definere aktivaforsikring | Microsoft-dokumentasjon
description: Du definerer et forsikringskort og generell informasjon om forsikringspolise for å behandle forsikringsdekning for aktiva.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ebb62a4ef9ea84ec5bfddc099dfb6120a4e6405
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774044"
---
# <a name="set-up-fixed-asset-insurance"></a><span data-ttu-id="87d57-103">Definere aktivaforsikring</span><span class="sxs-lookup"><span data-stu-id="87d57-103">Set Up Fixed Asset Insurance</span></span>
<span data-ttu-id="87d57-104">Hvis du vil behandle forsikringsdekning for aktiva, må du først sette opp noen generelle forsikringsopplysninger og et forsikringskort per polise.</span><span class="sxs-lookup"><span data-stu-id="87d57-104">To manage fixed asset insurance coverage, you must first set up some general insurance information and an insurance card per policy.</span></span>

## <a name="to-set-up-general-insurance-information"></a><span data-ttu-id="87d57-105">Slik definerer du generelle forsikringsopplysninger</span><span class="sxs-lookup"><span data-stu-id="87d57-105">To set up general insurance information</span></span>
<span data-ttu-id="87d57-106">Hvis du vil bruke forsikringsfunksjoner i [!INCLUDE[prod_short](includes/prod_short.md)], må du angi noen generelle forsikringsopplysninger.</span><span class="sxs-lookup"><span data-stu-id="87d57-106">To use the insurance features in [!INCLUDE[prod_short](includes/prod_short.md)], you must set up some general insurance information.</span></span>  

1. <span data-ttu-id="87d57-107">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktivaoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Setups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d57-108">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d57-108">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a><span data-ttu-id="87d57-109">Slik definerer du forsikringstyper</span><span class="sxs-lookup"><span data-stu-id="87d57-109">To set up insurance types</span></span>
<span data-ttu-id="87d57-110">Du kan gruppere forsikringspoliser i kategorier, for eksempel tyveriforsikring og brannforsikring.</span><span class="sxs-lookup"><span data-stu-id="87d57-110">You can group your insurance policies into categories, such as insurance against theft or fire insurance.</span></span> <span data-ttu-id="87d57-111">Forsikringstypene brukes på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="87d57-111">The insurance types are used on the insurance card.</span></span>

1. <span data-ttu-id="87d57-112">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringstyper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Types**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d57-113">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d57-113">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-cards"></a><span data-ttu-id="87d57-114">Slik definerer du forsikringskort</span><span class="sxs-lookup"><span data-stu-id="87d57-114">To set up insurance cards</span></span>
<span data-ttu-id="87d57-115">Du kan samle opplysninger om hver enkelt forsikringspolise på forsikringskortet.</span><span class="sxs-lookup"><span data-stu-id="87d57-115">You may accumulate information about each insurance policy on the insurance card.</span></span>  

1. <span data-ttu-id="87d57-116">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikring**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d57-117">Velg **Ny** for å opprette et nytt forsikringskort på **Forsikring**-siden.</span><span class="sxs-lookup"><span data-stu-id="87d57-117">On the **Insurance** page, choose the **New** action to create a  new insurance card.</span></span>  
3. <span data-ttu-id="87d57-118">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d57-118">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-templates"></a><span data-ttu-id="87d57-119">Slik definerer du forsikringskladdemaler</span><span class="sxs-lookup"><span data-stu-id="87d57-119">To set up insurance journal templates</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="87d57-120">oppretter automatisk en forsikringskladdemal første gang du åpner **Forsikringskladd**-siden, men du kan definere flere kladdemaler.</span><span class="sxs-lookup"><span data-stu-id="87d57-120">automatically creates an insurance journal template the first time that you open the **Insurance Journal** page, but you can set up additional journal templates.</span></span> <span data-ttu-id="87d57-121">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="87d57-121">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>  

1. <span data-ttu-id="87d57-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d57-123">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d57-123">Fill in the fields as necessary.</span></span>

## <a name="to-set-up-insurance-journal-batches"></a><span data-ttu-id="87d57-124">Slik definerer du forsikringskladder</span><span class="sxs-lookup"><span data-stu-id="87d57-124">To set up insurance journal batches</span></span>
<span data-ttu-id="87d57-125">Du kan definere kladder i en forsikringskladdemal.</span><span class="sxs-lookup"><span data-stu-id="87d57-125">You can set up batches in an insurance journal template.</span></span> <span data-ttu-id="87d57-126">Verdiene i kladden brukes som standardverdier hvis ikke feltene på kladdelinjene er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="87d57-126">The values in the journal batch are used as default values if the fields are not filled in on the journal lines.</span></span> <span data-ttu-id="87d57-127">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md)</span><span class="sxs-lookup"><span data-stu-id="87d57-127">For more information, see [Work with General Journals](ui-work-general-journals.md)</span></span>  

1. <span data-ttu-id="87d57-128">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Insurance Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87d57-129">Velg en forsikringskladdemal, og velg deretter **Kladder**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="87d57-129">Select an insurance journal template, and then choose the **Batches** action.</span></span>
3. <span data-ttu-id="87d57-130">På siden **Forsikringskladder** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="87d57-130">On the **Insurance Journal Batches** page, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="87d57-131">Tall har en bestemt funksjon i kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="87d57-131">Numbers have a special function in journal names.</span></span> <span data-ttu-id="87d57-132">Hvis en kladdemal eller et kladdenavn inneholder et tall, øker tallet automatisk med én hver gang du bokfører en kladd.</span><span class="sxs-lookup"><span data-stu-id="87d57-132">If a journal template name or journal batch name contains a number, the number automatically advances by one every time that the journal is posted.</span></span> <span data-ttu-id="87d57-133">Hvis for eksempel HH1 er angitt i feltet **Navn**, endres kladdenavnet til HH2 etter at kladden HH1 er bokført.</span><span class="sxs-lookup"><span data-stu-id="87d57-133">For example, if HH1 is entered in the **Name** field, the journal name will change to HH2 after the journal named HH1 has been posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="87d57-134">Se også</span><span class="sxs-lookup"><span data-stu-id="87d57-134">See Also</span></span>
[<span data-ttu-id="87d57-135">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="87d57-135">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="87d57-136">Aktiva</span><span class="sxs-lookup"><span data-stu-id="87d57-136">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="87d57-137">Finans</span><span class="sxs-lookup"><span data-stu-id="87d57-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="87d57-138">Bli klar til å gjøre forretninger</span><span class="sxs-lookup"><span data-stu-id="87d57-138">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="87d57-139">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87d57-139">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]