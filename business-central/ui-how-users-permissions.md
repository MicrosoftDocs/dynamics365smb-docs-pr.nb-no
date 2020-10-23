---
title: Opprette brukere i henhold til lisenser | Microsoft Docs
description: Beskriver hvordan du legger til brukere i Business Central Online eller lokalt basert på lisenser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: df34469bc28b081800ddf583e7aa9cf08a15dc27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925650"
---
# <a name="create-users-according-to-licenses"></a>Opprette brukere i henhold til lisenser

Denne artikkelen beskriver hvordan administratorer kan opprette brukere og definere hvem som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], og hvilke tillatelser som gis til ulike brukertyper i henhold til lisensene.

Når du oppretter brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du tilordne bestemte tillatelser til dem via tillatelsessett og organisere brukere i brukergrupper. Brukergrupper gjør det enklere å behandle tillatelser for flere brukere samtidig. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Prosessen med å behandle brukere og lisenser varierer avhengig av om [!INCLUDE[d365fin](includes/d365fin_md.md)] er distribuert elektronisk eller lokalt. For [!INCLUDE [prodshort](includes/prodshort.md)] online må du legge til brukere fra Microsoft 365. I lokale distribusjoner kan du opprette, redigere og slette brukere direkte.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Behandle brukere og lisenser i nettdistribusjoner

I den nettbaserte versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er antall brukere definert av abonnementet og lagt til leieren din i Microsoft Partner Center, vanligvis av en Microsoft-partner. Hvis du vil ha mer informasjon, se [Legge til en ny kunde](/partner-center/add-a-new-customer) og [Opprette eller avbryte kundeabonnementer](/partner-center/create-a-new-subscription) i hjelpen for Microsoft Partner Center.

Hvis du vil definere hvem som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], må du tilordne produktlisenser til brukere i henhold til de rollene de skal utføre i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kan gjøres på følgende måter:

- Selskapets Microsoft 365-administrator kan gjøre dette i [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com). Hvis du vil ha mer informasjon, se [Legge til brukere individuelt eller gruppevis i Microsoft 365](https://aka.ms/CreateOffice365Users).  
- En Microsoft-partner kan tilordne lisenser i administrasjonssenteret for Microsoft 365 eller i Microsoft Partner Center. Hvis du vil ha mer informasjon, se [Brukerbehandlingoppgaver for kundekonti](/partner-center/assign-licenses-to-users) i hjelpen for Microsoft Partner Center.

Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjelpen for administrasjon.

Når brukere får tilordnet en [!INCLUDE[d365fin](includes/d365fin_md.md)]-lisens i Microsoft 365, kan du importere dem til **Brukere**-siden i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke handlingen **Hent nye brukere fra Office 365**.

### <a name="to-add-a-user-or-update-user-information-in-business-central"></a><a name="adduser"></a>Slik legger du til en bruker eller oppdaterer brukerinformasjon i Business Central

Bruk dedikerte importfunksjoner til å legge til nye brukere eller oppdatere brukerinformasjon i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra administrasjonssenteret for Microsoft 365.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Oppdater brukere fra Office 365**.

    Hvis dette er første gang du legger til brukere fra Microsoft 365, velger du handlingen **Hent nye brukere fra Office 365**.  
3. Følg fremgangsmåten i veiledningen som vises.

De nye brukerne og brukerinformasjonen i Microsoft 365-abonnementet legges til på **Brukere**-siden i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nå kan du tilordne brukergrupper og tillatelser. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

Hvis du vil ha mer informasjon om å synkronisere brukerinformasjon med Microsoft 365, kan du se delen [Synkronisering med Microsoft 365](#m365).

> [!NOTE]
> Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til Business Central, slik at vedkommende kan arbeide med regnskapsdataene. Hvis du vil ha mer informasjon, kan du se [Invitere den eksterne regnskapsføreren til Business Central](finance-accounting.md#inviteaccountant)

### <a name="to-change-the-assigned-license-for-a-user"></a>Slik endrer du den tilordnede lisensen for en bruker

Noen ganger kan det hende du må endre lisensen som er tilordnet en bruker. Hvis du for eksempel bestemmer deg for å bruke Servicehåndtering-modulen og derfor må oppgradere alle Essential-lisenser til Premium. Eller hvis en brukers ansvar er endret, og du må erstatte en Team Member-lisens til Essential.

1. Endre lisensen i administrasjonssenteret for Microsoft 365. Hvis du vil ha mer informasjon, se [Legge til brukere individuelt eller gruppevis i Microsoft 365](https://aka.ms/CreateOffice365Users).
2. Logg på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administrator.
3. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
4. På siden **Brukere** velger du handlingen **Gjenopprett brukerens standardbrukergrupper**.

Brukerne vil bli flyttet til en riktig brukergruppe, og tillatelsessettene blir oppdatert. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser gjennom brukergrupper](ui-define-granular-permissions.md).

> [!NOTE]
> Alle brukere må tilordnes til den samme lisensen, enten Essential eller Premium. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/business-central/overview/)-nettstedet.

### <a name="to-remove-a-users-access-to-the-system"></a>Fjerne en brukers tilgang til systemet

I nettbaserte distribusjoner kan du fjerne en brukers tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Alle referanser til brukeren beholdes, men brukeren kan ikke logge på, og aktive økter for brukeren stoppes.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne **Brukerkort**-siden for den aktuelle brukeren, og velg deretter **Deaktivert** i **Tilstand**-feltet.
3. For å gi brukeren tilgang igjen setter du feltet **Status** til **Aktivert**.

Du kan også fjerne lisensen fra en bruker i administrasjonssenteret for Microsoft 365. Brukeren kan da ikke logge på. Hvis du vil ha mer informasjon, kan du se [Fjerne lisenser fra brukere](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisering med Microsoft 365

Når du tilordner en lisens for [!INCLUDE[d365fin](includes/d365fin_md.md)] til en bruker i Microsoft 365, kan du opprette brukeren i [!INCLUDE[d365fin](includes/d365fin_md.md)] på to måter.  

- Administratoren kan legge til brukeren ved å velge **Oppdater brukere fra Office 365**-handlingen på **Brukere**-siden som beskrevet i delen [Slik legger du til en bruker eller oppdaterer brukerinformasjon i Business Central](#adduser).
- Lisensinformasjonen blir oppdatert automatisk når brukeren logger på første gang.

I begge tilfeller utføres det en rekke innstillinger automatisk. Disse er oppført i andre og tredje kolonne i tabellen nedenfor.

Hvis du endrer brukerinformasjon i Microsoft 365, kan du oppdatere [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile endringen. Avhengig av hva du vil oppdatere, kan du bruke én av handlingene på **Brukere**-siden. Handlingene beskrives i de tre siste kolonnene i tabellen nedenfor.

|Hva skjer når:|Første bruker, første pålogging|Hent brukere fra Microsoft 365|Oppdater brukere fra Microsoft 365|Gjenopprett brukerens standardbrukergrupper|Oppdater brukergrupper|
|-|-|-|-|-|-|
|Omfang:|Gjeldende bruker|Nye brukere i Microsoft 365|Flere valgte brukere|Enkeltvalgt bruker (bortsett fra gjeldende)|Flere valgte brukere|
|Opprett den nye brukeren, og tilordne SUPER-tillatelsessett.<br /><br /><!--Platform-->|**X**|| | | |
|Oppdater brukerposten basert på faktisk informasjon i Microsoft 365: status, fullt navn, kontaktens e-post, godkjennings-e-post.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**| |
|Synkroniser brukerplaner (lisenser) med lisenser og roller tilordnet i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**| |**X**|**X**|
|Legg til brukeren i brukergrupper i henhold til gjeldende brukerplaner. Fjern tillatelsessettet SUPER for alle andre brukere enn den første brukeren som skal logge på, samt [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Det må være minst en forekomst av tillatelsessettet SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**| |**X**<br /><br />Fjerner manuelt tilordnede brukergrupper og tillatelser.|**X**<br /><br />Oppdater brukergruppetilordninger.|

## <a name="the-device-license"></a>Enhetslisensen

Enhetslisensen for Dynamics 365 Business Central tillater flere brukere å bruke en enhet som dekkes av lisensen samtidig. Dette kan for eksempel være et salgssted, et verksted eller en lagerenhet. Når du har kjøpt et antall enhetslisenser, kan opptil det antallet brukere som er tilordnet til gruppen Enhetsbrukere for Dynamics 365 Business Central, logge på samtidig. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/business-central/overview/)-nettstedet.

Selskapets Microsoft 365-administrator eller Microsoft-partner kan opprette gruppen Enhetsbrukere for Dynamics 365 Business Central og legge til enhetsbrukere som medlemmer i [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com/) eller i [Azure Portal](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Begrensninger for enhetsbrukere

Brukere med enhetslisensen kan ikke utføre følgende oppgaver i [!INCLUDE[d365fin](includes/d365fin_md.md)]:

- Definere jobber som skal kjøres som planlagte oppgaver i jobbkøen. Enhetsbrukere er samtidige brukere, og vi kan derfor ikke sikre at den involverte brukeren finnes i systemet når en oppgave utføres, noe som kreves.

- En enhetsbruker kan ikke være første bruker til å logge på. En bruker av typen administrator, fullstendig bruker eller ekstern regnskapsfører må være den første til å logge på, slik at de kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjelpen for administrasjon.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Slik oppretter du en Dynamics 365 Business Central-enhetsbrukergruppe

1. Gå til **Grupper**-siden i administrasjonssenteret for Microsoft 365.
2. Velg handlingen **Legg til en gruppe**.
3. På siden **Velg en gruppetype** velger du **Sikkerhet** og deretter **Legg til**.
4. På siden **Grunnleggende** angir du **Dynamics 365 Business Central Device Users** som navnet på gruppen.
  
   >[!NOTE]
   >Navnet på gruppen må være skrevet på engelsk nøyaktig som vist i trinn 4, selv om du bruker et annet språk.
5. Velg **Lukk**-knappen.

> [!NOTE]
> Du kan også opprette en gruppe av typen Microsoft 365. Hvis du vil ha mer informasjon, kan du se [Sammenligne grupper](https://docs.microsoft.com/office365/admin/create-groups/compare-groups).

### <a name="to-add-members-to-the-group"></a>Slik legger du til medlemmer i gruppen

1. I administrasjonssenteret for Microsoft 365 oppdaterer du **Grupper**-siden, slik at den nye gruppen vises.
2. Velg gruppen **Dynamics 365 Business Central Device Users**, og velg deretter **Vis alle og administrer medlemmer**.
3. Velg handlingen **Legg til medlemmer**.
4. Velg brukerne du vil legge til, og velg deretter **Lagre**-knappen.
5. Velg **Lukk**-knappen tre ganger.

Du kan legge til så mange brukere i gruppen Dynamics 365 Business Central Device Users som du trenger. Antall enheter som brukere kan logge på samtidig, blir imidlertid definert av antall kjøpte enhetslisenser.

> [!NOTE]
> Du trenger ikke å tilordne en [!INCLUDE[d365fin](includes/d365fin_md.md)]-lisens til brukere som er medlemmer av gruppen Dynamics 365 Business Central Device Users.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Behandle brukere og lisenser i lokale distribusjoner

For lokale distribusjoner er antallet brukerlisenser angitt i lisensfilen (.flf). Når en administrator eller Microsoft-partner laster opp lisensfilen, kan administratoren angi hvilke brukere som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ved distribusjon på stedet oppretter, redigerer og sletter administratoren brukere direkte fra **Brukere**-siden.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Slik redigerer eller sletter du en bruker i en lokal distribusjon

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil redigere, og velg deretter **Rediger**-handlingen.
3. På siden **Brukerkort** endrer du informasjonen etter behov.  
4. Hvis du vil slette en bruker, velger du brukeren du vil slette, og deretter velger du handlingen **Slett**.

> [!NOTE]
> For lokale distribusjoner kan en administrator angi hvordan brukerlegitimasjoner skal godkjennes i [!INCLUDE[server](includes/server.md)]-forekomsten. Når du oppretter en bruker, angir du legitimasjonstypen du bruker.
>
> Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrasjonshjelpen for [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også

[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Legg til brukere i Microsoft 365 for bedrifter](https://aka.ms/CreateOffice365Users)  
[Sikkerhet og beskyttelse i Business Central (administrasjonsinnhold)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
