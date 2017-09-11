---
title: GIFI-koder i Canada | Microsoft-dokumentasjon
Description: "I Canada kan du definere GIFI-koder (General Index of Financial Information) og tilordne dem til bokføringskonti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="0e525-103">Arbeide med GIFI-koder i Canada</span><span class="sxs-lookup"><span data-stu-id="0e525-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="0e525-104">Økonomiske informasjonen kan inkludere finanskontoer, rapporter, resultatregnskap, balanse og kontoutdrag for fri egenkapital.</span><span class="sxs-lookup"><span data-stu-id="0e525-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="0e525-105">Økonomisk informasjon klassifiseres ved hjelp av koder.</span><span class="sxs-lookup"><span data-stu-id="0e525-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="0e525-106">Bruken av koder lar myndighetene behandle informasjon, klargjøre for elektronisk lagring og validere mva-informasjon elektronisk.</span><span class="sxs-lookup"><span data-stu-id="0e525-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="0e525-107">Bruken av koder bidrar også til at statistiske organisasjoner kan arbeide mer effektivt. Økonomiske opplysninger er for eksempel lettere tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="0e525-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="0e525-108">Hvis du vil ha mer informasjon, kan du se [nettstedet for CRA](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="0e525-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="0e525-109">CRA bruker GIFI-koder (General Index of Financial Information) til å innhente, validere og behandle elektronisk økonomiske opplysninger og mva-informasjon.</span><span class="sxs-lookup"><span data-stu-id="0e525-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="0e525-110">Anbefalt fremgangsmåte er å tilordne GIFI-koder bare til bokføringskonti, slik at alle summeringer gjøres av din programvare for mva-klargjøring.</span><span class="sxs-lookup"><span data-stu-id="0e525-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="0e525-111">Når en konto tilknyttes en GIFI-kode, rapporteres den til skattemyndighetene under denne koden.</span><span class="sxs-lookup"><span data-stu-id="0e525-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="0e525-112">Flere konti kan alle ha samme GIFI-kode, men hver konto kan ha bare én GIFI-kode.</span><span class="sxs-lookup"><span data-stu-id="0e525-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="0e525-113">Du kan eksportere saldoinformasjon etter GIFI-kode og lagre den eksporterte filen i Excel, noe som er nyttig for overføring av informasjon til din programvare for mva-klargjøring.</span><span class="sxs-lookup"><span data-stu-id="0e525-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="0e525-114">Definere GIFI-koder</span><span class="sxs-lookup"><span data-stu-id="0e525-114">To set up GIFI codes</span></span>
<span data-ttu-id="0e525-115">I Dynamics NAV må du definere GIFI-koder for finanskontoer, rapporter, balanse, resultatregnskap og utdrag for fri egenkapital.</span><span class="sxs-lookup"><span data-stu-id="0e525-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="0e525-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **GIFI-koder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e525-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="0e525-117">I vinduet **GIFI-koder** velger du handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0e525-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="0e525-118">Definer GIFI-koder ved å fylle ut feltene.</span><span class="sxs-lookup"><span data-stu-id="0e525-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="0e525-119">Knytte GIFI-koder til finanskonti</span><span class="sxs-lookup"><span data-stu-id="0e525-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="0e525-120">Hvis du vil rapportere økonomiske opplysninger, må hver GIFI-kode være tilknyttet de aktuelle kontoene i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="0e525-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="0e525-121">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e525-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="0e525-122">Velg en relevant finanskonto, og velg deretter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0e525-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="0e525-123">I hurtigfanen **Kostregnskap**, i **GIFI-kode**-feltet , velger du en passende GIFI-kode.</span><span class="sxs-lookup"><span data-stu-id="0e525-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="0e525-124">Vise kontosaldoer ved hjelp av GIFI-koderapporten</span><span class="sxs-lookup"><span data-stu-id="0e525-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="0e525-125">Du kan se gjennom kontosaldoene etter GIFI-kode ved hjelp av rapporten **Kontosaldoer etter GIFI-koder**.</span><span class="sxs-lookup"><span data-stu-id="0e525-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="0e525-126">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontosaldoer etter GIFI-koder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e525-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="0e525-127">Angi hva du vil inkludere i rapporten ved å fylle ut feltene.</span><span class="sxs-lookup"><span data-stu-id="0e525-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0e525-128">Velg knappen **Skriv ut** eller **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="0e525-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="0e525-129">Eksportere saldoinformasjon ved hjelp av GIFI-koder</span><span class="sxs-lookup"><span data-stu-id="0e525-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="0e525-130">Du kan eksportere saldoinformasjon ved hjelp av GIFI-koder, og lagre den eksporterte filen i Excel.</span><span class="sxs-lookup"><span data-stu-id="0e525-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="0e525-131">Du kan endre, lagre eller slette filen.</span><span class="sxs-lookup"><span data-stu-id="0e525-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="0e525-132">Du kan bruke filen til å overføre informasjon til din programvare for mva-klargjøring.</span><span class="sxs-lookup"><span data-stu-id="0e525-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="0e525-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Eksporter GIFI-informasjon til Excel**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e525-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="0e525-134">Angi hva du vil eksportere til Excel ved å fylle ut feltene.</span><span class="sxs-lookup"><span data-stu-id="0e525-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0e525-135">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e525-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0e525-136">Excel-filen har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="0e525-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="0e525-137">Saldoen er avrundet til nærmeste prosent, men celleverdien beholder den samme prosenten som den gjør i Finans.</span><span class="sxs-lookup"><span data-stu-id="0e525-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="0e525-138">Negative tall representeres som positive tall i hakeparenteser.</span><span class="sxs-lookup"><span data-stu-id="0e525-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="0e525-139">-123 er derfor representert som (123).</span><span class="sxs-lookup"><span data-stu-id="0e525-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="0e525-140">Se også</span><span class="sxs-lookup"><span data-stu-id="0e525-140">See Also</span></span>
<span data-ttu-id="0e525-141">[Finans](finance.md) </span><span class="sxs-lookup"><span data-stu-id="0e525-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="0e525-142">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="0e525-142">Setting Up Finance</span></span>](finance-setup-finance.md)

