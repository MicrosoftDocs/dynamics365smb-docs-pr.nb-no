---
title: Konfigurere selskapskonsolidering
description: Lær hvordan du kan konfigurere hvordan data fra ulike selskaper i Business Central rapporteres til et konsolideringsselskap.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# <a name="set-up-company-consolidation"></a>Konfigurer selskapskonsolidering

Før du kan konsolidere finanspostene for to eller flere selskaper (datterselskaper) i et konsolidert selskap, må du klargjøre kontoplanen og konsolideringsselskapet.  

Det finnes to måter å definere konsolideringen på, avhengig av forretningenes kompleksitet:

* Hvis du ikke trenger avanserte innstillinger, for eksempel inkludere et selskap som du bare eier en del av, kan du bruke veiledningen **Selskapskonsolidering** med oppsett for å definere en konsolidering raskt. Veiledningen hjelper deg gjennom de grunnleggende trinnene.
* Hvis du trenger mer avanserte innstillinger, kan du definere det konsoliderte selskapet og konsernene selv.
  * I hvert konsern angir du hvilke finanskonti som skal inkluderes i konsolideringen, og oversettelsesmetoden for hver konto.
  * I det konsoliderte selskapet definerer du forretningsenhetskortet for hvert selskap som skal inkluderes i konsolideringen. Konsernkortet inneholder informasjon som datoene for konsernets regnskapsår, og hvor stor prosentandel av hver konto som skal inkluderes i konsolideringen.

## <a name="simple-consolidation-setup"></a>Enkelt konsolideringsoppsett

Hvis konsolideringen er enkel, for eksempel fordi du er eneeier av konsernene som skal konsolideres, vil veiledningen **Selskapskonsolidering** hjelpe deg gjennom følgende trinn:

* Opprett et nytt konsolidert selskap, eller konsolider et selskap du allerede har opprettet. Selskapet kan ikke inneholde transaksjoner.
* Forhåndsvis resultatene. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer at du kan overføre hoveddata og transaksjoner til det konsoliderte selskapet.

Hvis du vil bruke veiledningen med assistert oppsett, gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen.
2. Velg **Behandle konsolideringer**, og fullfør deretter hvert trinn i Selskapskonsolidering-veiledningen med assistert oppsett.

## <a name="advanced-consolidation-setup"></a>Avansert konsolideringsoppsett

Hvis du trenger mer avanserte innstillingene for konsolideringen, kan du definere konsolideringen manuelt. For eksempel hvis du har selskaper som du eier delvis, eller hvis du har selskaper som du ikke vil ta med i konsolideringen.  

### <a name="set-up-the-consolidated-company"></a>Konfigurer det konsoliderte selskapet

Du må først definere det konsoliderte selskapet. Du definerer det konsoliderte selskapet på samme måte som du definerer andre selskaper. Hvis du vil lære mer om hvordan du definerer et selskap, kan du gå til [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

Følgende oversikt illustrerer viktige aspekter ved det konsoliderte selskapet.

1. Definere kontoplanen.

    Hvis du vil lære mer om hvordan du definerer en kontoplan, går du til [Definere eller endre kontoplanen](finance-setup-chart-accounts.md).  

    Kontoplanene kan være like på tvers av konsernet og det konsoliderte selskapet, eller det konsoliderte selskapet kan ha en annen kontoplan. Hvis et konserns kontoplan er forskjellig fra den i det konsoliderte selskapet, må du angi tilordningen for kontoene til kontoene i forretningsenheten. Hvis du vil ha mer informasjon, kan du se gå til delen [Klargjøre finanskonti for konsolidering](#glacc).

2. Legge til konsern.

    Hvis du vil konsolidere dataene for flere selskaper, må du definere datterselskapene som konsern og angi hvor mye av saldoen som skal inkluderes. Hvis du vil lære mer om konsern, kan du gå til delen [Legge til konsern](#busunit).

3. Angi valutakurser om nødvendig.

    Angi valutakurser hvis du vil konsolidere data for konsern som bruker forskjellige valutaer. De tre valutakursene som brukes, er **Gjennomsnittskurs (manuell)**, **Sluttkurs** og **Siste sluttkurs**. Hvis du vil lære mer om valutakurser, kan du gå til delen [Angi valutakurser for konsolideringer](#exchrates).

4. Konsolidere dimensjonsinformasjon og finanskontoer.

    Hvis du vil ha mer informasjon, kan du se delen [Inkludere eller utelate dimensjoner](#dim).

### <a name="add-business-units"></a><a name="busunit"></a>Legge til konsern

I det konsoliderte selskapet konfigurerer du hvert selskap som du vil konsolidere data fra som et konsern. Før du kjører en konsolidering og genererer konsolideringsrapporten, er det lurt å kontrollere de økonomiske dataene i hvert konsern.

En stor del av oppsettet av konsernet er å angi hvordan enheten skal dele sine økonomiske data med det konsoliderte selskapet. Det finnes manuelle og automatiske alternativer:

* Hvis du vil bruke en manuell prosess, kan du eksportere en XML-fil som inneholder enhetens finansposter, for [!INCLUDE [prod_short](includes/prod_short.md)] online og lokalt Deretter importerer du filen i det konsoliderte selskapet.
* For å automatisere datautvekslingen, kan du for [!INCLUDE [prod_short](includes/prod_short.md)] online bruke en API som [!INCLUDE [prod_short](includes/prod_short.md)] gir mulighet til å dele data på tvers av miljøer. Hvis selskapene er i samme miljø, kan du bruke alternativet **Database**.

> [!NOTE]
> API-alternativet lar deg også dele økonomimoduloppføringer fra andre [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Hvis du vil bruke API-alternativet, må brukeren som konfigurerer konsolideringen, ha tillatelse til å få tilgang til finansposter. Tillatelsessettene D365 Basic og D365 Read gir for eksempel tilgang.

#### <a name="set-up-business-unit-currencies"></a>Konfigurer konsernvalutaer

Når du kjører konsolidering for konsern som bruker en utenlandsk valuta, må du være spesielt oppmerksom på valutakursene som brukes i ulike deler av prosessen, og enda mer når du kjører konsolideringen på nytt. Dette gjør du ved å bruke siden **Konfigurer konsernvalutaer** til å holde oversikt over kursene på en enkel måte.

Siden **Konfigurer konsernvalutaer** gir deg de siste kursene for gjennomsnittsvaluta, sluttkurs og siste sluttkurs. Du kan slå opp valutakursene i valutakurstabellen, noe som gjør det enklere å validere kurser. Du kan endre kursene for nåværende kjøring ved å angi verdiene eller kopiere dem fra tidligere kjøringer. Hvis du vil kopiere kursene, velger du **Velg blant tidligere konsolideringer**. Denne siden er spesielt nyttig når du vil kjøre en tidligere konsolidering på nytt, der du må bruke en tidligere sluttkurs. Dette er nødvendig for å revaluere balansepostene riktig. Siden **Velg blant tidligere konsolideringer** er også nyttig hvis du bare vil vise kursene som ble brukt, for eksempel når du feilsøker. Siden er filtrert etter kjøringer som inkluderte det valgte konsernet.

Du starter satsjobben **Kjør konsolidering** fra listesiden **Konsern**. Du finner også siden **Konfigurer konsernvalutaer** ved å velge handlingen **Valutakurser**.

> [!NOTE]
> Sidene for valutakursoppsett for gjennomsnittskurs, sluttkurs og siste sluttkurs som for øyeblikket er tilgjengelige på kortet **Konsern**, blir avskrevet i en fremtidig versjon. Du kan imidlertid fortsatt opprettholde disse kursene hvis du har konsern som du importerer via filer.

#### <a name="create-a-business-unit"></a>Opprett et konsern

1. Logg deg på det konsoliderte selskapet.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
3. Velg **Ny**, og deretter fyller du ut de nødvendige feltene i hurtigfanene **Generelt** og **Finanskontoer**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > Når du fyller ut feltene **Startdato** og **Sluttdato**, kontrollere at du overholde GAAP-reglene for regnskapsperiodene i konsernet kontra moderselskapet.
4. På hurtigfanen **Dataimport** i felltet **Standard dataimport**, angir du hvordan du vil dele finansposter med det konsoliderte selskapet:

   * Hvis du vil dele data mellom selskaper i samme miljø, velger du **Database**.
   * Hvis du vil dele data mellom selskaper i forskjellige miljøer, velger du **API** og fyller deretter ut feltet **API-ens endepunkt** .
        
        Du henter URL-adressen for endepunktet ved å åpne konsernselskapets [!INCLUDE [prod_short](includes/prod_short.md)], åpner **Konsernkort** og velger handlingen **Oppsett**. 
   * Hvis du vil eksportere en XML-fil og dele den manuelt, velger du **Filformat**.

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a>Klargjøre finanskonti for konsolidering

Kontoplanen for et selskap som skal konsolideres, må angi kontoer for konsolidering. For hver finanskonto det bokføres til i hvert selskap, må du angi finanskontoen i det konsoliderte selskapet som saldoen skal overføres til. Med denne tilordningen kan du konsolidere selskaper som har ulike kontoplaner.

Hvis kontoplanen i konsernet er forskjellig fra det konsoliderte selskapet, må du klargjøre finanskonti for konsolidering. Du kan angi kontiene for å bokføre debet og kredit og metoden som skal brukes til å oversette valutaer i det konsoliderte selskapet.

1. I hvert konserns [!INCLUDE [prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. Åpne kortet for kontoen, og deretter fyller du ut feltene på **Konsolidering**-hurtigfanen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Hvis du ikke fyller ut feltene **Konsolidert debetkonto** og **Konsolidert kredittkonto**, antar [!INCLUDE [prod_short](includes/prod_short.md)] at de er tildelt til de samme kontoene i det konsoliderte selskapet.

> [!TIP]
> Det kan være scenarioer der du ikke vil inkludere en konto i en konsolidering. Hvis du for eksempel vil at konsolideringsselskapet bare skal gjenspeile balansen fra datterselskapene. Hvis du vil ekskludere en konto fra konsolidering, aktiverer du veksleknappen **Utelat fra konsolidering** for kontoen.

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a>Angi valutakurser for konsolideringer

Hvis et konsern bruker en annen valuta enn det konsoliderte selskapet, må du angi valutakursmetoder for hver konto før du konsoliderer. For hver konto bestemmer innholdet i feltet **Kons. oversettelsesmetode** valutakursen. I det konsoliderte selskapet på hvert konsernkort angir du i feltet **Valutakurstabell** om konsolidering skal bruke valutakurser fra konsernselskapet eller det konsoliderte selskapet. Hvis du bruker valutakurser fra det konsoliderte selskapet, kan du endre valutakursene for et konsern. For konserner, hvis feltet **Valutakurstabell** på konsernkortet inneholder **Lokal**, kan du endre valutakursen fra konsernkortet. Valutakurser kopieres fra **Valutakurs**-tabellen, men du kan endre dem før konsolidering.

Tabellen nedenfor beskriver valutakursmetodene du kan bruke for kontoer.

|Valutakurs | Vanlig bruk |
|---|---|
|Gjennomsnittskurs (manuell) | Du beregner gjennomsnittskursen manuelt for perioden som skal konsolideres. Beregn gjennomsnittet som et aritmetisk gjennomsnitt eller som et best mulig overslag, og angi resultatet for hvert konsern. Bruke for resultatregnskapskonti.|
|Sluttkurs | Brukes for balansekonti.|
|Siste sluttkurs | Kursen som gjaldt på valutamarkedet på datoen som balansen eller resultatregnskapet forberedes for. Du angir denne kursen for hvert konsern. Bruke for balansekonti.|
|Historisk kurs | Valutakursen som var gyldig da transaksjonen ble utført.|
|Sammensatt kurs | Gjeldende periodebeløp omregnes med gjennomsnittskursen og legges til i den tidligere registrerte balansen i det konsoliderte selskapet. Du bruker vanligvis denne metoden for kontoer for fri egenkapital. Disse kontoene inkluderer beløp fra forskjellige perioder, så de inneholder beløp omregnet med forskjellige valutakurser.|
|Egenkapitalkurs | Dette alternativet lingner på **Sammensatt**. Forskjellene bokføres på separate finanskonti.|

Du kan angi valutakurser for et konsern ved å gjøre følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsern**, og velg deretter den relaterte koblingen.  
2. På siden **Konsernoversikt** velger du konsernet og velger deretter handlingen **Valutakurser**.  
3. På siden **Konfigurer konsernvalutaer** fyller du ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a>Inkludere eller utelate dimensjoner

Du kan konsolidere dimensjonsinformasjon og finanskontoer.

* I dimensjonene angir du **Konsolideringskode**-feltet eller lar det stå tomt.
  * Hvis du vil utelate en dimensjon i konsolideringen, lar du **Konsolideringskode**-feltet stå tomt på dimensjonen og velger ikke dimensjoner i **Kopier dimensjoner**-feltene i noen konsolideringsfunksjoner eller -rapporter.
  * Hvis du vil inkludere dimensjonsopplysninger i konsolideringen, lar du **Konsolideringskode**-feltet stå tomt. Konsolideringen vil imidlertid bare fungere hvis dimensjonsverdiene i konsernet er de samme som i det konsoliderte selskapet.
  * Hvis du vil konsolidere dimensjonsverdikoden i konsernet med en annen dimensjonsverdikode i det konsoliderte selskapet, fyller du ut **Konsolideringskode**-feltet i dimensjonene.  
* Legge til dimensjonene i finanskontiene.

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a>Utelate et selskap fra konsolidering

Hvis du ikke vil ta med et konsern i konsolideringen, kan du utelate det. Hvis du vil gjøre dette, går du til konsernkortet og fjerner merket for **Konsolider**.

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a>Inkludere et delvis eid selskap i konsolideringen

Hvis du bare eier en del av et selskap, kan du ta med en prosentandel av hver enkelt transaksjon som reflekterer prosentdelen av selskapet du eier. Hvis du for eksempel eier 70 % av selskapet, vil konsolideringen inkludere 70 kr av en faktura på 100 kr. For å angi hvor stor del av selskapet du eier, går du til konsernkortet og skriver inn prosentsatsen i feltet **Konsoliderings-%**.  

## <a name="see-also"></a>Se også

[Konsolidere finansielle data fra flere selskaper](finance-consolidated-company-reporting.md)  
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdataene til Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
