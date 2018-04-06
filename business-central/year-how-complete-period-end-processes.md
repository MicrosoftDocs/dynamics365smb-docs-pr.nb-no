---
title: Valgfrie aktiviteter for lukking av perioder | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av regnskapsperioder i Business Central.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42b5729d5d4013476fa0ff460db4dc999e629d66
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a>Oversikt over oppgaver for lukking av regnskapsperioder
[!INCLUDE[d365fin](includes/d365fin_md.md)] tvinger deg ikke å lukke perioder, men det er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre. Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av perioder.  

## <a name="general-ledger"></a>Finans
* Angi systemomfattende og brukerspesifikke bokføringsperioder.  

    Dette angir datoene som bokføringer som er tillatt mellom. Avhengig av forretningsbehovene vil du kanskje tillate bokføring ved begynnelsen av perioden eller mot slutten. Hvis du vil ha mer informasjon, kan du se [Angi bokføringsperioder](finance-how-specify-posting-periods.md).  
* Foreta alle nødvendige finansjusteringer.  
* Oppdater og bokfør gjentakelseskladder.  
  <!--* Process Consolidations-->
* Kjør kontoskjemaer som følger:  
  * Åpne **Kontoskjema**-vinduet, og velg deretter handlingen **Skriv ut**.  

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
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

