---
title: Tilpasse sider for roller | Microsoft Docs
description: Lær hvordan du tilpasser brukergrensesnittet for en profil (rolle), slik at alle brukere som har tilordnet rollen, ser et tilpasset arbeidsområde.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 470d2542864b8d0e0f16f89fd99e422807829404
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310807"
---
# <a name="customize-pages-for-profiles"></a>Tilpasse sider for profiler
Brukere kan tilpasse sider som utgjør arbeidsområdet, slik at de passer til deres egne behov. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

Administratorer kan tilpasse sider for en profil, for eksempel i henhold til den tilknyttede forretningsrollen eller avdelingen, slik at alle brukerne som er tilordnet profilen, får se det tilpassede sideoppsettet. Administratoren kan tilpasse sider ved å bruke samme funksjonalitet som brukere gjør når de tilpasser sider.

> [!NOTE]
> Den typiske forretningsbruken av en profil er en rolle. En profil er derfor kalt *Profil (rolle)* i grensesnittet.

Sidetilpassing starter fra siden **Profiler (roller)**, administratorens startpunkt for administrering av brukerprofiler på individuelle profilkort. I tillegg til å tilpasse sideoppsettet styrer du ulike innstillinger for profiler på siden **Profil (rolle)** for hver profil. Hvis du vil ha mer informasjon, kan du se [Administrere profiler](admin-users-profiles-roles.md).

## <a name="to-customize-pages-for-a-profile"></a>Tilpasse sider for en profil
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profiler (rolle)**, og velg deretter den relaterte koblingen.
2. Velg linjen for profilen du vil tilpasse sidene for, og velg deretter handlingen **Slett**.
3. Velg handlingen **Tilpass sider**.

    [!INCLUDE[d365fin](includes/d365fin_md.md)] åpnes i en ny leserkategori for den valgte profilen med banneret **Tilpasse** aktivert. Banneret **Tilpasning** tilbyr samme funksjonalitet som banneret **Tilpasning** som brukerne kan bruke.

4. Tilpass sider i henhold til behovene for gjeldende rolle eller avdeling, på samme måte som en bruker gjør ved tilpasning. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

    > [!NOTE]
    > Hvis du vil navigere under tilpasning, trykker du CTRL+klikk på en handling hvis den utheves av pilhodet.

5. Når du er ferdig med å endre oppsettet på én eller flere sider, velger du **Fullført**-knappen på banneret **Tilpasning**.
6. Lukk webleserkategorien.

Tilpassing av sider er nå registrert for profilen.

## <a name="to-view-all-customized-pages-for-a-profile"></a>Vise alle tilpassede sider for en profil
Du kan få en oversikt over hvilke sider som er tilpasset for en profil, for eksempel for å planlegge hvilke som skal tilpasses ytterligere eller slettes.

- På siden **Profil (rolle)** velger du handlingen **Tilpassede sider**.

## <a name="to-delete-all-customizations-for-a-profile"></a>Slette alle tilpasninger for en profil
Du kan avbryte alle tilpasninger du har gjort for en profil. Tilpasninger som er innført med en utvidelse, og personlige tilpasninger gjort av en bruker, slettes ikke. Du kan slette alle personlige tilpasninger med en annen handling. Hvis du vil ha mer informasjon, kan du se [Slette alle tilpasninger som er gjort av en bruker](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- På siden **Profil (rolle)** for en tilpasset profil velger du handlingen **Fjern tilpassede sider**.

Oppsettet på sider for profilen tilbakestilles til standardoppsettet.  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a>Slette tilpasninger for bestemte sider for en profil
Du kan slette individuelle sidetilpasninger som du har gjort for en profil. Tilpasninger som er innført med en utvidelse, og personlige tilpasninger gjort av en bruker, slettes ikke. Du kan slette spesifikke sidetilpasninger med en annen handling. Hvis du vil ha mer informasjon, se [Slette personlige tilpasninger for en bestemt side](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. På siden **Profil (rolle)** velger du handlingen **Tilpassede sider**.
2. På siden **Profiltilpasninger** velger du én eller flere linjer for sidetilpasninger du vil slette, og deretter velger du handlingen **Slett**.

Oppsettet på de valgte sidene justeres til endringene du har gjort.

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
