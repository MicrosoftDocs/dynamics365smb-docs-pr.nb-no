---
title: Aktiver Power BI-integrering med Business Central
description: 'Lær hvordan du konfigurerer tilkoblingen til Power BI. Med Power BI-rapporter kan du få innsikt, forretningsanalyse og nøkkelindikatorer fra Business Central-dataene.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
---
# <a name="enabling-power-bi-integration-with-"></a>Aktiver Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Denne artikkelen beskriver hvordan du klargjør [!INCLUDE[prod_short](includes/prod_short.md)] for integrering med Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] Online er allerede aktivert for integrering, selv om det er en del lisensieringsinformasjon du kanskje bør lese. For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt må du konfigurere miljøet slik at det kobler til Power BI, før brukerne kan arbeide med det.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-lisensiering

Med [!INCLUDE[prod_short](includes/prod_short.md)] får brukere en gratis Power BI-lisens som gir tilgang til de vanligste funksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Du kan også kjøpe en Power BI Pro-lisens som gir tilgang til ytterligere funksjoner. Tabellen nedenfor inneholder en oversikt over hvilke funksjoner som er tilgjengelige for hver enkelt lisens.

|Power-lisens|Vise rapporter|Opprette rapporter|Dele rapporter|Oppdatere rapporter| [!INCLUDE[prod_short](includes/prod_short.md)]-apper|
|-------------|--------||
|Power BI free|![en hake.](media/check.png)|![en ny hake](media/check.png)|(begrenset)|(begrenset)||
|Power BI Pro|![enda en ny hake.](media/check.png)|![det er en hake](media/check.png)|![igjen en hake](media/check.png)|(omfattende)|![siste hake](media/check.png)|

Hvis du vil ha mer informasjon, kan du se [Lisensiere Power BI-tjenesten for brukere i organisasjonen](/power-bi/admin/service-admin-licensing-organization) eller [Registrere deg for Power BI-tjenesten som enkeltperson](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Eksponer data gjennom API- eller OData-nettjenester

Business Central tilbyr to måter å vise data på som kan forbrukes av Power BI-rapporter: API-sider eller -spørringer og nettjenester for åpne dataprotokoller (OData).

### <a name="api-pages-and-queries"></a>API-sider og -spørringer

> **GJELDER:** bare Business Central Online

Utviklere kan definere sideobjekter og spørringsobjekter av typen *API*. På denne måten kan de vise data fra databasetabeller via en webhook-støttet, OData v4-aktivert, REST-tjeneste. Denne datatypen kan ikke vises i brukergrensesnittet, men er ment for å utvikle pålitelige integrasjonstjenester.

Business Central online leveres med et sett med innebygde API-er, som du kan bruke til å hente data for de mest vanlige forretningsenhetene, for eksempel kunder, varer, ordrer og så videre. Ekstra arbeid eller oppsett er ikke nødvendig for å bruke disse API-ene som en datakilde for Power BI-rapporter. Se [Business Central API v 2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) hvis du vil ha mer informasjon om disse API-ene.

Business Central online støtter også egen definerte API-er. Programutviklere for Business Central-løsninger kan opprette egne API-sider og -spørringer og pakke dem i apper. Du installerer deretter appene i leietakeren. Når den er installert, kan du bruke API-sidene for Power BI-rapportene, på samme måte som med de innebygde API-ene (v 2.0). Hvis du vil ha mer informasjon om hvordan du oppretter en API ved å eksponere sider eller spørringer, kan du se [Utvikle en egendefinert API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Fra og med februar 2022 blir Power BI-rapporter for [!INCLUDE[prod_short](includes/prod_short.md)] online hentet fra en sekundær, skrivebeskyttet databasereplika for ytelsesårsaker. I følge tilfeller bør AL-utviklere unngå å utforme API-sider som gjør databaseendringer mens sidene åpnes eller laster inn poster. Tenk særlig på koden på AL-utløserne: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord. Disse databaseendringene kan i noen tilfeller forårsake ytelsesproblemer og forhindre at rapporten oppdaterer data. Hvis du vil ha mer informasjon, kan du se [Ytelsesartikler for utviklere](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) i utviklingsinnholdet for Business Central.
>
> I sjeldne tilfeller vil virkemåten føre til en feil når en bruker prøver å hente data fra API for en rapport i Power BI Desktop. Hvis databaseendringer er nødvendige på den egendefinerte API, kan Power BI Desktop-brukerne imidlertid fremtvinge virkemåten. Hvis du vil ha mer informasjon, kan du se [Bygg Power BI-rapporter for å vise Business Central-data](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>OData-nettjenester

Du kan publisere Business Central-programobjekter, for eksempel codeunit, sider og spørringer, som [OData-nettjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Med Business Central online blir det publisert mange nettjenester som standard. Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Webtjenester** kontrollerer du at **Publiser**-feltet er valgt for webtjenestene som er oppført ovenfor. Hvis du vil ha mer informasjon om publisering av webtjenester, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

Hvis du vil vite mer om hva du kan gjøre for å sikre den beste ytelsen til webtjenester, sett fra Business Central-serveren (endepunktet) og fra forbrukeren (klienten), kan du lese [Skrive effektive webtjenester](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Velg om du vil bruke API-sider eller OData-nettjenester

Når det er mulig, oppfordrer vi til å bruke API-sider i stedet for OData-nettjeneste. API-sider er raskere ved innlasting av data i Power BI-rapporter enn OData-nettjenester. I tillegg er de mer fleksible fordi de lar deg hente data fra tabellfelter som ikke er definert i et sideobjekt.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## <a name="setting-up-dataflows"></a>Konfigurer dataflyt

Med dataflytprosesser kan du inkludere, transformere og laste inn data i et Power BI-arbeidsområde og deretter bruke dataene som grunnlag for rapportene. Disse dataflytene kan i noen tilfeller oppleve forbigående feil under en planlagt oppdatering. Feilmeldingen ser slik ut: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

Ved hjelp av Power Automate kan du konfigurere nye forsøk for denne situasjonen. Hvis du vil ha mer informasjon, kan du se [Prøv en dataflyt på nytt automatisk ved feil](/power-query/dataflows/automatically-retry-dataflow).

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
