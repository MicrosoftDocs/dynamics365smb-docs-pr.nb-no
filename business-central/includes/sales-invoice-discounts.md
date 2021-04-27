---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778650"
---
Når alle varene er registrert som salgslinjer, kan du beregne fakturarabatten for hele salgsdokumentet ved å velge handlingen **Beregn fakturarabatt**.

Rabatten beregnes basert på alle linjene i salgsdokumentet for varer, forutsatt at det står **Ja** i feltet **Tillat fakturarabatt** på ordrelinjen. Dette er standardinnstillingen for varer. Linjer med for eksempel varegebyrer tas ikke med i beregningen av fakturarabatten. Hvis du vil bruke en rabatt på slike linjer, må du angi feltet **Linjerabatt-%** på de aktuelle linjene.  

> [!TIP]
> Hvis **Beregn fakturarabatt**-feltet er valgt på siden **Oppsett av kunde- og leverandørkonto**, beregnes fakturarabatten automatisk når du gjør et av følgende på et salgsdokument:
>
> * Vis statistikk
> * Vis en testrapport
> * Skriv ut
> * Post

Fakturarabattbetingelsene for en kunde er definert på siden **Kundefakturarabatter** for kunden. Valutakoden på salgsdokumentet brukes til å finne betingelsene for fakturarabatt i den aktuelle valutaen.

Hvis fakturarabattene ikke er definert i fremmed valuta, er fakturarabattbetingelsene definert på siden **Kundefakturarabatt** med beløpene i lokal valuta, og valutakursen på bokføringsdatoen i salgsdokumentet til å beregne fakturarabatten i fremmed valuta.
