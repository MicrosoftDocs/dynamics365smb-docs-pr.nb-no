---
title: Tilordne eller redigere brukertillatelser | Microsoft-dokumentasjon
description: Beskriver hvordan du legger til Office 365-brukere i Business Central og deretter tilordner tillatelser, tilgangsrettigheter og sikkerhetsinnstillinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 11/07/2019
ms.author: sgroespe
ms.openlocfilehash: c64a14ed66668f8c3cbe09e8db3430a7dc25db5c
ms.sourcegitcommit: 2a6d629cf290645606356b714a77ef2872bdec64
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/07/2019
ms.locfileid: "2774822"
---
# <a name="create-users-according-to-licenses"></a>Opprette brukere i henhold til lisenser
Nedenfor beskrives hvordan du kan opprette brukere og definere hvem som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], og hvilke grunnleggende rettigheter ulike brukertyper har i henhold til lisensene.

Når det opprettes brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsette å tilordne bestemte tillatelser til brukere via tillatelsessett og organisere brukere i brukergrupper for enkel tillatelsesadministrasjon. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

> [!NOTE]
> Prosessen med å behandle brukere og lisenser varierer avhengig av om løsningen er distribuert elektronisk eller lokalt. I nettdistribusjoner kan du for eksempel bare deaktivere og aktivere en bruker når den er lagt til [!INCLUDE[d365fin](includes/d365fin_md.md)]. I lokale distribusjoner kan du opprette, redigere og slette brukere.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Behandle brukere og lisenser i nettdistribusjoner
I [!INCLUDE[d365fin](includes/d365fin_md.md)] online er antall brukere definert av abonnementet og lagt til leieren din i Microsoft Partner Center, vanligvis av en Microsoft-partner. Hvis du vil ha mer informasjon, se [Legge til en ny kunde](https://docs.microsoft.com/partner-center/add-a-new-customer) og [Opprette eller avbryte kundeabonnementer](https://docs.microsoft.com/partner-center/create-a-new-subscription) i hjelpen for Microsoft Partner Center.

Hvis du vil definere hvem som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)], må produktlisensene tilordnes til brukere i henhold til de rollene de skal utføre i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette kan gjøres på følgende måter:
- Selskapets Office 365-administrator kan gjøre dette i [administrasjonssenteret for Microsoft 365](https://admin.microsoft.com). Hvis du vil ha mer informasjon, se [Legge til brukere individuelt eller gruppevis i Office 365](https://aka.ms/CreateOffice365Users).  
- En Microsoft-partner kan tilordne lisenser i administrasjonssenteret for Microsoft 365 eller i Microsoft Partner Center. Hvis du vil ha mer informasjon, se [Brukerbehandlingoppgaver for kundekonti](https://docs.microsoft.com/partner-center/assign-licenses-to-users) i hjelpen for Microsoft Partner Center.

Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) i hjelpen for utviklere og IT-eksperter.

Når brukere med en [!INCLUDE[d365fin](includes/d365fin_md.md)]-lisens er opprettet i Office 365, kan de importeres til **Brukere**-siden i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke handlingen **Hent brukere fra Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Slik legger du til en bruker i Business Central
Hvis du vil legge til brukere fra administrasjonssenteret for Microsoft 365 til [!INCLUDE[d365fin](includes/d365fin_md.md)] online, bruker du en egen importfunksjon.  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Hent brukere fra Office 365**.

Alle nye brukere som allerede er opprettet for ditt Office 365-abonnement, legges til på siden **Brukere**. Brukere er tilordnet tillatelsessett i henhold til lisensen som er tilordnet til brukeren i Office 365. Du kan deretter fortsette med å tilordne mer detaljerte tillatelser til brukere og ordne dem i brukergrupper for enkel behandling av tillatelser. Hvis du vil ha mer informasjon, kan du se [Slik tilordner du tillatelsessett til brukere](ui-define-granular-permissions.md#to-assign-permission-sets-to-users).

### <a name="to-remove-a-users-access-to-the-system"></a>Fjerne en brukers tilgang til systemet
I nettdistribusjoner kan du fjerne en brukers tilgang til systemet ved angi feltet **Status** til **Deaktivert**. Alle referanser til brukeren vil bli beholdt, men brukeren kan ikke lenger logge seg på systemet, og aktive økter for brukeren avsluttes.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne **Brukerkort**-siden for den aktuelle brukeren, og velg deretter **Deaktivert** i **Tilstand**-feltet.
3. For å gi brukeren tilgang igjen setter du feltet **Status** til **Aktivert**.

I tillegg til å deaktivere en bruker kan du oppheve tilordningen av lisensen fra en bruker i administrasjonssenteret for Office 365. Brukeren kan da ikke logge på. Hvis du vil ha mer informasjon, kan du se [Oppheve tilordning av lisenser fra brukere](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>Slik endrer du den tilordnede lisensen for en bruker
Noen ganger kan det hende du må endre lisensen som er tilordnet en bruker. Hvis du for eksempel bestemmer deg for å bruke Servicehåndtering-modulen og derfor må oppgradere alle Essential-lisenser til Premium. Eller hvis en brukers ansvar er endret, og du må erstatte en Team Member-lisens til Essential.

1. Endre lisensen i administrasjonssenteret for Office 365. Hvis du vil ha mer informasjon, se [Legge til brukere individuelt eller gruppevis i Office 365](https://aka.ms/CreateOffice365Users).
2. Logg på [!INCLUDE[d365fin](includes/d365fin_md.md)] som administrator.
3. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
4. På siden **Brukere** velger du handlingen **Oppdater alle brukergrupper**.
Brukerne vil bli flyttet til en riktig brukergruppe, og tillatelsessettene blir oppdatert. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser gjennom brukergrupper](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Alle vanlige brukere i en løsning må tilordnes den samme lisensen, Essential eller Premium.
> For informasjon om lisensiering, se [Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

## <a name="managing-users-and-licenses-in-online-deployments"></a>Behandle brukere og lisenser i nettdistribusjoner
For distribusjon på stedet er det angitt en rekke lisensierte brukere i lisensfilen (.flf). Når administratoren eller Microsoft-partneren laster opp lisensfilen, kan administratoren angi hvilke brukere som kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ved distribusjon på stedet oppretter, redigerer og sletter administratoren brukere direkte fra **Brukere**-siden.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Redigere eller slette en bruker lokalt
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil redigere, og velg deretter **Rediger**-handlingen.
3. På siden **Brukerkort** endrer du informasjonen etter behov.    
4. Hvis du vil slette en bruker, velger du brukeren du vil slette, og deretter velger du **slett**-handlingen.

> [!NOTE]
> For lokale distribusjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan systemansvarlig velge mellom forskjellige legitimasjonsgodkjenningsmekanismer for brukerne. Når du deretter oppretter en bruker, angir du ulike opplysninger avhengig av legitimasjonstypen du bruker i den spesifikke forekomsten av [!INCLUDE[server](includes/server.md)].<br /><br />
> Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i Administrasjon-delen for utviklere og ITPro-innholdet for [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Administrere profiler](admin-users-profiles-roles.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Legge til brukere i Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Lisensveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)  
[Sikkerhet og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) i hjelpen for utviklere og IT-eksperter
