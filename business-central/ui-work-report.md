---
title: Planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett | Microsoft-dokumentasjon
description: Finn ut hvordan du legger en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: edupont
ms.openlocfilehash: f209088459f29ba5618b065c3a340b0e3bd250e5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788399"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Arbeide med rapporter, satsvise jobber og XML-porter

En rapport samler inn informasjon basert på et bestemt sett med vilkår og organiserer og viser informasjonen i et format som er lett å lese og som kan skrives ut og lagres som en fil. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene, salgsstatistikk og mer.

Satsvise jobber og XML-porter utfører mer eller mindre det samme som rapporter, men hensikten er å utføre en prosess eller eksportere data. For eksempel oppretter **Opprett purringer**-kjørselen purredokumenter for kunder med forfalte betalinger.  

> [!NOTE]
> Dette emnet dreier seg hovedsakelig om "rapport", men lignende informasjon gjelder kjørsler og XML-porter.

Du finner rapporter i kategorien **Rapporter** på utvalgte sider, eller du kan bruke søket ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") for å finne rapporter etter navn.

## <a name="specifying-the-data-to-include-in-reports"></a>Spesifisere dataene som skal inkluderes i rapporter
Når du åpner en rapport, satsvis jobb eller XMLport, vises vanligvis en forespørselsside der du kan angi forskjellige alternativer og filtre som bestemmer hva du vil ha med i rapporten.

Du kan definere filtre i en rapport mer eller mindre på samme måte som du angir filtre for oversikter. Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Delen **Filtrer listen etter** på en forespørselsside gir generell filtreringsfunksjonalitet for rapporter. Disse filtrene er valgfrie.
>
> Noen rapporter overser slike filtre, som betyr at uansett hvilket filter som er angitt i delen **Filtrer listen etter**, vil resultatet av rapporten være det samme. Det er ikke mulig å gi en oversikt over hvilke felt som ignoreres i hvilke rapporter, så du må eksperimentere med filtrene når du bruker dem.
>
> **Eksempel**: Når du bruker kjørselen **Opprett purringer** ignoreres et filter for feltet **Kundeposter** for **Siste utstedte purregrad**, fordi filtre fikses for denne kjørselen.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Bruke lagrede innstillinger
Forespørselssiden kan inneholde delen **Lagrede innstillinger**, som inneholder én eller flere oppføringer i boksen **Bruk standardverdi fra**. Lagrede innstillinger er en forhåndsdefinert gruppe med alternativer og filtre som du kan bruke i rapporten før du forhåndsviser eller sender rapporten til en fil. Oppføringen med lagrede innstillinger, som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativer og filtre som ble brukt forrige gang du brukte rapporten.

Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene. Når du har angitt boksen **Bruk standardverdi fra** til en post med lagrede innstillinger, kan du endre alle alternativer og filtre før forhåndsvisning eller lagring av rapporten. Endringene du gjør, blir ikke lagret i oppføringen for lagrede innstillinger du valgte, men de blir lagret i oppføringen **Sist brukte alternativer og filtre**.

>[!NOTE]
>Hvis du er administrator kan du opprette og administrere lagrede innstillinger for rapporter for alle brukere. Hvis du vil ha mer informasjon, se [Behandle lagrede innstillinger for rapporter og satsvise jobber](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Forhåndsvise en rapport

Velg **Forhåndsvisning** for å vise rapporten på rapportforespørselssiden. Bruk menylinjen i rapportforhåndsvisningen for å:

- Gå gjennom sider
- Zoome inn og ut
- Endre størrelse for å tilpasse siden
- Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Ved hjelp av musen kan du for eksempel trykke og holde der du vil starte, og deretter bevege musen for å merke ett eller flere ord, setninger eller avsnitt. Du kan deretter trykke på høyreklikknappen og velge **Kopier**. Du kan deretter lime inn den merkede teksten der du vil ha den.
- Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning slik at du kan vise andre områder i rapporten. Dette er nyttig når du har zoomet inn for å vise detaljer.  Ved hjelp av musen kan du for eksempel trykke på og holde museknappen hvor som helst i rapportforhåndsvisningen, og deretter flytte musen.

- Last ned til en PDF-fil på datamaskinen eller nettverket.
- Skriv ut

## <a name="saving-a-report"></a>Lagre en rapport
Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved å velge knappen **Send til** og deretter gjøre et valg.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Planlegge en rapport for kjøring

Du kan planlegge at en rapport eller satsvis jobb skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter og satsvise jobber legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du velger alternativet **Planlegg** etter at du har valgt knappen **Send til**, og deretter angir du informasjon som skriver, dato og klokkeslett. Rapporten legges deretter til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

Når du planlegger å kjøre en rapport, kan du for eksempel angi at den må kjøre hver torsdag ved å sette feltet **Datoformel for neste kjøring** til *D4*. Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).  

Du kan velge å lagre den behandlede rapporten som en fil, for eksempel en Excel-, Word- eller PDF-fil, skrive den ut på en valgt skriver eller bare behandle rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til området **Rapportinnboks** på Rollesenteret, der du kan vise den.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Skrive ut en rapport

Du skriver ut en rapport ved å velge **Skriv ut** på rapportforespørselssiden eller på menylinjen på siden **Forhåndsvisning**.

### <a name="printer-selection"></a>Skrivervalg

Rapporten skriver ut på skriveren som vises i felltet **Valgt skriver** på rapportforespørselssiden. Du kan ikke endre skriveren på denne siden.

Den valgte skriveren er enten angitt på **Skrivervalg**-siden, eller det er standardskriveren som er satt opp på siden **Utskriftsbehandling**. Hvis du vil bruke en annen skriver, kan du se [Konfigurere skrivere](ui-specify-printer-selection-reports.md).

Hvis det ikke er angitt noen skriver på **Skrivervalg**-siden, eller ingen skriver er satt som standard på siden **Utskriftsbehandling**, brukes leserutskriftsfunksjonen. I dette tilfellet vises **Nettleser** i feltet **Valgt skriver** på rapportforespørselssiden. 

### <a name="browser-printing"></a>Utskrift fra nettleser

Ettersom [!INCLUDE[prodshort](includes/prodshort.md)] er en skytjeneste, kan den ikke nå lokale skrivere som er koblet til datamaskinen din. Den kan imidlertid koble til skyaktiverte skrivere. I den generelle versjonen av [!INCLUDE[prodshort](includes/prodshort.md)], blir en skyskriver kalt **E-postskriver** installert som en utvidelse, og den er klar til bruk etter første installasjon.

Hvis en skyskriver ikke er installert og konfigurert, eller hvis en installert skriver mislykkes, blir utskriftsalternativene automatisk angitt for leseren.

> [!NOTE]
> Utskriftsalternativene i leseren arbeider uavhengig av [!INCLUDE[prodshort](includes/prodshort.md)]. Så eventuelle skriverinnstillinger som er satt opp fra skrivere i [!INCLUDE[prodshort](includes/prodshort.md)], overføres ikke til alternativene for nettleserutskrift.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Skrive ut rapporter på thai
Spesielt for den thailandske versjonen av [!INCLUDE[prodshort](includes/prodshort.md)], kan ikke **Utskrift**-knappen skrive ut rapporter riktig på grunn av begrensninger i tjenesten som genererer den utskrivbare PDF-filen. Du kan i stedet åpne rapporten i Word og deretter lagre den som en utskrivbar PDF.  

Du kan også be systemansvarlig om å opprette et Word-rapportoppsett for de mest brukte rapportene. Hvis du vil ha mer informasjon, kan du se [Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Endre rapportoppsett
Et rapportoppsett styrer hva som skal vises i en rapport, hvordan det er ordnet og stilen som brukes. Hvis du vil bytte til et annet oppsett, kan du se [Endre gjeldende rapportoppsett](ui-how-change-layout-currently-used-report.md). Hvis du vil tilpasse ditt eget rapportoppsett, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også

[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
