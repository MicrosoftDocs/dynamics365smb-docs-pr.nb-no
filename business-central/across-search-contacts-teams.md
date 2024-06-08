---
title: Søke etter kontakter fra Microsoft Teams
description: 'Finn ut hvordan du slår opp kunder, leverandører og andre kontakter for Business Central fra Microsoft Teams.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/16/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a>Søke etter kunder, leverandører og andre kontakter fra Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]. Introdusert i lanseringsbølge 1 for 2021.

[!INCLUDE [prod_short](includes/prod_short.md)] har et omfattende administrasjonssystem for forretningskontakter som er nødvendig for brukere i salg, operasjoner eller andre avdelingsroller. Hvis du er en bruker i en av disse rollene, må du ofte slå opp, møte eller starte en samtale med leverandører, kunder og andre kontakter. Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams kan du utføre disse oppgavene direkte fra grupper, uten å måtte bytte til [!INCLUDE [prod_short](includes/prod_short.md)]. I Teams kan du gjøre følgende:

- Slå opp [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter fra kommandoboksen i Teams eller fra meldingsområdet. Kontakter kan omfatte kundeemner, leverandører, kunder eller andre forretningsforhold.
- Dele en kontakt som et kort i en Teams-samtale.
- Vise detaljer om kontakten, samhandlingsloggen og annen innsikt som utestående betalinger eller åpne dokumenter.

## <a name="prerequisites"></a>Forutsetninger

- Du har tilgang til Microsoft Teams.
- Du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams. Hvis du vil ha mer informasjon, se [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)
- Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-konto med tilgang til kontakter i minst ett selskap.

> [!NOTE]
> Det kan hende at du blir bedt om å logge på eller sette opp appen første gang når du søker fra kommandoboksen eller meldingsboksen. Dette trinnet er nødvendig for å søke etter kontakter i det rette Business Central-selskapet. Hvis du vil ha informasjon om hvordan du definerer appen for å velge selskap, kan du se [Endre selskap og andre innstillinger i Teams](across-teams-settings.md).

## <a name="look-up-contacts-from-the-command-box"></a>Slå opp kontakter fra kommandoboksen

Kommandoboksen vises øverst i alle skjermbilder i Teams. Det gjør det mulig å søke, utføre raske handlinger eller starte apper, for eksempel [!INCLUDE [prod_short](includes/prod_short.md)]-appen. Søking fra kommandoboksen er nyttig for raskt å finne frem til kontakter og tilhørende data for eget bruk. La oss for eksempel anta at du vil slå opp en e-postadresse for en leverandør for å opprette et kalendermøte. Eller kanskje du vil søke etter samhandlingslogg mens du møter med en kunde.

1. Skriv inn **/Business Central** i kommandoboksen, og velg deretter Business Central-appen fra resultatene.

    ![Åpne Business Central-appen hvis du vil søke etter kontakter fra kommandoboks.](media/teams-contacts-command-1a.png)

2. I **Business Central**-boksen begynner du å skrive søketekst, som navn, adresse eller telefonnummer.

    Etter hvert som du skriver inn, vises samsvarsresultater.

    ![Søk etter Business Central-kontakter fra kommandoboksen i Teams.](media/teams-contacts-command-2.png)
3. Velg en kontakt fra resultatene.

    Kontaktkortet vises under kommandoboksen.

4. Hvis du vil legge til kontaktkortet i en samtale, går du til øvre høyre hjørne på kortet og velger **... (Flere alternativer)** > **Kopier**. Deretter limer du inn kopien i meldingsboksen i en samtale.  

Hvis du vil ha mer generell informasjon om kommandoboksen i Teams, kan du se [Teams – bruke kommandoboksen](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## <a name="look-up-contacts-from-the-message-compose-box"></a>Slå opp kontakter fra meldingsboksen

Fordelen med å bruke meldingsboksen er at du kan legge til et kontaktkort direkte i en samtale, slik at andre kan se det.

1. Under til meldingsboksen velger du **Business Central**-ikonet for å starte appen.

    Hvis **Business Central**-ikonet ikke vises, velger du **... (Meldingsutvidelser)**.

    ![Åpne Business Central-appen hvis du vil søke etter kontakter fra meldingsboks.](media/teams-contacts-message-box.png)

2. I **Business Central**-boksen begynner du å skrive søketekst, som navn, adresse eller telefonnummer.

    Etter hvert som du skriver inn, vises samsvarsresultater.

    ![Søk etter Business Central-kontakter fra meldingsboks.](media/teams-contacts-5.png)
3. Velg en kontakt fra resultatene.

    Kontaktkortet vises i meldingsboksen.

    > [!NOTE]
    > Kontaktkortet blir ikke sendt til samtalen med en gang slik at andre kan se det. Du har muligheten til å gå gjennom innholdet på kortet, og legge til tekst før eller etter det etter behov. Send deretter meldingen til chatten når du er klar.

<!--
### <a name="heres-another-way"></a>Here's another way

1. Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.
2. Enter your search terms in the box.
3. Use the up and down arrow keys on the keyboard to choose a contact, then select <kbd>Enter</kbd> to select it.-->

## <a name="viewing-contact-card-details"></a>Vise kontaktkortdetaljer

Kontaktkortet i Teams gir deg en rask oversikt over kunden, leverandøren eller kontakten. Kortet er interaktivt&mdash;noe som betyr at du kan vise mer informasjon eller endre en kontakt ved hjelp av knappen **Detaljer** eller **Eget vindu**.

Knappen **Detaljer** åpner et vindu i Teams som viser mer informasjon om kontakten, men ikke like mye som i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil vise all informasjon om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)], velger du **Eget vindu**.

Kontaktkortet fungerer på samme måte som kort for poster, for eksempel varer, kunder eller ordrer. Hvis du vil ha mer informasjon om kort, kan du se [Vise kortdetaljer](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Alle deltakere i en Teams-samtale kan vise kort for Business Central-kontakten du sender til en samtale. Men hvis de vil vise flere detaljer om poster, ved hjelp av **Detaljer** eller **Eget vindu**-knappene på et kort, trenger de tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Administrere Microsoft Teams-integrering](admin-teams-integration.md#minimum-requirements-1).

## <a name="see-also"></a>Se også

[Oversikt over Business Central og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Endre selskap og andre innstillinger i Teams](across-teams-settings.md)  
[Dele poster i Microsoft Teams](across-working-with-teams.md)  
[Feilsøke Teams](admin-teams-troubleshooting.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
