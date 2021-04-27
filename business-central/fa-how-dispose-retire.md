---
title: Avhende eller trekke tilbake aktiva | Microsoft-dokumentasjon
description: Du må bokføre en salgsverdi når du kasserer, selger eller trekker tilbake et aktivum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 041f228a0ea2e34fb9986ebb45e98c1300f02f8d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774033"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="05f26-103">Avhending eller tilbaketrekking av aktiva</span><span class="sxs-lookup"><span data-stu-id="05f26-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="05f26-104">Når du selger eller på annen måte avhender et aktiva, må salgsverdien bokføres for å beregne og registrere tap eller vinning.</span><span class="sxs-lookup"><span data-stu-id="05f26-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="05f26-105">En salgspost må være den siste posten som bokføres for et aktiva.</span><span class="sxs-lookup"><span data-stu-id="05f26-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="05f26-106">Du kan bokføre mer enn én salgspost for aktiva som er delvis solgt.</span><span class="sxs-lookup"><span data-stu-id="05f26-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="05f26-107">Summen av alle bokførte salgsbeløp må være et kreditbeløp.</span><span class="sxs-lookup"><span data-stu-id="05f26-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="05f26-108">Hvis du bytter ut et aktivum med et annet, må du registrere både salget av det gamle aktivumet (salg) og innkjøpet av det nye (anskaffelse).</span><span class="sxs-lookup"><span data-stu-id="05f26-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="05f26-109">Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="05f26-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="05f26-110">Følgende fremgangsmåte forutsetter at du allerede har konfigurert de aktuelle bokføringsgruppene på siden **Bokf. grupper-aktiva**.</span><span class="sxs-lookup"><span data-stu-id="05f26-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="05f26-111">Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="05f26-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="05f26-112">Slik bokfører du et salg fra aktivafinanskladden:</span><span class="sxs-lookup"><span data-stu-id="05f26-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="05f26-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="05f26-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="05f26-114">Opprett en innledende kladdelinje, og fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="05f26-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="05f26-115">I feltet **Aktivabokf.type** velger du **Salg**.</span><span class="sxs-lookup"><span data-stu-id="05f26-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="05f26-116">Velg **Sett inn aktivamotkonto**.</span><span class="sxs-lookup"><span data-stu-id="05f26-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="05f26-117">En ny kladdelinje opprettes for motkontoen som er satt opp for salgsbokføring.</span><span class="sxs-lookup"><span data-stu-id="05f26-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="05f26-118">Trinn 4 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder feltet **Konto for salg** finansdebetkontoen, og feltet **Motkonto for salg** inneholder finanskontoen du vil bokføre motposter for oppskrivning til.</span><span class="sxs-lookup"><span data-stu-id="05f26-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="05f26-119">Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="05f26-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="05f26-120">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="05f26-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="05f26-121">Hvis du selger eller på avhender deler av et aktiva, må du dele opp aktivaet før du kan registrere salgstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="05f26-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="05f26-122">Hvis du vil ha mer informasjon, kan du se [Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="05f26-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="05f26-123">Slik viser du salgsposter</span><span class="sxs-lookup"><span data-stu-id="05f26-123">To view disposal ledger entries</span></span>
<span data-ttu-id="05f26-124">Når du selger eller avhender et aktiva, bokføres salgsverdien til finans der du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="05f26-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="05f26-125">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="05f26-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="05f26-126">Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.</span><span class="sxs-lookup"><span data-stu-id="05f26-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="05f26-127">Velg avskrivningstablået du vil vise poster for, og velg deretter **Poster**.</span><span class="sxs-lookup"><span data-stu-id="05f26-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="05f26-128">Velg en linje med **Salg** i **Bokføringskategori, aktiva**-feltet, og velg deretter **Søk etter poster**.</span><span class="sxs-lookup"><span data-stu-id="05f26-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Find Entries** action.</span></span>  
5. <span data-ttu-id="05f26-129">På **Søk etter poster**-siden velger du finanspostlinjen og deretter **Vis relaterte poster**.</span><span class="sxs-lookup"><span data-stu-id="05f26-129">On the **Find Entries** page, select the general ledger entry line, and then choose the **Show Related Entries** action.</span></span>  

<span data-ttu-id="05f26-130">**Finansposter**-siden åpnes der du kan se postene som er resultat av salgsbokføringen.</span><span class="sxs-lookup"><span data-stu-id="05f26-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05f26-131">Se også</span><span class="sxs-lookup"><span data-stu-id="05f26-131">See Also</span></span>

[<span data-ttu-id="05f26-132">Aktiva</span><span class="sxs-lookup"><span data-stu-id="05f26-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="05f26-133">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="05f26-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="05f26-134">[Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="05f26-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="05f26-135">Finans</span><span class="sxs-lookup"><span data-stu-id="05f26-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="05f26-136">Bli klar til å gjøre forretninger</span><span class="sxs-lookup"><span data-stu-id="05f26-136">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="05f26-137">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="05f26-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="05f26-138">Søk etter poster</span><span class="sxs-lookup"><span data-stu-id="05f26-138">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]