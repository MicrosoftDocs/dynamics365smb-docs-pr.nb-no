---
title: Konfigurere e-post i Business Central (inneholder video)
description: 'Beskriver hvordan du kobler e-postkontoer til Business Central, slik at du kan sende utgående meldinger uten å måtte åpne en annen app.'
author: brentholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 11/22/2022
ms.author: bholtorf
---

# <a name="set-up-email"></a><a name="set-up-email"></a>Konfigurer e-post

Personer i bedrifter sender informasjon og dokumenter, for eksempel ordrer og bestillinger og fakturaer, per e-post hver dag. Administratoren kan koble en eller flere e-postkontoer til [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan sende dokumenter uten å måtte åpne en e-postapp. Du kan lage hver enkelt melding individuelt med grunnleggende formateringsverktøy, for eksempel skrifter, stiler, farger og så videre, og legge til vedlegg på opptil 100 MB. Med rapportoppsett kan administratorer ta med bare nøkkelinformasjonen fra dokumenter. Finn ut mer under [Send dokumenter i e-post](ui-how-send-documents-email.md).

E-post-funksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] er bare for utgående meldinger. Du kan ikke motta svar, det vil si at det ikke finnes noen innboksside.

> [!NOTE]
> Du kan bare bruke e-postfunksjonene til [!INCLUDE[prod_short](includes/prod_short.md)] online med Exchange Online. Vi støtter ikke hybride scenarier, for eksempel tilkobling av [!INCLUDE[prod_short](includes/prod_short.md)] online til en lokal Exchange-versjon.
>
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du opprette en appregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal før du kan konfigurere e-post. Appregistreringen gjør det mulig for [!INCLUDE[prod_short](includes/prod_short.md)] å autorisere og godkjenne e-postleverandøren. Hvis du vil ha mer informasjon, se [Konfigurere e-post for Business Central lokalt](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). I [!INCLUDE[prod_short](includes/prod_short.md)] på nett håndteres dette for deg.

## <a name="requirements"></a><a name="requirements"></a>Krav

Det er et par krav til å konfigurere og bruke e-postfunksjonene.

* Hvis du vil konfigurere e-post, må du ha tillatelsessettet **E-POSTOPPSETT**. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).
* Alle som skal bruke e-postfunksjonene, må være fullt lisensiert [!INCLUDE [prod_short](includes/prod_short.md)]. Delegerte administratorer og gjestebrukere kan for eksempel ikke bruke leierens e-postkonto.

## <a name="adding-email-accounts"></a><a name="adding-email-accounts"></a>Legge til e-postkontoer

Du legger til e-postkontoer gjennom utvidelser som gjør det mulig å koble kontoer fra ulike leverandører til [!INCLUDE[prod_short](includes/prod_short.md)]. Med standardtillegg kan du bruke kontoer fra Microsoft Exchange Online. Andre utvidelser som gjør det mulig å koble sammen kontoer fra andre leverandører, for eksempel Gmail, kan imidlertid være tilgjengelige.

Du kan angi forhåndsdefinerte forretningsscenarioer der e-postkontoen skal brukes til å sende e-postmeldinger. Du kan for eksempel angi at alle brukere sender salgsdokumenter fra en konto og kjøpsdokumenter fra en annen. Finn ut mer under [Tildel e-postscenarioer til e-postkontoer](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

Følgende tabell beskriver e-postutvidelsene som er tilgjengelige som standard.

|Utvidelse  |Beskrivelse  |Eksempler på når den kan brukes  |
|---------|---------|---------|
|**Microsoft 365-kobling**|Alle sender e-post fra en delt postboks i Exchange Online.|Når alle meldinger kommer fra samme avdeling, vil for eksempel salgsorganisasjonen sende meldinger fra en sales@cronus.com-konto. Dette alternativet krever at du konfigurerer en delt postboks i Microsoft 365-administrasjonssenteret. Se [Delte postbokser](/Exchange/collaboration/shared-mailboxes/shared-mailboxes) hvis du vil ha mer informasjon.|
|**Nåværende bruker-kobling**|Alle sender e-post fra kontoen de brukte til å logge på [!INCLUDE[prod_short](includes/prod_short.md)].|Tillat kommunikasjon fra individuelle konti.|
|**SMTP-kobling**|Bruk SMTP-protokoll til å sende e-poster.|Tillat kommunikasjon via SMTP-e-postserveren. |

> [!NOTE]
> Utvidelsene **Microsoft 365-kobling** og **Nåværende bruker-kobling** bruker de kontoene du konfigurerte for brukere i administrasjonssenteret for Microsoft 365 for Microsoft 365-abonnementet. Brukere må ha en gyldig lisens for Exchange Online for å sende e-post med utvidelsene. I tillegg krever disse utvidelsene at innstillingen **Tillat HttpClient-forespørsler** er aktivert i sandkassemiljøer. Du kan kontrollere om det er aktivert for disse utvidelsene ved å gå til siden **Utvidelsesbehandling**, velge utvidelsen og deretter velge alternativet **Konfigurer**.

> Eksterne brukere, for eksempel delegerte administratorer og eksterne regnskapsførere, kan ikke bruke disse utvidelsene til å sende e-postmeldinger fra [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="using-smtp"></a><a name="using-smtp"></a>Bruk SMTP

Hvis du vil bruke SMTP-protokollen til å sende e-postmeldinger fra [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruke SMTP-koblingsutvidelsen. Når du oppretter en konto som bruker SMTP, er feltet **Avsendertype** viktig. Hvis du velger **Spesifikk bruker**, sendes e-post ved hjelp av navnet og andre opplysninger fra kontoen du oppretter. Hvis du velger **Nåværende bruker**, sendes det imidlertid e-postmeldinger fra e-postkontoen som er angitt for hver brukers konto. Nåværende bruker ligner på Send som-funksjonen. Hvis du vil ha mer informasjon, kan du se [Bruk en erstatningsavsenderadresse i utgående e-postmeldinger](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Hvis du bruker den lokale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruke OAuth 2.0-protokollen til godkjenning. Du må opprette en appregistrering i Azure Portal og deretter kjøre veiledningen for assistert oppsett **Konfigurer Azure Active Directory** i [!INCLUDE[prod_short](includes/prod_short.md)] for å koble deg til Azure AD. Hvis du vil ha mer informasjon, kan du se [Opprette en programregistrering for Business Central i Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online avskriver bruk av enkel godkjenning for SMPT. Leiere som for øyeblikket bruker SMTP AUTH, påvirkes ikke av denne endringen. Vi anbefaler imidlertid på det sterkeste å bruke den nyeste versjonen av [!INCLUDE [prod_short](includes/prod_short.md)] og å konfigurere OAuth 2.0-godkjenning for SMTP. Vi vil ikke legge til sertifikat basert godkjenning for tidligere versjoner av [!INCLUDE [prod_short](includes/prod_short.md)], for eksempel versjon 14. Hvis du ikke kan konfigurere OAuth 2.0-godkjenning, oppfordres du til å utforske tredjepartsalternativer hvis du vil bruke SMTP-e-post i tidligere versjoner.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="add-email-accounts"></a><a name="add-email-accounts"></a>Legg til e-postkontoer

Den assisterte oppsettveiledningen **Konfigurer e-post** kan hjelpe deg raskt i gang med e-post.

> [!NOTE]
> Du må ha en standard e-postkonto selv om du bare legger til én konto. Standardkontoen blir brukt i alle e-postscenarioer som ikke er tilordnet en konto. Finn ut mer under [Tildel e-postscenarioer til e-postkontoer](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Konfigurer e-postkontoer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a><a name="assign-email-scenarios-to-email-accounts"></a>Tildel e-postscenarioer til e-postkontoer

E-postscenarioer er prosesser som omfatter sending av et dokument. Det kan for eksempel være en salgordre eller bestilling eller et varsel, for eksempel en invitasjon til en ekstern regnskapsfører. Bestemte e-postkontoer kan brukes for bestemte scenarioer. Du kan for eksempel angi at alle brukerne alltid sender salgsdokumenter fra en konto, kjøpsdokumenter fra en annen og lager- eller produksjonsdokumenter fra en tredje konto. Du kan tildele, tildele på nytt og fjerne scenarioer når du vil. Et scenario kan bare tildeles én e-postkonto om gangen. Standard e-postkonto blir brukt i alle scenarioer som ikke er tildelt en konto.

På siden **Tildeling av e-postscenario** kan du velge handlingen **Angi standardvedlegg** for å legge til vedlegg i e-postscenarioer. Vedleggene er alltid tilgjengelige når du setter en e-postmelding for et dokument som er knyttet til scenariet. Hvert e-postscenario kan ha ett eller flere standard vedlegg. Standardvedlegg legges automatisk til e-post i e-postscenarioet. Når du for eksempel sender en salgsordre per e-post, legges standardvedlegget som er angitt for salgsordrescenarioet, til. Standardvedlegg vises i **Vedlegg**-delen nederst på siden **Skriv en e-postmelding**. Du kan legge til ikke-standard vedlegg i e-posten manuelt.

<!--
## <a name="to-set-up-email"></a><a name="to-set-up-email"></a>To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a><a name="set-up-view-policies"></a>Definer visningspolicyer

Du kan kontrollere e-postmeldingene som en bruker har tilgang til, på sidene E-postutboks og Sendte e-poster.

Velg en bruker i **E-postvisningspolicyer for bruker**, og velg deretter et av følgende alternativer i feltet **E-postvisningspolicy**:

* **Vis egne e-poster** – Brukeren kan bare vise sine egne e-postmeldinger.
* **Vis alle e-poster** – Brukeren kan vise alle e-postmeldinger, inkludert e-postmeldinger som ble sendt av andre brukere.
* **Vis hvis tilgang til alle relaterte poster** – Denne visningspolicyen brukes hvis ingen annen policy er angitt. En bruker kan vise e-postmeldinger som andre brukere har sendt, hvis brukeren har tilgang til posten som ble sendt og alle relaterte poster. Eksempel: Bruker A sendte en bokført salgsfaktura til en kunde. Bruker B kan se e-postmeldingen hvis vedkommende har tilgang til både fakturaen og kunden.
* **Vis hvis tilgang til relaterte poster** – Brukeren kan vise e-postmeldinger som ble sendt av andre, hvis brukeren har tilgang til minst én post som er knyttet til posten som ble sendt. Eksempel: Bruker A sendte en bokført salgsfaktura til en kunde. Bruker B kan se e-postmeldingen hvis vedkommende har tilgang til enten fakturaen eller kunden.

> [!NOTE]
> Hvis du lar feltet **Bruker-ID** stå tomt og deretter velger handlingen **E-postvisningspolicy**, gjelder policyen du definerer alle brukerne.

## <a name="specify-how-many-messages-an-account-can-send-per-minute"></a><a name="specify-how-many-messages-an-account-can-send-per-minute"></a>Angi hvor mange meldinger en konto kan sende per minutt

Enkelte e-postleverandører (ISP-er) begrenser antall e-postmeldinger en e-postkonto kan sende samtidig, eller innenfor en viss tid, eller begge deler. *E-postbegrensing* hjelper ISP-er med å styre trafikken på serverne sine og forhindre søppelpost. Hvis en e-postkonto overskrider grensen, kan det hende at ISP-en blokkerer meldingene. Hvis du vil sikre at antall meldinger du sender fra [!INCLUDE [prod_short](includes/prod_short.md)], er i samsvar med grensen for ISP-en, angir du grensen for hver enkelt e-postkonto.

Standardgrensen for kontotypene Microsoft 365 og Nåværende bruker er 30, som tilsvarer grensen som er angitt av Exchange Online.

Det finnes to måter å angi grensen på:

* Når du bruker den assisterte oppsettveiledningen Konfigurer e-post til å opprette en ny konto, må du angi grensen i feltet **Frekvensgrense per minutt**.
* For eksisterende e-postkontoer angir du grensen i feltet **Frekvensgrense for e-post** på kontoen.

## <a name="set-up-reusable-email-texts-and-layouts"></a><a name="set-up-reusable-email-texts-and-layouts"></a>Definer gjenbrukbare e-posttekster og -oppsett

Du kan bruke rapporter til å ta med viktig informasjon fra salg, kjøp og servicedokumenter i tekster for e-poster. Rapportoppsett definerer stilen og innholdet i teksten i e-postmeldingen. Innholdet omfatter for eksempel tekst som hilsener eller instruksjoner som kommer før dokumentinformasjonen. Denne fremgangsmåten beskriver hvordan du konfigurerer rapporten **Salg – faktura** for bokførte salgsfakturaer, men prosessen er lik for andre rapporter.

> [!NOTE]
> Hvis du vil bruke oppsettet til å lage innhold i e-postmeldinger, må du bruke Word-filtypen for oppsettet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rapportvalg – salg**, og velg deretter den relaterte koblingen.
2. På siden **Rapportvalg - salg**, i **Bruk**-feltet, velger du **Faktura**.
3. På en ny linje i **-Rapport-ID**-feltet, velger du for eksempel standardrapport 1306.
4. Merk av for **Bruk for brødtekst i e-post**.
5. Velg feltet **Oppsettbeskrivelse for brødtekst i e-post**, og velg deretter et oppsett fra listen.
6. Hvis du vil vise eller redigere oppsettet som e-postteksten er basert på, velger du oppsettet på siden **Egendefinerte rapportoppsett** og velger deretter handlingen **Oppdater oppsett**. Hvis du tilpasser oppsettet, bruker du handlingen **Importer oppsett** til å laste opp det nye oppsettet.
    > [!NOTE]
    > Hvis du vil tilpasse et standardrapportoppsett, for eksempel 1306, må du lage en kopi av rapporten. Ved hjelp av [!INCLUDE [prod_short](includes/prod_short.md)] kan du lage en kopi når du importerer et egendefinert oppsett for en standardrapport. Navnet på det nye egendefinerte rapportoppsettet vil bli prefikset "kopi av".
7. Hvis du vil la kundene bruke en betalingstjeneste, for eksempel PayPal, må du definere tjenesten. Etterpå settes PayPal-informasjonen og-koblingen inn i e-postteksten. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger via PayPal](sales-how-enable-payment-service-extensions.md).
8. Velg **OK**.

Nå når du for eksempel velger **Send**-handlingen på siden **Bokført salgsfaktura**, vil brødteksten i e-posten inneholde dokumentinformasjonen fra rapport 1306 foran standardteksten i henhold til rapportoppsettet du valgte i trinn 5.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a><a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Bruk en erstatningsavsenderadresse i utgående e-postmeldinger

Hvis du bruker SMTP-koblingsutvidelsen, kan du bruke funksjonene **Send som** eller **Send på vegne** fra Microsoft Exchange til å endre avsenderadressen i utgående meldinger. [!INCLUDE[prod_short](includes/prod_short.md)] bruker SMTP-kontoen til å godkjenne til Exchange, men erstatter avsenderadressen med den du angir, eller endrer den med «på vegne av».

Når du oppretter en konto og vil bruke funksjonene Send som eller Send på vegne fra Exchange, velger du **Bestemt bruker** i feltet **Avsendertype**.

Du kan også velge **Nåværende bruker** for å tillate at brukerne sender meldinger gjennom SMTP-koblingen. Meldingen ser ut til å bli sendt fra e-postkontoen som er angitt i feltet Kontaktens e-post på brukerkortet for brukeren de er pålogget som. Den fungerer imidlertid på samme måte som Send som-funksjonen, og sendes fra kontoen som er angitt i oppsettet for SMTP-koblingen.

Følgende er eksempler på hvordan Send som og Send på vegne av brukes i [!INCLUDE[prod_short](includes/prod_short.md)]:

* Du vil kanskje at bestillinger og ordrer som du til leverandører og kunder, skal se ut som om de kommer fra en _noreply@yourcompanyname.com_-adresse.
* Når arbeidsflyten sender en godkjenningsforespørsel via e-post ved hjelp av e-postadressen til anmoderen.

> [!Note]
> Du kan bare bruke én konto til å erstatte avsenderadresser. Det vil si at du ikke kan ha én erstatningsadresse for innkjøpsprosesser og en annen for salgsprosesser.

<!--
### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a><a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a><a name="to-use-the-substitute-address-in-approval-workflows"></a>To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a><a name="set-up-document-sending-profiles"></a>Definere profiler for dokumentsending

Du kan spare tid ved å definere en foretrukket metode for å sende salgsdokumenter for hver av kundene. Du trenger ikke å velge et sende alternativ, for eksempel om dokumentet skal sendes med e-post eller som et elektronisk dokument hver gang du sender et dokument. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a><a name="optional-set-up-email-logging-in-exchange-online"></a>Valgfritt: Konfigurer loggføring av e-post i Exchange Online

Få mer ut av kommunikasjonen mellom selgere og de eksisterende eller potensielle kundene. Du kan spore e-postutvekslinger og deretter gjøre dem om til praktiske muligheter. Finn ut mer på [Spor utveksling av e-postmeldinger mellom selgere og kontakter](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="setting-up-email-for-business-central-on-premises"></a><a name="setting-up-email-for-business-central-on-premises"></a>Konfigurer e-post for Business Central lokalt

[!INCLUDE[prod_short](includes/prod_short.md)] lokalt kan integreres med tjenester som er basert på Microsoft Azure. Du kan for eksempel bruke Cortana Intelligence til smartere kontantstrømprognoser, Power BI til å visualisere bedriften din og Exchange Online til å sende e-post. Integrering med disse tjenestene er basert på en appregistrering i Azure Active Directory. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester for kommunikasjon. Hvis du vil bruke e-postfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må du registrere [!INCLUDE[prod_short](includes/prod_short.md)] som en app i Azure Portal, og deretter koble [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen. De følgende delene beskriver hvordan.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a><a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Opprett en appregistrering for Business Central i Azure Portal

Fremgangsmåten for å registrere [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Portal er beskrevet i [Registrer en app i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> For å kunne bruke e-postfunksjonen må appregistreringen bruke en flerklientskonfigurasjon.

Innstillingene som er spesifikke for e-postfunksjonen, er de delegerte tillatelsene du gir til appregistreringen. Tabellen nedenfor viser minimumstillatelsene.

|API / navn på tillatelse  |Type  |Beskrivelse  |
|---------|---------|---------|
|Microsoft Graph / User.Read |Delegert|Logg på og les brukerprofil.         |
|Microsoft Graph / Mail.ReadWrite |Delegert|Skriv e-postmeldinger.         |
|Microsoft Graph / Mail.Send|Delegert|Send e-postmeldinger.         |
|Microsoft Graph / offline_access|Delegert|Behold datatilgangssamtykke.|

Hvis du bruker SMTP-koblingen og vil bruke OAuth 2.0 til godkjenning, er tillatelsene litt forskjellige. Tabellen nedenfor viser tillatelsene.

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

Finn ut mer om generelle retningslinjer for å registrere en app under [Hurtigstart: Registrer et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Hvis du har problemer med å bruke SMTP-protokollen til å sende e-post etter at du har koblet [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen, kan det skyldes at SMTP-godkjenning ikke er aktivert for leieren din. Det anbefales at du bruker e-postkoblingene til Microsoft 365 og Gjeldende bruker i stedet, ettersom de bruker API-er for Microsoft Graph Mail. Hvis du imidlertid må bruke SMTP-protokollen, kan du aktivere SMTP-godkjenning. Hvis du vil ha mer informasjon, kan du se [Aktivere eller deaktivere SMTP-sending av godkjent klient (SMTP-godkjenning) i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect--to-your-app-registration"></a><a name="connect--to-your-app-registration"></a>Koble [!INCLUDE[prod_short](includes/prod_short.md)] til appregistreringen

Når du har registrert appen i Azure Portal, bruker du siden **AAD-registrering for e-postapp** i [!INCLUDE[prod_short](includes/prod_short.md)] til å koble [!INCLUDE[prod_short](includes/prod_short.md)] til den.

1. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **AAD-registrering for e-postapp**, og velger deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Hvis du kobler til for første gang, kan du også kjøre assistert oppsettveiledning **Konfigurer e-post**. I dette tilfellet vil også veiledningen omfatte siden AAD-registrering for e-postapp for å legge til informasjon for å koble til appregistreringen. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

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

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/set-up-email/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Delte postbokser i Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som innboks for virksomheten i Outlook](admin-outlook.md)  
[Henter [!INCLUDE[prod_short](includes/prod_short.md)] på mobilenheten min](install-mobile-app.md)
[Hente [!INCLUDE[prod_short](includes/prod_short.md)] på mobilenheten min](install-mobile-app.md)
[Analyserer e-posttelemetri (administrasjonsinnhold)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
