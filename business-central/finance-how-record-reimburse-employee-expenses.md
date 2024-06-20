---
title: Registrere og refundere ansattes utgifter
description: 'Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør deretter en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 03/13/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Registrere og refundere ansattes utgifter

[!INCLUDE[prod_short](includes/prod_short.md)] støtter transaksjoner for ansatte på lignende måte som for leverandører. Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.

> [!NOTE]  
> Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.

Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte. Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.  

Denne artikkelen forklarer hvordan du registrerer utgiftene i bøkene og hvordan du refunderer den ansatte. Organisasjonen kan ha en portal eller app der ansatte kan sende reiseregninger.

[!INCLUDE [prod_short](includes/prod_short.md)] er fleksibel nok til å dekke mange forskjellige rutiner. De nøyaktige kontonumrene som skal brukes, avhenger av organisasjonens konfigurasjon og prosesser.  

Du kan bruke finanskladder for ansattkontoer til å registrere ansattes utgifter og refusjonstransaksjoner i utenlandsk valuta, og deretter enkelt spore beløpene og sammenligne dem med mottak. La kalkulatoren ligge i skrivebordsskuffen – Business Central kan justere valutakursen for deg. Når du bruker finanskladder til å bokføre transaksjoner for ansattkontoer, for eksempel når du refunderer utgifter, kan du bruke feltet **Valutakode** til å angi valutaen for transaksjonene. Ved å angi en valuta kan du bruke de samme funksjonene som når du registrerer transaksjoner i kunde- og leverandørpostene. Ansatte kan for eksempel registrere en utgift i euro, men få betalt i dollar.

Hvis du vil sikre at valutakursen for beløpene er oppdatert, kan du justere de ansattes saldoer når du kjører satsjobben Valutakurs. Hvis du vil bruke valutakurstabellen, men gjøre opp ansattes saldoer i lokal valuta, kan du ekskludere ansattes kontoer når du justerer valutakursene.

## Slik registrerer du utgifter for en ansatt

Du bokfører utgifter for de ansatte på siden **Finanskladd**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.  
2. Åpne den relevante finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.

    > [!TIP]  
    > Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**. Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.
5. Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.

## Slik refunderer du en ansatt

Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer på siden **Utbetalingskladd**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.
2. Åpne den relevante kjørselen for utbetalingskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).
4. Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.
5. Velg handlingen **Bokfør** for å registrere refusjonen.  

## Slik avstemmer du refusjoner med finansposter for ansatte

Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel på siden **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan også utligne manuelt på siden **Ansattposter**. Hvis du vil ha mer informasjon, kan du se relatert [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).  

## Se også

[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Tilbakefør kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]