---
title: Administrere Microsoft Teams-integrering med Business Central | Microsoft Docs
description: Administrer Business Central-integrering med Microsoft Teams.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics365-business-central
---

# <a name="managing-microsoft-teams-integration-with-"></a>Administrere Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikkelen gir en oversikt over hva du kan gjøre som administrator for å styre Microsoft Teams-integrasjon med [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="in-microsoft-teams"></a>I Microsoft Teams

### <a name="minimum-requirements"></a>Minstekrav

Denne delen beskriver minimumskravene for at [!INCLUDE [prod_short](includes/prod_short.md)]-appfunksjonene skal fungere i Teams.

- Nødvendige lisenser

    [!INCLUDE[prod_short](includes/prod_short.md)]-appen krever en Teams-lisens gjennom et Microsoft 365 Business- eller Enterprise-abonnement. Frittstående Teams-abonnementer, for eksempel Microsoft Teams (kostnadsfritt) eller Microsoft Teams Essentials, støttes ikke.

    De fleste funksjoner i [!INCLUDE[prod_short](includes/prod_short.md)]-appen for Teams krever også en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens, som vist i tabellen nedenfor.

    |Hva|[!INCLUDE [prod_short](includes/prod_short.md)]-lisens|
    |----|---|
    |Søk etter [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter.|![avmerking](media/check.png "avmerking")|
    |Lim inn en kobling til en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale, og send den som et kort.|![avmerking](media/check.png "avmerking")|
    |Del en kobling fra en side i [!INCLUDE [prod_short](includes/prod_short.md)] til Teams-samtale.|![avmerking](media/check.png "avmerking")|
    |Vis et kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.||
    |Vis flere detaljer i kort for en [!INCLUDE [prod_short](includes/prod_short.md)]-post i en samtale.|![avmerking](media/check.png "avmerking")|
    |Åpne en sidekobling i [!INCLUDE [prod_short](includes/prod_short.md)] fra en samtale.|![avmerking](media/check.png "avmerking")|

- Tillat URL-forhåndsvisninger

    Policyinnstillingen **Tillat URL-forhåndsvisninger** må være aktivert. Ellers kan ikke et kort genereres for [!INCLUDE [prod_short](includes/prod_short.md)]-koblinger som limes inn i en Teams-samtale. Hvis du vil ha mer informasjon om denne innstillingen, kan du se [Administrere meldingspolicyer i Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the--app-optional"></a>Administrere [!INCLUDE [prod_short](includes/prod_short.md)]-appen (valgfritt)

Som Teams-administrator kan du behandle alle apper for organisasjonen, inkludert [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Du kan godkjenne eller installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for organisasjonen, hindre at brukere installerer appen, med mer.

Hvis du vil ha mer informasjon, kan du se følgende artikler i Microsoft Teams-dokumentasjonen:

- [Behandle appene i administrasjonssenteret i Microsoft Teams](/MicrosoftTeams/manage-apps)
- [Administrere policyer for appoppsett i Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## <a name="in-"></a>I [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements-1"></a>Minstekrav

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

## <a name="installing-the-business-central-app-by-using-centralized-deployment"></a>Installer Business Central-appen ved hjelp av sentralisert distribusjon

I Microsoft Teams-administrasjonssenteret konfigurerer du policyer for Teams-appkonfigurasjonspolicyer for organisasjonen. I Teams-administrasjonssenteret kan du bruke funksjonen for sentralisert distribusjon til å installere Business Central-appen i Teams for alle brukere i organisasjonen automatisk, bestemte grupper eller individuelle brukere.

> [!NOTE]
> Teams-kontoen må ha rollen **Teams-administrator** eller rollen **Global administrator** for å kunne konfigurere sentralisert distribusjon .

1. I Business Central velger du ikonet ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Teams-appen Sentralisert distribusjon**. Deretter velger du relatert kobling. Du kan også velge [her](https://businesscentral.dynamics.com/?page=1833) for å åpne siden direkte.
2. Les informasjonen om **Konfigurer Business Central-appen for Teams**, og velg deretter **Neste** når du er klar.
3. Åpne [administrasjonssenteret for Teams](https://go.microsoft.com/fwlink/?linkid=2163970), og følg fremgangsmåten nedenfor.
    1. Gå til **Teams-apper** > **Konfigurasjonspolicyer**.
    2. Opprett en ny policy, eller velg policyen du vil bruke til å installere Business Central-appen, og velg deretter **Legg til apper**.
    3. Søk etter og velg **Business Central** på siden **Legg til installerte apper**.
    4. Velg **Legg til**.

       Business Central skal nå vises under **Installerte apper** for policyen.
    5. Konfigurer flere innstillinger etter behov og velg **Lagre**.

    Hvis du vil ha mer informasjon om konfigurasjonspolicyer i Teams, kan du se [Administrere appkonfigurasjonspolicyer i Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) i Teams-dokumentasjonen.
4. Gå tilbake til **Team-appen Sentralisert distribusjon** av Business Central, og velg **Ferdig**.

> [!IMPORTANT]
> Det kan ta opptil 24 timer før appkonfigurasjonspolicyen tas i bruk, og appen distribueres til brukerne.

## <a name="managing-privacy-and-compliance"></a>Administrere personvern og samsvar

Microsoft Teams gir omfattende kontroller for samsvar og håndtering av sensitive eller personlige data, inkludert data som er lagt til i chatter og kanaler av [!INCLUDE [prod_short](includes/prod_short.md)]-appen.

### <a name="understanding-where--cards-are-stored"></a>Forstå hvor [!INCLUDE [prod_short](includes/prod_short.md)]-kort lagres

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

## <a name="show-or-hide-record-data-on-cards"></a>Vis eller skjul oppføringsdata på kort

Når en oppføring deles med andre i en Teams-nettprat eller -kanal, vises et kort med felter som inneholder data om oppføringen. Alle mottakere kan vise disse opplysningene (eller oppføringssammendraget) som standard, uavhengig av lisensen eller tillatelsene i Business Central. Hvis du er administrator, kan du bruke veiledningen for assistert oppsett for **Kortinnstillinger** til å skjule oppføringssammendraget fra å vises på kort i Teams. Når du skjuler oppføringssammendraget, fjernes alle felter og bilder, men fortsetter å vise knappen **Detaljer** og annen informasjon ikke om oppføringen på kortet.

|Oppføringssammendrag på|Oppføringssammendrag av|
|-|-|
|![Bilde som viser et kort i Teams når oppføringssammendraget er slått på.](media/card-settings-example-on.png)|![Bilde som viser et kort i Teams når oppføringssammendraget er slått av.](media/card-settings-example-off.png)|

Du konfigurerer innstillingen per miljø. Når du aktiverer eller deaktiverer oppføringssammendraget, vil det påvirke alle selskapene i miljøet.

1. Åpne miljøet du vil endre, i Business Central.

   > [!TIP]
   > Hvis du vil bytte miljø, velger du <kbd>CTRL</kbd>+<kbd>O</kbd>.
2. Velg ikonet ![Forstørrelsesglass som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kortinnstillinger**, og velg deretter den relaterte koblingen. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Les informasjonen om **kortinnstillingene**, og velg deretter **Neste** når du er klar.
4. På siden **Datasynlighet** slår du på bryteren **Vis oppføringssammendrag** for å vise data på kortene eller av for å skjule dataene.
5. Velg **Neste** og følg instruksjonene for å fullføre installasjonsveiledningen.

## <a name="see-also"></a>Se også

[Oversikt over [!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
