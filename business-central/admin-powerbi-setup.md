---
title: Aktivere Power BI-integrering med Business Central | Microsoft Docs
description: Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Business Central-apper for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 92b3bb1d04c58332db20c978928fe1b04ed2ab37
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697780"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Aktivere Power BI-integrering med [!INCLUDE[prodshort](includes/prodshort.md)]

Denne artikkelen beskriver hvordan du klargjør [!INCLUDE[prodshort](includes/prodshort.md)] for integrering med Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] Online er allerede aktivert for integrering, selv om det er en del lisensieringsinformasjon du kanskje bør lese. For [!INCLUDE[prodshort](includes/prodshort.md)] lokalt må du konfigurere miljøet slik at det kobler til Power BI, før brukerne kan arbeide med det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-lisensiering

Med [!INCLUDE[prodshort](includes/prodshort.md)] får brukere en gratis Power BI-lisens som gir tilgang til de vanligste funksjonene i [!INCLUDE[prodshort](includes/prodshort.md)] og Power BI. Du kan også kjøpe en Power BI Pro-lisens som gir tilgang til ytterligere funksjoner. Tabellen nedenfor inneholder en oversikt over hvilke funksjoner som er tilgjengelige for hver enkelt lisens.

|Power-lisens|Vise rapporter|Opprette rapporter|Dele rapporter|Oppdatere rapporter| [!INCLUDE[prodshort](includes/prodshort.md)]-apper|
|-------------|--------||
|Power BI free|![avmerking](media/check.png)|![avmerking](media/check.png)|(begrenset)|(begrenset)||
|Power BI Pro|![avmerking](media/check.png)|![avmerking](media/check.png)|![avmerking](media/check.png)|(omfattende)|![avmerking](media/check.png)|

Hvis du vil ha mer informasjon, kan du se [Lisensiere Power BI-tjenesten for brukere i organisasjonen](/power-bi/admin/service-admin-licensing-organization) eller [Registrere deg for Power BI-tjenesten som enkeltperson](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurere [!INCLUDE[prodshort](includes/prodshort.md)] lokalt for Power BI-integrering

Denne delen forklarer kravene til integrering av en distribusjon av [!INCLUDE[prodshort](includes/prodshort.md)] lokalt med Power BI.

1. OData-nettjenester og ODataV4-endepunktet er aktivert.

    OData-nettjenester må være aktivert på [!INCLUDE[server](includes/server.md)], og OData-porten må være åpnet i brannmuren. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server – OData-nettjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Den lokale serveren må være tilgjengelig fra Internett.

2. [!INCLUDE[prodshort](includes/prodshort.md)]-brukerkontoer har tilgangsnøkkel for webtjeneste.

    En tilgangsnøkkel for webtjeneste kreves for å vise [!INCLUDE[prodshort](includes/prodshort.md)]-data i Power BI. Du kan tilordne en tilgangsnøkkel for webtjeneste til hver brukerkonto. Eller du kan i stedet opprette en bestemt konto med en tilgangsnøkkel for webtjeneste som kan brukes av alle brukere. Hvis du vil ha mer informasjon, kan du se [Godkjenning av webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. NavUserPassword- eller Azure Active Directory-godkjenning er konfigurert.

4. Hvis du vil vise Power BI-rapporter som er innebygd på [!INCLUDE[prodshort](includes/prodshort.md)]-sider, må det registreres et program for [!INCLUDE[prodshort](includes/prodshort.md)] i Microsoft Azure.

    Det registrerte programmet trenger tillatelse til Power BI-tjenestene. Hvis du vil ha mer informasjon, kan du se [Registrere [!INCLUDE[prodshort](includes/prodshort.md)] lokalt i Azure AD for integrering med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis distribusjonen bruker NavUserPassword-godkjenning, kobles [!INCLUDE[prodshort](includes/prodshort.md)] til den samme Power BI-tjenesten for alle brukere. Du angir denne tjenestekontoen som en del av registreringen av programmet. Med Azure AD-godkjenning kobles [!INCLUDE[prodshort](includes/prodshort.md)] til Power BI-tjenesten som er knyttet til de enkelte brukerkontoene.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Publisere data som webtjenester

Kodeenheter, sider og spørringer du vil bruke som datakilden i Power BI-rapporter, må publiseres som webtjenester. Mange webtjenester er publisert som standard. Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prodshort](includes/prodshort.md)]. På siden **Webtjenester** kontrollerer du at **Publiser**-feltet er valgt for webtjenestene som er oppført ovenfor. Denne oppgaven er vanligvis en administrativ oppgave.

Hvis du vil ha mer informasjon om publisering av webtjenester, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

> [!TIP]
> Hvis du vil vite mer om hva du kan gjøre for å sikre den beste ytelsen til webtjenester, sett fra Business Central-serveren (endepunktet) og fra forbrukeren (klienten), kan du lese [Skrive effektive webtjenester](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Ved hjelp av [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
