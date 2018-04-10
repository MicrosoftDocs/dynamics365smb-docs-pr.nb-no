---
title: "Planlegge jobber til å kjøre automatisk | Microsoft-dokumentasjon"
description: "Planlagte aktiviteter administreres av jobbkøen. Disse jobbene kjører rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: fae1b2937a3c06fc947dd3dbec529826322d035c
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Bruke jobbkøer til å planlegge oppgaver
Med jobbkøer i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan brukere planlegge og kjøre bestemte rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger. Det kan for eksempel være at du vil kjøre rapporten **Selger - salgsstatistikk** ukentlig for å spore salg etter selger hver uke, eller du vil kanskje kjøre kodeenheten **Behandle e-postkø - service** daglig, for å sørge for at ventende e-postmeldinger angående serviceordrer sendes ut til kundene i rett tid.  

## <a name="add-jobs-to-the-job-queue"></a>Legge til jobber i jobbkøen
Vinduet **Poster i jobbkø** viser alle eksisterende jobber. Hvis du vil legge til en jobbkøpost du vil planlegge, må du angi informasjon om objekttypen du vil kjøre, for eksempel en rapport eller kodeenhet, og navnet og objekt-IDen for objektet du vil kjøre. Du kan også legge til parametere for å spesifisere hva jobbkøposten skal gjøre. Du kan for eksempel legge til en parameter for å sende bare bokførte ordrer. Du må ha tillatelse til å kjøre den aktuelle rapporten eller kodeenheten, ellers vises det en feilmelding når jobbkøen kjøres.  

Hvis du vil, kan du angi et filter i feltet **Filter for jobbkøkategori**. Jobbkøkategorier kan brukes til å gruppere jobber i oversikten.

[!INCLUDE[d365fin](includes/d365fin_md.md)] kjører jobbene automatisk i henhold til angitte de tidsplanene for hver jobbkøpost. Du kan også starte, stoppe og sette en jobbkøpost på vent manuelt.

### <a name="log-files"></a>Loggfiler
Feilmeldinger vises i vinduet **Loggposter for jobbkø**, som du får tilgang til fra båndet. Du kan også feilsøke jobbkøfeil. Data som genereres ved kjøring av en jobbkø, lagres i databasen.  

### <a name="background-posting-with-job-queues"></a>Bakgrunnsbokføring med jobbkøer
Jobbkøer er et effektivt verktøy for å planlegge kjøringen av forretningsprosesser i bakgrunnen. Det kan for eksempel være en forekomst der flere brukere prøver å bokføre ordrer samtidig, men bare én ordre kan behandles om gangen. Ved å sette opp en bakgrunnsbokføringsrutine kan du plassere bokføringer i en kø for behandling i bakgrunnen.  

 Du kan også planlegge bokføringer for timer når det passer for din organisasjon. I din virksomhet kan det for eksempel være fornuftig å kjøre visse rutiner etter at det meste av dagens dataregistrering er gjort. Du kan oppnå dette ved å angi at jobbkøen skal kjøre ulike massebokføringspostrapporter, for eksempel rapportene **Salgsfakturaer - massebokfør**, **Salgskr.notaer - massebokfør** og **Salgskr.notaer - massebokfør**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter bakgrunnsbokføring for følgende dokumenttyper:  

-   Salg: ordre, ordreretur, kreditnota, faktura  

-   Innkjøp: bestilling, bestillingsretur, kreditnota, faktura  

 Hvis jobbkøen ikke kan bokføre ordren, endres statusen til **Feil**, og ordren legges til i listen over ordrer som brukeren må håndtere.  

> [!NOTE]  
>  Når du planlegger et dokument for bokføring, og bokføringsprosessen begynner, konfigureres bokføringsrutinen automatisk til tidsavbrudd innen to timer hvis bokføringsrutinen av en eller annen grunn slutter å svare.  

Du konfigurere denne bruken av jobbkøen i henholdsvis vinduet **Salgsoppsett** eller **Kjøp**. På hurtigfanen **Bakgrunnsbokføring** merker du av for **Bokfør dokumenter via jobbkøen**, og deretter fyller du ut de aktuelle opplysningene. Her kan du også bruke feltet **Kategorikode for jobbkø** til å kjøre alle køposter med denne koden. Du kan for eksempel bruke en **Salgsbokf**-kategori som filtrerer etter alle ordrer som samsvarer med en jobbkø som har samme kategorikode.  

> [!IMPORTANT]  
>  Hvis du konfigurerer en jobb som bokfører og skriver ut dokumenter, og skriveren viser en dialogboks, for eksempel en forespørsel om legitimasjon eller en advarsel om lavt skriverblekk, blir dokumentet bokført, men ikke skrevet ut. Den tilsvarende jobbkøposten blir til slutt tidsavbrutt, og  **Status**    -feltet settes til  **Feil**. Vi anbefaler derfor at du ikke bruker et skriveroppsett som krever samhandling med visningen av dialogbokser for skriveren i forbindelse med bakgrunnsbokføring.  

## <a name="use-the-my-job-queue-part"></a>Bruke delen Min jobbkø
Delen **Min jobbkø** viser jobbkøpostene som en bruker har startet, men som ennå ikke er fullført. Som standard er delen ikke synlig, så du må legge den til i rollesenteret. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).  

I denne delen kan du se dokumentene som behandles eller er lagt i kø, og som IDen din er angitt for i feltet **Tilordnet bruker-ID**. Delen hjelper deg med å holde oversikt over alle jobbkøposter, inkludert de som er relatert til bakgrunnsbokføring. Delen kan på et øyeblikk fortelle deg om det har oppstått en feil i posteringen av et dokument, eller om det er feil i en jobbkøpost. Delen gjør det også mulig å avbryte en dokumentpostering hvis den ikke kjører.  

## <a name="security"></a>Sikkerhet  
Jobbkøposter kjører basert på tillatelser. Disse tillatelsene må tillate kjøring av rapporten eller kodeenheten.  

Når en jobbkø aktiveres automatisk, kjører den med legitimasjonen for brukeren. Når en jobbkø aktiveres som en plalagt oppgave, kjører den med legitimasjon for serverforekomsten. Når en jobb kjøres, kjører den med legitimasjon for jobbkøen som aktiverer den. Brukeren som opprettet denne jobbkøposten, må imidlertid også ha tillatelser. Når en jobb er "Kjør i brukerøkt" (for eksempel under bakgrunnsbokføring), kjører den med legitimasjonen til brukeren som opprettet jobben.  

> [!IMPORTANT]  
>  Hvis du bruker SUPER-tillatelsessettet som følger med [!INCLUDE[d365fin](includes/d365fin_md.md)], har du og brukerne tillatelse til å kjøre alle objektene. I dette tilfellet er tilgang for hver bruker bare begrenset av tillatelser til data.  

## <a name="using-job-queues-effectively"></a>Bruke jobbkøer effektivt  
Jobbkøposten inneholder mange felt som har som formål å sende parametere til en kodeenhet som du har angitt for kjøring sammen med en jobbkø. Dette betyr også at kodeenheter som skal kjøres via jobbkøen må angis med prosjektkøposten som en parameter i **OnRun**-utløseren. Dette gir et ekstra lag av sikkerhet, siden det forhindrer brukere fra å kjøre tilfeldige kodeenheter via jobbkøen. Hvis brukeren må sende parametere til en rapport, kan dette bare gjøres ved å wrappe rapportutførelsen i en kodeenhet, som deretter analyserer inndataparameterne og setter dem inn i rapporten før den utfører den.  

## <a name="see-also"></a>Se også  
[Administrasjon](admin-setup-and-administration.md)  
[Definere Business Central](setup.md)  

