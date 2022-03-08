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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989427"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Arbeide med Business Central Data i Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] tilbyr en app som kobler Microsoft Teams til forretningsdataene dine i [!INCLUDE [prodshort](includes/prodshort.md)], slik at du raskt kan dele detaljer mellom gruppemedlemmer og svare raskere på forespørsler. I denne artikkelen lærer du hvordan du bruker appen til å dele [!INCLUDE [prodshort](includes/prodshort.md)]-data med kolleger i en Teams-samtale.

## <a name="overview"></a>Oversikt

[!INCLUDE [prodshort](includes/prodshort.md)]-appen lar deg:

- Kopier en kobling til en Business Central-oppføring, og lim den inn i en Teams-samtale for å dele med kollegene dine. Koblingen vil utvide det til et kompakt, interaktivt kort som viser informasjon om posten.
- Når du er i samtalen, kan du og kollegaene dine vise flere detaljer om posten, redigere data og utføre handlinger uten å forlate Teams.

[![Teams-integrering med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Forutsetninger

- Du har tilgang til Microsoft Teams.
- Du har installert [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Teams. Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alle deltakere i en Teams-samtale kan vise kort for Business Central-oppføringer som du sender til samtalen. Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prodshort](includes/prodshort.md)]. Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Ta med et Business Central-kort i en Teams-samtale

1. Logg på [!INCLUDE [prodshort](includes/prodshort.md)] ved å bruke leseren.
2. Åpne posten du vil dele.

    Appen er utformet for å vise korttypesider fra [!INCLUDE [prodshort](includes/prodshort.md)]. Så åpne en side som viser én enkelt post, for eksempel en vare, kunde eller ordre. Du kan ikke bruke den til rollesentre eller sider som viser flere poster i en liste.

3. Kopier hele URL-adressen fra adresselinjen i nettleseren.

   ![Kopier URL-adressen for Business Central fra leseren](media/teams-url.png)
4. Gå til Teams og start en samtale, som kan være en chat med en person, gruppe med personer eller en teamkanal.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Lim inn URL-adressen i boksen der du legger til en melding.

   ![Lim inn URL-adresse for Business Central i Teams](media/teams-paste-url.png)
6. Første gang du limer inn en kobling i en samtale, blir du bedt om å logge på [!INCLUDE [prodshort](includes/prodshort.md)] og gi samtykke til at appen kan hente data. Bare følg instruksjonene på skjermen.

    > [!NOTE]
    > Du trenger bare å utføre dette trinnet én gang.

7. Vent et øyeblikk mens et kort genereres i meldingsboksen.

8. Når kortet vises, kan du se nøye gjennom innholdet på kortet for eventuell sensitiv informasjon før du sender meldingen. Dette trinnet er viktig fordi når du sender meldingen, kan alle i samtalen se kortet.

9. Hvis kortet ser bra ut, velger du **Send** for å sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du velger **Send**, kan du slette den innlimte URL-adressen hvis du vil det.

10. Hvis du vil vise flere detaljer eller gjøre endringer i posten, velger du **Detaljer**.

    Detaljsiden ligner på det du ser i [!INCLUDE [prodshort](includes/prodshort.md)]. Men den er noe trimmet for Teams. Når du er ferdig med å vise og gjøre endringer, lukker du vinduet for å gå tilbake til Teams-samtalen.

    > [!NOTE]
    > Eventuelle endringer du foretar, gjenspeiles ikke i kortet før neste gang du limer inn koblingen i en samtale.

## <a name="see-also"></a>Se også

[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Komme i gang](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
