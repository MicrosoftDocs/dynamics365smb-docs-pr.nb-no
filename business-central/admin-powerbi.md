---
title: Innføring i Business Central og Power BI
description: Få en oversikt over hvordan du bruker Power BI til å få innsikt, forretningsanalyse og KPI-er fra Business Central-data.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.search.form: 6316, 6317
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 74d51603f7675e7c4ba27bb78b6237a9241cb36e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129161"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] og Power BI

Det er enkelt å få innsikt i [!INCLUDE[prod_short](includes/prod_short.md)]-dataene med [Power BI](https://powerbi.microsoft.com) – et datavisualiseringssystem fra Microsoft. Power BI henter [!INCLUDE[prod_short](includes/prod_short.md)]-data, slik at du kan bygge instrumentbord og rapporter basert på disse dataene. Power BI gir deg et fleksibelt alternativ til rapporter som er bygget i [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan drille ned og tilpasse visualiseringen og til og med slå sammen data fra ulike selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]. Noen Power BI-rapporter kan også bygges inn i Business Central og vises uten å forlate systemet. Mer komplekse instrumentbord er bedre å oppleve fra Power BI-nettstedet.

![Power BI og Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Det du kan gjøre med Power BI og [!INCLUDE[prod_short](includes/prod_short.md)]

Det finnes ulike funksjoner for å arbeide med [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Du kan gjøre enkelte ting fra Power BI, mens andre ting gjør du fra [!INCLUDE[prod_short](includes/prod_short.md)]. I tillegg er noen funksjoner bare tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)] Online, ikke i den lokale versjonen. Du får en oversikt i tabellen nedenfor.

|Funksjon|Beskrivelse|Online|Lokalt|Mer informasjon|
|-------|-----------|--------------|-----------|----------------|
|Vis [!INCLUDE[prod_short](includes/prod_short.md)] data i Power BI.|Du kan vise dataene fra [!INCLUDE[prod_short](includes/prod_short.md)] i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] Online omfatter noen forhåndsdefinerte Power BI-rapporter. Det kan også hende at organisasjonen har gjort enkelte egendefinerte rapporter tilgjengelige for deg.|![Fungerer online.](media/check.png)|![Fungerer lokalt](media/check.png)|[Se ...](across-working-with-business-central-in-powerbi.md)|
|Vis Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter som viser [!INCLUDE[prod_short](includes/prod_short.md)]-data, kan bygges inn direkte i deler på [!INCLUDE[prod_short](includes/prod_short.md)]-sider. Du kan bytte del for å vise enhver rapport som er gjort tilgjengelig for deg. |![fungerer online.](media/check.png)|![Fungerer lokalt](media/check.png)<sup>[*](#onprem)</sup>|[Se ...](across-working-with-powerbi.md)|
|Opprett rapporter og instrumentbord i Power BI som viser [!INCLUDE[prod_short](includes/prod_short.md)]-dataene.|Bruk Power BI Desktop til å opprette egne rapporter og instrumentbord. Du kan publisere rapportene til din egen Power BI-tjeneste eller dele dem med andre i organisasjonen.|![Fungerer online.](media/check.png)|![fungerer lokalt](media/check.png)|[Se ...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-apper i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publiserer tre apper for Power BI på Microsoft AppSource. Disse appene oppretter detaljerte rapporter og instrumentbord i Power BI-tjenesten for å vise [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tilgjengelige apper omfatter følgende: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Fungerer online.](media/check.png)||[Se ...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Denne funksjonen krever et registrert program for Business Central i Microsoft Azure. Hvis du vil ha mer informasjon, kan du se [Registrere Business Central lokalt i Azure AD for integrering med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## <a name="getting-ready-to-use-power-bi"></a>Gjøre klart til bruk av Power BI

Det er noen få oppgaver du må gjøre før du kan begynne å bruke Power BI med [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> Oppgavene avhenger av din rolle i organisasjonen, og hva du vil gjøre med Power BI:

- Som en *forretningsbruker* ønsker du å vise Power BI-rapporter, enten i Power BI-tjenesten eller i Business Central
- Som *administrator* er du ansvarlig for å administrere innstillingene for hele organisasjonen, som styrer hvordan Business Central og Power BI fungerer.
- Som en *rapportoppretter* vil du lage egendefinerte Power BI-rapporter som du kan dele med andre brukere.

|Oppgave|Forretningsbruker|Administrator|Rapportoppretter|Mer informasjon|
|----|-------------|-------------|-----------------------|----------------|
|Få deg en Power BI-konto.|![enda en ny hake.](media/check.png)|![det er en hake](media/check.png)|![igjen en hake](media/check.png)|Gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Du registrerer deg for en konto ved å bruke e-postadressen og passordet for jobben din. <br /><br/>Registreringen krever at du har en lisens, men i de fleste tilfeller skal du allerede ha en gratis lisens. Hvis du vil ha mer informasjon, kan du se [Power BI-lisens](admin-powerbi-setup.md#license).|
|Skaff deg Power BI Desktop|||![igjen en hake.](media/check.png)|Hvis du vil laste ned, går du til [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Hvis du vil ha mer informasjon, kan du se [Få Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Eksponer Business Central-data til Power BI||![det er en hake.](media/check.png)|![igjen en hake](media/check.png)|[Eksponer data gjennom API-sider eller OData-nettjenester](admin-powerbi-setup.md#exposedata)
|Aktiver Power BI-integrering<br />(bare lokalt)||![det er en hake.](media/check.png)||[Konfigurer Business Central lokalt for Power BI-integrering](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Ved hjelp av [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]