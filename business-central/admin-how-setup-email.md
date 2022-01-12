---
title: Konfigurere e-post i Business Central (inneholder video)
description: Beskriver hvordan du kobler e-postkontoer til Business Central, slik at du kan sende utgående meldinger uten å måtte åpne en annen app.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: ce8856f250e4098256e9ac2b9959ec6900aaaadc
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940429"
---
# <a name="set-up-email"></a>Konfigurer e-post
Personer i bedrifter sender informasjon og dokumenter, for eksempel ordrer og bestillinger og fakturaer, per e-post hver dag. Systemansvarlige kan gjøre det enklere å gjøre ved å koble én eller flere e-postkontoer til [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan sende dokumenter uten å måtte åpne en e-postapp. Du kan lage hver enkelt melding individuelt med grunnleggende formateringsverktøy, for eksempel skrifter, stiler, farger og så videre, og legge til vedlegg på opptil 100 MB. Administratorer kan også definere rapportoppsett som bare omfatter nøkkelinformasjon fra dokumenter. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).

E-post-funksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] er bare for utgående meldinger. Du kan ikke motta svar, det vil si at det ikke finnes noen innboksside i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Du kan bare bruke e-postfunksjonene til [!INCLUDE[prod_short](includes/prod_short.md)] online med Exchange Online. Vi støtter ikke hybride scenarier, for eksempel tilkobling av [!INCLUDE[prod_short](includes/prod_short.md)] online til en lokal Exchange-versjon.
> 
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du opprette en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal før du kan konfigurere e-post. Appregistreringen gjør det mulig for [!INCLUDE[prod_short](includes/prod_short.md)] å autorisere og godkjenne e-postleverandøren. Hvis du vil ha mer informasjon, se [Konfigurere e-post for Business Central lokalt](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] på nett håndteres dette for deg.

## <a name="required-permissions"></a>Nødvendige tillatelser
Hvis du vil konfigurere e-post, må du ha tillatelsessettet **E-POSTOPPSETT**. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>Legge til e-postkontoer
Du legger til e-postkontoer gjennom utvidelser som gjør det mulig å koble kontoer fra ulike leverandører til [!INCLUDE[prod_short](includes/prod_short.md)]. Med standardutvidelsene kan du bruke kontoer fra Microsoft Exchange Online, men andre utvidelser kan være tilgjengelige som lar deg koble til kontoer fra andre leverandører, for eksempel Gmail.

Når du har lagt til en e-postkonto, kan du angi forhåndsdefinerte forretningsscenarioer der kontoen skal brukes til å sende e-postmeldinger. Du kan for eksempel angi at alle brukere sender salgsdokumenter fra en konto og kjøpsdokumenter fra en annen. Hvis du vil ha mer informasjon, kan du se [Tilordne e-postscenarioer til e-postkontoer](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Følgende tabell beskriver e-postutvidelsene som er tilgjengelige som standard.

|Utvidelse  |Beskrivelse  |Eksempler på når den kan brukes  |
|---------|---------|---------|
|**Microsoft 365**|Alle sender e-post fra en delt postboks i Exchange Online.|Når alle meldinger kommer fra samme avdeling, vil for eksempel salgsorganisasjonen sende meldinger fra en sales@cronus.com-konto. Dette krever at du konfigurerer en delt postboks i administrasjonssenteret i Microsoft 365. Se [Delte postbokser](/Exchange/collaboration/shared-mailboxes/shared-mailboxes) hvis du vil ha mer informasjon.|
|**Gjeldende bruker**|Alle sender e-post fra kontoen de brukte til å logge på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillat kommunikasjon fra individuelle konti.|
|**Andre (SMTP)**|Bruk SMTP-protokoll til å sende e-poster.|Tillat kommunikasjon via SMTP-e-postserveren. |

> [!NOTE]
> Utvidelsene **Microsoft 365** og **Gjeldende bruker** bruker de kontiene du konfigurerte for brukere i administrasjonssenteret for Microsoft 365 for Microsoft 365-abonnementet. Brukere må ha en gyldig lisens for Exchange Online for å sende e-post med utvidelsene. 
>
> I tillegg kan ikke eksterne brukere, for eksempel delegerte administratorer og eksterne regnskapsførere, bruke disse utvidelsene til å sende e-postmeldinger fra [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Gamle SMTP-innstillinger og utvidelsen E-post – SMTP-tilkobling
Hvis du allerede bruker [!INCLUDE[prod_short](includes/prod_short.md)] og har konfigurert e-post gjennom det gamle SMTP-oppsettet, kan du fortsette å bruke installasjonsprogrammet parallelt utvidelsen E-post – SMTP-tilkobling. Når vi oppdaterer [!INCLUDE[prod_short](includes/prod_short.md)] til neste versjon, kopierer vi de gamle SMTP-innstillingene til utvidelsen E-post – SMTP-tilkobling. Når den er klar, kan systemansvarlig aktivere de forbedrede e-postegenskapene, og du kan begynne å bruke utvidelsen E-post – SMTP-tilkobling. Hvis du vil ha mer informasjon, kan du se [Om funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management#about-feature-management). Det er imidlertid ingen synkronisering mellom utvidelsen SMTP-tilkobling og de gamle innstillingene. Hvis du endrer SMTP-innstillingene i utvidelsen, må du gjøre de samme endringene i det gamle SMTP-oppsettet, eller omvendt.

> [!NOTE]
> Hvis du har tilpasninger som er avhengige av det gamle oppsettet for SMTP-e-post, er det en mulighet for at noe går galt med tilpasningene dine hvis du begynner å bruke e-postutvidelser. Vi anbefaler at du konfigurerer og tester utvidelsene før du aktiverer funksjonen for forbedrede e-postfunksjoner.

> [!IMPORTANT]
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, kan du bruke OAuth 2.0 til godkjenning, men du må opprette en programregistrering i Azure-portalen, og deretter kjører du den assisterte oppsettsveiledningen **Konfigurer Azure Active Directory** i [!INCLUDE[prod_short](includes/prod_short.md)] for å koble til Azure AD. Hvis du vil ha mer informasjon, kan du se [Opprette en programregistrering for Business Central i Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>Legg til e-postkontoer
Den assisterte oppsettveiledningen **Konfigurer e-post** kan hjelpe deg raskt i gang med e-post.

> [!NOTE]
> Du må ha en standard e-postkonto selv om du bare legger til én konto. Standardkontoen blir brukt i alle e-postscenarioer som ikke er tilordnet en konto. Hvis du vil ha mer informasjon, kan du se [Tilordne e-postscenarioer til e-postkontoer](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Konfigurer e-postkontoer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Tilordne e-postscenarier til e-postkontoer
E-postscenarioer er prosesser som omfatter sending av et dokument, for eksempel en ordre eller bestilling, eller en varsling, for eksempel en invitasjon til en ekstern regnskapsfører. Du kan bruke bestemte e-postkontoer for bestemte scenarioer. Du kan for eksempel angi at alle brukerne alltid sender salgsdokumenter fra en konto, kjøpsdokumenter fra en annen og lager- eller produksjonsdokumenter fra en tredje konto. Du kan tilordne, tilordne på nytt og fjerne scenarioer når du måtte ønske det, men du kan bare tilordne et scenario til én e-postkonto om gangen. Standard e-postkonto blir brukt i alle scenarioer som ikke er tilordnet en konto.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Konfigurer gjenbrukbare e-posttekster og -oppsett for salgs- og kjøpsdokumenter
Du kan bruke rapporter til å ta med viktig informasjon fra salgs- og kjøpsdokumenter i tekster for e-poster. Denne fremgangsmåten beskriver hvordan du konfigurerer rapporten **Salg – faktura** for bokførte salgsfakturaer, men prosessen er lik for andre rapporter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rapportvalg – salg**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - salg**, i **Bruk**-feltet, velger du **Faktura**.
3. På en ny linje i **-Rapport-ID**-feltet, velger du for eksempel standardrapport 1306.
4. Merk av for **Bruk for brødtekst i e-post**.
5. Velg feltet **Oppsettbeskrivelse for brødtekst i e-post**, og velg deretter et oppsett fra listen.

    Rapportoppsett definerer stilen og innholdet i selve teksten i e-posten, inkludert tekster som en hilsen eller instruksjoner som kommer foran dokumentinformasjonen. Hvis organisasjonen din har mange oppsett, kan du vise alle tilgjengelige rapportoppsett hvis du velger **Velg fra hele listen**.
6. Hvis du vil vise eller redigere oppsettet som teksten i e-post er basert på, velger du oppsettet på siden **Egendefinerte rapportoppsett** og velger deretter handlingen **Oppdater oppsett**.
7. Hvis du vil tilby kundene å betale for salg med elektroniske, kan du konfigurere de relaterte betalingstjenestene, for eksempel PayPal, og deretter sette inn PayPal-informasjonen og -koblingen i teksten i e-posten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Velg **OK**.

Nå når du for eksempel velger **Send**-handlingen på siden **Bokført salgsfaktura**, vil brødteksten i e-posten inneholde dokumentinformasjonen fra rapport 1306 foran standardteksten i henhold til rapportoppsettet du valgte i trinn 5.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Bruke en erstatningsavsenderadresse i utgående e-postmeldinger
Hvis du bruker de gamle SMTP-innstillingene, kan du bruke funksjonene **Send som** eller **Send på vegne** fra Microsoft Exchange til å endre avsenderadressen i utgående meldinger. [!INCLUDE[prod_short](includes/prod_short.md)] bruker SMTP-kontoen til å godkjenne til Exchange, men erstatter avsenderadressen med den du angir, eller endrer den med «på vegne av».

Følgende er eksempler på hvordan Send som og Send på vegne av brukes i [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Når du sender dokumenter som for eksempel bestillinger eller ordrer til leverandører og kunder, vil du kanskje at de skal se ut som om de kommer fra en _ikkesvar@dittselskapsnavn.com_-adresse.
 * Når arbeidsflyten sender en godkjenningsforespørsel via e-post ved hjelp av e-postadressen til anmoderen.

> [!Note]
> Du kan bare bruke én konto til å erstatte avsenderadresser. Det vil si at du ikke kan ha én erstatningsadresse for innkjøpsprosesser og en annen for salgsprosesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Sette opp erstatningsavsenderadresse for alle utgående e-postmeldinger
1. I **Administrasjonssenter for Exchange** for Microsoft 365-kontoen finner du e-postboksen som skal brukes som erstatningsadresse, og deretter kopierer eller noterer du adressen. Hvis du trenger en ny adresse, går du til administrasjonssenteret for Microsoft 365 for å opprette en ny bruker og konfigurere postboksen.
2. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for SMTP-e-post**, og velg deretter den relaterte koblingen.
3. I **Send som**-feltet angir du erstatningsadressen.
4. Kopier eller noter adressen i feltet **Bruker-ID**.
5. I **Administrasjonssenter for Exchange** finner du postboksen som skal brukes som erstatningsadresse, og deretter angir du adressen fra **Bruker-ID**-feltet i **Send som**-feltet. Hvis du vil ha mer informasjon, kan du se [Bruk EAC til å tilordne tillatelser til individuelle postbokser](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Slik bruker du erstatningsadressen i arbeidsflyter for godkjenning
1. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for SMTP-e-post**, og velg deretter den relaterte koblingen.
2. Kopier eller noter adressen i feltet **Bruker-ID**.
3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.
4. I **Administrasjonssenter for Exchange** finner du postboksene for hver bruker i **Brukeroppsett for godkjenning**, og i feltet **Send som** angir du adressen fra feltet **Bruker-ID** fra siden **Oppsett for SMTP-e-post** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Administrer tillatelser for mottakere](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Oppsett for SMTP-e-post**, og velg deretter den relaterte koblingen.
6. For å aktivere erstatning slår du på aktivering/deaktivering av **Tillat avsendererstatning**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] vil avgjøre hvilken adresse som skal vises i følgende rekkefølge: <br><br> 1. Adressen som er angitt i feltet **E-post** på siden **Brukeroppsett for godkjenning** for meldinger i en arbeidsflyt. <br> 2. Adressen som er angitt i **Send som**-feltet på siden **Oppsett for SMTP-e-post**. <br> 3. Adressen som er angitt i **Bruker-ID**-feltet på siden **Oppsett for SMTP-e-post**.

## <a name="set-up-document-sending-profiles"></a>Definere en profil for dokumentsending
Du kan definere en foretrukket metode for å sende salgsdokumenter for hver av kundene, slik at du ikke trenger å velge et sendealternativ, for eksempel om du skal sende dokumentet via e-post eller som et elektronisk dokument hver gang du sender et dokument. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Definere fellesmapper og regler for e-postpålogging i Exchange Online
Få mer ut av kommunikasjonen mellom selgere og de eksisterende eller potensielle kundene ved å spore e-postutvekslinger og deretter gjøre dem om til salgsmuligheter. Hvis du vil ha mer informasjon, kan du se [Spore utveksling av e-postmeldinger mellom selgere og kontakter](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Deretter kobler du [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online. Hvis du vil ha mer informasjon, kan du se [Spore utveksling av e-postmeldinger mellom selgere og kontakter](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Konfigurere e-post for Business Central lokalt 
[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreres med tjenester som er basert på Microsoft Azure. Du kan for eksempel bruke Cortana Intelligence til smartere kontantstrømprognoser, Power BI til å visualisere bedriften din og Exchange Online til å sende e-post. Integrering med disse tjenestene er basert på en appregistrering i Azure Active Directory. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester for kommunikasjon. Hvis du vil bruke e-postfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du registrere [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure Portal, og deretter koble [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen. De følgende delene beskriver hvordan.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Opprette en programregistrering for Business Central i Azure Portal
Fremgangsmåten for å registrere [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal er beskrevet i [Registrer en app i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Innstillingene som er spesifikke for e-postfunksjonen, er de delegerte tillatelsene du gir til appregistreringen. Tabellen nedenfor viser minimumstillatelsene.

|API / navn på tillatelse  |Type  |Beskrivelse  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegert|Logg på og les brukerprofil.         |
|Microsoft Graph / Mail.ReadWrite |Delegert|Skriv e-postmeldinger.         |
|Microsoft Graph / Mail.Send|Delegert|Send e-postmeldinger.         |
|Microsoft Graph / offline_access|Delegert|Behold datatilgangssamtykke.|

Hvis du bruker et gammelt SMTP-oppsett eller SMTP-kontakten og vil bruke OAuth til godkjenning, er tillatelsene litt forskjellige. Tabellen nedenfor viser tillatelsene.

|API / navn på tillatelse  |Type  |Beskrivelse  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Delegert|Behold datatilgangssamtykke.|
|Microsoft Graph / openid|Delegert|Logger brukere på.|
|Microsoft Graph / User.Read |Delegert|Logg på og les brukerprofil.         |
|Microsoft Graph / SMTP.Send|Delegert|Sender e-postmeldinger fra postbokser ved hjelp av SMTP-godkjenning.         |
|Office 365 Exchange Online / User.Read |Delegert|Logger på og leser brukerprofil.         |

Når du oppretter appregistreringen, må du skrive ned følgende informasjon. Du trenger den for å koble [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen.
 
* App-ID (klient) 
* URI-adresse for omdirigering (valgfritt)
* Klienthemmelighet

Hvis du se generelle retningslinjer for å registrere en app, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Hvis du har problemer med å bruke det gamle SMTP-oppsettet til å sende e-post etter at du har koblet [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen, kan det skyldes at SMTP-godkjenning ikke er aktivert for leieren din. Det anbefales at du bruker e-postkoblingene til Microsoft 365 og Gjeldende bruker i stedet, ettersom de bruker APIer for Microsoft Graph Mail. Hvis du imidlertid må bruke SMTP-oppsettet, kan du aktivere SMTP-godkjenning. Hvis du vil ha mer informasjon, kan du se [Aktivere eller deaktivere SMTP-sending av godkjent klient (SMTP-godkjenning) i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>Koble [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen
Når du har registrert appen i Azure Portal, bruker du assistert oppsettveiledning **AAD-registrering for e-postapp** i [!INCLUDE[prod_short](includes/prod_short.md)] til å koble [!INCLUDE[prod_short](includes/prod_short.md)] til den.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **AAD-registrering for e-postapp**, og velger deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du kobler til for første gang, kan du også kjøre assistert oppsettveiledning **Konfigurer e-post**. Veiledningen krever informasjon for å koble til appregistreringen. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Se også

[Delte postbokser i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som innboks for virksomheten i Outlook](admin-outlook.md)  
[Henter [!INCLUDE[prod_short](includes/prod_short.md)] på mobilenheten min](install-mobile-app.md)
[Hente [!INCLUDE[prod_short](includes/prod_short.md)] på mobilenheten min](install-mobile-app.md)
[Analyserer e-posttelemetri (administrasjonsinnhold)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
