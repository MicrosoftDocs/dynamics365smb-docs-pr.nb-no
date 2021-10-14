---
title: Administrer OneDrive-integrering med Business Central
description: Finn ut mer om ting du kan gjøre for å administrere integrering mellom Business Central og OneDrive for Business.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: cceb05c1ad19a95494c188cd2482b45962535c94
ms.sourcegitcommit: 99c705d160451c05b226350ff94b52fb0c3ae7a0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606413"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Administrer OneDrive-integrering med Business Central 
Denne artikkelen gir en oversikt over hva en administrator kan gjøre for å styre OneDrive for Business-integrasjon med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online-kunder får fordeler fra automatisk integrasjon, uten at det kreves ekstra oppsett for å bruke disse funksjonene. 

## <a name="minimum-requirements"></a>Minstekrav

* Hver bruker må ha en lisens for [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive som en del av en Microsoft 365-plan.
* OneDrive må konfigureres for hver bruker.

## <a name="governance"></a>Styring
SharePoint-administrasjonssenteret gir omfattende kontroll over policyer som styrer bruken av OneDrive i hele organisasjonen. Globale administratorer eller brukere som har rollen SharePoint-administrator, kan konfigurere policyer som bestemmer hvem som kan få tilgang til OneDrive, hvor dataene er plassert, livssyklusen til innholdet og mye annet. Følgende koblinger gir informasjon om ofte brukte funksjoner og innstillinger som kan forbedre integreringen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Administrer delingsinnstillinger](/sharepoint/turn-external-sharing-on-or-off)
* [Bruk informasjonsbarrierer med SharePoint](/sharepoint/information-barriers)
* [Finn ut mer om hindring av datatap](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Angi standard lagringsplass for OneDrive-brukere](/onedrive/set-default-storage-space)
* [Legg til og fjern administratorer for en brukers OneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deaktiver OneDrive-oppretting for enkelte brukere](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Funksjoner for flere geografiske plasseringer i OneDrive og SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Noen funksjoner er kanskje bare tilgjengelige for bestemte planer.

## <a name="managing-privacy"></a>Administrer personvern
Administratorer og sluttbrukere kontrollerer innholdet som er lagret i OneDrive, og disse dataene eies bare av organisasjonen. Hvis du vil ha mer informasjon, kan du se [Hvordan SharePoint og OneDrive sikrer dataene i skyen](/sharepoint/safeguarding-your-data). Du kan også se [Microsofts personvernerklæring](https://privacy.microsoft.com/en-us/privacystatement), som forklarer dataene som Microsoft behandler, hvordan Microsoft behandler dem, og til hva slags formål.

## <a name="restoring-onedrive-and-prod_short"></a>Gjenopprett OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]
Som en del av en nødgjenopprettingsøvelse kan det hende at administratorer må gjenopprette et [!INCLUDE[prod_short](includes/prod_short.md)]-miljø til en sikkerhetskopi fra et tidspunkt i fortiden og synkronisere OneDrive-lagring med det samme tidspunktet. OneDrive inneholder ulike verktøy for dette, for eksempel gjenoppretting av en brukers OneDrive til et tidligere tidspunkt, gjenoppretting av en tidligere versjon av en enkelt fil eller gjenoppretting av slettede filer. Hvis du vil ha mer informasjon, kan du se disse artiklene:

* For [!INCLUDE[prod_short](includes/prod_short.md)]: se [Gjenopprett et miljø i administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* For OneDrive: se [gjenopprett din OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Konfigurering av Business Central On-Premises

En administrator må konfigurere tilkoblingen mellom [!INCLUDE[prod_short](includes/prod_short.md)] lokalt og OneDrive. I motsetning til [!INCLUDE[prod_short](includes/prod_short.md)] online er ikke tilkoblingen automatisk. Hvis tilkoblingen ikke er konfigurert, kan ikke brukerne bruke funksjonene i OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan bare kobles til OneDrive driftet av Microsoft i skyen. Tilkobling av [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til Mine områder-repositoriet til SharePoint Server støttes ikke.

> [!IMPORTANT]
> Ved å konfigurere denne funksjonen aktiverer du også eldre funksjoner som sender filer til OneDrive.  
>
>* Funksjonen Åpne i Excel kopierer automatisk Excel-filen til OneDrive og åpner den deretter i Excel Online. 
>* Hvis du eksporterer en rapport til en fil, kopieres filen automatisk til OneDrive, og deretter åpnes den i Excel Online, Word Online eller OneDrive. 
>* Andre funksjoner kan også åpnes automatisk i OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Slik klargjør du [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for tilkobling til OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Legg til et registrert program for Business Central i Azure AD-leietakeren i Microsoft 365-planen. På samme måte som andre Azure-tjenester som arbeider med Business Central, krever OneDrive en appregistrering i Azure Active Directory (Azure AD). Appregistreringen tilbyr godkjennings- og autorisasjonstjenester mellom Business Central og SharePoint, som brukes av OneDrive.

Konfigurer det registrerte programmet med følgende delegerte tillatelser til SharePoint-API-en:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Du gjør dette i Azure Portal. Pass på at du kopierer program-ID-en (klient) og klienthemmeligheten som brukes av det registrerte programmet. Du må ha denne informasjonen i neste oppgave.

Hvis du vil ha mer informasjon om å registrere et program og konfigurere tillatelser, kan du se [Registrer et program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) i hjelpen for utviklere og IT-eksperter.

> [!TIP]
> Hvis du allerede har registrert et program som en del av en integrering med et annet Microsoft-produkt, for eksempel Power BI, kan du bruke denne programregistreringen på nytt. I dette tilfellet må du bare angi SharePoint-tillatelser.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Slik konfigurerer du tilkoblingen i [!INCLUDE[prod_short](includes/prod_short.md)] lokalt

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Microsoft SharePoint-tilkoblingsoppsett** og velger den relaterte koblingen.
2. I feltet **Beskrivelse** angir du en beskrivelse for tilkoblingen, som **OneDrive**.
3. I feltet **Mappe** skriver du inn **Business Central**.
4. I feltet **Plassering** skriver du inn URL-adressen til OneDrive.

    URL-adressen for en OneDrive er vanligvis i følgende format: `https://<tenant name>-my.sharepoint.com`. Hvis du vil ha mer informasjon, kan du se [URL-adresser for OneDrive for brukere i organisasjonen](/onedrive/list-onedrive-urls) i OneDrive-dokumentasjonen.
5. I feltet **Klient-ID** angir du klient-ID-en fra programregistreringen.
6. I feltet **Klienthemmelighet** angir du hemmeligheten fra programregistreringen. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> Siden Tilkoblingsoppsett for SharePoint brukes til å konfigurere flere eldre funksjoner. **Generelt**-delen konfigurerer tilkoblingen til OneDrive, og delen **Delte dokumenter** omadresserer filer til SharePoint i stedet. Den gamle SharePoint-funksjonen blir avskrevet i nær fremtid. Vi anbefaler at du ikke konfigurerer delen **Delte dokumenter**.

## <a name="see-also"></a>Se også
[Business Central og OneDrive for Business-integrering](across-onedrive-overview.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)

