---
title: Ad hoc-analyse av bærekraftsdata
description: Lær hvordan du bruker dataanalysemodusen til å analysere bærekraftsdata.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse av bærekraftsdata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere bærekraftsdata direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er "Utslippsoversikt" eller "Utslipp etter omfang", eller andre visninger du kan tenke deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til ad hoc-analyse av bærekraftsdata:

- [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220)

## Ad hoc-analysescenarioer for bærekraft

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på bærekraftscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Utslippsoversikt (sum etter kategori)](#example-emission-overview-sum-by-category) | Analyser utslippene dine etter kategori. | [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonavn**, **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O**.|
| [Gjennomsnittlig utslipp etter kategori](#example-average-emissions-by-category) | Analyser dine gjennomsnittlige utslipp etter kategori. | [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220) | **Kontokategori**, **Kontonavn**, **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O**.|
| [Utslipp etter omfang](#example-emissions-by-scope) | Analyser utslippene dine etter omfang. | [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220) | **Utslippsomfang**, **Kontokategori**, **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O**.|

## Eksempel: Utslippsoversikt (sum etter kategori)

Hvis du vil analysere utslippene dine etter kategori, gjør du følgende:

1. Åpne siden [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220), og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra feltene **Kontokategori** og **Kontonavn** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltene **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O** til **Verdier**-området.
1. Endre navnet på analysefanen til **Utslippsoversikt (sum)** eller noe som beskriver denne analysen for deg.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Eksempel 1 på hvordan du utfører dataanalyse på siden Bærekraftsposter." lightbox="media/data-analysis-sustainability-entries.png":::

## Eksempel: Gjennomsnittlig utslipp etter kategori

Hvis du vil analysere dine gjennomsnittlige utslipp etter kategori, gjør du følgende:

1. Åpne siden [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220), og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra feltene **Kontokategori** og **Kontonavn** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltene **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O** til **Verdier**-området.
1. Velg hvert felt i **Verdier**-området, og endre aggregeringsfunksjonen til `Average`.
1. Endre navnet på analysefanen til **Utslippsoversikt (gj.sn.)** eller noe som beskriver denne analysen for deg.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Eksempel 2 på hvordan du utfører dataanalyse på siden Bærekraftsposter." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Eksempel: Utslipp etter omfang

Hvis du vil analysere utslippene dine etter omfang, gjør du følgende:

1. Åpne siden [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220), og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra feltene **Utslippsomfang** og **Kontokategori** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltene **Utslipp NH4**, **Utslipp CO2** og **Utslipp N2O** til **Verdier**-området.
1. Endre navnet på analysefanen til **Utslippsoversikt etter omgang** eller noe som beskriver denne analysen for deg.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Eksempel 3 på hvordan du utfører dataanalyse på siden Bærekraftsposter." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Datagrunnlag for ad hoc-analyse av bærekraft

Opplysningene du angir i en bærekraftskladd, er midlertidige og du kan endre dem mens de fortsatt befinner seg i kladden. Når du bokfører en bærekraftskladd, overføres informasjonen til bærekraftsposter på individuelle bærekraftskontoer, der du ikke kan endre dem. Du kan imidlertid bokføre tilbakeførings- eller korrigeringsposter. Listesiden [Bærekraftsposter](https://businesscentral.dynamics.com/?page=6220) er den viktigste datakilden for ad hoc-analyse av bærekraftsdata.

Hvis du vil vite mer om hvordan du bokfører bærekraftsposter, kan du gå til [Registrer bærekraftsposter](finance-sustainability-journal.md).

## Se også

[Registrer bærekraftsposter](finance-sustainability-journal.md)  
[Innebygde bærekraftsrapporter](sustainability-reports.md)   
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over bærekraftsbehandling](finance-manage-sustainability.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
