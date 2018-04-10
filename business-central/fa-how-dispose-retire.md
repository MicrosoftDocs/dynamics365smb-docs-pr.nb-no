---
title: Avhende eller trekke tilbake aktiva | Microsoft-dokumentasjon
description: "Du må bokføre en salgsverdi når du kasserer, selger eller trekker tilbake et aktivum."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f2ccb2c7c020220383591c468b9f0729722ea1b8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="84a93-103">Avhending eller tilbaketrekking av aktiva</span><span class="sxs-lookup"><span data-stu-id="84a93-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="84a93-104">Når du selger eller på annen måte avhender et aktiva, må salgsverdien bokføres for å beregne og registrere tap eller vinning.</span><span class="sxs-lookup"><span data-stu-id="84a93-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="84a93-105">En salgspost må være den siste posten som bokføres for et aktiva.</span><span class="sxs-lookup"><span data-stu-id="84a93-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="84a93-106">Du kan bokføre mer enn én salgspost for aktiva som er delvis solgt.</span><span class="sxs-lookup"><span data-stu-id="84a93-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="84a93-107">Summen av alle bokførte salgsbeløp må være et kreditbeløp.</span><span class="sxs-lookup"><span data-stu-id="84a93-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="84a93-108">Hvis du bytter ut et aktivum med et annet, må du registrere både salget av det gamle aktivumet (salg) og innkjøpet av det nye (anskaffelse).</span><span class="sxs-lookup"><span data-stu-id="84a93-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="84a93-109">Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="84a93-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="84a93-110">Slik bokfører du et salg fra aktivafinanskladden:</span><span class="sxs-lookup"><span data-stu-id="84a93-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="84a93-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="84a93-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="84a93-112">Opprett en innledende kladdelinje, og fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="84a93-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="84a93-113">I feltet **Aktivabokf.type** velger du **Salg**.</span><span class="sxs-lookup"><span data-stu-id="84a93-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="84a93-114">Velg **Sett inn aktivamotkonto**.</span><span class="sxs-lookup"><span data-stu-id="84a93-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="84a93-115">En ny kladdelinje opprettes for motkontoen som er satt opp for salgsbokføring.</span><span class="sxs-lookup"><span data-stu-id="84a93-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="84a93-116">Trinn 4 fungerer bare hvis du har definert følgende: I vinduet **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder feltet **Konto for salg** finansdebetkontoen, og feltet **Motkonto for salg** inneholder finanskontoen du vil bokføre motposter for oppskrivning til.</span><span class="sxs-lookup"><span data-stu-id="84a93-116">Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="84a93-117">Hvis du vil ha mer informasjon, kan du se Definere bokføringsgrupper for aktiva i [Definere generell aktivainformasjon](fa-how-setup-general.md).</span><span class="sxs-lookup"><span data-stu-id="84a93-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="84a93-118">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="84a93-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="84a93-119">Hvis du selger eller på avhender deler av et aktiva, må du dele opp aktivaet før du kan registrere salgstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="84a93-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="84a93-120">Hvis du vil ha mer informasjon, kan du se [Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md).</span><span class="sxs-lookup"><span data-stu-id="84a93-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="84a93-121">Slik viser du salgsposter</span><span class="sxs-lookup"><span data-stu-id="84a93-121">To view disposal ledger entries</span></span>
<span data-ttu-id="84a93-122">Når du selger eller avhender et aktiva, bokføres salgsverdien til finans der du kan se resultatet.</span><span class="sxs-lookup"><span data-stu-id="84a93-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="84a93-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="84a93-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="84a93-124">Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.</span><span class="sxs-lookup"><span data-stu-id="84a93-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="84a93-125">Velg avskrivningstablået du vil vise poster for, og velg deretter **Poster**.</span><span class="sxs-lookup"><span data-stu-id="84a93-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="84a93-126">Velg en linje med **Salg** i **Bokføringskategori, aktiva**-feltet, og velg deretter **Naviger**.</span><span class="sxs-lookup"><span data-stu-id="84a93-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="84a93-127">I **Naviger**-vinduet velger du finanspostlinjen og deretter **Vis**.</span><span class="sxs-lookup"><span data-stu-id="84a93-127">In the **Navigate** window, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="84a93-128">**Finansposter**-vinduet åpnes der du kan se postene som er resultat av salgsbokføringen.</span><span class="sxs-lookup"><span data-stu-id="84a93-128">The **General Ledger Entries** window opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="84a93-129">Se også</span><span class="sxs-lookup"><span data-stu-id="84a93-129">See Also</span></span>
[<span data-ttu-id="84a93-130">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="84a93-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="84a93-131">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="84a93-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="84a93-132">Finans</span><span class="sxs-lookup"><span data-stu-id="84a93-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="84a93-133">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="84a93-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="84a93-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84a93-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

