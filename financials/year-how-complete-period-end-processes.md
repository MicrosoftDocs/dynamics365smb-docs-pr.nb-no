---
title: Avslutte perioder| Microsoft-dokumentasjon
description: "Forklarer prosessene som må fullføres for å avslutte en periode."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 03/21/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d0af3dbc94c32447facfbd24747ddc140cc1691
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="closing-periods"></a>Avslutte perioder
[!INCLUDE[d365fin](includes/d365fin_md.md)] tvinger deg ikke å lukke perioder, men det er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre. Dette emnet gir en oversikt over valgfrie prosesser og aktiviteter for lukking av perioder.  

## <a name="general-ledger"></a>Finans
* Angi systemomfattende og brukerspesifikke bokføringsperioder.  

    Dette angir datoene som bokføringer som er tillatt mellom. Avhengig av forretningsbehovene vil du kanskje tillate bokføring ved begynnelsen av perioden eller mot slutten. Hvis du vil ha mer informasjon, kan du se [Angi bokføringsperioder](finance-how-specify-posting-periods.md).  
* Foreta alle nødvendige finansjusteringer.  
* Oppdater og bokfør gjentakelseskladder.  
  <!--* Process Consolidations-->
* Kjør kontoskjemaer som følger:  
  * Åpne **Kontoskjema**-vinduet, og klikk handlingen **Skriv ut**.  

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

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a>Beregn og behandle mva.
* Fullfør mva-oppgaver.  

## <a name="see-also"></a>Se også
[Avslutt år og perioder](year-close-years-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

