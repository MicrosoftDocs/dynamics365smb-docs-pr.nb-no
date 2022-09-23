---
title: Arbeid med Excel-oppsett
description: Lær hvordan du oppretter og endrer rapportoppsett som er bygd ved hjelp av Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 45f321afeb411eee4cb9f9dd215cefc393f58458
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529572"
---
# <a name="working-with-excel-layouts"></a>Arbeid med Excel-oppsett

Oppsett for Excel-rapporter er basert på Microsoft Excel-arbeidsbøker (XLSX-filer). De gjør det mulig å opprette rapporter ved hjelp av velkjente Excel-funksjoner for oppsummering, analyse og presentasjon av data, for eksempel formler, pivottabeller og pivotdiagrammer.

![Viser et eksempel på et Excel-oppsett.](media/excel-layout-2.png)

Denne artikkelen forklarer noen av de viktigste tingene du må vite for å komme i gang med Excel-oppsett.

## <a name="why-use-excel-layouts"></a>Hvorfor bruke Excel-oppsett?

Her er noen flere fordeler med å bruke Excel-oppsett:

- Opprett interaktive rapporter ved hjelp av effekter som slicere
- Vis rådata fra rapportdatasettet for å bidra til å forstå hvordan rapporten fungerer, og hvor dataene i visuelle effekter kommer fra
- Bruk innebygde Office-funksjoner til å utføre etterbehandling på gjengitte rapporter, på samme måte som:
  - [Beskytt regnearkene](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Bruk følsomhetsetiketter](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Legg til kommentarer og merknader](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognose og analyse](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Bruk installerte tillegg og programintegreringer, for eksempel Power Automate-flyter eller OneDrive.

## <a name="get-started"></a>Kom i gang

Det finnes hovedsakelig to oppgaver involvert i konfigurasjonen av et Excel-oppsett i en rapport:

1. Opprett den nye filen for Excel-oppsett.
2. Legg til det nye oppsettet i rapporten.

## <a name="task-1-create-the-excel-layout-file"></a>Oppgave 1: Opprett filen for Excel-oppsett

Det er tre måter å opprette en Excel-oppsettsfil for en rapport på, som forklart i denne delen

### <a name="from-any-report"></a>[Fra en rapport](#tab/any-report)

Du kan bruke følgende fremgangsmåte til å opprette et Excel-oppsett fra alle rapporter, uavhengig av gjeldende oppsettstype. Excel-oppsettet inneholder det nødvendige **Data**-arket og den nødvendige tabellen, et **Rapportmetadata**-ark og ingenting annet.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. I **Rapportoppsett**-listen velger du et oppsett for rapporten, og deretter velger du **Kjør rapport**-handlingen.
3. På siden for rapportforespørsel velger du **Send til** > **Microsoft Excel-dokument (bare data)** > **OK**.

   Dette trinnet laster ned en Excel-arbeidsbok som inneholder datasettet for rapport.
4. Åpne den nedlastede filen i Excel, gjør endringene og lagre deretter filen.

### <a name="from-another-excel-layout-on-a-report"></a>[Fra et annet Excel-oppsett i en rapport](#tab/other-layout)

Hvis det allerede finnes et Excel-oppsett for en rapport, bruker du det eksisterende oppsettet som et utgangspunkt. Det finnes to tilnærminger for å få en kopi av oppsettet. Du kan eksportere det eksisterende oppsettet fra siden **Rapportoppsett**, eller du kan laste ned oppsettet fra rapportens forespørselsside. Begge måter laster ned en Excel-oppsettsfil som inneholder alle arkene i den eksisterende filen. Forskjellen er at fra forespørselsside vil oppsettet inkludere faktiske data. Dataene er ikke nødvendige, men det hjelper å utforme oppsettet.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Fremgangsmåte 1: Eksporter oppsettet fra siden **Rapportoppsett**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg Excel-oppsettet fra oversikten, og velg deretter handlingen **Eksporter oppsett** fra toppen av siden.
3. Åpne filen i Excel, gjør endringene og lagre deretter filen.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Fremgangsmåte 2: Last ned oppsettet fra rapportens forespørselsside

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. I **Rapportoppsett**-listen velger du et oppsett for rapporten, og deretter velger du **Kjør rapport**-handlingen.
3. Velg **Last ned** på rapportens forespørselsside.
4. Åpne filen i Excel, gjør endringene og lagre deretter filen.

### <a name="from-al-code"></a>[Fra AL-kode](#tab/from-code)

Denne måten er den mest avanserte. Den krever kunnskap om AL-kode, slik at det er målrettet mot programmerere. Excel-oppsettene, i dette tilfellet, er en del av en tilleggspakke som du installerer. Hvis du vil ha mer informasjon, kan du se [Opprett en Excel-oppsettsrapport](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) i hjelpen for utviklere og IT-eksperter.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Oppgave 2: Legg til Excel-oppsettet i rapporten

Når du har Excel-oppsettsfilen, er den neste oppgaven å legge den til som et nytt oppsett for rapporten.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velg **Nytt oppsett**.
3. Angi **rapport-ID-en** som skal rapporteres.
4. Angi et navn i **Oppsettsnavn**.
5. Angi **Formatalternativer** til **Excel**.
6. Velg **OK** > **Velg** for å åpne filutforsker på enheten. 
7. Finn og velg Excel-filen, og velg deretter **Åpne**.

   Den valgte filen lastes opp til oppsettet, og du går tilbake til siden **Rapportoppsett**.
8. Hvis du vil se hvordan rapporten ser ut med det nye oppsettet, velger du oppsettet i listen, og deretter velger du **Kjør rapport**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Forstå Excel-oppsett

Det er noen få ting du bør vite eller vurdere når du begynner å opprette eller gjøre endringer i Excel-oppsett. Alle Excel-oppsett må inneholde to elementer: et **Data**-ark og en **Data**-tabell. Disse elementene fra grunnlaget for oppsettet ved å definere forretningsdataene fra Business Central som du kan arbeide med. Du kan betrakte **Data**-arket som en slags kontrakt mellom oppsettet i forretningsdataene. Du skal bruke disse dataene som kilde for beregninger og effekter du vil presentere i andre ark.

Det finnes bestemte krav til strukturen i Excel-arbeidsboken. Hvis kravene ikke er oppfylt, får du problemer med oppsettet. Følgende diagram og tabell beskriver elementene i et Excel-oppsett og kravene.

[![Viser de ulike elementene på et Excel-oppsett.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Antall|Element|Beskrivelse|Obligatorisk|
|---|-------|----|---|
|1|**Data**-ark|<ul><li>Må ha navnet **Data**</li><li>Kan bare inkludere én tabell, og tabellen må ha navnet **Data**</li></ul>|![Er obligatorisk](media/check.png) | 
|2|**Data**-tabell|<ul><li>Må ha navnet **Data**</li><li>Må ha minst én kolonne.</li><li>Kan bare inkludere kolonner som er i rapportdatasettet.</li><li>Må starte i den første cellen **A1** i **Data**-arket</li></ul>|![Er obligatorisk](media/check.png)|
|3|Presentasjonsark|<ul><li>Brukes til å presentere data.</li><li>Dataene kommer fra **Data**-arket. </li></ul>||
|4|**Rapportmetadata**-ark|<ul><li>Inkluderes automatisk hvis oppsettet ble opprettet ved å eksportere en annen rapport som Excel</li><li>Inneholder generell informasjon om rapporten</li><li>Kan slettes</li></ul>|

For å oppsummere hva du kan og ikke kan gjøre i **Data**-arket:

- Ikke endre navnet på **Data**-arket, **Data**-tabellen eller kolonnene.
- Du kan slette eller skjule kolonner.
- Ikke legg til noen kolonner med mindre de er inkludert i rapportdatasettet.
- Du kan plassere arkene i en hvilken som helst rekkefølge. **Data**-arket kan for eksempel være første eller siste.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Arbeide med rapporter, satsvise jobber og XML-porter](ui-work-report.md)  
[Klargjøre Financial Reporting med kontoskjemaer og kontokategorier](bi-how-work-account-schedule.md)  
[Forretningsintelligens](bi.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analyser rapportdata med Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
