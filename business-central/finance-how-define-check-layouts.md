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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: fea52bfa75d953b96aecc0f3e354806324f77d83
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306319"
---
# <a name="select-a-check-layout"></a>Velg et sjekkoppsett
Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene. Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.

Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.

## <a name="to-select-a-check-layout"></a>Slik velger du et sjekkoppsett
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.
3. Velg én av følgende rapport-ID-er:

| Rapport-ID | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Sjekk |Dette er standardrapporten. |
| 10411 |Sjekk (blanket/blankett/sjekk) |Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk. |
| 10412 |Sjekk (blanket/sjekk/blankett) |Denne rapporten er utformet for utskrift i formatet blankett/sjekk/blankett. |
| 10413 |Tre sjekker side |Denne rapporten er utformet for å skrive ut tre sjekker på hver side. |

Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**. Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).

Hvis du vil endre en av disse standardsjekkoppsettene, bruker du Word- eller RDLC-integrasjonen til å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett eller dokumentoppsett](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Opprette og endre et egendefinert rapportoppsett eller dokumentoppsett](ui-how-create-custom-report-layout.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fullføre prosesser ved periodens slutt](year-how-complete-period-end-processes.md)  
[Arbeide med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)
