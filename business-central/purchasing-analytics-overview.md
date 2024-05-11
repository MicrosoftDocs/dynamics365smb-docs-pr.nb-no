---
title: Analyse i kjøp
description: 'Business Central inneholder en rekke funksjoner som hjelper deg med å samle, analysere og dele verdifulle salgsdata for forretningsanalyse og beslutningstaking innenfor kjøpsorganisasjonen.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="analytics-in-purchasing"></a>Analyse i kjøp

Virksomheter registrerer mye data under daglige aktiviteter som støtter forretningsanalyse (BI) for kjøpssjefer:

- Forespørsler
- Bestillinger
- Kjøpsfakturaer

[!INCLUDE[prod_short](includes/prod_short.md)] gir funksjoner som hjelper deg å samle, analysere og dele organisasjonens kjøpsdata:

- Ad hoc-analyse på lister
- Ad hoc-analyse av data i Excel (ved å bruke Åpne i Excel)
- Innebygde salgsrapporter

Hver av disse funksjonene har fordeler og ulemper, avhengig av typen dataanalyse og brukerens rolle. Hvis du vil finne ut mer, kan du gå til [Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md).

Denne artikkelen innfører hvordan du kan bruke disse analysefunksjonene for å få kjøpsinnsikt.

## <a name="analytics-needs-in-purchasing"></a>Analysebehov i kjøp

Når du tenker på analysebehovet i kjøp, kan det hjelpe å bruke en identitetsbasert modell basert som beskriver forskjellige analysebehov på et høyt nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Personer i ulike roller har ulike behov når det gjelder data, og de bruker dataene på ulike måter. Personer i objektadministrasjon og finans samhandler for eksempel med data på en annen måte enn personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datasamling  | Vanlige måter å bruke data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CSO / CFO / CEO    | Ytelsesdata  | KPI-er <br> Instrumentbord <br> Finansrapporter           |
|Innkjøpssjef      | Trender, sammendrag | Innebygde administrasjonsrapporter <br> Ad hoc-analyse      | 
|Innkjøpssjef / Innkjøper | Detaljerte data     | Innebygde driftsrapporter <br> Oppgavedata på skjermen |

<!-- 
## <a name="purchasing-kpis"></a>Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-purchasing"></a>Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer (knyttet til kjøp)

Funksjonen **Finansrapportering** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Spesielt for kjøp kan du definere finansrapporter på finanskontoene du bruker til å spore kjøpsbokføringer.

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du kan legge til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, områder og produkter, og på en enkel måte få tak i disse gruppene i analyser. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Hvis du vil finne ut mer om finansrapporter, kan du gå til [Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-purchasing"></a>Finansrapportering mellom forretningsenheter eller juridiske enheter (knyttet til kjøp)

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som rapporterer til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap. Spesielt for innkjøpsadministrasjon vil du kanskje konsolidere finansposter for innkjøpskontoene for å spore salgsytelsesindikatorer på tvers av konsern eller juridiske enheter.

Hvis du vil finne ut mer, kan du gå til [Selskapskonsolidering](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-purchasing-data"></a>Ad hoc-analyse av kjøpsdata

Noen ganger trenger du bare å sjekke om tallene summeres riktig, eller raskt bekrefte en tall. Følgende funksjoner er gode for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med **dataanalysefunksjonen** kan du åpne nær sagt enhver listeside, for eksempel sidene **Bestillinger**, **Bokførte kjøpsfakturaer**, **Leverandørposter** eller **Finansposter**, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Kundeposter." lightbox="media/data-analysis-vendor-ledger-entries.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside, filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på kundepostdata ved å bruke Excel." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren.

Hvis du vil vite mer om hvordan du utfører ad hoc-analyse av kjøpsdata, kan du gå til [Ad hoc-analyse av kjøpsdata](ad-hoc-analysis-purchasing.md).

## <a name="built-in-reports-for-purchasing"></a>Innebygde rapporter for kjøp

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder flere innebygde rapporter, sporingsfunksjoner og verktøy som hjelper innkjøpsorganisasjoner med å rapportere om dataene sine.

Hvis du vil ha en oversikt over tilgjengelige rapporter, velger du **Alle rapporter** øverst på startsiden. Denne handlingen åpner rolleutforskeren, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Eksempel på rapporter i XXX-rollesenteret." lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Hvis du vil vite mer om rapporter som er relevante for kjøp, kan du gå til [Innebygde kjøpsrapporter](purchase-reports.md).

## <a name="on-screen-purchasing-analytics"></a>Kjøpsanalyse på skjermen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider som gir deg kjøpsoversikter og oppgaver å gjøre. Her er et eksempel for å komme i gang:

- [Beregn datoer for kjøp](purchasing-date-calculation-for-purchases.md)

### <a name="show-purchasing-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Vis kjøpsrelaterte finansposter og -saldoer fra siden Kontoplan

Siden Kontoplan viser alle finanskontoer med aggregerte numre på hva som er bokført i finans. Fra denne siden kan du gjøre ting som:  

- Vise rapporter som viser finansposter og saldoer.  
- Se gjennom en liste over bokføringsgrupper for kontoen.
- Vis separate debet- og kreditsaldoer for én konto.

Spesielt for kjøp kan du opprette en visning på Kontoplan-siden som bare viser kontoene du bruker til å bokføre kjøpsposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på hvordan siden Kontoplan viser finansinnsikt" lightbox="media/chart-of-accounts-page.png":::

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)

### <a name="analyze-data-by-dimensions-related-to-purchasing"></a>Analyser data etter dimensjoner (relatert til kjøp)

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel bestillinger. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

I stedet for å opprette separate finanskontoer for hver avdeling og hvert prosjekt eller sted, kan du bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplanstruktur.

Hvis du finne ut mer, går du til [Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Se også

[Selskapskonsolidering](finance-consolidated-company-reporting.md)  
[Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Håndter finansrapportering mellom forretningsenheter eller juridiske enheter](finance-consolidated-company-reporting.md)  
[Ad hoc-analyse av kjøpsdata](ad-hoc-analysis-purchasing.md)  
[Innebygde kjøpsrapporter](purchase-reports.md)  
[Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
