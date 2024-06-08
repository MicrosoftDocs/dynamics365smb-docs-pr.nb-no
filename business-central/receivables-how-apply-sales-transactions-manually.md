---
title: Avstemme kundebetalinger med innbetalingskladden eller fra kundeposter
description: Utligne kontantmottak eller refusjoner fra kunder mot én eller flere åpne kundeposter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="reconcile-customer-payments-with-a-cash-receipt-journal-or-from-customer-ledger-entries"></a>Avstemme kundebetalinger med en innbetalingskladd eller fra kundeposter

Når du mottar en kontant betaling fra en kunde eller gir en kontantrefusjon, kan du bruke betalingen eller refusjonen til å lukke åpne debet eller kredit. Du kan angi beløpet du vil utligne. Du kan for eksempel bruke akontobetalinger kundeposter. Det å lukke kundeposter holder kundestatistikk, kontoutdrag, rentenotaer osv. oppdatert.

> [!TIP]  
> På siden **Kundeposter** betyr rød skrift at forfallsdatoen for den relaterte betalingen er overskredet. Hvis forfalte betalinger blir et problem, kan vi hjelpe deg med å redusere hyppigheten. Du kan aktivere utvidelsen for **forsinkede betalingsprognoser**, som bruker en prediksjonsanalyse som vi har innebygd i Azure Machine Learning for å forutse tidsberegningen av betalinger. Disse forutsigelser hjelper deg med å redusere utestående tilgodehavender og finjustere innkrevingsstrategien. Hvis en betaling er forutsatt å bli sen, kan du justere betalingsbetingelsene eller betalingsmåten for kunden. Hvis du vil ha mer informasjon, kan du se [Forsinkede betalingsprognoser](ui-extensions-late-payment-prediction.md).  

Du kan utligne kundeposter på flere måter:

* Angi informasjon på følgende sider:
   * Siden **Betalingsavstemmingskladd**. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).
   * Siden **Betalingsregistrering**. Hvis du vil ha mer informasjon, kan du se [Avstemme kundebetalinger fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
   *  **Siden Innbetalingskladd** . Hvis du vil ha mer informasjon, kan du se [Fylle ut og bokføre en innbetalingskladd](#to-fill-and-post-a-cash-receipt-journal).
* Ved å fylle ut feltet **Utligningsdokumentnr.** på salgskreditnotadokumenter. Hvis du vil ha mer informasjon, kan du se [Slik utligner du en kreditnota på én kundepost](#to-apply-a-credit-memo-to-a-single-customer-ledger-entry).
* Ved hjelp av handlingen **Angi utlignings-ID** på en kundepost. Hvis du vil ha mer informasjon, kan du se [Slik utligner du en betaling mot én kundepost](#to-apply-a-payment-to-a-single-customer-ledger-entry).
* Ved å bruke handlingen **Utlign poster** på **Bankinnbetaling**-siden, og deretter angi fakturanummeret i **Utlignings-ID**-feltet. Hvis du vil ha mer informasjon, kan du se [Opprett bankinnbetalinger](bank-create-bank-deposits.md).

> [!NOTE]  
> Hvis feltet **Utligningsmetode** på kundekortet inneholder **Saldo**, utlignes betalinger automatisk mot den eldste åpne kreditposten, med mindre du ikke angir en post manuelt. Hvis utligningsmetoden er **Manuelt**, må du alltid utligne poster manuelt.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Fylle ut og bokføre en innbetalingskladd

En innbetalingskladd er en type finanskladd. Du kan bruke den til å bokføre transaksjoner til finans-, bank-, kunde-, leverandør- og aktivakontoer. Du kan utligne betalingen mot en eller flere debetposter når du bokfører betalingen. Du kan også utligne fra de bokførte postene senere.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Innbetalingskladd** og velg den relaterte koblingen.
2. Velg handlingen **Rediger kladd**.
3. Velg den aktuelle kjørselen i **Bunkenavn**-feltet.
4. Fyll ut feltet **Bokføringsdato**.  
5. Velg **Betaling** i **Bilagstype**-feltet.

    **Bilagsnr.**-feltet fylles ut med nummerserien som er tilordnet kjørselen.  
6. Bruk feltet **Eksterndokumentnr.** til å lagre en identifikator, for eksempel kundens sjekknummer.

   > [!NOTE]
   > Som standard er Eksternt dokumentnr. -feltet er skjult. Hvis den er det, og du vil bruke den, kan du bruke tilpasning for å legge den til. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

7. Velg **Kunde** i **Kontotype**-feltet.
8. I kontonummeret **.** -feltet, velger du kunden.
9. Hvis du vil bokføre søknaden samtidig som du bokfører kladden, fyller du ut følgende felt:
   1. I **Motkontotype**-feltet velger du **Finanskonto** for utbetalinger og **Bankkonto** for andre betalinger.
   2. I **Motkontonr.**-feltet velger du kassekonto for utbetalinger eller relevante bankkonti for andre betalinger.
10. Bokfør kladden.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Slik utligner du en betaling mot én kundepost

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innbetalingskladd** og velg den relaterte koblingen.
2. Velg handlingen **Rediger kladd**.
3. På den første kladdelinjen angir du aktuelle opplysninger om posten som skal utlignes.
4. Angi **Betaling** i **Bilagstype**-feltet.
5. Angi **Kunde** i **Kontotype**-feltet.
6. Angi **Bankkonto** i **Motkontotype**-feltet.
7. I feltet **Utligningsbilagsnr.** velger du feltet for å åpne siden **Utlign kundeposter**.
8. Velg posten som betalingen skal utlignes mot, på siden **Utlign kundeposter**.
9. I feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for posten. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.

    Nederst på siden **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
10. Velg **OK**-knappen. Siden **Innbetalingskladd** viser nå posten i feltene **Utligningsbilagstype** og **Utligningsbilagsnr.**.
11. Bokfør innbetalingskladden.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Slik utligner du en utbetaling mot flere kundeposter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Innbetalingskladd** og velg den relaterte koblingen.
2. Velg handlingen **Rediger kladd**.
3. På den første kladdelinjen angir du aktuelle opplysninger om posten som skal utlignes.
4. Angi **Betaling** i **Bilagstype**-feltet.
5. Angi **Kunde** i **Kontotype**-feltet.
6. Angi **Bankkonto** i **Motkontotype**-feltet.
7. Angi hele betalingen som et negativt beløp i **Beløp**-feltet.
8. Hvis du vil utligne betalingen mot flere kundeposter når du bokfører, velger du handlingen **Utlign poster**.  
9. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID**.  
10. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.

    Nederst på siden **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
11. Velg **OK**.
12. Bokfør innbetalingskladden.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Slik utligner du en kreditnota mot én kundepost

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Åpne den aktuelle salgskreditnotaen.
3. Hvis du vil utligne kreditnotaen mot én enkelt kundepost når du bokfører, velger du posten som du vil utligne betalingen mot, i feltet **Utligningsbilagsnr.**.
4. På linjen i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for posten.  

    Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet automatisk. Nederst på siden **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
5. Velg **OK**-knappen.  **Siden Salgskreditnota** viser nå posten du valgte i Utligningsbilagstype **og** **Utligningsbilagsnr.** Felt. Og beløpet på kreditnotaen som skal bokføres, utlignet for eventuelle betalingsrabatter.
6. Bokfør kreditnotaen.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Slik utligner du en kreditnota mot flere kundeposter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Åpne den aktuelle salgskreditnotaen.
3. Hvis du vil utligne kreditnotaen mot flere kundeposter når du bokfører, velger du handlingen **Utlign poster**.
4. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID**.
5. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.  

    Nederst på siden **Utlign kundeposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.  
6. Velg **OK**. Siden **Salgskreditnota** viser nå beløpet på kreditnotaen som skal bokføres, utlignet for eventuelle betalingsrabatter.
7. Bokfør kreditnotaen.

## <a name="to-apply-posted-customer-ledger-entries"></a>Slik utligner du bokførte kundeposter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne kundekortet med postene du vil utligne.
3. Velg handlingen **Poster**, og velg deretter linjen med posten som er den utlignede posten.
4. Velg handlingen **Utlign poster**. Siden **Utlign kundeposter** åpnes med de åpne postene for kunden.
5. Velg linjene med postene du vil at utligningsposten skal utlignes mot, og velg deretter handlingen **Angi utlignings-ID** .
6. For hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post. Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet.  

    Nederst på siden **Utlign kundeposter** kan du se det bestemte beløpet i feltet **Utlignet beløp**.  
7. Velg handlingen **Etterutligne**. Siden **Etterutligne** åpnes med dokumentnummeret for utligningsposten og bokføringsdatoen for posten med den seneste bokføringsdatoen.  
8. Velg **OK** for å bokføre applikasjonen.

    Hvis den bokførte utligningen resulterte i lukkede kundeposter, tømmes Åpne-feltet **for** disse postene.  
9. Hvis du vil se postene, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen. Bla til kortet for den relevante kunden for å se postene.  

I postoversikten er det ikke merket av for **Åpen** på linjen som inneholder posten som ble fullstendig utlignet.  

> [!NOTE]  
> Når du har valgt en post på siden **Utlign kundeposter** eller flere poster ved å angi **Utlignings-ID**, inneholder feltet **Utlignet beløp** på kladdelinjen summen av de gjenstående beløpene for de bokførte postene du har valgt, hvis ikke feltet allerede inneholder verdier. Hvis du velger **Saldo** i feltet **Utligningsmetode** på kundekortet, utlignes inntreffer utligningen automatisk.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Slik utligner du kundeposter i forskjellige valutaer mot hverandre

Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du likevel utligne fakturaen mot betalingen.  

Her er et eksempel. Du utligner post A i én valuta på post B i en annen valuta. Bokføringsdatoen i post A brukes til å finne valutakursen som skal brukes til å konvertere beløp i post B. Du finner valutakursen på Valutakurser-siden **·** .  

Utligning av kundeposter i forskjellige valutaer må være aktivert. Hvis du vil ha mer informasjon, kan du se [Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Innbetalingskladd** og velg den relaterte koblingen.
2. Åpne kladden du vil bruke, og fyll ut den første tomme kladdelinjen med en valutakode.
3. Velg handlingen **Utlign poster**.
4. Velg linjen med posten du vil utligne mot posten i innbetalingskladden. Deretter velger du handlingen **Angi utlignings-ID** og merker posten du vil utligne mot.
5. Velg **OK** for å gå tilbake til innbetalingskladden.
6. Bokfør salgskladden.  

> [!IMPORTANT]  
>   Når du utligner poster i ulike valutaer, konverteres postene til USD. Selv om valutakursene for de to valutaene er fast, for eksempel mellom USD og EUR, kan det oppstå et lite restbeløp når de omregnes til USD. Disse små restbeløpene bokføres som agio eller disagio for kontoen som er spesifisert i feltene **Konto for realisert agio** eller **Konto for realisert disagio** på siden **Valutaer**. Feltet **Beløp (USD)** justeres også i leverandørpostene.  

## <a name="to-correct-an-application-of-customer-entries"></a>Korrigere en utligning av kundeposter
Når du korrigerer en utligning, opprettes og bokføres korrigeringsposter for alle poster. Korrigeringspostene er de samme som originalene, men med motsatt rekkefølge i **Beløp**-feltet. Korrigeringspostene inkluderer alle finansposter som er avledet fra utligningen. Det kan for eksempel være kontantrabatt og valutagevinst/-tap. Postene som programmet lukket, åpnes på nytt.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne det relevante kundekortet.
3. Velg handlingen **Poster**.
4. Velg den relevante posten, og velg deretter handlingen **Opphev utligning**.
5. Du kan også velge handlingen **Detaljert post**.
6. Velg utligningsposten, og velg deretter handlingen **Opphev utligning**.
7. Fyll ut feltene i hodet, og klikk deretter handlingen **Opphev utligning**.  

> [!IMPORTANT]  
>   Hvis en post er utlignet av mer enn én utligningspost, må du oppheve utligningen av den seneste utligningsposten først.  

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
