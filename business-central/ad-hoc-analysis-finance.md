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

# <a name="ad-hoc-analysis-of-finance-data"></a>Ad hoc-analyse av finansdata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere finansdata direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er "Totale eiendeler over tid", "Kundefordringer", "Leverandørgjeld" eller andre visninger du kan forestille deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til å starte ad hoc-analyse av finansprosesser:

- [Finansposter](https://businesscentral.dynamics.com/?page=20)
- [Kundeposter](https://businesscentral.dynamics.com/?page=25)
- [Leverandørposter](https://businesscentral.dynamics.com/?page=29)

## <a name="finance-ad-hoc-analysis-scenarios"></a>Scenarioer for ad hoc-analyse for finans

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på finansscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Finans (kunde)](#example-finance-accounts-receivables) | Se hva kundene dine skylder deg, for eksempel inndelt i tidsintervaller for når beløp forfaller. | [Kundeposter](https://businesscentral.dynamics.com/?page=25) | **Kundenavn**, **Forfallsdato** og **Restbeløp** |
| [Finans (leverandør)](#example-finance-accounts-payable) | Se hva du skylder leverandørene, kanskje inndelt i tidsintervaller for når beløp forfaller. | [Leverandørposter](https://businesscentral.dynamics.com/?page=29) | **Leverandørnavn**, **Dokumenttype**, **Dokumentnr.**, **Forfallsdato (år)**, **Forfallsdato (måned)** og **Restbeløp**. |
| [Finans (resultatregnskap)](#example-finance-income-statement) | Se inntekten over inntektskontoene fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløpene ble bokført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bokføringsdato** og **Beløp**. |
| [Finans (objekter totalt)](#example-finance-total-assets) | Se objektene over objektkontoene fra kontoplanen, for eksempel inndelt i tidsintervaller for når beløpene ble bokført. | [Finansposter](https://businesscentral.dynamics.com/?page=20) | **Finanskontonr.**, **Bokføringsdato** og **Beløp**. |

### <a name="example-finance-accounts-receivables"></a>Eksempel: Finans (kunde)

Hvis du vil se hva kundene dine skylder deg, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne [Kundeposter](https://businesscentral.dynamics.com/?page=25)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av *Søk*-feltet til høyre).
1. Aktiver vekslebryteren **Pivot*-modus** (over **Søk**-feltet til høyre).
1. Dra **Kundenavn**-feltet til **Radgrupper**-området og dra **Restbeløp** til **Verdier**-området.
1. Dra feltet **Forfallsdato (måned)** til **Kolonneetiketter**-området.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).
1. Endre navnet på analysefanen til **Aldersfordelte kontoer etter måned** eller noe som beskriver denne analysen.

### <a name="example-finance-accounts-payable"></a>Eksempel: Finans (leverandør)

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

### <a name="example-finance-income-statement"></a>Eksempel: Finans (resultatregnskap)

Hvis du vil se inntekten over inntektskontoene fra kontoplanen, inndelt i tidsintervaller for når beløpene ble bokført, følg disse trinnene:

1. Åpne [Finansposter](https://businesscentral.dynamics.com/?page=20)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra **Finanskontonr.**-feltet til **Radgrupper**-området og dra **Beløp** til **Verdier**-området.
1. Dra feltet **Bokføringsdato (måned)** til **Kolonneetiketter**-området.
1. For resultatregnskapet filtrerer du på kontoene du bruker. I [!INCLUDE [prod_short](includes/prod_short.md)]-demodataene starter disse kontoene med "4", men kontoplanen din kan være annerledes. Angi et filter på passende kontoer på menyen **Analysefiltre** (under **Kolonner**-menyen til høyre).

   > [!TIP]
   > For å se hvilke kontoer som brukes i oppsettet, kjører rapporten [Råbalanse per periode](https://businesscentral.dynamics.com/?report=38).

1. Endre navnet på analysefanen til **Inntekt etter måned** eller noe som beskriver denne analysen.

### <a name="example-finance-total-assets"></a>Eksempel: Finans (objekter totalt)

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

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Datagrunnlag for ad hoc-analyse av finans

Når du bokfører kladder, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] poster i tabellen **Finanspost**. Derfor utføres ad hoc-analyse av generell finans vanligvis på siden [Finansposter](https://businesscentral.dynamics.com/?page=20). Når det gjelder kundefordringer og leverandørposter, kan du analysere henholdsvis [Kundeposter](https://businesscentral.dynamics.com/?page=25) og [Leverandørposter](https://businesscentral.dynamics.com/?page=29).

Du kan lære mer ved å gå til følgende artikler:

- [Datagrunnlag for ad hoc-analyse av salg](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Datagrunnlag for ad hoc-analyse av innkjøp](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Se også

[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over økonomisk analyse](bi.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Finansoversikt](finance.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
