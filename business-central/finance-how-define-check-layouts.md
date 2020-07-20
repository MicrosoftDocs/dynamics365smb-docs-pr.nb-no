---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 8346e8a868f73d3de729a56e86530048c58229aa
ms.sourcegitcommit: 3945f16d6d9c9853651e6291ce1465a44fd71fc8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2020
ms.locfileid: "3458928"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="ce140-103">Velg et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="ce140-103">Select a Check Layout</span></span>
<span data-ttu-id="ce140-104">Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene.</span><span class="sxs-lookup"><span data-stu-id="ce140-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="ce140-105">Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="ce140-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="ce140-106">Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.</span><span class="sxs-lookup"><span data-stu-id="ce140-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="ce140-107">Slik velger du et sjekkoppsett</span><span class="sxs-lookup"><span data-stu-id="ce140-107">To select a check layout</span></span>
1. <span data-ttu-id="ce140-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ce140-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="ce140-109">På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="ce140-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="ce140-110">Velg én av følgende rapport-ID-er:</span><span class="sxs-lookup"><span data-stu-id="ce140-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="ce140-111">Rapport-ID</span><span class="sxs-lookup"><span data-stu-id="ce140-111">Report ID</span></span> | <span data-ttu-id="ce140-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="ce140-112">Report Name</span></span> | <span data-ttu-id="ce140-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ce140-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ce140-114">1401</span><span class="sxs-lookup"><span data-stu-id="ce140-114">1401</span></span> |<span data-ttu-id="ce140-115">Sjekk</span><span class="sxs-lookup"><span data-stu-id="ce140-115">Check</span></span> |<span data-ttu-id="ce140-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="ce140-116">This is the default report.</span></span> |
| <span data-ttu-id="ce140-117">10411</span><span class="sxs-lookup"><span data-stu-id="ce140-117">10411</span></span> |<span data-ttu-id="ce140-118">Sjekk (blanket/blankett/sjekk)</span><span class="sxs-lookup"><span data-stu-id="ce140-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="ce140-119">Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk.</span><span class="sxs-lookup"><span data-stu-id="ce140-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="ce140-120">10412</span><span class="sxs-lookup"><span data-stu-id="ce140-120">10412</span></span> |<span data-ttu-id="ce140-121">Sjekk (blanket/sjekk/blankett)</span><span class="sxs-lookup"><span data-stu-id="ce140-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="ce140-122">Denne rapporten er utformet for utskrift i formatet blankett/sjekk/blankett.</span><span class="sxs-lookup"><span data-stu-id="ce140-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="ce140-123">10413</span><span class="sxs-lookup"><span data-stu-id="ce140-123">10413</span></span> |<span data-ttu-id="ce140-124">Tre sjekker side</span><span class="sxs-lookup"><span data-stu-id="ce140-124">Three Checks per Page</span></span> |<span data-ttu-id="ce140-125">Denne rapporten er utformet for å skrive ut tre sjekker på hver side.</span><span class="sxs-lookup"><span data-stu-id="ce140-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="ce140-126">Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="ce140-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="ce140-127">Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="ce140-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="ce140-128">Hvis du vil endre en av disse standardsjekkoppsettene, bruker du Word- eller RDLC-integrasjonen til å gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="ce140-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="ce140-129">Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="ce140-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="ce140-130">Bruke MICR-og sikkerhetsskrifter</span><span class="sxs-lookup"><span data-stu-id="ce140-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="ce140-131">Den elektroniske versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder forhåndsinstallerte skrifter på serverne som kan brukes til å definere sjekkoppsett.</span><span class="sxs-lookup"><span data-stu-id="ce140-131">The online version of [!INCLUDE[d365fin](includes/d365fin_md.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="ce140-132">Følgende beskriver hvilke skrifter som er tilgjengelige, og som inneholder koblinger til detaljert informasjon om tredjeparts leverandørene av skriftene.</span><span class="sxs-lookup"><span data-stu-id="ce140-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="ce140-133">MICR og sjekk sikkerhet-skrifter i Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] er lisensiert i en skriftpakke fra IDAutomation.com, Inc. Disse produktene kan bare brukes som en del av og i forbindelse med Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ce140-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="ce140-134">I oppdatering 15.3 og nyere kan MICR-skrifter installeres og være tilgjengelige for bruk.</span><span class="sxs-lookup"><span data-stu-id="ce140-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="ce140-135">Både E-13B- og de CMC-7-standardene støttes.</span><span class="sxs-lookup"><span data-stu-id="ce140-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="ce140-136">I tillegg til MICR-skrifter er spesielle sikkerhetsskrifter tilgjengelige for å generere tekst, navn, beløp og valutasymbolene dollar, euro, pund og yen, som kan være vanskelige å endre når en sjekk er skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="ce140-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="ce140-137">Av sikkerhetsgrunner og rettslige grunner kan du ikke laste opp egendefinerte skrifter til [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ce140-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[d365fin](includes/d365fin_md.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="ce140-138">MICR E-13B-spesifikasjoner</span><span class="sxs-lookup"><span data-stu-id="ce140-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="ce140-139">Følgende summerer spesifikasjoner for MICR E-13B-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="ce140-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="ce140-140">![MICR E-13B-spesifikasjoner](media/font_MICR_E-13B_Specifications.png "MICR E-13B-spesifikasjoner")</span><span class="sxs-lookup"><span data-stu-id="ce140-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="ce140-141">Skilletegn</span><span class="sxs-lookup"><span data-stu-id="ce140-141">Delimiter characters</span></span>
<span data-ttu-id="ce140-142">![Skilletegn](media/font-micr-letters.png "Skilletegn")</span><span class="sxs-lookup"><span data-stu-id="ce140-142">![Delimiter characters](media/font-micr-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="ce140-143">Den fullstendige spesifikasjonen av MICR E-13B-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="ce140-143">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="ce140-144">MICR CMC-7-spesifikasjoner</span><span class="sxs-lookup"><span data-stu-id="ce140-144">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="ce140-145">Følgende CMC-7-skrifter er tilgjengelige i [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span><span class="sxs-lookup"><span data-stu-id="ce140-145">The following CMC-7 fonts are available in [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span></span>

- <span data-ttu-id="ce140-146">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="ce140-146">IDAutomationCMC7</span></span>
- <span data-ttu-id="ce140-147">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="ce140-147">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="ce140-148">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="ce140-148">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="ce140-149">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="ce140-149">IDAutomationCMC7n40</span></span>

<span data-ttu-id="ce140-150">Følgende summerer spesifikasjoner for MICR CMC-7-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="ce140-150">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="ce140-151">![MICR CMC-7-spesifikasjoner](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-spesifikasjoner")</span><span class="sxs-lookup"><span data-stu-id="ce140-151">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

### <a name="delimiter-characters"></a><span data-ttu-id="ce140-152">Skilletegn</span><span class="sxs-lookup"><span data-stu-id="ce140-152">Delimiter characters</span></span>
<span data-ttu-id="ce140-153">![Skilletegn](media/font-cmc7-letters.png "Skilletegn")</span><span class="sxs-lookup"><span data-stu-id="ce140-153">![Delimiter characters](media/font-cmc7-letters.png "Delimiter characters")</span></span>

<span data-ttu-id="ce140-154">Den fullstendige spesifikasjonen av MICR CMC-7-skrifter finnes i dokumentasjonen for leverandøren her: (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="ce140-154">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="ce140-155">Spesifikasjoner for sikre skrifter</span><span class="sxs-lookup"><span data-stu-id="ce140-155">Secure Font Specifications</span></span>
<span data-ttu-id="ce140-156">Følgende summerer spesifikasjoner for sjekk sikkerhet-skrifter som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.</span><span class="sxs-lookup"><span data-stu-id="ce140-156">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="ce140-157">![Spesifikasjoner for sjekk sikkerhet-skrift](media/font_check-security-font_Specifications.png "Spesifikasjoner for sjekk sikkerhet-skrift")</span><span class="sxs-lookup"><span data-stu-id="ce140-157">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="ce140-158">Den fullstendige spesifikasjonen av sjekk sikkerhet-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="ce140-158">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="ce140-159">Skrifter for andre formål er også tilgjengelige i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ce140-159">Fonts for other purposes are also available in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="ce140-160">Hvis du vil ha mer informasjon, kan du se [Tilgjengelige skrifter](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="ce140-160">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="ce140-161">Se også</span><span class="sxs-lookup"><span data-stu-id="ce140-161">See Also</span></span>
[<span data-ttu-id="ce140-162">Opprette og endre et egendefinert rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="ce140-162">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="ce140-163">Skrifter i Business Central</span><span class="sxs-lookup"><span data-stu-id="ce140-163">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="ce140-164">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="ce140-164">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="ce140-165">[Avstemme bankkonter](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ce140-165">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="ce140-166">Fullføre prosesser ved periodens slutt</span><span class="sxs-lookup"><span data-stu-id="ce140-166">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="ce140-167">[Arbeide med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce140-167">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ce140-168">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ce140-168">General Business Functionality</span></span>](ui-across-business-areas.md)
