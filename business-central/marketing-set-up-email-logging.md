---
title: Konfig. loggføring av e-post
description: Lær hvordan du kan gjøre om e-postinteraksjon mellom selgere og kunder til reelle salgsmuligheter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 03/22/2022
ms.search.form: 1680, 1811, 5076
ms.author: bholtorf
ms.openlocfilehash: fc755362a5b29cca9eb8e8e403374e173cff3630
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516138"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spor utveksling av e-postmeldinger mellom selgere og kontakter
Få mer ut av kommunikasjonen mellom selgere og kundene ved å gjøre e-postutvekslinger om til salgsmuligheter. [!INCLUDE[prod_short](includes/prod_short.md)] fungerer med Exchange Online for å føre en logg over innkommende og utgående meldinger. Du kan vise og analysere innholdet i hver enkelt melding på siden **Samhandlingsposter**.

> [!NOTE]
> I 2022 lanseringsbølge 1 har vi strømlinjeformede prosesser for å konfigurere loggføring av e-post for å øke fleksibiliteten og sikkerheten. Hvis du er en ny kunde som bruker denne versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Loggføring av e-post med Microsoft Graph-API** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] online krever den nye opplevelsen at [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online er på samme leietaker.

## <a name="to-set-up-email-logging"></a>Konfigurer loggføring av e-post
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Loggføring av e-post med Microsoft Graph-API**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen **Gjeldende opplevelse**.

## <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience)

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Definere fellesmapper og regler for e-postpålogging i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Deretter kobler du [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online.

## <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online"></a>Konfigurer en delt postboks for loggføring av e-post i Exchange Online

> [!NOTE]
> Disse trinnene krever administratortilgang for Exchange Online.

Klargjør en delt postboks i administrasjonssenteret for Exchange. Alternativt kan du også bruke Exchange Online PowerShell. Hvis du vil ha mer informasjon, kan du se [Opprett en delt postboks](/microsoft-365/admin/email/create-a-shared-mailbox) eller [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Hvis du bruker Exchange Management PowerShell, er endringene tilgjengelige i administrasjonssenter for Exchange etter en forsinkelse. Forsinkelsen kan være på flere timer.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox"></a>Legg til en brukerkonto for medlemmer av den delte postboksen
Kontoen du skal bruke til loggføring av e-post, er en Exchange Online-konto. Den planlagte jobben bruker kontoen for å koble til den delte postboksen og behandle e-poster. Denne kontoen skal ikke knyttes til en bestemt person. Legg til e-postkontoen til medlemmene for den delte postboksen. Hvis du vil ha mer informasjon, kan du se [Bruk EAC til å redigere delt postboksdelegering](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails"></a>Tillat andre brukere å se loggførte e-poster
Du kan tillate at en annen bruker åpner en e-postmelding i Exchange som er knyttet til en samhandlingspost fra [!INCLUDE[prod_short](includes/prod_short.md)]. Gi brukeren ``Read``-tillatelse til **Arkiv**-mappen i den delte postboksen for å gjøre det. Se også [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) for mer informasjon.

### <a name="create-mail-flow-rules"></a>Opprett regler for e-postflyt
Regler for e-postflyt ser etter bestemte betingelser i meldinger og utfører handlinger på dem. Opprett to nye regler for e-postflyt basert på informasjonen i følgende tabell. Hvis du vil ha mer informasjon, kan du se [Administrer regler for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Regelhandlinger for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Formål  |Name  |Bruk denne regelen hvis ...  |Gjør følgende ...  |
|---------|---------|---------|---------|
|Regel for innkommende e-post     |Logge e-post sendt til denne organisasjonen|Avsenderen befinner seg utenfor organisasjonen, og mottakeren befinner seg i organisasjonen|Send blindkopi til e-postkontoen som er angitt for den delte postboksen.|
|Regel for utgående e-post     |Logge e-post sendt fra denne organisasjonen|Avsenderen befinner seg i organisasjonen, og mottakeren befinner seg utenfor organisasjonen.|Send blindkopi til e-postkontoen som er angitt for den delte postboksen.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] behandler bare meldinger i Innboks-mappen i den delte postboksen. Hvis en regel flytter meldinger fra innboksen til en annen mappe, vil ikke disse meldingene bli behandlet. I tillegg blir meldinger i Søppelpost-mappen også ignorert. 

---

## <a name="setting-up-prod_short-to-log-email-messages"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] for å logge e-postmeldinger
Disse trinnene er like for både gjeldende og nye opplevelser.

Kom i gang med e-postpålogging med to enkle trinn:

1. Koble [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online for Microsoft 365-abonnementet. Exchange Online behandler e-postmeldingene. Vi har gjort dette trinnet enkelt ved å tilby en veiledning for assistert oppsett. Du trenger bare administratorlegitimasjon for administratorkontoen i Microsoft 365. Gå til siden **Assistert oppsett** og velg deretter veiledningen **Konfigurer loggføring av e-post**.  

2. Kontroller at e-postadressene til selgerne og kontaktene i [!INCLUDE[prod_short](includes/prod_short.md)] er gyldige. For hver kunde eller selger åpner du **Kontakt** eller **Selger/innkjøper**-kortet og ser i **E-post** -feltet.

> [!Tip]
> Når du har fullført trinnene i guiden, kan du kontrollere om tilkoblingen var vellykket. Avhengig av om du bruker gjeldende eller ny opplevelse, gjør du ett av følgende: 
>
> * **Gjeldende opplevelse:** Søk etter **Markedsføringsoppsett**, og velg **Tilgang**, og velg deretter **Funksjoner** og deretter **Valider oppsett for loggføring av e-post**.
> * **Ny opplevelse**: Søk etter **Loggføring av e-post**, velg **Handlinger**, og velg deretter **Valider oppsett**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Vise utvekslinger av e-postmeldinger i samhandlingsloggen

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter en post på siden **Samhandlingslogg** hver gang en selger og en kontakt utveksler en e-postmelding. Hvis du vil vise samhandlingsloggen, åpner du **Kontakter**-kortet for personen, velg **Relatert**, og deretter velger du **Logg** og **Samhandlingsposter**. Det er et par ting du kan gjøre med hver oppføring i loggen, for eksempel:

- Vis innholdet i e-postmeldingen som ble utvekslet, ved å velge **Behandle** og deretter **Vis vedlegg**.
- Gjør en e-postutveksling om til en salgsmulighet. Hvis en oppføring ser lovende ut, kan du gjøre den om til en salgsmulighet og deretter håndtere fremdriften for den mot et salg. Hvis du vil gjøre en e-postutveksling om til en salgsmulighet, velger du posten, deretter **Prosess** og **Opprett salgsmulighet**. Hvis du vil ha mer informasjon, kan du se [Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Koble lokale versjoner til Microsoft Exchange

Du kan koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Exchange lokalt eller Exchange Online for loggføring av e-post. For begge versjoner av Exchange er innstillinger for tilkoblingen tilgjengelige på siden **Markedsføringsoppsett**. For Exchange Online kan du også bruke en assistert oppsettveiledning.

> [!IMPORTANT]
> Den nye opplevelsen støtter ikke tilkobling til Exchange on-Premises. Hvis du må bruke Exchange on-premises, må du ikke aktivere funksjonsoppdateringen for den nye opplevelsen.

## <a name="connecting-to-exchange-on-premises"></a>Koble til Exchange On-Premises
## <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience)
For å koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Exchange lokalt kan du bruke **Grunnleggende** på **Markedsføringsoppsett**-side som **godkjenningstype**, og deretter angi legitimasjon for brukerkontoen for Exchange lokalt. Deretter aktiverer du **Aktivert**-bryteren for å starte loggføring av e-post.

## <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
Den nye opplevelsen støtter ikke tilkoblinger til Exchange on-premises.

---

## <a name="connecting-to-exchange-online"></a>Koble til Exchange Online
Du må registrere et program i Azure Active Directory for å kunne koble til Exchange Online. Oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen for registreringen. Nettadressen for omdirigering er forhåndsangitt og skal fungere for de fleste installasjoner. Hvis du vil ha mer informasjon, kan du se [Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Du må også bruke **OAuth2** som **godkjenningstype**. Du må også registrere et program i Azure Active Directory. Oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen for registreringen. Nettadressen for omdirigering er forhåndsutfylt og skal fungere for de fleste installasjoner. Hvis du vil ha mer informasjon, kan du se Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online nedenfor.

Du må konfigurere installasjonen til å bruke HTTPS. Hvis du vil ha mer informasjon, kan du se [Konfigurere SSL for å sikre nettklienttilkoblingen for Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren slik at den har en annen hjemmeside, kan du endre nettadressen. Klienthemmeligheten vil bli lagret som en kryptert streng i databasen.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online
Fremgangsmåten nedenfor forutsetter at du bruker Azure Active Directory til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

## <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience) 
Fremgangsmåten nedenfor forutsetter at du bruker Azure Active Directory til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruker Azure Active Directory, kan du se [Bruk en annen identitet og tjeneste for administrasjon av tilgang](marketing-set-up-email-logging.md#use-another-identity-and-access-management-service). 

1. Velg **Godkjenning** i Azure Portal under **Behandle**.
2. Under **nettadresser for omdirigering** legger du til nettadressen for omdirigering som foreslås på siden **Markedsføringsoppsett** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis nettadressen for omdirigering på siden Markedsføringsoppsett er tom, finner du den foreslåtte nettadressen for omdirigering på siden **Assistert oppsett for loggføring av e-post**.

    > [!NOTE]
    > Hvis du ikke angir en nettadresse for omdirigering, kan du gjøre det senere ved å velge **Legg til en plattform** og deretter velge **Nett** for å legge til nettprogrammet og nettadressen for omdirigering. 

3. Velg **Manifest** under **Behandle**.
4. Finn **requiredResourceAccess**-egenskapen i manifestet, og legg til følgende kode i hakeparentesene ([]) for å legge til de nødvendige tillatelsene. Hvis du vil ha mer informasjon, kan du se [Registrer programmet](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application).

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Velg **Lagre**.
6. Under **Behandle** velger du **API-tillatelser**, og deretter kontrollerer du at følgende tillatelser er oppført:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Under **Behandle** velger du **Sertifikater og hemmeligheter**, og deretter oppretter du en ny hemmelighet for appen. Du bruker hemmeligheten enten i [!INCLUDE[prod_short](includes/prod_short.md)], i **Klienthemmelighet**-feltet på siden **Markedsføringsoppsett**, eller lagrer den på en sikker lagringsplass og angir den i et hendelsesabonnent.
8. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. **Program-ID (klient)**-verdien er klient-ID-en til programmet. Du må angi klient-ID-en på siden **Markedsføringsoppsett** i feltet **Klient-ID**, eller lagre den på en sikker lagringsplass og angi den i et hendelsesabonnent.
9. Under [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurere loggføring av e-post på siden **Markedsføringsoppsett** eller bruke veiledningen **Assistert oppsett for loggføring av e-post** til å hjelpe deg med prosessen.
    * Angi e-postkontoen til brukeren som planlagte jobben skal koble til Exchange Online og behandle e-poster med. Brukeren må ha en gyldig lisens for Exchange Online.
    * Angi nettadressen til Exchange Online. Dette er vanligvis nettadressen du har angitt i brukerens e-postadresse.
    * Angi **bane for kømappe** og **bane for lagringsmappe**.
10. Aktiver **Aktivert**-bryteren for å starte loggføring av e-post.
11. Logg på med administratorkontoen din for Azure Active Directory (denne kontoen må ha en gyldig lisens for Exchange og være administrator i Exchange Online). Når du har logget på, må du tillate at det registrerte programmet kan logge på Exchange Online på vegne av organisasjonen. Du må gi samtykke for å fullføre oppsettet.

   > [!NOTE]
   > Hvis du ikke blir bedt om å logge på med administratorkontoen, kan det skyldes at popup-vinduer er blokkert. Hvis du vil logge på, må du tillate popup-vinduer fra https://login.microsoftonline.com.

## <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
1. Velg **Godkjenning** i Azure Portal under **Behandle**.
2. Under **nettadresser for omdirigering** legger du til nettadressen for omdirigering som foreslås på siden **Loggføring av e-post** i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis feltet for nettadressen for omdirigering på siden Loggføring av e-post er tom, finner du den foreslåtte nettadressen for omdirigering på siden **Assistert oppsett**. Du åpner siden ved å velge **Handlinger** og deretter **Assistert oppsett** på siden **Loggføring av e-post**.

    > [!NOTE]
    > Hvis du ikke angir en nettadresse for omdirigering, kan du gjøre det senere ved å velge **Legg til en plattform** og deretter velge **Nett** for å legge til nettprogrammet og nettadressen for omdirigering.

3. Under **Administrer** velger du **API-tillatelser**, og deretter velger du **Microsoft Graph** og velger deretter **Delegerte tillatelser**.
4. Bruk søkefeltet til å finne og velge **E-post**, og legg deretter til tillatelsen **Mail.ReadWrite.Shared**. 
5. Under **Behandle** velger du **Sertifikater og hemmeligheter**, og deretter oppretter du en ny hemmelighet for appen. Du bruker hemmeligheten i feltet **Klienthemmelighet** på siden **Loggføring av e-post** i [!INCLUDE[prod_short](includes/prod_short.md)].
6. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. Dette er klient-ID-en for programmet. Du må angi den i feltet **Klient-ID** på siden **Loggføring av e-post**.
7. Under [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurere loggføring av e-post på siden **Loggføring av e-post** eller bruke veiledningen **Assistert oppsett** til å hjelpe deg.

### <a name="use-another-identity-and-access-management-service"></a>Bruk en annen identitet og tjeneste for administrasjon av tilgang
Hvis du ikke bruker Azure Active Directory til å administrere identiteter og tilgang, trenger du litt hjelp fra en utvikler. Hvis du foretrekker å lagre app-ID-en og -hemmeligheten på en annen plassering, kan du la feltene klient-ID og klienthemmelighet stå tomme og skrive en utvidelse for å hente ID-en og hemmeligheten fra plasseringen. Du kan gi hemmeligheten under kjøring ved å abonnere på hendelsene OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret i codeunit 1641, Konfig. loggføring av e-post.

---

## <a name="to-start-logging-email"></a>Slik starter du loggføring av e-post
1. For å starte loggføring av e-post slår du på **Aktivert**-bryteren på siden **Loggføring av e-post**.
2. Logg deg på med Exchange Online-kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster.

    > [!NOTE]
    > Hvis du ikke blir bedt om å logge deg på Exchange Online-kontoen, kan det skyldes at nettleseren blokkerer popup-vinduer. Hvis du vil logge deg på, må du tillate popup-vinduer fra https://login.microsoftonline.com.

## <a name="to-stop-logging-email"></a>Slik stopper du loggføring av e-post
## <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience)
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Markedsføringsoppsett** og velg den relaterte koblingen.
1. Deaktiver **Aktivert**-bryteren.

## <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen.
2. Deaktiver **Aktivert**-bryteren.

---

## <a name="to-change-the-user-account-used-for-email-logging"></a>Slik endrer du brukerkontoen som brukes til loggføring av e-post
Hvis du bruker den nye opplevelsen, kan du endre brukerkontoen som brukes til loggføring av e-post. Gjeldende opplevelse støtter ikke dette.

## <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience) 
Deaktiver gjeldende oppsett, endre brukeren på siden for **Loggføring av e-post**, og aktiver deretter loggføring av e-post på nytt. Du kan også kjøre den assisterte oppsettveiledningen på nytt.

## <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
### <a name="prod_short-online"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Online
1. Logg deg på [!INCLUDE[prod_short](includes/prod_short.md)] med kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster. Denne kontoen må ha tilgang til både [!INCLUDE[prod_short](includes/prod_short.md)] og Exchange Online.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen. 
3. Velg **Relatert**, og velg deretter **Prosjektkøpost**.
4. Start prosjektet **Loggføring av e-post** på nytt.

### <a name="prod_short-on-premises"></a>[!INCLUDE[prod_short](includes/prod_short.md)] On-Premises
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Loggføring av e-post**, og velg deretter den relaterte koblingen. 
2. Velg **Handlinger**, og deretter **Forny token**.
3. Logg deg på med Exchange Online-kontoen som den planlagte jobben skal bruke til å koble til den delte postboksen og behandle e-poster.

## <a name="see-also"></a>Se også
[Administrere forbindelser](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]