---
title: "Oversikt over oppgaver for å håndtere fordringer | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å håndtere fordringer og utligne betalinger mot kunde- eller leverandørposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a7944daaa0b07336361a03a9f46097f346481e66
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="managing-receivables"></a>Håndtere fordringer
Et vanlig trinn i en hvilken som helst finansielle rytmen er å avstemme bankkonti, som krever at du bruker betalinger til kunden eller leverandøren poster for å lukke salgsfakturaer og kreditnotaer til innkjøp.  

I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en av de raskeste måtene å registrere betalinger fra vinduet **Betalingsavstemmingskladd** på å importere en bankkontoutdragsfil eller feed for hurtig å registrere betalinger. Betalingene brukes til å åpne kunde- eller leverandørpostoppføringer basert på datasammenligninger mellom betalingstekst og oppføringsinformasjon. Du kan se gjennom og endre treff før du bokfører kladden, og lukk bankkontoposter for postene når du bokfører kladden. Bankkontoen avstemmes når alle betalinger er utlignet.

Det finnes imidlertid andre nyttige steder å utligne betalinger og avstemmer du bankkonti:  

* Vinduet **Bankkontoavstemminger**, der du kan også sjekke poster. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).  
* Vinduet **Betalingsregistrering**, der du kan utligne og manuelt kontrollere betalinger mottatt som kontanter, sjekk eller banktransaksjon, mot en generert liste over ubetalte salgsdokumenter. Legg merke til at denne funksjonen bare er tilgjengelig for salgsdokumenter.  
* Vinduet **Innbetalingskladd**, der du manuelt bokfører mottak på relevante finans-, kunde- eller andre kontoer, ved å angi en betalingslinje i. Du kan bruke mottaket eller refundere til én eller flere åpne poster før du bokfører innbetalingskladden, eller du kan utligne fra kundepostene.  

En annen del av håndtering av kundekonto er å samle utestående saldoer, inkludert rentenotaer og utstede purringer. [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder måter å gjøre også disse tingene på. For mer informasjon, se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

| Hvis du vil | Se |
| --- | --- |
| Utligne betalinger mot åpne kunde- eller leverandørposter basert på en importert bankkontoutdragsfil eller -feed, og avstemme bankkontoen når alle betalingene er utlignet. |[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Utligne betalinger mot åpne kundeposter basert på manuell oppføring i en liste over ubetalte salgsdokumenter. |[Avstemme kundebetalinger manuelt fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bokføre kontantmottak eller refusjoner for kunder i innbetalingskladden, og utligne mot kundeposter fra kladden eller bokførte poster. |[Avstemme kundebetalinger manuelt](receivables-how-apply-sales-transactions-manually.md) |
| Minne kundene om forfalte beløp, beregne rente og rentenotaer, og håndtere kortsiktige fordringer. |[Innkreve utestående saldi](receivables-collect-outstanding-balances.md) |
|Sikre at du vet hva leverte varer koster, ved å tilordne ekstra varekost, for eksempel frakt, fysisk håndtering, forsikring og transport, som du pådrar deg etter salg.|[Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md)|
|Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.|[Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

