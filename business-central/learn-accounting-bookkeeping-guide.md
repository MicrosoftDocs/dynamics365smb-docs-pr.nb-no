---
title: Regnskap og bokføring
description: Denne artikkelen inneholder informasjon som gjør at du kan bruke Microsoft Dynamics 365 Business Central til å utføre regnskap og bokføring for selskapet på riktig måte.
author: altotovi
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, bookkeeping'
ms.search.form: '16, 39, 108'
ms.date: 03/14/2023
ms.author: altotovi
---

# <a name="accounting-and-bookkeeping" />Regnskap og bokføring

Regnskap er en kritisk funksjon i alle ressursplanleggingsløsninger, og også i de fleste virksomheter. Regnskap representerer prosessen med å registrere og katalogisere selskapets økonomiske transaksjoner, og deretter hente, måle, oppsummere og presentere resultatene ved å bruke forskjellige rapporter som ofte kreves av lokale lover. Det primære målet ved denne prosessen er å hjelpe selskapets administrasjon med å forstå økonomien i regnskapet og måle resultatene av de økonomiske aktivitetene i selskapet.

Bokføring er en del av regnskapsprosessen og omfatter regelmessig registrering av alle finanstransaksjoner i et selskap. [!INCLUDE[prod_short](includes/prod_short.md)] er et ressursplanleggingssystem som inneholder integrerte verktøy for å gjøre bokføring enklere i systemet. Mange handlinger kan gjøres automatisk.

Denne artikkelen inneholder en oversikt over bokføringsprosesser, inkludert regler, prosedyrer og andre retningslinjer i [!INCLUDE[prod_short](includes/prod_short.md)]. Innholdet i denne artikkelen er ment å hjelpe regnskapsførere med å fullføre sine daglige oppgaver i dette ressursplanleggingssystemet. En kontekstbasert assistent er innebygd i [!INCLUDE[prod_short](includes/prod_short.md)] for ekstra hjelp. Denne assistenten inneholder koblinger til informasjon som er knyttet til nåværende side og instruksjoner for å arbeide med den aktuelle prosessen. Hvis du vil ha tilgang til den, velger du [**Hjelp**](product-help-and-support.md)-knappen øverst i høyre hjørne for å åpne ruten **Hjelp**. Deretter bruker du koblingene i delene **Om denne oppgaven eller siden** og **Relaterte ressurser fra Microsoft Learn**.

Denne videoen introduserer noen av nøkkelfunksjonene for regnskap og bokføring.

> [!Video https://www.microsoft.com/videoplayer/embed/RE4Fss4?rel=0]

Tabellen nedenfor beskriver en sekvens av oppgaver og tilbyr koblinger til artiklene som beskriver dem.

| Oppgave | Artikkel |
|------|---------|
| Vis eller rediger finanskontoene som alle finansposter bokføres til. | [Definere eller endre kontoplanen](finance-setup-chart-accounts.md) |
| Angi hvordan kundene skal betale deg, og hvordan du skal betale leverandørene. | [Konfigurer betalingsmåter:](finance-payment-methods.md) |
| Definer betalingsbetingelser for å håndtere forfallsdatoer og beregne mulige kontantrabatter. | [Konfigurer betalingsbetingelser](finance-payment-terms.md) |
| Angi bokføringsgruppene som tilordner enheter (som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter) til finanskontoer. | [Konfigurer bokføringsgrupper](finance-posting-groups.md)|
| Opprett finansrapporter og definere kontokategorier som bestemmer innholdet i økonomiske diagrammer og rapporter, for eksempel rapportene **Balanse** og **Resultatregnskap**. | [Klargjør Financial Reporting med finansdata og kontokategorier](bi-how-work-account-schedule.md)|
| Definer toleransen som systemet bruker til å avslutte en faktura, selv om betalingen, inkludert alle rabatter, ikke fullt ut dekker beløpet på fakturaen. | [Arbeid med betalingstoleranser og toleransegrenser for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Definere regnskapsperioder. | [Arbeide med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md) |
| Definer fakturabetingelser som minner kundene på å betale. | [Konfigurer påminnelsesbetingelser og -nivåer](finance-setup-reminders.md)|
| Definere hvordan du rapporterer merverdiavgiftsbeløp (mva.) som er innkrevd for salg, til skattemyndighetene. | [Konfigurer merverdiavgift (mva.)](finance-setup-vat.md) |
| Bestem hvordan du skal håndtere urealisert mva. i forbindelse med kontantbaserte regnskapsmetoder. | [Konfigurer urealisert merverdiavgift for kontantbasert regnskap](finance-setup-unrealized-vat.md) |
| Definer utenlandsk valuta du kan handle med eller rapportere transaksjoner i. | [Definer valutaer](finance-set-up-currencies.md) |
| Angi funksjoner for salg og kjøp til å håndtere betalinger i utenlandsk valuta. | [Aktiver utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md) |
| Definer en eller flere valutaer, slik at beløpene rapporteres automatisk i både lokal valuta og en tilleggsrapporteringsvaluta i hver finanspost og andre poster. | [Konfigurer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md) |
| Juster tilleggsvalutaangivelser periodisk for å kompensere for varierende valutakurser. | [Oppdater valutakurser](finance-how-update-currencies.md)|
| Definer flere rentesatser for forskjellige perioder som er knyttet til forsinkede betalinger handelstransaksjoner. | [Konfigurer flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md) |
| Ordne beløp som skal avrundes automatisk etter hvert som fakturaene opprettes. | [Konfigurer fakturaavrunding](finance-set-up-invoice-rounding.md) |
| Legg til nye kontoer i den eksisterende kontoplanen. | [Definere kontoplanen](finance-setup-chart-accounts.md) |
| Konfigurere forretningsintelligensdiagrammer (BI) for å analysere kontantstrøm. | [Definer kontantstrømanalyse](finance-setup-cash-flow-analyses.md) |
| Aktiver fakturering av en kunde som ikke er definert i systemet. | [Konfigurer kontantkunder](finance-how-to-set-up-cash-customers.md) |
| Definer Intrastat-rapportering, og send inn rapporten til myndighetene. | [Konfigurere og rapportere Intrastat](finance-how-setup-report-intrastat.md) |
| Sørg for at en journalpost fordeles mellom forskjellige kontoer som antall, prosent eller beløp når du bokfører den i journalen. | [Bruk fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md) |
| Definer kildekoder og årsakskoder for å spore revisjonsspor. | [Definere kildespor og årsaksspor for revisjonsspor](finance-setup-trail-codes.md) |
| Angi standardrapportene som skal brukes for ulike dokumenttyper. | [Rapportvalg i Business Central](across-report-selections.md) |
| Bruke inngående betalinger, avstemme bankkonti under betalingsutligning og samle utestående saldoer. | [Håndtere fordringer](receivables-manage-receivables.md) |
| Foreta betalinger, utligne utgående betalinger og arbeide med sjekker. | [Administrere skyldige beløp](payables-manage-payables.md) |
| Be kundene om å sende betaling før du leverer til dem, eller send betaling til leverandører før de leverer til deg. | [Fakturere forskuddsbetalinger](finance-invoice-prepayments.md) |
| Avstem og overføre penger mellom kontoer. | [Avstemme bankkonter](bank-manage-bank-accounts.md) |
| Konfigurer konserninterne partnere og behandle transaksjoner manuelt eller automatisk, mellom juridiske enheter i det samme selskapet. | [Behandle konserninterne transaksjoner](intercompany-manage.md) |
| Analyser kostbeløpene for å kjøre bedriften ved å tildele faktiske og budsjetterte kostbeløpe for operasjoner, avdelinger, produkter og prosjekter til kostsentre. | [Gjøre rede for kostnader](finance-manage-cost-accounting.md) |
| Håndter lager- og produksjonskost og rapporter kost og avstem kost mot Finans. | [Administrere lagerkostnader](finance-manage-inventory-costs.md) |
| Administrer og rapporter inngående og utgående kontantstrøm. | [Oversikt over kontantstrøm]( finance-cash-flow-overview.md) |
| Overvåke kontantstrømmen inn og ut av bedriften din. | [Analyser kontantstrømmer i selskapet](finance-analyze-cash-flow.md) |
| Følg en ende-til-ende-prosess som bruker finansrapporter til å lage kontantstrømprognoser. | [Lag kontantstrømprognoser ved å bruke finansrapporter](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Finn ut mer om finans og kontoplanen. | [Forstå Finans og kontoplanen](finance-general-ledger.md) |
| Kombinere finansposter fra flere selskaper i ett virtuelt konsolidert selskap for finansanalyse. | [Konsolider finansielle data fra flere selskaper](finance-consolidated-company-reporting.md)|
| Legg til dimensjoner for bedre forretningsanalyse. | [Arbeid med dimensjoner](finance-dimensions.md) |
| Opprett finansbudsjetter for å forutse ulike økonomiske aktiviteter og tildel dimensjoner for forretningsanalyseformål. | [Opprett finansbudsjetter](finance-how-create-budgets.md) |
| Registrer inntekt og utgifter direkte i Finans, uten å bokføre dedikerte forretningsdokumenter. | [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md) |
| Tilbakefør poster hvis du vil angre verdibokføringer i finanskladden eller antallsbokføringer i salgs- og kjøpsdokumenter. | [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md) |
| Fordele en post i en finanskladd til flere forskjellige konti når du bokfører kladden. | [Fordel kostnader og inntekter](year-allocate-costs-income.md) |
| Tildel ekstra kostnader, for eksempel frakt og fysisk håndtering som du pådrar deg i handel, til varene som er involvert. Kostnaden gjenspeiles deretter i lagerverdisetting. | [Bruk varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md) |
| Bokfør ansattutgifter for arbeidsrelaterte oppgaver og foreta refusjoner direkte til de ansattes bankkontoer. | [Registrer og refunder ansattes utgifter](finance-how-record-reimburse-employee-expenses.md) |
| Fordel inntekter og utgifter i andre perioder enn periodene da transaksjonene faktisk ble bokført. | [Periodiser inntekter og utgifter](finance-how-defer-revenue-expenses.md) |
| Finn ut mer om de tilgjengelige alternativene for sending av abonnementsfakturaer automatisk til kundene og registrere gjentakelsesomsetning. | [Arbeid med gjentakelsesomsetning](finance-recurring-invoicing.md) |
| Bruk flere valutaer og oppdater valutakurser automatisk. | [Oppdater valutakurser](finance-how-update-currencies.md) |
| Importere lønnstransaksjoner fra lønnssystemet til Finans. | [Importer lønnstransaksjoner](finance-how-import-payroll-transactions.md) |
| Beregn mva. på salgs- og kjøpstransaksjoner slik at du kan rapportere beløpene til skattemyndighetene. | [Arbeid med mva. på kjøp og salg](finance-work-with-vat.md) |
| Klargjør en rapport med oversikt over mva fra salg, og send inn rapporten til skattemyndighetene i EU. | [Rapporter mva til skattemyndighetene](finance-how-report-vat.md) |
| Konverter servicekontrakter til å endre mva-satsen manuelt. | [Konverter servicekontrakter som inkluderer mva-beløp](service-how-to-convert-service-contracts.md) |
| Arbeid med årsregnskap og økonomiske oversikter i Microsoft Excel. | [Analysere årsregnskap i Excel](finance-analyze-excel.md) |
| Bruk rollesenteret for regnskapsførere, kommuniserer en ekstern regnskapsfører, og bruk selskapssenteret til å håndtere kontoer for flere klienter. | [Regnskapsføreropplevelser i Business Central ](finance-accounting.md) |
| Definer Intrastat-rapportering for å gi handel med andre EU-medlemmer i henhold til lokal lovgivning. | [Konfigurer Intrastat-rapportering]( finance-how-setup-report-intrastat.md) |
| Fyll ut, valider og send Intrastat-rapporten. | [Arbeid med Intrastat-rapportering]( finance-how-report-intrastat.md) |
| Definer, fyll ut, valider og send tjenesteerklæringsrapporten for handelstjenester i hele EU. | [ Konfigurer og bruk tjenesteerklæring]( finance-how-setup-use-service-declaration.md) |
| Opprette aktiva, tilordne avskrivningsmetoder, bokføre anskaffelser, skrapverdier og skrive ut aktivaoversikter. | [Anskaffe aktiva](fa-how-acquire.md) |
| Registrere servicebesøk, bokføre vedlikeholdskostnader og overvåke vedlikeholdskostnader. | [Vedlikehold aktiva](fa-how-maintain.md) |
| Oppdatere forsikringsopplysninger, bokføre anskaffelseskostnader til forsikringspoliser, endre forsikringsdekningen, vise forsikringsstatistikk og vise forsikringspoliser. | [Forsikre aktiva](fa-how-insure.md) |
| Klassifiser aktiva på nytt, overføre aktiva til ulike lokasjoner, og del opp eller knytt sammen aktiva. | [Overfør, del opp eller kombiner aktiva](fa-how-trans-split-combine.md) |
| Juster verdien for aktiva og bokfør oppskrivnings- og nedskrivningstransaksjoner. | [Revaluer aktiva](fa-how-revalue.md) |
| Beregn og bokfør avskrivning og analyser avskrivning i aktivumrapporter. | [Avskriv eller amortiser aktiva](fa-how-depreciate-amortize.md) |
| Bokføre salgstransaksjoner, vise salgsposter og bokføre delvise salg. | [Avhending eller tilbaketrekking av aktiva](fa-how-dispose-retire.md) |
| Administrere aktivabudsjetter, og budsjettere anskaffelseskostnader, salg av aktiva og avskrivninger. | [Administrer budsjetter for aktiva](fa-how-manage-budgets.md) |
| Definer brukere for arbeidsflyt for godkjenning, angi hvordan brukere varsles, og opprett nye arbeidsflyter. For å opprette nye arbeidsflyter for scenarioer som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden. | [Konfigurer arbeidsflyter for godkjenning](across-set-up-workflows.md) |
| Aktiver arbeidsflyter for godkjenning, handle på arbeidsflytvarsler (f.eks. ved å be om og godkjenne et flyttrinn), og arkiver og slett arbeidsflyter. | [Bruk arbeidsflyter for godkjenning](across-use-workflows.md) |
| Vise faktiske beløp sammenlignet med budsjetterte beløp for alle konti og for flere perioder. | [Analysere faktiske beløp i forhold til budsjetterte beløp](bi-how-analyze-actual-versus-budget.md) |
| Opprette nye finansrapporter for å definere årsregnskap for rapportering eller for visning som diagrammer. | [Klargjøre finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md) |
| Analyser den finansielle ytelsen ved å definere KPI-er som er basert på finansrapporter, og publiser KPI-ene som nettjenester. Publiserte finansrapport-KPI-er kan vises på et nettsted eller importeres til Excel ved hjelp av OData-nettjenester. | [Konfigurer og publiser KPI-nettjenester basert på finansrapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Definere visninger for å analysere data ved hjelp av dimensjoner. | [Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md) |
| Opprette nye analyserapporter for salg, kjøp og beholdning, og definere analysemaler. | [Opprette analyserapporter](bi-how-create-analysis-views-reports.md) |
| Aktiver global finansrapportering til internasjonale regnskapsorganisasjoner med eXtensible Business Reporting Language-standarden (XBRL). | [Opprette rapporter med XBRL](bi-create-reports-with-xbrl.md) |
| Endre tilgangsformålet for databasen i rapporter, sider av typen API, og spørringer for å bidra til å redusere belastningen og forbedre ytelsen. | [Administrer databasetilgangsform](admin-data-access-intent.md) |

## <a name="see-also" />Se også

[Konfigurere finans](finance-setup-finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Avslutte regnskapsperioder](year-close-years-periods.md)  
[Administrere prosjekter](projects-manage-projects.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
