---
title: Administrer synkronisering av hoveddata
description: Finn ut hvordan du administrerer synkronisering av hoveddata
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a><a name="manage-master-data-synchronization"></a><a name="manage-master-data-synchronization"></a>Administrer synkronisering av hoveddata

Når du har satt opp synkronisering av hoveddata og synkroniserer for første gang, er poster i de valgte tabellene sammenkoblet, og en gjentakende jobbkøoppføring opprettes for hver tabell. Jobbkøoppføringene synkroniserer automatisk data i datterselskapene når noen foretar en endring i kildeselskapet. Hvis ikke trenger du ikke å gjøre noe.

> [!NOTE]
> Som standard er jobbkøoppføringene planlagt å kjøre hvert minutt, og du kan ikke endre tidsplanen.

Noen ganger går ting imidlertid galt, og det kan være situasjoner du må behandle eller undersøke. Hvis for eksempel andre endrer samme oppføring i både kildeselskapet og et datterselskap, vil synkroniseringen mislykkes, slik at du kan angi endringen som er riktig. Kildeselskapet kan eventuelt installere en utvidelse som endrer skjemaet for en av tabellene som synkroniseres, ved å legge til et felt eller to. Hvis du vil synkronisere de nye feltene i datterselskapene, må du installere de samme utvidelsene og oppdatere tabellskjemaene i oppsettet.

Denne artikkelen beskriver verktøyene du kan bruke slik at synkroniseringen går problemfritt.

## <a name="investigate-the-status-of-synchronization"></a><a name="investigate-the-status-of-synchronization"></a><a name="investigate-the-status-of-synchronization"></a>Undersøk statusen til synkroniseringen

Det finnes to handlinger på siden **Synkroniseringstabeller** som kan hjelpe deg med å overvåke synkroniseringen:

* **Synkroniseringsprosjekter for integrering**
* **Poster i prosjektkø**

Tabellen nedenfor beskriver handlingene.

|Side  |Beskrivelse  |
|---------|---------|
|**Synkroniseringsprosjekter for integrering**     | Åpne siden **Synkroniseringsjobber for integrering** for å undersøke hva som skjedde hver gang en jobbkøoppføring ble kjørt. Hvis du vil gå dypere ned i detaljene for nye oppføringer som ble lagt til, eller undersøke hvorfor en oppføring ikke kan synkroniseres, velger du tallene i kolonnene **Satt inn** eller **Mislykket**. Du kan også bruke denne siden til å rydde opp i eldre oppføringer som du kanskje ikke trenger. Hvis du vil ha mer informasjon om hvordan du rydder opp, går du til [Rydd opp i eldre oppføringer](#clean-up-old-entries).        |
|**Poster i prosjektkø**     | Få tilgang til detaljer om jobbkøoppføringen som synkroniserer data for en valgt tabell. Du kan for eksempel bruke denne siden til å håndtere statusen for jobbkøoppføringen. Hvis du vil finne ut mer om jobbkøoppføringer, går du til [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Hvis du finner en feil på siden **Synkroniseringsjobber for integrering** som du ikke kan løse selv, er det nyttig å oppgi feilmelding og kallstakkinformasjon hvis du kontakter partneren eller Microsoft for kundestøtte.

## <a name="synchronize-modified-records"></a><a name="synchronize-modified-records"></a><a name="synchronize-modified-records"></a>Synkroniser endrede oppføringer

Hvis du endrer en innstilling for en tabell eller et felt i et datterselskap, må du oppdatere synkroniseringen. Hvis du for eksempel merker av **Overskriv lokal endring** i et felt for å tillate data fra kildeselskapet å overskrive lokale endringer. Hvis du vil oppdatere synkroniseringen, bruker du handlingen **Synkroniser endrede poster** på siden **Synkroniseringstabeller**.

## <a name="update-table-schemas"></a><a name="update-table-schemas"></a><a name="update-table-schemas"></a>Oppdater tabellskjemaer

Hvis kildeselskapet endrer en tabell, for eksempel ved å legge til et felt som du vil synkronisere, må datterselskaper oppdatere felttildelingene sine. På siden **Synkroniseringsfelter** bruker du handlingen **Oppdater felter**. 

## <a name="enable-or-disable-couplings-between-records"></a><a name="enable-or-disable-couplings-between-records"></a><a name="enable-or-disable-couplings-between-records"></a>Aktiver eller deaktiver kobling mellom oppføringer

Hvis du vil starte eller stoppe kobling på bestemte oppføringer i en tabell, velger du feltene på siden **Synkroniseringsfelter** og deretter bruke enten handlingen **Aktiver** eller **Deaktiver**. 

> [!TIP]
> En rask måte å aktivere eller deaktivere flere felter samtidig på er å velge dem i listen og deretter bruke handlingene **Aktiver** eller **Deaktiver**.

## <a name="adding-extensions"></a><a name="adding-extensions"></a><a name="adding-extensions"></a>Legg til utvidelser

Hvis kildeselskapet installerer en ny utvidelse, må datterselskapet også installere den hvis de vil synkronisere data for den. Datterselskapet kan bruke handlingen **Oppdater felter** på siden **Synkroniseringsfelter** til å legge til tabellene fra utvidelsen i listen.

> [!NOTE]
> Enkelte tabeller henter data fra relaterte tabeller. Hvis du legger til en filtype som ikke inkluderer relaterte tabeller, vil ikke feltene i tabellene være tilgjengelige. Kontroller at du har lagt til alle relaterte tabeller.

## <a name="clean-up-old-entries"></a><a name="clean-up-old-entries"></a><a name="clean-up-old-entries"></a>Rydd opp i gamle oppføringer

Antall poster i synkroniseringsloggen blir stort over tid, så det kan være lurt å gjøre litt rydding for å fjerne unødvendige oppføringer. For å gjøre det enklere å rydde opp i gamle oppføringer gir siden **Synkroniseringsjobber for integrering** følgende handlinger:

* **Slett poster eldre enn sju dager**
* **Slett alle poster**

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a><a name="recreate-a-deleted-job-queue-entry"></a><a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Gjør deg klar til å synkronisere hoveddata](admin-set-up-data-sync.md)
