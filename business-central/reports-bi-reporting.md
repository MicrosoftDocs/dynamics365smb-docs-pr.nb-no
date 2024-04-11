---
title: 'Oversikt over analyse, forretningsanalyse og rapportering'
description: 'Gir en oversikt over alle analyse-, forretningsanalyse- og rapporteringsfunksjonene som støttes i Business Central-produktet.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# <a name="analytics-business-intelligence-and-reporting-overview"></a>Oversikt over analyse, forretningsanalyse og rapportering

Små og mellomstore selskaper svarer på innebygd analyse og rapporteringsfunksjonene de kan bruke med en gang til å holde oversikt over virksomheten. [!INCLUDE[prod_short](includes/prod_short.md)] gir rapporter og analyseverktøy som dekker grunnleggende og komplekse forretningsprosesser for slike organisasjoner. Du kan også utføre ad hoc-analyse direkte fra startsiden.  

## <a name="analytics-needs-in-organizations"></a>Analysebehov i organisasjoner

Når du tenker på analysebehov i organisasjoner, kan det hjelpe å bruke en mental modell basert på identitetene beskrevet på et høyt nivå og de forskjellige analysebehovene.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustrasjon av ulike identiteter for analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Modellen tar utgangspunkt i at ulike roller i en organisasjon har ulike behov når det gjelder data. Jo høyere en rolle er plassert i organisasjonskartet, jo mer aggregerte data trenger noen i rollen for å gjøre arbeidet sitt.

Roller har ofte foretrukne måter å konsumere og analysere data på, måter som gjenspeiler nivået av dataaggregering de trenger.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustrasjon av hvordan ulike identiteter har ulike analysebehov." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Bruk delene nedenfor til å lære mer om hvordan du kan bruke data fra [!INCLUDE[prod_short](includes/prod_short.md)]:

- Finansrapporter
- KPI-er og instrumentbord
- Ad hoc-analyse
- Rapporter

## <a name="using-financial-reports-to-produce-financial-statements-and-kpis"></a>Bruk Finansrapporter til å produsere årsregnskap og ytelsesindikatorer

Finansrapporter-funksjonen gir deg innsikt i finansdataene som er lagret i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Skjermbilde av en finansrapport." lightbox="media/acc_schedule_13_columns.jpg":::

Dimensjoner spiller en viktig rolle i forretningsanalyse. En dimensjon er data du kan legge til i en post som et slags parameter. Med dimensjoner kan du gruppere poster med de samme egenskapene, for eksempel kunder, områder, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Blant annet bruker du dimensjoner når du definerer analysevisninger, og når du oppretter finansrapporter. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

Hvis du vil lære mer om årsregnskap og KPI-er, kan du gå til [Bruk Financial Reporting til å produsere årsregnskap og ytelsesindikatorer](bi.md).

## <a name="using-key-performance-indicators-to-meet-your-business-goals"></a>Bruk ytelsesindikatorer til å oppfylle forretningsmålene

En ytelsesindikator er en målbar verdi som viser hvor effektivt du når målene dine. Tenk på ytelsesindikatorer som selskapets målstyring, en måte å måle om du når målene dine eller ikke.

Identifisering og sporing av ytelsesindikatorer forteller deg om virksomheten er på rett vei, eller om du bør endre kurs. Når ytelsesindikatorer brukes riktig, er de kraftige verktøy som hjelper deg med følgende:

- Overvåk selskapets økonomiske tilstand.
- Mål fremgang mot strategiske mål.
- Oppdag problemer tidlig.
- Gjør rettidige justeringer av taktikk.
- Motiver teammedlemmer.
- Ta bedre beslutninger, raskere.

For mer informasjon om ytelsesindikatorer, gå til [Bruk ytelsesindikatorer til å oppfylle forretningsmålene](./analytics-about-kpis.md)

## <a name="ad-hoc-data-analysis"></a>Analyse av ad hoc-data

Noen ganger vil du kanskje bare sjekke om tallene er riktig lagt sammen, raskt bekrefte eller avkrefte en hypotese om virksomheten, eller kanskje se etter uregelmessigheter i dine økonomiske data. For ad hoc-analyser har du kanskje ikke en innebygd rapport som hjelper deg med å svare på spørsmålene dine. Bruk disse to funksjonene for ad hoc-analyser:

- Dataanalyse på finanslistesider
- Åpne i Excel

Med dataanalysefunksjonen kan du åpne nær sagt enhver listeside, for eksempel sidene Finansposter og Kundeposter, åpne analysemodus og deretter gruppere, filtrere og pivotere data slik det passer. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Finansposter." lightbox="media/data-analysis-gl-entries.png":::

På samme måte kan du bruke handlingen **Åpne i Excel** til å åpne en listeside, eventuelt filtrere listen til et delsett av dataene og deretter bruke Excel til å arbeide med dataene. Du kan for eksempel bruke funksjoner som Analyser data, Hypotetisk analyse eller Prognoseark.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på finanspostdata ved å bruke Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Hvis du konfigurerer OneDrive for systemfunksjoner, åpnes Excel-arbeidsboken i nettleseren din ved hjelp av Excel for nettet.

Hvis du vil vite mer om ad hoc-analyser, kan du gå til [Analyse av ad hoc-data](reports-adhoc-analysis.md).

## <a name="reports"></a>Rapporter

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] samler informasjon basert på et angitt sett med kriterier. Rapporter organiserer og presenterer informasjonen i et leservennlig format som du kan bruke i Excel, skrive ut eller lagre som en fil.  

Som et eksempel på en interaktiv rapport i Excel kan du bruke rapporten ***Aldersfordelt saldoliste – kunde** til å analysere hva kundene dine skylder deg, og når betalingene forfaller.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Eksempel på den interaktive rapporten Aldersfordelt saldoliste – kunde i Excel." lightbox="media/aged-accounts-receivables-excel.png":::

For Aldersfordelt saldoliste – kunde inkluderer [!INCLUDE[prod_short](includes/prod_short.md)] også en rapport designet for utskrift. Muligheten til å skrive ut er nyttig hvis du foretrekker å ha dataene i en PDF-fil.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Eksempel på rapporten Aldersfordelt saldoliste – kunde i PDF." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] leveres med mer enn 300 innebygde rapporter som du kan bruke til å støtte forretningsprosessene dine med datadrevet innsikt. Hvis du vil ha en rask oversikt over alle rapportene som er tilgjengelige for din rolle, kan du åpne rapportutforskeren fra rollesenteret og alle listesidene og fra **Fortell meg**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Eksempel på hvordan rapportutforskeren viser alle rapporter for en rolle." lightbox="media/report-explorer-finance.png":::

Hvis du vil lære mer om hvordan du bruker rapportutforskeren til å se alle innebygde rapporter, kan du gå til [Utforsk rapporter per rolle](ui-role-explorer.md).

Tabellen nedenfor inneholder artikler om hvordan du bruker innebygde rapporter i [!INCLUDE[prod_short](includes/prod_short.md)].

| Til  | Se |
| --- | --- |
| Finn ut hvordan du bruker rapporter (bokmerk, kjør, skriv ut, planlegg og endre oppsettet). | [Bruk rapporter i daglig arbeid](reports-use-reports.md) |
| Finn ut mer om hvilke innebygde rapporter som er tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)]. |[Oversikt over rapporter](reports-available-reports.md)| 
| Bruk Rapportutforsker til å se alle innebygde rapporter. | [Utforsk rapporter per rolle](ui-role-explorer.md) |

## <a name="external-business-intelligence-and-reporting-tools"></a>Eksterne verktøy for forretningsanalyse og rapportering

Hvis du foretrekker å bruke forretningsanalyseverktøy som ikke er innebygd i [!INCLUDE[prod_short](includes/prod_short.md)], inneholder tabellen nedenfor koblinger til veiledning om verktøy og måter å bruke eksterne verktøy på.

| Til  | Se |
| --- | --- |
| Bruk Power BI med Business Central-data | [Bruk Power BI med Business Central](admin-powerbi.md) |
| Integrer eksterne forretningsanalyseverktøy med [!INCLUDE[prod_short](includes/prod_short.md)].| [Eksterne forretningsanalyseverktøy](reports-external-analysis.md) |
| Trekk ut data til datalagre eller datasjøer| [Slik trekker du ut data til datalagre eller datasjøer](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Analyser Business Central-data med Microsoft Fabric| [Innføring i Microsoft Fabric og Business Central](admin-fabric.md) |
| Les data fra Business Central ved hjelp av API-er | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## <a name="see-also"></a>Se også

[Bruk finansrapportering til å produsere årsregnskap og ytelsesindikatorer](bi.md)  
[Bruk ytelsesindikatorer (KPI-er) til å oppfylle forretningsmålene](analytics-about-kpis.md)  
[Utføre analyse av ad hoc-data](reports-adhoc-analysis.md)  
[Bruk rapporter i det daglige arbeidet](reports-use-reports.md)  
[Oversikt over innebygde rapporter](reports-available-reports.md)  
[Utforsk rapporter per rolle](ui-role-explorer.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
