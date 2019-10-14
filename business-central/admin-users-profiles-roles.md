---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: Finn ut hvordan du administrerer brukere og rollesentre i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 00a07acfb455b9b1ddf714f7ca7e49a56a8aebbc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304242"
---
# <a name="manage-profiles"></a>Administrere profiler
Alle brukere av [!INCLUDE[d365fin](includes/d365fin_md.md)] får tilordnet en profil som gjenspeiler forretningsrollen sin, avdelingen de arbeider i, eller en annen kategorisering. Profiler gjør det mulig for administratorer å definere og administrere sentralt hva ulike typer brukere kan se og gjøre i brukergrensesnittet, slik at de kan utføre forretningsoppgavene effektivt.

> [!NOTE]
> Den typiske forretningsbruken av en profil er en rolle. En profil er derfor kalt *Profil (rolle)* i grensesnittet.

Som administrator kan du opprette og behandle profiler på siden **Profiler (roller)**. Hver profil har et kort der du håndterer ulike innstillinger for den relaterte rollen, for eksempel rollenavnet, brukerinnstillingene og hvilket rollesenter profilen bruker. Hvis du vil ha mer informasjon om brukerinnstillinger og rollesentre, se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

Før du kan administrere brukernes profiler må brukerne opprettes og legges til ved hjelp av Office 365-administrasjonssenteret. Deretter kan du tilordne tillatelser til hver bruker eller brukergruppe for å definere hvilke funksjoner de kan vise og/eller redigere. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).

## <a name="page-customization"></a>Sidetilpasning
Du kan tilpasse sideoppsett for en profil, slik at alle brukerne som er tilordnet profilen, ser de tilpassede sidene. Som administrator kan du tilpasse sider ved å bruke samme funksjonalitet som brukere gjør når de tilpasser. Hvis du vil ha mer informasjon, kan du se [Tilpasse sider for profiler](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Slik oppretter du en profil
Hvis du ikke kan kopiere en eksisterende profil, kan du opprette en ny manuelt.

> [!NOTE]
> Alle profiler kan kopieres, men profilsidetilpasningene kan bare kopieres hvis de er opprettet av brukeren.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Profiler (roller)**, og velg deretter den relaterte koblingen.  
2. På siden **Profiler (roller)** velger du handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Kopiere en profil
Hvis du vil spare tid, kan du opprette en ny profil ved å kopiere en eksisterende. Kopier en som har lignende innstillinger som den du vil opprette.

1. På siden **Profiler (roller)** merker du linjen for profilen du vil kopiere, og deretter velger du handlingen **Kopier profil**.
2. Fyll ut feltene **Profil-ID** og **Visningsnavn**, og velg deretter **OK**.
3. Åpne siden **Profiler (roller)**, åpne det nylig opprettede profilkortet, og rediger deretter andre felt etter behov.

## <a name="to-edit-a-profile"></a>Redigere en profil
Du kan redigere en profil ved å endre feltene på siden **Profil (rolle)**.

> [!NOTE]
> Du kan ikke redigere en profil når brukerne som er tilordnet profilen, er pålogget.

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

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profiler (rolle)**, og velg deretter den relaterte koblingen.
2. Velg linje for profilen du vil endre brukerinnstillinger for, velg **Naviger**-handlingen, og velg deretter handlingen **Brukertilpasninger**.
3. Åpne siden **Brukertilpasninger**, åpne kortet for brukeren du vil endre innstillinger for.
4. På siden **Brukertilpasningskort** redigerer du feltene etter behov.

## <a name="to-activate-a-profile"></a>Aktivere en profil
Når du oppretter en profil, kan du velge ulike avmerkingsbokser som definerer om, hvor og hvordan profilen og den tilhørende informasjonen skal gjøres tilgjengelig for brukerne.

1. På siden **Profil (rolle)** merker du av for følgende avmerkingsbokser:
    - **Aktivert** for å angi om den relaterte rollen er synlig på siden **Tilgjengelige roller**, slik at brukerne kan velge.  
    - **Bruk som standardprofil** for å angi profilen som gjelder for brukere som ikke er tilordnet en bestemt rolle.
    - **Deaktiver tilpasning** for å angi om brukere av den relaterte rollen kan tilpasse arbeidsområdet sitt.
    - **Vis i Rolleutforsker** for å angi om menyelementer for forretningsfunksjoner som inngår i profilen, skal vises i funksjonsoversikten. Se [Finne sider fra en funksjonoversikt](ui-role-explorer.md) hvis du vil ha mer informasjon.

    ## <a name="to-export-user-created-profiles"></a>Eksportere brukeropprettede profiler
    Du kan eksportere profiler som er endret enten av deg eller av brukere, som angitt av **(Brukeropprettet)** i **Kilde**-feltet. Profilen eksporteres til en zip-fil som inneholder Al-filer som kan brukes på nytt til å utvikle utvidelser. Hvis du vil ha mer informasjon, se [Bruke klienten til å opprette profiler og sidetilpasninger](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

    * På siden **Profiler (roller)** velger du **Eksporter brukeropprettede profiler**.

    En zip-fil med Al-filene for profiler som nylig ble lagt til eller endret, eksporteres.

## <a name="to-delete-a-profile"></a>Slette en profil
Du kan slette en profil ved å velge **Slett**-handlingen på siden **Profiler (roller)**. Følgende begrensninger gjelder imidlertid:

- Du kan ikke slette profiler som stammer fra utvidelser. Filtypen må først avinstalleres.
- Profilen må være deaktivert. Dette sikrer også at ingen brukere som er tilordnet profilen, logges på når du sletter.
- Du kan bare slette én profil om gangen.  

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Slette alle tilpasninger som er gjort av brukeren
Du kan slette alle endringene en bruker har gjort på sidene som utgjør arbeidsområdet. Dette kan være nyttig hvis for eksempel en ansatt har endret rolle og ikke lenger trenger tilpasningene. Når du sletter brukernes tilpasninger, endres sideoppsettet tilbake til det som defineres av profilen.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukertilpasninger**, og velg deretter den relaterte koblingen.

    Siden **Brukertilpasninger** viser alle brukere som har utført tilpasninger.

2. Åpne kortet for en bruker som har tilpasningene du vil slette.
3. Velg siden **Brukertilpasningskort**, velg handlingen **Fjern tilpassede sider**, og godta deretter meldingen som vises.

Brukeren vil se endringene neste gang vedkommende logger på.

Du kan også slette alle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette alle tilpasninger for en profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Slette tilpasninger for bestemte sider
Du kan slette tilpasninger som én eller flere brukere har gjort på bestemte sider som utgjør arbeidsområdet. Dette kan for eksempel være nyttig hvis en endret forretningsprosess betyr at en personalisering ikke lenger kan brukes av brukere. Når du sletter brukernes tilpasninger, endres sideoppsettet tilbake til det som defineres av profilen.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukersidetilpasninger**, og velg deretter den relaterte koblingen.

    Siden **Brukersidetilpasninger** viser alle sidene som er tilpasset, og brukeren de tilhører.

    > [!Note]
    > Hvis det er merket av for **Gammel tilpassing**-feltet, angir dette at tilpassingen ble utført i en eldre versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterte tilpassing annerledes. Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpasning](ui-personalization-locked.md).

2. Velg linjen for sidetilpassingen du vil slette, og velg deretter handlingen **Slett**.

Brukeren vil se endringene neste gang vedkommende logger på.    

Du kan også slette individuelle sidetilpasninger for en profil. Hvis du vil ha mer informasjon, se [Slette tilpasninger for en bestemt side for en profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Se også  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)  
[Tilpasse sider for profiler](ui-personalization-manage.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
