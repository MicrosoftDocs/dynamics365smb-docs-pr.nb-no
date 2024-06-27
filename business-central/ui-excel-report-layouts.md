---
title: Arbeid med Excel-oppsett
description: Lær hvordan du oppretter og endrer rapportoppsett som er bygd ved hjelp av Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 05/30/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Arbeid med Microsoft Excel-oppsett

Oppsett for Microsoft Excel-rapporter er basert på Excel-arbeidsbøker (XLSX-filer). Med dem kan du opprette rapporter som omfatter velkjente Excel-funksjoner for oppsummering, analyse og presentasjon av data for eksempel formler, pivottabeller, pivotdiagrammer.

![Viser et eksempel på et Excel-oppsett.](media/excel-layout-2.png)

Denne artikkelen forklarer noen av de viktigste tingene du må vite for å komme i gang med Excel-oppsett.

## Hvorfor bruke Excel-oppsett?

Fordeler ved å bruke Excel-oppsett:

- Opprett interaktive rapporter ved hjelp av effekter som slicere.
- Vis rådata fra rapportdatasettet som hjelper deg med å forstå hvordan rapporten fungerer, og hvor dataene i visuelle effekter kommer fra.
- Bruk innebygde Microsoft Office-funksjoner til å utføre etterbehandling på gjengitte rapporter, inkludert:
  - [Beskytt regneark](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Bruk følsomhetsetiketter](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Legg til kommentarer og merknader](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognose og analyse](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Bruk installerte tillegg og programintegreringer, for eksempel Power Automate-flyter eller OneDrive.

> [!TIP]
> Når OneDrive-integreringen er konfigurert, kopieres Excel-arbeidsbokfilen til OneDrive og åpnes deretter i Excel Online når du kjører en rapport med et Excel-oppsett. Hvis du vil ha mer informasjon, kan du se [Lagre Excel-arbeidsbøker og rapportfiler i OneDrive](./across-onedrive-overview.md#save-excel-workbooks-and-report-files-in-onedrive)

## Kom i gang

Det finnes hovedsakelig to oppgaver involvert i konfigurasjonen av et Excel-oppsett i en rapport:

1. Opprett den nye filen for Excel-oppsett.
2. Legg til det nye oppsettet i rapporten.

## Oppgave 1: Opprett filen for Excel-oppsett

Dette er tre måter å opprette en Excel-oppsettsfil for en rapport på.

### [Fra en rapport](#tab/any-report)

Følg denne fremgangsmåten til å opprette et Excel-oppsett fra alle rapporter, uavhengig av gjeldende oppsettstype. Excel-oppsettet inneholder det nødvendige **Data**-arket og den nødvendige tabellen, et **Rapportmetadata**-ark og ingenting annet.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. På siden **Rapportoppsett** velger du et oppsett for rapporten, og deretter velger du **Kjør rapport**-handlingen.
3. På rapportens forespørselsside velger du **Send til** > **Microsoft Excel-dokument (bare data)** > **OK**.

   Dette trinnet laster ned en Excel-arbeidsbok som inneholder datasettet for rapport.
4. Åpne den nedlastede filen i Excel, gjør endringene og lagre deretter filen.

### [Fra et annet Excel-rapportoppsett](#tab/other-layout)

Hvis det allerede finnes et Excel-oppsett for en rapport, kan du bruke det eksisterende oppsettet som et utgangspunkt. Det finnes to tilnærminger for å få en kopi av oppsettet. Du kan eksportere det eksisterende oppsettet fra siden **Rapportoppsett**, eller du kan laste ned oppsettet fra rapportens forespørselsside. Begge måter laster ned en Excel-oppsettsfil som inneholder alle arkene i den eksisterende filen. Forskjellen er at når du laster den ned fra en forespørselsside, omfatter oppsettet faktiske data. (Dataene er ikke nødvendige, men det hjelper å utforme oppsettet.)

#### Fremgangsmåte 1: Eksporter oppsettet fra siden **Rapportoppsett**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg Excel-oppsettet fra oversikten, og velg deretter handlingen **Eksporter oppsett** fra toppen av siden.
3. Åpne filen i Excel, gjør endringene og lagre deretter filen.

#### Fremgangsmåte 2: Last ned oppsettet fra rapportens forespørselsside

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. På siden **Rapportoppsett** velger du et oppsett for rapporten, og deretter velger du **Kjør rapport**-handlingen.
3. Velg **Last ned** på rapportens forespørselsside.
4. Åpne filen i Excel, gjør endringene og lagre deretter filen.

### [Fra AL-kode](#tab/from-code)

Dette er den mest avanserte metoden for oppretting av et Excel-rapportoppsett. Den er målrettet programmerere fordi den krever kunnskap om AL-kode. I denne tilnærmingen er Excel-oppsettene en del av en tilleggspakke som du installerer. Finn ut mer under [Opprett en Excel-oppsettsrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) i hjelpen for utviklere og IT-eksperter.

---

## Oppgave 2: Legg til Excel-oppsettet i rapporten

Når du har Excel-oppsettsfilen, er den neste oppgaven å legge den til som et nytt oppsett for rapporten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg **Nytt oppsett**.
3. Angi **Rapport-ID** til *Rapport*.
4. Angi et navn i **Oppsettsnavn**.
5. Angi **Formatalternativer** til **Excel**.
6. Velg **OK** og gjør deretter et av følgende for å laste opp oppsettfilen for rapporten:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Den valgte filen lastes opp til oppsettet, og siden **Rapportoppsett** åpnes.
8. Hvis du vil se hvordan rapporten ser ut med det nye oppsettet, velger du oppsettet fra listen, og deretter velger du **Kjør rapport**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## Forstå Excel-oppsett

Det er noen få ting du må vite eller vurdere når oppretter eller gjør endringer i Excel-oppsett. Alle Excel-oppsett må inneholde to elementer: et **Data**-ark og en **Data**-tabell. Disse elementene fra grunnlaget for oppsettet ved å definere forretningsdataene fra Business Central som du kan arbeide med. Du kan betrakte **Data**-arket som en slags kontrakt mellom oppsettet og forretningsdataene. Du skal bruke disse dataene som kilde for beregninger og effekter du vil presentere i andre ark.

Det finnes bestemte krav til strukturen i Excel-arbeidsboken. Hvis kravene ikke er oppfylt, får du problemer med oppsettet. Følgende diagram og tabell beskriver elementene i et Excel-oppsett og kravene.

[![Viser de ulike elementene på et Excel-oppsett.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Antall|Element|Description|Obligatorisk|
|---|-------|----|---|
|1|**Data**-ark|<ul><li>Må ha navnet **Data**.</li><li>Kan bare inkludere én tabell som må ha navnet **Data**.</li></ul>|![Er obligatorisk](media/check.png) | 
|2|**Data**-tabell|<ul><li>Må ha navnet **Data**.</li><li>Må ha minst én kolonne.</li><li>Kan bare inkludere kolonner som er i rapportdatasettet.</li><li>Må starte i den første cellen **A1** i **Data**-arket.</li></ul>|![Er obligatorisk](media/check.png)|
|3|Presentasjonsark|<ul><li>Brukes til å presentere data.</li><li>Dataene kommer fra **Data**-arket. </li></ul>||
|4|**Rapportmetadata**-ark|<ul><li>Inkluderes automatisk hvis oppsettet ble opprettet ved å eksportere en annen Excel-rapport.</li><li>Inneholder generell informasjon om rapporten.</li><li>Kan slettes.</li></ul>|

I sammendraget er dette det du bør og ikke bør gjøre på **Data**-arket:

- Ikke endre navnet på **Data**-arket, **Data**-tabellen eller kolonnene.
- Du kan slette eller skjule kolonner.
- Ikke legg til noen kolonner med mindre de er inkludert i rapportdatasettet.
- Du kan plassere arkene i en hvilken som helst rekkefølge, med **Data**-arket først eller sist.

## Se også
[Opprette en Excel-oppsettsrapport (utviklerdokumentasjon)](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout?toc=/dynamics365/business-central/toc.json)  
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett (eldre)](ui-how-import-and-export-report-layout.md)  
[Analyser rapportdata med Excel](report-analyze-excel.md)  
[Arbeid med rapporter](ui-work-report.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
