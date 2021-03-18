---
title: Planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett | Microsoft-dokumentasjon
description: Finn ut hvordan du legger en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 7fe5d0870cfc18ab103dc57044fd0ba84b151662
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392449"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeide med rapporter, satsvise jobber og XML-porter

En rapport samler inn informasjon basert på et bestemt sett med vilkår og organiserer og viser informasjonen i et format som er lett å lese og som kan skrives ut og lagres som en fil. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene, salgsstatistikk og mer.

Satsvise jobber og XML-porter utfører mer eller mindre det samme som rapporter, men hensikten er å utføre en prosess eller eksportere data. For eksempel oppretter **Opprett purringer**-kjørselen purredokumenter for kunder med forfalte betalinger.  

> [!NOTE]
> Dette emnet dreier seg hovedsakelig om "rapport", men lignende informasjon gjelder kjørsler og XML-porter.

## <a name="getting-started"></a>Komme i gang

Du finner rapporter i kategorien **Rapporter** på utvalgte sider, eller du kan bruke søket ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") for å finne rapporter etter navn.

Når du åpner en rapport, satsvis jobb eller XMLport, vises vanligvis en forespørselsside der du kan angi forskjellige alternativer og filtre som bestemmer hva du vil ha med i rapporten. De følgende delene forklarer hvordan du bruker forespørselssiden til å bygge, forhåndsvise og skrive ut en rapport.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Bruke standardverdier – forhåndsdefinerte innstillinger 

De fleste forespørselssidene inkluderer feltet **Bruk standardverdi fra**. Med dette feltet kan du velge forhåndsdefinerte innstillinger for rapporten, som automatisk angir alternativer og filtre for rapporten. Velg en oppføring fra rullegardinlisten, og du vil se at alternativene og filtrene på forespørselssiden endres i henhold til dette.

Oppføringen som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativer og filtre som ble brukt forrige gang du kjørte rapporten.

Feltet **Bruk standardverdi fra** gir en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder riktige data. Når du har valgt en post, kan du endre alle alternativene og filtrene før du forhåndsviser eller skriver ut rapporten. Endringene du gjør, blir ikke lagret i oppføringen for forhåndsdefinerte innstillinger du valgte, men de blir lagret i oppføringen **Sist brukte alternativer og filtre**.

>[!NOTE]
> De forhåndsdefinerte innstillingene konfigureres og administreres vanligvis av en administrator. Hvis du vil lære mer, se [Behandle lagrede innstillinger for rapporter og satsvise jobber](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Spesifisere dataene som skal inkluderes i rapporter

Bruk feltene under **Alternativer** og **Filtre** for å endre avgrensningen av informasjon du ønsker i rapporten. Du kan definere filtre i en rapport mer eller mindre på samme måte som du angir filtre for oversikter. Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Delen **Filtrer listen etter** på en forespørselsside gir generell filtreringsfunksjonalitet for rapporter. Disse filtrene er valgfrie.
>
> Noen rapporter overser slike filtre, som betyr at uansett hvilket filter som er angitt i delen **Filtrer listen etter**, vil resultatet av rapporten være det samme. Det er ikke mulig å gi en oversikt over hvilke felt som ignoreres i hvilke rapporter, så du må eksperimentere med filtrene når du bruker dem.
>
> **Eksempel**: Når du bruker kjørselen **Opprett purringer** ignoreres et filter for feltet **Kundeposter** for **Siste utstedte purregrad**, fordi filtre fikses for denne kjørselen.

## <a name="previewing-a-report"></a>Forhåndsvise en rapport

Ved å forhåndsvise en rapport kan du se hvordan rapporten vil se ut før du skriver den ut. Forhåndsvisningen setter opp rapporten basert på [skriveren](#Printer) som vises i **Skriver**-feltet på forespørselssiden. Etter forhåndsvisning kan du gå tilbake til forespørselssiden og gjøre endringer i alternativer og filtre etter behov.

Hvis du vil forhåndsvise en rapport, velger du **Forhåndsvis** eller **Forhåndsvis & Lukk** på rapportforespørselssiden. Knappen som vises, avhenger av rapporten, så noen rapporter har **Forhåndsvisning**-knapp, mens andre har en **Forhåndsvis & Lukk**-knapp. Begge knappene åpner en forhåndsvisning av rapporten. Forskjellen er at **Forhåndsvisning** holder forespørselssiden åpen, slik at du kan gå tilbake til den, gjøre endringer, forhåndsvise på nytt eller skrive ut. Med **Forhåndsvis & Lukk** lukkes forespørselssiden, slik at du må åpne rapporten på nytt for å gjøre endringer eller skrive ut.

> [!NOTE]
> Hvis du bruker Business Central 2020 lanseringsbølge 1 eller tidligere, er det bare en **Forhåndsvisning**-knapp, som lukker forespørselssiden ved forhåndsvisning, som beskrevet for **Forhåndsvis & lukk**.

### <a name="working-with-the-preview"></a>Arbeide med forhåndsvisningen

I forhåndsvisningen bruker du menylinjen i rapportforhåndsvisningen for å:

- Gå gjennom sider
- Zoome inn og ut
- Endre størrelse for å tilpasse siden
- Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[prod_short](includes/prod_short.md)] eller Microsoft Word.  Ved hjelp av musen kan du for eksempel trykke og holde der du vil starte, og deretter bevege musen for å merke ett eller flere ord, setninger eller avsnitt. Trykk på høyreklikknappen og velg **Kopier**. Deretter limer du inn den merkede teksten der du vil ha den.
- Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning slik at du kan vise andre områder i rapporten. Panorering er nyttig når du har zoomet inn for å vise detaljer.  Ved hjelp av musen kan du for eksempel trykke på og holde museknappen hvor som helst i rapportforhåndsvisningen, og deretter flytte musen.

- Last ned til en PDF-fil på datamaskinen eller nettverket.
- Skriv ut

## <a name="saving-a-report"></a>Lagre en rapport

Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved å velge knappen **Send til** og deretter gjøre et valg.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlegge en rapport for kjøring

Du kan planlegge at en rapport eller satsvis jobb skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter og satsvise jobber legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du velger alternativet **Planlegg** etter at du har valgt knappen **Send til**, og deretter angir du informasjon som skriver, dato og klokkeslett. Rapporten legges deretter til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

Når du planlegger å kjøre en rapport, kan du for eksempel angi at den må kjøre hver torsdag ved å sette feltet **Datoformel for neste kjøring** til *D4*. Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan velge å lagre rapporten som en fil, for eksempel en Excel-, Word- eller PDF-fil, skrive den ut på en valgt skriver eller bare generere rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til området **Rapportinnboks** på Rollesenteret, der du kan vise den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skrive ut en rapport

Hvis du vil skrive ut en rapport, velger du **Skriv ut** på forespørselssiden eller på menylinjen på siden **Forhåndsvisning**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Skriver

**Skriver**-feltet på forespørselssiden viser navnet på skriveren som rapporten sendes til. **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise en standardopplevelse, der du kan velge en lokal skriver som er koblet til enheten.

Du kan ikke endre skriveren med feltet **Skriver**. Hvis du vil bytte skriver, må du gå til **Skrivervalg**- eller **Utskriftsbehandling**-sidene. Det å angi skriveren er vanligvis en administratoroppgave. Hvis du vil lære mer, kan du se [Konfigurere skrivere](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
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