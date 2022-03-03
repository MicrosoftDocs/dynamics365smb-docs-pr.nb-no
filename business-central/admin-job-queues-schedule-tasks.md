---
title: Planlegge jobber til å kjøre automatisk
description: Planlagte aktiviteter administreres av jobbkøen. Disse jobbene kjører rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 672, 673, 674, 671
ms.date: 10/01/2021
ms.author: edupont
ms.openlocfilehash: b09973b90a2721d83c309d63f42ce72e3d498e40
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130725"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Bruke jobbkøer til å planlegge oppgaver

Med jobbkøer i [!INCLUDE[prod_short](includes/prod_short.md)] kan brukere planlegge og kjøre bestemte rapporter og kodeenheter. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger. Du ønsker kanskje å kjøre rapporten **Selger - salgsstatistikk** hver uke for å spore salg etter selger hver uke, eller kanskje du ønsker å kjøre kodeenheten **Deleger godkjenningsforespørsler** daglig for å unngå at dokumenter hoper seg opp eller på andre måter blokkerer arbeidsflyten.

Siden **Poster i jobbkø** viser alle eksisterende jobber. Hvis du vil legge til en jobbkøpost du vil planlegge, må du angi informasjon om objekttypen du vil kjøre, for eksempel en rapport eller kodeenhet, og navnet og objekt-IDen for objektet du vil kjøre. Du kan også legge til parametere for å spesifisere hva jobbkøposten skal gjøre. Du kan for eksempel legge til en parameter for å sende bare bokførte ordrer. Du må ha tillatelse til å kjøre den aktuelle rapporten eller kodeenheten, ellers vises det en feilmelding når jobbkøen kjøres.  
> [!IMPORTANT]  
> Hvis du bruker SUPER-tillatelsessettet som følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du og brukerne tillatelse til å kjøre alle objektene i lisensen. Det er fremdeles ikke nok for delegert administrator eller brukere med enhetslisens, som ikke kan opprette jobbkøen.

En jobbkø kan ha mange oppføringer, som er jobbene som køen håndterer og kjører. Informasjonen i posten angir hvilken kodeenhet eller rapport som kjøres, når og hvor ofte posten kjøres, i hvilken kategori jobben kjøres, og hvordan den kjører.  

Når jobbkøer er satt opp og kjører, kan statusen endres på følgende måte i hver gjentakende periode:

* **Avvent**  
* **Klar**  
* **I arbeid**  
* **Feil**  
* **Ferdig**  

Etter at en jobb er fullført, fjernes den fra listen over jobbkøposter med mindre den er en gjentakende jobb. Hvis det er en gjentakende jobb, justeres feltet **Tidligste starttidspunkt** til å vise neste gang jobben er forventet å kjøre.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a>Overvåk status eller feil i jobbkøen

Data som genereres ved kjøring av en jobbkø, lagres i databasen, slik at du kan feilsøke jobbkøfeil.  

For hver jobbkøpost kan du vise og endre statusen. Når du oppretter en jobbkøpost, er statusen for posten satt til **Avvent**. Du kan for eksempel sette statusen til **Klar** og tilbake til **Avvent**. Ellers oppdateres statusinformasjon automatisk.

Tabellen nedenfor beskriver verdiene i feltet **Status**.

| Status | Beskrivelse |
|--|--|
| Klar | Angir at jobbkøposten er klar til å kjøres. |
| I arbeid | Angir at jobbkøposten er pågår. Dette feltet oppdateres mens jobbkøen kjører. |
| Avvent | Standard. Angir statusen for jobbkøposten når den opprettes. Velg handlingen **Sett status til Klar** for å endre statusen til **Klar**. Velg handlingene **Satt på vent** eller **Avbryt** for endre statusen tilbake til **Avvent**. |
| Feil | Angir at det finnes en feil. Velg **Vis feil** for å vise feilmeldingen. |
| Ferdig | Angir at jobbkøposten er fullført. |

### <a name="to-view-status-for-any-job"></a>Slik viser du statusen for en jobb

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Jobbkøposter**, og velg deretter den relaterte koblingen.
2. På siden **Poster i jobbkø** velger du en jobbkøpost og deretter **Loggposter**-handlingen.  

> [!TIP]
> Du kan også vise statusen for jobbkøposter ved å bruke Application Insights i Microsoft Azure for mer detaljert analyse basert på telemetri. Hvis du vil ha mer informasjon, kan du se [Overvåke og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere telemetri for jobbkølivsyklus](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) i utvikler- og administrasjonsinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="view-scheduled-tasks"></a>Vis planlagte oppgaver

Siden **Planlagte oppgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser hvilke oppgaver som er klare til å kjøres i jobbkøen. Siden viser også informasjon om selskapet som hver oppgave er definert til å kjøre i. Bare oppgaver som er merket som tilhører gjeldende miljø, kan imidlertid kjøres.  

Hvis for eksempel gjeldende selskap er i et miljø som er en kopi av et annet miljø, blir alle planlagte oppgaver automatisk stoppet. Bruk siden **Planlagte oppgaver** til å angi oppgaver som klare til å kjøres i jobbkøen.  

> [!NOTE]
> Interne administratorer og brukere kan planlegge oppgaver som skal kjøres. Delegerte administratorer kan ikke det.

## <a name="the-my-job-queue-part"></a>Delen Min jobbkø

Delen **Min jobbkø** viser i rollesenteret ditt viser jobbkøpostene som du har startet, men som ennå ikke er fullført. Som standard er delen ikke synlig, så du må legge den til i rollesenteret. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).  

Delen viser hvilke dokumenter med din ID i feltet **Tilordnet bruker-ID** som behandles eller er i kø, inkludert de som er relatert til bokføring i bakgrunnen. Delen kan på et øyeblikk fortelle deg om det har oppstått en feil i posteringen av et dokument, eller om det er feil i en jobbkøpost. Delen gjør det også mulig å avbryte en dokumentpostering hvis den ikke kjører.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Slik viser du en feil fra delen Min jobbkø:

1. I en oppføring med statusen **Feil** velger du **Vis feil**-handlingen.
2. Les feilmeldingen og løs problemet.

## <a name="examples-of-what-can-be-scheduled-using-job-queue"></a>Eksempler på hva som kan planlegges ved hjelp av jobbkø

### <a name="schedule-reports"></a>Planlegg rapporter

Du kan planlegge at en rapport eller satsvis jobb skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter og satsvise jobber legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du velger alternativet **Planlegg** etter at du har valgt handlingen **Send til**, og deretter angir du informasjon som skriver, dato og klokkeslett, gjentakelse.  

Hvis du vil ha mer informasjon, kan du se [Planlegge en rapport for kjøring](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between-prod_short-and-prod_short"></a>Planlegg synkronisering mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du har integrert [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruke jobbkøen til å planlegge når du vil synkronisere data for de postene du har kombinert i de to forretningsprogrammene. Avhengig av retningen og reglene du har definert for integrasjonen, kan synkroniseringsjobbene også opprette nye poster i målappen for å samsvare med kilden. Hvis for eksempel en selger oppretter en ny kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], kan synkroniseringsjobben opprette denne kontakten for den koblede selgeren i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-the-posting-of-sales-and-purchase-orders"></a>Planlegg bokføring av ordrer og bestillinger

Jobbkøer er et effektivt verktøy til å planlegge kjøring av forretningsprosesser i bakgrunnen, for eksempel når flere brukere prøver å bokføre ordrer, men bare én kan behandles om gangen.  

Hvis du vil ha mer informasjon, kan du se [Konfigurere bokføring i bakgrunnen med jobbkøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## <a name="monitor-the-job-queue-with-telemetry"></a>Overvåk jobbkøen med telemetri

Som administrator kan du bruke [Application Insights](/azure/azure-monitor/app/app-insights-overview) til å samle og analysere telemetri som du kan bruke til å identifisere problemer. Hvis du vil ha mer informasjon, kan du se [Overvåke og analysere telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) i utvikler- og administrasjonsinnholdet.  

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Definere Business Central](setup.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Analysere telemetri for sporing av jobbkølivssyklus](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]