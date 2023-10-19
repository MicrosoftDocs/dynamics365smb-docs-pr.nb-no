---
title: Konfigurer skrivere for Universell utskrift
description: Lær hvordan du kan bruke Universell utskrift til å gi skyutskrift i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# Konfigurer skrivere for Universell utskrift

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Universell utskrift er en tjeneste basert på et Microsoft 365-abonnement som kjører på Microsoft Azure. Den gir deg sentralisert utskriftsbehandling via portalen for Universell utskrift. [!INCLUDE[prod_short](includes/prod_short.md)] gjør at skrivere som er konfigurert med Universell utskrift, tilgjengelige for klientbrukere via utvidelsen **Integrering med Universell utskrift**.

![Konfigurasjon av Universell utskrift.](media/Universal-Print-arch.png)

Hele installasjonsprogrammet krever at du arbeider både i Microsoft Azure, ved hjelp av [Azure-portalen](https://portal.azure.com), og i [!INCLUDE[prod_short](includes/prod_short.md)]. Oppsettet deles mellom to hovedoppgaver som beskrevet i denne artikkelen:

1. I Microsoft Azure kan du konfigurere Universell utskrift og legger til skrivere som du vil bruke i Business Central til en utskriftsdeling. Gå til [denne delen](#set-up-universal-print-and-printers-in-microsoft-azure).
2. I [!INCLUDE[prod_short](includes/prod_short.md)] legger du til skriverne fra skriverdelingene i Universell utskrift. Gå til [denne delen](#add-printers-in-business-central-online) for nettversjonen eller [hit](#add-printers-in-business-central-on-premises) for den lokale versjonen.

## Forutsetninger

- Støttede skrivere

  [!INCLUDE[prod_short](includes/prod_short.md)] støtter de samme skriverne som Universell utskrift, som kan være enten kompatible eller ikke-kompatible skrivere for Universell utskrift. Ikke-kompatible skrivere kan ikke kommunisere med Universell utskrift direkte, så de krever ekstra koblingsprogramvare, som leveres av Universell utskrift. Det kan hende at enkelte eldre skrivere ikke støttes. 

- Universell utskrift:

  - Abonnement/lisens for Universell utskrift for organisasjonen.

    Finn ut mer under [Lisens for Universell utskrift](/universal-print/fundamentals/universal-print-license).

  - Du har rollene **Utskriftsadministrator** (eller Utskriftbehandler) og **Global administrator** i Azure.

    Hvis du skal administrere Universell utskrift, må kontoen din ha rollene **Utskriftsadministrator** (eller Utskriftsbehandler) og **Global administrator** i Microsoft Entra ID. Disse rollene er bare nødvendige for administrasjon av Universell utskrift. De er ikke nødvendige av personer som konfigurerer og bruker skriverne fra [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] nettversjon og lokal versjon:

  - Lanseringsbølge 1 eller nyere for [!INCLUDE[prod_short](includes/prod_short.md)] 2021.
  - Utvidelsen **Integrering med Universell utskrift** er installert.

    Denne utvidelsen publiseres og installeres som standard som en del av [!INCLUDE[prod_short](includes/prod_short.md)] Online og lokalt. Du kan kontrollere om den er installert på siden **Administrasjon av utvidelse**. Finn ut mer under [Installer og avinstaller utvidelser i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] bare lokalt:
  - Microsoft Entra ID eller NavUserPassword-godkjenning er konfigurert.
    > [!NOTE]
    >  Utvidelsen Universell utskrift støtter ikke tjeneste-til-tjeneste-godkjenning (S2S). Det krever en pålogget bruker for å sende utskriftsjobber til Universell utskrift-tjeneste via Graph API.
  - En applikasjon for Business Central er registrert i Microsoft Entra-leieren og [!INCLUDE[prod_short](includes/prod_short.md)].

    På samme måte som andre Azure-tjenester som arbeider med [!INCLUDE[prod_short](includes/prod_short.md)], krever Universell utskrift en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Entra ID. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Universell utskrift.

    Det kan hende at distribusjonen allerede bruker en appregistrering for andre Azure-tjenester, for eksempel Power BI. I så fall kan du også bruke den eksisterende programregistreringen for Universell utskrift, i stedet for å legge til en ny. Det eneste du trenger å gjøre, er å endre appregistreringen slik at den inneholder de relevante utskriftstillatelsene for Microsoft Graph API: **PrinterShare.ReadBasic.All**, **PrintJob.Create** og **PrintJob.ReadBasic.** 

    Slik registrerer du en app og angir de riktige tillatelsene, følger du fremgangsmåten som er beskrevet i [Registrere en applikasjon i Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

## Konfigurer Universell utskrift og skrivere i Microsoft Azure

Før du kan begynne å administrere skrivere for Universell utskrift i Business Central, er det flere oppgaver for å få Universell utskrift til å fungere i Azure med de skriverne du vil bruke.

Hvis du vil ha detaljerte instruksjoner om hvordan du konfigurerer, kan du se [Kom i gang: konfigurer Universal utskrift](/universal-print/fundamentals/universal-print-getting-started) i dokumentasjonen for Universell utskrift. Her er en oversikt over trinnene du må fullføre. De fleste av disse trinnene gjøres i Azure-portalen.

1. Tilordne lisenser for Universell utskrift til deg selv og andre brukere.

    Hvordan du tilordner lisensen, avhenger av om du integrerer med Business Central Online eller lokalt.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] Online kan du tildele lisenser ved hjelp av administrasjonssenteret i Microsoft 365.

      Finn ut mer under [Hjelp for administrasjonssenteret i Microsoft – Tildel lisenser til brukere](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan du tilordne lisenser i leieren ved hjelp av Azure-portalen.

      Finn ut mer under [Tilordne eller fjerne lisenser i Azure-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installer koblingen for Universell utskrift for å registrere skrivere som ikke kan kommunisere med Universell utskrift direkte.

    De fleste skrivere på markedet kan ikke kommunisere med Universell utskrift direkte, så du må installere koblingen Universell utskrift. Finn ut mer under [Installere koblingen Universell utskrift](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrer skriverne i Universell utskrift.

    Når du registrerer en skriver, blir den registrert av Universell utskrift.

    - For skrivere som kan kommunisere direkte med Universell utskrift, følger du instruksjonene fra skriverprodusenten.

    - For andre skrivere kan du registrere skriverne ved å bruke koblingen Universell utskrift. 

      Finn ut mer under [Skriverregistrering](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Endre skriveregenskaper (valgfritt)

    Når en skriver er registrert, kan du vise og endre skriveregenskaper, for eksempel standardinnstillinger.

    Finn ut mer under [Administrere skriverinnstillinger ved hjelp av portalen for Universell utskrift](/universal-print/portal/configure-printer-settings).

5. Del skriverne med brukerne.

    Alle skrivere du vil bruke i [!INCLUDE[prod_short](includes/prod_short.md)], må legger til i en *skriverdeling* i Universell utskrift. Alle brukere som trenger tilgang til skriveren, må legges til som et medlem av skriverdelingen. Finn ut mer under [Del en skriver](/universal-print/portal/share-printers).

    > [!TIP]
    > Du kan alltid legge til eller fjerne brukere senere. Finn ut mer under [Skrivertillatelser](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Aktiver dokumentkonvertering.

    Universell utskrift gjengir innhold for utskrift i XPS-format. Noen eldre skrivere i markedet støtter ikke gjengivelse av XPS-innhold, i mange tilfeller bare PDF-format. Utskrift til slike skrivere vil mislykkes med mindre Universell utskrift konfigureres til å konvertere dokumenter til formatet som støttes av skriveren.

    Finn ut mer under [Oversikt over dokumentkonvertering](/universal-print/portal/document-conversion).

Nå er du klar til å legge til skriverne i [!INCLUDE[prod_short](includes/prod_short.md)], konfigurerer du standardskrivere for rapporter og utskrift.  

## Legg til skrivere i nettversjonen av Business Central

Når skrivere er satt opp og delt med Universell utskrift, er du klar til å legge dem til i [!INCLUDE[prod_short](includes/prod_short.md)] for bruk. Du kan legge til skrivere for Universell utskrift på to måter. Du kan legge til skriverne samtidig eller enkeltvis, én om gangen.

Når du legger til skrivere enkeltvis, kan du konfigurere den samme skriveren for Universell utskrift i [!INCLUDE[prod_short](includes/prod_short.md)] mer enn én gang. Deretter kan du endre utskriftsinnstillingene, for eksempel papirskuff, størrelse og sideretning, for hver ekstra skriver. På denne måten kan du sette opp skrivere for ulike rapporter og dokumenter med spesielle krav til utdata.

> [!NOTE]
> Bruker den lokale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]? Hvis dette er tilfellet, går du til [neste avsnitt](#add-printers-in-business-central-on-premises), første gangs oppsett er litt forskjellig.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg **Universell utskrift**, og velg deretter ett av følgende alternativer:

   - **Legg til alle skrivere for Universell utskrift** for å legge til alle skrivere som ikke allerede er lagt til. Du kan bruke dette alternativet selv om skrivere allerede er lagt til.
   - **Legg til en skriver for Universell utskrift** for å legge til en bestemt skriver.  
3. Følg instruksjonene på skjermen.

    - Hvis du velger **Legg til alle skrivere for Universell utskrift**, starter oppsettet **Legg til skrivere for Universell utskrift**. 

    - Hvis du velger **Legg til en skriver for Universell utskrift**, vises siden **Innstillinger for Universell utskrift**. Fyll ut feltet **Navn**, og velg **...** ved siden av feltet **Utskriftsdeling i Universell utskrift** for å velge skriverdelingen som inneholder Universell utskrift-skriveren. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Når du har lagt til en skriver, kan du vise og endre innstillingene fra siden **Utskriftsbehandling**. Det er bare å velge skriveren, og deretter velger du **Rediger skriverinnstillinger**.

## Legg til skrivere i den lokale versjonen av Business Central

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Før en bruker kan legge til eller bruke Universell utskrift-skrivere i Business Central, må de godkjenne tilgang til Azure-tjenestene som brukes av Universell utskrift, og gi dem tillatelse til data og operasjoner som:

- Pålogging og lesing av brukerprofil
- Lesing av grunnleggende utskriftsjobbinformasjon
- Oppretting av utskriftsjobber

Dette gjøres vanligvis første gang de kobler seg til den Azure-registrerte appen som brukes til Universell utskrift. I nettversjonen av Business Central utføres denne autorisasjonsflyten på en sømløs måte, uten brukersamhandling. Men den lokale versjonen av Business Central fungerer annerledes. Det krever at du eller en annen bruker som ønsker å bruke Universell utskrift-skrivere, til å starte godkjenningsflyten – vanligvis bare én gang. Den mest direkte måten er beskrevet i fremgangsmåten nedenfor. En mindre direkte måte er å koble til en annen integrert tjeneste som bruker den samme Azure-registrerte appen, for eksempel Power BI eller OneDrive. Hver bruker må vanligvis bare gjøre oppgaven én gang.

> [!NOTE]
> Hvis du er en administrator, anbefaler vi at du fullfører denne oppgaven før andre brukere. Deretter må du varsle brukere som må bruke Universell utskrift-skrivere, hvordan de gjør det. Hvis den Azure-registrerte appen for Universell utskrift krever administratorsamtykke for API-tillatelser, er det enklere hvis du gir samtykke på vegne av organisasjonen. Du kan gi administratorsamtykke fra Azure Portal eller når du kjører trinnene som følger. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### Koble til Universell utskrift for første gang

Følg disse trinnene for å koble til Universell utskrift-tjenesten for første gang.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg **Universell utskrift** > **Legg til alle Universell utskrift-skrivere** for å starte veiviseren for assistert oppsett for **Legg til Universell utskrift.skrivere** (veiviser).
3. Følg instruksjonene på skjermen til du kommer til siden for **TILLATELSER FOR MICROSOFT ENTRA-TJENESTE**.

    <!--The MICROSOFT ENTRA SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Microsoft Entra ID setup, checking your Universal Print license, and then adding the printers.-->

   ![Viser siden TILLATELSER FOR MICROSOFT ENTRA-TJENESTEN](media/azure-ad-services-permissions.png "Viser siden TILLATELSER FOR MICROSOFT ENTRA-TJENESTEN")

4. Velg koblingen **Godkjenn Azure-tjenester**.

   1. Hvis siden **Tillatelse forespurt** vises, les den nøye, og velg **Godta** for å godta og fortsette. Hvis du kjører som administrator, kan du velge **Samtykk på vegne av organisasjonen** hvis du ønsker samtykke for alle brukere.

      ![Viser siden for tillatelser for Azure-forespørsler](media/azure-ad-permissions-requested.png "Siden for tillatelser for Azure-forespørsler").

   2. Hvis du blir bedt om det, logger du deg på med brukernavn og passord.

5. Når godkjenningen er fullført, kommer du tilbake til siden **Legg til Universell utskrift-skrivere**. Velg **Neste** > **Fullfør** for å fullføre oppsettet.

Når du har lagt til en skriver, kan du vise og endre innstillingene fra siden **Utskriftsbehandling**. Det er bare å velge skriveren, og deretter velger du **Rediger skriverinnstillinger**.

Når du har fullført den innledende påloggingen, kan du bruke Universell utskrift-skriverne til å skrive ut rapporter og andre utskriftsjobber. Hvis du vil ha mer informasjon, går du til [Skriv ut en rapport](ui-work-report.md#PrintReport). Hvis du vil legge til, fjerne eller endre skrivere, går du tilbake til siden **Utskriftsbehandling** og velger **Universell utskrift**.

## Vanlige problemer og løsninger

I denne delen lærer du om de vanligste problemene som brukere kan oppleve under forsøk på å konfigurere eller bruke Universell utskrift-skrivere.

### Du har ikke tilgang til skriveren \<your-printer\>.

Hvis en bruker får denne meldingen når de prøver å skrive ut et dokument til en Universell utskrift-skriver, kan det være forårsaket av et av følgende forhold:

- Brukeren har ikke Universell utskrift lisensiert til Microsoft 365- eller Azure Active AD-konto. 
- Brukeren er ikke tildelt skriverdelingen i Universell utskrift.
- (Lokalt) Azure-appregistreringen som brukes for Universell utskrift, fungerer ikke eller er nylig endret siden forrige gang brukeren logget seg på.
- (Lokalt) Brukeren har ikke logget seg på Azure-registrert app for Universell utskrift-app og er samtykket for første gang.

## Det oppstod en feil under henting av skrivere som er delt til deg.

Hvis en bruker får denne meldingen når de prøver å legge til en Universell utskrift-skriver fra siden **Utskriftsbehandling**, er det vanligvis fordi de ennå ikke er logget på Azure-registrert app for Universell utskrift-app og er samtykket for første gang. 
<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## Neste trinn
[Konfigurer standardskrivere](ui-specify-printer-selection-reports.md).

## Se også

[Oversikt over skrivere](admin-printer-setup-overview.md)  
[Konfigurer e-postskrivere](admin-printer-setup-email.md)
[Skriv ut en rapport](ui-work-report.md#PrintReport)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kjøre kjørsler](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
