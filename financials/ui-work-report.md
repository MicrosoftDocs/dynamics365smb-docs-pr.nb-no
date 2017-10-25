---
title: "Planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett | Microsoft-dokumentasjon"
description: "Finn ut hvordan du legger en rapport i en jobbkø og planlegger at den skal behandles på en bestemt dato og et bestemt klokkeslett."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: badcdee3dfa5bec3c2462149989cf9d4fb5af2a0
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-reports"></a>Arbeide med rapporter
En rapport samler inn informasjon basert på et bestemt sett med vilkår og organiserer og viser informasjonen i et format som er lett å lese og som kan skrives ut. Det finnes mange tilgjengelige rapporter i programmet. Rapportene inneholder informasjon i forhold til konteksten på siden du er på. **Kunde**-siden inneholder for eksempel rapporter for de 10 beste kundene og salgsstatistikken.

Du finner rapportene i **Rapporter**-kategorien på bestemte sider, eller du kan bruke Søk til å finne rapporter etter navn. Når du åpner en rapport, vises en side der du kan angi opplysninger (alternativer og filtre) som bestemmer hva du vil ha med i rapporten. Avhengig av rapporten kan du for eksempel angi et datointervall, en bestemt post som en kunde, eller sorteringsrekkefølge.

## <a name="previewing-a-report"></a>Forhåndsvise en rapport
Velg **Forhåndsvisning** for å vise rapporten i nettleseren. Pek på et område i rapporten for å vise menylinjen.  

![Verktøylinje for forhåndsvisning av rapport](media/report_viewer.png "Verktøylinje for forhåndsvisning av rapport").

Bruk menylinjen til følgende:

-   Gå gjennom sider
-   Zoome inn og ut
-   Endre størrelse for å tilpasse vinduet
-   Velg tekst

    Du kan kopiere tekst fra en rapport og lime den inn et annet sted, for eksempel en side i [!INCLUDE[d365fin](includes/d365fin_md.md)] eller Microsoft Word.  Ved hjelp av musen kan du for eksempel trykke og holde der du vil starte, og deretter bevege musen for å merke ett eller flere ord, setninger eller avsnitt. Du kan deretter trykke på høyreklikknappen og velge **Kopier**. Du kan deretter lime inn den merkede teksten der du vil ha den.
-   Panorer dokumentet

    Du kan flytte det synlige området i rapporten i en hvilken som helst retning slik at du kan vise andre områder i rapporten. Dette er nyttig når du har zoomet inn for å vise detaljer.  Ved hjelp av musen kan du for eksempel trykke på og holde museknappen hvor som helst i rapportforhåndsvisningen, og deretter flytte musen.

-   Last ned til en PDF-fil på datamaskinen eller nettverket.


## <a name="saving-a-report"></a>Lagre en rapport
Du kan lagre en rapport i et PDF-dokument, Microsoft Word-dokument eller Microsoft Excel-dokument ved å velge **Send til**, og deretter velge. 

## <a name="ScheduleReport"></a> Planlegge en rapport for kjøring
Du kan planlegge at en rapport skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du kan velge å lagre den behandlede rapporten som en fil, for eksempel en Excel-, Word- eller PDF-fil, skrive den ut på en valgt skriver eller bare behandle rapporten. Hvis du lagrer rapporten i en fil, sendes den behandlede rapporten til området **Rapportinnboks** på Hjem-siden, der du kan vise den.

Du kan planlegge en rapport når du åpner en rapport. Du velger **Tidsplan** og angir deretter informasjon om skriveren, og dato og klokkeslett. Rapporten legges deretter til i jobbkøen og kjøres på angitt tidspunkt. Når rapporten er behandlet, fjernes elementet fra jobbkøen. Hvis du lagret den behandlede rapporten i en fil, er den tilgjengelig i området **Rapportinnboks**.

## <a name="PrintReport"></a>Skrive ut en rapport
Når du vil skrive ut en rapport, må du laste ned rapporten som et PDF-, Word- eller Excel-dokument først ved å velge **Send til**. Nå kan du enten åpne rapportdokumentet med en gang og skrive det ut, eller lagre det og skrive det ut senere.

## <a name="using-saved-settings"></a>Bruke lagrede innstillinger
En rapport kan inneholde én eller flere poster i **Lagrede innstillinger**-feltet. *Lagrede innstillinger* er en forhåndsdefinert gruppe med alternativer og filtre som du kan bruke i rapporten før du forhåndsviser eller sender rapporten til en fil. Lagrede innstillinger er en rask og pålitelig metode for å generere konsekvent rapporter som inneholder de riktige dataene.

Oppføringen med lagrede innstillinger, som kalles **Sist brukte alternativer og filtre**, er alltid tilgjengelig. Denne posten angir at rapporten bruker alternativer og filtre som ble brukt forrige gang du så på rapporten.

>[!NOTE]
>Som administrator kan du opprette og administrere lagrede innstillinger for rapporter for alle brukere. Hvis du vil ha mer informasjon, se [Administrere lagrede innstillinger i rapporter](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Endre oppsettet og utseendet på en rapport
Et rapportoppsett styrer hva som skal vises i en rapport, hvordan det er ordnet og stilen som brukes. Hvis du ønsker å bytte til et annet oppsett, kan du se [Endre gjeldende oppsett som skal brukes i en rapports](ui-how-change-layout-currently-used-report.md). Hvis du vil tilpasse ditt eget rapportoppsett, se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Se også
[Angi skrivervalg for rapporter](ui-specify-printer-selection-reports.md)  
[Administrere rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

