---
title: Ad hoc-analyse av salgsdata
description: Lær hvordan du bruker dataanalysemodusen til å analysere salgsdata.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse av salgsdata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere salgsdata direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er Mine kunder eller Salgsstatistikk, eller andre visninger du kan tenke deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til ad hoc-analyse av salgsprosesser:

- [Ordrer](https://businesscentral.dynamics.com/?page=9305)
- Finansposter
- [Kundeposter](https://businesscentral.dynamics.com/?page=25)
- Vareposter
- Bokførte salgsfakturaer
- Ordrereturer

## Scenarioer for ad hoc-analyse for salg

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på salgsscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Salg (forventet salgsvolum)](#example-sales-expected-sales-volume) | Analyser forventet salgsvolum. | [Ordrer](https://businesscentral.dynamics.com/?page=9305) | **Salg til-kundenavn**, **Salg til-kundenr.**, **Nr.** , **Beløp**, **Bilagsdato (år)** og **Bilagsdato (måned)**. |
| [Salg (Kundesalg etter volum)](#example-sales-customer-sales-by-volume) | Få en oversikt over kundene som kjøper mest, eller kundene som skylder mest. | [Kundeposter](https://businesscentral.dynamics.com/?page=25) | **Kundenavn**, **Dokumentnr.**, **Beløp** og **Restbeløp**. |
| [Finans (kunde)](#example-finance-accounts-receivables) | Se hva kundene dine skylder deg, for eksempel inndelt i tidsintervaller for når beløp forfaller. | [Kundeposter](https://businesscentral.dynamics.com/?page=25) | **Kundenavn**, **Forfallsdato** og **Restbeløp**. |

## Eksempel: Salg (forventet salgsvolum)

Hvis du vil analysere forventet salgsvolum og salgsbeløp for ordrer som ikke er levert, for hver kunde etter år eller måned, gjør du følgende:

1. Åpne [Ordrer](https://businesscentral.dynamics.com/?page=9305)-listen, og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra feltene **Salg til-kundenavn**, **Salg til-kundenr.** og **Nr.** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltet **Beløp** til **Verdier**-området.
1. Dra feltene **Dokumentdato (år)** og **Dokumentdato (måned)** til **Kolonneetiketter**-området. Dra feltene i den rekkefølgen.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Flere filtre**. Menyen er til høyre på siden, rett under **Kolonner**-menyen.
1. Endre navnet på analysefanen til **Forventet salgsvolum** eller noe som beskriver denne analysen for deg.

## Eksempel: Salg (Kundesalg etter volum)

Hvis du vil produsere en rapport over kundene som kjøper mest, eller som skylder mest, følger du denne fremgangsmåten:

1. Åpne listen [Kundeposter](https://businesscentral.dynamics.com/?page=25) og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Dra **Kundenavn**-feltet til **Radgrupper**-området og **Dokumentnr.**-feltet under.
1. Velg feltene **Beløp** og **Restbeløp**.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Flere filtre**. Menyen er til høyre på siden, rett under **Kolonner**-menyen.
1. Endre navnet på analysefanen til **Kunde etter salgsvolum** eller noe som beskriver denne analysen for deg.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Kundeposter." lightbox="media/data-analysis-customer-ledger-entries.png":::

## Eksempel: Finans (kunde)

Hvis du vil se hva kundene dine skylder deg, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne listen [Kundeposter](https://businesscentral.dynamics.com/?page=25) og aktiver analysemodus.
1. På **Kolonner**-menyen fjerner du alle kolonner (merk av i boksen ved siden av **Søk**-feltet).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra **Kundenavn**-feltet til **Radgrupper**-området og dra **Restbeløp**-feltet til **Verdier**-området.
1. Dra feltet **Forfallsdato (måned)** til **Kolonneetiketter**-området.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Flere filtre**. Menyen er til høyre på siden, rett under **Kolonner**-menyen.
1. Endre navnet på analysefanen til **Aldersfordelte kontoer etter måned** eller noe som beskriver denne analysen for deg.

## Datagrunnlag for ad hoc-analyse av salg

Når du har angitt informasjon på en ordre og legger til alle ordrelinjene, kan du bokføre ordren. Bokføring oppretter en levering og en faktura. [!INCLUDE [prod_short](includes/prod_short.md)] oppdaterer kundens konto, finanspost og vareposter:

- For hver ordre opprettes en salgspost i **Finanspost**-tabellen. Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen. I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet.
- For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto). I tillegg registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.

Hvis du vil vite mer om bokføring av salg, kan du gå til [Bokføring av salg](ui-post-sales.md).

## Se også

[Bokføre salg](ui-post-sales.md)  
[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over salgsanalyse](sales-analytics-overview.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]