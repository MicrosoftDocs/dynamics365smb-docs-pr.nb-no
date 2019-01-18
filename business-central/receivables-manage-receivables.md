---
title: "Oversikt over oppgaver for å håndtere fordringer | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å håndtere fordringer og utligne betalinger mot kunde- eller leverandørposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 11/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 2e677a1170be8f55421869ca0308fb31961b58f7
ms.contentlocale: nb-no
ms.lasthandoff: 11/22/2018

---
# <a name="managing-receivables"></a>Håndtere fordringer
Et vanlig trinn i en hvilken som helst finansielle rytmen er å avstemme bankkonti, som krever at du bruker innkommende betalinger til kunden eller leverandøren poster for å lukke salgsfakturaer og kreditnotaer til innkjøp som betalt.

Selv om de fleste kundene i B2B-miljøer betaler en stund etter levering, slik at de bokførte salgsfakturaene er åpne og kan lukkes av regnskapsavdelingen når betalingen mottas, kan noen salgsfakturaer betales umiddelbart, for eksempel med PayPal. Slike fakturaer utlignes umiddelbart som betalt når de bokføres, og vises derfor ikke som betalinger som skal behandles i kortsiktige fordringer. Hvis du vil ha mer informasjon, kan du for eksempel se [Fakturere salg](sales-how-invoice-sales.md).  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en av de raskeste måtene å registrere betalinger på fra siden **Betalingsavstemmingskladd** ved å importere en bankkontoutdragsfil eller feed. Betalingene brukes til å åpne kunde- eller leverandørpostoppføringer basert på datasammenligninger mellom betalingstekst og oppføringsinformasjon. Du kan se gjennom og endre treff før du bokfører kladden, og lukk bankkontoposter for postene når du bokfører kladden. Bankkontoen avstemmes når alle betalinger er utlignet.

Det finnes andre sider der du kan utligne betalinger eller avstemme bankkonti:

* **Bankkontoavstemming**-siden, der du avstemmer bankkonti ved å samsvare importerte bankkontoutdragslinjer med bankkontopostene i systemet. Her kan du også avstemme sjekkutbetalinger. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md). Her kan du ikke utligne betalinger.
* Siden **Betalingsregistrering**, der du kan manuelt utligne betalinger mottatt som kontanter, sjekk eller banktransaksjon, mot en generert liste over ubetalte salgsdokumenter. Legg merke til at denne funksjonen bare er tilgjengelig for salgsdokumenter. Her kan du ikke utligne utgående betalinger, og du kan ikke avstemme bankkonti.
* Siden **Innbetalingskladd**, der du manuelt bokfører mottak på relevante finans-, kunde- eller andre kontoer, ved å angi en betalingslinje. Du kan bruke mottaket eller refundere til én eller flere åpne poster før du bokfører innbetalingskladden, eller du kan utligne fra kundepostene. Her kan du ikke avstemme bankkonti.  

Andre sider ved behandling av kundekontoer er å innkreve utestående saldi, inkludert rentenotaer og purringer, og å definere bankkonti for å tillate at kundebetalinger trekkes fra kontoen automatisk.

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

| Hvis du vil | Se |
| --- | --- |
| Utligne betalinger mot åpne kunde- eller leverandørposter basert på en importert bankkontoutdragsfil eller -feed, og avstemme bankkontoen når alle betalingene er utlignet. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Definer tilordninger mellom tekst på betalinger og bestemte debet-, kredit- og motkonti, slik at slike betalinger bokføres på de angitte kontiene når du bokfører kladden for betalingsavstemming.|[Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Utligne betalinger mot åpne kundeposter basert på manuell oppføring i en liste over ubetalte salgsdokumenter. |[Avstemme kundebetalinger manuelt fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bokføre kontantmottak eller refusjoner for kunder i innbetalingskladden, og utligne mot kundeposter fra kladden eller bokførte poster. |[Avstemme kundebetalinger manuelt](receivables-how-apply-sales-transactions-manually.md) |
| Minne kundene om forfalte beløp, beregne rente og rentenotaer, og håndtere kortsiktige fordringer. |[Innkreve utestående saldi](receivables-collect-outstanding-balances.md) |
| Forutse når betalinger foretas sent for salgsdokumenter. | [Utvidelsen Prognose for forsinket betaling](ui-extensions-late-payment-prediction.md) |
|Med kundens samtykke kan du kreve inn betaling direkte fra kundens bankkonto bare i euro.|[Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)|
|Sperr en kunde fra å bli registrert i dokumenter eller fra bokføring, for eksempel på grunn av insolvens.|[Sperre kunder](receivables-how-block-customers.md)|
|Sikre at du vet hva leverte varer koster, ved å tilordne ekstra varekost, for eksempel frakt, fysisk håndtering, forsikring og transport, som du pådrar deg etter salg.|[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)|
|Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.|[Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

