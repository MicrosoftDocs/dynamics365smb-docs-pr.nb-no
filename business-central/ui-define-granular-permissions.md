---
title: Definere detaljerte tillatelser
description: Dette emnet beskriver hvordan du definerer detaljerte tillatelser ved å gi bestemte brukere tilgang til objekter og tilordne tillatelsessett til dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 9807, 9808, 9830, 9831
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 634e21f291d15c78e8d4415399b6877240217eff
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/26/2022
ms.locfileid: "8028931"
---
# <a name="assign-permissions-to-users-and-groups"></a>Tilordne tillatelser til brukere og grupper

Med [!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhetssystemet kan du kontrollere hvilke objekter en bruker har tilgang til i hver database eller hvert enkelt miljø. Du kan angi for hver bruker om de kan lese, endre eller angi data i de valgte databaseobjektene. Hvis du vil ha mer informasjon, se [Datasikkerhet](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i utviklerhåndboken og ITPro-hjelpen for [!INCLUDE[prod_short](includes/prod_short.md)].

Før du tilordner tillatelser til brukere og brukergrupper, må du definere hvem som kan logge på ved å opprette brukere i henhold til lisensen som er definert i administrasjonssenteret for Microsoft 365. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)] finnes det to nivåer med tillatelser til databaseobjekter:

- Generelle tillatelser i henhold til lisensen, også kalt rettighet.
- Mer detaljerte tillatelser som tilordnet fra [!INCLUDE[prod_short](includes/prod_short.md)].

For å gjøre det enklere å behandle tillatelser for flere brukere, kan du organisere dem i brukergrupper og dermed tilordne eller endre ett tillatelsessett for mange brukere i én handling. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser gjennom brukergrupper](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> En tilleggsmetode som definerer hvilke funksjoner en bruker har tilgang til, er å angi **Opplevelse**-feltet på siden **Selskapsopplysninger**. Hvis du vil ha mer informasjon, se [Endre hvilke funksjoner som vises](ui-experiences.md).
>
> Du kan også definere hva brukere ser i brukergrensesnittet, og hvordan de samhandler med de tillate funksjonene gjennom sider. Dette gjør du gjennom profiler som du tilordner til ulike typer brukere i henhold til jobbrolle eller avdeling. Hvis du vil ha mer informasjon, kan du se [Administrere profiler](admin-users-profiles-roles.md) og [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Slik tilordner du tillatelsessett til brukere

Et tillatelsessett er en samling tillatelser for bestemte databaseobjekter. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[prod_short](includes/prod_short.md)].

En [!INCLUDE[prod_short](includes/prod_short.md)]-løsning inneholder vanligvis et antall forhåndsdefinerte tillatelsessett som legges til av Microsoft eller løsningsleverandøren. Du kan også legge til nye tillatelsessett som er skreddersydd for å dekke behovene i organisasjonen. Hvis du vil ha mer informasjon, kan du se [Slik oppretter eller viser du et tillatelsessett](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Hvis du ikke vil begrense brukerens tilgang mer enn det som allerede er definert av lisensen, kan du tilordne et spesielt tillatelsessett som kalles SUPER for brukeren. Dette tillatelsessettet sikrer at brukeren har tilgang til alle objektene som er angitt i lisensen.
>
> En bruker med Essential-lisensen og SUPER-tillatelsessettet har tilgang til mer funksjonalitet enn brukere med Team Member-lisensen og SUPER-tillatelsessettet.

Du kan tilordne tillatelsessett til brukere på to måter:

- Fra **Brukerkort**-siden ved å velge tillatelsessettet som skal tilordnes brukeren.
- Fra siden **Tillatelsessett etter bruker** ved å velge brukere som et tillatelsessett er tilordnet til.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Slik tilordner du et tillatelsesett på et brukerkort

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-siden.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. Hvis du vil ha mer informasjon, kan du se [Slik oppretter eller viser du et tillatelsessett](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Slik tilordner du et tillatelsessett på siden Tillatelsessett etter bruker

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. På siden **Brukere** velger du den aktuelle brukeren, og velger deretter handlingen **Tillatelsessett etter bruker**.
3. På siden **Tillatelsessett etter bruker** merker du av for **[brukernavn]** for en linje for det aktuelle tillatelsessettet for å tilordne settet til brukeren.
4. Merk av for **Alle brukere** for å tilordne tillatelsessettet til alle brukere.

## <a name="to-get-an-overview-of-a-users-permissions"></a>For å få en oversikt over en brukers tillatelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne kortet til den relevante brukeren.
3. Velg handlingen **Gyldige tillatelser**.

    Delen **Tillatelser** viser alle databaseobjektene som brukeren har tilgang til. Du kan ikke redigere denne delen.

    Delen **Etter tillatelsessett** viser de tilordnede tillatelsessettene som brukes til å gi tillatelser til brukeren, kilden og typen tillatelsessett og i hvilken grad de ulike tilgangstypene er tillatt.

    For hver rad du velger i delen **Tillatelser**, viser **Etter tillatelsessett** hvilke tillatelsessett som tillatelsen blir gitt via. I denne delen kan du redigere verdien i hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**.

    > [!NOTE]  
    > Bare tillatelsessett av typen **Brukerdefinert** kan redigeres.
    >
    > Rader for kilderettighet er hentet fra abonnementslisensen. Tillatelsesverdiene for rettigheten overstyrer verdier i andre tillatelsessett hvis de har en høyere rangering. En verdi i et ikke-berettiget tillatelsessett som har en høyere rangering enn den relaterte verdien i berettigelsen, vil stå i parenteser for å angi at den ikke er gyldig, siden den er overstyrt av berettigelsen.
    >
    > For en forklaring av rangering kan du se [Slik oppretter eller viser du tillatelsessett manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Hvis du vil redigere et tillatelsessett, går du til delen **Etter tillatelsessett** og linjen for et relevant tillatelsessett av typen **Brukerdefinerte** og velger ett av de fem tilgangstypefeltene og en annen verdi.

5. Hvis du vil redigere enkelttillatelser i tillatelsessettene, kan du velge verdien i feltet **Tillatelsessett** for å åpne **Tillatelser**-siden. Følg trinnene beskrevet under [Slik oppretter eller redigerer du tillatelser](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Når du redigerer et tillatelsessett, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

## <a name="to-create-or-modify-a-permission-set"></a>Opprette eller endre et tillatelsessett

Tillatelsessett fungerer som beholdere med tillatelser, slik at du enkelt kan behandle flere tillatelser i én post.

> [!NOTE]  
> En [!INCLUDE[prod_short](includes/prod_short.md)]-løsningen inneholder vanligvis et antall forhåndsdefinerte tillatelsessett som legges til av Microsoft eller programvareleverandøren. Disse tillatelsessettene er av typen **System** eller **Utvidelse**. Du kan ikke opprette eller redigere disse typene tillatelsessett eller tillatelsene i dem. Du kan imidlertid kopiere dem for å definere dine egne tillatelsessett og tillatelser.
>
> Tillatelse som brukere oppretter, fra nye eller som kopier, er av typen **Brukerdefinert** og kan redigeres.

### <a name="to-create-new-permission-set-from-scratch"></a>Slik oppretter du nye tillatelsessett fra grunnen av

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Tillatelsessett** og velger den relaterte koblingen.
2. Velg **Ny**-handlingen for å opprette et nytt tillatelsessett.
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Når du har opprettet et tillatelsessett, må du legge til de aktuelle tillatelsene. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre tillatelser manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Slik kopiere du et tillatelsessett

Du kan også bruke en kopieringsfunksjon til å overføre alle tillatelser i et annet tillatelsessett til et nytt tillatelsessett raskt.

> [!NOTE]  
> Hvis et systemtillatelsessett som du har kopiert, endres, vil du bli varslet (avhengig av hva du velger), slik at du kan ta hensyn til om endringene er relevante for å kopieres eller skrives inn i det brukerdefinerte tillatelsessettet ditt.

1. På siden **Tillatelsessett** merker du linjen for et tillatelsessett du vil kopiere, og velger deretter handlingen **Kopier tillatelsessett**.
2. På siden **Kopier tillatelsessett** angir du navnet på det nye tillatelsessettet, og velg deretter **OK**-knappen.
3. Merk av for **Varsle ved endret tillatelsessett** hvis du vil opprettholde en kobling mellom det opprinnelige og det kopierte tillatelsessettet. Koblingen brukes deretter til å varsle deg om navnet eller innholdet i det opprinnelige tillatelsessettet endres i en en fremtidig versjon som løsningen oppgraderes til senere.

Det nye tillatelsessettet, som inneholder alle tillatelsene i det kopierte tillatelsessettet, legges til som en ny linje på siden **Tillatelsessett**. Nå kan du endre tillatelser i det nye tillatelsessettet. Legg merke til at linjene sorteres alfabetisk innen hver type.

### <a name="to-export-and-import-a-permission-set"></a>Slik eksporterer og importerer du et tillatelsessett

Hvis du vil definere tillatelser raskt, kan du importere tillatelsessett du har eksportert fra en annen [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker.

I miljøer med mange leietakere importeres et tillatelsessett til en spesiell leietaker, det vil si at omfanget av importen er Leietaker.

1. I leietaker 1 på siden **Tillatelsessett** merker du linjen eller linjene for tillatelsessettene du vil eksportere, og velger deretter handlingen **Eksporter tillatelsessett**.

    En XML-fil opprettes i nedlastingsmappen på maskinen. Som standard kalles den Eksporter tillatelsessett.XML

2. I leietaker 2 på **Tillatelsessett**-siden velger du handlingen **Importer tillatelsessett**.
3. På siden **Importer tillatelsessett** må du vurdere om du vil slå sammen eksisterende tillatelsessett med nye tillatelsessett i XML-filen.

    Hvis du merker av for **Oppdater eksisterende tillatelser**, slås eksisterende tillatelsessett med samme navn som de som finnes i XML-filen, sammen med de importerte tillatelsessettene.

    Hvis du ikke merker av for **Oppdater eksisterende tillatelser**, blir eksisterende tillatelsessett med samme navn som de som finnes i XML-filen, hoppet over under importen. I dette tilfellet blir du varslet om tillatelsessett som hoppes over.

4. Fra siden **Importer** finner og velger du filen som skal importeres, og velger handlingen **Åpne**.

Tillatelsessettene importeres.

## <a name="to-create-or-modify-permissions-manually"></a>Opprette eller endre tillatelser manuelt

Denne fremgangsmåten beskriver hvordan du legger til eller redigerer tillatelser manuelt. Du kan også generere tillatelser automatisk fra handlingene i grensesnittet. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre tillatelser ved å registrere handlingene dine](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Når du redigerer en tillatelse og dermed det relaterte tillatelsessettet, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

1. På siden **Tillatelsessett** merker du linjen for et tillatelsessett og velger deretter handlingen **Tillatelser**.
2. På siden **Tillatelser** oppretter du en ny linje eller redigerer feltene i en eksisterende linje.

I hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**, kan du velge ett av følgende tre tillatelsesalternativer:

|Alternativ|Description|Rangering|
|------|-----------|-------|
|**Ja**|Brukeren kan utføre handlingen for det aktuelle objektet.|Høyeste|
|**Indirekte**|Brukeren kan utføre handlingen for det aktuelle objektet, men bare via et annet tilknyttet objekt som brukeren har full tilgang til. Hvis du vil ha mer informasjon om indirekte tillatelser, kan du se [Tillatetlser-egenskapen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) i hjelpen for utviklere og IT-eksperter.|Nest høyeste|
|**Tom**|Brukeren kan ikke utføre handlingen for det aktuelle objektet.|Laveste|

> [!IMPORTANT]
> Vær forsiktig når du tilordner **innsettingstillatelse** eller **endringstillatelse** til gruppen **9001 brukergruppemedlem** eller **9003 gruppetillatelsessett for bruker**. Alle brukere som er tilordnet tillatelsessettet, kan potensielt tilordne seg selv til andre brukergrupper, som i sin tur kan gi dem utilsiktede tillatelser.

### <a name="example---indirect-permission"></a>Eksempel - indirekte tillatelse

Du kan tilordne en indirekte tillatelse til å bruke et objekt, bare via et annet objekt.
En bruker kan for eksempel ha tillatelse til å kjøre kodeenhet 80, Sales-Post. Kodeenheten Sales-Post utfører mange oppgaver, inkludert å endre tabell 37, salgslinjen. Når du bokfører et salgsdokument, codeunit Sales-Post, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)] om brukeren har tillatelse til å endre Salgslinje-tabellen. Hvis ikke kan ikke kodeenheten fullføre oppgavene, og brukeren får en feilmelding. Hvis dette er tilfelle, kjører kodeenheten uten problemer.

Brukeren trenger imidlertid ikke full tilgang til tabellen Salgslinje for å kunne kjøre kodeenheten. Hvis brukeren har indirekte tillatelse til Salgslinje-tabellen, kjører codeunit Sales-Post uten problemer. Når en bruker har indirekte tillatelse, kan vedkommende bare endre tabellen Salgslinje ved å kjøre kodeenheten Sales-Post eller et annet objekt som har tillatelse til å endre tabellen Salgslinje. Brukeren kan bare endre Salgslinje-tabellen når det gjøres fra moduler som støttes. Brukeren kan ikke kjøre funksjonen ved en feiltakelse eller med onde hensikter ved hjelp av andre metoder.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Slik oppretter eller endrer du tillatelser ved å angi registrere handlingene

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Tillatelsessett** og velger den relaterte koblingen.
2. Du kan også gå til siden **Brukere** og velge handlingen **Tillatelsessett**.
3. På siden **Tillatelsessett** velger du handlingen **Ny**.
4. Fyll ut feltene etter behov på en ny linje.
5. Velg handlingen **Tillatelser**.
6. På **Tillatelser**-siden velger du **Registrer tillatelser**-handlingen, og velg deretter **Start**-handlingen.

    Dette starter en innspillingsprosess som fanger opp alle handlingene dine i brukergrensesnittet.
7. Gå til de ulike sidene og aktivitetene i [!INCLUDE[prod_short](includes/prod_short.md)] som du vil at brukere med dette tillatelsessettet skal få tilgang til. Du må utføre oppgaver som du vil registrere tillatelser for.
8. Når du vil avslutte opptaket, gå tilbake til **Tillatelser**-siden, og velg deretter **Stopp**-handlingen.
9. Velg **Ja**-knappen for å legge til registrerte rettigheter til det nye tillatelsessettet.
10. Angi om brukere skal kunne sette inn, endre eller slette poster i tabeller som er registrert for hvert objekt i listen over registrerte.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Sikkerhetsfiltre - Slik begrenser du brukerens adgang til bestemte poster i en tabell

For sikkerhet på postnivå i [!INCLUDE[prod_short](includes/prod_short.md)] bruker du sikkerhetsfiltrene til å begrense en brukers tilgang til data i en tabell. Du oppretter sikkerhetsfiltre på tabelldata. Et sikkerhetsfilter beskriver et sett med poster i en tablle som en bruker har tilgang til. Du kan for eksempel angi at en bruker bare kan lese poster som inneholder informasjon om en bestemt kunde. Dette betyr at brukeren ikke har tilgang til postene som inneholder informasjon om andre kunder. Hvis du vil ha mer informasjon, kan du se [Bruke sikkerhetsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) hjelpen for utviklere og IT-eksperter.

## <a name="to-manage-permissions-through-user-groups"></a>Slik behandler du tillatelser ved hjelp av brukergrupper

Du kan definere brukergrupper til å administrere tillatelsessett for grupper av brukere i firmaet.

Du starter med å opprette en brukergruppe. Deretter tilordner du tillatelsessett til gruppen for å definere hvilke objekter brukere av gruppen har tilgang til. Når du legger til en bruker i gruppen, vil tillatelsessettene som er definert for gruppen, gjelde for brukeren.

Tillatelsessett som tilordnes en bruker gjennom en brukergruppe, forblir synkronisert slik at en endring i brukergruppens tillatelser automatisk overføres til brukeren. Hvis du fjerner en bruker fra en brukergruppe, tilbakekalles de aktuelle tillatelsene automatisk.

### <a name="to-group-users-in-user-groups"></a>Slik grupperer du brukere i brukergrupper

Fremgangsmåten nedenfor forklarer hvordan du oppretter brukergrupper manuelt. Hvis du vil opprette brukergrupper automatisk, se [Slik kopierer du en brukergruppe og alle tillatelsessettene](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.
2. Du kan også gå til siden **Brukere** og velge handlingen **Brukergrupper**.
3. Gå til siden **Brukergruppe** og velg handlingen **Brukergruppemedlemmer**.
4. Velg **Legg til brukere** på siden **Brukergruppemedlemmer**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Slik kopierer du en brukergruppe og alle tillatelsessettene

For å definere en ny brukergruppe raskt kan du kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen.

> [!NOTE]
> Brukergruppemedlemmene kopieres ikke til den nye brukergruppen. Du må legge dem til manuelt etterpå. Hvis du vil ha mer informasjon, kan du se [Slik grupperer du brukere i brukergrupper](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.
2. Velg brukergruppen du vil kopiere, og velg deretter handlingen **Kopier brukergruppe**.
3. I feltet **Ny brukergruppekode** angir du et navn på gruppen, og velger deretter **OK**-knappen.

Den nye brukergruppen legges til på **Brukergrupper**-siden. Fortsett med å legge til brukere. Hvis du vil ha mer informasjon, kan du se [Slik grupperer du brukere i brukergrupper](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Slik tilordner du tillatelsessett til brukergrupper

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.
2. Velg brukergruppen du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Brukertillatelsessett** for å åpne siden **Brukertillatelsessett**.
4. På siden **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Slik tilordner du et tillatelsessett på siden **Tillatelsessett etter brukergruppe**

Fremgangsmåten nedenfor beskriver hvordan du kan tildele tillatelsessett til en brukergruppe på siden **Tillatelsessett etter brukergruppe**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. På siden **Brukere** velger du den aktuelle brukeren, og velger deretter handlingen **Tillatelsessett etter brukergruppe**.
3. På siden **Tillatelsessett etter brukergruppe** merker du av for **[brukergruppenavn]** for en linje for det aktuelle tillatelsessettet for å tilordne settet til brukergruppen.
4. Merk av for **Alle brukergrupper** for å tilordne tillatelsessettet til alle brukergrupper.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Slik fjerner du foreldede tillatelser fra alle tillatelsessett

1. På siden **Tillatelsessett** velger du handlingen **fjern foreldede tillatelsessett**.

## <a name="to-set-up-user-time-constraints"></a>Slik definerer du tidsbegrensninger for brukere:

Administratorer kan definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på. Administratorer kan også tilordne ansvarssentre til brukere. Hvis du vil ha mer informasjon, kan du se [Arbeide med ansvarssentre](inventory-responsibility-centers.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett** og velg den relaterte koblingen.
2. På siden **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.


## <a name="viewing-permission-changes-telemetry"></a>Vise telemetri ved tillatelsesendringer 

Du kan konfigurere at [!INCLUDE[prod_short](includes/prod_short.md)] skal sende endringer som er gjort i tillatelsen, til en Application Insights-ressurs i Microsoft Azure. Deretter kan du bruke Azure Monitor til å opprette rapporter og konfigurere varsler for de innsamlede dataene. Hvis du vil ha mer informasjon, kan du se følgende artikler i Hjelp for utviklere og IT-eksperter for [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Overvåke og analysere telemetri – aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysere telemetri for feltovervåking](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Se også

[Opprette brukere i henhold til lisenser](ui-how-users-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Legge til brukere i Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Sikkerhet og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjelpen for utviklere og IT-eksperter


[!INCLUDE[footer-include](includes/footer-banner.md)]