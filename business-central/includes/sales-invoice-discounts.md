---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
ms.openlocfilehash: 8849f1c5d33cd1f826e7f53be317cb01e513fcd1
ms.sourcegitcommit: a9c778b65925435a4099fad45b3611f310e0b203
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9652141"
---
Når du har lagt til alle varene på linjene, kan du beregne fakturarabatten for hele salgsdokumentet ved å velge handlingen **Beregn fakturarabatt**.

Rabatten beregnes basert på alle linjer i salgsdokumentet der det er merket av for **Tillat fakturarabatt**. Fakturarabatter er som standard tillatt. Linjer med for eksempel varegebyrer tas imidlertid ikke med i beregningen av fakturarabatten. Hvis du vil bruke en rabatt på slike linjer, må du angi en verdi i feltet **Linjerabattbeløp** på linjene.  

> [!NOTE]
> Feltene **Tillat fakturarabatt** og **Linjerabattbeløp** er skjult på linjer som standard. Hvis feltene ikke er tilgjengelige, kan du legge dem til ved å tilpasse siden. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Hvis feltet **Beregn fakturarabatt** er valgt på siden **Salgsoppsett**, beregnes fakturarabatten automatisk. Når beregningen skjer, varierer avhengig av hvilken type salgsdokument du bruker.
>
> Hvis du bruker en ordre, beregnes rabatten når du legger til en linje. For alle andre salgsdokumenter, for eksempel salgsfakturaer, beregnes rabatten når du gjør en av følgende handlinger:
>
> * Vis statistikk
> * Vis en testrapport
> * Skriv ut
> * Post

Du definerer fakturarabattbetingelsene for en kunde på siden **Kundefakturarabatter**. Valutakoden på salgsdokumentet brukes til å finne betingelsene for fakturarabatt i den aktuelle valutaen.

Hvis du ikke har definert fakturarabatter for utenlandsk valuta, brukes rabattbetingelsene på siden **Kundefakturarabatter** til å beregne rabatten. Beregningen bruker den lokale valutaen og valutakursen som var gyldig på dokumentets bokføringsdato.
