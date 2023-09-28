---
title: Definere økonomiske prosesser
description: 'Få informasjon om oppgavene som kreves for å konfigurere finans i virksomheten slik at alle regnskaps-, revisjons- og bokføringsbehov dekkes.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.date: 08/19/2022
ms.author: bholtorf
---
# Konfigurere finans

Før du kan begynne å drive selskapet, må du angi hvordan du vil administrere økonomiprosessene for selskapet. Først angir du de viktigste regnskapspostene i selskapet: kontoplanen. Deretter definerer du bokføringsgrupper, som gjør prosessen ved å tilordne standard bokføringsfinanskonti til kunder, leverandører og varer mer effektiv.

Noen finansoppsett kan utføres automatisk med assisterte oppsettsveiledninger, og noen må gjøres manuelt. Finn ut mer under [Bli klar til å gjøre forretninger](ui-get-ready-business.md). Siden **Finansoppsett** angir hvordan du håndterer selskapet ulike regnskapsprosesser. Du kan for eksempel bruke siden til å angi detaljopplysninger om fakturaavrunding, valutakode for lokal valuta, adresseformater, og om du vil bruke en tilleggsrapporteringsvaluta. Finn ut mer under [Forstå finans og kontoplan](finance-general-ledger.md).  

Du kan bruke dimensjoner for å legge til forskjellige typer informasjon for hver transaksjon. Du kan definere selskapets grunnleggende dimensjoner, for eksempel *prosjekter* og *avdelinger*. Senere kan du legge til flere dimensjoner når du trenger dem. Du kan for eksempel definere midlertidige dimensjoner som skal brukes i en begrenset tidsperiode, for eksempel under en salgskampanje. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Mange av konfigureringsoppgavene må fullføres før du kan å registrere finanstransaksjoner, men de fleste innstillingene kan justeres etter behov. Det er imidlertid valgfrie oppsettoppgaver også. Det kan for eksempel hende at du bare trenger å definere konserninterne bokføringer og konsolideringer hvis du arbeider med flere selskaper. Andre oppsettsoppgaver, for eksempel angivelse av perioden der bokføring er tillatt, må kanskje gjentas med jevne mellomrom.  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Til | Se |
| --- | --- |
|Vis eller rediger finanskontoene som alle finansposter bokføres til|[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)|
| Angi hvordan du vil betales av kunder, og hvordan du vil betale leverandørene. |[Definer betalingsmåter](finance-payment-methods.md) |
| Definer betalingsbetingelser for å håndtere forfallsdatoer og beregne mulige kontantrabatter.|[Definer betalingsbetingelser](finance-payment-terms.md) |
| Angi bokføringsgruppene som tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. |[Definer bokføringsgrupper](finance-posting-groups.md)|
|Opprett finansrapporter og definere kontokategorier som bestemmer innholdet i økonomiske diagrammer og rapporter, for eksempel balanse- og resultatregnskapsrapporter.|[Klargjøre Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md)|
|Definer en toleranse som avslutter systemet en faktura etter, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen.|[Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Definere regnskapsperioder. |[Arbeide med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md) |
|Definer fakturabetingelser som minner kundene på å betale.|[Definer betingelser og grader for purringer](finance-setup-reminders.md)|
| Definere hvordan du rapporterer merverdiavgiftsbeløp (mva.) du har innkrevd for salg, til skattemyndighetene. |[Definere merverdiavgift (mva)](finance-setup-vat.md)|
|Klargjør for å håndtere urealisert mva i forbindelse med kontantbaserte regnskapsmetoder.|[Definer urealisert merverdiavgift for kontantbasert regnskap](finance-setup-unrealized-vat.md)|
|Definere utenlandsk valuta du kan handle med eller rapportere transaksjoner i.|[Definer valutaer](finance-set-up-currencies.md)|
| Angi funksjoner for salg og kjøp til å håndtere betalinger i fremmed valuta.|[Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md)
|Definer én eller flere flere valutaer, slik at beløpene rapporteres automatisk i både lokal valuta (LV) og en tilleggsrapporteringsvaluta i hver finanspost og andre poster.|[Definer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)|
|Juster tilleggsvalutaangivelser periodisk for å utligne varierende valutakurser.|[Oppdater valutakurser](finance-how-update-currencies.md)|
|Definer flere rentesatser som skal brukes for forskjellige perioder for forsinkede betalinger handelstransaksjoner.|[Angi flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md)|
|Ordne beløp som skal avrundes automatisk etter hvert som fakturaene opprettes.|[Definere fakturaavrunding](finance-set-up-invoice-rounding.md)|
| Legg til nye kontoer i den eksisterende kontoplanen. |[Definere kontoplanen](finance-setup-chart-accounts.md) |
| Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm. |[Definer kontantstrømanalyse](finance-setup-cash-flow-analyses.md) |
|Aktiver fakturering av en kunde som ikke er definert i systemet.|[Definer kontantkunder](finance-how-to-set-up-cash-customers.md)|
| Definer Intrastat-rapportering, og send inn rapporten til myndighetene. | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md)|
|Sørg for at en journalpost fordeles mellom forskjellige kontoer som antall, prosent eller beløp når du bokfører den i journalen.|[Bruk fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md)|
|Definer kildekoder og årsakskoder for å bidra til å spore revisjonsspor.|[Definere kildespor og årsaksspor for revisjonsspor](finance-setup-trail-codes.md)|
|Angi standardrapporter som skal brukes for ulike dokumenttyper.|[Rapportvalg i Business Central](across-report-selections.md)|

> [!TIP]
> Avhengig av den geografiske plasseringen din kan enkelte Business Central-sider inneholde felter som ikke er beskrevet i artiklene ovenfor, fordi de gjelder lokale funksjoner eller tilpasninger. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## Se også

[Finans](finance.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analyser kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
