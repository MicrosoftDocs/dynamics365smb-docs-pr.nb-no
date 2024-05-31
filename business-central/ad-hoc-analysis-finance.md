---
title: Ad hoc-analyse av finansdata
description: Lær hvordan du bruker dataanalysemodusen til å analysere finansdata.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad hoc-analyse av finansdata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere finansdata direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er "Totale eiendeler over tid", "Kundefordringer", "Leverandørgjeld" eller andre visninger du kan forestille deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til å starte ad hoc-analyse av finansprosesser:

- [Finansposter](https://businesscentral.dynamics.com/?page=20)
- [Kundeposter](https://businesscentral.dynamics.com/?page=25)
- [Leverandørposter](https://businesscentral.dynamics.com/?page=29)

## Ad-hoc-analysescenarier i finans

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på finansscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
|[Eksempel: Finans (kundefordringer)](#example-finance-accounts-receivable) | Se hva kundene dine skylder deg, for eksempel inndelt i tidsintervaller for når beløp forfaller. | [Kundeposter](https://businesscentral.dynamics.com/?page=25) | **Kundenavn**, **Forfallsdato** og **Restbeløp** |
| [Finans (leverandør)](#example-finance-accounts-payable) | Se hva du skylder leverandørene, kanskje inndelt i tidsintervaller for når beløp forfaller. | [Leverandørposter](https://businesscentral.dynamics.com/?page=29) | **Leverandørnavn**, **Dokumenttype**, **Dokumentnr.**, **Forfallsdato (år)**, **Forfallsdato (måned)** og **Restbeløp**. |
| [Finans (salgsfakturaer etter finanskonto)](#example-finance-sales-invoices-by-gl-account) | Se hvordan salgsfakturaene distribueres over finanskonti fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløp ble bokført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonavn**, **Kildespor**, **Finanskontonavn**, **Finanskontonr.**, **Debetbeløp**, **Kreditbeløp**, **Bokføringsdato år**, **Bokføringsdato, Kvartal** og **Bokføringsdato Måned** |
| [Finans (resultatregnskap)](#example-finance-income-statement) | Se inntekten over inntektskontoene fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløpene ble bokført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bokføringsdato** og **Beløp**. |
| [Finans (objekter totalt)](#example-finance-total-assets) | Se objektene over objektkontoene fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløpene ble bokført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bokføringsdato** og **Beløp**. |

### Eksempel: Finans (kundefordringer)

Hvis du vil se hva kundene dine skylder deg, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne [Kundeposter](https://businesscentral.dynamics.com/?page=25)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av *Søk*-feltet til høyre).
1. Aktiver vekslebryteren **Pivot*-modus** (over **Søk**-feltet til høyre).
1. Dra **Kundenavn**-feltet til **Radgrupper**-området og dra **Restbeløp** til **Verdier**-området.
1. Dra feltet **Forfallsdato (måned)** til **Kolonneetiketter**-området.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).
1. Endre navnet på analysefanen til **Aldersfordelte kontoer etter måned** eller noe som beskriver denne analysen.

### Eksempel: Finans (leverandør)

Hvis du vil se du skylder leverandørene, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne listesiden [Leverandørposter](https://businesscentral.dynamics.com/?page=29) og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra feltene **Leverandørnavn**, **Dokumenttype** og **Dokumentnr.** til **Radgrupper**-området, og dra deretter **Restbeløp**-feltet til **Verdier**-området.
1. Dra feltene **Forfallsdato (år)** og **Forfallsdato (måned)** til **Kolonneetiketter**-området. Dra feltene i den rekkefølgen.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).
1. Endre navnet på analysefanen til **Aldersfordelte leverandørkontoer etter måned** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Kundeposter." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### Eksempel: Finans (salgsfakturaer etter finanskonto)

Hvis du vil se hvordan salgsfakturaene fordeler seg over finanskonti fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløp ble bokført, gjør du følgende:

1.  [Åpne siden Finansposter](https://businesscentral.dynamics.com/?page=20) .
1. Legg til feltene **Finanskontonavn** og **Kildekode** ved å tilpasse siden. På **Innstillinger**-menyen velger du **Tilpass**.
1. Avslutt tilpasningsmodus.
1. Velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. På **menyen Analysefiltre** setter du et filter i **feltet Kildespor** til **SALG**. Hvis du har tilpasninger som legger til andre verdier, kan du legge til disse også.
1. På **Kolonner**-menyen fjerner du alle kolonner (merk av i boksen ved siden av **Søk**-feltet).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra **finanskontonavnet** og **finanskontonummeret.** -felt til Radgrupper-området **·** .
1. Dra feltene Debetbeløp og Kreditbeløp **til Verdier-området**  **.**  **·** 
1. Dra feltene **Bokføringsdato, År**, **Bokføringsdato, Kvartal** og **Bokføringsdato måned** til **Kolonneetiketter-området** .
1. Endre navnet på analysefanen til **Fakturaoppdeling etter konto**, eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-gl-entries-invoices.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Finansposter (for å forstå salgsbokføringer)." lightbox="media/data-analysis-gl-entries-invoices.png":::

### Eksempel: Finans (resultatregnskap)

Hvis du vil se inntekten over inntektskontoene fra kontoplanen, inndelt i tidsintervaller for når beløpene ble bokført, følg disse trinnene:

1. Åpne [Finansposter](https://businesscentral.dynamics.com/?page=20)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra **Finanskontonr.**-feltet til **Radgrupper**-området og dra **Beløp** til **Verdier**-området.
1. Dra feltet **Bokføringsdato (måned)** til **Kolonneetiketter**-området.
1. For resultatregnskapet filtrerer du på kontoene du bruker. I [!INCLUDE [prod_short](includes/prod_short.md)]-demodataene starter disse kontoene med "4", men kontoplanen din kan være annerledes. Angi et filter på passende kontoer på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).

   > [!TIP]
   > For å se hvilke kontoer som brukes i oppsettet, kjører rapporten [Råbalanse per periode](https://businesscentral.dynamics.com/?report=38).

1. Endre navnet på analysefanen til **Inntekt etter måned** eller noe som beskriver denne analysen.

### Eksempel: Finans (objekter totalt)

Hvis du vil se objektene over objektkontoene fra kontoplanen, inndelt i tidsintervaller for når beløpene ble bokført, gjør du følgende:

1. Åpne [Finansposter](https://businesscentral.dynamics.com/?page=20)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra **Finanskontonr.**-feltet til **Radgrupper**-området og dra **Beløp** til **Verdier**-området.
1. Dra feltet **Bokføringsdato (måned)** til **Kolonneetiketter**-området.
1. For oversikten over totale objekter filtrerer du på kontoene du bruker. I [!INCLUDE [prod_short](includes/prod_short.md)]-demodataene starter disse kontoene med "10", men kontoplanen din kan være annerledes. Angi et filter på passende kontoer på menyen **Flere filtre** (til høyre under **Kolonner**-menyen.)

   > [!TIP]
   > For å se hvilke kontoer som brukes i oppsettet, kjører rapporten [Råbalanse per periode](https://businesscentral.dynamics.com/?report=38).

1. Endre navnet på analysefanen til **Inntekt etter måned** eller noe som beskriver denne analysen.

## Datagrunnlag for ad hoc-analyse av finans

Når du bokfører kladder, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] poster i tabellen **Finanspost**. Derfor utføres ad hoc-analyse av generell finans vanligvis på siden [Finansposter](https://businesscentral.dynamics.com/?page=20). Når det gjelder kundefordringer og leverandørposter, kan du analysere henholdsvis [Kundeposter](https://businesscentral.dynamics.com/?page=25) og [Leverandørposter](https://businesscentral.dynamics.com/?page=29).

Du kan lære mer ved å gå til følgende artikler:

- [Datagrunnlag for ad hoc-analyse av salg](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Datagrunnlag for ad hoc-analyse av innkjøp](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## Se også

[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over økonomisk analyse](bi.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]