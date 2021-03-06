---
title: Administrative oppgaver i Business Central | Microsoft-dokumentasjon
description: Enkelte oppgaver i Business Central krever sentral administrasjon og oppsett. Se hva de er, og finn ut hva som må gjøres.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 13f713756fc1f771243686c549c22f3ce0974b6b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777219"
---
# <a name="administration"></a>Administrasjon

Sentrale administrasjonsoppgaver utføres vanligvis av én rolle i selskapet. Omfanget av disse oppgavene kan avhenge av selskapets størrelse og administrators jobbansvar. Disse oppgavene kan omfatte administrasjon av databasesynkronisering for jobb- og e-postkøer, oppsett av brukere og tilpassing av brukergrensesnittet.  

Det å angi riktige oppsettverdier for begynnelsen av er viktig for suksessen til all ny forretningsprogramvare. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderer flere oppsettveiledninger som hjelper deg med å konfigurere kjernedata. Hvis du vil ha mer informasjon, kan du se [Definere Business Central](setup.md).

Enten du bruker RapidStart Services til å implementere oppsettsverdier eller du angir dem manuelt i det nye selskapet, kan du støtte opp om oppsettsbeslutningene dine ved å følge noen generelle anbefalinger for utvalgte oppsettsfelt som er kjent for å redusere løsningens effektivitet hvis de defineres feil.  

En superbruker eller en administrator kan opprette et rammeverk for datautveksling slik at brukere kan eksportere og importere data i bank- og lønnsfiler, for eksempel for forskjellige bankstyringsprosesser. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).

> [!NOTE]
> Du kan opprette et nytt selskap i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services. RapidStart Services er et verktøy som er utviklet for å forkorte distribusjonstiden, forbedre kvaliteten på implementeringen, introdusere en implementeringsmetode som kan gjentas og øke produktiviteten ved å automatisere og forenkle regelmessige oppgaver. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definer hvem som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)] ved å opprette brukere på administrasjonssenteret for Microsoft 365 i henhold til produktlisensene.|[Opprette brukere i henhold til lisenser](ui-how-users-permissions.md)|
|Tilordne tillatelser til brukerne, endre tillatelsessett, og gruppere brukere for enkel behandling av tillatelser.|[Tilordne tillatelser til brukere og grupper](ui-how-users-permissions.md)|
|Legg til brukere, behandle tillatelser og tilgang til data, tilordne roller.|[Administrere profiler](admin-users-profiles-roles.md)|
|Behandle brukerinnstillinger, for eksempel firma, rolle, språk, region og tidssone.|[Brukerinnstillinger](admin-manage-user-settings-preferences.md)|
|Konfigurer skrivere, og angi hvilke rapporter som skal skrives ut på hvilke skrivere.|[Konfigurere skrivere](ui-specify-printer-selection-reports.md)|
|Klassifisere datafølsomheter for feltene slik at du kan svare på forespørsler fra dataobjekter relatert til personlig informasjon.|[Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md)|
|Svare på forespørsler fra dataobjekter relatert til personlig informasjon.|[Svare på forespørsler om personopplysninger](admin-responding-to-requests-about-personal-data.md)|
|Konfigurere et nytt konsern ved hjelp av maler|[Opprette nye selskaper](about-new-company.md)|
|Spore alle direkte endringer som brukere gjør i data i databasen, for å finne ut hvor feil og dataendringer oppstår.|[Logge endringer](across-log-changes.md)|  
|Legge inn enkeltstående eller gjentakende forespørsler om å kjøre rapporter eller kodeenheter.|[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Slette dokumenter](admin-manage-documents.md)|  
|Vis sider, kodeenheter og spørringer som web-tjenester.|[Publisere en webtjeneste](across-how-publish-web-service.md)|
|Som en del av å opprette Connect apps mellom [!INCLUDE[prod_short](includes/prod_short.md)] og tredjepartløsninger gjennom REST-API-er, må du definere maler som brukes til å fylle ut tomme egenskaper på en enhet når du oppretter en POST-handling gjennom et API.|[Konfigurere API-maler](admin-configuring-api-template.md)|
|Krypter data på [!INCLUDE[prod_short](includes/prod_short.md)]-serveren ved å generere nye eller importere eksisterende krypteringsnøkler som du aktiverer på serveren.|[Administrere datakryptering](admin-manage-data-encryption.md)|
|Koble Dynamics 365 Sales med [!INCLUDE[prod_short](includes/prod_short.md)] for å få en sømløs integrasjon mellom kunderelasjoner og ordrebehandling i interessent-til-kontanter-prosessen.|[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Endre hvilke felt og handlinger som skal vises i brukergrensesnittet, slik at det passer ditt selskaps forretningsprosesser, og utvid løsningen med apper.|[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|
|Overvåke bruk og feilsøke økter.|[Miljøtelemetri i administrasjonssenteret for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Behandle brukerøkter, inkludert avbryte en økt, hvis brukeren er blokkert.|[Behandle økter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Forretningsfunksjoner](across-business-functionality.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]