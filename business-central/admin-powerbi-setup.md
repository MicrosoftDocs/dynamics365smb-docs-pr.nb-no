---
title: Aktivere Power BI-integrering med Business Central
description: Lær hvordan du konfigurerer tilkoblingen til Power BI, slik at du får innsikt, forretningsintelligens og KPI-er fra Business Central-data med Business Central-appene for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 17e41dd44dd4f7f99eabd4904d5ebd7c48d9964d
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5492984"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Aktivere Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)]

Denne artikkelen beskriver hvordan du klargjør [!INCLUDE[prod_short](includes/prod_short.md)] for integrering med Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] Online er allerede aktivert for integrering, selv om det er en del lisensieringsinformasjon du kanskje bør lese. For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt må du konfigurere miljøet slik at det kobler til Power BI, før brukerne kan arbeide med det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-lisensiering

Med [!INCLUDE[prod_short](includes/prod_short.md)] får brukere en gratis Power BI-lisens som gir tilgang til de vanligste funksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Du kan også kjøpe en Power BI Pro-lisens som gir tilgang til ytterligere funksjoner. Tabellen nedenfor inneholder en oversikt over hvilke funksjoner som er tilgjengelige for hver enkelt lisens.

|Power-lisens|Vise rapporter|Opprette rapporter|Dele rapporter|Oppdatere rapporter| [!INCLUDE[prod_short](includes/prod_short.md)]-apper|
|-------------|--------||
|Power BI free|![en hake](media/check.png)|![en ny hake](media/check.png)|(begrenset)|(begrenset)||
|Power BI Pro|![enda en ny hake](media/check.png)|![det er en hake](media/check.png)|![igjen en hake](media/check.png)|(omfattende)|![siste hake](media/check.png)|

Hvis du vil ha mer informasjon, kan du se [Lisensiere Power BI-tjenesten for brukere i organisasjonen](/power-bi/admin/service-admin-licensing-organization) eller [Registrere deg for Power BI-tjenesten som enkeltperson](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for Power BI-integrering

Denne delen forklarer kravene til integrering av en distribusjon av [!INCLUDE[prod_short](includes/prod_short.md)] lokalt med Power BI.

1. Konfigurer enten NavUserPassword eller Azure Active Directory-godkjenning for distribusjonen.

    Power BI-integrering støtter ikke Windows-godkjenning.  

2. Aktiver OData-nettjenester og ODataV4-endepunktet.

    OData-nettjenester må være aktivert på [!INCLUDE[server](includes/server.md)], og OData-porten må være åpnet i brannmuren. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server – OData-nettjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokale serveren må være tilgjengelig fra Internett.

3. Gi [!INCLUDE[prod_short](includes/prod_short.md)]-brukerkontoer en tilgangsnøkkel for webtjeneste.

    En tilgangsnøkkel for webtjeneste kreves bare for å vise [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tilordne en tilgangsnøkkel for webtjeneste til hver brukerkonto. Eller du kan i stedet opprette en bestemt konto med en tilgangsnøkkel for webtjeneste som kan brukes av alle brukere. Hvis du vil ha mer informasjon, kan du se [Godkjenning av webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Opprett en programregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    Hvis du vil vise Power BI-rapporter som er innebygd på [!INCLUDE[prod_short](includes/prod_short.md)]-sider, må et program være registrert for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure. Det registrerte programmet trenger tillatelse til Power BI-tjenestene. Hvis du vil ha mer informasjon, kan du se [Registrere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt i Azure AD for integrering med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis distribusjonen bruker NavUserPassword-godkjenning, kobles [!INCLUDE[prod_short](includes/prod_short.md)] til den samme Power BI-tjenesten for alle brukere. Du angir denne tjenestekontoen som en del av registreringen av programmet. Med Azure AD-godkjenning kobles [!INCLUDE[prod_short](includes/prod_short.md)] til Power BI-tjenesten som er knyttet til de enkelte brukerkontoene.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Foreta den første tilkoblingen fra Business Central til Power BI.

    Før sluttbrukere kan bruke Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], må en administrator av Azure-programmet gi samtykke til Power BI-tjenesten.

    For å opprette den første tilkoblingen må du åpne [!INCLUDE[prod_short](includes/prod_short.md)] og kjøre **Kom i gang med Power BI** fra rollesenteret. Denne handlingen leder deg gjennom samtykkeprosessen og kontrollerer Power BI-lisensen. Logg deg på med en Azure-administratorkonto når du blir bedt om det. Hvis du vil ha mer informasjon, kan du se [Koble til Power BI – kun én gang](across-working-with-powerbi.md#connect).

## <a name="publish-data-as-web-services"></a>Publisere data som webtjenester

Kodeenheter, sider og spørringer du vil bruke som datakilden i Power BI-rapporter, må publiseres som webtjenester. Mange webtjenester er publisert som standard. Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Webtjenester** kontrollerer du at **Publiser**-feltet er valgt for webtjenestene som er oppført ovenfor. Denne oppgaven er vanligvis en administrativ oppgave.

Hvis du vil ha mer informasjon om publisering av webtjenester, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

> [!TIP]
> Hvis du vil vite mer om hva du kan gjøre for å sikre den beste ytelsen til webtjenester, sett fra Business Central-serveren (endepunktet) og fra forbrukeren (klienten), kan du lese [Skrive effektive webtjenester](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Ved hjelp av [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]