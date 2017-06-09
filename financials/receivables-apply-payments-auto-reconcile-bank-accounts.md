---
title: Utligne betalinger automatisk og avstemme bankkonti| Microsoft-dokumentasjon
description: Bruke betalinger automatisk og avstemme bankkonti
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0c56da9bc395ed16a5be223e65c9e9594e643993
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="apply-payments-automatically-and-reconcile-bank-accounts"></a>Bruke betalinger automatisk og avstemme bankkonti
Du må regelmessig avstemme bankkontoene og samlekontoene for kunder og leverandører ved å utligne betalinger som er registrert på bankkontoen, mot de tilknyttede ubetalte fakturaene og kreditnotaene eller andre åpne poster i [!INCLUDE[d365fin](includes/d365fin_long_md.md)].  

Du kan utføre denne oppgaven i vinduet **Betalingsavstemmingskladd** ved å importere en bankkontoutdragsfil eller feed for hurtig å registrere betalinger. Betalinger brukes til å åpne kunde- eller leverandørpostoppføringer basert på sammenligninger mellom betalingstekst og oppføringsinformasjon. Du kan se gjennom og endre automatiske utligninger før du bokfører kladden. Du kan velge å lukke alle åpne bankposter relatert til de utlignede postene når du bokfører kladden. Bankkontoen avstemmes automatisk når alle betalinger er utlignet.  

Hvis du vil importere bankkontoutdrag som en bankfeed, må du først konfigurere og aktivere bankfeedtjenesten Envestnet Yodlee og deretter knytte bankkontoene til relaterte nettbankkonti. Hvis du vil ha mer informasjon, kan du se [Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  

Du kan også bruke konverteringstjenesten for bankdata til å konvertere en bankkontoutdragsfil fra hvilket som helst format, til en datastrøm du kan importere til [!INCLUDE[d365fin](includes/d365fin_long_md.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurere konverteringstjenesten for bankdata](bank-how-setup-bank-data-conversion-service.md)  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

| Hvis du vil | Se |
| --- | --- |
| Utligne betalinger mot åpne kunde- eller leverandørposter ved å importere et bankkontoutd, og avstemme bankkontoen når alle betalingene er utlignet. |[Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md) |
| Utlign betalinger manuelt ved å vise detaljert informasjon om samsvarende data og forslag til åpne kandidatposter som betalinger kan utlignes mot. |[Se gjennom eller utligne betalinger etter automatisk utligning](receivables-how-review-apply-payments-auto-application.md) |
| Løse betalinger som ikke kan brukes automatisk på de tilknyttede åpne postene. For eksempel fordi beløpene er forskjellige, eller fordi en relatert post ikke finnes. |[Avstemme betalinger som ikke kan utlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Koble tekst på betalinger til bestemte kunde-, leverandør- eller finanskontoer for alltid å bokføre gjentakende innbetalinger eller utgifter på disse kontoene når det ikke finnes noen dokumenter å utligne dem på. |[Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

