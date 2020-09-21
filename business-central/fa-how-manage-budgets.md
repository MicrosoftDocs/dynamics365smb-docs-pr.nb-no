---
title: Administrere aktivabudsjetter | Microsoft-dokumentasjon
description: Du kan definere informasjon om fremtidige investeringer, salg og avskrivning av aktiva for å bidra til å klargjøre budsjetter og prognoser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5baf1342dc019233529386d43a28159adfc08af6
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780313"
---
# <a name="manage-budgets-for-fixed-assets"></a><span data-ttu-id="e744d-103">Behandle budsjetter for aktiva</span><span class="sxs-lookup"><span data-stu-id="e744d-103">Manage Budgets for Fixed Assets</span></span>
<span data-ttu-id="e744d-104">Du kan definere budsjetterte aktiva.</span><span class="sxs-lookup"><span data-stu-id="e744d-104">You can set up budgeted fixed assets.</span></span> <span data-ttu-id="e744d-105">Dette gjør det for eksempel mulig å ta med forventede anskaffelser og salg i rapporter.</span><span class="sxs-lookup"><span data-stu-id="e744d-105">For example, this lets you include anticipated acquisitions and sales in reports.</span></span>  

<span data-ttu-id="e744d-106">Når du skal forberede et budsjettert resultatregnskap, balansebudsjett og likviditetsbudsjett, må du ha opplysninger om fremtidige investeringer, salg og aktivaavskrivninger.</span><span class="sxs-lookup"><span data-stu-id="e744d-106">To prepare your budgeted income statement, budgeted balance sheet, and cash budget, you need information about future investments, disposals and depreciation of fixed assets.</span></span> <span data-ttu-id="e744d-107">Du finner disse opplysningene i rapporten **Aktiva - forventet verdi**.</span><span class="sxs-lookup"><span data-stu-id="e744d-107">You can get this information from the **Fixed Asset - Projected Value** report.</span></span> <span data-ttu-id="e744d-108">Før du skriver ut denne rapporten, må du forberede budsjettet.</span><span class="sxs-lookup"><span data-stu-id="e744d-108">Before you print this report, you must prepare the budget.</span></span>  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a><span data-ttu-id="e744d-109">Slik budsjetterer du anskaffelseskost for et aktiva:</span><span class="sxs-lookup"><span data-stu-id="e744d-109">To budget the acquisition cost of a fixed asset</span></span>
<span data-ttu-id="e744d-110">Når du skal forberede et budsjett, må du definere aktivakort for aktiva som du vil kjøpe senere.</span><span class="sxs-lookup"><span data-stu-id="e744d-110">To prepare a budget, you have to set up fixed asset cards for fixed assets that you intend to buy in the future.</span></span> <span data-ttu-id="e744d-111">De budsjetterte aktivaene er definert som vanlige aktiva, men må være konfigurert slik at de ikke bokføres i Finans.</span><span class="sxs-lookup"><span data-stu-id="e744d-111">The budget fixed assets are set up as ordinary fixed assets, but it must be set up to not post to the general ledger.</span></span>

<span data-ttu-id="e744d-112">Når du bokfører anskaffelseskosten, angir du nummeret for det budsjetterte aktivaet i feltet **Budsjettert aktivanr.**</span><span class="sxs-lookup"><span data-stu-id="e744d-112">When you post the acquisition cost, you enter the number of the budgeted fixed asset in the **Budgeted FA No.** field.</span></span> <span data-ttu-id="e744d-113">Dermed bokføres en anskaffelseskost med motsatt fortegn for det budsjetterte aktivaet.</span><span class="sxs-lookup"><span data-stu-id="e744d-113">This will post an acquisition cost with an opposite sign for the budgeted asset.</span></span> <span data-ttu-id="e744d-114">Dette betyr at den totale anskaffelseskosten for det budsjetterte aktivaet er differansen mellom den budsjetterte og den faktiske anskaffelseskosten.</span><span class="sxs-lookup"><span data-stu-id="e744d-114">This means that the total acquisition cost on the budgeted asset is the difference between the budgeted and the actual acquisition cost.</span></span>

1. <span data-ttu-id="e744d-115">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e744d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="e744d-116">Velg **Ny** for å opprette et nytt aktivakort for det budsjetterte aktivaet.</span><span class="sxs-lookup"><span data-stu-id="e744d-116">Choose the **New** action to create a new fixed asset card for the budgeted fixed asset.</span></span>
3. <span data-ttu-id="e744d-117">Merk av for **Budsjettert aktiva** for å hindre bokføring til finans.</span><span class="sxs-lookup"><span data-stu-id="e744d-117">Select the **Budgeted Asset** check box to prevent posting to the general ledger.</span></span>
4. <span data-ttu-id="e744d-118">Fyll ut resten av feltene, tilordne et avskrivningstablå, og bokfør deretter den første anskaffelseskosten med det budsjetterte aktivaet som er angitt i feltet **Budsjettert aktivanr.** på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="e744d-118">Fill in the remaining fields, assign a depreciation book, and then post the first acquisition cost with the budgeted fixed asset entered in the **Budgeted FA No.** field on the journal line.</span></span> <span data-ttu-id="e744d-119">Hvis du vil ha mer informasjon, kan du se [Anskaffe aktiva](fa-how-acquire.md).</span><span class="sxs-lookup"><span data-stu-id="e744d-119">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a><span data-ttu-id="e744d-120">Slik budsjetterer du salget av et aktiva:</span><span class="sxs-lookup"><span data-stu-id="e744d-120">To budget the disposal of a fixed asset</span></span>
<span data-ttu-id="e744d-121">Hvis du planlegger å selge aktiva i budsjettperioden, kan du angi opplysninger om salgsprisen og salgsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e744d-121">If you plan to sell assets within the budget period, you can enter information about sales price and sales date.</span></span>

1. <span data-ttu-id="e744d-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e744d-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="e744d-123">Velg aktivaet som skal avhendes, og velg deretter **Avskrivningstablåer**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="e744d-123">Select the fixed asset to be disposed of, and then choose the **Depreciation Books** action.</span></span>
3. <span data-ttu-id="e744d-124">Fyll ut feltene **Forventet salgsdato** og **Forventet gevinst ved salg** på siden **Aktivaavskrivningstablå**.</span><span class="sxs-lookup"><span data-stu-id="e744d-124">On the **FA Depreciation Books** page, fill in the **Projected Disposal Date** and **Projected Proceeds on Disposal** fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a><span data-ttu-id="e744d-125">Slik viser du forventede salgsverdier</span><span class="sxs-lookup"><span data-stu-id="e744d-125">To view projected disposal values</span></span>
<span data-ttu-id="e744d-126">Hvis du vil se de forventede salgsverdiene og beregne tap og vinning, kan du bruke rapporten **Aktiva - forventet verdi**.</span><span class="sxs-lookup"><span data-stu-id="e744d-126">To see the projected disposal values and have the gain and loss calculated, you can use the **FA Projected Value** report.</span></span>

1. <span data-ttu-id="e744d-127">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva – forventet verdi**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e744d-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="e744d-128">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e744d-128">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e744d-129">Velg knappen **Skriv ut** eller **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="e744d-129">Choose the **Print** or **Preview** button.</span></span>

## <a name="to-budget-depreciation"></a><span data-ttu-id="e744d-130">Slik budsjetterer du avskrivninger</span><span class="sxs-lookup"><span data-stu-id="e744d-130">To budget depreciation</span></span>
<span data-ttu-id="e744d-131">Du kan bruke rapporten **Aktiva - forventet verdi** til å beregne fremtidig avskrivning.</span><span class="sxs-lookup"><span data-stu-id="e744d-131">You can use the **Fixed Asset - Projected Value** report to calculate future depreciation.</span></span> <span data-ttu-id="e744d-132">Rapporten viser den bokførte verdien og den akkumulerte avskrivningen ved begynnelsen og slutten av den valgte perioden, samt endringer i perioden.</span><span class="sxs-lookup"><span data-stu-id="e744d-132">The report shows the book value and accumulated depreciation at the start of the selected period, changes during the period, and the book value and accumulated depreciation at the end of the selected period.</span></span>

1. <span data-ttu-id="e744d-133">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva – forventet verdi**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e744d-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset Projected Value**, and then choose the related link.</span></span>
2. <span data-ttu-id="e744d-134">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="e744d-134">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="e744d-135">Hvis du vil se de samlede verdiene for alle aktiva, fjerner du avmerkingen for **Skriv ut per aktiva**.</span><span class="sxs-lookup"><span data-stu-id="e744d-135">To see total values for all assets, clear the **Print per Fixed Asset** check box.</span></span>
4. <span data-ttu-id="e744d-136">La hurtigfanen **Aktiva** stå tom hvis du vil ha med alle aktivaene.</span><span class="sxs-lookup"><span data-stu-id="e744d-136">Leave the **Fixed Asset** FastTab blank to have all assets included.</span></span> <span data-ttu-id="e744d-137">I feltet **Budsjettert aktiva** angir du **Nei** hvis du ikke vil ha med budsjetterte aktiva, eller **Ja** hvis du bare vil se på de budsjetterte aktivaene.</span><span class="sxs-lookup"><span data-stu-id="e744d-137">In the **Budgeted Asset** field, enter **No** to exclude budgeted assets or **Yes** to see budgeted assets only.</span></span>
5. <span data-ttu-id="e744d-138">Velg knappen **Skriv ut** eller **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="e744d-138">Choose the **Print** or **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="e744d-139">Se også</span><span class="sxs-lookup"><span data-stu-id="e744d-139">See Also</span></span>
[<span data-ttu-id="e744d-140">Anleggsmidler</span><span class="sxs-lookup"><span data-stu-id="e744d-140">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="e744d-141">Definere aktiva</span><span class="sxs-lookup"><span data-stu-id="e744d-141">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="e744d-142">Finans</span><span class="sxs-lookup"><span data-stu-id="e744d-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="e744d-143">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="e744d-143">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="e744d-144">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e744d-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
