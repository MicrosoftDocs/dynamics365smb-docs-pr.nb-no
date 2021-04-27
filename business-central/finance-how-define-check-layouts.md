---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 24d046d9284797e371a9cca98ad68618bf248be7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781609"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="53ffe-103">Velg et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="53ffe-103">Select a Check Layout</span></span>
<span data-ttu-id="53ffe-104">Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene.</span><span class="sxs-lookup"><span data-stu-id="53ffe-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="53ffe-105">Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="53ffe-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="53ffe-106">Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.</span><span class="sxs-lookup"><span data-stu-id="53ffe-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="53ffe-107">Slik velger du et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="53ffe-107">To select a check layout</span></span>
1. <span data-ttu-id="53ffe-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="53ffe-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="53ffe-109">På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="53ffe-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="53ffe-110">Velg én av følgende rapport-ID-er:</span><span class="sxs-lookup"><span data-stu-id="53ffe-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="53ffe-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="53ffe-111">Report ID</span></span> | <span data-ttu-id="53ffe-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="53ffe-112">Report Name</span></span> | <span data-ttu-id="53ffe-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="53ffe-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="53ffe-114">1401</span><span class="sxs-lookup"><span data-stu-id="53ffe-114">1401</span></span> |<span data-ttu-id="53ffe-115">Sjekk</span><span class="sxs-lookup"><span data-stu-id="53ffe-115">Check</span></span> |<span data-ttu-id="53ffe-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="53ffe-116">This is the default report.</span></span> |
| <span data-ttu-id="53ffe-117">10411</span><span class="sxs-lookup"><span data-stu-id="53ffe-117">10411</span></span> |<span data-ttu-id="53ffe-118">Sjekk (blanket/blankett/sjekk)</span><span class="sxs-lookup"><span data-stu-id="53ffe-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="53ffe-119">Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="53ffe-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="53ffe-120">10412</span><span class="sxs-lookup"><span data-stu-id="53ffe-120">10412</span></span> |<span data-ttu-id="53ffe-121">Sjekk (blanket/sjekk/blankett)</span><span class="sxs-lookup"><span data-stu-id="53ffe-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="53ffe-122">Denne rapporten er utformet for utskrift i formatet blankett/sjekk/blankett.</span><span class="sxs-lookup"><span data-stu-id="53ffe-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="53ffe-123">10413</span><span class="sxs-lookup"><span data-stu-id="53ffe-123">10413</span></span> |<span data-ttu-id="53ffe-124">Tre sjekker side</span><span class="sxs-lookup"><span data-stu-id="53ffe-124">Three Checks per Page</span></span> |<span data-ttu-id="53ffe-125">Denne rapporten er utformet for å skrive ut tre sjekker på hver side.</span><span class="sxs-lookup"><span data-stu-id="53ffe-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="53ffe-126">Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="53ffe-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="53ffe-127">Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="53ffe-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="53ffe-128">Hvis du vil endre en av disse standardsjekkoppsettene, bruker du Word- eller RDLC-integrasjonen til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="53ffe-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="53ffe-129">Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="53ffe-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="53ffe-130">Bruke MICR-og sikkerhetsskrifter</span><span class="sxs-lookup"><span data-stu-id="53ffe-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="53ffe-131">Den elektroniske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] inneholder forhåndsinstallerte skrifter på serverne som kan brukes til å definere sjekkoppsett.</span><span class="sxs-lookup"><span data-stu-id="53ffe-131">The online version of [!INCLUDE[prod_short](includes/prod_short.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="53ffe-132">Følgende beskriver hvilke skrifter som er tilgjengelige, og som inneholder koblinger til detaljert informasjon om tredjeparts leverandørene av skriftene.</span><span class="sxs-lookup"><span data-stu-id="53ffe-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="53ffe-133">MICR og sjekk sikkerhet-skrifter i Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] er lisensiert i en skriftpakke fra IDAutomation.com, Inc. Disse produktene kan bare brukes som en del av og i forbindelse med Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="53ffe-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="53ffe-134">I oppdatering 15.3 og nyere kan MICR-skrifter installeres og være tilgjengelige for bruk.</span><span class="sxs-lookup"><span data-stu-id="53ffe-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="53ffe-135">Både E-13B- og de CMC-7-standardene støttes.</span><span class="sxs-lookup"><span data-stu-id="53ffe-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="53ffe-136">I tillegg til MICR-skrifter er spesielle sikkerhetsskrifter tilgjengelige for å generere tekst, navn, beløp og valutasymbolene dollar, euro, pund og yen, som kan være vanskelige å endre når en sjekk er skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="53ffe-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="53ffe-137">Av sikkerhetsgrunner og rettslige grunner kan du ikke laste opp egendefinerte skrifter til [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet.</span><span class="sxs-lookup"><span data-stu-id="53ffe-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[prod_short](includes/prod_short.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="53ffe-138">MICR E-13B-spesifikasjoner</span><span class="sxs-lookup"><span data-stu-id="53ffe-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="53ffe-139">Følgende summerer spesifikasjoner for MICR E-13B-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="53ffe-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="53ffe-140">![MICR E-13B-spesifikasjoner](media/font_MICR_E-13B_Specifications.png "MICR E-13B-spesifikasjoner")</span><span class="sxs-lookup"><span data-stu-id="53ffe-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="53ffe-141">Skilletegn</span><span class="sxs-lookup"><span data-stu-id="53ffe-141">Delimiter characters</span></span>
<span data-ttu-id="53ffe-142">![Skilletegn](media/font-micr-letters.png "Skilletegn")</span><span class="sxs-lookup"><span data-stu-id="53ffe-142">![Delimiter characters](media/font-micr-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="53ffe-143">Den fullstendige spesifikasjonen av MICR E-13B-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="53ffe-143">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="53ffe-144">MICR CMC-7-spesifikasjoner</span><span class="sxs-lookup"><span data-stu-id="53ffe-144">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="53ffe-145">Følgende CMC-7-skrifter er tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)] online:</span><span class="sxs-lookup"><span data-stu-id="53ffe-145">The following CMC-7 fonts are available in [!INCLUDE[prod_short](includes/prod_short.md)] online:</span></span>

- <span data-ttu-id="53ffe-146">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="53ffe-146">IDAutomationCMC7</span></span>
- <span data-ttu-id="53ffe-147">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="53ffe-147">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="53ffe-148">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="53ffe-148">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="53ffe-149">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="53ffe-149">IDAutomationCMC7n40</span></span>

<span data-ttu-id="53ffe-150">Følgende summerer spesifikasjoner for MICR CMC-7-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="53ffe-150">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="53ffe-151">![MICR CMC-7-spesifikasjoner](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-spesifikasjoner")</span><span class="sxs-lookup"><span data-stu-id="53ffe-151">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="53ffe-152">Skilletegn</span><span class="sxs-lookup"><span data-stu-id="53ffe-152">Delimiter characters</span></span>
<span data-ttu-id="53ffe-153">![Skilletegn](media/font-cmc7-letters.png "Skilletegn")</span><span class="sxs-lookup"><span data-stu-id="53ffe-153">![Delimiter characters](media/font-cmc7-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="53ffe-154">Den fullstendige spesifikasjonen av MICR CMC-7-skrifter finnes i dokumentasjonen for leverandøren her: (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="53ffe-154">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="53ffe-155">Spesifikasjoner for sikre skrifter</span><span class="sxs-lookup"><span data-stu-id="53ffe-155">Secure Font Specifications</span></span>
<span data-ttu-id="53ffe-156">Følgende summerer spesifikasjoner for sjekk sikkerhet-skrifter som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="53ffe-156">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="53ffe-157">![Spesifikasjoner for sjekk sikkerhet-skrift](media/font_check-security-font_Specifications.png "Spesifikasjoner for sjekk sikkerhet-skrift")</span><span class="sxs-lookup"><span data-stu-id="53ffe-157">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="53ffe-158">Den fullstendige spesifikasjonen av sjekk sikkerhet-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="53ffe-158">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="53ffe-159">Skrifter for andre formål er også tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="53ffe-159">Fonts for other purposes are also available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="53ffe-160">Hvis du vil ha mer informasjon, kan du se [Tilgjengelige skrifter](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="53ffe-160">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="53ffe-161">Se også</span><span class="sxs-lookup"><span data-stu-id="53ffe-161">See Also</span></span>
[<span data-ttu-id="53ffe-162">Opprette og endre et egendefinert rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="53ffe-162">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="53ffe-163">Skrifter i Business Central</span><span class="sxs-lookup"><span data-stu-id="53ffe-163">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="53ffe-164">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="53ffe-164">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="53ffe-165">[Avstemme bankkonter](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="53ffe-165">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="53ffe-166">Fullføre prosesser ved periodens slutt</span><span class="sxs-lookup"><span data-stu-id="53ffe-166">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="53ffe-167">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="53ffe-167">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="53ffe-168">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="53ffe-168">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]