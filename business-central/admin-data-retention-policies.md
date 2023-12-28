---
title: Rydd opp data med oppbevaringspolicyer
description: Du kan angi hvor ofte du vil slette visse typer data.
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
---
# Definere oppbevaringspolicyer

Denne artikkelen beskriver hvordan administratorer kan definere oppbevaringspolicyer for å angi hvor ofte foreldede data skal slettes i tabeller som inneholder loggoppføringer og arkiverte poster. Hvis loggposter ryddes, kan det for eksempel bli enklere å arbeide med mer relevante dataene. Policyer kan slette data basert på en utløpsdato, eller du kan legge til filtre som bare inkluderer visse utløpte data.

## Nødvendige konfigurasjoner og tillatelser

Før du kan opprette oppbevaringspolicyer, må du sette opp tabellene som skal inkluderes, og tidsperioder for å beholde data.

|Installasjon  |Description  |
|---------|---------|
|**Tillatte tabeller**     |Vi gir en liste over tabeller som du kan inkludere i oppbevaringspolicyer. Hvis du vil legge til tabeller fra en utvidelse til en oppbevaringspolicy, må en utvikler legge til tabellene i listen. Hvis du vil ha mer informasjon, kan du gå til [Inkluder utvidelsen i en oppbevaringspolicy](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Oppbevaringsperioder**     |Angi tidsperioder det skal beholdes data i tabellene, i en policy. Periodene bestemmer hvor ofte data slettes.         |

I tillegg må du ha **SUPER**-brukertillatelsene eller tillatelsessettet **Oppbevaringspolicyoppsett**. Brukere som har tillatelsessettet Oppbevaringspolicyoppsett kan definere oppbevaringspolicyer for tabeller. Det er sant, selv om de ikke har lese- og slettetillatelser for tabellene. Jobbkøoppføringen må kjøre som en bruker med tillatelser til å lese og slette dataene. Ikke gi tillatelsessettet Oppbevaringspolicyoppsett til brukere som ikke skal kunne slette data.

> [!NOTE]
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, og du vil prøve ut oppbevaringspolicyer i Cronus-demonstrasjonsdatabasen, er det noen ting du må gjøre. Demonstrasjonsselskapet inneholder ikke tabeller som du kan bruke med oppbevaringspolicyer, så du må legge dem til. Det gjør du ved å opprette et nytt, tomt selskap i demonstrasjonsdatabasen. I det nye selskapet importerer du RapidStart-konfigurasjonspakken for landet/området ditt som tilsvarer standard NAV17.0.W1.ENU.STANDARD.rapidstart-pakken. Oppsettsdataene for oppbevaringspolicyer vil være tilgjengelige i det nye selskapet.

### Opprett oppbevaringsperioder

Oppbevaringsperioder kan være så lang eller så kort du vil. Hvis du vil opprette oppbevaringsperioder, bruker du handlingen **Oppbevaringsperiode** på siden **Oppbevaringspolicyer**. Periodene du definerer, er tilgjengelige for alle policyer.

> [!NOTE]
> Av hensyn til samsvar har vi definert en minimums oppbevaringsperiode for noen tabeller. Hvis du angir en oppbevaringsperiode som er kortere enn minimumskravet, vises en melding med den obligatoriske perioden.

### Definere en oppbevaringspolicy

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppbevaringspolicyer**, og velg deretter den relaterte koblingen.
2. Velg tabellen du vil ta med i policyen, i **Tabell-ID**-feltet.
3. I feltet **Oppbevaringsperiode** angir du hvor lenge dataene i tabellen skal beholdes.
4. Valgfritt: Hvis du vil bruke policyen på bestemte data i en tabell, deaktiverer du **Bruk på alle poster**. Hurtigfanen **Oppbevaringspolicy for post** vises slik at du kan definere filtre for å opprette delsett med data for hver linje. Hvis du vil vite mer, kan du gå til [Filtrering](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Hver linje har sin egen oppbevaringsperiode. Hvis du angir forskjellige oppbevaringsperioder for de samme dataene, brukes den lengste perioden. I tillegg inneholder noen tabeller filtre som du ikke kan endre eller fjerne. For å gjøre det lettere å identifisere disse filtrene, vises de i en lysere fargeskrift.

#### Videoveiledning

Denne videoen gir et eksempel på hvordan du setter opp en oppbevaringspolicy.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## Bruk oppbevaringspolicyer

Du kan bruke en jobbkøpost til å bruke oppbevaringspolicyer for å slette data automatisk, eller du kan bruke policyer manuelt.

Hvis du vil bruke en oppbevaringspolicy automatisk, oppretter og aktiverer du bare en policy. Når du aktiverer en policy, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] en prosjektkøpost som bruker den i henhold til oppbevaringsperioden dens. Alle oppbevaringspolicyer vil bruke samme jobbkøpost. Som standard bruker jobbkøposten policyen hver dag klokken 0200. Du kan endre standarden, men hvis du gjør det, anbefaler vi at den kjøres utenfor arbeidstiden. Hvis du vil vite mer, kan du gå til [Bruk prosjektkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md). 

Du kan bruke en policy manuelt ved hjelp av handlingen **Bruk manuelt** på siden **Oppbevaringspolicyer**. Hvis du alltid vil bruke en policy manuelt, slår du på **Manuell**. Jobbkøposten vil ikke ta hensyn til policyen når den kjøres.

## Vis loggoppføringer for oppbevaringspolicy

Du kan vise aktivitet som er knyttet til oppbevaringspolicyer, på siden **Oppbevaringspolicylogg**. Det opprettes for eksempel poster når en policy brukes, eller hvis det oppstod feil.

## Inkluder utvidelsen i en oppbevaringspolicy (krever hjelp fra en utvikler)

Som standard dekker oppbevaringsretningslinjer bare [!INCLUDE[prod_short](includes/prod_short.md)] i listen vi tilbyr. Du kan fjerne standardtabeller fra listen, og du kan legge til tabeller som du eier. Det vil si at du ikke kan legge til en tabell du ikke har opprettet selv. Du kan for eksempel ikke legge til andre tabeller fra [!INCLUDE[prod_short](includes/prod_short.md)] eller fra en utvidelse du har kjøpt.

Hvis du vil legge til tabellene dine i listen over tillatte tabeller, må en utvikler legge til kode. For eksempel til installasjons-codeunit for utvidelsen (en codeunit med undertypen *installer*).

Når en utvikler legger til en tabell, kan de angi obligatoriske og standard filtre. Obligatoriske filtre kan ikke fjernes eller endres senere når du legger til tabeller for å definere en oppbevaringspolicy. Standardfiltrene er bare forslag.

Følgende er eksempler på hvordan du legger til en tabell i listen over tillatte tabeller med, og uten, obligatoriske eller standard filtre. Hvis du vil ha et mer komplisert eksempel, kan du gå til codeunit 3999 Oppbev. Pol. Install - BaseApp".

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Følgende eksempel inneholder et obligatorisk filter.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Når en utvikler har lagt til tabeller i listen, kan en administrator inkludere dem i en oppbevaringspolicy. 

## Se også

[Analysere sporingstelemetri for oppbevaringspolicy](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Revidere endringer i Business Central](across-log-changes.md)  
[Filtrering](ui-enter-criteria-filters.md#filtering)  
[Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]