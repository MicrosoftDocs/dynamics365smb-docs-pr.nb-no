---
title: Definere rapporter som skal skrives ut på bestemte skrivere | Microsoft-dokumentasjon
description: Finn ut hvordan du angir en skriver for en rapport og bruker siden Skrivervalg.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 04/17/2020
ms.author: edupont
ms.openlocfilehash: 4bf794dd423a2049887eb1a4fe725a091fdbd190
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781188"
---
# <a name="set-up-printers"></a>Konfigurere skrivere
Ettersom [!INCLUDE[prodshort](includes/prodshort.md)] er en skytjeneste, kan den ikke nå lokale skrivere som er koblet til brukernes maskiner. Den kan imidlertid koble til skyaktiverte skrivere. I den generelle versjonen av [!INCLUDE[prodshort](includes/prodshort.md)], blir en skyskriver kalt **E-postskriver** installert som en utvidelse, og den er klar til bruk etter første installasjon.

Hvis en skyskriver ikke er installert og konfigurert, eller hvis en installert skriver mislykkes, blir utskriftsalternativene automatisk angitt for leseren. Dette angis av denne verdien i feltet **Skriver** på rapportforespørselssiden: *(ingen, behandlet av leseren)*.

På siden **Utskriftsbehandling** kan du se hvilke skrivere som er definert. Når du har opprettet én eller flere skrivere, kan du åpne siden **Skrivervalg** for å opprette brukerkontoen som bestemte rapporter som skal skrives ut med hvilken skriver.

Når en skriver er definert og tilordnet bestemte rapporter, skriver du ut en rapport ved å velge **Skriv ut** på rapportforespørselssiden. Hvis du vil ha mer informasjon, kan du se [Skrive ut en rapport](ui-work-report.md#PrintReport).

### <a name="sizing-print-jobs"></a>Endre størrelse på utskriftsjobber
Skyutskrifter er utformet for dokumenter med en fornuftig størrelse. De fleste skytjenester, inkludert PrintNode og HP ePrint, har en grense på 10 MB per jobb. Hvis du må skrive ut store rapporter, må du kanskje dele dem opp i flere utskrifter.

## <a name="to-set-up-a-printer"></a>Slik definerer du en skriver
På siden **Utskriftsbehandling** kan du se skriverne som er definert, og du kan få tilgang til siden **Innstillinger** for hver skriver for å redigere et eksisterende oppsett eller definere en ny skriver.

Følgende fremgangsmåte viser hvordan du konfigurerer den eksisterende **e-postskriveren**, som er en forhåndsinstallert utvidelse.

> [!NOTE]
> For å kunne bruke utskrift av e-post, må du installere e-postfunksjonalitet. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg linjen for skriveren **E-postskriver**, og velg deretter handlingen **Rediger skriverinnstillinger**.
3. Fyll ut de nødvendige feltene på siden **Innstillinger**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du må velge riktig papirstørrelse manuelt for en skriver, ettersom ingen lokale skrivere eller brukerinnstillinger kan lagres.
    >
    > Vær oppmerksom på at utvidelsen for e-postskriver er satt til papirstørrelsen **A4** som standard, noe som for eksempel ikke passer i Nord-Amerika.
4. Hvis du vil at en skriver skal være standard velger du **Angi som min standardskriver** på siden **Utskriftsbehandling**.

### <a name="privacy-notice"></a>Personvernerklæring
Hvis du bruker utvidelsen E-postskriver, vil alle eller enkelte utskriftsjobber bli sendt til e-postadressen du har oppgitt når du konfigurerer skriveren. Det anbefales på det sterkeste at en unik e-post-ID blir knyttet til en skriverenhet med bare de offisielle tjenestene fra maskinvareprodusenten, for eksempel HP ePrint, KonicaMinolta EveryonePrint eller Epson E-Mail Printing.

Du må ta alle nødvendige forholdsregler for personvern, inkludert å sørge for at utskriftsløsningen for e-post har riktig konfigurerte tillatelser, personverninnstillinger og oppbevaringspolicyer. Det er ditt ansvar å oppgi en riktig, bekreftet og fungerende e-postadresse. Hvis du vil ha mer informasjon, kan du se [Personvernerklæring for Microsoft](https://privacy.microsoft.com/en-us/privacystatement).

## <a name="to-select-which-printers-print-which-reports"></a>Slik velger du hvilke skrivere som skriver ut hvilke rapporter

På siden **Skrivervalg** kan du definere hvilke rapporter som skrives ut av hvilken skriver, for brukerkontoen din. Dette er nyttig hvis du arbeider med forskjellige rapporter som krever ulike skrivere på grunn av sin plassering i firmaet eller utskriftsmulighetene.

> [!IMPORTANT]
> For lokal [!INCLUDE[prodshort](includes/prodshort.md)] kan siden **Skrivervalg** bare brukes for skrivere som er definert av skriverutvidelser. Den kan ikke brukes for lokale skrivere.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Skrivervalg**, og velg deretter den relaterte koblingen. Alternativt kan du velge siden **Utskriftsbehandling**, velge en skriver, og deretter velge handlingen **Skrivervalg**.
2. Velg handlingen **Ny** hvis du vil legge til et skrivervalg for en bestemt rapport.
3. Fyll ut feltene etter behov.

Den angitte rapporten er nå konfigurert slik at den skriver ut til den valgte skriveren som standard.

> [!NOTE]
> Når du skriver ut den aktuelle rapporten, kan du overstyre dette oppsettet ved å velge en annen skriver på forespørselssiden **Utskriftsinnstillinger**.

> [!NOTE]
> Hvis du ikke definerer en rapport for en bestemt skriver på siden **Skrivervalg**, blir den skrevet ut på standardskriveren til selskapet, som definert på siden **Utskriftsbehandling**.

Du eller administratoren kan også bruke siden **Skrivervalg** til å definere andre variasjoner av utskrift for brukere og rapporter. Tabellen nedenfor beskriver kombinasjonen av verdier for å angi et annet utskriftsoppsett for en rapport.

|Hvis du vil                                                 |Angi følgende verdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skrive ut en rapport på en bestemt skriver for alle brukere |Angi verdier i feltene **Rapport-ID** og **Skrivernavn**, og la feltet **Bruker-ID** stå tomt.|
|Skrive ut alle rapporter på en bestemt skriver til en bestemt bruker|Angi verdier i feltene **Bruker-ID** og **Skrivernavn**, og la feltet **Rapport-ID** stå tomt.|
|Angi standardskriver for alle rapporter|Angi en verdi i feltet **Skrivernavn**, og la feltene **Bruker-ID** og **Rapport-ID** stå tomme.|
|Skrive ut en bestemt rapport på brukerens standardskriver|Angi en verdi i feltet **Rapport-ID**, og la feltene **Skrivernavn** og **Bruker-ID** stå tomme.|
|Skrive ut en bestemt rapport på en bestemt skriver til en bestemt bruker|Angi verdier i alle tre feltene.|

> [!NOTE]
> Flere spesifikke skrivervalg har forrang over et mer generelt skrivervalg. Et skrivervalg som har verdier i feltene **Bruker-ID**, **Rapport-ID** og **Skrivernavn**, har for eksempel forrang over et skrivernavn som har tomme poster i feltene **Bruker-ID** eller **Rapport-ID**.

## <a name="see-also"></a>Se også
[Skrive ut en rapport](ui-work-report.md#PrintReport)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Kjøre kjørsler](ui-how-run-batch-jobs.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
