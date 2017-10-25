---
title: Administrere aktivabudsjetter | Microsoft-dokumentasjon
description: "Du kan definere informasjon om fremtidige investeringer, salg og avskrivning av aktiva for å bidra til å klargjøre budsjetter og prognoser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2185a1fc40ddae772e20994f6531b02d7e703e17
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-budgets-for-fixed-assets"></a><span data-ttu-id="107bc-103">Behandle budsjetter for aktiva</span><span class="sxs-lookup"><span data-stu-id="107bc-103">How to: Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="107bc-104">Du kan definere budsjetterte aktiva.</span><span class="sxs-lookup"><span data-stu-id="107bc-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="107bc-105">Dette gjør det for eksempel mulig å ta med forventede anskaffelser og salg i rapporter.</span><span class="sxs-lookup"><span data-stu-id="107bc-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="107bc-106">Når du skal forberede et budsjettert resultatregnskap, balansebudsjett og likviditetsbudsjett, må du ha opplysninger om fremtidige investeringer, salg og aktivaavskrivninger.</span><span class="sxs-lookup"><span data-stu-id="107bc-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="107bc-107">Du finner disse opplysningene i rapporten **Aktiva - forventet verdi**.</span><span class="sxs-lookup"><span data-stu-id="107bc-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="107bc-108">Før du skriver ut denne rapporten, må du forberede budsjettet.</span><span class="sxs-lookup"><span data-stu-id="107bc-108">Before you print this report, you must prepare the budget.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="107bc-109">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="107bc-109">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="107bc-110">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="107bc-110">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="107bc-111">Slik budsjetterer du anskaffelseskost for et aktiva:</span><span class="sxs-lookup"><span data-stu-id="107bc-111">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="107bc-112">Når du skal forberede et budsjett, må du definere aktivakort for aktiva som du vil kjøpe senere.</span><span class="sxs-lookup"><span data-stu-id="107bc-112">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="107bc-113">De budsjetterte aktivaene er definert som vanlige aktiva, men må være konfigurert slik at de ikke bokføres i Finans.</span><span class="sxs-lookup"><span data-stu-id="107bc-113">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="107bc-114">Når du bokfører anskaffelseskosten, angir du nummeret for det budsjetterte aktivaet i feltet **Budsjettert aktivanr.**</span><span class="sxs-lookup"><span data-stu-id="107bc-114">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="107bc-115">Dermed bokføres en anskaffelseskost med motsatt fortegn for det budsjetterte aktivaet.</span><span class="sxs-lookup"><span data-stu-id="107bc-115">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="107bc-116">Dette betyr at den totale anskaffelseskosten for det budsjetterte aktivaet er differansen mellom den budsjetterte og den faktiske anskaffelseskosten.</span><span class="sxs-lookup"><span data-stu-id="107bc-116">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="107bc-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="107bc-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="107bc-118">Velg **Ny** for å opprette et nytt aktivakort for det budsjetterte aktivaet.</span><span class="sxs-lookup"><span data-stu-id="107bc-118">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="107bc-119">Merk av for **Budsjettert aktiva** for å hindre bokføring til finans.</span><span class="sxs-lookup"><span data-stu-id="107bc-119">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="107bc-120">Fyll ut resten av feltene, tilordne et avskrivningstablå, og bokfør deretter den første anskaffelseskosten med det budsjetterte aktivaet som er angitt i feltet **Budsjettert aktivanr.** på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="107bc-120">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="107bc-121">Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="107bc-121">For more information, see [How to: Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="107bc-122">Slik budsjetterer du salget av et aktiva:</span><span class="sxs-lookup"><span data-stu-id="107bc-122">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="107bc-123">Hvis du planlegger å selge aktiva i budsjettperioden, kan du angi opplysninger om salgsprisen og salgsdatoen.</span><span class="sxs-lookup"><span data-stu-id="107bc-123">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="107bc-124">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="107bc-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="107bc-125">Velg aktivaet som skal avhendes, og velg deretter **Avskrivningstablåer**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="107bc-125">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="107bc-126">Fyll ut feltene **Forventet salgsdato** og **Forventet gevinst ved salg** i vinduet **Aktivaavskrivningstablå**.</span><span class="sxs-lookup"><span data-stu-id="107bc-126">In the **FA Depreciation Books** window, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="107bc-127">Slik viser du forventede salgsverdier</span><span class="sxs-lookup"><span data-stu-id="107bc-127">To view projected disposal values</span></span>
<span data-ttu-id="107bc-128">Hvis du vil se de forventede salgsverdiene og beregne tap og vinning, kan du bruke rapporten **Aktiva - forventet verdi**.</span><span class="sxs-lookup"><span data-stu-id="107bc-128">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="107bc-129">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Aktiva - forventet verdi**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="107bc-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="107bc-130">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="107bc-130">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="107bc-131">Velg knappen **Skriv ut** eller **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="107bc-131">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="107bc-132">Slik budsjetterer du avskrivninger</span><span class="sxs-lookup"><span data-stu-id="107bc-132">To budget depreciation</span></span>
<span data-ttu-id="107bc-133">Du kan bruke rapporten **Aktiva - forventet verdi** til å beregne fremtidig avskrivning.</span><span class="sxs-lookup"><span data-stu-id="107bc-133">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="107bc-134">Rapporten viser den bokførte verdien og den akkumulerte avskrivningen ved begynnelsen og slutten av den valgte perioden, samt endringer i perioden.</span><span class="sxs-lookup"><span data-stu-id="107bc-134">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="107bc-135">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Aktiva - forventet verdi**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="107bc-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="107bc-136">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="107bc-136">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="107bc-137">Hvis du vil se de samlede verdiene for alle aktiva, fjerner du avmerkingen for **Skriv ut per aktiva**.</span><span class="sxs-lookup"><span data-stu-id="107bc-137">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="107bc-138">La hurtigfanen **Aktiva** stå tom hvis du vil ha med alle aktivaene.</span><span class="sxs-lookup"><span data-stu-id="107bc-138">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="107bc-139">I feltet **Budsjettert aktiva** angir du **Nei** hvis du ikke vil ha med budsjetterte aktiva, eller **Ja** hvis du bare vil se på de budsjetterte aktivaene.</span><span class="sxs-lookup"><span data-stu-id="107bc-139">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="107bc-140">Velg knappen **Skriv ut** eller **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="107bc-140">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="107bc-141">Se også</span><span class="sxs-lookup"><span data-stu-id="107bc-141">See Also</span></span>
[<span data-ttu-id="107bc-142">Aktiva</span><span class="sxs-lookup"><span data-stu-id="107bc-142">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="107bc-143">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="107bc-143">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="107bc-144">Finans</span><span class="sxs-lookup"><span data-stu-id="107bc-144">Finance</span></span>](finance.md)  
<span data-ttu-id="107bc-145">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="107bc-145">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="107bc-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="107bc-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

