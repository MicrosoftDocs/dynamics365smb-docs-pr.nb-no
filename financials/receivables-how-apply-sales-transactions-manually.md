---
title: Avstemme kundebetalinger manuelt| Microsoft-dokumentasjon
description: Avstemme kundebetalinger manuelt
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 929404a3385a7964136226ae1ee1a8775dd7a62a
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-customer-payments-manually"></a>Avstemme kundebetalinger manuelt
Når du mottar en innbetaling fra en kunde eller foretar en refusjon, må du bestemme om du vil utligne betalingen eller refusjonen for å lukke én eller flere åpne debet- eller kreditposter. Du kan angi beløpet du vil utligne. Du kan for eksempel bruke akontobetalinger kundeposter. Lukke kundeposter sørger for at informasjon som kundestatistikk, kontoutdrag og rentenotaer er riktig.

**Merk**: I vinduet **Kundeposter** rødt betyr at relaterte betalingen på forfallsdatoen.

Du kan utligne kundeposter på flere måter:

* Ved å skrive inn informasjon i dedikerte vinduer, som vinduet **Innbetalingskladd** og **Betalingsavstemmingskladd**.
* Fra salgskreditnotadokumenter.
* Fra kundeposter etter at salgsdokumenter er postert, men ikke utlignet.

**Merk**: Hvis **Utligningsmetode**-feltet i kundekortet inneholder **Saldo**, utlignes betalinger automatisk mot den eldste åpne kreditposten, hvis du ikke manuelt angir en post. Hvis utligningsmetoden er **Manuelt**, må du alltid utligne poster manuelt.

Du kan utligne kundebetalinger manuelt i vinduet **Innbetalingskladd**. En innbetalingskladd er en type finanskladd, så du kan bruke den til å bokføre transaksjoner til finans-, bank-, kunde-, leverandør- og aktivakonti. Du kan utligne betalingen mot en eller flere debetposter når du bokfører betalingen, eller du kan utligne fra de bokførte postene senere.

Du kan også utligne kundebetalinger og leverandørbetalinger i vinduet **Betalingsavstemmingskladd**, ved hjelp av funksjoner for import av bankkontoutdrag, automatisk utligning og bankkontoavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md). Du kan også avstemme kundebetalinger basert på en liste over ubetalte salgsdokumenter i vinduet **Betalingsregistrering**. Hvis du vil ha mer informasjon, kan du se [Avstemme kundebetalinger fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Fylle ut og bokføre en innbetalingskladd
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innbetalingskladd**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Rediger kladd**.
3. Velg den aktuelle kjørselen i **Bunkenavn**-feltet.
4. Fyll ut feltet **Bokføringsdato**.  
5. Velg **Betaling** i **Bilagstype**-feltet.

    **Bilagsnr.**- feltet fylles ut av nummerserien som er tilordnet partiet.  
6. Bruk **Eksterndokumentnr.**- feltet til å lagre en identifikator, for eksempel kundens sjekknummer.
7. Velg **Kunde** i **Kontotype**-feltet.
8. I **Kontonummer** -feltet velger du den aktuelle finanskontoen.
9. Hvis du vil bokføre utligningen samtidig som du bokfører kladden, gjør du ett av følgende.
10. I **Motkontotype**-feltet velger du **Finanskonto** for utbetalinger og **Bankkonto** for andre betalinger.
11. I **Motkontonr.**- -feltet velger du kassekonto for utbetalinger eller relevante bankkonti for andre betalinger.
12. Bokfør kladden.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Slik utligner du en betaling mot én kundepost
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innbetalingskladd**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Rediger kladd**.
3. På den første kladdelinjen angir du aktuelle opplysninger om posten som skal utlignes.
4. Angi **Betaling** i **Bilagstype**-feltet.
5. Angi **Kunde** i **Kontotype**-feltet.
6. Angi **Bankkonto** i **Motkontotype**-feltet.
7. I **Utligningsbilagsnr.** -feltet velger du feltet for å åpne vinduet **Utlign kundeposter**.
8. Velg posten som betalingen skal utlignes mot, i vinduet **Utlign kundeposter**.
9. I feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for posten. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.

    Nederst i vinduet **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
10. Velg **OK**-knappen. Vinduet **Innbetalingskladd** viser nå posten du har valgt, registrert i feltene **Utligningsbilagstype** og **Utligningsbilagsnr.** -feltene.
11. Bokfør innbetalingskladden.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Slik utligner du en utbetaling mot flere kundeposter
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innbetalingskladd**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Rediger kladd**.
3. På den første kladdelinjen angir du aktuelle opplysninger om posten som skal utlignes.
4. Angi **Betaling** i **Bilagstype**-feltet.
5. Angi **Kunde** i **Kontotype**-feltet.
6. Angi **Bankkonto** i **Motkontotype**-feltet.
7. Angi hele betalingen som et negativt beløp i **Beløp**-feltet.
8. Hvis du vil utligne betalingen mot flere kundeposter når du bokfører, velger du handlingen **Utlign poster**.
9. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID**.
10. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.

    Nederst i vinduet **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
11. Velg **OK**-knappen.
12. Bokfør innbetalingskladden.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Slik utligner du en kreditnota mot én kundepost
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Salgskreditnotaer**, og deretter velger du den beslektede koblingen.
2. Åpne den aktuelle salgskreditnotaen.
3. Hvis du vil utligne kreditnotaen til én kundepost når du bokfører i feltet **Utligningsbilagsnr.**,  velger du posten du vil utligne betalingen mot.
4. På linjen i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for posten.  

    Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet automatisk. Nederst i vinduet **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.    
5. Velg **OK**-knappen. Vinduet **Salgskreditnota** viser nå posten du har valgt, registrert i feltene **Utligningsbilagstype** og **Utligningsbilagsnr.** -feltene. Og beløpet på kreditnotaen som skal bokføres, utlignet for eventuelle betalingsrabatter.
6. Bokfør kreditnotaen.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Slik utligner du en kreditnota mot flere kundeposter
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Salgskreditnotaer**, og deretter velger du den beslektede koblingen.
2. Åpne den aktuelle salgskreditnotaen.
3. Hvis du vil utligne kreditnotaen mot flere kundeposter når du bokfører, velger du handlingen **Utlign poster**.
4. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID**.
5. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.  

    Nederst i vinduet **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
6. Velg **OK**-knappen. Vinduet **Salgskreditnota** viser nå beløpet på kreditnotaen som skal bokføres, utlignet for eventuelle betalingsrabatter.
7. Bokfør kreditnotaen.

## <a name="to-apply-posted-customer-ledger-entries"></a>Slik utligner du bokførte kundeposter
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kunder**, og deretter velger du den beslektede koblingen.
2. Åpne kundekortet med postene du vil utligne.
3. Velg handlingen **Poster**, og velg deretter linjen med posten som skal være utligningsposten.
4. Velg handlingen **Utlign poster**. Vinduet **Utlign kundeposter** åpnes med de åpne postene for kunden.
5. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID** .
6. For hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.  

    Nederst i vinduet **Utlign kundeposter** kan du se det bestemte beløpet i feltet **Utlignet beløp**.  
7. Velg handlingen **Etterutligne**. Vinduet **Etterutligne** vises med dokumentnummeret for utligningsposten og bokføringsdatoen for posten med den seneste bokføringsdatoen.  
8. Velg **OK**-knappen for å bokføre applikasjonen.

    Hvis den bokførte utligningen har resultert i lukkede kundeposter, er **Åpne**-feltet tomt for disse postene.    
9. Hvis du vil se kundeposter, i øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kunder**, og deretter velger du den beslektede koblingen. Bla til kortet for den relevante kunden for å se postene.  

I postoversikten er det ikke merket av for **Åpen** på linjen som inneholder posten som ble fullstendig utlignet.  

**Merk**: Når du har valgt en post fra vinduet **Utlign kundeposter** eller flere poster ved å angi **Utlignings-ID**, inneholder feltet **Utlignet beløp** på kladdelinjen summen av de gjenstående beløpene for de bokførte postene du har valgt, hvis ikke feltet allerede inneholder verdier. Hvis du velger **Saldo** i feltet **Utligningsmetode** på kundekortet, utlignes inntreffer utligningen automatisk.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Slik utligner du kundeposter i forskjellige valutaer mot hverandre
Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du likevel utligne fakturaen mot betalingen.  

Hvis du utligner en post (post 1) i én valuta mot en post (post 2) i en annen valuta, brukes bokføringsdatoen i post 1 til å søke etter den relevante valutakursen for å konvertere beløp i post 2. Den relevante valutakursen finnes i **Valutakurser**-vinduet.  

Utligning av kundeposter i forskjellige valutaer må være aktivert. Hvis du vil ha mer informasjon, kan du se [Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Innbetalingskladd**, og deretter velger du den beslektede koblingen.
2. Åpne kladden du vil bruke, og fyll ut den første tomme kladdelinjen med en valutakode.
3. Velg handlingen **Utlign poster**.
4. Velg linjen med posten du vil utligne mot posten i innbetalingskladden. Deretter velger du handlingen **Angi utlignings-ID** og merker posten du vil utligne mot.
5. Velg **OK**-knappen for å gå tilbake til innbetalingskladden.
6. Bokfør salgskladden.  

**Viktig**: Når du utligner poster i ulike valutaer, konverteres postene til USD. Selv om valutakursene for de to valutaene er fast, for eksempel mellom USD og EUR, kan det oppstå et lite restbeløp når de omregnes til USD. Disse små restbeløpene bokføres som agio eller disagio for kontoen som er spesifisert i feltet **Konto for realisert agio** eller **Konto for realisert disagio** i vinduet **Valutaer**. Feltet **Beløp (USD)** justeres også i leverandørpostene.  

## <a name="to-correct-an-application-of-customer-entries"></a>Korrigere en utligning av kundeposter
Når du korrigerer en utligning, opprettes og bokføres korreksjonsposter (poster som er identiske med de opprinnelige postene, men som har motsatt fortegn i beløpsfeltet) for alle poster, inkludert alle finansbokføringer som er avledet fra utligningen, for eksempel betalingsrabatt og valutagevinst/-tap. Postene som ble lukket av utligningen, åpnes på nytt.  

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kunder**, og deretter velger du den beslektede koblingen.
2. Åpne det relevante kundekortet.
3. Velg handlingen **Poster**.
4. Velg den relevante posten, og velg deretter handlingen **Opphev utligning**.
5. Du kan også velge handlingen **Detaljert post**.
6. Velg utligningsposten, og velg deretter handlingen **Opphev utligning**.
7. Fyll ut feltene i hodet, og klikk deretter handlingen **Opphev utligning**.  

**Viktig**: Hvis en post er utlignet av mer enn én utligningspost, må du oppheve utligningen av den seneste utligningsposten først.  

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

