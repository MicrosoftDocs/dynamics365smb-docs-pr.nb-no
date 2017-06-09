---
title: Definere sjekkoppsett| Microsoft-dokumentasjon
description: "Lær mer om sjekkoppsettene som er tilgjengelige i Finans."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6081b6d09fa75b868138817442d6df4d9a8d0d7f
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-define-check-layouts"></a>Definere sjekkoppsett
Du kan utforme sjekkene dine slik at de samsvarer med standardene som er angitt av de lokale myndighetene. Sjekkbilder kan skrives ut på engelsk, fransk eller spansk.

Sjekkene er utformet for utskrift i sjekkbildeformatene for USA og Canada i formatet sjekk-blankett-sjekk eller blankett-sjekk-blankett.

## <a name="to-define-check-layouts"></a>Definere sjekkoppsett
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Rapportvalg - bankkonto**, og deretter velger du den beslektede koblingen.
2. I **Rapportvalg - bankkonto** -vinduet, i feltet **Bruk**, velger du **Sjekk**.
3. Velg én av følgende rapport-ID-er:

| Rapport-ID | Rapportnavn | Beskrivelse |
| --- | --- | --- |
| 1401 |Sjekk |Dette er standardrapporten. |
| 10401 |Sjekk (blanket/blankett/sjekk) |Denne rapporten er utformet for utskrift i formatet blankett/blankett/sjekk. |
| 10411 |Sjekk (blanket/sjekk/blankett) |Denne rapporten er utformet for utskrift i formatet sjekk/blankett/sjekk. |

Når du har definert sjekkoppsettene, kan du skrive ut sjekker fra vinduet **Betalingskladd**. Hvis du vil ha mer informasjon, kan du se [Arbeide med sjekker](payables-how-work-checks.md).

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)   
[Fullføre prosesser ved periodens slutt](year-how-complete-period-end-processes.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

