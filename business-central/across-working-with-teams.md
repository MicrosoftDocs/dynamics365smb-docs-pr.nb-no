---
title: Deling av Business Central-oppføringer i Microsoft Teams
description: Lær hvordan du bruker Business Central-appen for Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 16/18/2023
ms.author: jswymer
ms.custom: bap-template
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams"></a>Deling av Business Central-oppføringer og sidekoblinger i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] tilbyr et par måter å dele data på fra Business Central direkte i en Microsoft Teams-samtale:

<!-- 
## <a name="overview"></a>Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Når [!INCLUDE [prod_short](includes/prod_short.md)]-appen er installert i Teams, kan du ta med et interaktivt kort med Business Central-oppføring i en Teams-samtale.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Med eller uten [!INCLUDE [prod_short](includes/prod_short.md)]-appen installert, kan du dele en kobling fra sider i Business Central til en Teams-samtale.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Følgende avsnitt beskriver de ulike måtene mer detaljert.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation"></a>Ta med og vis et Business Central-kort i en Teams-samtale

Med Business Central-appen for Teams kan du kopiere en kobling fra en hvilken som helst Business Central-oppføring, for eksempel en kunde eller ordre, og lime inn koblingen i en Teams-samtale. Appen kobler Microsoft Teams til forretningsdataene i [!INCLUDE [prod_short](includes/prod_short.md)]\. Den utvider deretter koblingen til et kompakt, interaktivt kort som viser informasjon om posten. Når du er i samtalen, kan du og kollegaene dine vise flere detaljer om posten, redigere data og utføre handlinger uten å forlate Teams.

[![Teams-integrering med Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites"></a>Forutsetninger

- Du har tilgang til Microsoft Teams.
- Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Alle deltakere i en Teams-samtale kan vise kort for Business Central-oppføringer som du sender til samtalen. Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation"></a>Ta med et Business Central-kort i en Teams-samtale

1. Logg på [!INCLUDE [prod_short](includes/prod_short.md)] ved å bruke leseren.
2. Åpne posten du vil dele.

    Appen er utformet for å vise et kort for nesten alle typer [!INCLUDE [prod_short](includes/prod_short.md)]-sider. Men den gir best opplevelse når det brukes for sider som viser én enkelt post, for eksempel en vare, kunde eller ordre.
3. Kopier koblingen til siden.

    Det finnes to måter å kopiere koblingen på. Den enkleste og foretrukne måten er å velge **Del** ![Del-ikon i Business Central](media/share-icon.png) > **Kopier kobling**. Den andre måten er å kopiere hele nettadressen fra adresselinjen i nettleseren.

    [![Kopier nettadressen for Business Central fra nettleseren.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Gå til Teams og start en samtale, som kan være en chat med en person, gruppe med personer eller en teamkanal.
5. Lim inn nettadressen i meldingsboksen der du skriver en melding.

    ![Lim inn URL-adresse for Business Central i Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Hvis du får en melding som denne: *Business Central ønsker å forhåndsvise denne koblingen.*, betyr det at du ikke har Business Central-appen for Teams installert. Hvis du vil installere appen, velger du **Vis forhåndsvisning** og følger instruksjonene.

    > [!NOTE]
    > Avhengig av Business Central-versjonen din kan det hende du blir bedt om å logge deg på [!INCLUDE [prod_short](includes/prod_short.md)] og gi samtykke for appen til å hente data første gang du limer inn en kobling i en samtale. Bare følg instruksjonene på skjermen. Du trenger bare å utføre dette trinnet én gang.
6. Vent et øyeblikk mens et kort genereres i meldingsboksen.
7. Når kortet vises, kan du se nøye gjennom innholdet på kortet for eventuell sensitiv informasjon før du sender meldingen. Dette trinnet er viktig fordi når du sender meldingen, kan alle i samtalen se kortet.
8. Hvis kortet ser bra ut, velger du **Send** for å sende det til samtalen.

    > [!TIP]
    > Når kortet vises, og før du velger **Send**, kan du slette den innlimte URL-adressen hvis du vil det.
9. Hvis du vil vise flere detaljer eller gjøre endringer i posten som vises på kortet, velger du **Detaljer**. Hvis du vil ha mer informasjon, kan du se neste avsnitt.

### <a name="view-card-details"></a>Vis kortdetaljer

Når et kort er sendt til en samtale, kan alle deltakerne med de [riktige tillatelsene](admin-teams-integration.md#permissions) velge **Detaljer** for å åpne et vindu som viser mer informasjon om posten, og eventuelt gjøre endringer i posten. Det spiller ingen rolle om du er den som sender kortet, eller den som mottar kortet. **Detaljer**-funksjonen er spesielt nyttig for mottakere fordi den raskt gir dem konsis, målrettet informasjon om posten.

Detaljer-vinduet ligner på det du ser i [!INCLUDE [prod_short](includes/prod_short.md)], men det er fokusert på siden eller posten som kortet handler om. Når du er ferdig med å vise og gjøre endringer, lukker du vinduet for å gå tilbake til Teams-samtalen.

Her er noen ting du må huske på når du arbeider med kortdetaljene:

- For å vise kortdetaljene må brukere ha tillatelse på siden og tilhørende data i [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Kort i Teams-chatter oppdateres ikke automatisk til endringer. Eventuelle endringer du lagrer i en post i detaljvinduet, lagres i [!INCLUDE [prod_short](includes/prod_short.md)]\. Kortet i Teams viser derfor ikke endringene i konverteringen før du limer inn koblingen på nytt.

Hvis du vil vite mer om hvordan du arbeider med kort og kortdetaljer, kan du se [Vanlige spørsmål om Teams](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams"></a><a name="share-link"></a>Del en kobling til side i Business Central til Teams

Fra de fleste samlingssider, for eksempel **Varer**-siden, og detaljsider, for eksempel **Vare**-kortet, kan du sende en kobling til siden til bestemte mottakere i en Teams-samtale. Du kan for eksempel dele en kobling til en filtrert visning av postene. Mottakerne kan deretter velge koblingen for å åpne siden i [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!Del-menyen som vises på et kort.](media/teams-share-link-v2.png "Del-menyen som vises på et kort.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites-1"></a>Forutsetninger

- Du har tilgang til Microsoft Teams.
- (Valgfritt) Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. 

  Når appen er installert, inneholder meldinger du sender sammen med koblingen, også et kompakt kort for siden. Hvis du vil ha mer informasjon om hvordan du installerer appen, kan du se [Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link"></a>Del en kobling

1. I [!INCLUDE [prod_short](includes/prod_short.md)]\, åpner du siden som du vil dele.
2. Velg ikonet ![!Del til andre apper-handling på sider.](media/share-icon.png) øverst på siden og deretter **Del til Teams**.
3. Hvis du blir bedt om det, logger du deg på Teams med brukernavn og passord.
4. På siden **Del til Teams** skriver du inn navnet på en person, gruppe eller kanal du vil sende meldingen til.
5. Meldingsboksen inneholder en kobling til siden. Hvis [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Team er installert, vil et kort for den koblede posten eller siden også vises i meldingsboksen.

   Legg til flere opplysninger hvis du vil, og velg **Del**.
6. Koblingen er nå delt. Hvis du vil gå til samtalen, velger du **Gå til Teams**.

## <a name="see-also"></a>Se også

[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Søke etter kunder, leverandører og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Endre selskap og andre innstillinger i Teams](across-teams-settings.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
