---
title: Arbeide med GIFI-koder i Canada | Microsoft-dokumentasjon
description: Finn ut mer om GIFI-koder
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/23/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 03316fe6ad7a63c79a88f540a9c49f61450922f4
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-gifi-codes-in-canada"></a>Arbeide med GIFI-koder i Canada
Økonomiske informasjonen kan inkludere finanskontoer, rapporter, resultatregnskap, balanse og kontoutdrag for fri egenkapital. Økonomisk informasjon klassifiseres ved hjelp av koder. Bruken av koder lar myndighetene behandle informasjon, klargjøre for elektronisk lagring og validere mva-informasjon elektronisk. Bruken av koder bidrar også til at statistiske organisasjoner kan arbeide mer effektivt. Økonomiske opplysninger er for eksempel lettere tilgjengelig. Hvis du vil ha mer informasjon, kan du se [nettstedet for CRA](http://www.cra-arc.gc.ca/).

CRA bruker GIFI-koder (General Index of Financial Information) til å innhente, validere og behandle elektronisk økonomiske opplysninger og mva-informasjon. Anbefalt fremgangsmåte er å tilordne GIFI-koder bare til bokføringskonti, slik at alle summeringer gjøres av din programvare for mva-klargjøring.

Når en konto tilknyttes en GIFI-kode, rapporteres den til skattemyndighetene under denne koden. Flere konti kan alle ha samme GIFI-kode, men hver konto kan ha bare én GIFI-kode.

Du kan eksportere saldoinformasjon etter GIFI-kode og lagre den eksporterte filen i Excel, noe som er nyttig for overføring av informasjon til din programvare for mva-klargjøring.

## <a name="to-set-up-gifi-codes"></a>Definere GIFI-koder
I Dynamics NAV må du definere GIFI-koder for finanskontoer, rapporter, balanse, resultatregnskap og utdrag for fri egenkapital.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **GIFI-koder**, og deretter velger du den beslektede koblingen.
2. I vinduet **GIFI-koder** velger du handlingen **Ny**.
3. Definer GIFI-koder ved å fylle ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a>Knytte GIFI-koder til finanskonti
Hvis du vil rapportere økonomiske opplysninger, må hver GIFI-kode være tilknyttet de aktuelle kontoene i kontoplanen.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kontoplan**, og deretter velger du den beslektede koblingen.
2. Velg en relevant finanskonto, og velg deretter handlingen **Rediger**.
3. I hurtigfanen **Kostregnskap**, i **GIFI-kode**-feltet , velger du en passende GIFI-kode.

## <a name="to-view-account-balances-using-the-gifi-code-report"></a>Vise kontosaldoer ved hjelp av GIFI-koderapporten
Du kan se gjennom kontosaldoene etter GIFI-kode ved hjelp av rapporten **Kontosaldoer etter GIFI-koder**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kontosaldoer etter GIFI-koder**, og deretter velger du den beslektede koblingen.
2. Angi hva du vil inkludere i rapporten ved å fylle ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="to-export-balance-information-using-gifi-codes"></a>Eksportere saldoinformasjon ved hjelp av GIFI-koder
Du kan eksportere saldoinformasjon ved hjelp av GIFI-koder, og lagre den eksporterte filen i Excel. Du kan endre, lagre eller slette filen. Du kan bruke filen til å overføre informasjon til din programvare for mva-klargjøring.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Eksporter GIFI-informasjon til Excel**, og deretter velger du den beslektede koblingen.
2. Angi hva du vil eksportere til Excel ved å fylle ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg **OK**-knappen.

**Merk:** Excel-filen har følgende egenskaper:

* Saldoen er avrundet til nærmeste prosent, men celleverdien beholder den samme prosenten som den gjør i Finans.
* Negative tall representeres som positive tall i hakeparenteser. -123 er derfor representert som (123).

## <a name="see-also"></a>Se også
[Finans](finance.md)   
[Konfigurere finans](finance-setup-finance.md)

