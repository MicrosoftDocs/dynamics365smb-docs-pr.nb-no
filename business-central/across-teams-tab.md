---
title: Legg til Business Central-fane i Microsoft Teams
description: Lær hvordan du legger til faner i Teams som viser Business Central-sider.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams" />Legg til Business Central-fane i Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

I Teams vises faner øverst i kanaler og nettpratvinduer, noe som gir deltakerne rask tilgang til relevant informasjon. Denne artikkelen forklarer ulike måter å legge til en fane som viser [!INCLUDE [prod_short](includes/prod_short.md)]-data på.

![Faner i Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs" />Om Business Central-faner

En [!INCLUDE [prod_short](includes/prod_short.md)]-fane inneholder en fokusert visning av [!INCLUDE [prod_short](includes/prod_short.md)]-liste og -kortsider. Fanen viser ikke hele [!INCLUDE [prod_short](includes/prod_short.md)]-nettklienten. Det finnes ingen kantlinje i nettleseren, [!INCLUDE [prod_short](includes/prod_short.md)]-banner (f.eks. Fortell meg, søk, hjelp) eller øvre navigasjonsmeny – bare sideinnhold og tilhørende handlinger. Innholdet er interaktiv, noe som betyr at du kan velge handlinger og koblinger, endre data og så videre. Du er begrenset til det du ser og kan gjøre med de samme tillatelsene som er tildelt kontoen i [!INCLUDE [prod_short](includes/prod_short.md)].

Hvis du vil ha mer informasjon om hvem som kan se innholdet i en [!INCLUDE [prod_short](includes/prod_short.md)]-fane, kan du se [Hvem kan se innholdet i en fane?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Er du en utvikler? Du kan også legge til faner programmatisk ved hjelp av Microsoft Graph-API-en. Hvis du vil ha mer informasjon, kan du se [Legg til en Business Central-faner i Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites" />Forutsetninger

Følgende forutsetninger må være oppfylt for å legge til en [!INCLUDE [prod_short](includes/prod_short.md)]-fane:

- Du har tilgang til Microsoft Teams.
- Du må ha en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens.
- Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md).

Hvis du vil vise [!INCLUDE [prod_short](includes/prod_short.md)]-fanen som ble lagt til av en annen deltaker i kanalen eller nettpraten, må følgende krav oppfylles:

- Du har tilgang til Microsoft Teams.
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-lisens eller begrenset tilgang til Business Central med bare en Microsoft 365-lisens. Hvis du vil ha mer informasjon, kan du se [Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md).
- Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.

## <a name="add-tab-using-recommended-content" />Legg til fane med anbefalt innhold

Bruk denne fremgangsmåten til å legge til en fane ved å velge hva som skal vises fra en lett tilgjengelig liste over anbefalt innhold som er basert på rollesenteret – å forlate Teams. Hvis du vil vite mer om innholdet du kan velge mellom, kan du se [Hvor kommer det anbefalte innholdet fra?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Velg **+ Legg til en fane** øverst i en kanal eller nettprat i Teams.
2. I boksen **Søk** skriver du inne *business central*, velger **[!INCLUDE [prod_short](includes/prod_short.md)]**-ikonet og venter til [!INCLUDE [prod_short](includes/prod_short.md)]-fanekonfigurasjonsvinduet vises.

   ![Viser konfigurasjonsvinduet for Business Central-fanen i Teams](media/teams-bc-tab-config-window.png)

3. Alternativet **Velg fra innhold som anbefales for** viser selskapet du arbeider med i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil vise innhold fra et annet selskap, velger du det aktuelle selskapet og bruker deretter alternativene for **Miljø** og **Selskap** til å angi hvilket selskap du vil arbeide med.
4. Velg pil ned i alternativet **Faneinnhold** og velg innholdet du vil vise.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Noen sider kan inneholde ulike visninger som er varianter av siden som er filtrert for å vise bestemte data. Hvis du vil endre visningen av innholdet, velger du pil ned for alternativet **Foretrukket visning** og velger visningen fra listen.

   Hvis du vil ha mer informasjon om visninger, kan du se [Lagre og tilpass visninger](ui-views.md).
6. Velg **Publiser til kanalen om denne fanen** for å legge inn en kunngjøring i Teams-kanalen eller -nettpraten automatisk for å la deltakerne vite at du har lagt til denne fanen.
7. Velg **Lagre**.

## <a name="add-tab-using-a-page-link" />Legg til fane ved hjelp av en sidekobling

En annen måte å legge til en fane er ved å bruke en kobling (nettadresse) på siden du vil vise. Denne måten er nyttig når du vil vise en bestemt [!INCLUDE [prod_short](includes/prod_short.md)]-post eller en listeside som ikke er bokmerket i rollesenteret.

1. Velg **+ Legg til en fane** øverst i en kanal eller nettprat i Teams.
2. I boksen **Søk** skriver du inn *business central*, og deretter velger du **[!INCLUDE [prod_short](includes/prod_short.md)]**-ikonet.
3. Vent til [!INCLUDE [prod_short](includes/prod_short.md)]-fanekonfigurasjonsvinduet vises, og velg deretter alternativet **Lim inn en [!INCLUDE [prod_short](includes/prod_short.md)]-kobling i stedet**.

   ![Viser konfigurasjonsvinduet for Business Central-fanen i Teams og uthever koblingsalternativet](media/teams-bc-tab-config-window-page-link.png)
4. Gå til [!INCLUDE [prod_short](includes/prod_short.md)], og åpne siden du vil vise i fanen.
5. Kopier koblingen til siden.

   Det finnes to måter å kopiere koblingen på. Den enkleste og foretrukne måten er å velge **Del** ![Del-ikon i Business Central](media/share-icon.png) > **Kopier kobling**. Den andre måten er å kopiere hele nettadressen fra adresselinjen i nettleseren. Hvis du vil ha mer informasjon om dette trinnet, kan du se [Deling av Business Central-poster og -sidekoblinger](across-working-with-teams.md).

6. Gå tilbake til Teams og lim inn koblingen i boksen **Nettadresse**.
7. Skriv inn et navn som skal vises i fanen, i boksen **Fanenavn**.
8. Velg **Publiser til kanalen om denne fanen** for å legge inn en kunngjøring i Teams-kanalen eller -nettpraten automatisk for å la deltakerne vite at du har lagt til denne fanen.
9. Velg **Lagre**.

## <a name="add-tab-by-pinning-card-details" />Legg til fane ved å feste kortdetaljer

Bruk disse trinnene til å legge til en fane for en post som ble delt eller limt inn i en Teams-kanal eller -nettprat. Hvis du vil lære hvordan du deler poster og sidekoblinger i Teams, kan du se [Del poster og sidekoblinger i Teams](across-working-with-teams.md).

1. Velg **Detaljer**-knappen på kortet i Teams.
2. Øverst i høyre hjørne av kortdetaljer velger du **Fest til toppen av nettpratvindu** ![Festeikon for å legge til Teams-fane i Business Central](media/pin-teams.png)-ikonet.

## <a name="change-a-tab-and-its-content" />Endre en fane og innholdet

Når en fane er lagt til, kan du foreta bestemte endringer i fanen. Du kan for eksempel gi nytt navn til fanen, flytte den og fjerne den. Du finner disse handlingene i fanealternativene som er tilgjengelige, ved å velge pil ned i fanen.

![Viser konfigurasjonsvinduet for Business Central-fanen i Teams og menyen for fanealternativer](media/teams-bc-tab-config-window-options.png)

Du kan endre dataene hvis du har tilgang til innholdet i en fane. Hvis du endrer dataene, vil ikke andre se endringene før de forlater fanen og kommer tilbake. Det samme gjelder hvis noen andre endrer data. Du kan ikke endre siden som vises i fanen, så du trenger bare å fjerne fanen og legge til en annen av seriene.

Du kan også endre visningen av siden og dataene, for eksempel sortering og endring av oppsettet mellom liste- og flisvisninger. Når du gjør slike endringer, påvirker de ikke det andre ser. De ser det du opprinnelig la inn, inntil de gjør lignende endringer selv.

## <a name="see-also" />Se også

[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Deling av Business Central-oppføringer og sidekoblinger i Microsoft Teams](across-working-with-teams.md)
[Vanlige spørsmål om Teams](teams-faq.md)  
[Søk etter kunder, leverandører og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Endre selskap og andre innstillinger i Teams](across-teams-settings.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
