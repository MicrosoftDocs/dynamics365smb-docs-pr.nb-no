---
title: Definere fakturaavrunding | Microsoft-dokumentasjon
description: Du kan runde av fakturabeløp når du oppretter fakturaer. I tillegg kan lokale forskrifter eller lokale regler kreve at fakturaen rundes av på en bestemt måte, for eksempel til et beløp som kan deles på 0,05.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: bb114e6ea550ca5cc453c8319e72da5b11cec6e8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882473"
---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="9a3ac-104">Definere fakturaavrunding</span><span class="sxs-lookup"><span data-stu-id="9a3ac-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="9a3ac-105">Hvis du må runde av fakturabeløp når du oppretter fakturaer, kan du bruke funksjonen for automatisk avrunding.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="9a3ac-106">Når en faktura rundes av, legges det til en ekstra linje med avrundingsbeløpet, og denne linjen bokføres sammen med de andre fakturalinjene.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="9a3ac-107">Lokale forskrifter eller lokale regler kan kreve at fakturaen rundes av på en bestemt måte, for eksempel til et beløp som kan deles på 0,05.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  

<span data-ttu-id="9a3ac-108">Hvis du vil bruke automatisk fakturaavrunding, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="9a3ac-108">To use automatic invoice rounding, you must:</span></span>  

* <span data-ttu-id="9a3ac-109">Angi finanskontiene der avrundingsdifferanser skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="9a3ac-110">Definere regler for avrunding av fakturaer i lokal valuta og utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="9a3ac-111">Aktivere funksjonen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-111">Activate the function.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9a3ac-112">I tillegg til funksjonene for fakturaavrunding kan beløp på fakturaer rundes av med prisavrundingsfunksjonen og beløpsavrundingsfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="9a3ac-113">Definere finanskonti i for avrundingsdifferanser på fakturaer</span><span class="sxs-lookup"><span data-stu-id="9a3ac-113">Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="9a3ac-114">Hvis du vil bruke funksjonen for automatisk fakturaavrunding, må du opprette finanskontoen(e) der avrundingsdifferansen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="9a3ac-115">Før du kan gjøre dette, må du opprette mva-bokføringsgrupper for varer.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="9a3ac-116">Hvis du vil ha mer informasjon, kan du se [Konfigurere mva](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="9a3ac-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="9a3ac-117">Slik setter du opp finanskonti for avrundingsdifferanser på fakturaer</span><span class="sxs-lookup"><span data-stu-id="9a3ac-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="9a3ac-118">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a3ac-119">Sett opp kontoen på siden **Kontoplan**, og gi den navnet **Fakturaavrunding** eller noe lignende.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="9a3ac-120">bruker kontonavnet som tekst for fakturaer som er avrundet.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-120">will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="9a3ac-121">Avhengig av om du bruker mva eller salgsmva, i feltene **Mva-bokføringsgruppe - vare** eller **Mva-bokf.gruppe - vare** velger du en bokføringsgruppe for avrundede beløp.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="9a3ac-122">Du kan også definere en ny gruppekode som skal brukes til fakturaavrunding.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="9a3ac-123">La feltet **Bokføringstype** og ett av feltene **Mva-bokføringsgruppe - firma** eller **Mva-bokf.gruppe - firma** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

<span data-ttu-id="9a3ac-124">Du kan nå tilordne fakturaavrundingskontoen til bokføringsgrupper på siden **Bokføringsgrupper - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="9a3ac-125">Definere avrunding for fremmed og lokal valuta</span><span class="sxs-lookup"><span data-stu-id="9a3ac-125">Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="9a3ac-126">Før du kan bruke funksjonen for automatisk fakturaavrunding for fakturaer, må du definere avrundingsregler for fremmed og lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="9a3ac-127">Slik oppretter du avrundingsregler for fremmed valuta</span><span class="sxs-lookup"><span data-stu-id="9a3ac-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="9a3ac-128">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a3ac-129">På **Valutaer**-siden velger du den fremmede valutaen for å åpne **valutakortet**, og deretter fyller du ut feltet **Avrundingspresisjon, beløp**, **Avrundingspresisjon, pris**, **Avrundingspresisjon, faktura** og **Fakturaavrundingstype**.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>

### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="9a3ac-130">Slik oppretter du avrunding for den lokale valutaen</span><span class="sxs-lookup"><span data-stu-id="9a3ac-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="9a3ac-131">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finansoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a3ac-132">På siden **Finansoppsett** på hurtigfanen **Generelt** fyller du ut feltene **Avrund.presisjon faktura** og **Fakturaavrundingstype**.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="activate-the-invoice-rounding-function"></a><span data-ttu-id="9a3ac-133">Aktivere funksjonen for fakturaavrunding</span><span class="sxs-lookup"><span data-stu-id="9a3ac-133">Activate the invoice rounding function</span></span>  
<span data-ttu-id="9a3ac-134">For å sørge for at salgs- og kjøpsfakturaer avrundes automatisk, må du aktivere fakturaavrundingsfunksjonen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="9a3ac-135">Du aktiverer fakturaavrunding separat for salgs- og kjøpsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="9a3ac-136">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett** eller **Kjøpsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="9a3ac-137">På hurtigfanen **Generelt** velger du **Fakturaavrunding**.</span><span class="sxs-lookup"><span data-stu-id="9a3ac-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9a3ac-138">Se også</span><span class="sxs-lookup"><span data-stu-id="9a3ac-138">See Also</span></span>  
[<span data-ttu-id="9a3ac-139">Fakturere salg</span><span class="sxs-lookup"><span data-stu-id="9a3ac-139">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="9a3ac-140">Registrere kjøp</span><span class="sxs-lookup"><span data-stu-id="9a3ac-140">Record Purchases</span></span>](purchasing-how-record-purchases.md)
