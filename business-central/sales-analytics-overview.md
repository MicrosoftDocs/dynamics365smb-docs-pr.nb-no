---
title: Salgsanalyse
description: 'Business Central inneholder en rekke funksjoner som hjelper deg med å samle, analysere og dele verdifulle salgsdata for forretningsanalyse og beslutningstaking innenfor salgsorganisasjonen.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Salgsanalyse

Virksomheter registrerer mye data under daglige aktiviteter som støtter forretningsanalyse (BI) for salgssjefer:

- Salgsmuligheter
- Tilbud
- Ordrer
- Salgsfakturaer

[!INCLUDE[prod_short](includes/prod_short.md)] gir funksjoner som hjelper deg å samle, analysere og dele organisasjonens salgsdata:

- Ad hoc-analyse på lister
- Ad hoc-analyse av data i Excel (ved å bruke Åpne i Excel)
- Innebygde verktøy for salgsanalyse
- Innebygde salgsrapporter

Hver av disse funksjonene har sine fordeler og ulemper, avhengig av typen dataanalyse og brukerens rolle. Hvis du vil finne ut mer, kan du gå til [Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md).

Denne artikkelen innfører hvordan du kan bruke disse analysefunksjonene til å få salgsinnsikt.

## Analysebehov i salg

Når du tenker på analysebehovet i salgsadministrasjon, kan det hjelpe å bruke en identitetsbasert modell basert som beskriver forskjellige analysebehov på et høyt nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Personer i ulike roller har ulike behov når det gjelder data, og de bruker dataene på ulike måter. Personer i objektadministrasjon og finans samhandler for eksempel med data på en annen måte enn personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datasamling  | Vanlige måter å bruke data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO / CFO / CEO    | Ytelsesdata  | KPI-er <br> Instrumentbord <br> Finansrapporter           |
|Salgssjef      | Trender, sammendrag | Innebygde administrasjonsrapporter <br> Ad hoc-analyse      | 
|Kundeansvarlig / selger | Detaljerte data     | Innebygde driftsrapporter <br> Oppgavedata på skjermen |

<!-- 
## Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer knyttet til salg

Funksjonen **Finansrapportering** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Spesielt for salgsadministrasjon kan du definere finansrapporter på finanskontoene du bruker til å spore salgsbokføringer.

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du legger til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, områder, produkter og selgere. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Hvis du vil finne ut mer om finansrapporter, kan du gå til [Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Finansrapportering mellom forretningsenheter eller juridiske enheter knyttet til salg

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som rapporterer til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap. Spesielt for salgsadministrasjon vil du kanskje konsolidere finansposter for salgskontoene for å kunne spore salgsytelsesindikatorer på tvers av konsern eller juridiske enheter.

Hvis du vil finne ut mer, kan du gå til [Selskapskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse av salgsdata

Noen ganger trenger du bare å sjekke om tallene summeres riktig, eller raskt bekrefte en tall. Følgende funksjoner er gode for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med Dataanalyse-funksjonen kan du åpne nær sagt enhver listeside, for eksempel **Finansposter**, **Kundeposter**, **Vareposter** eller **Bokførte fakturaer**, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Kundeposter." lightbox="media/data-analysis-customer-ledger-entries.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside, eventuelt filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på kundepostdata ved å bruke Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren.

Hvis du vil vite mer om hvordan du utfører ad hoc-analyse av salgsdata, kan du gå til [Ad hoc-analyse av salgsdata](ad-hoc-analysis-sales.md). 

## Innebygde rapporter for salg

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder flere innebygde rapporter, sporingsfunksjoner og verktøy som hjelper salgsorganisasjoner med å rapportere om dataene sine.

Hvis du vil ha en oversikt over tilgjengelige rapporter, velger du **Alle rapporter** øverst i ruten på startsiden. Denne handlingen åpner rolleutforskeren, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter i salgsrollesenteret." lightbox="media/report-explorer-sales.png":::

De innebygde rapportene kommer i to smaker:

- Utformet for utskrift (pdf).
- Utformet for analyse i Excel.

Hvis du vil vite mer om rapporter som er relevante for salg, kan du gå til [Innebygde salgsrapporter](sales-reports.md).

## Salgsanalyse på skjermen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider som gir deg salgsoversikter og oppgaver å gjøre. Her er noen eksempler for å komme i gang:

- [Åpne listen **Tilbud**](https://businesscentral.dynamics.com/?page=9300)
- [Åpne listen **Ordrer**](https://businesscentral.dynamics.com/?page=9305)
- [Åpne listen **Bokførte salgsfakturaer**](https://businesscentral.dynamics.com/?page=143)
- [Åpne listen **Ordrereturer**](https://businesscentral.dynamics.com/?page=9304)
- [Beregn ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)
- [Beregn leveringsdatoer for ordrer](sales-date-calculation-for-sales.md)
- [Spor pakker](sales-how-track-packages.md)
- [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)
- [Status for rammeordre](sales-how-to-create-blanket-sales-orders.md#to-view-the-status-of-a-blanket-sales-order)
- [Vis ikke-bokførte og bokførte rammeordrelinjer](sales-how-to-create-blanket-sales-orders.md#to-view-unposted-and-posted-blanket-sales-order-lines)


### Vis salgsrelaterte finansposter og -saldoer fra siden Kontoplan

Siden Kontoplan viser alle finanskontoer med aggregerte numre på hva som er bokført i finans. Fra denne siden kan du gjøre ting som:  

- Vise rapporter som viser finansposter og saldoer.  
- Se gjennom en liste over bokføringsgrupper for kontoen.
- Vis separate debet- og kreditsaldoer for én konto.

Spesielt for salg kan du opprette en visning på Kontoplan-siden som bare viser kontoene du bruker til å bokføre salgsposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på hvordan siden Kontoplan viser finansinnsikt" lightbox="media/chart-of-accounts-page.png":::

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)

### Analyser data etter dimensjoner (relatert til salg)

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

I stedet for å opprette separate finanskontoer for hver avdeling og hvert prosjekt eller sted, kan du bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplanstruktur.

Hvis du finne ut mer, går du til [Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md).

## Se også

[Selskapskonsolidering](finance-consolidated-company-reporting.md)   
[Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Håndter finansrapportering mellom konsern eller juridiske enheter](finance-consolidated-company-reporting.md)  
[Ad hoc-analyse av salgsdata](ad-hoc-analysis-sales.md)   
[Innebygde salgsrapporter](sales-reports.md)   
[Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
