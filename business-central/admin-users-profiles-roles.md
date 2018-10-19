---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: Finn ut hvordan du administrerer brukere og rollesentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Forstå brukere, profiler og rollesentre

I [!INCLUDE[d365fin](includes/d365fin_md.md)] legges brukere til av en administrator som gir også brukere tilgang til deler av [!INCLUDE[d365fin](includes/d365fin_md.md)] som de trenger i arbeidet.  

Tilgang til funksjonene behandles gjennom *brukergrupper* og *profiler*. Du kan som administrator legge til og fjerne brukere som en del av [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnementet, og du kan tilordne brukertillatelser gjennom brukergrupper.  

## <a name="adding-users"></a>Legge til brukere

For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://aka.ms/CreateOffice365Users).

Administrator kan deretter tilordne tillatelser til hver enkelt bruker og brukergruppe. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Brukere av lokale distribusjoner

For lokale distribusjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan systemansvarlig velge mellom forskjellige legitimasjonsgodkjenningsmekanismer for brukerne. Når du deretter oppretter en bruker, angir du ulike opplysninger avhengig av legitimasjonstypen du bruker i den spesifikke forekomsten av [!INCLUDE[server](includes/server.md)]. Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i Administrasjon-delen for utviklere og ITPro-innholdet for [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personene i selskapet som har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle tilordnet en *profil* som gir dem tilgang til et *rollesenter*.

Profiler er samlinger av [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som deler samme rollesenter. Et rollesenter er utgangspunktet og hjemmesiden for [!INCLUDE[d365fin](includes/d365fin_md.md)], som gir deg rask tilgang til de viktigste oppgavene og viser forskjellig innsikt og viktige ytelsesindikatorer (KPI-er) om arbeidet.  

> [!NOTE]  
>  I den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet kan du legge til, endre eller slette profiler.  

## <a name="configuration-and-personalization"></a>Konfigurasjon og tilpasning
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Brukere tilpasser brukergrensesnittet i sin egen versjon ved å tilpasse brukergrensesnittet når de er logget på sine egne konti. Denne tilpasningen kan slettes av systemansvarlig. Hvis du vil ha mer informasjon, se [Tilpasse arbeidsområdet ](ui-personalization-user.md).  

## <a name="see-also"></a>Se også  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)  
[Administrere tilpasning som Administrator](ui-personalization-manage.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  

