---
title: Opprette brukere i henhold til lisenser
description: Beskriver hvordan du legger til brukere i Business Central Online eller lokalt basert på lisenser.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9173
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2c81046828e6be26683853d2c9cb7836ed939fb1
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029169"
---
# <a name="create-users-according-to-licenses"></a>Opprette brukere i henhold til lisenser

Denne artikkelen beskriver hvordan administratorer kan opprette brukere og definere hvem som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)], og hvilke tillatelser som gis til ulike brukertyper i henhold til lisensene.

Når du oppretter brukere i [!INCLUDE[prod_short](includes/prod_short.md)], kan du tilordne bestemte tillatelser til dem via tillatelsessett og organisere brukere i brukergrupper. Brukergrupper gjør det enklere å behandle tillatelser for flere brukere samtidig. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

Hvis du vil ha mer informasjon om de ulike typene lisenser og hvordan lisensiering fungerer i [!INCLUDE[prod_short](includes/prod_short.md)], kan du se [Laste ned lisensieringsveiledningen for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Prosessen med å behandle brukere og lisenser varierer avhengig av om [!INCLUDE[prod_short](includes/prod_short.md)] er distribuert elektronisk eller lokalt. For [!INCLUDE [prod_short](includes/prod_short.md)] online må du legge til brukere fra Microsoft 365. I lokale distribusjoner kan du opprette, redigere og slette brukere direkte.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Behandle brukere og lisenser i nettdistribusjoner

I den nettbaserte versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] er antall brukere definert av abonnementet og lagt til leieren din i Microsoft Partner Center, vanligvis av en Microsoft-partner. Hvis du vil ha mer informasjon, se [Legge til en ny kunde](/partner-center/add-a-new-customer) og [Opprette eller avbryte kundeabonnementer](/partner-center/create-a-new-subscription) i hjelpen for Microsoft Partner Center.

Hvis du vil definere hvem som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)], må du tilordne produktlisenser til brukere i henhold til de rollene de skal utføre i [!INCLUDE[prod_short](includes/prod_short.md)]. Dette kan gjøres på følgende måter:

- Selskapets Microsoft 365-administrator kan gjøre dette i [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com). Hvis du vil ha mer informasjon, kan du se [Legge til brukere individuelt eller gruppevis i Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- En Microsoft-partner kan tilordne lisenser i administrasjonssenteret for Microsoft 365 eller i Microsoft Partner Center. Hvis du vil ha mer informasjon, se [Brukerbehandlingoppgaver for kundekonti](/partner-center/assign-licenses-to-users) i hjelpen for Microsoft Partner Center.

Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjelpen for administrasjon.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Slik legger du til brukere eller oppdaterer brukerinformasjon og lisenstilordninger i Business Central
Når du har lagt til brukere eller endret brukerinformasjon i administrasjonssenteret for Microsoft 365, kan du raskt importere brukerinformasjonen til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette omfatter lisenstilordninger. 

1. Logg på [!INCLUDE[prod_short](includes/prod_short.md)] ved å bruke en administratorkonto.
2. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.  
3. Velg **Oppdater brukere fra Microsoft 365**.

Hvis du legger til nye brukere, er det neste trinnet å tilordne brukergrupper og -tillatelser. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md). Hvis du oppdaterer brukerinformasjon, og oppdateringen omfatter en lisensendring, blir brukerne tilordnet til den aktuelle brukergruppen, og tilhørende tillatelsessett blir oppdatert. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser gjennom brukergrupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Alle brukere må tilordnes til den samme lisensen, enten Essential eller Premium. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/business-central/overview/)-nettstedet.

Hvis du vil ha mer informasjon om å synkronisere brukerinformasjon med Microsoft 365, kan du se delen [Synkronisering med Microsoft 365](#m365).

> [!NOTE]
> Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til Business Central, slik at vedkommende kan arbeide med regnskapsdataene. Hvis du vil ha mer informasjon, kan du se [Invitere den eksterne regnskapsføreren til Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>Fjerne en brukers tilgang til systemet

I nettbaserte distribusjoner kan du fjerne en brukers tilgang til [!INCLUDE[prod_short](includes/prod_short.md)]. Alle referanser til brukeren beholdes, men brukeren kan ikke logge på, og aktive økter for brukeren stoppes.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne siden **Brukerkort** for den aktuelle brukeren, og velg deretter **Deaktivert** i feltet **Status**.
3. Hvis du vil gi brukeren tilgang igjen, setter du verdien for feltet **Status** til **Aktivert**.

Du kan også fjerne lisensen fra en bruker i administrasjonssenteret for Microsoft 365. Brukeren kan da ikke logge på. Hvis du vil ha mer informasjon, kan du se [Fjerne lisenser fra brukere](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synkronisere med Microsoft 365

Når du tilordner en lisens for [!INCLUDE[prod_short](includes/prod_short.md)] til en bruker i Microsoft 365, kan du opprette brukeren i [!INCLUDE[prod_short](includes/prod_short.md)] på to måter.  

- Administratoren kan legge til brukeren ved å velge **Oppdater brukere fra Microsoft 365**-handlingen på **Brukere**-siden som beskrevet i delen [Slik legger du til en bruker eller oppdaterer brukerinformasjon i Business Central](#adduser).
- Lisensinformasjonen blir oppdatert automatisk når brukeren logger på første gang.

I begge tilfeller utføres det en rekke innstillinger automatisk. Disse er oppført i andre og tredje kolonne i tabellen nedenfor.

Hvis du endrer brukerinformasjon i Microsoft 365, kan du oppdatere [!INCLUDE[prod_short](includes/prod_short.md)] for å gjenspeile endringen. Avhengig av hva du vil oppdatere, kan du bruke én av handlingene på **Brukere**-siden. Handlingene beskrives i de tre siste kolonnene i tabellen nedenfor.

> [!NOTE]
> Handlingene som er beskrevet i tabellen nedenfor, er nøyaktige, men den eneste du trenger, er **Oppdatere brukerne fra Microsoft 365**, som ble lagt til for å forenkle prosessen. De andre handlingene blir fjernet i en fremtidig versjon av [!INCLUDE[prod_short](includes/prod_short.md)].

|Hva skjer når:|Første bruker, første pålogging|Hent brukere fra Microsoft 365|Oppdater brukere fra Microsoft 365|Gjenopprett brukerens standardbrukergrupper|Oppdater brukergrupper|Oppdater brukerinformasjon fra Microsoft 365|
|-|-|-|-|-|-|-|
|Omfang:|Gjeldende bruker|Nye brukere i Microsoft 365|Flere valgte brukere|Enkeltvalgt bruker (bortsett fra gjeldende)|Flere valgte brukere|Flere valgte brukere|
|Opprett den nye brukeren, og tilordne SUPER-tillatelsessett.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Oppdater brukeren basert på informasjon i Microsoft 365: status, fullt navn, kontaktens e-post, godkjennings-e-post.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synkroniser brukerplaner (lisenser) med lisenser og roller tilordnet i Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Legg til brukeren i brukergrupper i henhold til gjeldende brukerplaner. Fjern tillatelsessettet SUPER for alle andre brukere enn den første brukeren som skal logge på, samt [administratorer](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Det må være minst en forekomst av tillatelsessettet SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Fjerner manuelt tilordnede brukergrupper og tillatelser.|**X**<br /><br />Oppdater brukergruppetilordninger.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Behandle brukere og lisenser i lokale distribusjoner

For lokale distribusjoner er antallet brukerlisenser angitt i lisensfilen (.flf). Når en administrator eller Microsoft-partner laster opp lisensfilen, kan administratoren angi hvilke brukere som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)].

Ved distribusjon på stedet oppretter, redigerer og sletter administratoren brukere direkte fra **Brukere**-siden.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Slik redigerer eller sletter du en bruker i en lokal distribusjon

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil redigere, og velg deretter **Rediger**-handlingen.
3. På siden **Brukerkort** endrer du informasjonen etter behov.  
4. Hvis du vil slette en bruker, velger du brukeren du vil slette, og deretter velger du handlingen **Slett**.

> [!NOTE]
> For lokale distribusjoner kan en administrator angi hvordan brukerlegitimasjoner skal godkjennes i [!INCLUDE[server](includes/server.md)]-forekomsten. Når du oppretter en bruker, angir du legitimasjonstypen du bruker.
>
> Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i administrasjonshjelpen for [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Lisensiering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Legge til brukere i Microsoft 365 for business](/microsoft-365/admin/add-users/add-users)  
[Sikkerhet og beskyttelse i Business Central (administrasjonsinnhold)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]