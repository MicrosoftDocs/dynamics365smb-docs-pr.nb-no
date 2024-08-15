---
title: Oversikt over oppgaver for å behandle betalinger til leverandører
description: 'Gir en oversikt over oppgavene for å behandle betalinger til leverandører eller kreditorer, inkludert bokføring av betalingslinjene og oversikt over forfalt saldo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 07/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-payments"></a>Foreta betalinger

Du betaler leverandører eller kunder eller refusjoner til de ansatte ved å bokføre betalingslinjer på siden **Betalingskladd**. Utbetalingskladden er en finanskladd som er tilpasset for betalinger, med mange avanserte handlinger. Eksempler på dette er handlingen **Betalingsforslag – leverandør**, som finner leverandørbetalinger som har forfalt, og rapporten **Leverandør – forfallsoversikt**, som viser en oversikt over forfalte leverandørbetalinger.  

Du kan begynne betalingsprosessen fra lister, kort og poster for leverandører, kunder og ansatte. Hver av disse sidene har en knapp som starter betalingsflyten og hjelper deg med å fylle ut utbetalingskladden.  

Fra betalingskladden kan du skrive ut maskinelle sjekker eller registrere når sjekker skrives. Hvis du velger **Maskinell sjekk** i feltet **Bankbetalingstype**, må du skrive ut linjer som representerer sjekker, før du kan bokføre betalingskladden.

Når du har bokført betalingene, kan du eksportere dem til en bankfil som du kan laste opp til banken for behandling.

Når betalingene er foretatt i banken, må du utligne dem på deres tilknyttede åpne leverandør- eller ansattposter. Du kan utligne dem manuelt eller ved å importere en bankkontoutdragsfil og utligne betalingene automatisk. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

| Til | Se |
| --- | --- |
|Forstå grunnleggende funksjoner på siden **Utbetalingskladd**, som er basert på finanskladden, for å klargjøre for bokføring av betalinger til leverandører eller ansatte.|[Arbeid med finanskladder](ui-work-general-journals.md)|
|Bokfør betalinger til leverandører eller ansatte og refusjoner til kunder og eventuelt utligne betalingene til de relaterte ubetalte fakturaene/kreditnotaene for å lukke dem som betalt.|[Registrere betalinger og refusjoner](payables-how-post-payments-refunds.md)|
| Bruk en funksjon på **Utbetalingskladd**-siden til å foreslå leverandørbetalinger i henhold til valgte kriterier som forfallsdato, rabattberettigelse og din likviditet. |[Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md) |
| Utstede sjekker for leverandørbetalinger eller kunderefusjoner, enten som utskrifter eller maskinelle sjekker. Kansellere sjekker før eller etter bokføring. |[Foreta sjekkbetalinger](payables-how-work-checks.md) |
|Utfør elektroniske betalinger i henhold til standarden for EU SEPA-kredittoverføring.|[Betale med AMC Banking 365 Fundamentals-utvidelsen eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Betal leverandøren kontant eller med sjekk, og bokfør betalingen når du bokfører selve fakturaen. |[Gjøre opp kjøpsfakturaer omgående](finance-how-to-settle-purchase-invoices-promptly.md) |
| Du kan sørge for at at banken bare fjerner validerte sjekker og beløp ved å sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling. |[Eksporter en Positive Pay-fil](finance-how-positive-pay.md) |

## <a name="see-also"></a>Se også

[Administrere skyldige beløp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
