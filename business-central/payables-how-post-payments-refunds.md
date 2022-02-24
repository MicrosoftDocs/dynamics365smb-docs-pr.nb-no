---
title: Utligne betalinger mot dokumenter og bokføre dem | Microsoft Docs
description: Beskriver hvordan du registrerer betalinger du gjør til leverandører og refusjoner du gjør til kunder.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: a35dc8fb1bd6725d4c1f62d387408234f7419b74
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076976"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Registrere betalinger og refusjoner i utbetalingskladden

På siden **Utbetalingskladd** registrerer du betalinger du gjør til leverandører og refusjoner du gjør til kunder. Når du bokfører en utbetalingskladdelinje, registreres det betalte beløpet på den angitte systembankkontoen. Deretter må du utføre trinnene for å foreta den faktiske pengeoverføringen fra den aktuelle bankkontoen.  

Utbetalingskladden er en finanskladd som er tilpasset for betalinger. Du kan raskt legge til linjer manuelt, du kan la [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå leverandørbetalinger, og du kan utligne betalingen mot bokførte dokumenter. Selv om du foretar betalinger, kan du angi et positivt beløp i feltet **Dokumentbeløp**. Avhengig av dokumenttypen for kladdelinjen konverteres dette beløpet deretter til et negativt beløp i de underliggende transaksjonene. På denne måten er det raskere for deg å legge til kladdelinjene manuelt. Hvis du foretrekker å angi negative beløp, kan du tilpasse utbetalingskladden til å vise feltet **Beløp** i stedet.  

- Utligne betalinger mot fakturaer eller kreditnotaer

    Hvis du fyller ut feltet **Utligningsbilagsnr.** med fakturaen eller kreditnotaen som skal betales eller refunderes, settes det aktuelle dokumentet til betalt når du bokfører kladden. Dette omtales som «utlignet». Som et alternativ til å utligne under betalingsbokføringen, kan du bruke siden **Utlign levrd.poster** og **Utlign kundeposter** når du har utført betalingsbokføringen. Hvis du vil ha mer informasjon, kan du for eksempel se [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).  

- Hente foreslåtte betalinger til leverandører eller ansatte

    Funksjonene **Betalingsforslag - leverandør** og **Betalingsforslag - ansatt** kan hjelpe deg med å fylle ut betalingskladdelinjene automatisk i henhold til leverandørprioritering og forfallsdatoer. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md). Med denne funksjonen er **Utligningsbilagsnr.**-feltet alltid fylt ut.  

- Skrive ut sjekker og sende betalinger elektronisk til banken

    I tillegg til å registrere at betalingen er utført, kan du også bruke siden **Utbetalingskladd** for å legge ut betalingen for ytterligere behandling av banken. Hvis du vil ha mer informasjon, kan du se [Foreta sjekkbetalinger](payables-how-work-checks.md) og [Foreta elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Foreta betalinger i utbetalingskladden

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.
2. Åpne kladden som er reservert for betalinger.
3. Hvis du vet hvem du skal betale eller refundere, fyller du ut feltene manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du også vil utligne betalingen mot den tilknyttede fakturaen eller kreditnotaen, velger du **Utligningsbilagsnr.**-feltet på **Utlign levrd.poster**-siden, velger den aktuelle fakturaen eller kreditnotaen, og velger deretter **OK**-knappen.

    Mange felt som **Dokumentbeløp** og **Forfallsdato** er nå fylt ut med opplysninger fra det valgte dokumentet.
5. Du kan også bruke funksjonen **Betalingsforslag - leverandør**. Alle utligningsopplysninger og beløper angis også deretter på kladdelinjene. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).

    Meldinger hjelper deg med å fylle ut obligatoriske felt på riktig måte.
6.  Når alle utbetalingskladdelinjene er fullført, kan du velge handlingen **Bokfør**.

## <a name="see-also"></a>Se også
[Foreta sjekkbetalinger](payables-how-work-checks.md)  
[Foreta elektroniske betalinger](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
