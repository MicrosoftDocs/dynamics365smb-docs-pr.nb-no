---
title: Sette opp brukerkontoer for integrasjon med Dynamics 365 for Sales | Microsoft Docs
description: Lær hvordan du definerer brukerkontoene som appene bruker til å utveksle data, og som brukes til å få tilgang til og synkronisere data i appene.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246577"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Sette opp brukerkontoer for integrasjon med Dynamics 365 for Sales
Denne artikkelen gir en oversikt over hvordan du definerer brukerkontoene som er nødvendige for å integrere [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Definere administratorbrukerkontoen i Sales
Du må legge til brukerkontoen for administrator for [!INCLUDE[d365fin](includes/d365fin_md.md)] som en bruker i [!INCLUDE[crm_md](includes/crm_md.md)], og deretter forfremme brukeren til administrator i [!INCLUDE[crm_md](includes/crm_md.md)]. Brukerkontoen for administrator må også ha rollen Systemtilpasser og minst én annen ikke-administrativ brukerrolle, for eksempel Salgssjef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurere brukerkontoen for integrasjonen
Du må opprette en dedikert brukerkonto i Office 365-abonnement som både [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan bruke til å synkronisere data. Denne kontoen må være i stand til å logge på [!INCLUDE[crm_md](includes/crm_md.md)], som betyr at denne brukeren må ha en lisens for [!INCLUDE[crm_md](includes/crm_md.md)]. Denne kontoen må også være en ikke-interaktiv konto i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon om hvordan du oppretter brukere i [!INCLUDE[crm_md](includes/crm_md.md)], kan du se [Håndtere sikkerhet, brukere og team](http://go.microsoft.com/fwlink/?LinkID=616518). Når tilkoblingen er opprettet, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] tilordne brukerkontoen sikkerhetsrollene som nødvendige i [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Assistert oppsettsveiledning viser sted for å angi brukerlegitimasjon for synkronisering](media/sync-user-setup.png "Veiviserside for assistert oppsett for visualisering viser sted for å angi brukerlegitimasjon for synkronisering")

> [!IMPORTANT]  
> Ikke bruk administratorkontoen for [!INCLUDE[crm_md](includes/crm_md.md)] til synkronisering. Når du gjør det, brytes synkroniseringen.
> I tillegg, for å unngå konstant synkronisering, endringer i data som utførtes av integreringsbrukerkontoen, synkroniseres ikke. <!--What changes would this account make?--> Når tilkoblingen er opprettet, anbefales det å angi tilgangsmodus for brukerkontoen for integrering til ikke-interaktivt modus i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Opprette en ikke-interaktiv brukerkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Definere kontoer for selgerne
Du må opprette kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] for selgerne fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. For å gjøre det enklere tilbyr Microsoft 365-administrasjonssenteret en Excel-mal du kan bruke. På siden **Aktive brukere** velger du **Mer**, og deretter klikker du på **Importer flere brukere**. Velg **Last ned en CSV-fil med bare topptekst**, og deretter angir du opplysninger for selgeren. Hvis du vil se et eksempel kan du velge **Last ned en CSV-eksempelfil med topptekst og eksempelbrukerinformasjon**. Når du har angitt informasjon om brukerne, er neste trinn i importprosessen å tilordne brukerlisensene til Dynamics 365 Customer Engagement-planen.  

Når du importerer brukere og tilordner dem lisenser for Dynamics 365 Customer Engagement, må du tilordne brukerne til rollen **Selger** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Koble selgere til brukere i Dynamics 365 for Sales](media/couple-salespeople.png "Visualisering av kobling av selgerne til brukere i Dynamics 365 for Sales")

## <a name="see-also"></a>Se også  
[Integrere med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
