---
title: La Business Central foreslå verdier
description: Du kan unngå manuelle beregninger og fullføre oppgaver raskt og nøyaktig ved å konfigurere automatisk dataregistrering slik at Business Central fyller ut utvalgte felt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="let--suggest-values"></a>La oss [!INCLUDE[prod_short](includes/prod_short.md)] foreslå verdier
[!INCLUDE[prod_short](includes/prod_short.md)] kan hjelpe deg med å fullføre oppgaver raskere og mer riktig ved å forhåndsutfylle felt eller hele linjer med data som du ellers måtte beregne og skrive inn selv. Selv om slik automatisk dataregistrering alltid er riktig, kan du endre den senere ved behov.

Funksjonalitet som angir feltverdiene for deg tilbys vanligvis for oppgaver der du skriver inn store mengder transaksjonsdata og vil unngå feil og spare tid. Denne artikkelen inneholder et utvalg av slike funksjoner. Flere avsnitt vil bli lagt til i fremtidige oppdateringer av [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Avmerkingsboksen **Foreslå motkontobeløp** på siden **Finanskladder**
Når du for eksempel angir finanskladdelinjer for flere utgifter som alle må bokføres på samme bankkonto, kan du få **Beløp-feltet** på bankkontolinjen automatisk oppdatert til beløpet som balanserer utgiftene, hver gang du angir en ny kladdelinje for en utgift. Hvis du vil ha mer informasjon om hvordan du arbeider med finanskladder, kan du se [Arbeid med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Fylle ut **Beløp**-feltet automatisk på finanskladdlinjer for motkonto
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. På linjen for din foretrukne finanskladd kan du merke av for **Foreslå motkontobeløp**.
3. Åpne finanskladden, og fortsett med å registrere og bokføre transaksjoner ved hjelp av funksjonen som er beskrevet for automatisk registrering av en feltverdi.       

Hvis du vil ha informasjon om hvordan du konfigurerer en personlig finanskladd, for eksempel for håndtering av utgifter, kan du se [Arbeid med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Feltet **Fyll ut mottaksdato automatisk** på siden **Betalingsregistrering**
 **Siden Registrer kundebetalinger** viser utestående innbetalinger som linjer som representerer salgsdokumenter der et beløp forfaller til betaling. Hvis du vil ha mer informasjon om utligning av kundebetalinger, kan du se [Avstemme kundebetalinger fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Hovedhandlingene på siden er å fylle ut avmerkingsboksene **Betaling utført** og **feltet Mottatt** dato. Du kan definere at [!INCLUDE[prod_short](includes/prod_short.md)] automatisk angir arbeidsdatoen i feltet **Mottatt den** når du merker av for **Betaling utført**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Fylle ut feltet **Mottatt den** automatisk på siden **Betalingsregistrering**
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistreringsoppsett** og velge den relaterte koblingen.
2. Merk av for **Fyll ut mottaksdato automatisk**.
3.  **Åpne siden Registrer kundebetalinger**, og fortsett med å behandle innkommende kundebetalinger ved hjelp av den beskrevne funksjonaliteten for automatisk registrering av en feltverdi.

## <a name="see-also"></a>Se også
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finans](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
