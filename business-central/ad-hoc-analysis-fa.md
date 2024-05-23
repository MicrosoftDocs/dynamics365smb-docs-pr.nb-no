---
title: Ad hoc-analyse av aktivadata
description: Lær hvordan du bruker dataanalysemodusen til å analysere aktivadata.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse av aktivadata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere aktiva direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er Totale eiendeler, Avskrivning over tid eller andre visninger du kan forestille deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til å starte ad hoc-analyse av aktivaprosesser:

- [Aktivaposter](https://businesscentral.dynamics.com/?page=5604)
- [Finansposter](https://businesscentral.dynamics.com/?page=20)

## Scenarioer med ad hoc-analyse av aktiva

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på aktivascenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Aktiva (nåverdi)](#example-fixed-assets-current-value) | Spor aktivaverdi, både på tvers av alle aktiva og på ett enkelt aktiva. | [Aktivaposter](https://businesscentral.dynamics.com/?page=5604) | **Avskrivningstablå**, **Aktivanr.**, **Aktivabokføringsdato**, **Aktivabokføringstype** og **Beløp** |
| [Aktivaverdiendringer over tid](#example-asset-value-changes-over-time) | Spor aktivaverdiendringer over tid. | [Aktivaposter](https://businesscentral.dynamics.com/?page=5604) | **Aktivabokføringstype**, **Aktivabokføringsdato** og **Beløp** |
|[Aktivaavskrivninger over tid](#example-fixed-asset-depreciations-over-time) | Spor avskrivning over tid, både på tvers av alle aktiva og på ett enkelt aktiva. | [Aktivaposter](https://businesscentral.dynamics.com/?page=5604) | **Avskrivningstablå**, **Aktivanr.**, **Aktivabokføringsår**, **Aktivabokføringsmåned**, **Beløp** og **Aktivabokføringstype** |

### Eksempel: gjeldende verdi for aktiva

Hvis du vil spore verdien av ett eller flere aktiva, gjør du følgende:

1. Åpne [Aktivaposter](https://businesscentral.dynamics.com/?page=5604)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Dra **Avskrivningstablået** og **Aktivanr.** -feltene til **Radgrupper**-området.
1. Velg feltene **Aktivabokføringsdato** og **Aktivabokføringstype**.
1. Dra **Beløp**-feltet til **Verdier**-området.
1. Endre navnet på analysefanen til **Aktivaoversikt - verdi** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Aktivaposter for å se verdien av et aktiva." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### Eksempel: spor aktivaverdiendringer over tid

Hvis du vil spore aktivaverdiendringer over tid, gjør du følgende:

1. Åpne [Aktivaposter](https://businesscentral.dynamics.com/?page=5604)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Flytt feltet **Aktivabokføringstype** til **Radgrupper**-området.
1. Dra feltene **Aktivabokføringsår** og **Aktivabokføringsmåned** til **Kolonneetiketter**-området.
1. Dra **Beløp**-feltet til **Verdier**-området.
1. Endre navnet på analysefanen til **Aktivaverdiendringer over tid** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Aktivaposter for å se aktivaverdiendringer over tid." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### Eksempel: aktivaavskrivninger over tid

Hvis du vil spore avskrivningen av ett eller flere aktiva, gjør du følgende:

1. Åpne [Aktivaposter](https://businesscentral.dynamics.com/?page=5604)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra **Avskrivningstablået** og **Aktivanr.** -feltene til **Radgrupper**-området.
1. Dra feltene **Aktivabokføringsår** og **Aktivabokføringsmåned** til **Kolonneetiketter**-området.
1. Dra **Beløp**-feltet til **Verdier**-området.
1. I filteret **Aktivabokf.type** velger du **Avskrivning**.
1. Endre navnet på analysefanen til **Avskrivning over tid** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Aktivaposter for å se avskrivning over tid." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## Datagrunnlag for ad hoc-analyse av aktiva

Når du bokfører aktivakladder, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] poster i tabellen **Aktivapost**. Derfor utføres ad hoc-analyse av aktiva vanligvis på siden [Aktivaposter](https://businesscentral.dynamics.com/?page=5604).

## Bidragsytere

*Microsoft vedlikeholder denne artikkelen. Deler av eksemplene er opprinnelig skrevet av følgende bidragsyter.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)]-konsulent

## Se også

[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over analyse av aktiva](fa-analytics-overview.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over aktiva](fa-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]