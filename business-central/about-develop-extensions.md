---
title: Tilpasse Dynamics 365 Business Central | Microsoft-dokumentasjon
description: Bygg, vis og frem appen og utvidelsene dine for Business Central.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/12/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 69f660f8a19bd1fd9cb39a79d5be7977e68d3a47
ms.contentlocale: nb-no
ms.lasthandoff: 06/28/2018

---
# <a name="extending-included365finlongincludesd365finlongmdmd"></a>Utvide [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er en løsning for bedriftsadministrasjon som hjelper selskaper å knytte sammen økonomi, salg, service og drift for å strømlinjeforme forretningsprosesser, forbedre kundesamhandling og ta bedre beslutninger. [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er tilgjengelig i skyen og for brukere av forskjellige enheter som alltid er oppdatert. Med denne moderne forretningsplattformen kan du raskt og enkelt skreddersy, utvide og lage programmer slik at de passer til dine behov, med liten eller ingen kodeutvikling.  

Det finnes mange fordeler med å bruke [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] som en plattform for apputviklere, blant annet disse:

* Komme i gang med en sømløs introduksjonsopplevelse 
* Bruke Microsofts Go-To-Market-tjenester
* Tilpasse siden med appoversikten 
* Direkte kontakt med beslutningstakere og nå flere kunder
* Forbedre forretningsverdien og øke avtalestørrelsen med eksisterende og nye kunder
* Oppnå mer med en plattform som gir moderne opplevelse og tilbyr skala  
* Få innsikt i ytelsen til oppføringene dine via skypartnerportalen eller publiseringsprosessen for Office-apper.
* Sammen med intelligente businessapper som PowerApps, Flow, Power BI, Cortana Intelligence og mange flere  

Ta med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-tjenestene til Microsoft AppSource som: 

**Individuelle apper** – der du tar med bransjekunnskapen din til markedet.  
**Pakkede konsulenttjenester** – der du tar med ferdigpakkede engasjementer til markedet.

Med de nye utviklingsverktøyene kan du bygge utvidelser for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-brukere. Hvis du vil gjøre deg kjent med de nye verktøyene eller lære om utvidelser 2.0, kan du ta en titt her: [aka.ms/GetStartedWithApps](http://aka.ms/GetStartedWithApps).  

Finn opplysninger om apper og konsulenttjenester som er tilgjengelige i [Microsoft AppSource ](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1).

Microsoft har lagt til en katalog med konsulenttjenestetilbud for løsninger basert på [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], Power BI og PowerApps i AppSource som hjelper forretningsbrukere å komme raskt i gang. Lær mer om [konsulenttjenestene](/dynamics-nav/developer/readiness/readiness-consulting).

## <a name="choosing-which-services-to-offer-with-included365finlongincludesd365finlongmdmd"></a>Velge tjenestene som skal tilbys med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] 

### <a name="integrate-a-3rd-party-solution"></a>Integrere en tredjepartsløsning
[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] viser mange API-er som er klare til bruk for [tilkoblingsapper](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-connect-apps) for at integrasjonen mellom tjenesten og [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] skal bli sømløs. Du kan gruppere tjenestene sammen med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] og gi kundene en integrert opplevelse. Lær mer om å [integrere en tredjepartsløsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-thirdparty-solution).

### <a name="development-of-a-vertical-solution"></a>Utvikling av en vertikal løsning
Opprett en app som er spesialisert innen en bestemt bransje. Med [Bygg inn app](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-embed-apps) kan du utvide og tilpasse den eksisterende [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-applikasjonen og berike sluttbrukeropplevelsen med en bransjespesifikk funksjonalitet ved hjelp av nye og moderne utviklingsverktøy og utvidelsesversjon 2.0. Lær mer om [Utvikling av en vertikal løsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-vertical).

### <a name="development-of-a-horizontal-solution"></a>Utvikling av en horisontal løsning
Utvid opplevelsen og muligheten i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ved å opprette en [tilleggsapp](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-add-on-apps) som er integrert med brukeropplevelsen i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]. Bygg et grensesnitt som er basert på hvordan du vil at data skal flyte mellom [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] og tjenestene dine. Lær mer om [Utvikling av en horisontal løsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-horizontal). 

### <a name="development-of-a-localization-solution"></a>Utvikling av en lokaliseringsløsning
Overhold lokale lovmessige funksjoner ved å utvikle for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], som tilpasser funksjonsområder til kravene i det lokale markedet sammen med [Dynamics 365-oversettelsestjenesten](/dynamics365/unified-operations/dev-itpro/lifecycle-services/translation-service-overview). Juster sentrale funksjoner i henhold til lokale lovmessige krav, og utvid eksisterende funksjonalitet for å konkurrere på det lokale markedet. Lær mer om [Utvikling av en lokaliseringsløsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization).

### <a name="reseller-solution"></a>Forhandlerløsning
Ettersom hver virksomhet er unik, kan du med [Tilpasse leiere](/dynamics-nav/developer/readiness/readiness-customizing-tenants), tilpasse måten du arbeider på, til de strømlinjeformede prosessene, terminologien og hvordan de ansatte eller avdelingene har kontakt og samarbeider. I tillegg kan du videreselge og tilpasse [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] til kundenes individuelle behov ved å tilby [konsulenttjenester](/dynamics-nav/developer/readiness/readiness-consulting). Eller bruk Microsoft Flow, Power Apps og Power BI til å opprette [Tilpassede arbeidsflyter](/dynamics-nav/developer/readiness/readiness-no-code), apper og forretningsinnsiktsrapporter uten å skrive kode. Lær mer om [Dynamics 365 Reseller (VAR)](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-reseller). 

## <a name="where-do-i-learn-more"></a>Hvor finner jeg mer informasjon?
Hvis du vil lære mer om Microsoft-AppSource-konsulenttjenestetilbudene, velger du følgende koblinger: 

[Konsulenttilbud for AppSource](https://appsource.microsoft.com/en-us/marketplace/consulting-services?country=US&page=1)  
[Partnerberettigelse](https://smp-cdn-prod.azureedge.net/documents/Microsoft%20AppSource%20Partner%20Listing%20Guidelines.pdf)  
[Partnernomineringsskjema](https://appsource.microsoft.com/en-us/partners/list-consulting-service)  

## <a name="the-ready-to-go-program"></a>Ready to Go-programmet
Ready to Go-programmet er laget for å støtte deg når du skal ta med Microsoft [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-tilbudene dine til Microsoft Appsource. Programmet inneholder: 

- [Elektronisk opplæring](http://aka.ms/ReadyToGoOnlineLearning)
- [Opplæring og arbeidsgrupper](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go#the-ready-to-go-coaching)
- [Microsoft Collaborate-plattformen](http://aka.ms/Collaborate)

Lær mer om hvordan du kan lage et [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-tilbud i [Ready to Go-program](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-ready-to-go)-detaljene. Hvis du har spørsmål eller tilbakemelding om **Ready to Go**-programtilbudet, kan du [kontakte oss](mailto:dyn365bep@microsoft.com). 

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[https://appsource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365-for-financials&page=1)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

