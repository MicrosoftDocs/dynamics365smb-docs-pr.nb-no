---
title: Aktivaanalyse
description: 'Lær hvordan du samler, analyserer og deler data om aktiva for forretningsintelligens.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 04/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Aktivaanalyse

Virksomheter med aktiva registrerer mye data om dem under daglige aktiviteter. Disse dataene støtter verdifull forretningsintelligens (BI) for aktivaforvaltere:

- Objektanskaffelse
- Objektavskrivninger
- Forsikring og reparasjon og vedlikehold
- Objektbudsjetter

[!INCLUDE[prod_short](includes/prod_short.md)] gir funksjoner som hjelper deg å samle, analysere og dele data om organisasjonens aktiva:

- Finansrapportering (for finansutdrag og ytelsesindikatorer på aktivakontoer)
- Ad hoc-analyse på lister
- Ad hoc-analyse av data i Excel (ved å bruke Åpne i Excel)
- Innebygde analyseverktøy for aktiva
- Innebygde aktivarapporter

> [!NOTE]
> Analyse for aktive er litt annerledes enn andre områder. Du må analysere data som allerede finnes, for eksempel objektanskaffelser, avskrivninger og forsikring, men også data om fremtiden, for eksempel avskrivninger og objektavviklinger. For sistnevnte type analyse har [!INCLUDE[prod_short](includes/prod_short.md)] innebygde rapporter som kan beregne disse tallene.

Hver funksjon har sine fordeler og ulemper, avhengig av typen dataanalyse og brukerens rolle. Hvis du vil finne ut mer, kan du gå til [Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md).

I denne artikkelen beskriver vi hvordan du kan bruke disse analysefunksjonene til å få innsikt i aktivaene.

## Analysebehov i objektadministrasjon

Når du tenker på analysebehovet i objektadministrasjon, kan det hjelpe å bruke en identitetsbasert modell basert som beskriver analysebehov på et høyt nivå.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Når det gjelder data, har personer i ulike roller ulike behov når det gjelder data, og de bruker dataene på ulike måter. Personer i objektadministrasjon og finans samhandler for eksempel med data på en annen måte enn personer i salg.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rolle              | Datasamling  | Vanlige måter å bruke data på                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO / COO / CEO                 | Ytelsesdata  | KPI-er <br> Instrumentbord <br> Finansrapporter           |
|Aktivaadministrasjon/kontrollør   | Trender, sammendrag | Innebygde administrasjonsrapporter <br> Ad hoc-analyse      | 
|Regnskapsfører                      | Detaljerte data     | Innebygde driftsrapporter <br> Oppgavedata på skjermen |

## Ytelsesindikatorer for objektadministrasjon

En ytelsesindikator er en målbar verdi som viser hvor effektivt du når målene dine. I objektadministrasjon bruker person ofte følgende ytelsesindikatorer til å overvåke organisasjonens bruk av objekter:

- Total aktivaomsetning
- Avkastning på eiendeler

## Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer knyttet til aktiva

Funksjonen **Finansrapportering** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Spesielt for objektadministrasjon kan du definere finansrapporter på finanskontoene du bruker til å spore aktivabokføringer.

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du kan legge til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Hvis du vil finne ut mer om finansrapportering, kan du gå til [Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md).

## Finansrapportering mellom forretningsenheter eller juridiske enheter (knyttet til aktiva)

Noen organisasjoner bruker [!INCLUDE [prod_short](includes/prod_short.md)] i flere konsern eller juridiske enheter. Andre bruker [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaper rapporterer til overordnede organisasjoner. [!INCLUDE [prod_short](includes/prod_short.md)] gir regnskapsførere verktøy som hjelper dem med å overføre finansposter fra to eller flere selskaper (datterselskaper) til et konsolidert selskap. Spesielt for objektadministrasjon vil du kanskje konsolidere finansposter for aktivakontoene for å kunne spore aktivasytelsesindikatorer på tvers av konsern eller juridiske enheter.

Hvis du vil finne ut mer, kan du gå til [Selskapskonsolidering](finance-consolidated-company-reporting.md).

## Ad hoc-analyse av aktivadata

Noen ganger trenger du bare å sjekke om tallene summeres riktig, eller raskt bekrefte en tall. Følgende funksjoner er gode for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med dataanalysefunksjonen kan du åpne nær sagt enhver listeside, for eksempel **Finansposter** eller **Aktivaposter**, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Aktivaposter for å se aktivaverdi." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside for poster, eventuelt filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren din ved hjelp av Excel for nettet. 

Hvis du vil ha mer informasjon om hvordan du utfører ad hoc-analyse på aktiva, kan du se [Ad hoc-analyse av aktivadata](ad-hoc-analysis-fa.md).


## Innebygde rapporter for aktiva

[!INCLUDE [prod_short](includes/prod_short.md)] inkluderer flere innebygde rapporter, sporingsfunksjoner og verktøy som hjelper revisorer eller kontrollører som rapporterer om aktiva.

Hvis du vil ha en oversikt over tilgjengelige rapporter, velger du **Alle rapporter** øverst på startsiden. Denne handlingen åpner rolleutforskersiden, som er filtrert etter funksjonene i alternativet **Rapport og analyse**. Hvis du vil finne rapporter som er knyttet til aktiva, angir du **aktiva** i **Søk**-feltet. Hvis du vil finne ut mer, kan du gå til [Finn rapporter med rolleutforskeren](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Eksempel på rapporter i finansrollesenteret." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Hvis du vil ha mer informasjon om rapporter som er relevante for aktiva, kan du se [Innebygde aktivarapporter](fa-reports.md).

## Aktivaanalyse på skjermen

[!INCLUDE [prod_short](includes/prod_short.md)] har flere sider som gir deg aktivaoversikter og oppgaver å gjøre. Her er noen eksempler for å komme i gang:

- [Beregn avskrivning, bokføre avskrivning og analysere avskrivning](fa-how-depreciate-amortize.md)
- [Overvåk vedlikeholdskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)
- [Overvåk forsikringsdekning](fa-how-insure.md#to-monitor-insurance-coverage)
- [Vis endrede avskrivningstablåverdier](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Vis avhendingsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Vis forventede avhendingsverdier](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### Vis aktivaposter og -saldoer fra siden Kontoplan

Siden Kontoplan viser alle finanskontoer med aggregerte numre i finans. Fra denne siden kan du gjøre ting som:  

- Vise rapporter som viser finansposter og saldoer.  
- Se gjennom en liste over bokføringsgrupper for kontoen.
- Vis separate debet- og kreditsaldoer for én konto.

Spesielt for aktiva kan du opprette en visning på Kontoplan-siden som bare viser kontoene du bruker til å bokføre aktivaposter.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Eksempel på hvordan siden Kontoplan viser finansinnsikt" lightbox="media/chart-of-accounts-page.png":::

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)

### Analyser data etter dimensjoner (relatert til aktiva)

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel aktivakladder. Dimensjoner kan for eksempel angi avdelingen og stedet en post kommer fra.  

I stedet for å opprette separate finanskontoer for hver avdeling og hvert prosjekt eller sted, kan du bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplanstruktur.

Hvis du finne ut mer, går du til [Analyser data etter dimensjoner](bi-how-analyze-data-dimension.md)

## Se også

[Håndter finansrapportering mellom forretningsenheter eller juridiske enheter](finance-consolidated-company-reporting.md)  
[Klargjør finansrapporter med finansdata og kontokategorier](bi-how-work-account-schedule.md)  
[Forstå kontoplanen](finance-general-ledger.md#the-chart-of-accounts)  
[Ad hoc-analyse av aktivadata](ad-hoc-analysis-fa.md)   
[Innebygde aktivarapporter](fa-reports.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
