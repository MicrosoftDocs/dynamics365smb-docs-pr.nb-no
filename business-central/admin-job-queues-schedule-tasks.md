---
title: Planlegge jobber til å kjøre automatisk | Microsoft-dokumentasjon
description: Planlagte aktiviteter administreres av jobbkøen. Disse jobbene kjører rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5e8c611ed5d542436f470781c92d17095ecd1f5d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924581"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Bruke jobbkøer til å planlegge oppgaver

Med jobbkøer i [!INCLUDE[d365fin](includes/d365fin_md.md)] kan brukere planlegge og kjøre bestemte rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger. Du ønsker kanskje å kjøre rapporten **Selger - salgsstatistikk** hver uke for å spore salg etter selger hver uke, eller kanskje du ønsker å kjøre kodeenheten **Deleger godkjenningsforespørsler** daglig for å unngå at dokumenter hoper seg opp eller på andre måter blokkerer arbeidsflyten.

Siden **Poster i jobbkø** viser alle eksisterende jobber. Hvis du vil legge til en jobbkøpost du vil planlegge, må du angi informasjon om objekttypen du vil kjøre, for eksempel en rapport eller kodeenhet, og navnet og objekt-IDen for objektet du vil kjøre. Du kan også legge til parametere for å spesifisere hva jobbkøposten skal gjøre. Du kan for eksempel legge til en parameter for å sende bare bokførte ordrer. Du må ha tillatelse til å kjøre den aktuelle rapporten eller kodeenheten, ellers vises det en feilmelding når jobbkøen kjøres.  

En jobbkø kan ha mange oppføringer, som er jobbene som køen håndterer og kjører. Informasjonen i posten angir hvilken kodeenhet eller rapport som kjøres, når og hvor ofte posten kjøres, i hvilken kategori jobben kjøres, og hvordan den kjører.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Konfigurere bokføring i bakgrunnen med jobbkøer

Jobbkøer er et effektivt verktøy til å planlegge kjøring av forretningsprosesser i bakgrunnen, for eksempel når flere brukere prøver å bokføre ordrer, men bare én kan behandles om gangen.  

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer ordrebokføring i bakgrunnen. Trinnene er de samme for kjøp.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Salgsoppsett** merker du av for **Bokfør med jobbkø**.
3. Velg feltet **Kategorikode for jobbkø**, og angi deretter koden **SALGSBOKF**.

    > [!NOTE]
    > Noen av jobbene endrer samme data og bør ikke kjøres samtidig, fordi dette kan forårsake konflikter. Bakgrunnsjobber for salgsdokumenter vil for eksempel prøve å endre de samme dataene samtidig. Jobbkøkategorier bidrar til å forhindre denne typen konflikter ved å sørge for at et annet prosjekt som tilhører samme jobbkøkategori, ikke blir kjørt før den er ferdig. Et prosjekt som for eksempel tilhører en jobbkøkategori for salg, vil vente til alle andre salgsrelaterte jobber er utført. Du angir en jobbkøkategori på hurtigfanen **Bakgrunnsbokføring** på siden **Salgsoppsett**.
    >
    > [!INCLUDE[d365fin](includes/d365fin_md.md)] gir jobbkøkategorier for salg, kjøp og finansbokføring. Vi anbefaler at én av disse eller en du oppretter, alltid angis. Hvis det oppstår feil på grunn av konflikter, kan du vurdere å definere en kategori for all bakgrunnsbokføring av salg, kjøp og finans.

    Hvis du også vil at salgsdokumenter skal skrives ut når de bokføres, merker du av for **Bokfør og skriv ut med jobbkø** på siden **Salgsoppsett**.  

    > [!IMPORTANT]  
    > Hvis du konfigurerer en jobb som bokfører og skriver ut dokumenter, og skriveren viser en dialogboks, for eksempel en forespørsel om legitimasjon eller en advarsel om lavt skriverblekk, blir dokumentet bokført, men ikke skrevet ut. Den tilsvarende jobbkøposten blir til slutt tidsavbrutt, og **Status**-feltet settes til **Feil**. Vi anbefaler derfor at du ikke bruker et skriveroppsett som krever samhandling med visningen av dialogbokser for skriveren i forbindelse med bakgrunnsbokføring.

    Neste gang du bokfører salgsdokumenter, oppretter [!INCLUDE [prodshort](includes/prodshort.md)] automatisk en jobbkøpost for hvert dokument og kjører jobbene i bakgrunnen, én etter én.

4. Hvis du vil kontrollere at jobbkøen fungerer som forventet, bokfører du en ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).

5. Se på siden **Loggposter for jobbkø** hvis ordren ble bokført. Hvis du vil ha mer informasjon, se [Vise status eller feil i jobbkøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Opprette en jobbkøpost for massebokføring av ordrer

Du kan også utsette bokføringer til når det passer for organisasjonen. I din virksomhet kan det for eksempel være fornuftig å kjøre visse rutiner etter at det meste av dagens dataregistrering er gjort. Du kan oppnå dette ved å angi at jobbkøen skal kjøre ulike massebokføringspostrapporter, for eksempel rapportene **Massebokfør ordrer**, **Salgsfakturaer - massebokfør** og lignende rapporter. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter ordrebokføring i bakgrunnen for alle salgs-, kjøps- og servicedokumenter.

Følgende fremgangsmåte viser hvordan du konfigurerer rapporten **Massebokfør ordrer** slik at ordrer bokføres automatisk kl. 16:00 på ukedager.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Poster i jobbkø**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. I feltet **Objekttype som skal kjøres** velger du **Rapport**.  
4. I feltet **Objekt-ID som skal kjøres** velger du 296, **Massebokfør ordrer**.

   Du kan også bruke følgende rapporter:
  
   * 900 **Massebokfør monteringsordrer**
   * 497 **Kjøpsfakturaer - massebokfør**
   * 496 **Bestillinger - massebokfør**
   * 498 **Kjøpskr.notaer - massebokfør**
   * 6665 **Massebokfør bestillingsreturer**
   * 298 **Salgskr.notaer - massebokfør**
   * 297 **Salgsfakturaer - massebokfør**
   * 296 **Massebokfør ordrer**
   * 6655 **Massebokfør ordrereturer**
   * 6005 **Massebokfør salgskreditnotaer (service)**
   * 6004 **Massebokfør servicefakturaer**
   * 6001 **Massebokfør serviceordrer**

5. Merk av for **Rapportforespørselsside**.
6. På forepørselssiden **Massebokfør ordrer** må du definere hva som skal tas med ved automatisk bokføring av ordrer, og deretter velge **OK**-knappen.

    > [!IMPORTANT]
    > Husk å angi strenge filtre. Ellers bokfører [!INCLUDE [prodshort](includes/prodshort.md)] alle dokumenter, selv om de ikke er klare. Vurder å definere et filter i **Status**-feltet for verdien *Frigitt* og et filter for **Bokføringsdato**-feltet for verdien *..i dag*. Hvis du vil ha mer informasjon, kan du se [Sortere, søke etter og filtrere](ui-enter-criteria-filters.md).
7. Merk av i alle bokser fra **Kjør på mandager** til **Kjør på fredager**.
8. I feltet **Starttidspunkt** angir du 16:00.
9. Velg **Sett status til Klar**-handlingen.

Ordrer som er innenfor definerte filtre, blir nå bokført hver ukedag kl. 16:00.

> [!NOTE]
> Hvis jobbkøen ikke kan bokføre ordren, endres statusen til **Feil**, og ordren legges til i listen over ordrer som brukeren må håndtere manuelt. Hvis du vil ha mer informasjon, se [Vise status eller feil i jobbkøen](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Når jobbkøer er satt opp og kjører, kan statusen endres på følgende måte i hver gjentakende periode:

* **Avvent**  
* **Klar**  
* **I arbeid**  
* **Feil**  
* **Ferdig**  

Etter at en jobb er fullført, fjernes den fra listen over jobbkøposter med mindre den er en gjentakende jobb. Hvis det er en gjentakende jobb, justeres feltet **Tidligste starttidspunkt** til å vise neste gang jobben er forventet å kjøre.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Vise status eller feil i jobbkøen
Data som genereres ved kjøring av en jobbkø, lagres i databasen, slik at du kan feilsøke jobbkøfeil.

### <a name="to-view-status-for-any-job"></a>Slik viser du statusen for en jobb
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Poster i jobbkø**, og velg deretter den relaterte koblingen.
2. På siden **Poster i jobbkø** velger du en jobbkøpost og deretter **Loggposter**-handlingen.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Slik viser du status fra et salgs- eller kjøpsdokument
1. Fra dokumentet du har prøvd å bokføre med bakgrunnsbokføring, velger du feltet **Jobbkøstatus**, som inneholder **Feil**.
2. Les feilmeldingen og løs problemet.

## <a name="the-my-job-queue-part"></a>Delen Min jobbkø
Delen **Min jobbkø** viser i rollesenteret ditt viser jobbkøpostene som du har startet, men som ennå ikke er fullført. Som standard er delen ikke synlig, så du må legge den til i rollesenteret. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).  

Delen viser hvilke dokumenter med din ID i feltet **Tilordnet bruker-ID** som behandles eller er i kø, inkludert de som er relatert til bokføring i bakgrunnen. Delen kan på et øyeblikk fortelle deg om det har oppstått en feil i posteringen av et dokument, eller om det er feil i en jobbkøpost. Delen gjør det også mulig å avbryte en dokumentpostering hvis den ikke kjører.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Slik viser du en feil fra delen Min jobbkø:
1. I en oppføring med statusen **Feil** velger du **Vis feil**-handlingen.
2. Les feilmeldingen og løs problemet.

## <a name="security"></a>Sikkerhet  
Jobbkøposter kjører basert på tillatelser. Disse tillatelsene må tillate kjøring av rapporten eller kodeenheten.  

Når en jobbkø aktiveres automatisk, kjører den med legitimasjonen for brukeren. Når en jobbkø aktiveres som en plalagt oppgave, kjører den med legitimasjon for serverforekomsten. Når en jobb kjøres, kjører den med legitimasjon for jobbkøen som aktiverer den. Brukeren som opprettet denne jobbkøposten, må imidlertid også ha tillatelser. Når en jobb er «Kjør i brukerøkt» (for eksempel under bakgrunnsbokføring), kjører den med legitimasjonen til brukeren som opprettet jobben.  

> [!IMPORTANT]  
> Hvis du bruker SUPER-tillatelsessettet som følger med [!INCLUDE[d365fin](includes/d365fin_md.md)], har du og brukerne tillatelse til å kjøre alle objektene. I dette tilfellet er tilgang for hver bruker bare begrenset av tillatelser til data.  

## <a name="using-job-queues-effectively"></a>Bruke jobbkøer effektivt  
Jobbkøposten inneholder mange felt som har som formål å sende parametere til en kodeenhet som du har angitt for kjøring sammen med en jobbkø. Dette betyr også at kodeenheter som skal kjøres via jobbkøen må angis med prosjektkøposten som en parameter i **OnRun**-utløseren. Dette gir et ekstra lag av sikkerhet, siden det forhindrer brukere fra å kjøre tilfeldige kodeenheter via jobbkøen. Hvis brukeren må sende parametere til en rapport, kan dette bare gjøres ved å wrappe rapportutførelsen i en kodeenhet, som deretter analyserer inndataparameterne og setter dem inn i rapporten før den utfører den.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Planlegge synkronisering mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]

Hvis du har integrert [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)], kan du bruke jobbkøen til å planlegge når du vil synkronisere data for de postene du har kombinert i de to forretningsprogrammene. Avhengig av retningen og reglene du har definert for integrasjonen, kan synkroniseringsjobbene også opprette nye poster i målappen for å samsvare med kilden. Hvis for eksempel en selger oppretter en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], kan synkroniseringsjobben opprette denne kontakten for den koblede selgeren i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Definere Business Central](setup.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
