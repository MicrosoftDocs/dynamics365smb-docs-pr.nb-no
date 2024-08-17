---
title: Behandle brukere og roller
description: Finn ut hvordan du administrerer brukerprofiler i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# <a name="manage-user-profiles"></a>Administrer brukerprofiler

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

## <a name="create-a-profile"></a>Opprette en profil

Hvis du ikke kan kopiere en eksisterende profil, kan du opprette en ny manuelt.

1. Velg den ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") , angi **Profiler (roller),** og Velg deretter den relaterte opprette en kobling.  
2. På **siden Profiler (roller)**  Velg handlingen **Ny** .  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du vil at en bestemt profil skal være tilgjengelig bare for svært spesifikke brukere, kan du sette **Beskrivelse**-feltet til `Navigation menu only.`. På denne måten utelates profilen fra listen over tilgjengelige roller i **Mine innstillinger**.

## <a name="copy-a-profile"></a>Kopiere en profil

Hvis du vil spare tid, kan du opprette en ny profil ved å kopiere en eksisterende. Kopier en som har lignende innstillinger som den du vil opprette.

Når du kopierer en profil, kopieres alle de involverte sidetilpassingene i tillegg, både brukeropprettede og de som utledes fra utvidelsene.

1. På **siden Profiler (roller)**  Velg du linjen for profilen du vil kopiere, og deretter Velg handlingen **Kopier profil** .
2. Fyll ut feltene **Profil-ID** og **Visningsnavn**, og Velg deretter OK-knappen **·** .
3. Åpne siden **Profiler (roller)**, åpne det nylig opprettede profilkortet, og rediger deretter andre felt etter behov.

## <a name="edit-a-profile"></a>Redigere en profil

Du kan redigere en profil ved å endre feltene på siden **Profiler (roller)**. Endringene vil imidlertid ikke være synlige for brukeren som har tildelt profilen, før de logges av og igjen.

> [!Caution]
> Ikke gi nytt navn til en profil mens brukere tilordnet profilen er logget på, siden brukere kan oppleve at produktet fryser og må startes på nytt.

## <a name="assign-a-profile-to-a-user"></a>Tilordne en profil til en bruker

Brukere kan tildele seg selv en rolle (som representerer en profil) ved å velge feltet **Rolle** på siden **Mine innstillinger**. Som administrator kan du gjøre det samme på siden **Profiler (roller)**.

1. På **siden Profiler (roller)**  Velg du profilen du vil tilordne, og deretter Velg handlingen **Brukertilpasningsliste** .
2. På siden Brukerinnstillinger **Velg** du brukeren du vil tilordne profilen til, og deretter Velg handlingen **Rediger** .
3. I feltet **Profil-ID** velger du den relevante profilen.

Hvis du tilordner en annen profil til en bruker, beholdes eventuelle tilpasninger som er gjort av brukeren med den forrige profilen.

## <a name="define-user-settings-for-a-profile"></a>Definere brukerinnstillinger for en profil

På siden **Mine innstillinger** kan brukerne definere grunnleggende virkemåte for kontoen, for eksempel Rollesenteret, språket og hvilke meldinger de får. Hvis du vil ha mer informasjon om brukerinnstillinger, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Som administrator kan du definere innstillinger for en profil. Innstillingene gjelder for alle brukerne som er tilordnet rollen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Profiler (roller),** og Velg deretter den relaterte opprette en kobling.
2. Velg linjen for profilen du vil endre brukerinnstillinger for, og Velg deretter handlingen **Brukertilpasningsliste** .
3. Åpne siden **Brukertilpasninger**, åpne kortet for brukeren du vil endre innstillinger for.
4. På siden **Brukertilpasningskort** redigerer du feltene etter behov.

## <a name="activate-a-profile"></a>Aktivere en profil

Når du oppretter en profil, kan du definere om, hvor og hvordan profilen og den tilhørende informasjonen er tilgjengelig for brukerne.

På siden **Profiler (roller)** merker du av for følgende avmerkingsbokser:

* **Aktivert** for å angi om den relaterte rollen er synlig på siden **Tilgjengelige roller**, slik at brukerne kan velge.  
* **Bruk som standardprofil** for å angi profilen som gjelder for brukere som ikke er tildelt en bestemt rolle.
* **Deaktiver tilpasning** for å angi om brukere av den relaterte rollen kan tilpasse arbeidsområdet sitt.
* **Vis i Rolletforsker** for å angi om handlinger til forretningsfunksjoner som er inkludert i profilen, vises i utvidet visning av rolleutforskeren, en funksjonsoversikt. Hvis du vil ha mer informasjon om rolleutforskeren, kan du se [Finn sider med rolleutforskeren](ui-role-explorer.md).

## <a name="export-profiles"></a>Eksportere profiler

Du kan eksportere profiler fra [!INCLUDE[prod_short](includes/prod_short.md)] og bruke dem på nytt i en annen leier. Profilene eksportere til en ZIP-fil som inneholder AL-filene (programspråk). Du kan gjenbruke AL-filene for å utvikle utvidelser. Hvis du vil ha mer informasjon om å eksportere profiler, kan du se [Bruk klienten til å opprette profiler og sidetilpasninger](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* På **siden Profiler (roller)**  Velg handlingen **Eksporter profiler** .

    Denne handlingen eksporterer en zip-fil som inneholder AL-filene for alle profiler.

## <a name="import-profiles"></a>Importer profiler

Du kan importere profiler som er eksportert fra Business Central. Trinnene er mer eller mindre enn de motsatte av trinnene for å eksportere profiler.

1. På **siden Profiler (roller)**  Velg handlingen **Importer profiler** .
1. Følg trinnene i veiviseren **Importere profiler**.

    Hvis du bare vil importere valgte profiler, bruker du avmerkingsboksen **Valgt** til å angi hvilken som skal importeres.
1. Velg den **Importer valgt-knappen** .

    Denne handlingen importerer en zip-fil som inneholder AL-filene for de valgte profilene.

## <a name="delete-a-profile"></a>Slette en profil

Du kan slette en profil ved å velge **Slett**-handlingen på siden **Profiler (roller)**. Følgende begrensninger gjelder imidlertid:

* Du kan ikke slette en profil som er tildelt en bruker eller en brukergruppe.
* Du kan ikke slette profiler som stammer fra utvidelser. Filtypen må først avinstalleres.
* Du kan bare slette én profil om gangen.

## <a name="delete-personalizations"></a>Slette tilpasninger

### <a name="delete-all-personalizations-made-by-a-specific-user"></a>Slett alle tilpasninger som er gjort av en bestemt bruker

Du kan slette alle endringer en bruker gjør på alle sider, noe som tilbakestiller sidene til det opprinnelige oppsettet. Tilpasninger er ikke knyttet til en profil (rolle). Hvis en bruker tilpasser en side, opplever de tilpasningene på siden uansett hvilken rolle de bruker.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Brukerinnstillinger**, og Velg deretter den relaterte opprette en kobling.

    Siden Brukerinnstillinger **viser** alle brukere<!--who make personalizations-->.

2. Velg brukeren du vil slette personlige tilpasninger for.
3. På **siden Brukerinnstillinger**  kort Velg handlingen **Fjern tilpassede sider**, og godta deretter meldingen som vises.

Brukeren ser endringene neste gang de logger på.

Du kan også slette alle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette alle tilpasninger for en profil](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### <a name="delete-personalizations-for-specific-pages"></a>Slette tilpasninger for bestemte sider

Du kan slette tilpasninger som én eller flere brukere gjør på bestemte sider. Sletting av tilpasninger kan være nyttige hvis en forretningsprosessendring betyr at en personalisering ikke lenger kan brukes. Slettinger gjenoppretter sideoppsettet tilbake til det som profilen definerer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Tilpassede sider**, og Velg deretter de relaterte opprette en kobling.

     **Siden Personlige sider** viser alle sidene som er tilpasset, og brukeren de tilhører.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Velg linjen for sidetilpasningen du vil slette, og Velg deretter handlingen **Slett** .

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
