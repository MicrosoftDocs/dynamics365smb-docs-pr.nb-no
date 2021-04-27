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
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: ecb3f88bf14c74f026f10fd49efe28f189036589
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882208"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Administrere Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikkelen gir en oversikt over hva du kan gjøre som administrator for å styre Microsoft Teams-integrasjon med [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minstekrav

Denne delen beskriver minimumskravene for at [!INCLUDE [prod_short](includes/prod_short.md)]-appfunksjonene skal fungere i Teams.

- Nødvendige lisenser

    Denne tabellen gir deg en oversikt over nødvendige lisenser for at [!INCLUDE [prod_short](includes/prod_short.md)]-appfunksjonene skal fungere i Teams.

    |Hva|Teams-lisens|[!INCLUDE [prod_short](includes/prod_short.md)]-lisens|
    |----|---|---|
    |Søk etter [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter.|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|
    |Lim inn en kobling til en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale, og send den som et kort.|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|
    |Vis et kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![avmerking](media/check.png "avmerking")||
    |Vis flere detaljer i kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![avmerking](media/check.png "avmerking")|![avmerking](media/check.png "avmerking")|

- Tillat URL-forhåndsvisninger

    Policyinnstillingen **Tillat URL-forhåndsvisninger** må være aktivert. Ellers kan ikke et kort genereres for [!INCLUDE [prod_short](includes/prod_short.md)]-koblinger som limes inn i en Teams-samtale. Hvis du vil ha mer informasjon om denne innstillingen, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>Administrere [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valgfritt)

Som Teams-administrator kan du behandle alle apper for organisasjonen, inkludert [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkjenne eller installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for organisasjonen, hindre at brukere installerer appen, med mer.

Hvis du vil ha mer informasjon, kan du se følgende artikler i Microsoft Teams-dokumentasjonen:

- [Behandle appene i administrasjonssenteret i Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Administrere policyer for appoppsett i Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>I [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Minstekrav

- [!INCLUDE [prod_short](includes/prod_short.md)] versjon:

    Lanseringsbølge 1 eller nyere for [!INCLUDE [prod_short](includes/prod_short.md)] 2021. Teams-integrasjon støttes bare for [!INCLUDE [prod_short](includes/prod_short.md)] online, ikke lokalt.

- Codeunit **2718 Page Summary Provider** publiseres som en webtjeneste:

    Denne codeunit publiseres som en webtjeneste som standard. Codeunit-en er en del av [!INCLUDE [prod_short](includes/prod_short.md)]-systemapplikasjonen. Den brukes til å hente feltdataene for en [!INCLUDE [prod_short](includes/prod_short.md)]-side som legges til i en Teams-samtale. Hvis du vil ha informasjon om publisering av nettjenester, kan du se [Publiser en nettjeneste](across-how-publish-web-service.md).

- <a name="permissions"></a>Brukertillatelser:

    For det meste kontrolleres kontaktene, søkene, sidene og dataene som brukere kan vise og redigere i en Teams-samtale, av tillatelsene deres i [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - For å kunne søke etter kontakter, må brukerne minst ha lesetilgang til tabellen **Kontakter**. 
    - For å lime inn en [!INCLUDE [prod_short](includes/prod_short.md)]-kobling i en Teams-samtale og la den utvides til et kort, må brukerne minst ha lesetillatelse på siden og tilhørende data.
    - Når et kort er sendt til en samtale, kan alle brukere i denne samtalen vise kortet uten tillatelse til [!INCLUDE [prod_short](includes/prod_short.md)].
    - For å vise flere detaljer for et kort eller åpne posten i [!INCLUDE [prod_short](includes/prod_short.md)], må brukere ha lesetillatelse på siden og tilhørende data.
    - For å endre data må brukere ha endringstillatelse.
    
    Hvis du vil ha informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

## <a name="managing-privacy-and-compliance"></a>Administrere personvern og samsvar 

Microsoft Teams gir omfattende kontroller for samsvar og håndtering av sensitive eller personlige data, inkludert data som er lagt til i chatter og kanaler av [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Forstå hvor [!INCLUDE [prod_short](includes/prod_short.md)]-kort lagres 

Når et kort er sendt til en chat, blir kortet og feltene som vises på kortet, kopiert til Teams. Denne informasjonen er underlagt Teams-policyene for organisasjonen, for eksempel policyer for dataoppbevaring. Når du viser kortopplysninger, lagres ingen av dataene i detaljvinduet i Teams. Dataene forblir lagret i [!INCLUDE [prod_short](includes/prod_short.md)] og hentes bare av Teams når brukeren velger å vise detaljene. 

- Hvis du vil vite mer om hvor Teams lagrer disse dataene, kan du se [Plasseringen av dataene i Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Hvis du vil finne ut mer om oppbevaringspolicyer i Teams, kan du se [Oppbevaringspolicyer i Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Begrense deling av kort 

Du hindrer at bestemte brukere eller grupper sender kort til chatter eller kanaler ved å definere meldingspolicyer som deaktiverer innstillingen **URL-forhåndsvisning**. Hvis du vil ha mer informasjon om denne innstillingen, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams). 

Du kan også bruke informasjonshindringer for å hindre at enkelt personer eller grupper kommuniserer med hverandre. Hvis du vil finne ut mer, kan du se [informasjonshindringer i Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Funksjonene for hindring av tap av data i Microsoft 365 Security & Compliance Center kan ikke brukes spesifikt på kort. Men de kan brukes på chatmeldingene som inneholder kortene. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### <a name="responding-to-data-requests"></a>Svare på dataforespørsler

Du tillater at teammedlemmer og teameiere sletter meldinger som inneholder sensitive kort ved å definere meldingspolicyer, for eksempel **Eiere kan slette sendte meldinger** og **Brukere kan slette sendte meldinger**. Hvis du vil ha mer informasjon, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

Funksjonene for innholdssøk og eDiscovery-samsvar i Microsoft 365 Security & Compliance Center kan også brukes for kort.

Ettersom kortdata i Teams er en kopi av data i [!INCLUDE [prod_short](includes/prod_short.md)], kan du også bruke [!INCLUDE [prod_short](includes/prod_short.md)]-funksjoner til å eksportere kundens data hvis du blir bedt om det. Hvis du vil ha mer informasjon om personvern i [!INCLUDE [prod_short](includes/prod_short.md)], kan du se [Vanlige spørsmål om personvern for Business Central-kunder](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Se også
[Oversikt over [!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]