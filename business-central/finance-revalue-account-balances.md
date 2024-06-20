---
title: Revaluer finanskontosaldoer
description: Lær hvordan du revaluerer finanskontosaldoer før du produserer regnskapsoppgjørene.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# <a name="revalue-general-ledger-account-balances"></a>Revaluer finanskontosaldoer

Hvis du bruker finanskontoer til å registrere balanseposter i utenlandsk valuta, bør du revaluere kontosaldoene før du produserer regnskapsoppgjør. Valutakurser endres ofte, og revaluering bidrar til å gjøre regnskapene mer nøyaktige.

## <a name="set-up-revaluations"></a>Konfigurer revalueringer

Du definerer hver konto du vil ta med i revalueringene, på siden **Finanskort**. Du kan velge om du vil bokføre revalueringsjusteringer på realiserte eller urealiserte gevinst-/tapskontoer. Bokføring av gevinst og tap under en valutakursjustering følger vanlig bokføringsrutine. Du gjør det for eksempel for hvert oppsett på siden **Valutaer**. Hvis du vil vite mer om valutakursjusteringer, kan du gå til [Oppdater valutakurser](finance-how-update-currencies.md).

Du kan minimere feil ved å sette opp en validering for valutaene du vil tillate bokføring på individuelle finanskontoer, i feltet **Bokføring av kildevaluta**:

* Alle valutaer (tom)
* Flere valutaer
* Samme valuta
* Lokal valuta

## <a name="run-a-revaluation"></a>Kjør en revaluering

Hvis du vil revaluere beløpene i utenlandsk valuta i lokal valuta for finanskontosaldoer, bruker du handlingen **Revaluering av finansvaluta** på siden **Kontoplan** for å starte en satsjobb. Satsjobben oppretter justeringsposter i kladden du velger. Når du bokfører postene, justerer du saldoen i lokal valuta for kontoen. Finanskontosaldoer som alltid vises i lokal valuta, gjenspeiler nå endringer i valutaene som postene ble bokført i. Denne revalueringen gjør det mulig å produsere et mer nøyaktig regnskap med mindre anstrengelse.

Hvis du bruker en tilleggsrapporteringsvaluta, har revalueringspostene for finans et beløp for tilleggsrapporteringsvaluta. Beløpet som bare svarer til beløpet i lokal valuta på disse postene, ikke saldoen for tilleggsrapporteringsvalutaen på finanskontoen. Hvis du justerer kursene for tilleggsrapporteringsvalutaen etter at du har bokført justeringene, kjører du justeringen av valutakursen én gang til for å justere alle finanspostene.

> [!IMPORTANT]
> Revaluering av finanskonto oppfyller kanskje ikke alle kravene for transaksjons- og aktivaregistreringer som trenger revaluering. Eksempel: Finansobjekter, verdipapirer, leide aktiva, eller hvis du bruker dem til bestemte eller store mengder transaksjoner eller aktiva. Vi anbefaler at du diskuterer med revisor om du kan bruke funksjonen, og i så fall hvordan du bør bruke den. Hvis du for eksempel lar valutaer blandes for en konto, eller hvis du må ha en separat konto for hvert innholdselement du vil spore.

> [!NOTE]
> Revaluering gir ikke mulighet til å utligne eller oppheve utligning av poster, slik du kan med kunde- og leverandørposter. Justeringer skjer på saldo per valuta-basis.

## <a name="revaluate-accounts-vs-customer-and-vendor-exchange-rate-adjustments"></a>Revaluer kontoer kontra valutakursjusteringer for kunde og leverandør

Revaluering forenkler oppgaven med å justere finanskontosaldoer. Funksjonen evaluerer saldoen per valuta per finanskonto omtrent på samme måte som du gjør for justeringer av finanskontoer som er knyttet til bankkontoer. Hvis du bruker en finanskonto til å spore flere aktiva, bør du vurdere å bruke en leverandør eller kundekonto i stedet.

> [!NOTE]
> Revaluering av finanskonto oppfyller kanskje ikke alle kravene for transaksjons- og aktivaregistreringer som trenger revaluering. Eksempel: Finansobjekter, verdipapirer, leide aktiva, eller hvis du bruker dem til bestemte eller store mengder transaksjoner eller aktiva. Vi anbefaler at du diskuterer med revisor om du kan bruke funksjonen, og i så fall hvordan du bør bruke den. Hvis du for eksempel lar valutaer blandes for en konto, eller hvis du må ha en separat konto for hvert innholdselement du vil spore.

Eksemplene nedenfor illustrerer forskjellen mellom å bruke en finanskonto og å bruke en leverandørkonto til å spore saldoen for to monetære aktiva som bruker en utenlandsk valuta.

**Bruk en finanskonto** Hvis du bruker én finanskonto til å spore flere aktiva (f.eks. lån eller aktiva) i samme valuta, eller enkeltdeltransaksjoner for samme aktiva, men fortsatt i samme valuta, gir revaluering av finans én post per revaluering for valutaen. Dette betyr at du ikke kan spore justeringene som er knyttet til enkeltaktiva eller enkelttransaksjoner for det samme aktivumet.

**Bruk en leverandørkonto** Hvis du definerer flere aktiva som leverandører og bokfører transaksjoner til dem, enten i samme eller forskjellige valutaer, får du en justering per valuta per leverandør. Hvis du aktiverer veksleknappen **Bokføring per post** i prosjektkøposten **Juster valutakurs**, får du en justeringspost for hver enkelt leverandørpost.

Denne forskjellen er viktig når du vurderer om finansrevaluering er den riktige funksjonen for deg for rapporteringsbehovene dine.

> [!TIP]
> Vi anbefaler at du spør regnskapsføreren eller revisoren om hvilken type konto som er best for din virksomhet. Det kan også være en app for [!INCLUDE [prod_short](includes/prod_short.md)] på [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) som passer dine forretningsscenarioer.

## <a name="see-also"></a>Se også

[Gå gjennom beløp i finanskontoer](finance-review-accounts.md)  
[Forstå Finans og kontoplanen](finance-general-ledger.md)  
