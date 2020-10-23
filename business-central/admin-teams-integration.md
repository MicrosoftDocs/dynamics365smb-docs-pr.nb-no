---
title: Administrere Microsoft Teams-integrering med Business Central | Microsoft Docs
description: Administrer Business Central-integrering med Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989361"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Administrere Microsoft Teams-integrering med Business Central

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Denne artikkelen gir en oversikt over hva du kan gjøre som administrator for å styre Microsoft Teams-integrasjon med [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minstekrav

Denne delen beskriver minimumskravene for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunksjonene skal fungere i Teams.

- Nødvendige lisenser

    Denne tabellen gir deg en oversikt over nødvendige lisenser for at [!INCLUDE [prodshort](includes/prodshort.md)]-appfunksjonene skal fungere i Teams.

    |Hva|Teams-lisens|Business Central-lisens|
    |----|---|---|
    |Lim inn en kobling til en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale, og send den som et kort.|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|
    |Vis et kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.|![avmerking](media/check.png "avmerking")||
    |Vis flere detaljer i kort for en [!INCLUDE [prodshort](includes/prodshort.md)]-post i en samtale.|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|

- Tillat URL-forhåndsvisninger

    Policyinnstillingen **Tillat URL-forhåndsvisninger** må være aktivert. Ellers kan ikke et kort genereres for Business Central-koblinger som limes inn i en Teams-samtale. Hvis du vil ha mer informasjon om denne innstillingen, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>Administrere Business Central-appen (valgfritt)

Som Teams-administrator kan du behandle alle apper for organisasjonen, inkludert [!INCLUDE [prodshort](includes/prodshort.md)]-appen. Du kan godkjenne eller installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for organisasjonen, hindre at brukere installerer appen, med mer.

Hvis du vil ha mer informasjon, kan du se følgende artikler i Microsoft Teams-dokumentasjonen:

- [Behandle appene i Microsoft Teams-administrasjonssenteret](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Administrere policyer for appoppsett i Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>I [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Minstekrav

- [!INCLUDE [prodshort](includes/prodshort.md)] versjon:

    [!INCLUDE [prodshort](includes/prodshort.md)] 2020 lanseringsbølge 2 (versjon 17) eller nyere. Teams-integrasjon støttes bare for [!INCLUDE [prodshort](includes/prodshort.md)] online, ikke lokalt.

- Codeunit **2718 Page Summary Provider** publiseres som en webtjeneste:

    Denne codeunit publiseres som en webtjeneste som standard. Codeunit-en er en del av [!INCLUDE [prodshort](includes/prodshort.md)]-systemapplikasjonen. Den brukes til å hente feltdataene for en [!INCLUDE [prodshort](includes/prodshort.md)]-side som legges til i en Teams-samtale. 

- Brukertillatelser:

    For det meste kontrolleres sidene og dataene som brukere kan vise og redigere i en Teams-samtale, av tillatelsene deres i [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - For å lime inn en [!INCLUDE [prodshort](includes/prodshort.md)]-kobling i en Teams-samtale og la den utvides til et kort, må brukerne minst ha lesetillatelse på siden og tilhørende data.
    - Når et kort er sendt til en samtale, kan alle brukere i denne samtalen vise kortet uten tillatelse til Business Central.
    - For å vise flere detaljer for et kort eller åpne posten i [!INCLUDE [prodshort](includes/prodshort.md)], må brukere ha lesetillatelse på siden og tilhørende data.
    - For å endre data må brukere ha endringstillatelse.
    
    Hvis du vil ha informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

## <a name="see-also"></a>Se også
[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Komme i gang](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
