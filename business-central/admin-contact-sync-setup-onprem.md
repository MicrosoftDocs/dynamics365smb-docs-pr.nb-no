---
title: Konfigurer kontaktsynkronisering med Outlook for Business Central lokalt
description: Lær hvordan du konfigurerer en envirSet up-kontaktsynkronisering for Business Central lokalt med Outlook for Business Central lokalt
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 03/17/2023
ms.custom: bap-template
---

# Konfigurer kontaktsynkronisering med Outlook for Business Central lokalt

I denne artikkelen lærer du hvordan du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokal for å synkronisere kontakter i [!INCLUDE[prod_short](includes/prod_short.md)] med kontakter i Outlook. Hvis du vil ha mer informasjon om dette, kan du gå til [Synkroniser kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Introduksjon

Kontaktsynkronisering krever bruk av OAuth 2.0-protokollen for godkjenning med Exchange Online. Tidligere ble enkel godkjenning også støttet, men den er avskrevet og støttes ikke lenger med Exchange Online. Du kan lese mer om avskrivingen ved [Avskriving av enkelt godkjenning i Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Denne endringen betyr at kontaktsynkronisering i Business Central kan ha sluttet å virke i det lokale miljøet. Denne artikkelen forklarer hvordan du får det til å fungere igjen.

## Forutsetninger

- Exchange Online, enten en frittstående versjon eller gjennom Microsoft 365-planen  
- Tilgang til Azure Active Directory-leietakeren (Azure AD) som brukes av Exchange Online
- [!INCLUDE[prod_short](includes/prod_short.md)]-brukere har en Microsoft 365- eller Exchange Online-e-postkonto som er tildelt kontoene i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan kontrollere denne innstillingen i delen **Microsoft 365-godkjenning** av brukerprofilen din i **Brukere**-listen. 

## Konfigurer kontaktsynkronisering

Fullfør fremgangsmåten nedenfor for å konfigurere kontaktsynkronisering. Hvis du kjører [!INCLUDE[prod_short](includes/prod_short.md)] Spring 2019 (v.14), må du utføre et ekstra trinn som enten endrer programkode eller setter opp en forbindelse til Power BI.

1. <a name="registerapp"></a>Registrer en app for Exchange Online API i Azure AD-leietakeren.

   I dette trinnet legger du til en registrert app i Azure AD-leietakeren i Microsoft 365- eller Exchange Online-planen. På samme måte som andre Azure-tjenester som fungerer med Business Central, krever Exchange Online en appregistrering i Azure AD. Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom Business Central og Exchange Online.

   Følg de detaljerte instruksjonene i hjelpen for utviklere og IT-eksperter under [Registrer en app i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Husk følgende punkter når du går gjennom instruksjonene:

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

   - Definer Power BI ved å følge instruksjonene i [Konfigurer Business Central on-Premises for Power BI-integrering](admin-powerbi-setup.md#setup).

   Når løsningen du har valgt, er på plass, ber du brukerne om å kjøre den nye/endrede siden eller å [koble seg til Power BI](across-working-with-powerbi.md#connect). De trenger bare å gjøre dette trinnet én gang.

## Neste trinn

[Synkronisere kontakter i Business Central med kontakter i Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
