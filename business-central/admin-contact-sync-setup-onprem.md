---
title: Konfigurer kontaktsynkronisering med Outlook for Business Central lokalt
description: Lær hvordan du konfigurerer et lokalt Business Central-miljø for å synkronisere kontakter i Business Central og Outlook.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-op
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
---

# <a name="set-up-contact-sync-with-outlook-for-business-central-on-premises"></a>Konfigurer kontaktsynkronisering med Outlook for Business Central lokalt

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I denne artikkelen lærer du hvordan du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokal for å synkronisere kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] med kontakter i Outlook. Hvis du vil ha mer informasjon om dette, kan du gå til [Synkroniser kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## <a name="introduction"></a>Introduksjon

Kontaktsynkronisering krever bruk av OAuth 2.0-protokollen for godkjenning med Exchange Online. Tidligere ble enkel godkjenning også støttet, men den er avskrevet og støttes ikke lenger med Exchange Online. Du kan lese mer om avskrivingen ved [Avskriving av enkelt godkjenning i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Denne endringen betyr at kontaktsynkronisering i Business Central kan ha sluttet å virke i det lokale miljøet. Denne artikkelen forklarer hvordan du får det til å fungere igjen.

## <a name="prerequisites"></a>Forutsetninger

- Exchange Online, enten en frittstående versjon eller gjennom Microsoft 365-planen  
- Tilgang til Microsoft Entra-leietakeren som brukes av Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)]-brukere har en Microsoft 365- eller Exchange Online-e-postkonto som er tildelt kontoene i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kontrollere denne innstillingen i delen **Microsoft 365-godkjenning** av brukerprofilen din i **Brukere**-listen. 

## <a name="set-up-contact-sync"></a>Konfigurer kontaktsynkronisering

Fullfør fremgangsmåten nedenfor for å konfigurere kontaktsynkronisering. Hvis du kjører [!INCLUDE[prod_short](includes/prod_short.md)] Spring 2019 (v.14), må du utføre et ekstra trinn som enten endrer programkode eller setter opp en forbindelse til Power BI.

1. <a name="registerapp"></a>Registrer en app for Exchange Online API i Microsoft Entra-leietakeren.

   I dette trinnet legger du til en registrert app i Microsoft Entra-leietakeren i Microsoft 365- eller Exchange Online-planen. På samme måte som andre Azure-tjenester som arbeider med Business Central, krever Exchange Online en appregistrering i Microsoft Entra ID. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom Business Central og Exchange Online.

   Følg de detaljerte instruksjonene i hjelpen for utviklere og IT-eksperter under [Registrer en app i Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Husk følgende punkter når du går gjennom instruksjonene:

   - Hvis du allerede har registrert et program som en del av en integrering med et annet Microsoft-produkt, for eksempel Power BI, kan du bruke denne appregistreringen på nytt. I dette tilfellet må du bare angi appen med Office 365 Exchange Online-tillatelser beskrevet i neste punkt.

   - Konfigurer den registrerte appen med følgende delegerte tillatelser til Office 365 Exchange Online-API-en:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. For [!INCLUDE[prod_short](includes/prod_short.md)], versjon 14 gjør du en av følgende oppgaver:

   - Endre side 6700 ved å endre `FALSE` til `TRUE` i følgende kodelinje i `OnPageOpen`-utløseren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Opprett ny side med følgende kode på OnPageOpen-utløseren:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Definer Power BI ved å følge instruksjonene i [Konfigurer Business Central on-Premises for Power BI-integrering](across-working-with-business-central-in-powerbi.md).

   Når løsningen du har valgt, er på plass, ber du brukerne om å kjøre den nye/endrede siden eller å [koble seg til Power BI](across-working-with-powerbi.md#connect). De trenger bare å gjøre dette trinnet én gang.

## <a name="next-steps"></a>Neste trinn

[Synkronisere kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
