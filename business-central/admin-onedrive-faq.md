---
title: Vanlige spørsmål om OneDrive for Business
description: Få svar på enkelte vanlige spørsmål om å arbeide med OneDrive for Business og Business Central.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: f54e8b6290e9dd653180b3ea05246255b84dc2ae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144053"
---
# <a name="onedrive-for-business-faq"></a>Vanlige spørsmål om OneDrive for Business

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikkelen besvarer noen av spørsmålene du kan ha om å arbeide med OneDrive og [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="does-this-work-with-all-prod_short-clients"></a>Fungerer dette med alle [!INCLUDE[prod_short](includes/prod_short.md)]-klienter?

Ja. Du kan åpne filer i OneDrive fra [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappene når du viser kortopplysninger i Microsoft Teams, eller til og med fra Outlook-tillegget.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Er OneDrive det samme som SharePoint for lagring av filer?

Som en del av Microsoft 365-abonnementet ditt, gir organisasjonen deg OneDrive, din fillagring i skyen. OneDrive er privat som standard, der du organiserer innholdet og velger hvilke filer eller mapper som skal deles og med hvem. I SharePoint gir imidlertid et filbasert repositorium i skyen som deles med andre i organisasjonen.  

## <a name="does-prod_short-support-consumer-onedrive"></a>Støtter [!INCLUDE[prod_short](includes/prod_short.md)] OneDrive for forbruker?

Nei. Denne integreringen er utelukkende beregnet for OneDrive for Business og støtter bare arbeidskontoen din. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Støttes alle OneDrive for Business-planer?

[!INCLUDE[prod_short](includes/prod_short.md)] støtter ikke frittstående planer for OneDrive for Business. OneDrive må kjøpes som en del av en Microsoft 365 Business- eller Enterprise-plan. Hvis du vil ha mer informasjon, kan du se [Sammenlign priser og planer på skybasert OneDrive-lagring](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Hvor kan jeg se tilstanden til OneDrive-tjenesten?

Administratorer kan få tilgang til instrumentbordet for tjenestetilstand som en del av Microsoft 365-administrasjonssenteret. Instrumentbordet omfatter OneDrives tjenestetilgjengelighet. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>Er OneDrive-integrering tilgjengelig for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt?

Ja, men i motsetning til [!INCLUDE[prod_short](includes/prod_short.md)] online krever det tilleggsoppsett. Hvis du vil ha mer informasjon, kan du se [Konfigurering av Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>Bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt tilkobling med SharePoint Server?

Antall Denne distribusjonskombinasjonen støttes ikke selv om SharePoint Server har Mine områder aktivert.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>Bruker [!INCLUDE[prod_short](includes/prod_short.md)] online tilkobling med SharePoint Server?

Antall Denne distribusjonskombinasjonen støttes ikke selv om SharePoint Server har Mine områder aktivert.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Hvordan fungerer dette i en organisasjon med flere miljøer?

Integreringen antar at selskapsnavn er unike i alle [!INCLUDE[prod_short](includes/prod_short.md)]-miljøer. Når selskapsnavn er unike på tvers av organisasjonen, kopierre OneDrive filen til en mappe som er oppkalt etter det gjeldende selskapet når du åpner en fil. Hvis selskapsnavn ikke er unike i miljøer, blir filer fra identiske selskapsnavn plassert i samme mappe.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Vi har endret selskapsnavnet. Hva skjer med mine tidligere filer?

[!INCLUDE[prod_short](includes/prod_short.md)] overfører ikke filer du har åpnet tidligere, automatisk i OneDrive til den nye mappen. Når du har gitt nytt navn til selskapet, kopierer handlingen Åpne i OneDrive filer til en mappe med det nye selskapsnavnet.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Når jeg legger ved filer i [!INCLUDE[prod_short](includes/prod_short.md)], hvordan jeg velger jeg en fil fra OneDrive? 
[!INCLUDE[prod_short](includes/prod_short.md)] inneholder ikke en skyfilvelger. Du må laste ned filen fra OneDrive til enheten og deretter laste den opp til [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Jeg vil åpne filer i SharePoint i stedet. Hvordan gjør jeg dette?

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder ikke funksjoner for å kopiere filer til SharePoint og åpne dem fra et SharePoint-bibliotek. Kontakt Microsoft-partneren din for å forstå alternativene, eller søk etter apper på AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Hvordan slår jeg av integrering med OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)] online har ikke et alternativ for å aktivere eller deaktivere integrering til OneDrive.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Skal jeg bruke siden Tilkoblingsoppsett for SharePoint til å koble til SharePoint?

Dette er en eldre funksjon der alle [!INCLUDE[prod_short](includes/prod_short.md)]-filer fra alle brukere sendes til én enkelt SharePoint-mappe. Vi anbefaler at du ikke konfigurerer hurtigfanen Delte dokumenter på siden Tilkoblingsoppsett for SharePoint, fordi vi arbeider mot å avvikle denne funksjonen.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Hvilken versjon av [!INCLUDE[prod_short](includes/prod_short.md)] støtter OneDrive?

Integrering med OneDrive ble tilgjengelig i lanseringsbølge 2 for 2021.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Vil Microsoft fortsette å forbedre integreringen til OneDrive?

Hos Microsoft hører vi konstant på tilbakemelding fra våre mange brukerfellesskap og agerer på de mest populære forslagene. Hvis du vil vite mer om hva som kommer for integreringer med Microsoft 365-apper, kan du se [Lanseringsplanen for Dynamics 365](/dynamics365-release-plan/2021wave1).  

Hvis du ønsker å delta i å forbedre OneDrive-forbedring , eller hvis du har et forslag som vil forbedre fildeling og samarbeid i [!INCLUDE[prod_short](includes/prod_short.md)], kan du legge til et forslag eller stemme på eksisterende forslag på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="troubleshooting"></a>Feilsøking

Denne delen gir informasjon om hvordan du kan identifisere og løse problemer som kan oppstå når du bruker OneDrive med [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Jeg må logge hver gang jeg åpner en fil

Beklager, det er et kjent problem, og vi arbeider med det. Vi forventer å gi en jevnere opplevelse med en forestående oppdatering.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central finner ikke min OneDrive

Når du får meldingen «Finner ikke plasseringen til OneDrive for Business. Kontakt partneren din for å konfigurere dette»., må du kontrollere om brukeren har åpnet OneDrive minst én gang. Hvis brukeren ikke har det, kan du be vedkommende om å gå til portal.office.com/onedrive for å konfigurere det. Det kan ta litt tid. Hvis meldingen fremdeles vises etter 24 timer, kontakter du kundestøtte.  
 

## <a name="see-also"></a>Se også
[Business Central og OneDrive-integrering](across-onedrive-overview.md)  
[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
