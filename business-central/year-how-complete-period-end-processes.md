---
title: Valgfrie aktiviteter for lukking av perioder | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av regnskapsperioder i Business Central.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 104f63e07e4bfd8945f73581a4fb7810f946304f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755570"
---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Oversikt over oppgaver for lukking av regnskapsperioder
[!INCLUDE[prod_short](includes/prod_short.md)] tvinger deg ikke å lukke perioder, men det er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre. Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av perioder.  

## <a name="general-ledger"></a>Finans
* Angi systemomfattende og brukerspesifikke bokføringsperioder.  

    Dette angir datoene som bokføringer som er tillatt mellom. Avhengig av forretningsbehovene vil du kanskje tillate bokføring ved begynnelsen av perioden eller mot slutten. Hvis du vil ha mer informasjon, kan du se [Angi bokføringsperioder](finance-how-specify-posting-periods.md).  
* Foreta alle nødvendige finansjusteringer.  
* Oppdater og bokfør gjentakelseskladder.  
  <!--* Process Consolidations-->
* Kjør kontoskjemaer som følger:  
  * Åpne **Kontoskjema**-siden, og velg deretter handlingen **Skriv ut**.  

## <a name="sales-and-receivables"></a>Salg
* Bokfør alle ordrer, fakturaer, kreditnotaer og ordrereturer.  
* Bokfør alle innbetalingskladder.  
* Oppdater og bokfør gjentakelseskladder som er relatert til salg.  
* Avstem kortsiktige fordringer mot Finans.  
* Kjør kjørselen **Slett fakturerte ordrer**.  

## <a name="purchases-and-payables"></a>Kjøp
* Bokfør alle bestillinger, fakturaer, kreditnotaer og ordrereturer.  
* Bokfør alle utbetalingskladder.  
* Oppdater og bokfør gjentakelseskladder som er relatert til kjøp.  
* Kjør rapporten **Aldersfordelt saldoliste - lev.**, og avstem leverandørgjeld mot Finans.  
* Kjør kjørselen **Slett fakturerte bestillinger**.  

Anleggsmidler
* Bokfør all vedlikeholdskost gjennom aktivakladdene eller fakturaene.
* Bokfør justeringer.
* Bokfør oppskrivning.
* Bokfør avskrivning.
* Oppdater og bokfør gjentakende aktivakladd.

Konsernintern
* Behandle konserninterne transaksjoner

## <a name="calculate-and-process-sales-tax"></a>Beregn og behandle mva.
* Fullfør mva-oppgaver.  

## <a name="see-also"></a>Se også
[Avslutte år og perioder](year-close-years-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]