---
title: Konfigurere selskapskonsolidering
description: Lær hvordan du kan konfigurere hvordan data fra ulike selskaper i Business Central rapporteres til et konsolideringsselskap.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 453cebcddb1fdfd2f3127fd08548deccc8fe1876
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8512207"
---
# <a name="set-up-company-consolidation"></a>Konfigurere selskapskonsolidering

Før du kan konsolidere finanspostene for to eller flere separate selskaper (datterselskaper) i et konsolidert selskap, må du klargjøre kontoplanen og konsolideringsselskapet.  

Det finnes to måter å definere konsolideringen på, avhengig av forretningenes kompleksitet:

* Hvis du ikke trenger avanserte innstillinger, for eksempel inkludere et selskap som du bare eier en del av, kan du bruke veiledningen **Selskapskonsolidering** med assistert oppsett for å definere en konsolidering raskt. Veiledningen hjelper deg gjennom de grunnleggende trinnene.
* Hvis du trenger mer avanserte innstillinger, kan du definere det konsoliderte selskapet og konsernene selv.
  * I hvert konsern angir du hvilke finanskonti som skal inkluderes i konsolideringen, og angir konsolideringsoversettelsesmetoden for hver konto.
  * I konsolideringsselskapet definerer du et konsernkort for hvert selskap som skal inkluderes i konsolideringen. Konsernkortet inneholder informasjon som datoene for konsernets regnskapsår, og hvor stor prosentandel av hver konto som skal inkluderes i konsolideringen.

## <a name="simple-consolidation-setup"></a>Enkelt konsolideringsoppsett

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Hvis konsolideringen er enkel, for eksempel fordi du er eneeier av konsernene som skal konsolideres, vil veiledningen **Selskapskonsolidering** med assistert oppsett hjelpe deg gjennom følgende trinn:

* Velg om du vil opprette et nytt konsolidert selskap eller om du vil konsolidere dataene i et selskap som allerede er opprettet for konsolidering. Selskapet kan ikke inneholde transaksjoner.
* Forhåndsvis resultatene. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer at hoveddata og transaksjoner kan bli overført til det konsoliderte selskapet.

Hvis du vil bruke veiledningen med assistert oppsett, gjør du følgende:

1. I **Regnskapsfører**-rollesenteret velger du **Assistert oppsett**.
2. Velg **Konfigurer konsolideringsrapportering**, og fullfør deretter hvert trinn i veiledningen med assistert oppsett.

## <a name="advanced-consolidation-setup"></a>Avansert konsolideringsoppsett

Hvis du trenger mer avanserte innstillingene for konsolideringen, kan du definere konsolideringen manuelt. For eksempel hvis du har selskaper som du bare eier delvis, eller hvis du har selskaper som du ikke vil ta med i konsolideringen.  

### <a name="set-up-the-consolidated-company"></a>Konfigurer det konsoliderte selskapet

Du må først definere det konsoliderte selskapet. Du definerer det konsoliderte selskapet på samme måte som du definerer andre selskaper. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

Følgende oversikt illustrerer viktige aspekter ved det konsoliderte selskapet.

1. Definere kontoplanen

    Hvis du vil ha mer informasjon, kan du se [Definere eller endre kontoplanen](finance-setup-chart-accounts.md).  

    Kontoplanene kan være like på tvers av konsernet og det konsoliderte selskapet, eller det konsoliderte selskapet kan ha en annen kontoplan. Hvis et konserns kontoplan er forskjellig fra den i det konsoliderte selskapet, må du angi tilordningen mellom kontoer i kontoene i konsernet. Hvis du vil ha mer informasjon, kan du se delen [Klargjøre finanskonti for konsolidering](#glacc).

2. Legge til konsern

    Hvis du vil konsolidere økonomiske data fra flere selskaper i et konsolidert selskap, må du angi informasjon om datterselskapene som konsern som skal inkluderes, og om hvor mye av tallene skal inkluderes.

    Hvis du vil ha mer informasjon, kan du se delen [Legge til konsern](#busunit).
3. Du kan angi valutakurser ved konsolidering av årsregnskapet for konsern, hvis årsregnskapene er i en utenlandsk valuta.

    De tre valutakursene som brukes, er **Gjennomsnittskurs (manuell)**, **Sluttkurs** og **Siste sluttkurs**. Hvis du vil ha mer informasjon, kan du se delen [Angi valutakurser for konsolideringer](#exchrates).
4. Du kan konsolidere dimensjonsinformasjon og finanskontoer.

    Hvis du vil ha mer informasjon, kan du se delen [Inkludere eller utelate dimensjoner](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Legge til konsern

[!INCLUDE[prod_short](includes/prod_short.md)] lar deg sette opp en liste over konsern som skal konsolideres, bekrefte regnskapsdataene før du konsoliderer dem, importere filer og generere konsolideringsrapporter.  

1. Logg deg på det konsoliderte selskapet.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Velg **Ny**, og fyll deretter ut de obligatoriske feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Når du fyller ut feltene **Startdato** og **Sluttdato**, kontrollere at du overholde GAAP-reglene for regnskapsperiodene i konsernet kontra moderselskapet.
4. Gjenta trinn 3 for hvert ekstra konsern

Hvis konsernet bruker en fremmed valuta, må du angi hvilken valutakurs som skal brukes i konsolideringen. Du må også angi konsolideringsopplysninger om konsernets finanskonti. Disse prosessene beskrives nedenfor.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Klargjøre finanskonti for konsolidering

Kontoplanen for et selskap som skal konsolideres, må angi kontoer for konsolidering. For hver finanskonto det bokføres til i hvert selskap, må du angi finanskontoen i det konsoliderte selskapet som saldoen skal overføres til ved konsolidering. Dette er en tilknytning som gjør at selskaper med ulike kontoplaner kan konsolideres sammen.

Hvis kontoplanen i konsernet er forskjellig fra det konsoliderte selskapet, må du klargjøre finanskonti for konsolidering. Du kan angi kontiene for å bokføre debet og kredit og metoden som skal brukes til å oversette valutaer i det konsoliderte selskapet. Dette er for eksempel nyttig hvis du kjører rapporten ofte.

1. I hvert konserns [!INCLUDE [prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. Åpne kortet for kontoen, og deretter fyller du ut feltene på **Konsolidering**-hurtigfanen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Angi valutakurser for konsolideringer

Hvis et konsern bruker en annen valuta enn det konsoliderte selskapet, må du angi valutakursmetoder for hver konto før du konsoliderer. For hver konto bestemmer innholdet i feltet **Kons. oversettelsesmetode** valutakursen. I det konsoliderte selskapet på hvert konsernkort angir du i **Valutakurstabell**-feltet om konsolidering skal bruke valutakurser fra konsernselskapet eller det konsoliderte selskapet. Hvis du bruker valutakurser fra det konsoliderte selskapet, kan du endre valutakursene for et konsern. For konserner, hvis feltet **Valutakurstabell** på konsernkortet inneholder **Lokal**, kan du endre valutakursen fra konsernkortet. Valutakurser kopieres fra **Valutakurs**-tabellen, men du kan endre dem før konsolidering.

Tabellen nedenfor beskriver valutakursmetodene du kan bruke for kontoer.

|Valutakurs | Vanlig bruk |
|---|---|
|Gjennomsnittskurs (manuell) | Du beregner gjennomsnittskursen manuelt for perioden som skal konsolideres. Beregn gjennomsnittet som et aritmetisk gjennomsnitt eller som et best mulig overslag, og angi resultatet for hvert konsern. Brukes for resultatregnskapskonti.|
|Sluttkurs | Brukes for balansekonti.|
|Siste sluttkurs | Kursen som gjaldt på valutamarkedet på datoen som balansen eller resultatregnskapet forberedes for. Du angir denne kursen for hvert konsern. Brukes for balansekonti.|
|Historisk kurs | Valutakursen som var gyldig da transaksjonen ble utført.|
|Sammensatt kurs | Gjeldende periodebeløp omregnes med gjennomsnittskursen og legges til i den tidligere registrerte balansen i det konsoliderte selskapet. Denne metoden brukes vanligvis for konti for fri egenkapital fordi de inkluderer beløp fra forskjellige perioder og består dermed av en sammensetning av beløp som er omregnet med forskjellig valutakurs.|
|Egenkapitalkurs | Dette ligner på **Sammensatt**. Forskjellene bokføres på separate finanskonti.|

Du kan angi valutakurser for konserner ved å gjøre følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
2. På siden **Konsernoversikt** velger du konsernet og velger deretter **Gjennomsnittskurs (manuell)**.  
3. På siden **Endre valutakurs** har innholdet i feltet **Tilhørende valutakursbeløp** blitt kopiert fra **Valutakurs**-tabellen, men du kan endre det. Lukk siden.  
4. Velg handlingen **Sluttkurs**.  
5. I feltet **Tilhørende valutakursbeløp** angir du valutakursen.

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Inkludere eller utelate dimensjoner

Du kan konsolidere dimensjonsinformasjon og finanskontoer.

* I de aktuelle dimensjonene angir du **Konsolideringskode**-feltet eller lar det stå tomt
  * Hvis du vil utelate en dimensjon i konsolideringen, lar du **Konsolideringskode**-feltet stå tomt på dimensjonen og velger ikke dimensjoner i **Kopier dimensjoner**-feltene i noen konsolideringsfunksjoner eller -rapporter.
  * Hvis du vil inkludere dimensjonsopplysninger i konsolideringen, lar du **Konsolideringskode**-feltet stå tomt. Konsolideringen vil imidlertid bare fungere hvis dimensjonsverdiene i konsernet er de samme som i det konsoliderte selskapet.
  * Hvis du vil konsolidere dimensjonsverdikoden i konsernet med en annen dimensjonsverdikode i det konsoliderte selskapet, fyller du ut **Konsolideringskode**-feltet i de relevante dimensjonene.  
* Legge til de relevante dimensjonene i de aktuelle finanskontiene

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Utelate et selskap fra konsolidering

Hvis du ikke vil ta med et konsern i konsolideringen, kan du utelate det. Hvis du vil gjøre dette, går du til konsernkortet og fjerner merket for **Konsolider**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Inkludere et delvis eid selskap i konsolideringen

Hvis du bare eier en del av et selskap, kan du ta med en prosentandel av hver enkelt transaksjon som samsvarer med prosentdelen av selskapet du eier. Hvis du for eksempel eier 70 % av selskapet, vil konsolideringen inkludere 70 kr av en faktura på 100 kr. For å angi hvor stor del av selskapet du eier, går du til konsernkortet og skriver inn prosentsatsen i feltet **Konsoliderings-%**.  

## <a name="see-also"></a>Se også

[Konsolidere finansielle data fra flere selskaper](finance-consolidated-company-reporting.md)  
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdataene til Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]