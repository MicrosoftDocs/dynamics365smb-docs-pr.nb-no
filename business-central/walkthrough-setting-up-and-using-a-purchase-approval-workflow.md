---
title: Definere og bruke en arbeidsflyt for kjøpsgodkjenning
description: Denne gjennomgangen tar deg gjennom alle trinnene for å konfigurere og bruke en arbeidsflyt for bestillingsgodkjenning i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning

Du kan automatisere prosessen med å godkjenne nye eller endrede poster, for eksempel dokumenter, kladdelinjer og kundekort, ved å opprette arbeidsflyter med trinnene for godkjenninger som er aktuelle.

Før du oppretter arbeidsflyter for godkjenning, må du definere en godkjenner og stedfortredende godkjenner for hver bruker for godkjenning. Du kan også angi godkjenneres beløpsgrenser for å definere hvilke salgs- og kjøpsposter de er kvalifisert til å godkjenne. Forespørsler om godkjenning og andre meldinger kan sendes som e-post eller intern merknad. For hvert brukeroppsett for godkjenning kan du også definere når de mottar meldinger.

> [!NOTE]
> I tillegg til arbeidsflytfunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] kan du bruke Power Automate til å definere arbeidsflyter for hendelser i [!INCLUDE[prod_short](includes/prod_short.md)]. Legg merke til at selv om de er to separate arbeidsflytsystemer, legges en flytmal som du oppretter med Power Automate, til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Bruk Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).  

Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn. Finn ut mer under [Arbeidsflyt](across-workflow.md).  

## Om denne gjennomgangen

Denne gjennomgangen er et scenario som illustrerer følgende oppgaver:  

- Definere godkjenningsbrukere  
- Definere meldinger for godkjenningsbrukere  
- Endre og aktivere en godkjenningsarbeidsflyt  
- Be om godkjenning av en bestilling (som Charlotte)  
- Motta en varsling og deretter godkjenne forespørselen (som Stig)  

## Hovedscenario

Stig er en superbruker hos CRONUS og oppretter to godkjenningsbrukere. En er Charlotte som representerer en innkjøper. Den andre er Sean selv, som representerer Alicias godkjenner. Sean gir selv ubegrensede rettigheter for kjøpsgodkjenning og angir at han skal motta meldinger ved internt notat så snart en relevant hendelse inntreffer. Til slutt oppretter Stig den nødvendige godkjenningsarbeidsflyten som en kopi av den eksisterende malen *Godkjenningsarbeidsflyt for bestilling*, lar alle eksisterende hendelsesbetingelser og svaralternativer stå uendret, og aktiverer deretter arbeidsflyten.  

For å teste godkjenningsarbeidsflyten logger Stig seg på [!INCLUDE[prod_short](includes/prod_short.md)] som Charlotte, og ber deretter om godkjenning av en bestilling. Sean logger seg deretter på som seg selv, ser notatet i rollesenteret, følger koblingen til godkjenningsforespørselen for bestillingen, og godkjenner forespørselen.  

## Brukere

Før du kan definere godkjenningsbrukere og varslingsmetode, må du kontrollere at disse brukerne finnes i [!INCLUDE[prod_short](includes/prod_short.md)]: én bruker representerer Charlotte. Den andre brukeren, deg selv, representerer Stig. Finn ut mer under [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).

### Definere godkjenningsbrukere

Når du er logget på som deg selv, definer Alicia som godkjenningsbruker med deg selv om godkjenner. Sett opp godkjenningsrettigheter og angi hvordan og når du blir varslet om forespørsler om godkjenning.  

#### Slik definerer du deg selv og Charlotte som godkjenningsbrukere

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. På siden **Brukeroppsett for godkjenning** velger du handlingen **Ny**.  

    > [!NOTE]  
    >  Du må definere en godkjenner før du kan definere brukere som krever godkjenning fra denne godkjenneren. Dette betyr at du må definere deg selv før du definerer Charlotte.  

3. Definer to godkjenningsbrukere ved å fylle ut feltene som beskrevet i følgende tabell.  

    |Bruker-ID|Godkjenner-ID|Ubegrenset kjøpsgodkjenning|  
    |-------|-----------|---------------------------|  
    |DU||Valgt|
    |CHARLOTTE|DU||

### Definer varsler

I denne gjennomgangen varsles brukeren med et internt varsel om forespørsler som må godkjennes. Godkjenningsvarsler kan også være sendt via e-post, og du kan legge til et trinn for arbeidsflytsvar som varsler avsenderen når en forespørsel godkjennes eller avslås. Finn ut mer under [Angi når og hvor du kan motta arbeidsflytvarsler](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### Slik definerer du hvordan og når du blir varslet

1. På siden **Brukeroppsett for godkjenning** velger du linjen for deg selv og deretter handlingen **Oppsett av varsling**.  
2. I feltet **Oppsett av varsling** på siden **Varslingstype** velger du **Godkjenning**.  
3. I feltet **Varslingsmetode** velger du **Bemerkning**.  
4. På siden **Oppsett av varsling** velger du handlingen **Tidsplan for varsling**.  
5. Velg **Umiddelbart** i **Gjentakelse**-feltet på siden **Tidsplan for varsling**.  

## Opprette arbeidsflyten for godkjenning

Opprett arbeidsflyten for godkjenning av innkjøp ved å kopiere trinnene fra malen **Arbeidsflyt for bestillingsgodkjenning**. La de eksisterende trinnene i arbeidsflyten forblir uendret, og aktiver deretter arbeidsflyten.  

> [!TIP]
> Du kan eventuelt legge til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist. Finn ut mer under [Angi når og hvor du kan motta arbeidsflytvarsler](across-how-to-specify-when-and-how-to-receive-notifications.md).

### Slik oppretter og aktiverer du en arbeidsflyt for bestillingsgodkjenning:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. På siden **Arbeidsflyter** velger du **Handlinger**, velger **Ny** og velger handlingen **Ny arbeidsflyt fra mal**.  
3. På siden **Arbeidsflytmaler** velger du arbeidsflytmalen kalt **Arbeidsflyt for bestillingsgodkjenning**.  

   **Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen. Verdien i **Kode**-feltet utvides med *-01* for å angi at dette er den første arbeidsflyten opprettet fra malen **Arbeidsflyt for bestillingsgodkjenning**.  
4. Slå på vekslebryteren **Aktivert** i hodet på **Arbeidsflyt**-siden.  

## Bruk arbeidsflyten for godkjenning

Bruk den nye arbeidsflyten for bestillingsgodkjenning ved først å logge på [!INCLUDE[prod_short](includes/prod_short.md)] som Alicia for å be om godkjenning av en bestilling. Deretter logger du på som deg selv, viser notatet i rollesenteret, følger koblingen til forespørsel om godkjenning og godkjenner forespørselen.  

### Slik ber du om godkjenning av en bestilling som Charlotte:

1. Logg på som Charlotte.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
3. Velg linjen for å åpne *bestilling 106001*.  
4. På siden **Bestilling** velger du **Handlinger**, **Be om godkjenning** og deretter velger du handlingen **Send godkjenningsforespørsel**.  

Legg merke til at verdien i **Status**-feltet er endret til **Venter på godkjenning**.  

### Slik godkjenner du bestillingen som Stig:

1. Logg på som Stig.
2. I området **Selvbetjening** i rollesenteret velger du **Forespørsler å godkjenne**.
3. På siden **Forespørsler å godkjenne** velger du linjen for bestillingen fra Charlotte, og deretter velger du **Godkjenn**-handlingen.  

Verdien i **Status**-feltet i Charlottes bestilling endres til **Frigitt**.  

Du har nå definert og testet en enkel godkjenningsarbeidsflyt basert på de to første trinnene av arbeidsflyten **Arbeidsflyt for bestillingsgodkjenning**. Du kan enkelt utvide denne arbeidsflyten til å postere Charlottes bestilling automatisk når Stig godkjenner den. Hvis du vil gjøre dette, må du aktivere **Arbeidsflyt for kjøpsfaktura**, der svaret på en frigitt kjøpsfaktura, er å bokføre den. Først må du endre betingelsen for hendelsen i det første arbeidsflyttrinnet fra (kjøp) **Faktura** til **Ordre**.  

Den generiske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] inneholder mange arbeidsflytmaler for scenarioer som støttes av programkoden. De fleste av disse malene er for arbeidsflyter for godkjenning.  

Du kan definere variasjoner i arbeidsflyter ved å fylle ut felter på arbeidsflytlinjer ved å bruke faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurer arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Bruke arbeidsflyter for godkjenning](across-how-use-approval-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Bruk Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
