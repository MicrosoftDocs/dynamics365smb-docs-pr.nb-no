---
title: Automatiser purringer i innkrevinger
description: 'Spar tid i innkrevinger ved å automatisere prosessene for å opprette, utstede og sende purringer til kunder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="automate-reminders-in-collections"></a>Automatiser purringer i innkrevinger

Gjør innkrevingene mer effektive ved å automatisere prosessen for å opprette, utstede og sende purringer til kundene. Automatisering kan redusere tiden du bruker på innkrevinger betydelig, gi bedre oversikt over prosessen og gi deg full kontroll over hvert trinn.

På siden **Automatisering av purring** definerer du de enkelte handlingene (trinnene). Du kan kombinere trinnene for å opprette, utstede og sende purringer, eller du kan opprette en separat automatisering for hvert trinn hvis det er bedre for innkrevingsprosessene. Automatiseringer er basert på purrebetingelser og purregrader. Hvis du vil lære mer, kan du gå til [Konfigurer purrebetingelser og -grader](finance-setup-reminders.md) Du kan angi filtre for purrebetingelser for en automatisering som helhet, og angi filtre for hver handling i automatiseringen. Du kan også legge ved utestående fakturaer i e-poster som PDF-filer.

Automatisering skjer gjennom en prosjektkøoppføring. Når du definerer en automatisering, bruker du feltet **Frekvens** til å angi hvordan og når den skal kjøres. Hvis du velger **Manuelt**, kjører automatiseringen én gang når du bruker **Start**-handlingen. Du kan også velge **Ukentlig**, **Månedlig** eller **Egendefinert** for å angi en mer detaljert frekvens. Hvis du velger **Egendefinert**, må du angi en datoformel. Hvis du vil lære mer om hvordan du angir en datoformel, kan du gå til [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas). Når du velger et annet alternativ enn **Manuelt**, kjøres automatiseringen til du stanser den midlertidig for å sette den på vent. Hvis du vil være enda mer spesifikt om når den kjører, bruker du handlingen **Prosjektkøposter** til å åpne siden **Prosjektkøposter** og justere gjentakelsen, for eksempel til daglig eller en bestemt ukedag.

## <a name="automate-the-reminders-flow"></a>Automatiser purreflyten

Delene nedenfor beskriver hvordan du konfigurerer purringer som skal opprettes, utstedes og sendes automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Automatisering av purringer**, og velg deretter den relaterte koblingen.
1. Velg **Ny**, og deretter fyller du ut feltene i **Generelt**-hurtigfanen.
1. I feltet **Filter for purrebetingelser** velger du purrebetingelsen eller -betingelsene du vil bruke denne automatiseringen for.
1. I feltet **Frekvens** velger du hvor ofte automatiseringen skal kjøre.
1. Velg **Ny** på hurtigfanen **Handlinger**, og velg deretter om automatiseringen skal opprette, utstede eller sende purringer. Velg **OK**.
1. Avhengig av hvilken type handling automatiseringen utfører, fyller du ut feltene etter behov på oppsettssiden. Hvis du vil vite mer om innstillingene, kan du gå til [Innstillinger for purrehandlinger](#settings-for-reminder-actions).
1. Når du har definert handlingene for automatiseringen, kan du bruke handlingene **Flytt opp** og **Flytt ned** til å justere rekkefølgen de kjøres i.

## <a name="settings-for-reminder-actions"></a>Innstillinger for purrehandlinger

Oppsettinnstillingene er forskjellige for handlingene Opprett, Utsted og Send purring. De følgende delene handler om hvordan du bruker dem.

### <a name="create"></a>Opprett

* Angi høyeste nivå på alle linjer for purring.  
* Opprett purringer for poster som er på vent. Denne innstillingen er for eksempel nyttig hvis du er i en pågående tvist med en kunde og vil at vedkommende skal se helheten.
* Opprett purringer for alle ubetalte fakturaer, ikke bare fakturaene som er forfalt. Rapporten viser forfalte fakturaer og fakturaer som er ubetalt, men ikke forfalt, i separate deler.
* Angi filtre for å gjøre purringen mer spesifikk.

### <a name="issue"></a>Utsted

Når du utsteder en purring, oppretter du poster i kundeposten som inneholder bokføringsdatoen og avgiftsdatoen. Bruk innstillingene på siden **Oppsett for Utsted purringer** til å angi om informasjonen i den utstedte purringen skal erstattes med informasjonen fra den opprettede purringen. Hvis du for eksempel opprettet purringen i går og utstedte den i dag, flyttes forfallsdatoen én dag.

### <a name="send"></a>Send

> [!NOTE]
> Send-automatiseringen krever at du har konfigurert e-post i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post, går du til [Konfigurer e-post](admin-how-setup-email.md).

Innholdet i e-postene, for eksempel vedleggstekster, brødtekst i e-post og språk, kommer fra oppsettet for purrebetingelsen. Hvis du vil lære mer om e-postinnstillinger, kan du gå til [Konfigurer purringsbetingelser og -grader](finance-setup-reminders.md).

Bruk innstillingene på siden **Oppsett for Send purringer** til å kontrollere følgende:

* Generelle innstillinger, for eksempel beskrivelsen, og hvor mange ganger du skal sende den samme purringen.
* Innstillinger for hva som skal tas med i purringen.
* Innstillinger for sporing av purringer du sender ved å opprette samhandlinger, om du skriver ut eller sender purringen via e-post, og om du bare vil legge ved forfalte fakturaer, alle fakturaer eller ingen fakturaer. 

## <a name="access-the-history-of-a-reminder"></a>Få tilgang til loggen for en purring

[!INCLUDE [prod_short](includes/prod_short.md)] holder rede på hver gang en automatisering kjøres. Du får tilgang til loggen ved å velge handlingen **Loggposter**. Du kan også bruke handlingen **Utstedte purringer** for å få tilgang til en liste over purringene du har utstedt.

## <a name="handle-errors"></a>Håndter feil

På hurtigfanen **Handlinger** kan du for hver handling angi om du vil at automatiseringen skal stoppe hvis handlingen inneholder en feil. Hvis du gjør det, behandler ikke automatiseringen handlingene som kommer etterpå. Hvis du vil aktivere eller deaktivere denne funksjonen, bruker du handlingene **Angi stopp ved feil** eller **Fjern stopp ved feil**.

## <a name="change-action-settings-for-an-automation"></a>Endre handlingsinnstillinger for en automatisering

Du kan når som helst endre innstillingene for en automatisering. Velg **Oppsett** på hurtigfanen **Handlinger**, og utfør deretter endringene.

## <a name="see-also"></a>Se også

[Konfigurer purringsbetingelser og -grader](finance-setup-reminders.md)  
[Send purringer om utestående saldoer](receivables-send-reminders.md)  
