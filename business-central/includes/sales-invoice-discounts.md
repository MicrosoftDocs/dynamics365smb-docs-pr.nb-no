---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035791"
---
Når alle varene er registrert på ordrelinjene, kan du beregne fakturarabatten for hele salgsdokumentet ved å velge handlingen **Beregn fakturarabatt**.

Hvis **Beregn fakturarabatt**-feltet er valgt i vinduet **Oppsett av kunde- og leverandørkonto**, beregnes fakturarabatten automatisk når du gjør et av følgende på et salgsdokument:

* Vis statistikk
* Vis en testrapport
* Skriv ut
* Post

Rabatten fordeles på alle linjene i salgsdokumentet for varer, forutsatt at det står **Ja** i feltet **Tillat fakturarabatt** på ordrelinjen. Dette er standardinnstillingen for varer.

Fakturarabattbetingelsene er definert på siden **Kundefakturarabatter** til å beregne fakturarabatt. Valutakoden på salgsdokumentet brukes til å finne betingelsene for fakturarabatt i den aktuelle valutaen.

Hvis fakturarabattene ikke er definert i fremmed valuta, er fakturarabattbetingelsene definert på siden **Kundefakturarabatt** med beløpene i lokal valuta, og valutakursen på bokføringsdatoen i salgsdokumentet til å beregne fakturarabatten i fremmed valuta.
