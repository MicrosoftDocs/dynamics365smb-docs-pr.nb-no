---
title: Tilpass sider for roller
description: 'Lær hvordan du tilpasser brukergrensesnittet for en profil (rolle), slik at alle brukere som har tilordnet rollen, ser et tilpasset arbeidsområde.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: 9171
ms.date: 08/25/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# Tilpass sider for profiler

Business Central inneholder både [tilpassing](ui-personalization-user.md) for brukere og egendefinering for administratorer. Med tilpassing kan brukere skreddersy arbeidsområdet ved å justere sideoppsett etter egne preferanser. Administratorer kan egendefinere sideoppsett for en bestemt profil, basert på forretningsroller og avdelinger, slik at alle tilordnede brukere ser samme egendefinerte side. Mens personlig tilpassing lar brukere vise, skjule og flytte felt og handlinger på en side, gir egendefinering ekstra muligheter. Egendefinering lar deg for eksempel vise felt som er i sidens kildetabell eller utvidelsestabeller, men som ikke er definert på sideobjektet&mdash;denne egendefineringen er ikke mulig.  <!--For more information, see [Personalize Your Workspace](ui-personalization-user.md).-->

<!--Similarly, administrators can customize pages for a profile, according to the related business role or department, so that all users assigned the profile see the customized page layout. As an administrator, you customize pages by using the same functionality as users do when they personalize pages, except with few extra capabilities. Like personalization, you can show, hide, and move fields, actions, or parts on a page. But while personalization only allows you to work with fields that are defined on the page object, customization allows you add fields that are in the source table or table extension, but not defined on the page object. -->

> [!NOTE]
> Den typiske forretningsbruken av en profil er en rolle. En profil er derfor kalt *Profil (rolle)* i grensesnittet.

Sidetilpassing starter fra siden **Profiler (roller)**, administratorens startpunkt for administrering av brukerprofiler på individuelle profilkort. I tillegg til å tilpasse sideoppsettet styrer du ulike innstillinger for profiler på siden **Profil (rolle)** for hver profil. Hvis du vil ha mer informasjon, kan du se [Administrere profiler](admin-users-profiles-roles.md).

## Forutsetninger

- Business Central-kontoen må ha **Profiladm. for D365**-tillatelsessett eller tilsvarende tillatelser. 

   Tillatelsessettet **Profiladm. for D365** inkluderer utføringstillatelsen på systemobjektet **9026 Legg til felt i tabellen**. Hvis du ikke har denne tillatelsen, kan du ikke legge til felt på siden med mindre de er definert i sideobjektet. 

## Egendefinere sider for en profil

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Profiler (roller)**, og velg deretter den relaterte koblingen.
2. Velg linjen for profilen du vil tilpasse sidene for, og velg deretter handlingen **Slett**.
3. Velg handlingen **Tilpass sider**.

    [!INCLUDE[prod_short](includes/prod_short.md)] åpnes i en ny leserkategori for den valgte profilen med banneret **Tilpasse** aktivert. Banneret **Tilpasning** tilbyr samme funksjonalitet som banneret **Tilpasning** som brukerne kan bruke.

4. Tilpass sider i henhold til behovene for gjeldende rolle eller avdeling, på samme måte som en bruker gjør ved tilpasning. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

    > [!NOTE]
    > Hvis du vil navigere under tilpasning, trykker du <kbd>Ctrl</kbd>+<kbd>Klikk</kbd> på en handling hvis den utheves av pilhodet.

5. Når du er ferdig med å endre oppsettet på én eller flere sider, velger du **Fullført**-knappen på banneret **Tilpasning**.
6. Lukk webleserkategorien.

Tilpassing av sider er nå registrert for profilen.

## Vise alle egendefinerte sider for en profil

Du kan få en oversikt over hvilke sider som er tilpasset for en profil, for eksempel for å planlegge hvilke sider som skal egendefineres ytterligere eller slettes.

- På siden **Profil (rolle)** velger du handlingen **Administrer tilpassede sider**.

På siden **Tilpassede sider** kan du slette tilpasninger, og du kan feilsøke ved å skanne etter mulige problemer.  

## Slette alle egendefineringer for en profil

Du kan avbryte alle tilpasninger du har gjort for en profil. Egendefineringer som er innført med en utvidelse, og egendefinering gjort av en bruker, slettes ikke. Du kan slette alle personlige tilpasninger med en annen handling. Hvis du vil ha mer informasjon, kan du se [Slette alle tilpasninger som er gjort av en bruker](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- På siden **Profil (rolle)** for en tilpasset profil velger du handlingen **Fjern tilpassede sider**.

Oppsettet på sider for profilen tilbakestilles til standardoppsettet.  

## Slette egendefinering for bestemte sider for en profil

Du kan slette individuelle sidetilpasninger som du har gjort for en profil. Egendefineringer som er innført med en utvidelse, og egendefinering gjort av en bruker, slettes ikke. Du kan slette spesifikke sidetilpasninger med en annen handling. Hvis du vil ha mer informasjon, se [Slette personlige tilpasninger for en bestemt side](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. På siden **Profil (rolle)** velger du handlingen **Administrer tilpassede sider**.
2. På siden **Tilpassede sider** velger du én eller flere linjer for sidetilpasninger du vil slette, og deretter velger du handlingen **Slett**.

Oppsettet på de valgte sidene justeres til endringene du har gjort.

## Legg til et felt

Du legger til felt på siden fra ruten **Legg til felt på side**, som du åpner ved å velge handlingen **+ Felt** når du er i egendefineringsmodus. Det er viktig å forstå at ruten **Legg til felt på side** brukes til å vise felt som allerede finnes&mdash;enten på siden og i kildetabellene,&mdash;, men som for øyeblikket er skjult. Du kan ikke opprette nye felt.

Ruten **Legg til felt på side** viser alle felt som kan vises på siden. Feltene deles inn i følgende kategorier, som bestemmes av den underliggende utformingen av selve siden, kildetabellen og utvidelser:

|Kategori|Description|
|-|-|
|Tabellfelter som ikke er på sideobjektet|Inkluderer felt som er definert i basistabellen eller utvidelsestabellene, men som ikke er definert på siden. Verktøytipset for disse feltene inkluderer etiketten **Definert av tabellen**.<br><br>|
|Sidefelter som er bundet til en tabell|Inkluderer felt som er definert i basistabellen eller tabellutvidelsene, og som også er definert på siden som vist eller skjult. Verktøytipset for disse feltene inkluderer etiketten **Definert av siden**.|
|Sidefelter som ikke er bundet til en tabell| Felt som bare er definert på siden, ikke i basetabellen eller utvidelsestabellene. Disse feltene brukes vanligvis til variabel eller beregning. Verktøytipset for disse feltene inkluderer etiketten **Definert av siden**.|

<!--
- Table fields not on the page object. Includes fields that are defined in the base table or extension tables, but aren't defined on the page, either as shown or hidden.   
- Page fields bound to a table. Includes fields that are defined in the base table or table extensions and are also defined on the page as either shown or hidden. 
 - Page fields that are not bound to a table. Fields that are Includes fields that are only defined on the page, not in base table or extension table. These fields typically used for variable or calculation. -->

Bruk filterknappen over listen til å endre hvilken feltkategori som vises: **Legg til felt**-side.  

:::image type="content" source="media/customization-filter.svg" alt-text="Viser filterknappen i ruten Legg til et felt i egendefineringsmodus.":::
 
### Legge til tabellfelter som ikke er på sideobjektet

Hvis du vil gjøre et rent tabellfelt tilgjengelig for brukere på en side, må du først legge det til på siden. Når du har lagt til feltet, kan brukerne velge å vise eller skjule feltet som de vil ved hjelp av tilpasning. Du kan legge til et felt på flere måter.

- Én måte er å dra det fra **Legg til felt til side**-ruten til ønsket plassering.
- En annen måte er å velge feltet i ruten for å vise den anbefalte plasseringen på siden. Gå deretter til feltplasseringen på sidene, velg pilspissen, og velg deretter **Legg til**. 

Når feltet er lagt til, endres verktøytipset for feltet i ruten **Legg til i side** til **Definert av siden**. Det tilføyde feltet er låst for redigering og kan ikke låses opp.

## Fjerne et felt

Hvis du har lagt til et tabellfelt som opprinnelig ikke var i sideobjektet, kan du fjerne det igjen. Å fjerne et felt er annerledes enn å skjule det. Når du skjuler et felt, kan brukerne fremdeles vise det i arbeidsområdet ved hjelp av personlig tilpasning. Hvis du imidlertid fjerner et felt, er ikke feltet lenger tilgjengelig for visning eller skjuling. Hvis feltet for øyeblikket vises i en brukers arbeidsområde, forsvinner det fra arbeidsområdet når du fjerner det. 

Hvis du vil fjerne et felt, velger du pilspissen i feltet på siden og deretter **Fjern**. Hvis du ikke finner feltet, velger du det i ruten **Legg til felt på side** for å angi den skjulte plasseringen. 

> [!IMPORTANT]
> Selv om du fjerner et felt, slettes ikke data som er lagret i feltet eller kildetabellene. Det fjerner bare feltet fra visningen. 

## Låse og låse opp redigering

Egendefinering lar deg låse (tillater redigering) eller låse opp redigering (hindrer redigering) av de fleste felt på en side. Hvis du vil låse eller låse opp redigering, merker du feltet på siden, velger pilhodet og deretter **Lås redigering** eøøer **Lås opp redigering**. Det er viktig å huske på noen regler om låsing og opplåsing av felt:

- Felt som opprinnelig ikke var i sideobjektet, men som ble lagt til på siden ved egendefinering, er alltid låst og kan ikke låses opp ved hjelp av egendefinering eller tilpasning.
- Utformingen av feltet kan også hindre at det blir redigert. Hvis AL-utvikleren setter egenskapen [Redigerbar egenskap](/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) til `false`, er den alltid låst og kan ikke låses opp.
- Det er viktig å merke seg at låseredigeringsfunksjonen er ment å hjelpe til med nøyaktigheten, konsistensen og påliteligheten til data. Det er ikke ment å sikre dataintegritet.


<!--However, whatever option you choose for a field, users can always change the setting on their own workspace using personalization. For this reason, it's important to consider locking as a deterrence measure and not a preventative measure.--> 
## Viktig informasjon og tips 

- Det er ikke sikkert at alle tabellfelt er tilgjengelige for egendefinering fra ruten **Legg til felt på side** . Utvikleren av en tabell kan velge å hindre at et felt vises i egendefinering ved å angi [egenskap AllowInCustomization](/dynamics365/business-central/dev-itpro/developer/properties/devenv-allowincustomizations-property) for feltet til `false`.
- Du kan ikke egendefinere en side som er i [analysemodus](analysis-mode.md). **Analyse**-bryteren er deaktivert. Hvis du bytter til egendefineringsmodus mens siden er i analysemodus, deaktiveres analysemodus automatisk. 
- Noen sider har flere sidefelt som tilordnes til samme kildetabell. Ruten **Legg til felt på side** viser alle disse sidefeltene uavhengig av hverandre. Du kan vise, skjule eller flytte disse feltene uavhengig av hverandre uten at det påvirker de andre.
- Hvis en del eller gruppe er skjult, kan du fremdeles identifisere skjulte felt i delen eller gruppen, men du kan ikke legge til, flytte eller vise felt i delen eller gruppen før de er synlige. 
## Se også

[Tilpass arbeidsområdet](ui-personalization-user.md)  
[Administrer profiler](admin-users-profiles-roles.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
