---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed62e60d3b5b1af2158d8adc6c411884ea4c12aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133579"
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
