---
title: Konfigurer et selskap med RapidStart Services
description: Du kan sette opp et nytt selskap i Business Central med RapidStart Services for å øke produktiviteten ved å automatisere og forenkle regelmessige oppgaver.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518314"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Konfigurer et selskap med RapidStart Services

Du kan opprette et nytt selskap i [!INCLUDE[prod_short](includes/prod_short.md)] med RapidStart Services. RapidStart Services er et verktøy som er utviklet for å forkorte distribusjonstiden, forbedre kvaliteten på implementeringen, introdusere en implementeringsmetode som kan gjentas og øke produktiviteten ved å automatisere og forenkle regelmessige oppgaver.  

Bruk disse funksjonene til å skalere bedriften som en forhandler. De fleste av de relevante sidene gjelder både [!INCLUDE [prod_short](includes/prod_short.md)] på nettet og lokalt. Noen prosesser bruker imidlertid tilgang til filer på disken og er for komplekse til å kunne brukes for [!INCLUDE [prod_short](includes/prod_short.md)] på nettet. For [!INCLUDE [prod_short](includes/prod_short.md)] lokalt ønsker du sannsynligvis å bruke Windows PowerShell til å hjelpe deg med å distribuere. Hvis du vil ha mer informasjon, kan du se [Administrasjon av Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/administration) og [Administrasjon av Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).  

RapidStart Services hjelper deg å få oversikt over installasjonsprosessen for det nye selskapet ved å tilby et forslag hvor du kan definere tabellene som ofte er involvert prosessen med konfigurasjon av nye selskaper. Mens du gjør dette, kan du opprette et spørreskjema for å lede kundene gjennom samling av oppsettsinformasjon. Kundene har muligheten til å bruke spørreskjemaet til å installere modulene, eller de kan åpne installasjonssiden direkte og gjennomføre installasjonen der. Viktigst av alt, RapidStart Services hjelper deg som kunde å forberede selskapet med standard oppsettsdata som du kan finjustere og tilpasse. Til slutt, når du bruker RapidStart Services, kan du konfigurere og flytte eksisterende kundedata, for eksempel en liste over kunder eller varer, til det nye selskapet.

Du kan bruke følgende komponenter for å få et raskere oppsett av selskapet:  

- Konfigurasjonsveiviser  
- Konfigurasjonsforslag  
- Konfigurasjonspakker  
- Konfigurasjonsmaler  
- Konfigurasjonsspørreskjema  

> [!Note]  
> Det finnes moduler i [!INCLUDE[prod_short](includes/prod_short.md)] som må konfigureres manuelt. Disse inkluderer å legge til brukere, definere regnskapsperioder og definere dimensjoner for forretningsintelligens. Hvis du vil ha mer informasjon, kan du se [Definere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emner som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Opprett et nytt selskap, og importer grunnleggende oppsettsdata og maler.|[Definere selskapskonfigurasjon](admin-set-up-company-configuration.md)|  
|Distribuer den konfigurerte pakken til kunden for implementering.|[Bruke konfigurasjoner for nye selskaper](admin-apply-configuration-to-new-companies.md)|
|Definer og valider kundens oppsettsverdier for alle kjerneområder, for eksempel selskapsopplysninger, finans, lager, salg eller produksjon.|[Samle oppsettsverdier for kunde](admin-gather-customer-setup-values.md)|  
|Konfigurer kjernehoveddataposter som bruker maler, for å klargjøre overføring av eksisterende kundedata.|[Klargjøre for å flytte kundedata](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Definer tabeller og felt, valider eksisterende kundedata, og overfør data til [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.|[Flytte kundedata](admin-migrate-customer-data.md)|
|Klargjør for gjenbruk av firmakonfigurasjoner i andre selskaper (i utvikler- og administrasjonsinnholdet).|[Opprett egendefinerte konfigurasjonspakker for selskap](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Finn løsninger på kjente problemer i RapidStart Services-verktøyet.|[Tips og triks: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]