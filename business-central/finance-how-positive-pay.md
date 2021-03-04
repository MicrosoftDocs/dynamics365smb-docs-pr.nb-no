---
title: Eksportere Positive Pay-filer | Microsoft-dokumentasjon
description: Du kan sikre at banken bare innfrir validerte sjekker og beløp, ved å eksportere en Positive Pay-fil som inneholder leverandør-og betalingsinformasjon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8856ee09ae728d685d3f57786abc29d9aca93778
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750858"
---
# <a name="export-a-positive-pay-file"></a>Eksportere en Positive Pay-fil
For å sørge for at banken bare innfrir validerte sjekker og beløp, kan du eksportere en Positive Pay-fil med relevant leverandørinformasjon, sjekknummer og betalingskonto, som du deretter sender til banken for referanse når du behandler betalinger.

[!INCLUDE[prod_short](includes/prod_short.md)] er forhåndskonfigurert til å støtte Positive Pay-filer for Bank of America og City Bank.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Slik definerer du en bankkonto for Positive Pay
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Åpne kortet for bank du vil bruke Positive Pay for.
3. Angi POSPAYBANK i feltet **Kode for eksport for Positive Pay**.
4. Lukk siden.

## <a name="to-export-a-positive-pay-file"></a>Slik eksporterer du en Positive Pay-fil
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg bankkontoen som du vil eksportere en Positive Pay-fil for.
3. Velg **Eksport for Positive Pay**.

    Siden **Eksport for Positive Pay** åpnes med betalinger som er gjort for bankkontoen siden den forrige datoen for opplasting, som vist i feltene **Dato for siste oppdatering** og **Klokkeslett for siste oppdatering**.
4. I feltet **Dato for frist for oppdatering** field angir du en dato, og betalinger blir ikke inkludert i den eksporterte filen før denne datoen.
5. Velg handlingen **Eksporter**.
6. På siden **Eksporter fil** velger du **Lagre**-knappen, og deretter lagrer du filen på en passende plassering.
7. Last opp filen til det elektroniske bankområdet.
8. Skriv ned eller kopier bekreftelsesnummeret som vises når filopplastingen er vellykket.

Vise eksporterte Positive Pay-poster

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg bankkontoen som du vil vise Positive Pay-eksportposter for.
3. Velg **Poster for Positive Pay**.

    På siden **Poster for Positive Pay** kan du se alle Positive Pay-eksportpostene for bankkontoen.
4. I feltet **Bekreftelsesnummer** angir du bekreftelsesnummeret som du får når opplastingen av filen til banken er vellykket, for hver post for eksport.
5. For å vise de relaterte betalingslinjene, velger du **Detaljer for poster for Positive Pay**.

Eksportere Positive Pay-filer på nytt

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg bankkontoen som du vil eksportere Positive Pay-filer på nytt for.
3. Velg **Poster for Positive Pay**.
4. Velg linjen for Positive Pay-eksportfilen som du vil eksportere på nytt.
5. På siden **Poster for Positive Pay** velger du **Eksporter Positive Pay til fil på nytt**.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]