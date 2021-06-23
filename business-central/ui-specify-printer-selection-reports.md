---
title: Konfigurere skrivere
description: Lære om oppsett av skrivere du kan bruke til rapporter og dokumenter.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.date: 05/17/2021
ms.author: jswymer
ms.openlocfilehash: c98006d85607a62f99286e1179728b969fa4d005
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2021
ms.locfileid: "6063455"
---
# <a name="set-up-printers"></a>Konfigurere skrivere

Utskrift av dokumenter og rapporter fra [!INCLUDE[prod_short](includes/prod_short.md)] er en viktig oppgave for forretningsbrukere. Brukere vil vanligvis sende utskriftsjobber direkte til en av skriverne i organisasjonen uansett hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-klient eller -app de bruker. Ettersom [!INCLUDE[prod_short](includes/prod_short.md)] Online er en skytjeneste, kan den ikke kommunisere direkte med lokale skrivere som er koblet til brukernes enheter, men den kan koble til skyaktiverte skrivere.

[!INCLUDE[prod_short](includes/prod_short.md)] tilbyr følgende funksjoner for å støtte dine utskriftsbehov:

|Funksjon|Beskrivelse|Webklient| Mobilapp|App for Teams|
|-------|-----------|----------|-----------|--------------|
|Universell utskrift|Universell utskrift er en utskriftsbehandlingsløsning som er tilgjengelig som en skytjeneste fra Microsoft. Med denne funksjonen kan du konfigurere skriverne med Universell utskrift, og deretter registrere dem for bruk i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funksjonen krever abonnement på Universell utskrift og utvidelsen **Integrering med Universell utskrift**|![fungerer online](media/check.png)|![fungerer online](media/check.png)|![fungerer online](media/check.png)|
|E-postutskrift|Med denne funksjonen kan du konfigurere e-postbaserte skrivere. [!INCLUDE[prod_short](includes/prod_short.md)] sender deretter utskriftsjobber til en skriver ved å bruke e-postadressen til skriveren. Denne funksjonen krever e-postbaserte skrivere og filtypen **Send til e-post**.|![fungerer online](media/check.png)|![fungerer online](media/check.png)|![fungerer online](media/check.png)|
|Utskrift fra nettleser|Utskriftsjobber håndteres av utskriftsfunksjonaliteten i brukerens nettleser. Hvis en skyskriver ikke er installert og konfigurert, eller hvis en installert skriver mislykkes, blir utskriftsalternativene automatisk angitt for leseren. Feltet **Skriver** på forespørselssiden vil vise *(Håndteres av nettleseren)*.|![fungerer online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] støtter også egen definerte skriverinnstillinger som legger til enda flere utskriftsfunksjoner. Hvis det er installert egendefinerte skrivere, kan det derfor hende at programmet inneholder utskriftsfunksjoner som ikke er beskrevet i denne artikkelen. 

## <a name="set-up-universal-print"></a>Konfigurere Universell utskrift

Universell utskrift er en tjeneste basert på et Microsoft 365-abonnement som kjører på Microsoft Azure. Den gir deg sentralisert utskriftsbehandling via portalen for Universell utskrift. [!INCLUDE[prod_short](includes/prod_short.md)] gjør at skrivere som er konfigurert med Universell utskrift, tilgjengelige for klientbrukere via utvidelsen **Integrering med Universell utskrift**.

![Konfigurasjon av Universell utskrift](media/Universal-Print-arch.png)

Hele installasjonsprogrammet krever at du arbeider både i Microsoft Azure, ved hjelp av [Azure-portalen](https://portal.azure.com), og i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Støttede skrivere

[!INCLUDE[prod_short](includes/prod_short.md)] støtter de samme skriverne som Universell utskrift, som kan være enten kompatible eller ikke-kompatible skrivere for Universell utskrift. Ikke-kompatible skrivere kan ikke kommunisere med Universell utskrift direkte, så de krever ekstra koblingsprogramvare, som leveres av Universell utskrift. Det kan hende at enkelte eldre skrivere ikke støttes. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Forutsetninger

**For [!INCLUDE[prod_short](includes/prod_short.md)]**

- Lanseringsbølge 1 eller nyere for [!INCLUDE[prod_short](includes/prod_short.md)] 2021
- Utvidelsen **Integrering med Universell utskrift** er installert

    Denne utvidelsen publiseres og installeres som standard som en del av [!INCLUDE[prod_short](includes/prod_short.md)] Online og lokalt.  Du kan kontrollere om den er installert på siden **Administrasjon av utvidelse**. Hvis du vil ha mer informasjon, kan du se [Installere og avinstallere utvidelser i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] lokalt:
  - Azure Active Directory (AD) eller NavUserPassword-godkjenning er konfigurert
  - En applikasjon for Business Central er registrert i Azure AD-leieren og [!INCLUDE[prod_short](includes/prod_short.md)]

      På samme måte som andre Azure-tjenester som arbeider med [!INCLUDE[prod_short](includes/prod_short.md)], krever Universell utskrift en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Active Directory (Azure AD). Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Universell utskrift.

      Det kan hende at distribusjonen allerede bruker en appregistrering for andre Azure-tjenester, for eksempel Power BI. I så fall kan du også bruke den eksisterende programregistreringen for Universell utskrift, i stedet for å legge til en ny. Det eneste du trenger å gjøre, er å endre appregistreringen slik at den inneholder de relevante utskriftstillatelsene for Microsoft Graph API.

      Slik registrerer du en app som angir de riktige tillatelsene, følger du fremgangsmåten som er beskrevet i [Registrere en applikasjon i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**For Universell utskrift**

- Abonnement/lisens for Universell utskrift for organisasjonen.

    Hvis du vil ha mer informasjon, kan du se [Lisens for Universell utskrift](/universal-print/fundamentals/universal-print-license).

- Du har rollene **Utskriftsbehandling** og **Global administrator** i Azure.

    Hvis du skal administrere Universell utskrift, må kontoen din ha rollene **Utskriftsbehandling** og **Global administrator** i Azure AD. Disse rollene er bare nødvendige for administrasjon av Universell utskrift. De er ikke nødvendige for brukere å bruke skriverne fra [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Konfigurere Universell utskrift og legge til skrivere i Microsoft Azure

Før du kan begynne å administrere skrivere for Universell utskrift i Business Central, må du gå gjennom en rekke oppgaver for å få Universell utskrift til å fungere i Azure med de skriverne du vil bruke.

Hvis du vil ha detaljerte instruksjoner om hvordan du konfigurerer, kan du se [Kom i gang: konfigurer Universal utskrift](/universal-print/fundamentals/universal-print-getting-started) i dokumentasjonen for Universell utskrift. Her er en oversikt over trinnene du må fullføre. De fleste av disse trinnene gjøres i Azure-portalen.

1. Tilordne lisenser for Universell utskrift til deg selv og andre brukere.

    Hvordan du tilordner lisensen, avhenger av om du integrerer med Business Central Online eller lokalt.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] Online kan du tilordne lisenser ved hjelp av administrasjonssenteret i Microsoft 365.

      Hvis du vil ha mer informasjon, kan du se [Hjelp for administrasjonssenteret i Microsoft – Tilordne lisenser til brukere](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan du tilordne lisenser i Azure-leieren ved hjelp av Azure-portalen.

      Hvis du vil ha mer informasjon, kan du se [Azure Directory – Tilordne eller fjerne lisenser i Azure Active Directory-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installer koblingen for Universell utskrift for å registrere skrivere som ikke kan kommunisere med Universell utskrift direkte.

    De fleste skrivere som er i markedet, kan ikke kommunisere med Universell utskrift direkte. Du må installere koblingen Universell utskrift for disse skriverne. Hvis du vil ha mer informasjon, kan du se [Installere koblingen Universell utskrift](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrer skriverne i Universell utskrift.

    Når du registrerer en skriver, blir den registrert av Universell utskrift.

    - For skrivere som kan kommunisere direkte med Universell utskrift, følger du instruksjonene fra skriverprodusenten.

    - For andre skrivere kan du registrere skriverne ved å bruke koblingen Universell utskrift. 

      Hvis du vil ha mer informasjon, kan du se [Skriverregistrering](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Endre skriveregenskaper (valgfritt)

    Når en skriver er registrert, kan du vise og endre skriveregenskaper, for eksempel standardinnstillinger.

    Hvis du vil ha mer informasjon, kan du se [Administrere skriverinnstillinger ved hjelp av portalen for Universell utskrift](/universal-print/portal/configure-printer-settings).

5. Del skriverne.

    Alle skrivere du vil bruke i [!INCLUDE[prod_short](includes/prod_short.md)], må deles i Universell utskrift.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Hvis du vil ha mer informasjon, kan du se [Del en skriver](/universal-print/portal/share-printers).

6. Gi brukere tilgang til de delte skriverne.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Hvis du vil ha mer informasjon, kan du se [Skrivertillatelser](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Aktiver dokumentkonvertering.

    Universell utskrift gjengir innhold for utskrift i XPS-format. Noen eldre skrivere i markedet støtter ikke gjengivelse av XPS-innhold, i mange tilfeller bare PDF-format. Utskrift til slike skrivere vil mislykkes med mindre Universell utskrift konfigureres til å konvertere dokumenter til formatet som støttes av skriveren.

    Hvis du vil ha mer informasjon, kan du se [Oversikt over dokumentkonvertering](/universal-print/portal/document-conversion).

    > [!TIP]
    > Hvis ingen av skriverne krever format for gjengivelse av PDF-innhold, anbefales det at du ikke aktiverer dokumentkonvertering, ettersom det kan påvirke utskriftskvaliteten.

Nå er du klar til å legge til skriverne i [!INCLUDE[prod_short](includes/prod_short.md)], konfigurerer du standardskrivere for rapporter og utskrift.  

### <a name="add-universal-printer-printers-to-business-central"></a>Legge til skrivere for Universell utskrift i Business Central

Når skrivere er satt opp og delt med Universell utskrift, er du klar til å bruke dem i Business Central. Du kan legge til skrivere for Universell utskrift på to måter. Du kan legge til skriverne samtidig eller enkeltvis, én om gangen.

Når du legger til skrivere enkeltvis, kan du konfigurere den samme skriveren for Universell utskrift i Business Central mer enn én gang. Deretter kan du endre utskriftsinnstillingene, for eksempel papirskuff, størrelse og sideretning, for hver ekstra skriver. På denne måten kan du sette opp skrivere for ulike rapporter og dokumenter som har spesielle krav til utdata.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg **Universell utskrift**, og velg deretter ett av følgende alternativer:

    - **Legg til alle skrivere for Universell utskrift** for å legge til alle skrivere som ikke allerede er lagt til. Du kan bruke dette alternativet selv om skrivere allerede er lagt til. 

    - **Legg til en skriver for Universell utskrift** for å legge til en bestemt skriver.  
3. Følg instruksjonene på skjermen.

    - Hvis du velger **Legg til alle skrivere for Universell utskrift**, starter oppsettet **Legg til skrivere for Universell utskrift**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Hvis du velger **Legg til en skriver for Universell utskrift**, vises siden **Innstillinger for Universell utskrift**. Fyll ut feltet **Navn**, og velg **...** ved siden av feltet **Utskriftsdeling i Universell utskrift** for å velge skriveren for Universell utskrift. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Disse handlingene kontrollerer Azure AD-oppsettet (for lokale forekomster), kontrollerer at du har en lisens for Universell utskrift, og legger til slutt skriverne til.

    > [!NOTE]
    > For lokale forekomster vises siden TILLATELSER FOR AZURE ACTIVE DIRECTORY-TJENESTEN hvis dette er første gang du kobler til Universal utskrift, og du blir bedt om å gi samtykke til Azure-tjenester. Du trenger bare å gi samtykke én gang.

Når du har lagt til en skriver, kan du vise og endre innstillingene fra **Utskriftsbehandling**. Det er bare å velge skriveren, og deretter velger du **Rediger skriverinnstillinger**. 

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

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Konfigurere e-postutskrift

### <a name="prerequisites"></a>Forutsetninger

- Lanseringsbølge 1 eller nyere for [!INCLUDE[prod_short](includes/prod_short.md)] 2020
- Utvidelsen **Sende til e-postskriver** blir installert

    Denne utvidelsen er installert som standard. Hvis du vil ha mer informasjon om installasjon av utvidelser, kan du se 
- E-postfunksjonalitet er konfigurert.

   Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Legge til en e-postskriver

Siden **Utskriftsbehandling** viser skriverne som for øyeblikket er konfigurert. På denne siden får du også tilgang til siden **Innstillinger** for hver skriver for å redigere et eksisterende oppsett eller konfigurere en ny skriver.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg **E-postutskrift**, og velg deretter **Legg til en e-postskriver**.
3. Fyll ut de nødvendige feltene på siden **Innstillinger for e-postskriver**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du må velge riktig papirstørrelse manuelt for en skriver, ettersom ingen lokale skrivere eller brukerinnstillinger kan lagres.
    >
    > Vær oppmerksom på at utvidelsen for e-postskriver er satt til papirstørrelsen **A4** som standard, noe som for eksempel ikke passer i Nord-Amerika.

### <a name="privacy-notice"></a>Personvernerklæring

Hvis du bruker utvidelsen E-postskriver, vil alle eller enkelte utskriftsjobber bli sendt til e-postadressen du har konfigurert for skriveren. Det anbefales på det sterkeste at en unik e-post-ID knyttes til en skriverenhet med bare de offisielle tjenestene fra maskinvareprodusenten, for eksempel HP ePrint, KonicaMinolta EveryonePrint eller Epson E-Mail Printing.

Ta alle nødvendige forholdsregler for personvern, inkludert å sørge for at utskriftsløsningen for e-post har riktig konfigurerte tillatelser, personverninnstillinger og oppbevaringspolicyer. Det er ditt ansvar å oppgi en riktig, bekreftet og fungerende e-postadresse. Hvis du vil ha mer informasjon, kan du se [Personvernerklæring for Microsoft](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Konfigurere standardskrivere

Det finnes noen andre måter å konfigurere skrivere på som skal brukes som standard for utskriftsjobber. En standardskriver er nyttig hvis du arbeider med forskjellige rapporter som krever ulike skrivere på grunn av sin plassering i firmaet eller utskriftsmulighetene.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Angi en skriver som standardskriver for alle utskriftsjobber

På siden **Utskriftsbehandling** kan du konfigurere en skriver som standardskriver for alle utskriftsjobber. Du kan bare angi skriveren som standard for deg selv eller for alle brukere.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utskriftsbehandling**, og velg deretter den relaterte koblingen.

    > [!TIP]
    > Du kan også åpne siden **Utskriftsbehandling** fra siden **Skrivertvalg** ved å velge **Utskriftsbehandling**.  
2. På siden **Utskriftsbehandling** velger du en skriver fra listen, velger **Behandle**, og velger deretter **Angi som min standardskriver** eller **Angi som standardskriver for alle brukere**.

> [!NOTE]
> Når du angir en standardskriver fra **Utskriftsbehandling**, legges det til en oppføring under **Skrivervalg**.

### <a name="set-a-default-printer-for-specific-reports"></a>Angi en standardskriver for bestemte rapporter

På siden **Skrivervalg** kan du angi hvilken skriver en rapport skal bruke som standard. Standardskriveren er angitt på brukerkontobasis. Du kan angi en standardskriver for bare deg selv, en annen bruker eller alle brukere.

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan siden **Skrivervalg** bare brukes for skybaserte skrivere som er definert av skriverutvidelser, for eksempel skrivere for E-postutskrift og Universell utskrift. Den kan ikke brukes for lokale skrivere.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Skrivervalg**, og velg deretter den relaterte koblingen. Fra siden **Utskriftsbehandling** kan du i stedet velge en skriver, og deretter velger du handlingen **Skrivervalg**.
2. Velg handlingen **Ny** hvis du vil legge til et skrivervalg for en bestemt rapport.
3. Fyll ut feltene etter behov.

Den angitte rapporten er nå konfigurert slik at den skriver ut til den valgte skriveren som standard.

> [!NOTE]
> Når du skriver ut den aktuelle rapporten, kan du velge en annen skriver ved hjelp av feltet **Skriv ut** på forespørselssiden.

> [!NOTE]
> Hvis du ikke definerer en rapport for en bestemt skriver på siden **Skrivervalg**, blir den skrevet ut på standardskriveren til selskapet, som definert på siden **Utskriftsbehandling**.

Du eller administratoren kan også bruke siden **Skrivervalg** til å definere andre variasjoner av utskrift for brukere og rapporter. Tabellen nedenfor beskriver kombinasjonen av verdier for å angi et annet utskriftsoppsett for en rapport.

|Hvis du vil                                                 |Angi følgende verdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skrive ut en rapport på en bestemt skriver for alle brukere |Angi verdier i feltene **Rapport-ID** og **Skrivernavn**, og la feltet **Bruker-ID** stå tomt.|
|Skrive ut alle rapporter på en bestemt skriver til en bestemt bruker|Angi verdier i feltene **Bruker-ID** og **Skrivernavn**, og la feltet **Rapport-ID** stå tomt. Denne oppføringen gjør det samme som handlingen **Angi som min standardskriver** på siden **Utskriftsbehandling**.|
|Angi standardskriveren for alle rapporter for alle brukere|Angi en verdi i feltet **Skrivernavn**, og la feltene **Bruker-ID** og **Rapport-ID** stå tomme. Denne oppføringen gjør det samme som handlingen **Angi som standardskriver for alle brukere** på siden **Utskriftsbehandling**.|
|Skrive ut en bestemt rapport på brukerens standardskriver|Angi en verdi i feltet **Rapport-ID**, og la feltene **Skrivernavn** og **Bruker-ID** stå tomme.|
|Skrive ut en bestemt rapport på en bestemt skriver til en bestemt bruker|Angi verdier i alle tre feltene.|

> [!NOTE]
> Flere spesifikke skrivervalg har forrang over et mer generelt skrivervalg. Et skrivervalg som har verdier i feltene **Bruker-ID**, **Rapport-ID** og **Skrivernavn**, har for eksempel forrang over et skrivernavn som har tomme poster i feltene **Bruker-ID** eller **Rapport-ID**.

### <a name="sizing-print-jobs"></a>Endre størrelse på utskriftsjobber

Skyutskrifter er utformet for dokumenter med en fornuftig størrelse. De fleste skytjenester, inkludert PrintNode og HP ePrint, har en grense på 10 MB per jobb. Hvis du må skrive ut store rapporter, må du kanskje dele dem opp i flere utskrifter.

## <a name="see-also"></a>Se også

[Skrive ut en rapport](ui-work-report.md#PrintReport)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kjøre kjørsler](ui-how-run-batch-jobs.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]