---
title: Konfig. loggføring av e-post
description: Lær hvordan du kan gjøre om e-postinteraksjon mellom selgere og kunder til reelle salgsmuligheter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts" />Spor utveksling av e-postmeldinger mellom selgere og kontakter

Få mer ut av kommunikasjonen mellom selgere og kundene ved å gjøre e-postutvekslinger om til salgsmuligheter. [!INCLUDE[prod_short](includes/prod_short.md)] fungerer med Exchange Online for å føre en logg over innkommende og utgående meldinger. Du kan vise og analysere innholdet i hver enkelt melding på siden **Samhandlingsposter**.

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] online må [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online være på samme leietaker.

## <a name="to-set-up-email-logging" />Konfigurer loggføring av e-post

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online" />Definer fellesmapper og regler for e-postpålogging i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Deretter kobler du [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online.

### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online" />Konfigurer en delt postboks og regler for loggføring av e-post i Exchange Online

> [!NOTE]
> Disse trinnene krever administratortilgang for Exchange Online.

Klargjør en delt postboks i administrasjonssenteret for Exchange. Alternativt kan du også bruke Exchange Online PowerShell. Hvis du vil ha mer informasjon, kan du se [Opprett en delt postboks](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Hvis du bruker Exchange Management PowerShell, er endringene tilgjengelige i administrasjonssenter for Exchange etter en forsinkelse. Forsinkelsen kan være på flere timer.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox" />Legg til en brukerkonto for medlemmer av den delte postboksen

Kontoen du skal bruke til loggføring av e-post, er en Exchange Online-konto. Den planlagte jobben bruker kontoen for å koble til den delte postboksen og behandle e-poster. Denne kontoen skal ikke knyttes til en bestemt person. Legg til e-postkontoen til medlemmene for den delte postboksen. Hvis du vil ha mer informasjon, kan du se [Bruk EAC til å redigere delt postboksdelegering](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails" />Tillat andre brukere å se loggførte e-poster

Du kan tillate at en annen bruker åpner en e-postmelding i Exchange som er knyttet til en samhandlingspost fra [!INCLUDE[prod_short](includes/prod_short.md)]. Gi brukeren ``Read``-tillatelse til **Arkiv**-mappen i den delte postboksen for å gjøre det. Se også [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) for mer informasjon.

### <a name="create-mail-flow-rules" />Opprett regler for e-postflyt

Regler for e-postflyt ser etter bestemte betingelser i meldinger og utfører handlinger på dem. Opprett to nye regler for e-postflyt basert på informasjonen i følgende tabell. Hvis du vil ha mer informasjon, kan du se [Administrer regler for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Regelhandlinger for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Formål  |Name  |Bruk denne regelen hvis ...  |Gjør følgende ...  |
|---------|---------|---------|---------|
|Regel for innkommende e-post     |Logge e-post sendt til denne organisasjonen|Avsenderen befinner seg utenfor organisasjonen, og mottakeren befinner seg i organisasjonen|Send blindkopi til e-postkontoen som er angitt for den delte postboksen.|
|Regel for utgående e-post     |Logge e-post sendt fra denne organisasjonen|Avsenderen befinner seg i organisasjonen, og mottakeren befinner seg utenfor organisasjonen.|Send blindkopi til e-postkontoen som er angitt for den delte postboksen.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandler bare meldinger i Innboks-mappen i den delte postboksen. Hvis en regel flytter meldinger fra innboksen til en annen mappe, vil ikke disse meldingene bli behandlet. I tillegg blir meldinger i Søppelpost-mappen også ignorert.

## <a name="set-up-includeprodshortincludesprodshortmd-to-log-email-messages" />Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)] for å logge e-postmeldinger

Kom i gang med e-postpålogging med to enkle trinn:

1. Koble [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online for Microsoft 365-abonnementet. Exchange Online behandler e-postmeldingene. Vi har gjort dette trinnet enkelt ved å tilby en veiledning for assistert oppsett. Du trenger bare administratorlegitimasjon for administratorkontoen i Microsoft 365. Gå til siden **Assistert oppsett** og velg deretter veiledningen **Konfigurer loggføring av e-post**.  

2. Kontroller at e-postadressene til selgerne og kontaktene i [!INCLUDE[prod_short](includes/prod_short.md)] er gyldige. For hver kunde eller selger åpner du **Kontakt** eller **Selger/innkjøper**-kortet og ser i **E-post** -feltet.

    > [!Tip]
    > Når du har fullført trinnene i guiden, kan du kontrollere om tilkoblingen var vellykket. Søk etter **Loggføring av e-post**, velg **Handlinger**, og velg deretter **Valider oppsett**.

## <a name="view-email-message-exchanges-in-the-interaction-log" />Vis utvekslinger av e-postmeldinger i samhandlingsloggen

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter en post på siden **Samhandlingslogg** hver gang en selger og en kontakt utveksler en e-postmelding. Hvis du vil vise samhandlingsloggen, åpner du **Kontakter**-kortet for personen, velg **Relatert**, og deretter velger du **Logg** og **Samhandlingsposter**. Det er et par ting du kan gjøre med hver oppføring i loggen, for eksempel:

* Vis innholdet i e-postmeldingen som ble utvekslet, ved å velge **Behandle** og deretter **Vis vedlegg**.
* Gjør en e-postutveksling om til en salgsmulighet. Hvis en oppføring ser lovende ut, kan du gjøre den om til en salgsmulighet og deretter håndtere fremdriften for den mot et salg. Hvis du vil gjøre en e-postutveksling om til en salgsmulighet, velger du posten, deretter **Prosess** og **Opprett salgsmulighet**. Hvis du vil ha mer informasjon, kan du se [Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online" />Postboks- og mappebegrensninger i Exchange Online

Det finnes postboks- og mappebegrensninger i Exchange Online, for eksempel grenser for mappestørrelser og antall meldinger. Hvis du vil ha mer informasjon, kan du se [Exchange Online-grenser](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) og [Grenser for fellesmapper i Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] lagrer loggede e-postmeldinger i en mappe i Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] lagrer også en kobling til hver loggede melding. Koblingene åpner de loggede meldingene i Exchange Online fra sidene Samhandlingsposter, Kontaktkort og Selgerkort i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis en loggført melding flyttes til en annen mappe, brytes koblingen. En melding kan for eksempel flyttes manuelt eller Exchange Online kan automatisk starte automatisk deling når lagringsgrensen er nådd.

De følgende trinnene kan hjelpe deg å unngå å bryte koblinger til meldinger i Exchange Online.

1. Ikke flytt eksisterende meldinger til en annen mappe når du har endret innstillingene for oppsett av e-postlogging. Hvis de vil beholde eksisterende meldinger, beholdes koblingene. Koblinger til meldinger i den nye mappen vil være gyldig.
2. Unngå å nå grensene for postboksen og mappen. Hvis du er i ferd med å nå en grense, gjør du følgende:
    1. Opprett en ny delt postboks i Exchange Online.
    2. Oppdater regler for e-postflyt i Exchange Online.
    3. Oppdater oppsettet for loggføring av e-post i Business Central i henhold til dette

## <a name="connect-on-premises-versions-to-microsoft-exchange" />Koble lokale versjoner til Microsoft Exchange

Du kan koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Exchange lokalt eller Exchange Online for loggføring av e-post. For begge versjoner av Exchange er innstillinger for tilkoblingen tilgjengelige på siden **Markedsføringsoppsett**. For Exchange Online kan du også bruke en assistert oppsettveiledning.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## <a name="connect-to-exchange-on-premises" />Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## <a name="connect-to-exchange-online" />Koble til Exchange Online

Du må registrere et program i Azure Active Directory for å kunne koble til Exchange Online. Oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen for registreringen. Nettadressen for omdirigering er forhåndsangitt og skal fungere for de fleste installasjoner. Hvis du vil ha mer informasjon, kan du se [Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du må også bruke **OAuth2** som **godkjenningstype**. Du må også registrere et program i Azure Active Directory. Oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen for registreringen. Nettadressen for omdirigering er forhåndsutfylt og skal fungere for de fleste installasjoner. Hvis du vil ha mer informasjon, kan du se Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online nedenfor.

Du må konfigurere installasjonen til å bruke HTTPS. Hvis du vil ha mer informasjon, kan du se [Konfigurere SSL for å sikre nettklienttilkoblingen for Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren slik at den har en annen hjemmeside, kan du endre nettadressen. Klienthemmeligheten vil bli lagret som en kryptert streng i databasen.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online" />Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online

Fremgangsmåten nedenfor forutsetter at du bruker Azure Active Directory til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

1. Velg **Godkjenning** i Azure Portal under **Behandle**.
2. Under **nettadresser for omdirigering** legger du til nettadressen for omdirigering som foreslås på siden **Loggføring av e-post** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis feltet for nettadressen for omdirigering på siden Loggføring av e-post er tom, finner du den foreslåtte nettadressen for omdirigering på siden **Assistert oppsett**. Du åpner siden ved å velge **Handlinger** og deretter **Assistert oppsett** på siden **Loggføring av e-post**.

    > [!NOTE]
    > Hvis du ikke angir en nettadresse for omdirigering, kan du gjøre det senere ved å velge **Legg til en plattform** og deretter velge **Nett** for å legge til nettprogrammet og nettadressen for omdirigering.

3. Under **Administrer** velger du **API-tillatelser**, og deretter velger du **Microsoft Graph** og velger deretter **Delegerte tillatelser**.
4. Bruk søkefeltet til å finne og velge **E-post**, og legg deretter til tillatelsen **Mail.ReadWrite.Shared**. 
5. Under **Behandle** velger du **Sertifikater og hemmeligheter**, og deretter oppretter du en ny hemmelighet for appen. Du bruker hemmeligheten i feltet **Klienthemmelighet** på siden **Loggføring av e-post** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. Dette er klient-ID-en for programmet. Du må angi den i feltet **Klient-ID** på siden **Loggføring av e-post**.
7. Under [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurere loggføring av e-post på siden **Loggføring av e-post** eller bruke veiledningen **Assistert oppsett** til å hjelpe deg.

### <a name="use-another-identity-and-access-management-service" />Bruk en annen identitet og tjeneste for administrasjon av tilgang

Hvis du ikke bruker Azure Active Directory til å administrere identiteter og tilgang, trenger du litt hjelp fra en utvikler. Hvis du foretrekker å lagre app-ID-en og -hemmeligheten på en annen plassering, kan du la feltene klient-ID og klienthemmelighet stå tomme og skrive en utvidelse for å hente ID-en og hemmeligheten fra plasseringen. Du kan gi hemmeligheten under kjøring ved å abonnere på hendelsene OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret i codeunit 1641, Konfig. loggføring av e-post.

## <a name="to-start-logging-email" />Slik starter du loggføring av e-post

1. For å starte loggføring av e-post slår du på **Aktivert**-bryteren på siden **Loggføring av e-post**.
2. Logg deg på med Exchange Online-kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster.

    > [!NOTE]
    > Hvis du ikke blir bedt om å logge deg på Exchange Online-kontoen, kan det skyldes at nettleseren blokkerer popup-vinduer. Hvis du vil logge deg på, må du tillate popup-vinduer fra https://login.microsoftonline.com.

## <a name="to-stop-logging-email" />Slik stopper du loggføring av e-post

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen.
2. Deaktiver **Aktivert**-bryteren.

## <a name="to-change-the-user-account-used-for-email-logging" />Slik endrer du brukerkontoen som brukes til loggføring av e-post

### <a name="includeprodshortincludesprodshortmd-online" />[!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Logg deg på [!INCLUDE[prod_short](includes/prod_short.md)] med kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster. Denne kontoen må ha tilgang til både [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen. 
3. Velg **Relatert**, og velg deretter **Prosjektkøpost**.
4. Start prosjektet **Loggføring av e-post** på nytt.

### <a name="includeprodshortincludesprodshortmd-on-premises" />[!INCLUDE[prod_short](includes/prod_short.md)] On-Premises

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen.
2. Velg **Handlinger**, og deretter **Forny token**.
3. Logg deg på med Exchange Online-kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster.

## <a name="see-also" />Se også
[Administrere forbindelser](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
