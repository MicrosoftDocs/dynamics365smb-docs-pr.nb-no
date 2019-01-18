---
title: "Planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett | Microsoft-dokumentasjon"
description: "Finn ut hvordan du legger en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 706464cf1b9a264f7575156c7835540ce3c254b0
ms.contentlocale: nb-no
ms.lasthandoff: 11/22/2018

---
# <a name="working-with-reports"></a>Arbeide med rapporter
En rapport samler inn informasjon basert på et bestemt sett med vilkår og organiserer og viser informasjonen i et format som er lett å lese og som kan skrives ut. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene og salgsstatistikken.

Du finner rapporter i kategorien **Rapporter** på bestemte sider, eller du kan bruke Søk ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") for å finne rapporter etter navn.


## <a name="specifying-the-data-to-include-in-the-report"></a>Spesifiser dataene som skal inkluderes i rapporten
Når du åpner en rapport, vises vanligvis en side der du kan angi forskjellige alternativer og filtre som bestemmer hva du vil ha med i rapporten. Denne siden kalles rapportforespørselssiden. Du kan for eksempel bruke forespørselssiden til å lage en rapport for en bestemt kunde, et bestemt datointervall eller sortere rekkefølgen av informasjonen i rapporten. Her er et eksempel på en forespørselside for en rapport:

![Alternativer for rapport](media/report_options.png "Alternativer for rapport")

### <a name="SavedSettings"></a>Bruke lagrede innstillinger
Med noen av rapportene, avhengig av hvordan de er utformet, kan rapportsiden ha med seksjonen **Lagrede innstillinger** som inneholder ett eller flere poster i boksen **Bruk standardverdi fra**. Postene i denne avmerkingsboksen kalles *Lagrede innstillinger*. Lagrede innstillinger er en forhåndsdefinert gruppe med alternativer og filtre som du kan bruke i rapporten før du forhåndsviser eller sender rapporten til en fil. Oppføringen med lagrede innstillinger, som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativer og filtre som ble brukt forrige gang du så på rapporten.

Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene. Når du har angitt boksen **Bruk standardverdi fra** til en post med lagrede innstillinger, kan du endre alle alternativer og filtre før forhåndsvisning eller lagring av rapporten. Endringene du gjør blir ikke lagret i valgte post med lagrede innstillinger, men de blir lagret i **Sist brukte alternativer og filtre**.

>[!NOTE]
>Hvis du er administrator kan du opprette og administrere lagrede innstillinger for rapporter for alle brukere. Hvis du vil ha mer informasjon, se [Administrere lagrede innstillinger i rapporter](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Angi alternativer og filtre
Hvis du vil ytterligere begrense eller tilspisse dataene som er inkludert i en rapport, kan du definere flere alternativer og filtre.

Med filtre kan du vise data basert på bestemte kriterier. Filtre er gruppert etter enheten de tilhører, som for eksempel **Kunde** i eksemplet ovenfor. Du definerer et filter ved å sette boksen **Hvor** til feltet som du vil filtrere etter, og deretter legge til kriterier i boksen **er:**. Eksemplet ovenfor er et enkelt filter som oppretter en rapport for kunden som har **Nr.** er lik **01121212**.

Du kan legge til flere filtre ved å definere boksene **Legg til**. Når du har flere enn ett filter, vil kun et resultatet som oppfyller kriteriene for alle filtre være med i rapporten.

Avhengig av hvilket felt du filtrerer på, kan du angi filterkriteriene til å søke etter et nøyaktig treff, delvis samsvar, verdiområder og så videre. Hvis du vil ha hjelp med å definerer filtre, kan du se:
-   [Filtrering](ui-enter-criteria-filters.md#FilterCriteria)
-   [Sette inn datointervaller](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Forhåndsvise en rapport
Velg **Forhåndsvisning** for å vise rapporten i nettleseren. Pek på et område i rapporten for å vise menylinjen.  

![Verktøylinje for forhåndsvisning av rapport](media/report_viewer.png "Verktøylinje for forhåndsvisning av rapport")

Bruk menylinjen til følgende:

-   Gå gjennom sider
-   Zoome inn og ut
-   Endre størrelse for å tilpasse siden
-   Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Ved hjelp av musen kan du for eksempel trykke og holde der du vil starte, og deretter bevege musen for å merke ett eller flere ord, setninger eller avsnitt. Du kan deretter trykke på høyreklikknappen og velge **Kopier**. Du kan deretter lime inn den merkede teksten der du vil ha den.
-   Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning slik at du kan vise andre områder i rapporten. Dette er nyttig når du har zoomet inn for å vise detaljer.  Ved hjelp av musen kan du for eksempel trykke på og holde museknappen hvor som helst i rapportforhåndsvisningen, og deretter flytte musen.

-   Last ned til en PDF-fil på datamaskinen eller nettverket.
-   Skriv ut


## <a name="saving-a-report"></a>Lagre en rapport
Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved å velge **Send til**, og deretter velge.

## <a name="ScheduleReport"></a> Planlegge en rapport for kjøring
Du kan planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du kan velge å lagre den behandlede rapporten som en fil, for eksempel en Excel-, Word- eller PDF-fil, skrive den ut på en valgt skriver eller bare behandle rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til området **Rapportinnboks** på Rollesenteret, der du kan vise den.

Du kan planlegge en rapport når du åpner en rapport. Du velger **Tidsplan** og angir deretter informasjon om skriveren, og dato og klokkeslett. Rapporten legges deretter til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Hvis du lagret den behandlede rapporten i en fil, er den tilgjengelig i området **Rapportinnboks**.

## <a name="PrintReport"></a>Skrive ut en rapport
Du kan skrive ut en rapport fra **Skriv ut**-knappen på siden med alternativer som vises når du åpner rapporten, eller fra menylinjen i forhåndsvisningen.

## <a name="changing-the-layout-and-look-of-a-report"></a>Endre oppsettet og utseendet på en rapport
Et rapportoppsett styrer hva som skal vises i en rapport, hvordan det er ordnet og stilen som brukes. Hvis du vil bytte til et annet oppsett, kan du se [Endre gjeldende oppsett som skal brukes i en rapport](ui-how-change-layout-currently-used-report.md). Hvis du vil tilpasse ditt eget rapportoppsett, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Angi skrivervalg for rapporter](ui-specify-printer-selection-reports.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

