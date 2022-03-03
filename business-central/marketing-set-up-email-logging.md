---
title: Konfigurere loggføring av e-post| Microsoft Docs
description: Lær hvordan du kan gjøre om e-postinteraksjon mellom selgere og kunder til reelle salgsmuligheter.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 2abc0406fa8e86646d2382a4c7bbb1e228439728
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148411"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spor utveksling av e-postmeldinger mellom selgere og kontakter

Få mer ut av kommunikasjonen mellom selgere og de eksisterende eller potensielle kundene ved å spore e-postutvekslinger og deretter gjøre dem om til salgsmuligheter. [!INCLUDE[prod_short](includes/prod_short.md)] fungerer med Exchange Online for å føre en logg over innkommende og utgående meldinger. Du kan vise og analysere innholdet i hver enkelt melding på siden **Samhandlingsposter**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Definere fellesmapper og regler for e-postpålogging i Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Deretter kobler du [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] for å logge e-postmeldinger

Kom i gang med e-postpålogging med to enkle trinn:

1. Koble [!INCLUDE[prod_short](includes/prod_short.md)] til Exchange Online for Microsoft 365-abonnementet. Exchange Online behandler e-postmeldingene. Vi har gjort dette trinnet enkelt ved å tilby en veiledning for assistert oppsett. Du trenger bare administratorlegitimasjon for administratorkontoen i Microsoft 365. Gå til siden **Assistert oppsett** og velg deretter veiledningen **Konfigurer loggføring av e-post**.  

2. Kontroller at det er angitt gyldige e-postadresser i [!INCLUDE[prod_short](includes/prod_short.md)] for selgere og kontakter, avhengig av om de er potensielle eller eksisterende kunder. For hver kunde eller selger åpner du **Kontakt** eller **Selger/innkjøper**-kortet og ser i **E-post** -feltet.

> [!Tip]
> Når du har fullført trinnene i guiden, kan du kontrollere om tilkoblingen var vellykket. Søk etter **Markedsføringsoppsett**, og velg **Tilgang**, og velg deretter **Funksjoner** og deretter **Valider oppsett for loggføring av e-post**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Vise utvekslinger av e-postmeldinger i samhandlingsloggen

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter en post på siden **Samhandlingslogg** hver gang en selger og en kontakt utveksler en e-postmelding. Hvis du vil vise samhandlingsloggen, åpner du **Kontakter**-kortet for personen, velg **Relatert**, og deretter velger du **Logg** og **Samhandlingsposter**. Det er et par ting du kan gjøre med hver oppføring i loggen, for eksempel:

- Vis innholdet i e-postmeldingen som ble utvekslet, ved å velge **Behandle** og deretter **Vis vedlegg**.
- Gjør en e-postutveksling om til en salgsmulighet – Hvis en oppføring ser lovende ut, kan du gjøre den om til en salgsmulighet og deretter håndtere fremdriften for den mot et salg. Dette gjør du ved å velge oppføringen og deretter velge **Behandle** og deretter **Opprett salgsmulighet**. Hvis du vil ha mer informasjon, kan du se [Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>Koble lokale versjoner til Microsoft Exchange

Du kan koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Exchange lokalt eller Exchange Online for loggføring av e-post. For begge versjoner av Exchange er innstillinger for tilkoblingen tilgjengelige på siden **Markedsføringsoppsett**. For Exchange Online kan du også bruke en assistert oppsettveiledning.

### <a name="connecting-to-exchange-on-premises"></a>Koble til Exchange lokalt

For å koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Exchange lokalt kan du bruke **Grunnleggende** på **Markedsføringsoppsett**-side som **godkjenningstype**, og deretter angi legitimasjon for brukerkontoen for Exchange lokalt. Deretter aktiverer du **Aktivert**-bryteren for å starte loggføring av e-post.

### <a name="connecting-to-exchange-online"></a>Koble til Exchange Online

For å koble til Exchange Online må du bruke **OAuth2** som **godkjenningstype**. Du må også registrere et program i Azure Active Directory, og oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen som skal brukes til omdirigering. Nettadressen for omdirigering er forhåndsutfylt og skal fungere for de fleste installasjoner. Hvis du vil ha mer informasjon, kan du se Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online nedenfor.

Du må konfigurere installasjonen til å bruke HTTPS. Hvis du vil ha mer informasjon, kan du se [Konfigurere SSL for å sikre nettklienttilkoblingen for Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren slik at den har en annen hjemmeside, kan du endre nettadressen. Klienthemmeligheten vil bli lagret som en kryptert streng i databasen.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Exchange Online

Fremgangsmåten nedenfor forutsetter at du bruker Azure Active Directory til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruker Azure Active Directory, kan du se [Bruke en annen identitet og tjeneste for administrasjon av tilgang](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

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
8. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. Dette er klient-ID-en for programmet. Du må angi den på siden **Markedsføringsoppsett** i feltet **Klient-ID**, eller lagre den på en sikker lagringsplass og angi den i et hendelsesabonnent.
9. Under [!INCLUDE[prod_short](includes/prod_short.md)] kan du konfigurere loggføring av e-post på siden **Markedsføringsoppsett** eller bruke veiledningen **Assistert oppsett for loggføring av e-post** til å hjelpe deg med prosessen.
    * Angi e-postkontoen til brukeren som planlagte jobben skal koble til Exchange Online og behandle e-poster med. Brukeren må ha en gyldig lisens for Exchange Online.
    * Angi nettadressen til Exchange Online. Dette er vanligvis domenet du har angitt i brukerens e-postadresse.
    * Angi **bane for kømappe** og **bane for lagringsmappe**.
10. Aktiver **Aktivert**-bryteren for å starte loggføring av e-post.
11. Logg på med administratorkontoen din for Azure Active Directory (denne kontoen må ha en gyldig lisens for Exchange og være administrator i Exchange Online). Når du har logget på, blir du bedt om å tillate at det registrerte programmet kan logge på Exchange Online på vegne av organisasjonen. Du må gi samtykke for å fullføre oppsettet.

   > [!NOTE]
   > Hvis du ikke blir bedt om å logge på med administratorkontoen, kan det skyldes at popup-vinduer er blokkert. Hvis du vil logge på, må du tillate popup-vinduer fra https://login.microsoftonline.com.

### <a name="using-another-identity-and-access-management-service"></a>Bruke en annen identitet og tjeneste for administrasjon av tilgang
Hvis du ikke bruker Azure Active Directory til å administrere identiteter og tilgang, trenger du litt hjelp fra en utvikler. Hvis du foretrekker å lagre app-ID-en og -hemmeligheten på en annen plassering, kan du la feltene klient-ID og klienthemmelighet stå tomme og skrive en utvidelse for å hente ID-en og hemmeligheten fra plasseringen. Du kan gi hemmeligheten under kjøring ved å abonnere på hendelsene OnGetEmailLoggingClientId og OnGetEmailLoggingClientSecret i codeunit 1641, Konfig. loggføring av e-post.

### <a name="to-stop-logging-email"></a>Slik stopper du loggføring av e-post
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Markedsføringsoppsett** og velg den relaterte koblingen.
2. Deaktiver **Aktivert**-bryteren.

## <a name="see-also"></a>Se også
[Administrere forbindelser](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]