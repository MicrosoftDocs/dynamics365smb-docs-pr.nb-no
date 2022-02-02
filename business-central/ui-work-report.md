---
title: Arbeide med rapporter, satsvise jobber og XML-porter
description: Finn ut hvordan du legger en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: d62c16ef8c511464fde86a1766499e37f8a07b1f
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972203"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeide med rapporter, satsvise jobber og XML-porter

En rapport samler informasjon basert på et angitt sett med kriterier. Den organiserer og presenterer informasjonen i et leservennlig format som du kan skrive ut eller lagre som en fil. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene, salgsstatistikk og mer.

Satsvise jobber og XML-porter utfører mer eller mindre det samme som rapporter, men brukes mer til å behandling og eksport av data. For eksempel oppretter **Opprett purringer**-kjørselen purredokumenter for kunder med forfalte betalinger.  

> [!NOTE]
> Dette emnet dreier seg hovedsakelig om "rapport", men lignende informasjon gjelder kjørsler og XML-porter.

## <a name="getting-started"></a>Komme i gang

Du finner rapporter i fanen **Rapporter** på utvalgte sider, eller du kan bruke søket ![Lyspære som åpner Fortell meg-funksjonen.](media/ui-search/search_small.png "Fortell hva du vil gjøre") til å finne rapporter etter navn.

Når du åpner en rapport, satsvis jobb eller XMLport, vises vanligvis en forespørselsside der du kan angi forskjellige alternativer og filtre som bestemmer hva du vil ha med i rapporten. De følgende delene forklarer hvordan du bruker forespørselssiden til å bygge, forhåndsvise og skrive ut en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Bruke standardverdier – forhåndsdefinerte innstillinger 

De fleste forespørselssidene inkluderer feltet **Bruk standardverdi fra**. Med dette feltet kan du velge forhåndsdefinerte innstillinger for rapporten, som automatisk angir alternativer og filtre for rapporten. Velg en oppføring fra rullegardinlisten, og du vil se at alternativene og filtrene på forespørselssiden endres i henhold til dette.

Oppføringen som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativer og filtre som ble brukt forrige gang du kjørte rapporten.

Feltet **Bruk standardverdi fra** gir en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder riktige data. Når du har valgt en post, kan du endre alle alternativene og filtrene før du forhåndsviser eller skriver ut rapporten. Endringene du gjør, blir ikke lagret i oppføringen for forhåndsdefinerte innstillinger du valgte, men de blir lagret i oppføringen **Sist brukte alternativer og filtre**.

>[!NOTE]
> De forhåndsdefinerte innstillingene konfigureres og administreres vanligvis av en administrator. Hvis du vil lære mer, se [Behandle lagrede innstillinger for rapporter og satsvise jobber](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Spesifisere dataene som skal inkluderes i rapporter

Bruk feltene under **Alternativer** og **Filtre** for å endre avgrensningen av informasjon du ønsker i rapporten. Du kan definere filtre i en rapport mer eller mindre på samme måte som du angir filtre for oversikter. Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Delen **Filtrer listen etter** på en forespørselsside gir generell filtreringsfunksjonalitet for rapporter. Disse filtrene er valgfrie.
>
> Noen rapporter overser slike filtre, som betyr at uansett hvilket filter som er angitt i delen **Filtrer listen etter**, vil resultatet av rapporten være det samme. Det er ikke mulig å gi en oversikt over hvilke felt som ignoreres i hvilke rapporter, så du må eksperimentere med filtrene når du bruker dem.
>
> **Eksempel**: Når du bruker kjørselen **Opprett purringer** ignoreres et filter for feltet **Kundeposter** for **Siste utstedte purregrad**, fordi filtre fikses for denne kjørselen.

## <a name="previewing-a-report"></a>Forhåndsvise en rapport

Ved å forhåndsvise en rapport kan du se hvordan rapporten vil se ut før du skriver den ut. Forhåndsvisningen er ikke basert på skriveren valgt i feltet **Skriver** på forespørselssiden. Det kontrolleres av nettleseren. Etter forhåndsvisning kan du gå tilbake til forespørselssiden og gjøre endringer i alternativer og filtre etter behov.

Hvis du vil forhåndsvise en rapport, velger du **Forhåndsvis** eller **Forhåndsvis & Lukk** på rapportforespørselssiden. Knappen som vises, avhenger av rapporten, så noen rapporter har **Forhåndsvisning**-knapp, mens andre har en **Forhåndsvis & Lukk**-knapp. Begge knappene åpner en forhåndsvisning av rapporten. Forskjellen er at **Forhåndsvisning** holder forespørselssiden åpen, slik at du kan gå tilbake til den, gjøre endringer, forhåndsvise på nytt eller skrive ut. Med **Forhåndsvis & Lukk** lukkes forespørselssiden, slik at du må åpne rapporten på nytt for å gjøre endringer eller skrive ut.

> [!NOTE]
> Hvis du bruker lanseringsbølge 1 eller tidligere for Business Central 2020, er det bare en **Forhåndsvisning**-knapp, som lukker forespørselssiden ved forhåndsvisning, som beskrevet for **Forhåndsvis & lukk**.

### <a name="working-with-the-preview"></a>Arbeide med forhåndsvisningen

I forhåndsvisningen bruker du menylinjen i rapportforhåndsvisningen for å:

- Gå gjennom sider
- Zoome inn og ut
- Endre størrelse for å tilpasse siden
- Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Du kan for eksempel bruke musen til å trykke og holde nede der du vil begynne. Deretter flytter du musen for å merke et eller flere ord, setninger eller avsnitt. Trykk på høyreklikknappen og velg **Kopier**. Deretter limer du inn den merkede teksten der du vil ha den.
- Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning slik at du kan vise andre områder i rapporten. Panorering er nyttig når du har zoomet inn for å vise detaljer.  Ved hjelp av musen kan du for eksempel trykke på og holde museknappen hvor som helst i rapportforhåndsvisningen, og deretter flytte musen.

- Last ned til en PDF-fil på datamaskinen eller nettverket.
- Skriv ut

## <a name="saving-a-report-to-a-file"></a>Lagre en rapport i en fil

Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-regneark ved å velge knappen **Send til** og deretter gjøre et valg.

### <a name="send-to-excel"></a>Send til Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Det er to alternativer for å lagre rapportresultatene som et regneark i en Excel-arbeidsbok: **Microsoft Excel-dokumenter (data og oppsett)** og **Microsoft Excel-dokument (bare data)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Microsoft Excel-dokument (data og oppsett)](#tab/data-and-layout)

Dette alternativet er bare tilgjengelig for rapporter som bruker et RDLC oppsett. Det eksporterer rapportresultatene når RDLC-oppsettet er brukt. Bruk dette alternativet hvis du vil eksportere dataene én gang, og bare vil gjøre små endringer i utseendet, for eksempel skrift og fargevalg.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Microsoft Excel-dokument (bare data)](#tab/data-only)

Alternativet **Microsoft Excel-dokument (bare data)** eksporterer rapportresultatene og kriteriene som ble brukt til å generere dem, men de inneholder ikke rapportoppsettet. Excel-filen vil inneholde hele datasettet, som rådata, ordnet i rader og kolonner. Alle datakolonnene i datasettet til rapporten inkluderes, uavhengig av om de brukes i rapportoppsettet.  Bruk dette alternativet når du vil:

- Foreta ad hoc-analyser av dataene. Du kan for eksempel filtrere dataene og bruke Power Pivot til å vise dem.

  Hver gang du eksporterer resultater, opprettes et nytt regneark. Ved hjelp av alternativet **Microsoft Excel-dokument (bare data)** kan du kjøre samme rapport og bruke formateringsendringer på nytt. Du kan for eksempel for Power Pivot kjøre rapporten på nytt i en annen tidsperiode, kopiere resultatene til regnearket og deretter oppdatere regnearket. Du kan også finne en rapporteringsapp i [AppSource](https://appsource.microsoft.com/).
- Kontroller datasettet i rapporten når du oppretter eller endrer egendefinerte rapportoppsett.

  Hvis du vil ha informasjon om hvordan du oppretter egendefinerte rapportoppsett, kan du se [Opprette eller endre egendefinerte rapportoppsett](ui-how-create-custom-report-layout.md)
- Diagnostiser dataproblemer i rapporter.

##### <a name="for-administrators"></a>For systemansvarlige

- **Microsoft Excel-dokument (bare data)** ble introdusert som en valgfri funksjon i 2021 lanseringsbølge 1, oppdatering 18.3. Hvis du vil gi brukere tilgang til denne funksjonen, aktiverer du funksjonsoppdateringen **Lagre rapportdatasett i Microsoft Excel-dokument** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management). I 2021 lanseringsbølge 2 blir denne funksjonen permanent, slik at du ikke trenger å aktivere den.

- Brukerkontoer vil trenge tillatelsen **<!--Export Report Dataset To Excel-->Tillat handlingen Eksporter rapportdatasett i Excel**, som du kan bruke ved hjelp av tillatelsessettet **Feilsøkingsverktøy** eller **Eksporter rapport Excel**.  

- Du kan ikke eksportere en rapport som har mer enn 1 048 576 rader eller 16 384 kolonner.

    > [!NOTE]
    > Med Business Central lokal kan maksimalt antall eksporterte rader være enda mindre. Business Central Server inneholder en konfigurasjonsinnstilling **Maks datarader som tillates å sende til Excel**, for å redusere grensen fra maksimumsverdien. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eller kontakte systemansvarlig.

##### <a name="for-developers-and-advanced-users"></a>For utviklere og avanserte brukere

Alternativet **Microsoft Excel-dokument (bare data)** eksporterer alle kolonner, inkludert kolonner som inneholder filtre og formateringsinstruksjoner for andre verdier. Her er noen viktige punkter:

- Binære data i et felt, for eksempel et bilde, eksporteres ikke.

  I kolonner som inneholder binære data, inneholder feltet **Binære data ({0} byte)**, der **{0}** indikerer antall byte.
- Fra og med Business Central 2021 lanseringsbølge 2 inneholder Excel-filen også regnearket **Rapportmetadata**.

  Dette regnearket viser hvilke filtre som er brukt på rapporten og egenskaper for den generelle rapporten, for eksempel navn, ID og utvidelsesinformasjon. Filtrene vises i **Filter (DataItem::Table::FilterGroupNo::FieldName)**-kolonnen. Filtrene i denne kolonnen inkluderer filtre som er angitt på forespørselssiden for rapporten. Det inneholder også filtre som er definert i AL-kode, for eksempel av [egenskapen DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [egenskapen DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Hvis du vil ha mer informasjon om rapportutforming, kan du se [Rapportoversikt](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Noen rapporter eksporterer tall som tekst, og gjør at du ikke kan utføre beregninger eller bruke Power Pivot-celler i Excel-regnearket. Etter eksporten er det lurt å kontrollere tallene i regnearket. Hvis du vil analysere og lage en oversikt over tallene, endrer du formatet for de aktuelle cellene fra **Tekst** til **Tall**. Hvis du vil ha mer informasjon om hvordan du formaterer tall i celler, kan du se denne videoen [Formateringstall i celler i Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

### <a name="microsoft-word-document"></a>Microsoft Word-dokument
Bruk alternativet **Microsoft Word-dokument** til å generere en rapport som et Word-dokument.  

> [!NOTE]
> Du kan angi oppsettet som skal brukes for hver rapport på siden **Rapportvalg** i feltet **Valgt oppsett**. Standardinnstillingen for rapporter er **RDLC (innebygd)**, som produserer rapporter i samme eller liknende oppsett som oppsettet **Microsoft Word-dokument**. Hovedforskjellen er imidlertid om du vil generere et eller flere rapportdokumenter. For enkeltdokumenter kan du bruke alternativet RDLC (innebygd). Hvis du vil ha flere dokumenter, angir du **Microsoft Word-dokumentet** som standardoppsett for rapporten. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlegge en rapport for kjøring

Du kan planlegge at en rapport eller satsvis jobb skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter og satsvise jobber legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du velger alternativet **Planlegg** etter at du har valgt knappen **Send til**, og deretter angir du informasjon som skriver, dato og klokkeslett. Rapporten legges deretter til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

Når du planlegger å kjøre en rapport, kan du for eksempel angi at den må kjøre hver torsdag ved å sette feltet **Datoformel for neste kjøring** til *D4*. Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan velge å lagre rapporten som en fil (for eksempel en Excel-, Word- eller PDF-fil), skrive den ut eller bare generere rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til området **Rapportinnboks** på Rollesenteret, der du kan vise den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skrive ut en rapport

Hvis du vil skrive ut en rapport, velger du **Skriv ut** på forespørselssiden eller på menylinjen på siden **Forhåndsvisning**.

### <a name="printer"></a><a name="Printer"></a>Skriver

**Skriver**-feltet på forespørselssiden viser navnet på skriveren som rapporten sendes til. Hvis du vil bytte skriver, velger du ganske enkelt skriveren fra listen.

> [!NOTE]
> **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise en standardopplevelse, der du kan velge en lokal skriver som er koblet til enheten. **(Håndteres av nettleseren)** er ikke tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen eller appen for Microsoft Teams.

> [!TIP]
> Skriveren som er valgt som standard, konfigureres på siden **Skrivervalg**. Hvis du vil ha informasjon om hvordan du endrer standardskriver, kan du se [Slik velger du hvilke skrivere som skriver ut hvilke rapporter](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Skrive ut rapporter på thai

Spesielt for den thailandske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)], kan ikke **Utskrift**-knappen skrive ut rapporter riktig på grunn av begrensninger i tjenesten som genererer den utskrivbare PDF-filen. Du kan i stedet åpne rapporten i Word og deretter lagre den som en utskrivbar PDF.  

Du kan også be systemansvarlig om å opprette et Word-rapportoppsett for de mest brukte rapportene. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Endre rapportoppsett

Et rapportoppsett styrer hva som skal vises i en rapport, hvordan det er ordnet og stilen som brukes. Hvis du vil bytte til et annet oppsett, kan du se [Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md). Hvis du vil tilpasse ditt eget rapportoppsett, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Avanserte alternativer

Feltene under **Avansert** setter begrensninger på den genererte rapporten for å kontrollere skriverressurser. Du trenger vanligvis ikke endre disse innstillingene, med mindre du har en stor rapport. Hvis en rapport overskrider disse begrensningene når du prøver å forhåndsvise eller skrive ut, vises en melding som forteller deg hvilken begrensning som ble overskredet. Deretter kan du endre innstillingene slik at de passer til rapporten. Hvert felt har imidlertid en maksimumsverdi som du bør være klar over:

|Felt|Maksimumsverdi|
|-----|-------------|
|Maksimal gjengivelsestid|12:00:00|
|Maksimalt antall rader|1000000|
|Maksimalt antall dokumenter|500|

> [!NOTE]
> Maksimumsverdiene kan være forskjellige for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, og en administrator kan endre dem. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server – Rapporter](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Hvis du vil ha en oversikt over rapporters begrensninger [!INCLUDE[prod_short](includes/prod_short.md)] online, kan du se [Driftsgrenser](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Se også

[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]