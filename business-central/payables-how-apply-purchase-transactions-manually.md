---
title: Avstem leverandørbetalingsmottak eller refusjoner i utbetalingskladden
description: Hvis du vil behandle eller avstemme leverandørbetalinger eller refusjoner manuelt, utligner du beløpet mot én eller flere åpne leverandørposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.search.form: 62, 233, 522, 623
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2be99ab30035a96d7c7d631caa84276d50a42b3e
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953287"
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter
Når du sender en betaling eller mottar en refusjon fra en leverandør, må du bestemme om du vil utligne betalingen eller refundere til én eller flere åpne poster. Du kan angi det nøyaktige beløpet du vil utligne mot, kvitteringen eller refusjonen, og deretter bare delvis utligne leverandørposter. Du må utligne alle leverandørposter for å få riktig leverandørstatistikk og riktige rapporter av kontoutdrag og rentenotaer.

> [!NOTE]  
>   Leverandører kan noen ganger gi en betalingsrefusjon i stedet for en kreditnota som motregnes mot fremtidige fakturaer, spesielt i tilfeller der du returnerer varer du allerede har betalt for, eller når du har betalt for mye for en faktura.

Du kan utligne leverandørposter på tre forskjellige måter:

* Ved å skrive inn informasjon på dedikerte sider, for eksempel **Betalingskladd** og **Betalingsavstemmingskladd**.
* Fra kjøpskreditnotadokumenter.
* Fra leverandørposter etter at kjøpsdokumenter er postert, men ikke utlignet.

> [!NOTE]  
>   Hvis **Utligningsmetode**-feltet på leverandørkortet inneholder **Saldo**, utlignes betalinger automatisk mot den eldste åpne kreditposten hvis du ikke manuelt angir hvilken post som det skal utlignes mot. Hvis utligningsmetoden for en kunde er **Manuelt**, må du deretter utligne poster manuelt.

Du kan utligne leverandørbetalinger manuelt til de relaterte kjøpsdokumentene når du bokfører betalinger på siden **Betalingskladd**. Hvis du vil ha informasjon om utfylling betalingsjournalen, kan du se [Utføre betalinger](payables-make-payments.md).

Du kan også utligne leverandørbetalinger og kundebetalinger etter at betalingene vises som negative banktransaksjoner i banken. På siden **Betalingsavstemmingskladd** kan du bruke funksjonene for bankkontoutdragsimport, automatisk utligning og bankkontoavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Utligne en betaling mot en eller flere leverandørposter
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladd** og velg den relaterte koblingen.
2. På siden **Betalingskladd**, på den første kladdelinjen, angir du aktuelle opplysninger om betalingsposten.
3. Utligne én enkelt leverandørpost:
   1. I feltet **Utligningsbilagsnr.** velger du feltet for å åpne siden **Utlign leverandørposter**.
   2. Velg posten som betalingen skal utlignes mot, på siden **Utlign leverandørposter**.
   3. På linjen i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for posten.
4. Du kan også utligne flere leverandørposter:

   1. Velg handlingen **Utlign poster**.
   2. Velg linjene med postene som betalingen skal utlignes mot, på siden **Utlign levrd.poster**.
   3. Velg handlingen **Angi utlignings-ID**.  
   4. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post.

      Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet automatisk. Nederst på siden **Utlign leverandørposter** kan du se det spesifikke beløpet i feltet Utlignet beløp, og også om utligningen går i balanse.
5. Velg **OK**.
6. Velg handlingen **Bokfør** for å bokføre betalingskladden.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Utligne en kreditnota mot en eller flere leverandørposter
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpskreditnota**, og velg deretter den relaterte koblingen.
2. Åpne kjøpskreditnotaen du vil utligne.
3. Skriv inn relevant informasjon i hodet.
4. For å utligne en enkelt leverandørpost, på hurtigfanen **Utligning** i feltet **Utligningsbilagsnr.** velger du posten som kreditten skal utlignes til, og deretter, i feltet **Beløp som skal utlignes** angir du beløpet som skal utlignes til posten.
5. Du kan også utligne flere leverandørposter:

   1. Velg handlingen **Utlign poster**.
   2. Velg linjene med postene du vil utligne kreditnotaen mot.
   3. Velg handlingen **Angi utlignings-ID**.  
   4. På hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post.

       Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet automatisk. Nederst på siden **Utlign leverandørposter** kan du se det spesifikke beløpet i feltet **Utlignet beløp**, og også om utligningen går i balanse.
6. Velg **OK**.  
   Siden **Kjøpskreditnota** viser posten du har valgt, som du registrerte i feltene **Utligningsbilagstype** og **Utligningsbilagsnr.** Siden viser også beløpet på kreditnotaen som skal bokføres, utlignet for eventuelle betalingsrabatter.
7. Velg **Bokfør**-knappen for å bokføre kjøpskreditnotaen.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Slik utligner du bokførte leverandørposter
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne den aktuelle leverandøren med poster som allerede er bokført.
3. Velg handlingen **Poster**, og velg deretter handlingen **Utlign poster**.
4. De åpne postene for leverandøren vises på siden **Utlign levrd.poster**.
5. Velg linjen med posten som skal utlignes.
6. Velg handlingen **Angi utlignings-ID**.

    Feltet **Utlignings-ID** viser tre stjerner hvis du arbeider i et system for enkelt bruker, eller bruker-ID-en din hvis du arbeider i et flerbrukersystem.  
7. For hver linje i feltet **Beløp som skal utlignes** skriver du inn beløpet du vil utligne for hver enkelt post.

    Hvis du ikke registrerer et beløp, utlignes maksimumsbeløpet automatisk. Nederst på siden **Utlign leverandørposter** kan du se beløpet i feltet **Utlignet beløp**.
8. Velg handlingen **Etterutligne**.  

    Siden **Etterutligne** åpnes med dokumentnummeret for utligningsposten og bokføringsdatoen for posten med den seneste bokføringsdatoen.
9. Velg **OK** for å bokføre applikasjonen.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Slik utligner du leverandørposter i forskjellige valutaer mot hverandre
Hvis du kjøper fra en leverandør i én valuta og betaler i en annen valuta, kan du likevel utligne fakturaen mot betalingen.

Hvis du utligner en post (post 1) i én valuta mot en post (post 2) i en annen valuta, brukes bokføringsdatoen i post 1 til å søke etter den relevante valutakursen for å konvertere beløp i post 2. Den relevante valutakursen finnes på **Valutakurser**-siden. I så fall må du aktivere utligning av leverandørposter i forskjellige valutaer. Hvis du vil ha mer informasjon, kan du se [Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladd** og velg den relaterte koblingen.
2. Åpne kladden du vil bruke, og fyll ut den første tomme kladdelinjen med en valutakode.
3. Velg handlingen **Utlign poster**.
4. Velg linjen med posten du vil utligne mot posten i betalingskladden. Deretter velger du handlingen **Angi utlignings-ID** og merker posten du vil utligne mot.
5. Velg **OK** for å gå tilbake til utbetalingskladden.
6. Bokfør utbetalingskladden.

> [!IMPORTANT]  
>   Når du utligner poster i ulike valutaer mot hverandre, konverteres postene til USD. Selv om valutakursene for de to aktuelle valutaene er fast, for eksempel mellom USD og EUR, kan det oppstå et lite restbeløp når disse beløpene i fremmed valuta omregnes til USD. Disse små restbeløpene bokføres som agio eller disagio for kontoen som er spesifisert i feltet **Konto for realisert agio** eller **Konto for realisert disagio** på siden **Valutaer**. Feltet **Beløp (USD)** justeres også i de aktuelle leverandørpostene.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Oppheve utligning av utlignede leverandørposter
Når du opphever utligningen for en feilaktig utligning, opprettes og bokføres korreksjonsposter (poster som er identiske med de opprinnelige postene, men som har motsatt fortegn i beløpsfeltet) for alle poster, inkludert alle finansbokføringer som er avledet fra utligningen, for eksempel betalingsrabatt og valutagevinst/-tap. Postene som ble lukket av utligningen, åpnes på nytt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne det aktuelle leverandørkortet.
3. Velg handlingen **Poster**.
4. Velg den relevante posten, og velg deretter handlingen **Opphev utligning**.
5. Du kan også velge handlingen **Detaljert post**.
6. Velg utligningsposten, og velg deretter handlingen **Opphev utligning**.
7. Fyll ut feltene i hodet, og klikk deretter handlingen **Opphev utligning**.

> [!IMPORTANT]  
>   Hvis en post er utlignet av mer enn én utligningspost, må du oppheve utligningen av den seneste utligningsposten først.

## <a name="see-also"></a>Se også
[Kjøp](payables-manage-payables.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]