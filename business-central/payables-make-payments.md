---
title: "Oversikt over oppgaver for å behandle betalinger til leverandører | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å behandle betalinger til leverandører eller kreditorer, inkludert bokføring av betalingslinjene og oversikt over forfalt saldo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 6b912e8f54fd0e3fb4ac4a1eee3c376c209ffe65
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2018

---
# <a name="making-payments"></a>Utføre betalinger
Når du foretar betalinger til leverandører eller refusjoner til de ansatte, kan du bokføre de relaterte betalingslinjene i vinduet **Betalingskladd**. Du kan bruke funksjonen **Betalingsforslag – leverandør** til å finne leverandørbetalinger som har forfalt. Du kan også bruker rapporten **Leverandør – forfallsoversikt** til å få oversikt over leverandørbetalinger som har forfalt.

Fra betalingskladden kan du skrive ut maskinelle sjekker eller registrere når sjekker skrives. Hvis du velger **Maskinell sjekk** i feltet **Bankbetalingstype**, må eventuelle linjer som representerer sjekker skrives ut før betalingskladden kan bokføres.

Når betalingene er bokført, kan du eksportere dem til en bankfil for opplasting til banken for behandling.

Når betalingene er foretatt i banken, må du utligne dem på deres tilknyttede åpne leverandør- eller ansattposter. Du kan gjøre dette manuelt eller ved å importere en bankkontoutdragsfil og utligne betalingene automatisk. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Til | Se |
| --- | --- |
|Forstå grunnleggende funksjoner i vinduet **Utbetalingskladd**, som er basert på finanskladden, for å klargjøre for bokføring av betalinger til leverandører eller ansatte.|[Arbeide med finanskladder](ui-work-general-journals.md)|
|Bokfør betalinger til leverandører og refusjoner til kunder og eventuelt utligne betalingene til de relaterte ubetalte fakturaene/kreditnotaene for å lukke dem som betalt.|[Registrere betalinger og refusjoner](payables-how-post-payments-refunds.md)|
| Bruk en funksjon i **Utbetalingskladd**-vinduet til å foreslå leverandørbetalinger i henhold til valgte kriterier som forfallsdato, rabattberettigelse og din likviditet. |[Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md) |
| Utstede sjekker for leverandørbetalinger eller kunderefusjoner, enten som utskrifter eller maskinelle sjekker. Kansellere sjekker før eller etter bokføring. |[Foreta sjekkbetalinger](payables-how-work-checks.md) |
|Foreta elektroniske betalinger ved å eksportere betalinger til en bankfil som du laster opp til banken for behandling, inkludert EFT (elektronisk pengeoverføring) i Nord-Amerika. |[Foreta elektroniske betalinger](payables-how-export-payments-bank-file.md)|
|Utfør elektroniske betalinger i henhold til standarden for EU SEPA-kredittoverføring.|[Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Betal leverandøren kontant eller med sjekk, og bokfør betalingen når du bokfører selve fakturaen. |[Gjøre opp kjøpsfakturaer omgående](finance-how-to-settle-purchase-invoices-promptly.md) |
|Refunder de ansatte for personlige utgifter under firmaaktiviteter ved å betale dem på deres bankkontoer.|[Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md)|
| Du kan sørge for at at banken bare fjerner validerte sjekker og beløp ved å sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling. |[Eksportere en Positive Pay-fil](finance-how-positive-pay.md) |

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

