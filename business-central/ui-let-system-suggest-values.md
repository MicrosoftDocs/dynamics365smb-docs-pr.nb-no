---
title: La Business Central foreslå verdier
description: Du kan unngå manuelle beregninger og fullføre oppgaver raskt og nøyaktig ved å konfigurere automatisk dataregistrering slik at Business Central fyller ut utvalgte felt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '39, 251, 981'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="letting-includeprodshortincludesprodshortmd-suggest-values" />La [!INCLUDE[prod_short](includes/prod_short.md)] foreslå verdier
[!INCLUDE[prod_short](includes/prod_short.md)] kan hjelpe deg med å fullføre oppgaver raskere og mer riktig ved å forhåndsutfylle felt eller hele linjer med data som du ellers måtte beregne og skrive inn selv. Selv om slik automatisk dataregistrering alltid er riktig, kan du endre den senere ved behov.

Funksjonalitet som angir feltverdiene for deg tilbys vanligvis for oppgaver der du skriver inn store mengder transaksjonsdata og vil unngå feil og spare tid. Dette emnet inneholder et utvalg av slik funksjonalitet. Flere avsnitt vil bli lagt til i fremtidige oppdateringer av [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page" />Avmerkingsboksen **Foreslå motkontobeløp** på siden **Finanskladder**
Når du for eksempel angir finanskladdlinjer for flere utgifter som alle må bokføres til samme bankkonto, kan du få **Beløp**-feltet på bankkontolinjen oppdateres automatisk til beløpet som balanserer utgiftene, hver gang du angir en ny kladdelinje for en utgift. Hvis du vil ha mer informasjon om hvordan du arbeider med finanskladder, kan du se [Arbeid med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically" />Fylle ut **Beløp**-feltet automatisk på finanskladdlinjer for motkonto
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. På linjen for din foretrukne finanskladd kan du merke av for **Foreslå motkontobeløp**.
3. Åpne finanskladden, og fortsett med å registrere og bokføre transaksjoner ved hjelp av funksjonen som er beskrevet for automatisk registrering av en feltverdi.       

Hvis du vil ha informasjon om hvordan du konfigurerer en personlig finanskladd, for eksempel for håndtering av utgifter, kan du se [Arbeid med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page" />Feltet **Fyll ut mottaksdato automatisk** på siden **Betalingsregistrering**
Siden **Betalingsregistrering** viser utestående innkommende betalinger som linjer som representerer salgsdokumenter der et beløp er forfalt til betaling. Hvis du vil ha mer informasjon om utligning av kundebetalinger, kan du se [Avstemme kundebetalinger fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

De viktigste handlingene på siden er å merke av for **Betaling utført** og fylle ut feltet **Mottatt den**. Du kan definere at [!INCLUDE[prod_short](includes/prod_short.md)] automatisk angir arbeidsdatoen i feltet **Mottatt den** når du merker av for **Betaling utført**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically" />Fylle ut feltet **Mottatt den** automatisk på siden **Betalingsregistrering**
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsregistreringsoppsett** og velge den relaterte koblingen.
2. Merk av for **Fyll ut mottaksdato automatisk**.
3. Åpne siden **Betalingsregistrering**, og fortsett med å behandle inngående kundebetalinger ved hjelp av funksjonen som er beskrevet for automatisk registrering av en feltverdi.

## <a name="see-also" />Se også
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finans](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
