---
title: Behandle brukere og roller
description: Finn ut hvordan du administrerer brukerprofiler i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# <a name="manage-user-profiles"></a>Administrer brukerprofiler

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Tilordne alle brukere til profiler som gjenspeiler:

* Forretningsrollen
* Avdelingen de arbeider i
* En annen type kategorisering

Profiler gjør det mulig for systemansvarlige å definere og håndtere ulike typer brukere som har tilgang til Business Central.

Den typiske forretningsbruken av en profil er en rolle. En profil er derfor kalt *Profil (rolle)* i grensesnittet.

Som administrator kan du opprette og behandle profiler på siden **Profiler (roller)**. Hver profil har et kort der du behandler innstillinger for den relaterte rollen. Kortet inneholder følgende informasjon:

* Navnet på rollen
* Brukerinnstillinger
* Rollesenteret som profilen bruker

Hvis du vil ha mer informasjon om brukerinnstillinger og rollesentre, se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Før du kan administrere brukernes profiler må brukerne opprettes og legges til ved hjelp av administrasjonssenteret for Microsoft 365. Deretter kan du tilordne tillatelser til hver bruker eller brukergruppe. Tillatelser definerer hvilke funksjoner brukere kan få tilgang til. Hvis du vil ha mer informasjon om tillatelsesinnstillinger, kan du se [Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)

## <a name="page-customization"></a>Sidetilpasning

Du kan tilpasse sideoppsett for en profil, slik at alle brukerne som er tilordnet profilen, ser de tilpassede sidene. Som administrator kan du tilpasse sider ved å bruke samme funksjonalitet som brukere gjør når de tilpasser. Hvis du vil ha mer informasjon om hvordan du tilpasser sideoppsett, kan du se [Tilpass sider for profiler](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Slik oppretter du en profil

Hvis du ikke kan kopiere en eksisterende profil, kan du opprette en ny manuelt.

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og skriv inn **Profiler (roller)**, og velg deretter den relaterte koblingen.  
2. På siden **Profiler (roller)** velger du handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du vil at en bestemt profil skal være tilgjengelig bare for svært spesifikke brukere, kan du sette **Beskrivelse**-feltet til `Navigation menu only.`. På denne måten utelates profilen fra listen over tilgjengelige roller i **Mine innstillinger**.

## <a name="to-copy-a-profile"></a>Kopiere en profil

Hvis du vil spare tid, kan du opprette en ny profil ved å kopiere en eksisterende. Kopier en som har lignende innstillinger som den du vil opprette.

Når du kopierer en profil, kopieres alle de involverte sidetilpassingene i tillegg, både brukeropprettede og de som utledes fra utvidelsene.

1. På siden **Profiler (roller)** merker du linjen for profilen du vil kopiere, og deretter velger du handlingen **Kopier profil**.
2. Fyll ut feltene **Profil-ID** og **Visningsnavn**, og velg deretter **OK**.
3. Åpne siden **Profiler (roller)**, åpne det nylig opprettede profilkortet, og rediger deretter andre felt etter behov.

## <a name="to-edit-a-profile"></a>Redigere en profil

Du kan redigere en profil ved å endre feltene på siden **Profiler (roller)**. Endringene vil imidlertid ikke være synlige for brukeren som har tildelt profilen, før de logges av og igjen.

> [!Caution]
> Ikke gi nytt navn til en profil mens brukere tilordnet profilen er logget på, siden brukere kan oppleve at produktet fryser og må startes på nytt.

## <a name="to-assign-a-profile-to-a-user"></a>Tilordne en profil til en bruker

Brukere kan tildele seg selv en rolle (som representerer en profil) ved å velge feltet **Rolle** på siden **Mine innstillinger**. Som administrator kan du gjøre det samme på siden **Profiler (roller)**.

1. På siden **Profiler (roller)** merker du profilen du vil tilordne, og deretter velger du handlingen **Brukertilpasningsliste**.
2. På siden **Brukertilpasninger** merker du brukeren du vil tilordne profilen til, og deretter velger du handlingen **Rediger**.
3. I feltet **Profil-ID** velger du den relevante profilen.

Hvis du tilordner en annen profil til en bruker, beholdes eventuelle tilpasninger som er gjort av brukeren med den forrige profilen.

## <a name="to-define-user-settings-for-a-profile"></a>Definere brukerinnstillinger for en profil

På siden **Mine innstillinger** kan brukerne definere grunnleggende virkemåte for kontoen, for eksempel Rollesenteret, språket og hvilke meldinger de får. Hvis du vil ha mer informasjon om brukerinnstillinger, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Som administrator kan du definere innstillinger for en profil. Innstillingene gjelder for alle brukerne som er tilordnet rollen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Profiler (roller)**, og velg deretter den relaterte koblingen.
2. Velg linje for profilen du vil endre brukerinnstillinger for, og velg deretter handlingen **Brukertilpasningsliste**.
3. Åpne siden **Brukertilpasninger**, åpne kortet for brukeren du vil endre innstillinger for.
4. På siden **Brukertilpasningskort** redigerer du feltene etter behov.

## <a name="to-activate-a-profile"></a>Aktivere en profil

Når du oppretter en profil, kan du definere om, hvor og hvordan profilen og den tilhørende informasjonen er tilgjengelig for brukerne.

På siden **Profiler (roller)** merker du av for følgende avmerkingsbokser:

* **Aktivert** for å angi om den relaterte rollen er synlig på siden **Tilgjengelige roller**, slik at brukerne kan velge.  
* **Bruk som standardprofil** for å angi profilen som gjelder for brukere som ikke er tildelt en bestemt rolle.
* **Deaktiver tilpasning** for å angi om brukere av den relaterte rollen kan tilpasse arbeidsområdet sitt.
* **Vis i Rolletforsker** for å angi om handlinger til forretningsfunksjoner som er inkludert i profilen, vises i utvidet visning av rolleutforskeren, en funksjonsoversikt. Hvis du vil ha mer informasjon om rolleutforskeren, kan du se [Finn sider med rolleutforskeren](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Slik eksporterer du profiler

Du kan eksportere profiler fra [!INCLUDE[prod_short](includes/prod_short.md)] og bruke dem på nytt i en annen leier. Profilene eksportere til en ZIP-fil som inneholder AL-filene (programspråk). Du kan gjenbruke AL-filene for å utvikle utvidelser. Hvis du vil ha mer informasjon om å eksportere profiler, kan du se [Bruk klienten til å opprette profiler og sidetilpasninger](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* På siden **Profiler (roller)** velger du handlingen **Eksporter profiler**.

    Denne handlingen eksporterer en zip-fil som inneholder AL-filene for alle profiler.

## <a name="to-import-profiles"></a>Slik importerer du profiler

Du kan importere profiler som er eksportert fra Business Central. Trinnene er mer eller mindre enn de motsatte av trinnene for å eksportere profiler.

1. På siden **Profiler (roller)** velger du handlingen **Importer profiler**.
1. Følg trinnene i veiviseren **Importere profiler**.

    Hvis du bare vil importere valgte profiler, bruker du avmerkingsboksen **Valgt** til å angi hvilken som skal importeres.
1. Velg knappen **Importer valgt**.

    Denne handlingen importerer en zip-fil som inneholder AL-filene for de valgte profilene.

## <a name="to-delete-a-profile"></a>Slette en profil

Du kan slette en profil ved å velge **Slett**-handlingen på siden **Profiler (roller)**. Følgende begrensninger gjelder imidlertid:

* Du kan ikke slette en profil som er tildelt en bruker eller en brukergruppe.
* Du kan ikke slette profiler som stammer fra utvidelser. Filtypen må først avinstalleres.
* Du kan bare slette én profil om gangen.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Slette alle tilpasninger som er gjort av brukeren

Du kan slette alle endringene en bruker gjør på sidene. Dette kan være nyttig å slette endringer hvis for eksempel en ansatt endrer rolle og ikke lenger trenger dem. Profilen definerer sideoppsettet, og slettinger gjenoppretter det til denne definisjonen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukertilpasninger**, og velg deretter den relaterte koblingen.

    Siden **Brukertilpasninger** viser alle brukere som gjør tilpasninger.

2. Åpne kortet for en bruker som har tilpasningene du vil slette.
3. Velg siden **Brukertilpasningskort**, velg handlingen **Fjern tilpassede sider**, og godta deretter meldingen som vises.

Brukeren vil se endringene neste gang vedkommende logger på.

Du kan også slette alle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette alle tilpasninger for en profil](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Slette tilpasninger for bestemte sider

Du kan slette tilpasninger som én eller flere brukere gjør på bestemte sider. Sletting av tilpasninger kan være nyttige hvis en forretningsprosessendring betyr at en personalisering ikke lenger kan brukes. Slettinger gjenoppretter sideoppsettet tilbake til det som profilen definerer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukersidetilpasninger**, og velg deretter den relaterte koblingen.

    **Brukersidetilpasninger** viser alle sidene som er tilpasset, og brukeren de tilhører.

    Hvis det er merket av for feltet **Gammel tilpassing**, angir dette at tilpassingen ble utført i en eldre versjon av [!INCLUDE[prod_short](includes/prod_short.md)], som håndterte tilpassing annerledes. Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden.

2. Velg linjen for sidetilpassingen du vil slette, og velg deretter handlingen **Slett**.

Brukeren vil se endringene neste gang vedkommende logger på.  

Du kan også slette individuelle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette tilpasninger for en bestemt side for en profil](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Behandle brukerøkter

Du kan som administrator for [!INCLUDE[prod_short](includes/prod_short.md)] online behandle brukerøkter i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Behandle økter][def] i administrasjonsinnholdet.  

For lokal [!INCLUDE[prod_short](includes/prod_short.md)] kan du for eksempel behandle økter som bruker SQL Server Management Studio. Hvis du vil ha mer informasjon, kan du se [teknisk dokumentasjon for SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Se også

[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Tilpass sider for profiler](ui-personalization-manage.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
