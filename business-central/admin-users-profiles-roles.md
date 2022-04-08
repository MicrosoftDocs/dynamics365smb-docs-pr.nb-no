---
title: Behandle brukere og roller
description: Finn ut hvordan du administrerer brukerprofiler og rollesentre i Business Central. Profiler gjør det mulig for administratorer å definere og håndtere hva brukere kan se og gjøre.
author: SorenGP
ms.topic: conceptual
ms.search.keywords: profiles, users
ms.search.form: 9171
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: b17a4f5a375e4fa1ad067d2679b37bb3d0f5da95
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514150"
---
# <a name="manage-user-profiles"></a>Administrer brukerprofiler

Alle brukere av [!INCLUDE[prod_short](includes/prod_short.md)] får tilordnet en profil som gjenspeiler forretningsrollen sin, avdelingen de arbeider i, eller en annen kategorisering. Profiler gjør det mulig for administratorer å definere og administrere sentralt hva ulike typer brukere kan se og gjøre i brukergrensesnittet, slik at de kan utføre forretningsoppgavene effektivt.

> [!NOTE]
> Den typiske forretningsbruken av en profil er en rolle. En profil er derfor kalt *Profil (rolle)* i grensesnittet.

Som administrator kan du opprette og behandle profiler på siden **Profiler (roller)**. Hver profil har et kort der du håndterer ulike innstillinger for den relaterte rollen, for eksempel rollenavnet, brukerinnstillingene og hvilket rollesenter profilen bruker. Hvis du vil ha mer informasjon om brukerinnstillinger og rollesentre, se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Før du kan administrere brukernes profiler må brukerne opprettes og legges til ved hjelp av Microsoft 365-administrasjonssenteret. Deretter kan du tilordne tillatelser til hver bruker eller brukergruppe for å definere hvilke funksjoner de kan vise og/eller redigere. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sidetilpasning
Du kan tilpasse sideoppsett for en profil, slik at alle brukerne som er tilordnet profilen, ser de tilpassede sidene. Som administrator kan du tilpasse sider ved å bruke samme funksjonalitet som brukere gjør når de tilpasser. Hvis du vil ha mer informasjon, kan du se [Tilpasse sider for profiler](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Slik oppretter du en profil

Hvis du ikke kan kopiere en eksisterende profil, kan du opprette en ny manuelt.

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og skriv inn **Profiler (roller)**, og velg deretter den relaterte koblingen.  
2. På siden **Profiler (roller)** velger du handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du vil at en bestemt profil skal være tilgjengelig bare for svært spesifikke brukere, kan du sette **Beskrivelse**-feltet til `Navigation menu only.`. På denne måten utelates profilen fra listen over tilgjengelige roller i **Mine innstillinger**.

## <a name="to-copy-a-profile"></a>Kopiere en profil
Hvis du vil spare tid, kan du opprette en ny profil ved å kopiere en eksisterende. Kopier en som har lignende innstillinger som den du vil opprette.

> [!NOTE]
> Når du kopierer en profil, kopieres alle de involverte sidetilpassingene i tillegg, både brukeropprettede og de som utledes fra utvidelsene.

1. På siden **Profiler (roller)** merker du linjen for profilen du vil kopiere, og deretter velger du handlingen **Kopier profil**.
2. Fyll ut feltene **Profil-ID** og **Visningsnavn**, og velg deretter **OK**.
3. Åpne siden **Profiler (roller)**, åpne det nylig opprettede profilkortet, og rediger deretter andre felt etter behov.

## <a name="to-edit-a-profile"></a>Redigere en profil
Du kan redigere en profil ved å endre feltene på siden **Profil (rolle)**. Endringene vil imidlertid ikke være synlige for brukeren som har tilordnet profilen, før de logges av og igjen.

> [!Caution]
> Ikke gi nytt navn til en profil mens brukere tilordnet profilen er logget på, siden brukere kan oppleve at produktet fryser og må startes på nytt.

## <a name="to-assign-a-profile-to-a-user"></a>Tilordne en profil til en bruker
Brukere kan tildele seg selv en rolle (som representerer en profil) ved å velge feltet **Rolle** på siden **Mine innstillinger**. Som administrator kan du gjøre det samme på siden **Profiler (roller)**.

1. På siden **Profiler (roller)** merker du profilen du vil tilordne, og deretter velger du handlingen **Brukertilpasningsliste**.
2. På siden **Brukertilpasninger** merker du brukeren du vil tilordne profilen til, og deretter velger du handlingen **Rediger**.
3. I feltet **Profil-ID** velger du den relevante profilen.

> [!NOTE]
> Hvis du tilordner en annen profil til en bruker, beholdes eventuelle tilpasninger som er gjort av brukeren med den forrige profilen.

## <a name="to-define-user-settings-for-a-profile"></a>Definere brukerinnstillinger for en profil
På siden **Mine innstillinger** kan brukerne definere grunnleggende virkemåte for kontoen, for eksempel Rollesenteret, språket og hvilke meldinger de får. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Som administrator kan du definere disse innstillingene for en profil og dermed bruke innstillingene for alle brukerne av den relaterte rollen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Profiler (roller)**, og velg deretter den relaterte koblingen.
2. Velg linje for profilen du vil endre brukerinnstillinger for, og velg deretter handlingen **Brukertilpasningsliste**.
3. Åpne siden **Brukertilpasninger**, åpne kortet for brukeren du vil endre innstillinger for.
4. På siden **Brukertilpasningskort** redigerer du feltene etter behov.

## <a name="to-activate-a-profile"></a>Aktivere en profil
Når du oppretter en profil, kan du velge ulike avmerkingsbokser som definerer om, hvor og hvordan profilen og den tilhørende informasjonen skal gjøres tilgjengelig for brukerne.

* På siden **Profil (rolle)** merker du av for følgende avmerkingsbokser:
    - **Aktivert** for å angi om den relaterte rollen er synlig på siden **Tilgjengelige roller**, slik at brukerne kan velge.  
    - **Bruk som standardprofil** for å angi profilen som gjelder for brukere som ikke er tilordnet en bestemt rolle.
    - **Deaktiver tilpasning** for å angi om brukere av den relaterte rollen kan tilpasse arbeidsområdet sitt.
    - **Vis i Rolletforsker** for å angi om handlinger til forretningsfunksjoner som er inkludert i profilen, vises i utvidet visning av rolleutforskeren, en funksjonsoversikt. Hvis du vil ha mer informasjon, se [Finne sider med rolleutforskeren](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Slik eksporterer du profiler
Du kan eksportere profiler fra [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel for å bruke dem på nytt i en annen leier. Profilene blir eksportert til en ZIP-fil som inneholder AL-filer som kan brukes på nytt til å utvikle utvidelser. Hvis du vil ha mer informasjon, se [Bruk klienten til å opprette profiler og sidetilpasninger](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* På siden **Profiler (roller)** velger du handlingen **Eksporter profiler**.

En ZIP-fil med AL-filene for alle profiler blir eksportert.

## <a name="to-import-profiles"></a>Slik importerer du profiler
Du kan importere profiler som er eksportert fra [!INCLUDE[prod_short](includes/prod_short.md)]. Trinnene er mer eller mindre enn de motsatte av trinnene for å eksportere profiler. Hvis du vil ha mer informasjon, kan du se [Slik eksporterer du profiler](admin-users-profiles-roles.md#to-export-profiles).

1. På siden **Profiler (roller)** velger du handlingen **Importer profiler**.
2. Følg trinnene i veiviseren **Importere profiler**.

    Hvis du bare vil importere valgte profiler, bruker du avmerkingsboksen **Valgt** til å angi hvilken som skal importeres.
3. Velg knappen **Importer valgt**.

En ZIP-fil med AL-filer for de valgte profilene blir importert.

## <a name="to-delete-a-profile"></a>Slette en profil
Du kan slette en profil ved å velge **Slett**-handlingen på siden **Profiler (roller)**. Følgende begrensninger gjelder imidlertid:

- Du kan ikke slette en profil som er tilordnet en bruker eller en brukergruppe.
- Du kan ikke slette profiler som stammer fra utvidelser. Filtypen må først avinstalleres.
- Du kan bare slette én profil om gangen.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Slette alle tilpasninger som er gjort av brukeren
Du kan slette alle endringene en bruker har gjort på sidene som utgjør arbeidsområdet. Dette kan være nyttig hvis for eksempel en ansatt har endret rolle og ikke lenger trenger tilpasningene. Når du sletter brukernes tilpasninger, endres sideoppsettet tilbake til det som defineres av profilen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukertilpasninger**, og velg deretter den relaterte koblingen.

    Siden **Brukertilpasninger** viser alle brukere som har utført tilpasninger.

2. Åpne kortet for en bruker som har tilpasningene du vil slette.
3. Velg siden **Brukertilpasningskort**, velg handlingen **Fjern tilpassede sider**, og godta deretter meldingen som vises.

Brukeren vil se endringene neste gang vedkommende logger på.

Du kan også slette alle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette alle tilpasninger for en profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Slette tilpasninger for bestemte sider
Du kan slette tilpasninger som én eller flere brukere har gjort på bestemte sider som utgjør arbeidsområdet. Dette kan for eksempel være nyttig hvis en endret forretningsprosess betyr at en personalisering ikke lenger kan brukes av brukere. Når du sletter brukernes tilpasninger, endres sideoppsettet tilbake til det som defineres av profilen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukersidetilpasninger**, og velg deretter den relaterte koblingen.

    Siden **Brukersidetilpasninger** viser alle sidene som er tilpasset, og brukeren de tilhører.

    > [!Note]
    > Hvis det er merket av for **Gammel tilpassing**-feltet, angir dette at tilpassingen ble utført i en eldre versjon av [!INCLUDE[prod_short](includes/prod_short.md)], som håndterte tilpassing annerledes. Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpasning](ui-personalization-locked.md).

2. Velg linjen for sidetilpassingen du vil slette, og velg deretter handlingen **Slett**.

Brukeren vil se endringene neste gang vedkommende logger på.  

Du kan også slette individuelle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette tilpasninger for en bestemt side for en profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Behandle brukerøkter

Du kan som administrator for [!INCLUDE[prod_short](includes/prod_short.md)] online behandle brukerøkter i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Behandle økter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions) i administrasjonsinnholdet.  

For lokal [!INCLUDE[prod_short](includes/prod_short.md)] kan du for eksempel behandle økter som bruker SQL Server Management Studio. Hvis du vil ha mer informasjon, kan du se [teknisk dokumentasjon for SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Se også  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Tilpasse sider for profiler](ui-personalization-manage.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]