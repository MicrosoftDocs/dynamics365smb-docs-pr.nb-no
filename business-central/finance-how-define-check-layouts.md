---
title: Angi oppsettet for en sjekk | Microsoft-dokumentasjon
description: Du kan utforme og skrive ut sjekker i forskjellige formater for å følge standarder.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: eace865bc70f56206d478f8e8d38fd217133925e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "935261"
---
# <a name="define-check-layouts"></a>Definere sjekkoppsett
Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene. Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.

Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.

## <a name="to-define-check-layouts"></a>Definere sjekkoppsett
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportvalg – bankkonto**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - bankkonto**, i **Bruk**-feltet, velger du **Sjekk**.
3. Velg én av følgende rapport-ID-er:

| Rapport-ID | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Sjekk |Dette er standardrapporten. |
| 10401 |Sjekk (blanket/blankett/sjekk) |Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk. |
| 10411 |Sjekk (blanket/sjekk/blankett) |Denne rapporten er utformet for utskrift i formatet sjekk/blankett/sjekk. |

Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra siden **Betalingskladd**. Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fullføre prosesser ved periodens slutt](year-how-complete-period-end-processes.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)
