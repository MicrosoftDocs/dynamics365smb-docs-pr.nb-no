---
title: Lageranalyse
description: 'Business Central inneholder en rekke funksjoner som hjelper deg med å samle, analysere og dele verdifulle data i lageret for forretningsanalyse og beslutningstaking i organisasjonen.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Lageranalyse

Virksomheter registrerer mye data under daglige aktiviteter som støtter forretningsanalyse (BI) for lagerledere:

- Levering av varer når ordrer er oppfylt.
- Mottak av varer når bestillinger er oppfylt.
- Flytting av varer mellom lokasjoner.

[!INCLUDE[prod_short](includes/prod_short.md)] gir funksjoner som hjelper deg å samle, analysere og dele organisasjonens lagerdata:

- Ad hoc-analyse på lister
- Ad hoc-analyse av data i Excel (ved å bruke Åpne i Excel)
- Innebygde verktøy for lageranalyse
- Innebygde lagerrapporter

Hver av disse funksjonene har sine fordeler og ulemper, avhengig av typen dataanalyse og brukerens rolle. Hvis du vil finne ut mer, kan du gå til [Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md).

Denne artikkelen viser hvordan du kan bruke disse analysefunksjonene for å få innsikt i lageret.

## Analysebehov i lageret

Når du tenker på analysebehovet i lageradministrasjon, kan det hjelpe å bruke en identitetsbasert modell basert som beskriver forskjellige analysebehov på et høyt nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Personer i ulike roller har ulike behov når det gjelder data, og de bruker dataene på ulike måter. Personer i objektadministrasjon og finans samhandler for eksempel med data på en annen måte enn personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datasamling  | Vanlige måter å bruke data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CFO / CEO    | Ytelsesdata  | KPI-er, instrumentbord, finansrapporter           |
|Lagerleder  | Trender, sammendrag | Innebygde ledelsesrapporter, ad-hoc-analyse      | 
|Lagermedarbeider   | Detaljerte data     | Innebygde driftsrapporter, oppgavedata på skjermen |

<!-- 
## Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer knyttet til lager

Funksjonen **Finansrapportering** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Spesielt for lagerstyringen kan du definere finansrapporter på finanskontoene du bruker til å spore lagerbokføringer.

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du legger til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, områder, produkter og selgere. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Hvis du vil finne ut mer om finansrapporter, kan du gå til [Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Finansrapportering mellom forretningsenheter eller juridiske enheter (knyttet til lager)

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper som rapporterer til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap. Spesielt for lagerstyringen vil du kanskje konsolidere finansposter for lagerkontoene for å kunne spore salgsytelsesindikatorer på tvers av konsern eller juridiske enheter.

Hvis du vil finne ut mer, kan du gå til [Selskapskonsolidering](finance-consolidated-company-reporting.md).

## Ad-hoc-analyse av lagerdata

Noen ganger trenger du bare å sjekke om tallene summeres riktig, eller raskt bekrefte en tall. Følgende funksjoner er gode for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med dataanalysefunksjonen kan du åpne nær sagt enhver listeside, for eksempel **Finansposter**, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Eksempel på hvordan du utfører dataanalyse på gammelt varelager, på siden Vareposter." lightbox="media/data-analysis-inventory-dead-stock.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside, eventuelt filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren.

Hvis du vil vite mer om hvordan du utfører ad hoc-analyse av lagerdata, kan du gå til [Ad hoc-analyse av lagerdata](ad-hoc-analysis-inventory.md).

## Innebygde rapporter for lager

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder flere innebygde rapporter, sporingsfunksjoner og verktøy som hjelper lagerorganisasjoner med å rapportere om dataene sine.

Hvis du vil ha en oversikt over tilgjengelige rapporter, velger du **Alle rapporter** på startsiden. Denne handlingen åpner Rapportutforsker, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Under overskriften **Salg og markedsføring** velger du **Utforsk**. Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Eksempel på rapporter i salgsrollesenteret." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Hvis du vil vite mer om rapporter som er relevante for lager, kan du gå til [Innebygde lagerrapporter](inventory-WMS-reports.md).

## Lageranalyse på skjermen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider som gir deg lageroversikter og oppgaver å gjøre. Her er noen eksempler for å komme i gang:

- [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)
- [Spor varer med serie-, parti- og pakkenumre](inventory-how-work-item-tracking.md)
- [Spor varesporede varer](inventory-how-to-trace-item-tracked-items.md)
- [Revider avstemmingen mellom lagerposten og finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Vis kryssoverførte varer i et leverings- eller plukkforslag](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Salgsmodulen inkluderer også analysesider relatert til lager:

- [Beregn ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)
- [Beregn leveringsdatoer for ordrer](sales-date-calculation-for-sales.md)
- [Spor pakker](sales-how-track-packages.md)

### Vis lager relaterte finansposter og -saldoer fra siden Kontoplan

Siden **Kontoplan** viser alle finanskontoer med aggregerte numre på hva som er bokført i finans. Fra denne siden kan du gjøre ting som:  

- Vise rapporter som viser finansposter og saldoer.  
- Se gjennom en liste over bokføringsgrupper for kontoen.
- Vis separate debet- og kreditsaldoer for én konto.

Spesielt for lagerstyringen kan du opprette en visning på Kontoplan-siden som bare viser kontoene du bruker til å bokføre lagerposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på hvordan siden Kontoplan viser finansinnsikt" lightbox="media/chart-of-accounts-page.png":::

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)

### Analysere lagerdata etter dimensjoner

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

I stedet for å opprette separate finanskontoer for hver avdeling og hvert prosjekt eller sted, kan du bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplanstruktur.

Hvis du finne ut mer, går du til [Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md).

## Se også

[Selskapskonsolidering](finance-consolidated-company-reporting.md)   
[Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Håndter finansrapportering mellom konsern eller juridiske enheter](finance-consolidated-company-reporting.md)  
[Ad hoc-analyse av lagerdata](ad-hoc-analysis-inventory.md)  
[Innebygd beholdnings- og lagerrapporter](inventory-WMS-reports.md)  
[Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
