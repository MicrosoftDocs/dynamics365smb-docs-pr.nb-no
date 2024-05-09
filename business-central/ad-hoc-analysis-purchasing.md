---
title: Ad hoc-analyser i innkjøp
description: Lær hvordan du bruker dataanalysemodusen til å analysere data i innkjøp.
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

# Ad hoc-analyser i innkjøp

Denne artikkelen forklarer hvordan du analyserer innkjøpsdata fra listesider og spørringer ved hjelp av funksjonen **Dataanalyse**. Funksjonen lar deg analysere data direkte fra siden, uten å måtte kjøre en rapport eller åpne et annet program, for eksempel Excel. Dataanalyse gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er Mine leverandører eller Innkjøpsstatistikk, eller andre visninger du kan tenke deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til ad hoc-analyse av kjøpsprosesser:

- [Bestillinger](https://businesscentral.dynamics.com/?page=9307)
- [Kjøpslinjer](https://businesscentral.dynamics.com/?page=518)
- [Bokførte kjøpsfakturaer](https://businesscentral.dynamics.com/?page=146)
- [Leverandørposter](https://businesscentral.dynamics.com/?page=29)
- [Finansposter](https://businesscentral.dynamics.com/?page=20)

## Ad hoc-analysescenarioer for innkjøp

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport
- Hvis det ikke finnes en rapport for dine spesifikke behov
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på innkjøpsscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Oversikt over GRNI](#example-goods-received-not-invoiced-grni-overview) | Få en oversikt over varer mottatt, ikke fakturert (GRNI) på tvers av leverandører. | **Type**, **Mottatt, ikke fakturert (beløp) (lokal valuta)** (filtrer etter disse feltene), **Leverandørnr.**, **Dokumentnr.**, **Nr**. og **Motatt ikke fakturert (beløp) (lokal valuta)** <br> **Obs!** Du må tilpasse siden for å legge til disse feltene. Hvis du vil finne ut mer, går du til [Tilpass arbeidsområdet](ui-personalization-user.md). | 
| [Finans (leverandør)](#example-finance-accounts-payable) | Se hva du skylder leverandørene, kanskje inndelt i tidsintervaller for når beløp forfaller. | [Leverandørposter](https://businesscentral.dynamics.com/?page=29) | **Leverandørnavn**, **Dokumenttype**, **Dokumentnr.**, **Forfallsdato (år)**, **Forfallsdato (måned)** og **Restbeløp**. |

## Eksempel: Oversikt over mottatte varer, ikke fakturert (GRNI)

Hvis du vil opprette en oversikt over mottatte, ikke fakturerte varer (GRNI) på tvers av leverandører, gjør du følgende:
 
1. Åpne listesiden [Kjøpslinjer](https://businesscentral.dynamics.com/?page=518).
1. Tilpass siden for å legge til feltet **Mottatt beløp, ikke fakturert**. Hvis du vil tilpasse siden, velger du **Innstillinger** og deretter **Tilpass**.
1. Aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. På menyen **Flere filtre** (til høyre på siden, rett under **Kolonner**-menyen) angir du følgende filtre:
    - **Type = Vare**
    - **Mottatt, ikke fakturert (lokal valuta) > 0**. 
1. Dra feltene **Leverandørnr.**, **Dokumentnr.** og **Nr.** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Legg til feltet **Mottatt, ikke fakturert (beløp) (lokal valuta)** for å ta det med i oversikten.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Flere filtre**. Menyen er til høyre på siden, rett under **Kolonner**-menyen.
1. Endre navnet på analysefanen til **Varer mottatt, ikke fakturert (GRNI)** eller noe som beskriver denne analysen for deg.

## Eksempel: Finans (leverandør)

Hvis du vil se du skylder leverandørene, kanskje inndelt i tidsintervaller for når beløp forfaller, følger du denne fremgangsmåten:

1. Åpne listesiden [Leverandørposter](https://businesscentral.dynamics.com/?page=29) og aktiver analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Aktiver **Pivotmodus** (rett over feltet **Søk**).
1. Dra feltene **Leverandørnavn**, **Dokumenttype** og **Dokumentnr.** til **Radgrupper**-området, og dra deretter **Restbeløp**-feltet til **Verdier**-området.
1. Dra feltene **Forfallsdato (år)** og **Forfallsdato (måned)** til **Kolonneetiketter**-området. Dra feltene i den rekkefølgen.
1. Hvis du vil utføre analysen for et gitt år eller kvartal, bruker du et filter på menyen **Flere filtre** (til høyre på siden, rett under **Kolonner**-menyen.)
1. Endre navnet på analysefanen til **Aldersfordelte leverandørkontoer etter måned** eller noe som beskriver denne analysen for deg.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Kundeposter." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## Datagrunnlag for ad hoc-analyse av innkjøp

Når bokfører et kjøpsdokument, oppdaterer [!INCLUDE [prod_short](includes/prod_short.md)] leverandørens konto, finans og vareposter, og ressursposter:

- For hvert kjøpsdokument opprettes det en kjøpspost i tabellen **Finanspost**. Det opprettes også en post på leverandørens konto i **Leverandørpost**-tabellen, og en finanspost opprettes i den relevante samlekontoen. I tillegg kan bokføring av kjøpet resultere i en mva-post og en finanspost for rabattbeløpet.
- Følgende poster blir opprettet for hver kjøpslinje, etter behov, i:
  - **Varepost**-tabellen hvis kjøpslinjen er av typen Vare.
  - **Finanspost**-tabellen hvis kjøpslinjen er av typen Finanskonto.
  - **Ressurspost**-tabellen hvis kjøpslinjen er av typen Ressurs.
- I tillegg registreres alltid kjøpsdokumenter i tabellene **Mottakshode** og **Kjøpsfakturahode**.

Hvis du vil finne ut mer, går du til [Bokføring av kjøp](purchasing-how-record-purchases.md#posting-purchases).

## Se også

[Bokføre kjøp](purchasing-how-record-purchases.md#posting-purchases)  
[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over kjøp](purchasing-manage-purchasing.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over kjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]