---
title: Definere økonomiske prosesser
description: Få informasjon om oppgavene som kreves for å konfigurere finans i virksomheten slik at alle regnskaps-, revisjons- og bokføringsbehov dekkes.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: f0112cfb60321a44d833ad6a51db209a71494bf1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513942"
---
# <a name="setting-up-finance"></a>Konfigurere finans
Før du kan begynne å drive selskapet, må du angi regler og standarder for hvordan du vil administrere økonomiprosessene for dette selskapet. Du starter ved å definere de viktigste regnskapspostene i selskapet - kontoplanen. Deretter definerer du bokføringsgrupper, som gjør prosessen ved å tilordne standard bokføringsfinanskonti til kunder, leverandører og varer mer effektiv.

Noen finansoppsett kan utføres automatisk med assisterte oppsettsveiledninger, og noen må gjøres manuelt. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md). Siden **Finansoppsett** angir hvordan du håndterer mange ulike regnskapssaker i firmaet. Du kan for eksempel bruke siden til å angi detaljopplysninger om fakturaavrunding, valutakode for lokal valuta, adresseformater, og om du vil bruke en tilleggsrapporteringsvaluta. Hvis du vil ha mer informasjon, kan du se [Forstå finans og kontoplanen](finance-general-ledger.md).  

Du kan bruke dimensjoner for å legge til forskjellige typer informasjon for hver transaksjon. Du kan definere selskapets grunnleggende dimensjoner, for eksempel *prosjekter* og *avdelinger*. Senere kan du legge til flere dimensjoner når du trenger dem, og du kan definere midlertidige dimensjoner for bruk under et begrenset tidsrom, for eksempel i forbindelse med en salgskampanje. Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).

Mange av konfigureringsoppgavene må fullføres før du kan å registrere finanstransaksjoner, men de fleste innstillingene kan endres på et senere tidspunkt. Noen av oppsettsoppgavene er valgfrie. Du kan for eksempel bare definere konserninterne bokføringer og konsolideringer hvis du arbeider med flere selskaper. Noen oppsettsoppgaver, for eksempel angivelse av perioden der bokføring er tillatt, må kanskje gjentas med jevne mellomrom.  

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
|Vis eller rediger finanskontoene som alle finansposter bokføres til|[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)|
| Angi hvordan du vil betales av kunder, og hvordan du vil betale leverandørene. |[Definer betalingsmåter](finance-payment-methods.md) |
| Definer betalingsbetingelser for å håndtere forfallsdatoer og beregne mulige kontantrabatter.|[Definere betalingsbetingelser](finance-payment-terms.md) |
| Angi bokføringsgruppene som tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. |[Definer bokføringsgrupper](finance-posting-groups.md)|
|Opprette kontoskjemaer og definere kontokategorier for å angi innholdet i økonomiske diagrammer og rapporter, for eksempel balanse- og resultatregnskapsrapporter.|[Klargjøre finansrapportering med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md)|
|Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.|[Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Definere regnskapsperioder. |[Arbeide med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md) |
|Definer purrebetingelser som hjelper deg med å samle inn forfalte betalinger.|[Definer betingelser og grader for purringer](finance-setup-reminders.md)|
| Definere hvordan du rapporterer merverdiavgiftsbeløp du har innkrevd for salg, til skattemyndighetene. |[Definere merverdiavgift (mva)](finance-setup-vat.md)|
|Klargjør for å håndtere urealisert mva i forbindelse med kontantbaserte regnskapsmetoder.|[Definere urealisert merverdiavgift for kontantbasert regnskap](finance-setup-unrealized-vat.md)|
|Definere utenlandsk valuta du kan handle med eller rapportere transaksjoner i.|[Definer valutaer](finance-set-up-currencies.md)|
| Angi funksjoner for salg og kjøp til å håndtere betalinger i fremmed valuta.|[Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definer én eller flere flere valutaer, slik at beløpene rapporteres automatisk i både LV og en tilleggsrapporteringsvaluta i hver finanspost og andre poster.|[Definere en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)|
|Juster tilleggsvalutaangivelser periodisk for å utligne varierende valutakurser.|[Oppdatere valutakurser](finance-how-update-currencies.md)|
|Definer flere rentesatser som skal brukes for forskjellige perioder for forsinkede betalinger handelstransaksjoner.|[Angi flere rentesatser.](finance-how-to-set-up-multiple-interest-rates.md)|
|Klargjør for å runde av fakturabeløp automatisk når du oppretter fakturaer.|[Definere rakturaavrunding](finance-set-up-invoice-rounding.md)|
| Legg til nye kontoer i den eksisterende kontoplanen. |[Definere kontoplanen](finance-setup-chart-accounts.md) |
| Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm. |[Definere kontantstrømanalyse](finance-setup-cash-flow-analyses.md) |
|Aktiver fakturering av en kunde som ikke er definert i systemet.|[Definere kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Definere Intrastat-rapportering, og send inn rapporten til myndighetene | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md)|
|Sørg for at en post i en finanskladd fordeles til flere forskjellige konti når du bokfører kladden, enten antall, prosent eller beløp.|[Bruke fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md)|
|Definere kildekoder og årsakskoder som du kan bruke til å spore revisjonsspor|[Definere kildespor og årsaksspor for revisjonsspor](finance-setup-trail-codes.md)|
|Angi standardrapporter som skal brukes for ulike dokumenttyper.|[Rapportvalg i Business Central](across-report-selections.md)|

> [!TIP]
> Avhengig av den geografiske plasseringen din kan enkelte sider inneholde felt som ikke er beskrevet i artiklene som er oppført her, fordi de gjelder for lokale funksjoner eller tilpasninger. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analyser kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]