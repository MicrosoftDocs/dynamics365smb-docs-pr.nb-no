---
title: Koble deg til Power BI fra Business Central lokalt | Microsoft Docs
description: 'Få innsikt, forretningsanalyse og KPI-er fra Business Central-dataene ved å bruke Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="connect-to-power-bi-from-business-central-on-premises"></a>Koble deg til Power BI fra Business Central lokalt

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## <a name="get-ready"></a>Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## <a name="get-started"></a>Kom i gang

Hvis du bruker [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, må den aktiveres for Power BI-integrering. Denne oppgaven utføres vanligvis av en administrator. Hvis du vil ha mer informasjon om hvordan du aktiverer Power BI-integrering med Business Central Online, kan du se [Konfigurer Business Central lokalt for Power BI-integrering](admin-powerbi-setup.md).

Enkelte funksjoner bare tilgjengelige i Business Central Online, ikke i den lokale versjonen. Hvis du vil ha mer informasjon, kan du se [Innføring i Business Central og Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="set-up--on-premises-for-power-bi-integration"></a><a name="setup"></a>Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for Power BI-integrering

Denne delen forklarer kravene til integrering av en distribusjon av [!INCLUDE[prod_short](includes/prod_short.md)] lokalt med Power BI.

1. Konfigurer enten [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) eller [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) som godkjenningsmetode for distribusjonen.  
    
    > [!NOTE]
    > Power BI-integrering støtter ikke Windows-godkjenning og støttes ikke på Windows-klienten.

2. Aktiver OData-nettjenester og ODataV4-endepunktet.

    OData-nettjenester må være aktivert på [!INCLUDE[server](includes/server.md)], og OData-porten må være åpnet i brannmuren. Hvis du vil ha mer informasjon, kan du se [Konfigurere Business Central Server – OData-nettjenester](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Den lokale serveren må være tilgjengelig fra Internett.

3. Gi [!INCLUDE[prod_short](includes/prod_short.md)]-brukerkontoer en tilgangsnøkkel for webtjeneste.

    En tilgangsnøkkel for webtjeneste kreves bare for å vise [!INCLUDE[prod_short](includes/prod_short.md)]-data i Power BI. Du kan tilordne en tilgangsnøkkel for webtjeneste til hver brukerkonto. Eller du kan i stedet opprette en bestemt konto med en tilgangsnøkkel for webtjeneste som kan brukes av alle brukere. Hvis du vil ha mer informasjon, kan du se [Godkjenning av webtjenester](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Opprett en programregistrering for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure.

    Hvis du vil vise Power BI-rapporter som er innebygd på [!INCLUDE[prod_short](includes/prod_short.md)]-sider, må det registreres et program for [!INCLUDE[prod_short](includes/prod_short.md)] i Microsoft Azure. Det registrerte programmet trenger tillatelse til Power BI-tjenestene. Appen krever som et minimum tillatelsen **User.ReadWrite.All**. For at brukere skal kunne vise rapporter fra delte Power BI-arbeidsområder, krever appen tillatelsen **Workspace.Read.All**. Hvis du vil ha mer informasjon, kan du se [Registrere [!INCLUDE[prod_short](includes/prod_short.md)] lokalt i Microsoft Entra ID for integrering med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Hvis distribusjonen bruker NavUserPassword-godkjenning, kobles [!INCLUDE[prod_short](includes/prod_short.md)] til den samme Power BI-tjenesten for alle brukere. Du angir denne tjenestekontoen som en del av registreringen av programmet. Med Microsoft Entra-godkjenning kobles [!INCLUDE[prod_short](includes/prod_short.md)] til Power BI-tjenesten som er knyttet til de enkelte brukerkontoene.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Foreta den første tilkoblingen fra Business Central til Power BI.

    Før sluttbrukere kan bruke Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], må en administrator av Azure-programmet gi samtykke til Power BI-tjenesten.

    For å opprette den første tilkoblingen må du åpne [!INCLUDE[prod_short](includes/prod_short.md)] og kjøre **Kom i gang med Power BI** fra startsiden. Denne handlingen leder deg gjennom samtykkeprosessen og kontrollerer Power BI-lisensen. Logg deg på med en Microsoft Entra-administratorkonto når du blir bedt om det. Hvis du vil ha mer informasjon, kan du se [Koble til Power BI – kun én gang](across-working-with-powerbi.md#connect).

## <a name="build-power-bi-reports-to-display--data"></a>Bygg Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data

Gjør Dynamics 365 Business Central-dataene tilgjengelige som en datakilde i Power BI Desktop, og bygg kraftige rapporter om status for din bedrift.

Bruk Power BI Desktop til å opprette rapporter som viser Dynamics 365 Business Central-data. Når du har opprettet rapporter, kan du publisere dem i Power BI-tjenesten eller dele dem med alle brukerne i organisasjonen. Når disse rapportene er i Power BI-tjenesten, kan brukerne som er konfigurert for den, vise rapportene i Dynamics 365 Business Central.

- Hent følgende informasjon for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt:

  - OData URL-adressen for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Denne nettadressen har vanligvis formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for eksempel `https://localhost:7048/BC190/ODataV4`. Hvis du har en distribusjon med flere leietakere, tar du med leietakeren i nettadressen, for eksempel `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Et brukernavn og en tilgangsnøkkel for webtjeneste for en [!INCLUDE[prod_short](includes/prod_short.md)]-konto.

    Power BI bruker enkel godkjenning til å hente data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Så du trenger et brukernavn og en tilgangsnøkkel for webtjeneste for å koble til. Kontoen kan være din egen brukerkonto, eller organisasjonen kan ha en bestemt konto for dette formålet.

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop

Den første oppgaven i opprettelse av rapporter, er å legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop. Når den er tilkoblet, kan du begynne å bygge rapporten.

1. Start Power BI Desktop.
2. Velg **Hent data**.

    Hvis du ikke ser **Hent data**, velger du **Fil**-menyen og deretter **Hent data**.
3. På **Hent data**-siden velger du **Online Services**.
4. I ruten **Nettbaserte tjenester** kobler du til [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, velger **Dynamics 365 Business Central (on-premises)** og deretter **Koble til**.
5. Logg på [!INCLUDE [prod_short](includes/prod_short.md)] (bare én gang).

    Hvis du ikke er logget på [!INCLUDE [prod_short](includes/prod_short.md)] fra Power BI Desktop før, blir du bedt om å logge på.

   - For [!INCLUDE [prod_short](includes/prod_short.md)] lokal skriver du først inn URL-adressen OData for [!INCLUDE[prod_short](includes/prod_short.md)] og deretter velger du **OK**. Når du blir bedt om det, skriver du inn brukernavnet og passordet for kontoen du vil bruke til å koble til [!INCLUDE[prod_short](includes/prod_short.md)]. I **Passord**-boksen angir du tilgangsnøkkelen for webtjeneste. Velg **Koble til** når du er ferdig.
   
    > [!NOTE]  
    > Når du er koblet til [!INCLUDE[prod_short](includes/prod_short.md)], blir du ikke bedt på nytt om å logge på. [Hvordan endrer eller tømmer jeg kontoen jeg for øyeblikket bruker til koble til Business Central fra Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Når du er tilkoblet, kontakter Power BI Business Central-tjenesten. **Navigatør**-vinduene vises og viser tilgjengelige datakilder for bygging av rapporter. Velg en mappe for å utvide den, og se de tilgjengelige datakildene. 

   Disse datakildene representerer alle nettjenestene og API-sidene som er publisert for [!INCLUDE [prod_short](includes/prod_short.md)]. Datakildene er gruppert etter Business Central-miljøer og -selskaper.

   > [!NOTE]
    > Strukturen for Business Central lokal er forskjellig, fordi den ikke støtter API-sider.

7. Velg datakilden eller -kildene du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
8. Hvis du senere vil legge til flere Business Central-data, kan du gjenta trinnene ovenfor.

Når dataene er lastet inn, kan du se dem i høyre navigering på siden. Nå har du koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-dataene, og du kan begynne å bygge Power BI-rapporten.  

> [!TIP]
> Hvis du vil ha mer informasjon om hvordan du bruker Power BI Desktop, kan du se [Kom i gang med Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="manage-and-modify-reports"></a>Behandle og endre rapporter

> [!NOTE]
> Du kan ikke behandle og endre rapporter. 

## <a name="upload-reports"></a>Laste opp rapporter

For [!INCLUDE [prod_short](includes/prod_short.md)] lokalt er det ingen tilgjengelige demorapporter, så du må starte fra bunnen av ved å bruke Power BI Desktop. Alternativt kan Power BI-rapporter distribueres som filer du kan laste opp direkte fra Power BI-nettjeneste. Hvis du vil ha mer informasjon, kan du se [Laste opp rapporten til tjenesten](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### <a name="refresh-manually"></a>Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### <a name="schedule-a-refresh"></a>Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
[Last opp rapport fra filer](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
