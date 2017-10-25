---
title: Administrative oppgaver i Dynamics 365 | Microsoft-dokumentasjon
description: "Enkelte oppgaver i [!INCLUDE[d365fin](includes/d365fin_md.MD)] krever sentral administrasjon og oppsett. Se hva de er, og finn ut hva som må gjøres."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09c3460a50088098bfe5c2fb633e76dccbac0794
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a>Oppsett og administrasjon i Dynamics 365 for Financials
Sentrale administrasjonsoppgaver utføres vanligvis av én rolle i selskapet. Omfanget av disse oppgavene kan avhenge av selskapets størrelse og administrators jobbansvar. Disse oppgavene kan omfatte administrasjon av databasesynkronisering for jobb- og e-postkøer, oppsett av brukere, tilpassing av brukergrensesnittet og administrasjon av krypteringsnøkler.  

Det å angi riktige oppsettverdier for begynnelsen av er viktig for suksessen til all ny forretningsprogramvare. [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer flere oppsettveiledninger som hjelper deg med å konfigurere kjernedata. Hvis du vil ha mer informasjon, se [Konfigurere Dynamics 365 for Financials](setup.md).

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

En superbruker eller en administrator kan opprette et rammeverk for datautveksling slik at brukere kan eksportere og importere data i bank- og lønnsfiler, for eksempel for forskjellige bankstyringsprosesser.  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Legg til brukere, behandle tillatelser og tilgang til data, tilordne roller.|[Brukere, profiler og rollesentre i Dynamics 365 for Financials](admin-users-profiles-roles.md)|  
|Spore alle direkte endringer som brukere gjør i data i databasen, for å finne ut hvor feil og dataendringer oppstår.|[Logging av endringer i Dynamics 365 for Financials](across-log-changes.md)|  
|Støtt opp om oppsettsbeslutningene dine med anbefalinger for valgte felt som er kjent for å kunne forårsake at løsningen blir ineffektiv hvis feilaktig satt opp.|[Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)|  
|Vis sider, kodeenheter og spørringer som web-tjenester.|[Publisere en webtjeneste](across-how-publish-web-service.md)|  
|Konfigurere en SMTP-server for å aktivere e-postkommunikasjon inn og ut av Dynamics 365 for Financials| [Konfigurere e-post manuelt eller bruke assistert oppsett](madeira-how-setup-email.md)|  
|Legge inn enkeltstående eller gjentakende forespørsler om å kjøre rapporter eller kodeenheter.|[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Administrere dokumenter](admin-manage-documents.md)|  
|Konfigurere et nytt konsern ved hjelp av maler|[Opprette nye seleskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)|  

## <a name="see-also"></a>Se også
[Oversikt over forretningsfunksjoner](madeira-business-functionality.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

