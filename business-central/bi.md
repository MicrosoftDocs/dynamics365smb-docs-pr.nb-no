---
title: Finansanalyse i Business Central
description: 'Business Central inneholder en rekke funksjoner som hjelper deg med å samle, analysere og dele verdifulle firmadata for forretningsanalyse og beslutningstaking.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: kepontop
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Finansanalyse i Business Central

Virksomheter registrerer en enorm mengde data under daglige aktiviteter som støtter verdifull forretningsanalyse (BI) for beslutningstakere: 

- Salgstall
- Innkjøp
- Driftsutgifter
- Funksjonærlønn
- Budsjetter

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder en rekke funksjoner som hjelper deg å samle, analysere og dele organisasjonens finansdata:

- Finansrapportering (for årsregnskap og ytelsesindikatorer)
- Ad hoc-analyse på lister
- Ad hoc-analyse av data i Excel (ved å bruke Åpne i Excel)
- Innebygde finansrapporter

Hver av disse funksjonene har sine egne fordeler og ulemper, avhengig av typen dataanalyse og brukerens rolle. Hvis du vil finne ut mer, kan du gå til [Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md).

Denne artikkelen innfører hvordan du kan bruke disse analysefunksjonene til å gi finansinnsikt.

## Analysebehov i finans

Når du tenker på analysebehov i finans, kan det hjelpe å bruke en mental modell basert på identitetene beskrevet på et høyt nivå og de forskjellige analysebehovene.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Personer i ulike roller har ulike behov når det gjelder data, og de bruker dataene på ulike måter. Personer i finans samhandler for eksempel med data på en annen måte enn personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datasamling  | Vanlige måter å bruke data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|Økonomisk direktør / daglig leder          | Ytelsesdata  | KPI-er <br> Instrumentbord <br> Finansrapporter           |
|Økonomistyring | Trender, sammendrag | Innebygde administrasjonsrapporter <br> Ad hoc-analyse      | 
|Regnskapsfører         | Detaljerte data     | Innebygde driftsrapporter <br> Oppgavedata på skjermen |

## Finansytelsesindikatorer

En ytelsesindikator er en målbar verdi som viser hvor effektivt du når målene dine. I finans bruker person ofte følgende ytelsesindikatorer til å overvåke organisasjonens finanstilstand:

- Brutto fortj.margin
- Netto fortjenestemargin
- Arbeidskapital
- Nåværende/hurtigforhold
- Finansiell innflytelse, også kjent som Equity Multiplier
- Gjeldsgrad
- Total aktivaomsetning
- Avkastning på egenkapitalen
- Avkastning på eiendeler

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer

Funksjonen **Finansrapporter** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Resultatet vises i diagrammer og rapporter på startsiden, for eksempel ut Kontantstrøm-diagrammet og rapportene Resultatregnskap og Balanse.

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du kan legge til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, områder, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

> [!TIP]
> Som en rask måte å analysere transaksjonsdata, kan du filtrere totalene i kontoplanen og alle postene på **Poster**-sider per dimensjon. Se etter handlingen **Angi dimensjonsfilter**.  

Tabellen nedenfor beskriver en sekvens av oppgaver i finansrapportering, og har koblinger til artiklene som beskriver dem.  

| Til | Se |
| --- | --- |
| Opprette nye finansrapporter for å definere årsregnskap for rapportering eller for visning som diagrammer.| [Klargjøre finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)|
| Bruke statistiske kontoer til å supplere informasjon i finansrapporter. Med statistiske kontoer kan du legge til målinger basert på ikke-transaksjonelle data. Du kan legge til ikke-transaksjonsdata som nummerbaserte enheter, for eksempel antall ansatte, kvadratmeter eller antall kunder med forfalte kontoer. | [Analyser data med statistiske kontoer](bi-use-statistical-accounts.md) |
| Lær hvordan du konfigurerer en ny finansrapport ved hjelp av eksempler. | [Gjennomgang: Bruk finansrapportering til å lage kontantstrømprognoser](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Analyser den finansielle ytelsen ved å definere KPIer som er basert på finansrapporter, som du deretter publiserer som web-tjenester. Publiserte finansrapport-KPIer kan vises på et webområde eller importeres til Microsoft Excel ved hjelp av OData-webtjenester. |[Konfigurere og publisere KPI-webtjenester basert på finansrapporter](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Definere visninger for å analysere data ved hjelp av dimensjoner.|[Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md)|
| Opprette nye analyserapporter for salg, kjøp og beholdning, og definere analysemaler. |[Opprett analyserapporter](bi-how-create-analysis-views-reports.md)|

## Finansrapportering mellom forretningsenheter eller juridiske enheter

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som må rapportere til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap.  

Hvis du vil finne ut mer, kan du gå til [Selskapskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse av finansdata

Noen ganger trenger du bare å sjekke om tallene summeres riktig, eller raskt bekrefte en tall. Følgende funksjoner er gode for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med dataanalysefunksjonen kan du åpne nesten en listeside, for eksempel finansposter, aktivaposter, sjekkposter eller bankkontoposter, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-gl-entries.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside for poster, eventuelt filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på finanspostdata ved å bruke Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren din ved hjelp av Excel for nettet. 

<!-- Not ready yet
For more information on how to do ad-hoc analysis on ledgers, see [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md). 
-->
## Innebygde rapporter for finans

[!INCLUDE [prod_short](includes/prod_short.md)] inkluderer flere innebygde rapporter, sporingsfunksjoner og verktøy som hjelper revisorer eller kontrollører som er ansvarlige for rapportering til økonomiavdelingen.

Hvis du vil ha en oversikt over tilgjengelige rapporter, kan du klikke på **Alle rapporter** i den øverste ruten på startsiden. Dette tar deg til rolleutforskeren, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Eksempel på rapporter i finansrollesenteret." lightbox="media/report-explorer-finance.png":::

Innebygde rapporter kommer i to smaker:

- Utformet for utskrift (pdf).
- Utformet for analyse i Excel.

Hvis du vil ha mer informasjon, kan du se disse oversiktene for rapporter som er relevante for finans.

- [Innebygde Excel-finansrapporter](finance-analyze-excel.md)
- [Innebygde nøkkelfinansrapporter](finance-reports.md)
- [Innebygde aktivarapporter](fa-reports.md)
- [Innebygde rapporter om utestående fordringer](receivables-reports.md)
- [Innebygde rapporter om leverandørgjeld](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Finansoppgavesider på skjermen

[!INCLUDE [prod_short](includes/prod_short.md)] har en rekke sider som gir deg finansoversikter og oppgaver å gjøre.

### Vis finansposter og -saldoer fra siden Kontoplan

Siden Kontoplan viser alle finanskontoer med aggregerte numre for hva som er bokført i finans. Fra denne siden kan du gjøre ting som:  

- Vise rapporter som viser finansposter og saldoer.  
- Se gjennom en liste over bokføringsgrupper for kontoen.
- Vise separate debet- og kreditsaldoer for én konto.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på hvordan siden Kontoplan viser finansinnsikt" lightbox="media/chart-of-accounts-page.png":::

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)

### Vis faktiske beløp sammenlignet med budsjetterte beløp for alle kontoer og for flere perioder

Som en del av innsamling, analyse og deling av selskapsdataene ønsker du kanskje å vise faktiske beløp sammenlignet med budsjetterte beløp for alle kontoer og for flere perioder. Du kan gjøre dette fra siden **Kontoplan** ved å velge handlingen **Finanssaldo/Budsjett**.

Hvis du vil finne ut mer, kan du gå til [Analyser faktiske beløp kontra budsjetterte beløp](bi-how-analyze-actual-versus-budget.md).

### Analyser data etter dimensjoner

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

I stedet for å opprette separate finanskontoer for hver avdeling og hvert prosjekt, kan du bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplanstruktur.

I finansanalyse er en dimensjon data du kan legge til i en finanspost som et slags merke. Disse dataene brukes til å gruppere finansposter med de samme egenskapene, for eksempel kunder, områder, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Du kan bruke dimensjoner på poster i kladder, dokumenter og budsjetter. Hvis du vil ha mer informasjon, kan du se [Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md)

### Analyser kontantstrøm

På startsiden for regnskapsfører under **Finansytelse**, gir diagrammene Kontantsyklus, Kontantstrøm samt Inntekter og utgifter muligheter til å analysere kontantstrøm:

- Gå gjennom tallene i en periode ved hjelp av skyvekontrollen for tidslinjen.
- Filtrere diagrammet ved å velge kilden i forklaringen.
- Endre lengden på perioden, eller gå til forrige eller neste periode, ved å velge alternativer på den Finansytelse rullegardinlisten.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Eksempel på hvordan visualobjektene for kontantstrøm ser ut i rollesenteret for regnskapsfører" lightbox="media/cashflow-accountant-rolecentre.png":::

Hvis du vil undersøke prognosen, i tillegg til prognosen oppføringer, kan du også se på kontantstrømforslaget. Du kan for eksempel se hvordan prognosen:

- Håndterer bekreftede salg og innkjøp.
- Trekker fra tilgodehavende og legger til skyldig beløp.
- Hopper over dupliserte salgsordrer og bestillinger.

Hvis du vil finne ut mer, kan du gå til [Analyser kontantstrømmen i selskapet](finance-analyze-cash-flow.md)

## Se også

[Håndter finansrapportering mellom forretningsenheter eller juridiske enheter](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
<!-- [Ad-hoc analysis on finance data](ad-hoc-analysis-finance.md)   -->
[Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Innebygde Excel-finansrapporter](finance-analyze-excel.md)  
[Innebygde nøkkelfinansrapporter](finance-reports.md)  
[Innebygde aktivarapporter](fa-reports.md)  
[Innebygde rapporter om utestående fordringer](receivables-reports.md)  
[Innebygde rapporter om leverandørgjeld](payables-reports.md)  
[Oversikt over finans](finance.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
