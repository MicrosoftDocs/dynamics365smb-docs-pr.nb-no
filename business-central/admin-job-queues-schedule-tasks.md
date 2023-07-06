---
title: Planlegge jobber til å kjøre automatisk
description: Lær hvordan du bruker prosjektkøoppføringer til å kjøre rapporter og codeunit.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 03/20/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
---
# <a name="use-job-queues-to-schedule-tasks"></a><a name="use-job-queues-to-schedule-tasks"></a><a name="use-job-queues-to-schedule-tasks"></a>Bruke jobbkøer til å planlegge oppgaver

Bruk siden **prosjektkøoppføring** til å planlegge og kjøre bestemte rapporter og codeunits. Du kan angi at jobbene skal kjøre én gang, eller gjentas flere ganger. Du ønsker kanskje å kjøre rapporten **Selger * salgsstatistikk** hver uke for å spore salg etter selger hver uke eller kjøre codeunit **Deleger godkjenningsforespørsler** daglig for å unngå at dokumenter hoper seg opp.

Siden Poster i jobbkø viser alle eksisterende jobber. Hvis du legger til en ny prosjektkøoppføring som skal kjøre på en plan, må du angi noen opplysninger. Eksempel:

* Typen objekt du vil kjøre, for eksempel en rapport eller codeunit. Du må ha tillatelse til å kjøre den bestemte rapporten eller codeunit.
* Navnet og objekt-ID-en for kostobjektet.
* Parametere som skal spesifisere hva jobbkøposten skal gjøre. Du kan for eksempel legge til en parameter for å sende bare bokførte ordrer.
* Når, og hvor ofte, vil jobbkøen skal kjøre.

> [!IMPORTANT]  
> Hvis du har SUPER-tillatelsessettet som følger med [!INCLUDE[prod_short](includes/prod_short.md)], har du tillatelse til å kjøre alle objektene i lisensen. Hvis du har rollen Delegert administrator, kan du opprette og planlegge jobbkøposter, men bare administratorer og lisensierte brukere kan kjøre dem. Brukere med denne enhetslisensen kan ikke opprette eller kjøre hele køen.

Når jobbkøer er satt opp og kjører, kan statusen endres på følgende måte i hver gjentakende periode:

* **Avvent**  
* **Klar**  
* **I arbeid**  
* **Feil**  
* **Ferdig**  

Etter at en jobb er fullført, fjernes den fra listen over jobbkøposter med mindre den er en gjentakende jobb. Hvis det er gjentakende jobber, justeres feltet **Tidligste starttidspunkt** til å vise neste gang jobben skal kjøres.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a><a name="monitor-status-or-errors-in-the-job-queue"></a><a name="monitor-status-or-errors-in-the-job-queue"></a>Overvåk status eller feil i jobbkøen

Data som jobbkøen genererer, lagres slik at du kan feilsøke feil.  

For hver jobbkøpost kan du vise og endre statusen. Når du oppretter en jobbkøpost, er statusen for posten satt til **Avvent**. Du kan for eksempel sette statusen til **Klar** og tilbake til **Avvent**. Ellers oppdateres statusinformasjon automatisk.

Tabellen nedenfor beskriver verdiene i feltet **Status**.

| Status | Description |
|--|--|
| Klar | Jobbkøposten er klar til å kjøres. |
| I arbeid | Jobbkøposten er pågår. Dette feltet oppdateres mens jobbkøen kjører. |
| Avvent | Standardstatusen for jobbkøposten når den opprettes. Velg handlingen **Sett status til Klar** for å endre statusen til **Klar**. Velg handlingen **Satt på vent** eller tilbakefør statusen til **Avvent**. |
| Feil | Noe gikk galt. Velg **Vis feil** for å vise feilmeldingen. |
| Ferdig | Jobbkøposten er fullført. |

> [!Tip]  
> Jobbkøposter slutter å kjøre når det oppstår en feil. Dette kan for eksempel være et problem når en post kobler til en ekstern tjeneste, for eksempel en bank. Hvis tjenesten midlertidig ikke er tilgjengelig og jobbkøen ikke kan koble til, vil posten vise en feil og slutte å kjøre. Du må starte jobbkøposten på nytt manuelt. Men feltene **Maksimalt antall forsøk** og **Forsinkelse for ny kjøring (s)** kan hjelpe deg å unngå denne situasjonen. Feltet **Maksimalt antall forsøk** lar deg angi hvor mange ganger jobbkøposten kan mislykkes før den slutter å prøve å kjøre. Med feltet **Forsinkelse for ny kjøring (s)** kan du angi hvor lang tid, i sekunder, det er mellom forsøk. Kombinasjonen av disse to feltene kan føre til at jobbkøposten kjører før den eksterne tjenesten blir tilgjengelig.

### <a name="to-view-status-for-any-job"></a><a name="to-view-status-for-any-job"></a><a name="to-view-status-for-any-job"></a>Slik viser du statusen for en jobb

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Jobbkøposter**, og velg deretter den relaterte koblingen.
2. På siden **Poster i jobbkø** velger du en jobbkøpost og deretter **Loggposter**-handlingen.  

> [!TIP]
> For inngående analyse basert på telemetri kan du bruke Application Insights i Microsoft Azure til å gå gjennom statusen for prosjektkøoppføringer. Hvis du vil lære mer om telemetri, går du til [Overvåk og analyser telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere telemetri for sporing av prosjektkølivssyklus](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a><a name="view-scheduled-tasks"></a><a name="view-scheduled-tasks"></a>Vis planlagte oppgaver

Siden **Planlagte oppgaver** i [!INCLUDE [prod_short](includes/prod_short.md)] viser hvilke oppgaver som er klare til å kjøres i jobbkøen. Siden viser også informasjon om selskapet som hver oppgave er definert til å kjøre i. Bare oppgaver som er merket som tilhører gjeldende miljø, kan imidlertid kjøres.  

Alle planlagte oppgaver stopper for eksempel hvis selskapet er i et miljø som er en kopi av et annet miljø. Bruk siden **Planlagte oppgaver** til å angi oppgaver som klare til å kjøres i jobbkøen.  

> [!NOTE]
> Interne administratorer og lisensierte brukere kan planlegge oppgaver som skal kjøres. Delegerte administratorer kan definere og planlegge oppgaver som skal kjøres, men bare lisensierte brukere kan kjøre dem.

## <a name="the-my-job-queue-part"></a><a name="the-my-job-queue-part"></a><a name="the-my-job-queue-part"></a>Delen Min jobbkø

Delen **Min jobbkø** viser i rollesenteret ditt viser jobbkøpostene som du har startet, men som ennå ikke er fullført. Som standard er delen ikke synlig, men du kan legge den til i rollesenteret. Hvis du vil ha mer informasjon om tilpasning, kan du gå til [Tilpass arbeidsområdet](ui-personalization-user.md).  

Delen viser følgende informasjon:

* Hvilke dokumenter med din ID i feltet **Tildelt bruker-ID** som behandles eller er i kø, inkludert dokumenter som bokføres i bakgrunnen. 
* Om det oppstod en feil under bokføring av et dokument eller i jobbkøposten. 

Delen Min jobbkø gjør det også mulig å avbryte en dokumentpostering.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a><a name="to-view-an-error-from-the-my-job-queue-part"></a><a name="to-view-an-error-from-the-my-job-queue-part"></a>Slik viser du en feil fra delen Min jobbkø:

1. I en oppføring med statusen **Feil** velger du **Vis feil**-handlingen.
2. Les feilmeldingen og løs problemet.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a><a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a><a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Eksempler på hva du kan planlegge med prosjektkøoppføringer

### <a name="schedule-reports"></a><a name="schedule-reports"></a><a name="schedule-reports"></a>Planlegg rapporter

Du kan planlegge at en rapport eller satsvis jobb skal kjøres på en bestemt dato og et bestemt klokkeslett. Planlagte rapporter og satsvise jobber legges i jobbkøen og behandles på det planlagte tidspunktet, på samme måte som andre jobber. Du velger alternativet **Planlegg** etter at du har valgt handlingen **Send til**, og deretter angir du informasjon som skriver, dato og klokkeslett, gjentakelse.  

Hvis du vil lære mer om planlegging, går du til [Planlegging av en rapport som skal kjøres](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a><a name="schedule-synchronization-between--and-includeprod_short"></a><a name="schedule-synchronization-between--and-includeprod_short"></a>Planlegg synkronisering mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du har integrert [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du bruke jobbkøen til å planlegge når du skal synkronisere data. Avhengig av retningen og reglene du har definert, kan jobbkøposten opprette poster i én app for å samsvare med poster i den andre. Et godt eksempel er når du registrerer en kontakt i [!INCLUDE[crm_md](includes/crm_md.md)], kan jobbkøposten konfigurere kontakten for deg i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon om planlegging, går du til [Planlegge en synkronisering mellom Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a><a name="schedule-when-to-post-sales-and-purchase-orders"></a><a name="schedule-when-to-post-sales-and-purchase-orders"></a>Planlegg når ordrer og bestillinger skal bokføres

Du kan bruke jobbkøposter til å planlegge at forretningsprosesser skal kjøre i bakgrunnen. Bakgrunnsoppgaver er nyttig for eksempel når flere brukere bokfører ordrer samtidig, men bare én ordre kan behandles om gangen. Hvis du vil lære mer om bakgrunnsbokføring, går du til [Slik setter du opp bakgrunnsbokføring med prosjektkøer](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a><a name="handle-job-queue-entry-issues"></a><a name="handle-job-queue-entry-issues"></a>Behandle problemer med prosjektkøoppføring

Hvis en prosjektkøoppføringer viser en feil, er det første alternativet for å løse problemet å starte prosjektkøoppføringen på nytt. Du kan sette statusen til prosjektkøoppføringer til **På vent** og deretter til **Klar**, eller bare starte den på nytt.

Hvis en omstart ikke hjelper, kan problemet være i koden. Du kan finne eieren (også kalt *utgiveren*) av koden i Al-stakksporet i loggen for prosjektkø. Hvis feilen kommer fra en app/utvidelse, kontakter du Microsoft-partneren. Hvis feilen kommer fra et Microsoft-program, kan du åpne en støtteforespørsel med Microsoft.

Hvis du kontakter Microsoft-partneren eller Microsoft for støtte, må du oppgi følgende informasjon:

* ID-en for prosjektkøoppføringskjøringen der feilen oppstod
* Tidsstempelet for når feilen oppstod
* Tidssonen din

> [!TIP]
> Du må samle opplysningene på følgende måter, avhengig av om [!INCLUDE [prod_short](includes/prod_short.md)] er tidligere eller senere enn versjon 22.1:
>
> * For tidligere versjoner må du oppgi et skjermbilde av siden **Loggposter for prosjektkø**.
> * For senere versjoner bruker du handlingen **Kopier detaljer** på siden Loggposter for prosjektkø til å kopiere opplysningene (ID for prosjektkø, tidsstempel og tidssone).

## <a name="monitor-the-job-queue-with-telemetry"></a><a name="monitor-the-job-queue-with-telemetry"></a><a name="monitor-the-job-queue-with-telemetry"></a>Overvåk jobbkøen med telemetri

Administratorer kan bruke [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) til å samle og analysere telemetri som bidrar til å identifisere problemer. Hvis du vil lære mer om telemetri, går du til [Overvåk og analyser telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) og [Analysere telemetri for sporing av prosjektkølivssyklus](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Telemetri lar administratorer konfigurere varsler om saker i prosjektkøen som sender en tekstmelding, e-post eller en melding i Teams, hvis noe ikke er riktig. Hvis du vil vite mer om disse varslene, går du til [Varsel om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Definere Business Central](setup.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Analysere telemetri for sporing av jobbkølivssyklus](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Varsel om telemetri](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
