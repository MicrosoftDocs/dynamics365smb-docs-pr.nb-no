---
title: Ad-hoc-analyse av lagerdata
description: Lær hvordan du bruker dataanalysemodusen til å analysere lagerdata.
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

# <a name="ad-hoc-analysis-of-inventory-data"></a>Ad-hoc-analyse av lagerdata

Denne artikkelen forklarer hvordan du bruker funksjonen **Dataanlyse** til å analysere lagerdata direkte fra listesider og spørringer. Du trenger ikke å kjøre en rapport eller bytte til et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er "utgående lager" eller "toppselgere, eller andre visninger du kan tenke deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

Bruk følgende listesider til ad hoc-analyse av lagerprosesser:

- [Vareposter](https://businesscentral.dynamics.com/?page=38)

## <a name="inventory-ad-hoc-analysis-scenarios"></a>Scenarioer for ad hoc-analyse for lager

Bruk **Dataanalyse**-funksjonen for rask faktasjekking og ad hoc-analyse:

- Hvis du ikke vil kjøre en rapport.
- Hvis det ikke finnes en rapport for ditt spesifikke behov.
- Hvis du vil gjenta raskt for å få en god oversikt over en del av virksomheten din.

Avsnittene nedenfor inneholder eksempler på lagerscenarioer i [!INCLUDE [prod_short](includes/prod_short.md)].

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Lagerbeholdning](#example-inventory-on-hand) | Få en oversikt over varer som er tilgjengelige på lageret. | [Vareposter](https://businesscentral.dynamics.com/?page=38) | **Varenr.**, **Restantall** |
|[Eksempel: spor utløpende eller gammelt lager](#example-track-expiring-or-old-stock) | Få oversikt over varer på lageret ditt som har vært på lager lenge og ikke selger godt. | [Vareposter](https://businesscentral.dynamics.com/?page=38) | **Bokføringsdato (år)**, **Bokføringsdato (måned)**, **Varenr.**, **Bokføringsdato**, **Posttype**, **Antall** og **Restantall**. |
| [Returnerte varer etter returårsak](#example-returned-items-by-return-reason) | Få en oversikt over varer som kunder returnerer, kategorisert etter returårsak. Bruk dette til analyse for kvalitetskontroll. | [Vareposter](https://businesscentral.dynamics.com/?page=38) | **Returårsakskode**, **Bokføringsdato, Måned**, **Antall** , **Kostbeløp**, **Bokføringsdato**, **Bilagstype**, **Varenr.** og **Bilagsnr.**. |
| Lagergjennomstrømning | Få oversikt over kjøp og salg på lageret etter måned eller kvartal. | [Vareposter](https://businesscentral.dynamics.com/?page=38) | **Bokføringsdato (år)**, **Bokføringsdato**, **Varenr.**, **Antall**, **Salgsbeløp**, **Kostbeløp (faktisk)** og **Bokføringsdato (måned)** |
| [Lagerflyttinger] | Få oversikt over hvordan varer i lageret flyttes mellom lokasjoner. | [Vareposter](https://businesscentral.dynamics.com/?page=38) | **Lokasjonskode**, **Antall**, **Bokføringsdato**, **Varenr.** |

## <a name="example-inventory-on-hand"></a>Eksempel: Lagerbeholdning

Hvis du vil analysere varer i lagerbeholdningen som er på lager, gjør du følgende:

1. Åpne [Vareposter](https://businesscentral.dynamics.com/?page=38)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet ).
1. Dra feltet **Varenr** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltet **Restantall** til **Verdier**-området.
1. Sett filteret **Ikke lik** til **0** for **Restantall**. Hvis du ikke tillater negative lagernivåer, setter du et **Større enn**-filter til **0**.
1. Du kan eventuelt legge til andre felt i analysen og kanskje pivotere på lokasjon eller andre felt.
1. Endre navnet på analysefanen til **Tilgjengelig beholdning** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Eksempel på hvordan du utfører en lagerdataanalyse." lightbox="media/data-analysis-inventory-on-hand.png":::

## <a name="example-track-expiring-or-old-stock"></a>Eksempel: spor utløpende eller gammelt lager

Følg disse trinnene for å analysere varer på lageret ditt som har vært på lager lenge og ikke selger godt.

1. Åpne [Vareposter](https://businesscentral.dynamics.com/?page=38)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Dra feltene **Bokføringsdato (år)**, **Bokføringsdato (måned)** og **Varenr.** til området **Radgrupper**. Dra feltene i den rekkefølgen.
1. I **Kolonner**-området velger du feltene **Bokføringsdato**, **Posttype**, **Antall** og **Restantall**.
1. Sett et **Mindre enn**-filter til **Bokføringsdato** for å definere hva du mener med "gammel".
1. Endre navnet på analysefanen til **Gammelt lager** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Eksempel på hvordan du utfører dataanalyse på varelager som ikke kan selges, på siden Vareposter." lightbox="media/data-analysis-inventory-dead-stock.png":::

## <a name="example-returned-items-by-return-reason"></a>Eksempel: returnerte varer etter returårsak

Hvis du vil analysere returnerte varer sortert etter årsakene til returen, gjør du følgende:

1. Åpne listen [Vareposter](https://businesscentral.dynamics.com/?page=38).
1. Legg til **Returårsakskode**-feltet ved å tilpasse siden. På **Innstillinger**-menyen velger du **Tilpass**.
1. Avslutt tilpasningsmodus.
1. Velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Dra feltene **Returårsakskode** og **Bokføringsdatomåned** til **Radgrupper**-området. Dra feltene i den rekkefølgen.
1. Dra feltene **Antall** og **Kostbeløp** til **Verdier**-området.
1. Legg til eventuelle andre felt du vil ha med i analysen , og aktiver dem i **Kolonner**-området. Du kan for eksempel legge til feltene **Bokføringsdato**, **Bilagstype**, **Varenr.** og  **Bilagsnr.**.
1. Endre navnet på analysefanen til **Returnerte varer etter returårsak** eller noe som beskriver denne analysen.  

## <a name="example-inventory-throughput"></a>Eksempel: lagergjennomstrømning

1. Åpne [Vareposter](https://businesscentral.dynamics.com/?page=38)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Aktiver vekslebryteren **Pivot-modus** (over **Søk**-feltet til høyre).
1. Dra feltene **Bokføringsdato (år)**, **Bokføringsdato (måned)** og **Varenr.** til området **Radgrupper**.
1. Dra feltene **Antall**, **Salgsbeløp** og **Kostbeløp (faktisk)** til **Verdier**-området.
1. Dra feltet **Bokføringsdato (måned)** til **Kolonnegrupper**-området.
1. Endre navnet på analysefanen til **Lagergjennomstrømning etter måned** eller noe som beskriver denne analysen.  

## <a name="inventory-movements"></a>Lagerflyttinger

Hvis du vil spore lagerflyttinger mellom lokasjoner, gjør du følgende:

1. Åpne [Vareposter](https://businesscentral.dynamics.com/?page=38)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: for å aktivere analysemodus.
1. Gå til **Kolonner**-menyen og fjern alle kolonner (merk av i boksen ved siden av **Søk**-feltet til høyre).
1. Dra feltet **Lokasjonskode** til **Radgrupper**-området.
1. Dra feltet **Antall** til **Verdier**-området.
1. Legg til eventuelle andre felt du vil ha med i analysen , og aktiver dem i **Kolonner**-området. Du kan for eksempel legge til **Varenr**-feltet.
1. Endre navnet på analysefanen til **Lagerflyttinger** eller noe som beskriver denne analysen.  

   > [!TIP]
   > Hvis du legger til feltet Bokføringsdato, kan du også spore bevegelser over tid.

## <a name="data-foundation-for-ad-hoc-analysis-on-inventory"></a>Datagrunnlag for ad hoc-analyse på lager

Når du posterer en salgsordre, oppdaterer [!INCLUDE [prod_short](includes/prod_short.md)] kundens konto, finans og varepostene.

- For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjene inneholder varenumre). I tillegg registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**. Hvis du vil vite mer om bokføring av salg, kan du gå til [Bokføring av salg](ui-post-sales.md).

Når du bokfører et kjøpsdokument, oppdaterer [!INCLUDE [prod_short](includes/prod_short.md)] leverandørens konto, finans og vareposter, og ressursposter.

- For hver bestillingslinje opprettes poster i **Varepost**-tabellen (hvis bestillingslinjen er av typen Vare). I tillegg registreres alltid kjøpsdokumenter i tabellene **Mottakshode** og **Kjøpsfakturahode**. Hvis du vil finne ut mer, går du til [Bokføring av kjøp](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Se også

[Analyser liste- og spørringsdata med analysemodus](analysis-mode.md)  
[Oversikt over lageranalyse](inventory-analytics-overview.md)  
[Oversikt over analyse, forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Oversikt over lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
