---
title: Definere detaljerte tillatelser
description: Denne artikkelen beskriver hvordan du definerer detaljerte tillatelser og tildeler hver bruker tillatelsessettet vedkommende trenger for å gjøre jobben.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
ms.service: dynamics-365-business-central
---

# Tilordne tillatelser til brukere og grupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

[!INCLUDE[prod_short](includes/prod_short.md)]-sikkerhetssystemet styrer hvilke objekter en bruker har tilgang til i hver database eller hvert miljø, sammen med brukerens lisens. For hver bruker kan du angi om de kan lese, endre eller angi data i de valgte databaseobjektene. Hvis du vil ha mer informasjon, se [Datasikkerhet](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) i utvikler- og administrasjonsinnholdet for [!INCLUDE[prod_short](includes/prod_short.md)].

Før du tilordner tillatelser til brukere og brukergrupper, må du definere hvem som kan logge på ved å opprette brukere i henhold til lisensen. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).

I [!INCLUDE[prod_short](includes/prod_short.md)] finnes det to nivåer med tillatelser til databaseobjekter:

- Generelle tillatelser i henhold til lisensen, også kalt rettighet.

  Lisensene inkluderer standard tillatelsessett. Fra lanseringsbølge 1 for 2022 kan administratorer tilpasse disse standardtillatelsene for de aktuelle lisenstypene. Hvis du vil ha mer informasjon, kan du se [Konfigurer tillatelser basert på lisenser](ui-how-users-permissions.md#licensespermissions).  

- Detaljerte tillatelser som du tildeler i [!INCLUDE[prod_short](includes/prod_short.md)].

Denne artikkelen beskriver hvordan du definerer og bruker tillatelser i [!INCLUDE [prod_short](includes/prod_short.md)] til å endre standardkonfigurasjonen.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Hvis du vil ha mer informasjon, kan du se [Delegert administratortilgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online inneholder standard brukergrupper som tildeler brukere automatisk basert på lisensen. Du kan endre standardkonfigurasjonen ved å endre eller legge til sikkerhetsgrupper, tillatelsessett og tillatelser. Følgende tabell beskriver nøkkelscenarioer for å endre standardtillatelsene.  

|Hvis du vil  |Se  |
|---------|---------|
|For å gjøre det enklere å behandle tillatelser for flere brukere, kan du organisere dem i sikkerhetsgrupper og dermed tilordne eller endre ett tillatelsessett for mange brukere i én handling.| [Slik behandler du tillatelser ved hjelp av brukergrupper](#to-manage-permissions-through-user-groups) |
|Slik behandler du tillatelsessett for bestemte brukere | [Slik tilordner du tillatelsessett til brukere](#to-assign-permission-sets-to-users) |
|Slik lærer du hvordan du definerer et tillatelsessett|[Slik oppretter du et tillatelsessett](#to-create-a-permission-set)|
|Slik viser eller feilsøker du en brukers tillatelser|[For å få en oversikt over en brukers tillatelser](#to-get-an-overview-of-a-users-permissions)|
|Slik lærer du om sikkerhet på postnivå|[Sikkerhetsfiltre begrenser brukerens tilgang til bestemte poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> En bredere måte for å definere hvilke funksjoner brukere har tilgang til, er å angi **Opplevelse**-feltet på siden **Selskapsopplysninger**. Hvis du vil ha mer informasjon, kan du se [Endre hvilke funksjoner som vises](ui-experiences.md).
>
> Du kan også definere funksjonene som er tilgjengelige for brukere i brukergrensesnittet, og hvordan de samhandler med dem gjennom sider. Dette gjør du gjennom profiler som du tilordner til ulike typer brukere i henhold til jobbrolle eller avdeling. Hvis du vil ha mer informasjon, kan du se [Administrere profiler](admin-users-profiles-roles.md) og [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## Slik oppretter du et tillatelsessett

> [!NOTE]
> I lanseringsbølge 2 i 2022 gjorde vi det enklere å legge til tillatelser i tillatelsessett. I stedet for å legge til tillatelser enkeltvis, kan du legge til hele tillatelsessett. Om nødvendig kan du utelate individuelle tillatelser. Hvis du vil ha mer informasjon, kan du se [Slik legger du til andre tillatelsessett](#to-add-other-permission-sets). For å gjøre dette mulig erstattet vi siden Tillatelsessett med en ny side. Nøkkelforskjellene er de nye rutene **Tillatelsessett** og **Resultater** og faktaboksen **Inkluderte tillatelser**. Hvis du vil fortsette å bruke den erstattede siden Tillatelser, velger du handlingen **Tillatelser (eldre)** på siden **Tillatelsessett**.

Vedlikehold er også enklere. Når du legger til systemtillatelser, oppdateres det brukerdefinerte tillatelsessettet automatisk med endringer som Microsoft gjør med disse tillatelsene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Tillatelsessett** og velger den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg handlingen **Tillatelser**.
5. På siden **Tillatelsessett** tar du med eller utelater tillatelsene for objektet i **Type**-feltet som følger:

  For å inkludere tillatelsen velger du **Inkluder** og deretter tilgangsnivået som skal gis i feltene **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**. Tabellen nedenfor beskriver alternativene.

  |Alternativ|Description|Rangering|
  |------|-----------|-------|
  |**Tom**|Brukeren kan ikke utføre handlingen for objektet.|Laveste|  
  |**Ja**|Brukeren kan utføre handlingen for objektet.|Høyeste|
  |**Indirekte**|Brukeren kan utføre handlingen for objektet, men bare via et annet tilknyttet objekt som brukeren har full tilgang til. Hvis du vil ha mer informasjon, kan du se [Eksempel – indirekte tillatelse](#example---indirect-permission) i denne artikkelen og [Tillatelser-egenskapen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) i hjelpen for utviklere og IT-eksperter.|Nest høyeste|
  
  Hvis du vil utelate tillatelsen eller et eller flere tilgangsnivåer, velger du **Utelat**, og deretter velger du tilgangsnivået du vil gi. Tabellen nedenfor beskriver alternativene.

  |Alternativ|Description|
  |------|-----------|-------|
  |**Tom**|Bruk tilgangsnivået basert på hierarkiet med tillatelser i settet.  |
  |**Utelat**|Fjern det spesifikke tilgangsnivået for objektet.|
  |**Reduser til indirekte**|Endre tilgangsnivået til indirekte hvis det er noen tillatelsessett som gir direkte tilgang til objektet. Velg for eksempel dette alternativet hvis tillatelsessettet gir direkte tilgang til finansposter, men du ikke vil at brukerne skal ha full tilgang til postene.|
  
  > [!NOTE]
  > Hvis en tillatelse er i et tillatelsessett som er inkludert, og også er i et tillatelsessett som er ekskludert, blir tillatelsen utelatt.

6. Bruk feltene **Objekttype** og **Objekt-ID** til å angi objektet du gir tilgang til.

  > [!TIP]
  > Nye linjer viser standardverdier. Feltet **Objekttype** inneholder for eksempel **tabelldata**, og feltet **Objekt-ID** inneholder **0**. Standardverdiene er bare plassholdere, og de brukes ikke. Du må velge en objekttype og et objekt i feltet **Objekt-ID** før du kan opprette en ny linje.

7. Valgfritt: Hvis du definerer tillatelser for en dataobjekttype for tabell, kan du filtrere dataene som en bruker har tilgang til i feltene i den valgte tabellen, i feltet **Sikkerhetsfilter**. Det kan for eksempel hende at du vil gi en bruker tilgang til bare å lese poster som inneholder informasjon om en bestemt kunde. Hvis du vil ha mer informasjon, kan du se [Sikkerhetsfiltre begrense en brukers tilgang til bestemte poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table) og [Bruk sikkerhetsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valgfritt: Legg til et eller flere andre tillatelsessett i ruten **Tillatelsessett**. Hvis du vil ha mer informasjon, kan du se [Slik legger du til andre tillatelsessett](#to-add-other-permission-sets).

> [!IMPORTANT]
> Vær forsiktig når du tilordner **innsettingstillatelse** eller **endringstillatelse** til gruppen **9001 brukergruppemedlem** eller **9003 gruppetillatelsessett for bruker**. Alle brukere som er tilordnet tillatelsessettet, kan potensielt tilordne seg selv til andre brukergrupper, som i sin tur kan gi dem utilsiktede tillatelser.

### Eksempel - indirekte tillatelse

Du kan tildele indirekte tillatelse for å la en bruker bruke et objekt, men bare via et annet objekt. En bruker har for eksempel tillatelse til å kjøre codeunit 80, Sales-Post. Kodeenheten Sales-Post utfører mange oppgaver, inkludert å endre tabell 37, salgslinjen. Når brukeren bokfører et salgsdokument med Sales-Post codeunit, kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)] om brukeren har tillatelse til å endre Salgslinje-tabellen. Hvis ikke kan ikke codeunit fullføre oppgavene, og brukeren får en feilmelding. Hvis dette er tilfelle, kjører kodeenheten uten problemer.

Brukeren trenger imidlertid ikke full tilgang til tabellen Salgslinje for å kunne kjøre codeunit. Hvis brukeren har indirekte tillatelse til Salgslinje-tabellen, kjører codeunit Sales-Post uten problemer. Når en bruker har indirekte tillatelse, kan vedkommende bare endre tabellen Salgslinje ved å kjøre codeunit Sales-Post eller et annet objekt som har tillatelse til å endre tabellen Salgslinje. Brukeren kan bare endre Salgslinje-tabellen når det gjøres fra moduler som støttes. Brukeren kan ikke kjøre funksjonen ved en feiltakelse eller med onde hensikter ved hjelp av andre metoder.

### Slik legger du til tillatelsessett

Utvid et tillatelsessett ved å legge til andre tillatelsessett i det. Etterpå kan du inkludere eller utelate bestemte tillatelser eller hele tillatelsessett, i hvert sett du legger til. Dette omfatter tillatelser i tillatelsessettene Utvidelse og Systemtype, noe som ellers ikke er tillatt. Utelatelser gjelder bare tillatelsessettet du utvider. Det opprinnelige settet påvirkes ikke.

På siden **Tillatelsessett** legger du til et tillatelsessett i ruten **Tillatelsessett**. Ruten **Resultat** viser en oversikt over alle tillatelsessett som er lagt til. Hvis du vil utforske tillatelsene som er inkludert i et sett du har lagt til, velger du settet i Resultat-ruten så viser faktaboksen **Inkluderte tillatelser** tillatelsene.

I **Resultat**-ruten bruker du feltet **Inkluderingsstatus** til å identifisere tillatelsessettene der du har utelatt tillatelser eller tillatelsessett. Hvis noe er utelatt, er statusen **Delvis**.

Hvis du vil ha en samlet visning av tillatelser i tillatelsessettet, velger du handlingen **Vis alle tillatelser**. Siden **Utvidede tillatelser** viser alle tillatelser som allerede er tildelt tillatelsessettet, og tillatelsene i de tilføyde tillatelsessettene.

Hvis du vil utelukke alle tillatelser fra et tillatelsessett, merker du linjen i **Resultat**-ruten, velger **Vis flere alternativer** og velger **Utelat**. Når du utelater et tillatelsessett, opprettes en linje i ruten **Tilgangssett** i typen Utelukket. Hvis du har utelukket et tillatelsessett, men vil ta det med på nytt, sletter du linjen i ruten **Tillatelsessett**.

Hvis du vil utelukke eller delvis utelukke en bestemt tillatelse i et sett du har lagt til, oppretter du en linje for objektet under **Tillatelser**. Feltene for tilgangsnivå, Innsettingstillatelse, Endringstillatelse og så videre vil alle inneholde **Utelat**. Hvis du vil tillate et bestemt tilgangsnivå, velger du det aktuelle alternativet.

Når du utelater et tillatelsessett, ekskluderes alle tillatelsene i settet. [!INCLUDE [prod_short](includes/prod_short.md)] beregner tillatelser som følger:

1. Beregn hele listen over inkluderte tillatelser
2. Beregn hele listen over utelatte tillatelser
3. Fjern utelatte tillatelser fra listen over inkluderte tillatelser (fjerning av en indirekte tillatelse er det samme som Reduser til Indirekte)

## Slik kopiere du et tillatelsessett

Opprett et nytt tillatelsessett ved å kopiere et annet. Det nye settet vil inneholde alle tillatelser og tillatelsessett fra settet du har kopiert. Hvordan tillatelsene og tillatelsessettene ordnes i det nye tillatelsessettet, er avhengig av valget i **Kopier operasjon**-feltet. Tabellen nedenfor beskriver alternativene.

|Alternativ  |Description  |
|---------|---------|
|**Kopier etter referanse**     | Det opprinnelige tillatelsessettet og alle tillatelsessettene som ble lagt til det, vises i **Resultat**-ruten.       |
|**Kopi med flat tillatelse**  | Alle tillatelser fra alle tillatelsessettene inkluderes i en flat liste i **Tillatelser**-ruten. Tillatelser er ikke ordnet etter tillatelsessett.        |
|**Klon**     | Opprett en nøyaktig kopi av det opprinnelige tillatelsessettet.        |

1. På siden **Tillatelsessett** merker du linjen for et tillatelsessett du vil kopiere, og velger deretter handlingen **Kopier tillatelsessett**.
2. På siden **Kopier tillatelsessett** angir du navnet på det nye tillatelsessettet.
3. I **Kopier operasjon**-feltet angir du hvordan du vil ordne tillatelse i det nye tillatelsessettet.
4. Valgfritt: Hvis du legger til et systemtillatelsessett, blir du kanskje varslet hvis navnet eller innholdet i det opprinnelige tillatelsessettet endres i en fremtidig versjon. Dette gjør at du kan vurdere om du vil oppdatere det brukerdefinerte tillatelsessettet. Hvis du vil motta en melding, slår du på vekslebryteren **Varsel ved endret tillatelsessett**.

> [!NOTE]
> Varslingen krever at varslingen **Opprinnelig systemtillatelsessett er endret** er aktivert på siden **Mine varslinger**.

## Slik oppretter eller endrer du tillatelser ved å angi registrere handlingene

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Tillatelsessett** og velger den relaterte koblingen.

    Du kan også gå til siden **Brukere** og velge handlingen **Tillatelsessett**.
2. På siden **Tillatelsessett** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov på en ny linje.
4. Velg handlingen **Tillatelser**.
5. På **Tillatelser**-siden velger du **Registrer tillatelser**-handlingen, og velg deretter **Start**-handlingen.  
    Opptaket må utføres ved å bruke funksjonen **Åpne siden i et nytt vindu** (popup) for å få **Tillatelser**-opptaksvinduet side ved side, eller ved å arbeide i samme fane.  
    En innspillingsprosess starter og registrerer alle handlingene dine i brukergrensesnittet.
6. Gå til de ulike sidene og aktivitetene i [!INCLUDE[prod_short](includes/prod_short.md)] som du vil at brukere med dette tillatelsessettet skal få tilgang til. Du må utføre oppgaver som du vil registrere tillatelser for.
7. Når du vil avslutte opptaket, gå tilbake til **Tillatelser**-siden, og velg deretter **Stopp**-handlingen.
8. Velg **Ja**-knappen for å legge til registrerte rettigheter til det nye tillatelsessettet.
9. Angi om brukere skal kunne sette inn, endre eller slette poster i tabeller som er registrert for hvert objekt i listen over registrerte.

### Slik eksporterer og importerer du et tillatelsessett

Hvis du vil definere tillatelser raskt, kan du importere tillatelsessett du har eksportert fra en annen [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker.

I miljøer med mange leietakere importeres et tillatelsessett til en spesiell leietaker. Med andre ord er omfanget av importen *Leier*.

1. I leietaker 1 på siden **Tillatelsessett** merker du linjen eller linjene for tillatelsessettene du vil eksportere, og velger deretter handlingen **Eksporter tillatelsessett**.

    En XML-fil opprettes i nedlastingsmappen på maskinen. Som standard kalles den *Eksporter tillatelsessett.XML*.

2. I leietaker 2 på **Tillatelsessett**-siden velger du handlingen **Importer tillatelsessett**.
3. På siden **Importer tillatelsessett** må du vurdere om du vil slå sammen eksisterende tillatelsessett med nye tillatelsessett i XML-filen.

    Hvis du merker av for **Oppdater eksisterende tillatelser**, slås eksisterende tillatelsessett med samme navn som i XML-filen, sammen med de importerte tillatelsessettene.

    Hvis du ikke merker av for **Oppdater eksisterende tillatelser**, blir eksisterende tillatelsessett med samme navn i XML-filen, hoppet over under importen. I dette tilfellet blir du varslet om tillatelsessett som hoppes over.

4. Fra siden **Importer** finner og velger du XML-filen som skal importeres, og velger handlingen **Åpne**.

Tillatelsessettene importeres.

## Slik fjerner du foreldede tillatelser fra alle tillatelsessett

På siden **Tillatelsessett** velger du handlingen **fjern foreldede tillatelsessett**.

## Slik definerer du tidsbegrensninger for brukere

Administratorer kan definere tidsperioder som de bestemte brukerne kan bokføre. Administratorer kan også angi om system logger hvor lang tid brukere er logget på. Administratorer kan også tildele ansvarssentre til brukere. Hvis du vil ha mer informasjon, kan du se [Arbeide med ansvarssentre](inventory-responsibility-centers.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett** og velg den relaterte koblingen.
2. På siden **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.

## Slik behandler du tillatelser ved hjelp av brukergrupper

Brukergrupper hjelper deg med å håndtere tillatelsessett i hele selskapet. [!INCLUDE [prod_short](includes/prod_short.md)] online inneholder standard brukergrupper som tildeler brukere automatisk basert på lisensen. Du kan legge til brukere manuelt i en brukergruppe, og du kan opprette nye brukergrupper som kopier av eksisterende filer.  

Du starter med å opprette en brukergruppe. Deretter tilordner du tillatelsessett til gruppen for å definere hvilke objekter brukere av gruppen har tilgang til. Når du legger til en bruker i gruppen, vil tillatelsessettene som er definert for gruppen, gjelde for brukeren.

Tillatelsessett som tildeles en bruker gjennom en brukergruppe, forblir synkronisert. En endring i brukergruppetillatelsene overføres automatisk til brukerne. Hvis du fjerner en bruker fra en brukergruppe, tilbakekalles de aktuelle tillatelsene automatisk.

### Slik legger du til brukere i en brukergruppe

Fremgangsmåten nedenfor forklarer hvordan du oppretter brukergrupper manuelt. Hvis du vil opprette brukergrupper automatisk, se [Slik kopierer du en brukergruppe og alle tillatelsessettene](#to-copy-a-user-group-and-all-its-permission-sets).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.

    1. Du kan også gå til siden **Brukere** og velge handlingen **Brukergrupper**.
2. Gå til siden **Brukergruppe** og velg handlingen **Brukergruppemedlemmer**.
3. Velg **Legg til brukere** på siden **Brukergruppemedlemmer**.

### Slik kopierer du en brukergruppe og alle tillatelsessettene

For å definere en ny brukergruppe raskt kan du kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen.

> [!NOTE]
> Brukergruppemedlemmene kopieres ikke til den nye brukergruppen. Du må legge dem til manuelt etterpå. Hvis du vil ha mer informasjon, kan du se delen [Slik legger du til brukere i en brukergruppe](#to-add-users-to-a-user-group).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.
2. Velg brukergruppen du vil kopiere, og velg deretter handlingen **Kopier brukergruppe**.
3. I feltet **Ny brukergruppekode** angir du et navn på gruppen, og velger deretter **OK**-knappen.

Den nye brukergruppen legges til på **Brukergrupper**-siden. Fortsett med å legge til brukere. Hvis du vil ha mer informasjon, kan du se delen [Slik legger du til brukere i en brukergruppe](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Du får en valideringsfeil hvis du prøver å tildele en brukergruppe til brukeren som henviser til et tillatelsessett som ble definert i en avinstallert utvidelse. Det er fordi app-ID-en til utvidelsen valideres når det henvises til den. Hvis du vil tildele brukergruppen til en bruker, kan du enten installere utvidelsen på nytt, fjerne referansen for den avinstallerte utvidelsen fra tillatelsessettet, eller fjerne tillatelsessettet fra brukergruppen.

### Slik tilordner du tillatelsessett til brukergrupper

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukergrupper** og velg den relaterte koblingen.
2. Velg brukergruppen du vil tilordne tillatelse til.  

    Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Brukertillatelsessett** for å åpne siden **Brukertillatelsessett**.
4. På siden **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje.

### Slik tilordner du et tillatelsessett på siden **Tillatelsessett etter brukergruppe**

Fremgangsmåten nedenfor beskriver hvordan du kan tildele tillatelsessett til en brukergruppe på siden **Tillatelsessett etter brukergruppe**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. På siden **Brukere** velger du den aktuelle brukeren, og velger deretter handlingen **Tillatelsessett etter brukergruppe**.
3. På siden **Tillatelsessett etter brukergruppe** velger du feltet **[brukergruppenavn]** for en linje for det aktuelle tillatelsessettet for å tilordne settet til brukergruppen.
4. Merk av for **Alle brukergrupper** for å tilordne tillatelsessettet til alle brukergrupper.

Du kan også tildele tillatelsessett direkte til en bruker.

## Slik tilordner du tillatelsessett til brukere

Et tillatelsessett er en samling tillatelser for bestemte databaseobjekter. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[prod_short](includes/prod_short.md)].  

En [!INCLUDE[prod_short](includes/prod_short.md)]-løsning inneholder forhåndsdefinerte tillatelsessett som legges til av Microsoft eller løsningsleverandøren. Du kan også legge til nye tillatelsessett som er skreddersydd for å dekke behovene i organisasjonen. Hvis du vil ha mer informasjon, kan du se delen [Slik oppretter du et tillatelsessett](#to-create-a-permission-set).

> [!NOTE]
> Hvis du ikke vil begrense brukerens tilgang mer enn det som allerede er definert av lisensen, kan du tilordne et spesielt tillatelsessett som kalles SUPER for brukeren. Dette tillatelsessettet sikrer at brukeren har tilgang til alle objektene som er angitt i lisensen.
>
> En bruker med Essential-lisensen og SUPER-tillatelsessettet har tilgang til mer funksjonalitet enn brukere med Team Member-lisensen og SUPER-tillatelsessettet.

Du kan tilordne tillatelsessett til brukere på to måter:

- Fra **Brukerkort**-siden ved å velge tillatelsessettet som skal tilordnes brukeren.
- Fra siden **Tillatelsessett etter bruker** ved å velge brukere som et tillatelsessett er tilordnet til.

### Slik tilordner du et tillatelsesett på et brukerkort

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-siden.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. Hvis du vil ha mer informasjon, kan du se [Slik oppretter eller redigerer du et tillatelsessett](ui-define-granular-permissions.md#to-create-a-permission-set).

   Bruk **Selskap**-feltet for å bruke tillatelsessett på et bestemt selskap. Hvis du lar feltet stå tomt, gjelder det for alle selskaper.

## Slik tilordner du et tillatelsessett på siden Tillatelsessett etter bruker

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. På siden **Brukere** velger du handlingen **Tillatelsessett etter bruker**.
3. På siden **Tillatelsessett etter bruker** merker du av for **[brukernavn]** for en linje for det aktuelle tillatelsessettet for å tildele settet til brukeren.

    Merk av for **Alle brukere** for å tildele tillatelsessettet til alle brukere.

## For å få en oversikt over en brukers tillatelser

Du kan vise andre brukeres gyldige tillatelser bare hvis du tilordner til tillatelsessettet SUPER eller SECURITY. 

Siden **Gjeldende tillatelser** inneholder tilleggsinformasjon om kilden til hver tillatelse. Du kan for eksempel velge om kilden er en sikkerhetsgruppe, eller om det skal arves en tillatelse. Siden inneholder også en kolonne der administratorer kan se gjennom sikkerhetsfiltrene som brukes. Hvis du vil ha mer informasjon om sikkerhetsfiltre, kan du gå til [Sikkerhetsfiltre begrense en brukers tilgang til bestemte poster i en tabell](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

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
    > For en forklaring av rangering kan du se [Slik oppretter du et tillatelsessett](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Hvis du vil redigere et tillatelsessett, går du til delen **Etter tillatelsessett** og linjen for et relevant tillatelsessett av typen **Brukerdefinerte** og velger ett av de fem tilgangstypefeltene og en annen verdi.

5. Hvis du vil redigere enkelttillatelser i tillatelsessettene, kan du velge verdien i feltet **Tillatelsessett** for å åpne **Tillatelser**-siden.

> [!NOTE]  
> Når du redigerer et tillatelsessett, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

### Sikkerhetsfiltre begrenser brukerens tilgang til bestemte poster i en tabell

For sikkerhet på postnivå i [!INCLUDE[prod_short](includes/prod_short.md)] bruker du sikkerhetsfiltrene til å begrense en brukers tilgang til data i en tabell. Du oppretter sikkerhetsfiltre på tabelldata. Et sikkerhetsfilter beskriver et sett med poster i en tablle som en bruker har tilgang til. Du kan for eksempel angi at en bruker bare kan lese poster som inneholder informasjon om en bestemt kunde. På denne måten har ikke brukeren tilgang til postene som inneholder informasjon om andre kunder. Hvis du vil ha mer informasjon, kan du se [Bruk sikkerhetsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) i administrasjonsinnholdet.

## Vise telemetri ved tillatelsesendringer

Du kan konfigurere at [!INCLUDE[prod_short](includes/prod_short.md)] skal sende endringer som er gjort i tillatelsen, til en Application Insights-ressurs i Microsoft Azure. Deretter kan du bruke Azure Monitor til å opprette rapporter og konfigurere varsler for de innsamlede dataene. Hvis du vil ha mer informasjon, kan du se følgende artikler i Hjelp for utviklere og administratorer for [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Overvåke og analysere telemetri – aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysere telemetri for feltovervåking](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## Delegerte administratorbrukere

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## Se også

[Opprette brukere i henhold til lisenser](ui-how-users-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Legge til brukere i Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Sikkerhet og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjelpen for utviklere og IT-eksperter  
[Tilpass en telemetri-ID til brukere](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
