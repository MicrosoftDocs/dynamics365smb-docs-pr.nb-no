---
title: Avstem bankkontoer og utlign betalinger
description: Gir en oversikt over oppgaver for å avstemme bank- og samlekontiene, bokføre innbetalinger og utgifter og utligne betalinger automatisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.search.form: 1290, 1291, 1293, 1294
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 12da473253ff3c494ec2c63e4fbfc32aedd5d1f9
ms.sourcegitcommit: f4b32ba1f926a2a712400c36305616f320757723
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/08/2022
ms.locfileid: "8101220"
---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a>Utligne betalinger automatisk og avstemme bankkonti
Du må regelmessig avstemme bankkontoene og samlekontoene for kunder og leverandører ved å utligne betalinger som er registrert på bankkontoen, mot de tilknyttede åpne (ubetalte) fakturaene og kreditnotaene eller andre åpne poster i [!INCLUDE[prod_short](includes/prod_short.md)].  

Du kan utføre denne oppgaven på siden **Betalingsavstemmingskladd**, for eksempel ved å importere en bankkontoutdragsfil eller feed for hurtig å registrere betalinger. Betalinger brukes til å åpne kunde- eller leverandørpostoppføringer basert på sammenligninger mellom betalingstekst og oppføringsinformasjon. Du kan se gjennom og endre automatiske utligninger før du bokfører kladden. Du kan velge å lukke alle åpne bankposter relatert til de utlignede postene når du bokfører kladden. Bankkontoen avstemmes automatisk når alle betalinger er utlignet.

Logikken som styrer hvordan betalingstekst automatisk sammenlignes med oppføringsinformasjon, defineres på siden **Betalingsutligningsregler** som en rekke prioriterte regler du kan redigere.

Du kan også avstemme bankkonti uten å utligne betalinger samtidig. Du kan gjøre dette på siden **Bankkontoavstemming**. Hvis du vil ha mer informasjon, kan du se [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).   

Hvis du vil importere bankkontoutdrag som en bankfeed, må du først konfigurere og aktivere tjenesten Envestnet Yodlee Bank Feeds og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Du kan også importere bankkontoutdragsfiler i komma- eller semikolondelt format (.CSV). Bruk veiviseren **Definer et filformat for bankkontoutdrag** for assistert installasjon til å definere importformater for bankkontoutdrag og knytte formatet til en bankkonto. Du kan deretter bruke disse formatene når du importerer bankkontoutdrag på siden **Bankkontoavstemming**.

Du kan også bruke utvidelsen AMC Banking 365 Fundamentals til å konvertere en bankkontoutdragsfil fra hvilket som helst format, til en datastrøm du kan importere til [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Bruke AMC Banking 365 Fundamentals-utvidelsen](ui-extensions-amc-banking.md).  

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.  

| Hvis du vil | Se |
| --- | --- |
| Utligne betalinger mot åpne kunde- eller leverandørposter ved å importere et bankkontoutd, og avstemme bankkontoen når alle betalingene er utlignet. |[Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md) |
| Utlign betalinger manuelt ved å vise detaljert informasjon om samsvarende data og forslag til åpne kandidatposter som betalinger kan utlignes mot. |[Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md) |
| Løse betalinger som ikke kan brukes automatisk på de tilknyttede åpne postene. For eksempel fordi beløpene er forskjellige, eller fordi en relatert post ikke finnes. |[Avstemme betalinger som ikke kan utlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koble tekst på betalinger til bestemte kunde-, leverandør- eller finanskontoer for alltid å bokføre gjentakende innbetalinger eller utgifter på disse kontoene når det ikke finnes noen dokumenter å utligne dem på. |[Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Definer regler for å styre hvordan betalinger/banktransaksjoner skal utlignes automatisk mot de relaterte åpne finanspostene, når du bruker funksjonen **Utlign automatisk** på siden **Betalingsavstemmingskladd**.|[Definere regler for automatisk utligning av betalinger](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]