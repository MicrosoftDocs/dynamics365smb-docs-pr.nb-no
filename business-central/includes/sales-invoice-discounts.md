---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470290"
---
Når alle varene er registrert på salgslinjene, kan du beregne fakturarabatten for hele dokumentet ved å velge handlingen **Beregn fakturarabatt**.

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
