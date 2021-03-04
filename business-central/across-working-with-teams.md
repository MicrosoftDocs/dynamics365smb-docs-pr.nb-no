---
title: Arbeide med Business Central-data i Microsoft Teams | Microsoft Docs
description: Lær hvordan du bruker Business Central-appen for Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 0f7c1e8016a1bc1915d7d6a54a183aa0e8cea2ea
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046457"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbeide med Business Central Data i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] tilbyr en app som kobler Microsoft Teams til forretningsdataene dine i [!INCLUDE [prod_short](includes/prod_short.md)], slik at du raskt kan dele detaljer mellom gruppemedlemmer og svare raskere på forespørsler. I denne artikkelen lærer du hvordan du bruker appen til å dele [!INCLUDE [prod_short](includes/prod_short.md)]-data med kolleger i en Teams-samtale.

## <a name="overview"></a>Oversikt

[!INCLUDE [prod_short](includes/prod_short.md)]-appen lar deg:

- Kopier en kobling til en Business Central-oppføring, og lim den inn i en Teams-samtale for å dele med kollegene dine. Appen utvider deretter koblingen til et kompakt, interaktivt kort som viser informasjon om posten.
- Når du er i samtalen, kan du og kollegaene dine vise flere detaljer om posten, redigere data og utføre handlinger uten å forlate Teams.

[![Teams-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Forutsetninger

- Du har tilgang til Microsoft Teams.
- Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alle deltakere i en Teams-samtale kan vise kort for Business Central-oppføringer som du sender til samtalen. Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Ta med et Business Central-kort i en Teams-samtale

1. Logg på [!INCLUDE [prod_short](includes/prod_short.md)] ved å bruke leseren.
2. Åpne posten du vil dele.

    Appen er utformet for å vise korttypesider fra [!INCLUDE [prod_short](includes/prod_short.md)]. Så åpne en side som viser én enkelt post, for eksempel en vare, kunde eller ordre. Du kan ikke bruke den til rollesentre eller sider som viser flere poster i en liste.

3. Kopier hele URL-adressen fra adresselinjen i nettleseren.

   ![Kopier URL-adressen for Business Central fra leseren](media/teams-url-v2.png)
4. Gå til Teams og start en samtale, som kan være en chat med en person, gruppe med personer eller en teamkanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Lim inn URL-adressen i meldingsboksen der du skriver en melding.

   ![Lim inn URL-adresse for Business Central i Teams](media/teams-paste-url-v2.png)
6. Første gang du limer inn en kobling i en samtale, blir du bedt om å logge på [!INCLUDE [prod_short](includes/prod_short.md)] og gi samtykke til at appen kan hente data. Bare følg instruksjonene på skjermen.

    > [!NOTE]
    > Du trenger bare å utføre dette trinnet én gang.

7. Vent et øyeblikk mens et kort genereres i meldingsboksen.

8. Når kortet vises, kan du se nøye gjennom innholdet på kortet for eventuell sensitiv informasjon før du sender meldingen. Dette trinnet er viktig fordi når du sender meldingen, kan alle i samtalen se kortet.

9. Hvis kortet ser bra ut, velger du **Send** for å sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du velger **Send**, kan du slette den innlimte URL-adressen hvis du vil det.

10. Hvis du vil vise flere detaljer eller gjøre endringer i posten som vises på kortet, velger du **Detaljer**. Hvis du vil ha mer informasjon, kan du se neste avsnitt.

## <a name="view-card-details"></a>Vis kortdetaljer

Når et kort er sendt til en samtale, kan alle deltakerne med de [riktige tillatelsene](admin-teams-integration.md#permissions) velge **Detaljer** for å åpne et vindu som viser mer informasjon om posten, og eventuelt gjøre endringer i posten. Det spiller ingen rolle om du er den som sender kortet, eller den som mottar kortet. **Detaljer**-funksjonen er spesielt nyttig for mottakere fordi den raskt gir dem konsis, målrettet informasjon om posten, i motsetning til å måtte skanne hele posten.

Detaljvinduet ligner på det du ser i [!INCLUDE [prod_short](includes/prod_short.md)]-posten. Men den er noe trimmet for Teams. Når du er ferdig med å vise og gjøre endringer, lukker du vinduet for å gå tilbake til Teams-samtalen.

Her er noen ting du må huske på når du arbeider med kortdetaljene:

- For å vise kortdetaljene må brukere ha tillatelse på siden og tilhørende data i [!INCLUDE [prod_short](includes/prod_short.md)].
- Kort i Teams-chatter oppdateres ikke automatisk til endringer. Eventuelle endringer du lagrer i en post i detaljvinduet, lagres i [!INCLUDE [prod_short](includes/prod_short.md)]. Kortet i Teams viser derfor ikke endringene i konverteringen før du limer inn koblingen på nytt.

Hvis du vil vite mer om hvordan du arbeider med kort og kortdetaljer, kan du se [Vanlige spørsmål om Teams](teams-faq.md).

## <a name="see-also"></a>Se også

[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]