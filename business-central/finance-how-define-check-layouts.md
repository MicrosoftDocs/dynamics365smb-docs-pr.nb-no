---
title: Angi oppsettet for en sjekk
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder angitt av lokale myndigheter.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.search.form: 374, 404
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 7be12b5fe3c6bac93a6ea51454a193ba76320a8e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8149052"
---
# <a name="select-a-check-layout"></a>Velg et sjekkoppsett

Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene. Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.

Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.

## <a name="to-select-a-check-layout"></a>Slik velger du et sjekkoppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.
3. Velg én av følgende rapport-ID-er:

| Rapport-ID | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Sjekk |Dette er standardrapporten. |
| 10411 |Sjekk (blanket/blankett/sjekk) |Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk. |
| 10412 |Sjekk (blanket/sjekk/blankett) |Denne rapporten er utformet for utskrift i formatet blankett/sjekk/blankett. |
| 10413 |Tre sjekker side |Denne rapporten er utformet for å skrive ut tre sjekker på hver side. |

Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**. Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).

Hvis du vil endre en av disse standardsjekkoppsettene, bruker du Word- eller RDLC-integrasjonen til å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="using-micr-and-security-fonts"></a>Bruke MICR-og sikkerhetsskrifter

Den elektroniske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] inneholder forhåndsinstallerte skrifter på serverne som kan brukes til å definere sjekkoppsett. Følgende beskriver hvilke skrifter som er tilgjengelige, og som inneholder koblinger til detaljert informasjon om tredjeparts leverandørene av skriftene.

> [!Important]
> MICR og sjekk sikkerhet-skrifter i Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)] er lisensiert i en skriftpakke fra IDAutomation.com, Inc. Disse produktene kan bare brukes som en del av og i forbindelse med Microsoft Dynamics [!INCLUDE[prod_short](includes/prod_short.md)].

I oppdatering 15.3 og nyere kan MICR-skrifter installeres og være tilgjengelige for bruk. Både E-13B- og de CMC-7-standardene støttes. I tillegg til MICR-skrifter er spesielle sikkerhetsskrifter tilgjengelige for å generere tekst, navn, beløp og valutasymbolene dollar, euro, pund og yen, som kan være vanskelige å endre når en sjekk er skrevet ut.

> [!NOTE]
> Av sikkerhetsgrunner og rettslige grunner kan du ikke laste opp egendefinerte skrifter til [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet.

### <a name="micr-e-13b-specifications"></a>MICR E-13B-spesifikasjoner

Følgende summerer spesifikasjoner for MICR E-13B-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.

![MICR E-13B-spesifikasjoner.](media/font_MICR_E-13B_Specifications.png "MICR E-13B-spesifikasjoner")

### <a name="delimiter-characters"></a>Skilletegn

![Skilletegn.](media/font-micr-letters.png "Skilletegn")

Den fullstendige spesifikasjonen av MICR E-13B-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/micr-fonts/e13b/).

### <a name="micr-cmc-7-specifications"></a>MICR CMC-7-spesifikasjoner

Følgende CMC-7-skrifter er tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Følgende summerer spesifikasjoner for MICR CMC-7-skriftene som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.

![MICR CMC-7-spesifikasjoner.](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-spesifikasjoner")

### <a name="delimiter-characters"></a>Skilletegn

![Skilletegn for CMC-7.](media/font-cmc7-letters.png "Skilletegn for CMC-7")

Den fullstendige spesifikasjonen av MICR CMC-7-skrifter finnes i dokumentasjonen for leverandøren her: (http://www.idautomation.com/micr-fonts/cmc7/).

### <a name="secure-font-specifications"></a>Spesifikasjoner for sikre skrifter

Følgende summerer spesifikasjoner for sjekk sikkerhet-skrifter som kan være nyttige når du kalibrerer skrifter for å være på sjekkoppsett med spesifikke MICR-skrivere.

![Spesifikasjoner for sjekk sikkerhet-skrift.](media/font_check-security-font_Specifications.png "Spesifikasjoner for sjekk sikkerhet-skrift")

Den fullstendige spesifikasjonen av sjekk sikkerhet-skrifter finnes i dokumentasjonen for leverandøren her: (https://www.idautomation.com/security-fonts/).

Skrifter for andre formål er også tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Tilgjengelige skrifter](ui-fonts.md)

## <a name="see-also"></a>Se også

[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Skrifter i Business Central](ui-fonts.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)   
[Fullføre prosesser ved periodens slutt](year-how-complete-period-end-processes.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]