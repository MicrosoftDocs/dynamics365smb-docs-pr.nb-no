---
title: Synkroniser transaksjoner og utbetalinger
description: Definer og kjør import av transaksjoner og utbetalinger fra Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="transactions-and-payouts"></a>Transaksjoner og utbetalinger

Når en kunde utfører en betaling i nettbutikken, lagres betalingsinformasjonen som en **transaksjon**. Det kan hende flere transaksjoner er koblet til ordren, for eksempel når en kunde bruker et gavekort til å betale noen av kostnadene, og deretter har et kredittkort eller en PayPal for restbeløpet.

Hvis du bruker Shopify Payment som betalingsleverandør, kan du i tillegg til informasjon om penger som mottas fra kunden av betalingsleverandøren, også vise utbetalinger fra Shopify til bankkontoen.

## <a name="transactions"></a>Transaksjoner

Betalingstransaksjonene som finner sted i Shopify, synkroniseres med ordrene, og kan ses på siden **Shopify-ordrer**.

Hvis du vil se gjennom alle transaksjoner, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transaksjoner**. Velg den relaterte koblingen.

Feltet **Bokført fakturanr.** kan være en nyttig i avstemmingsprosessen.

Hvis du konfigurerte en betalingsmåtetildeling, vil det opprettede salgsdokumentet være tildelt en kode for betalingsmåte. Finn ut mer under [Betalingsmåtetildeling](#payment-method-mapping).

## <a name="payouts"></a>Utbetalinger

Hvis butikken bruker Shopify Payment, mottar du betalinger gjennom **Shopify-utbetalinger** når en kunde betaler ved hjelp av Shopify Payments og raskere betalinger.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil synkronisere utbetalinger med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser utbetalinger**.

Hvis du vil se gjennom alle utbetalinger, velger du ikon ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalinger**. Velg den relaterte koblingen.

**Utbetalinger** er bare til informasjonsformål og har ingen innvirkning på finans eller bankfinans, men de kan være nyttige når du behandler bankkontoutdraget.

## <a name="payment-method-mapping"></a>Tildeling av betalingsmåte

Hvis du vil fylle ut **betalingsmåtekoden** for salgsdokumenter som er importert fra Shopify automatisk, må du konfigurere **Tilordning av betalingsmåte**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil definere tildeling for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Tildeling av betalingsmåte**.
4. Skriv inn navnet på betalingsmåten fra i feltene **Gateway** og **Kredittkortfirma** fra Shopify. Posten opprettes automatisk når du importerer Shopify-ordrer.
5. Angi **betalingsmåtekoden** med den tilsvarende betalingsmåten i [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Angi **prioritet** for tilfeller der kunden bruker flere betalingsmåter. Betalingsmåten med høyest prioritet blir valgt i salgsdokumentet. Hvis begge betalingsmåtene har samme prioritet, brukes betalingsmåten med høyeste beløp.

> [!NOTE]  
> Hvis tilsvarende betalingsmåte i [!INCLUDE[prod_short](../includes/prod_short.md)] har **motkontotype** og **motkontonr.** fylt ut, vil fakturasystemet opprette en motpost av *betalingstypen* og bruke den på *fakturatypen* i kundeposten.

## <a name="use-cases"></a>Brukssaker
  
Parter:

* Kjøper – person som kjøper varer fra Shopify-nettbutikken.
* Forhandler – selskapet ditt.
* Betalingsleverandør – selskapet som tilrettelegger betalingsbehandlingen for deg. Kan være Shopify Payments eller en tredjepart.

### <a name="how-money-flows"></a>Hvordan penger flyter

Kjøperen kjøper varer i nettbutikk. Den siste fasen er å behandle betaling.

>[!NOTE]
> Dette eksemplet dekker ikke tilfeller når betalingen utføres utenfor Shopify-kassen, som er gyldig for B2B-scenarioer.
  
Kjøperen betaler med kredittkort, PayPal eller en lokal betalingsmåte som MobilePay i Danmark. Betalingsleverandøren tar hele beløpet fra kjøperen. På dette tidspunktet flyttes kjøperens penger til betalingsleverandøren.

Avhengig av betalingsleverandøren kan forhandleren se pengene på kontoen sin på betalingsleverandøren – både mottatte beløp og fratrukket provisjon. Betalingsleverandører tar ofte en provisjon fra hver transaksjon, og i noen tilfeller kan de også ha et fast gebyr.
  
Avhengig av betalingsleverandøren utløser forhandleren en overføring av pengene mot bankkontoen (utbetaling) manuelt, eller som skjer automatisk innenfor en definert periode, én gang per dag, én gang i måneden og så videre.
  
Avhengig av banken kan forhandleren se denne innkommende transaksjonen på bankkontoen via nettbank eller i bankkontoutdraget.

Det er flere alternativer for hvordan du håndterer betalingstransaksjoner i [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices"></a>Alternativ 1: Avstem innkommende overføringer til bankkonto mot de opprinnelige fakturaene
  
Forhandleren importerer ordrer til [!INCLUDE[prod_short](../includes/prod_short.md)] og bokfører følgeseddel og faktura.

Resultat: Systemet oppretter en **kundepost** av typen *faktura* med hele beløpet, Ja er valgt for **Åpen**. **Gjenværende beløp** er lik det fakturerte beløpet.

Forhandleren importerer bankkontoutdrag ved hjelp av betalingsavstemmingskladd.

Problemer:

1. Kan være vanskelig hvis det finnes flere fakturaer (og kreditnotaer), men én utbetaling fra betalingsleverandøren med en engangssum.
2. Beløp stemmer vanligvis ikke på grunn av provisjon. Du kan bruke betalingstoleranse eller kontantrabatter til å håndtere gebyr.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider"></a>Alternativ 2: Avstem innkommende overføringer til bankkonto mot en midlertidig konto som representerer penger hos betalingsleverandøren
  
Forhandleren importerer ordrer til [!INCLUDE[prod_short](../includes/prod_short.md)] og bokfører følgeseddel og faktura.
  
Resultat: Systemet oppretter en kundepost av typen **faktura** med hele beløpet, og Ja er valgt for **Åpen**. **Gjenværende beløp** er lik det fakturerte beløpet.

Siden ordren har en betalingsmåtekode der feltene **Motkontotype** og **Motkontonr.** er fylt ut, oppretter imidlertid systemet automatisk flere kunde poster av typen **betaling** og utligner den mot kundeposten som ble opprettet tidligere.

>[!NOTE]
> Systemet fyller ut feltet Betalingsmåtekode basert på betalingsmåtetilordning. Finn ut mer under [Betalingsmåtetildeling](#payment-method-mapping).
  
Du kan definere motkontoer for betalingsmåter på to måter:

* **Motkontotype** angitt som *Bank*, og **Motkontonr.** fyller ut den spesielle bankkontoen som representerer kontoen din hos betalingsleverandøren.
* **Motkontotype** angitt som *Finanskonto**, og **Motkontonr.** fyller ut finanskontoen som representerer kontoen din hos betalingsleverandøren.

Det er fornuftig å bruke en bankkonto hvis betalingsleverandøren eksporterer en slagskontooppgave som du kan importere inn i bankkontoavstemmingen.

Forhandleren importerer bankkontoutdrag ved hjelp av betalingsavstemmingskladd. Innkommende utbetaling kan behandles:

* som en overføring fra en annen bank. Hvis overføringen tar noen dager eller har valutakurs, kan det være at du vil bruke en midlertidig finanskonto.
* som en differanse på finanskontoen som representerer kontoen din hos betalingsleverandøren.
  
Den resterende saldoen på finans- eller bankkontoen som representerer kontoen hos betalingsleverandøren, kan skrives av som gebyrer/provisjon

Problemer:

1. Du kan opprette flere finans- eller bankkontoer hvis du er i ferd med å håndtere flere betalingsleverandører. Ordrer i [!INCLUDE[prod_short](../includes/prod_short.md)] støtter imidlertid bare én betalingsmåtekode, noe som gjør det vanskelig å håndtere saker når en kjøper bruker flere betalingsmåter for en ordre.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
