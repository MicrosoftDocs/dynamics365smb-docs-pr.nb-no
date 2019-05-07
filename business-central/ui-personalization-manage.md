---
title: Administrere tilpasnings om administrator i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du kan tilpasse brukergrensesnittet slik at det passer til din arbeidsmåte.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "910865"
---
# <a name="managing-personalization-as-an-administrator"></a>Administrere tilpasning som Administrator

 Brukere kan tilpasse arbeidsområdet etter egne behov. Som en administrator kan du kontrollere og håndtere tilpasning av:

-   Aktivering eller deaktivering av funksjonen for tilpasning for hele programmet (bare lokal installasjon).
-   Aktivering eller deaktivering av funksjonen for tilpasning for brukere av en bestemt profil.
-   Fjerning av sidetilpasninger som brukere har opprettet.

## <a name="EnablePersonalization"></a>Aktivere eller deaktivere tilpasning (bare lokalt)

Som standard er tilpasning ikke aktivert i klienten. Du aktiverer eller deaktiverer tilpasning ved å endre konfigurasjonsfilen (navsettings.json) for webserverforekomsten av Business Central som betjener klientene.

1. Legg til følgende linje i filen navsettings.json for å aktivere tilpasning:

    ```
    "PersonalizationEnabled": "true"
    ```

    Hvis du vil deaktivere tilpasning, fjerner du linjen eller endrer den til:

    ```
    "PersonalizationEnabled": "false"
    ```

    Du finner mer informasjon om hvordan du kan endre filen navsettings.json, i [Endre filen navsettings.json direkte](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Generere og laste ned programsymbolene.

    Dette trinnet er valgfritt og kreves ikke for å aktivere tilpasning. Det sikrer imidlertid at nye sider som er opprettet av utviklere, kan tilpasses.

    1. Først må du generere symbolene ved å kjøre finsql.exe med `generatesymbolreference`-kommandoen. Filen finsql.exe finnes i installasjonsmappen for [!INCLUDE[server](includes/server.md)] og Dynamics NAV Development Environment (CSIDE). For å generere symbolene åpne en ledetekst, endre katalogen der filen er lagret, og kjør følgende kommando:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Eksempel:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Hvis du vil ha mer informasjon, se [Kjøre C/SIDE og AL side ved side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Konfigurere [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-forekomst til **Aktivere lasting av programsymbolreferanser ved serveroppstart** (EnableSymbolLoadingAtServerStartup). Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Deaktivere tilpasning for en profil

Du kan hindre alle brukere som tilhører en bestemt profil, fra å tilpasse sine sider.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Profiler**, og velg deretter den relaterte koblingen.
2. Velg profilen i listen som du vil endre.
3. Merk av for **Deaktiver tilpasning**, og velg deretter **OK**.

## <a name="to-clear-user-personalizations"></a>Fjerne brukertilpasninger

Hvis du fjerner sidetilpasninger, endres siden tilbake til det opprinnelige oppsettet før eventuelle tilpasninger ble utført. Du kan slette tilpasninger brukere har gjort med sider, på to måter: ved hjelp av siden **Slett brukertilpasning** og ved hjelp av siden **Brukertilpasningskort**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Slette brukertilpasninger ved hjelp av siden Slett brukertilpasning

Siden **Slett brukertilpasning** lar deg slette tilpasninger for hver enkelt side og bruker.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett brukertilpasning**, og velg deretter den relaterte koblingen.

    Siden viser alle sidene som er tilpasset, og brukerne de tilhører.

    >[!NOTE]
    > Hvis det er merket av for **Gammel tilpassing**-kolonnene, angir dett at tilpassingen ble utført i en eldre versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterte tilpassing annerledes enn nå. Brukere som prøver å tilpasse disse sidene, er låst fra å gjøre dette med mindre de ønsker å låse opp siden. Hvis du vil ha mer informasjon, kan du se [Hvorfor en side er låst fra tilpassing](ui-personalization-locked.md).

2. Velg posten du vil slette, og velg deretter handlingen **Slett**.

    Brukeren vil se endringene neste gang vedkommende logger på.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Slette brukertilpasninger ved hjelp av siden Brukertilpasningskort

Siden **Brukertilpasningskort** gir deg muligheten til å slette tilpasningen på alle sider for en bestemt bruker. Dette krever skrivetilgang til tabellen 2000000072 **profil**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukertilpasning**, og velg deretter den relaterte koblingen.

    Siden **Brukertilpasning** viser alle brukerne som kan ha tilpassede sider. Hvis du ikke finner en bruker i listen, betyr det at de ikke har tilpassede sider.

2. Velg brukeren fra listen, og velg deretter handlingen **Rediger**.

3. I kategorien **Handlinger** velger du **Fjern tilpassede sider**.

    Brukeren vil se endringene neste gang vedkommende logger på.

## <a name="see-also"></a>Se også
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
