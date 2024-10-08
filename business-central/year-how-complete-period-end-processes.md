---
title: Valgfrie aktiviteter for avslutningsperioder
description: Denne artikkelen beskriver de valgfrie prosessene og aktivitetene for lukking av regnskapsperioder i Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments'
ms.date: 08/02/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="overview-of-tasks-to-close-accounting-periods"></a>Oversikt over oppgaver som skal lukkes regnskapsperioder

[!INCLUDE[prod_short](includes/prod_short.md)] tvinger deg imidlertid ikke til å lukke perioder, Der er mange aktiviteter ved periodeslutt (månedsslutt) du kan gjøre. Denne artikkelen gir en oversikt over valgfrie prosesser og aktiviteter for avslutningsperioder.  

## <a name="general-ledger"></a>Finans

* Angi systemomfattende og brukerspesifikke bokføringsperioder.  

    Dette angir datoene som bokføringer som er tillatt mellom. Avhengig av virksomheten vil du kanskje tillate bokføring i begynnelsen av perioden eller mot slutten. Lær mer under [Spesifiser bokføringsperioder](finance-how-specify-posting-periods.md).  
* Foreta alle nødvendige finansjusteringer.  
* Oppdater og bokfør gjentakelseskladder.  
  <!--* Process Consolidations-->
* Kjør finansrapporter på følgende måte:  
  * Åpne siden **Finansrapporter** og velg **Skriv ut**-handlingen.  

## <a name="sales-and-receivables"></a>Salg

* Bokfør alle ordrer, fakturaer, kreditnotaer og ordrereturer.  
* Bokfør alle innbetalingskladder.  
* Oppdater og bokfør gjentakelseskladder i forbindelse med salg.  
* Avstem kortsiktige fordringer mot Finans.  
* Kjør kjørselen **Slett fakturerte ordrer**.  

## <a name="purchases-and-payables"></a>Kjøp

* Bokfør alle bestillinger, fakturaer, kreditnotaer og ordrereturer.  
* Bokfør alle utbetalingskladder.  
* Oppdater og bokfør gjentakelseskladder i forbindelse med kjøp.  
* Kjør rapporten **Aldersfordelt saldoliste - lev.**, og avstem leverandørgjeld mot Finans.  
* Kjør kjørselen **Slett fakturerte bestillinger**.  

## <a name="fixed-assets"></a>Aktiva

* Bokfør all vedlikeholdskost som har blitt bokført gjennom aktivakladdene eller fakturaene.
* Bokfør justeringer.
* Bokfør oppskrivning.
* Bokfør avskrivning.
* Oppdater og bokfør gjentakende aktivakladd.

## <a name="intercompany"></a>Konserninternt

* Behandle konserninterne transaksjoner.

## <a name="calculate-and-process-sales-tax"></a>Beregn og behandle mva.

* Fullfør avgiftsoppgaver.  

## <a name="see-also"></a>Se også

[Lukk år og perioder](year-close-years-periods.md)  
[Avslutte tablåer](year-close-books.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
