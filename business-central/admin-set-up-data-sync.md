---
title: Konfigurer selskaper for å synkronisere hoveddata
description: Lær hvordan du definerer et eller flere selskaper for å synkronisere hoveddata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# <a name="get-ready-to-synchronize-master-data"></a>Gjør deg klar til å synkronisere hoveddata

Når to eller flere selskaper bruker noen av de samme hoveddataene, kan du synkronisere dataene i stedet for å legge dem til manuelt i hvert selskap. Synkronisering av data er for eksempel nyttig når du definerer nye datterselskaper.

Hoveddata omfatter innstillinger og ikke-transaksjonelle opplysninger om forretningsenheter. Det kan for eksempel være kunder, leverandører, varer og ansatte. Dataene gir kontekst for forretningstransaksjoner. Dette er noen få eksempler på hoveddata for en kunde:

* Name
* Identifikasjonsnummer
* Adresse
* Betalingsbetingelser
* Kredittgrense

Du kan konfigurere synkronisering i datterselskapene. Ved å bruke en pull-modell trekker datterselskaper dataene fra kildeselskapet de trenger for å gjøre forretninger med dem. Når du har definert synkronisering og synkronisert data for første gang, er du klar. Prosjektkøposter oppdaterer koblede poster i datterselskaper når noen endrer data i kildeselskapet.

## <a name="uni-directional-synchronization-only"></a>Bare enveissynkronisering

Du kan bare synkronisere data fra kildeselskapet til datterselskapene på en pull-måte. Datterselskaper kan ikke pushe data til kildefirmaet.

> [!NOTE]
> Selv om det er mulig, anbefaler vi ikke at du oppretter toveissynkronisering. Det vil si å synkronisere data fra kildeselskapet til datterselskapene og fra datterselskapene til kildeselskapet. Synkronisering av data i begge retninger kan føre til konflikter eller uønskede overskrivinger.

## <a name="before-you-start"></a>Før du begynner

Følgende er kravene for å konfigurere synkronisering.

* Alle selskaper må være i samme miljø.
* Brukeren som konfigurerer datterselskapet, må ha lisensen **Essential**, **Premium** eller **Basic ISV**.

> [!NOTE]
> Med Team Member- og Intern administrator-lisensen kan du få tilgang til dem, men ikke endre poster, slik at de ikke kan brukes til å konfigurere synkroniseringen. Delegert administrator-lisensen lar deg ikke planlegge bakgrunnsoppgaver, slik at du ikke kan fullføre oppsettet.

## <a name="specify-the-source-company"></a>Angi kildeselskapet

De første trinnene er å angi hvilket selskap som skal være datakilden, og aktivere synkronisering. Datterselskaper henter data fra kildefirmaet.

1. I et datterselskap velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for hoveddatabehandling** og velger deretter den relaterte koblingen.
1. I **Kildeselskap**-feltet angir du selskapet du vil hente endringer fra.
1. Slå på bryteren **Aktiver synkronisering**.
1. Velg **OK** i bekreftelsesdialogen. [!INCLUDE [prod_short](includes/prod_short.md)] finner tabellene og feltene som er tilgjengelige fra kildefirmaet.

Neste trinn er å aktivere tabeller og felter for synkronisering.

## <a name="enable-or-disable-tables-and-fields"></a>Aktiver eller deaktiver tabeller og felter

Hvis du vil spare tid, gir [!INCLUDE [prod_short](includes/prod_short.md)] en liste over tabeller som virksomheter synkroniserer ofte. Noen tabeller er aktivert for synkronisering som standard. Du kan endre, deaktivere eller slette dem etter behov. Som en ekstra tidsbesparelse er noen felter i tabellene allerede deaktivert, fordi de sannsynligvis ikke er relevante for datterselskapet.

> [!NOTE]
> Hvis en eller flere utvidelser er installert i kildeselskapet, når et datterselskaper konfigurerer synkronisering, omfatter siden **Synkroniseringstabeller** tabellene fra utvidelsene, og du får tilgang til feltene i dem. Hvis kildeselskapet imidlertid legger til en utvidelse etter at synkroniseringen er definert, må hvert datterselskap manuelt legge til tabellene. Hvis du vil ha mer informasjon om hvordan du legger til tabeller, kan du gå til [Legg til eller slett tabeller i listen over synkroniseringstabeller](#add-or-delete-tables-from-the-synchronization-tables-list). Hvis du vil lære mer om utvidelse av [!INCLUDE [prod_short](includes/prod_short.md)], går du til [Utvikling av utvidelser i Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for hoveddatabehandling** og velger deretter den relaterte koblingen.
1. Velg handlingen **Synkroniseringstabeller**.
1. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> **Tabellfilter**-feltet er nyttig når du skal kontrollere hva som skal synkroniseres for en tabell. Du kan definere filtre som skal synkroniseres bare når visse betingelser er oppfylt. Du kan for eksempel legge til filtre som angir at du bare synkroniserer leverandører i et bestemt område. Eller kunder som bruker en bestemt valuta.
>
> Hvis datterselskapet allerede har data i tabellene, er en annen god måte å angi kriterier for synkronisering på å konfigurere treffbasert kobling. Hvis du vil vite mer om samsvar, går du til [Bruk treffbasert kobling](#use-match-based-coupling).

1. Hvis du vil aktivere felter for en tabell, velger du tabellen og velger deretter handlingen **Felter**.
1. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> En rask måte å aktivere eller deaktivere flere felter samtidig på er å velge dem i listen og deretter bruke handlingene **Aktiver** eller **Deaktiver**.

### <a name="use-match-based-coupling"></a>Bruk treffbasert kobling

Du kan angi hvilke data som skal synkroniseres for en tabell, ved å samsvare poster basert på kriterier. På siden **Oppsett av hoveddatabehandling** velger du handlingen **Treffbasert kobling** for å åpne siden **Velg koblingskriterier**. Du kan definere følgende kriterier for samsvaret:

* Om du vil synkronisere etter at du har koblet poster.
* Om det skal opprettes en ny post i datterselskapet hvis et unikt, ikke-koblet samsvar blir funnet ved å bruke samsvarskriteriene. Hvis du vil aktivere denne funksjonen, slår du på handlingen **Opprett ny hvis det ikke finnes et samsvar**.
* Feltene som brukes til å samsvare poster, og om samsvaret skiller mellom store og små bokstaver.
* Prioriter rekkefølgen du søker etter poster i, ved å angi en samsvarsprioritet. [!INCLUDE [prod_short](includes/prod_short.md)] vil søke etter samsvar i stigende rekkefølge basert på samsvarsprioritet. En tom verdi er lik prioritet 0, som er den høyeste prioriteten. Felter som har prioriteten 0, vurderes først.

## <a name="synchronize-for-the-first-time"></a>Synkroniser for første gang

Når du er klar, velger du handlingen **Start første synkronisering** på siden **Oppsett av hoveddatabehandling**. Velg synkroniseringstypen du vil bruke for hver tabell, på siden **Innledende synkronisering av hoveddata**.

* Hvis du allerede har poster både i kilde- og datterselskapene og du vil tildele eksisterende poster, velger du handlingen **Bruk treffbasert kobling**. [!INCLUDE [prod_short](includes/prod_short.md)] samsvarer postene i datterselskapet med poster i kildeselskapet. Treffene er basert på samsvarskriteriene du definerer. For flere standardtabeller har [!INCLUDE [prod_short](includes/prod_short.md)] allerede samsvart eksisterende poster ved hjelp av primærnøkkelen, men du kan endre det hvis du vil. Du kan også la synkroniseringen opprette nye poster i datterselskapet for poster i kildeselskapet som datterselskapet ikke har. Hvis du vil vite mer om samsvar, går du til [Bruk treffbasert kobling](#use-match-based-coupling).
* Hvis du velger **Kjør fullstendig synkronisering**, oppretter synkroniseringen nye poster for alle poster i kildeselskapet som ikke er koblet ennå. Dette alternativet er for eksempel nyttig i følgende scenarioer:

    * Datterselskapet har ikke data i tabellen.
    * Du vil legge til poster fra kildeselskapet uten samsvar.  

Når du har valgt alternativet som skal brukes, velger du **Start alle**-handlingen for å starte synkroniseringen.

Mens synkroniseringen kjører, viser kolonnen **Prosjektstatus** på siden **Innledende fullstendig synkronisering av hoveddata** statusen for hver enkelt Jobbkø. Trykk på **F5** på tastaturet for å oppdatere statusen.

> [!TIP]
> Tabeller synkroniseres i en forhåndsdefinert rekkefølge. Hvis synkroniseringen sitter fast på en tabell, merker du tabellen og velger deretter handlingen **Start på nytt** for å få den i gang igjen.

Hvis du vil ha tilgang til detaljer, for eksempel antall poster som er satt inn eller endret, velger du verdien i kolonnen **Prosjektstatus** for å åpne siden **Vis – integreringssynkroniseringsjobber**. For poster som ble satt inn, kan du velge tallet i kolonnen **Satt inn** for å få tilgang til flere detaljer om de nye postene.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list"></a>Legg til eller slett tabeller i listen over synkroniseringstabeller

### <a name="add-a-table"></a>Legg til en tabell

> [!IMPORTANT]
> Tabeller som inneholder transaksjonsdata, er tilgjengelige i oversikten, for eksempel tabeller som inneholder poster, bør du ikke velge dem. Synkronisering fungerer bare for tabeller som inneholder ikke-transaksjonsbaserte data.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniseringstabeller**, og velg deretter den relaterte koblingen.
1. Velg **Opprett** og velg tabellen du vil legge til.
1. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table"></a>Slett en tabell

> [!NOTE]
> Hvis du sletter en post i kildeselskapet, slettes den ikke også i datterselskapet. Dette bidrar til å hindre uønsket tap av data. Datterselskapet kan selv bestemme om de vil slette tabellen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Synkroniseringstabeller**, og velg deretter den relaterte koblingen.
1. Velg handlingen **Slett**.

## <a name="use-export-and-import-to-share-a-synchronization-setup"></a>Bruk eksport og import til å dele et synkroniseringsoppsett

Hvis du definerer flere datterselskaper som bruker samme eller lignende synkroniseringsinnstillinger, er det en tidssparer. Definer ett datterselskap og eksporter deretter oppsettet til en XML-fil. Filen inneholder hele oppsettet, inkludert tabell- og felttildelinger og filterkriterier. Deretter kan du importere filen til neste datterselskap. Hvis du vil importere eller eksportere et oppsett, bruker du handlingene **Importer** eller **Eksporter** på siden **Oppsett av hoveddatabehandling**.

## <a name="see-also"></a>Se også

[Administrer hoveddatasynkronisering](admin-sync-master-data.md)
