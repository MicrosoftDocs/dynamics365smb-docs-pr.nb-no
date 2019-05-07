---
title: Definere økonomiske prosesser | Microsoft-dokumentasjon
description: Få informasjon om oppgavene for å konfigurere finans i virksomheten slik at alle regnskaps-, revisjons- og bokføringsbehov dekkes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 68128de48b014e7ca44fba3909cf72dcf0d87135
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "920418"
---
# <a name="setting-up-finance"></a>Konfigurere finans
For å få deg raskt i gang inkluderer [!INCLUDE[d365fin](includes/d365fin_md.md)] standardkonfigurasjoner for de fleste økonomiske prosesser. Hvis du vil endre konfigurasjoner til bedriften din, er det bare å fortsette. Fra Rollesenteret kan du for eksempel bruke en assistert installasjonsveiledningen til å definere mva-satsen for din plassering.  

Det er imidlertid noen ting du må definere selv. For eksempel hvis du vil bruke dimensjoner som grunnlag for forretningsanalyse.  

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Velg hvordan du betaler dine leverandører. |[Definere betalingsmåter](finance-payment-methods.md) |
| Angi bokføringsgruppene som tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. |[Definere bokføringsgrupper](finance-posting-groups.md)|
|Opprette kontoskjemaer og definere kontokategorier for å angi innholdet i økonomiske diagrammer og rapporter, for eksempel balanse- og resultatregnskapsrapporter.|[Klargjøre finansrapportering med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md)|
|Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.|[Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Definere regnskapsperioder. |[Åpne et nytt regnskapsår](finance-how-open-new-fiscal-year.md) |
| Definere hvordan du rapporterer merverdiavgiftsbeløp du har innkrevd for salg, til skattemyndighetene. |[Definere beregninger og bokføringsmetoder for merverdiavgift](finance-setup-vat.md)|
|Klargjør for å håndtere urealisert mva i forbindelse med kontantbaserte regnskapsmetoder.|[Definere urealisert merverdiavgift for kontantbasert regnskap](finance-setup-unrealized-vat.md)|
| Angi funksjoner for salg og kjøp til å håndtere betalinger i fremmed valuta.|[Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definer én eller flere flere valutaer, slik at beløpene rapporteres automatisk i både NOK og en tilleggsrapporteringsvaluta i hver finanspost og andre poster.|[Definere en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)|
|Juster tilleggsvalutaangivelser periodisk for å utligne varierende valutakurser.|[Oppdatere valutakurser](finance-how-update-currencies.md)|
|Definer flere rentesatser som skal brukes for forskjellige perioder for forsinkede betalinger handelstransaksjoner.|[Angi flere rentesatser.](finance-how-to-set-up-multiple-interest-rates.md)|
|Klargjør for å runde av fakturabeløp automatisk når du oppretter fakturaer.|[Definere rakturaavrunding](finance-set-up-invoice-rounding.md)|
| Legg til nye kontoer i den eksisterende kontoplanen. |[Definere kontoplanen](finance-setup-chart-accounts.md) |
| Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm. |[Definere kontantstrømanalyse](finance-setup-cash-flow-analyses.md) |
|Aktiver fakturering av en kunde som ikke er definert i systemet.|[Definere kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Definere Intrastat-rapportering, og send inn rapporten til myndighetene | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md)|
|Forbered rapporten konsolidert råbalanse i rollesenteret for regnskapsfører for å få en økonomisk oversikt på tvers av flere selskaper.|[Konsolidere finansielle data fra flere selskaper](finance-consolidated-company-reporting.md)|
|Sørg for at en post i en finanskladd fordeles til flere forskjellige konti når du bokfører kladden, enten antall, prosent eller beløp.|[Bruke fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md)|

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
