---
title: "Utligne betalinger mot dokumenter og bokføre dem | Microsoft Docs"
description: "Beskriver hvordan du registrerer betalinger du gjør til leverandører og refusjoner du gjør til kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: nb-no
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Registrere betalinger og refusjoner
I vinduet **Utbetalingskladd** registrerer du betalinger du gjør til leverandører og refusjoner du gjør til kunder. Når du bokfører en utbetalingskladdelinje, registreres det betalte beløpet på den angitte systembankkontoen. Deretter må du utføre trinnene for å foreta den faktiske pengeoverføringen fra den aktuelle bankkontoen.

Hvis du fyller ut feltet **Utligningsbilagsnr.** med fakturaen eller kreditnotaen som skal betales eller refunderes, settes det aktuelle dokumentet til betalt når du bokfører kladden. Dette omtales som «utlignet». Som et alternativ til å utligne under betalingsbokføringen, kan du bruke vinduet **Utlign levrd.poster** og **Utlign kundeposter** når du har utført betalingsbokføringen. Hvis du vil ha mer informasjon, kan du for eksempel se [Avstemme leverandørbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).

**Betalingsforslag - leverandør**-funksjonen kan hjelpe deg med å fylle ut betalingskladdelinjene automatisk i henhold til leverandørprioritering og forfallsdatoer. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md). Med denne funksjonen er **Utligningsbilagsnr.**-feltet alltid fylt ut.

I tillegg til å registrere at betalingen er utført, kan du også bruke vinduet **Utbetalingskladd** for å legge ut betalingen for ytterligere behandling av banken. Hvis du vil ha mer informasjon, kan du se [Foreta sjekkbetalinger](payables-how-work-checks.md) og [Foreta elektroniske betalinger](payables-how-export-payments-bank-file.md).  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.
2. Åpne kladden som er reservert for betalinger.
3. Hvis du vet hvem du skal betale eller refundere, fyller du ut feltene manuelt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du også vil utligne betalingen mot den tilknyttede fakturaen eller kreditnotaen, velger du **Utligningsbilagsnr.**-feltet i **Utlign levrd.poster**-vinduet, velger den aktuelle fakturaen eller kreditnotaen, og velger deretter **OK**-knappen.

    Mange felt som **Beløp** og **Forfallsdato** er nå fylt ut med opplysninger fra det valgte dokumentet.
5. Du kan også bruke funksjonen **Betalingsforslag - leverandør**. Alle utligningsopplysninger og beløper angis også deretter på kladdelinjene. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).

    Meldinger hjelper deg med å fylle ut obligatoriske felt på riktig måte.
6.  Når alle utbetalingskladdelinjene er fullført, kan du velge handlingen **Bokfør**.

## <a name="see-also"></a>Se også
[Foreta sjekkbetalinger](payables-how-work-checks.md)  
[Foreta elektroniske betalinger](payables-how-export-payments-bank-file.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

