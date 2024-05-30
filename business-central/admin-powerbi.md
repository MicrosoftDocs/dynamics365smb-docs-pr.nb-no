---
title: Innføring i Business Central og Power BI
description: Få en oversikt over hvordan du bruker Power BI til å få innsikt og KPI-er fra Business Central-data.
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Innføring i Business Central og Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Det er enkelt å få innsikt i [!INCLUDE[prod_short](includes/prod_short.md)]-dataene med [Power BI](https://powerbi.microsoft.com) – et datavisualiseringssystem fra Microsoft. Power BI henter [!INCLUDE[prod_short](includes/prod_short.md)]-data slik at du kan bygge instrumentbord og rapporter basert på disse dataene. Power BI gir deg et fleksibelt alternativ til rapporter som er bygget i [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan drille ned og tilpasse visualiseringen og til og med slå sammen data fra ulike selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]. Noen Power BI-rapporter kan også bygges inn i Business Central og vises uten å forlate systemet. Mer komplekse instrumentbord er bedre å oppleve fra Power BI-nettstedet.

![Power BI og Business Central.](media/power-bi-intro.png)

## Hva du kan gjøre med Power BI og Business Central

Det finnes ulike funksjoner for å arbeide med [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Du kan gjøre enkelte ting fra Power BI, mens andre ting gjør du fra [!INCLUDE[prod_short](includes/prod_short.md)]. I tillegg er noen funksjoner bare tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)] Online, ikke i den lokale versjonen. Du får en oversikt i tabellen nedenfor.

|Funksjon|Description|Online|Lokal|Finn ut mer|
|-------|-----------|--------------|-----------|----------------|
|Vis [!INCLUDE[prod_short](includes/prod_short.md)] data i Power BI.|Du kan vise dataene fra [!INCLUDE[prod_short](includes/prod_short.md)] i rapporter i Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] Online omfatter noen forhåndsdefinerte Power BI-rapporter. Det kan også hende at organisasjonen har enkelte egendefinerte rapporter.|![Fungerer online.](media/check.png)|![Fungerer lokalt](media/check.png)|[Her ...](across-working-with-powerbi.md)|
|Vis Power BI-rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.| Power BI-rapporter som viser [!INCLUDE[prod_short](includes/prod_short.md)]-data, kan bygges inn direkte i deler på [!INCLUDE[prod_short](includes/prod_short.md)]-sider. Du kan bytte del for å vise enhver rapport som er gjort tilgjengelig for deg. |![fungerer online.](media/check.png)|![Fungerer lokalt](media/check.png)<sup>[*](#onprem)</sup>|[Her ...](across-working-with-powerbi.md).|
|Opprett rapporter og instrumentbord i Power BI som viser [!INCLUDE[prod_short](includes/prod_short.md)]-dataene.|Bruk Power BI Desktop til å opprette egne rapporter og instrumentbord. Du kan publisere rapportene til din egen Power BI-tjeneste eller dele dem med andre i organisasjonen.|![Fungerer online.](media/check.png)|![fungerer lokalt](media/check.png)|[Her ...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)]-apper i Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publiserer tre apper for Power BI på Microsoft AppSource. Disse appene oppretter detaljerte rapporter og instrumentbord i Power BI-tjenesten for å vise [!INCLUDE[prod_short](includes/prod_short.md)]-data. Tilgjengelige apper omfatter følgende: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] – CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] – Sales </li></ul>  |![Fungerer online.](media/check.png)||[Her ...](across-powerbi-business-central-apps.md)|
|Arbeid med [!INCLUDE [prod_short](includes/prod_short.md)]-data i datatorg og dataflyt|Fra og med juli 2022 kan du bruke [!INCLUDE [prod_short](includes/prod_short.md)]-koblingen i Power Query Online på dataflytprosesser som du deler på tvers av forskjellige rapporter og instrumentbord.|![fungerer online.](media/check.png)||[Her ...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Denne funksjonen krever et registrert program for Business Central i Microsoft Azure. Hvis du vil ha mer informasjon, kan du se [Registrer Business Central lokalt i Microsoft Entra ID for integrering med andre tjenester](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## Gjør deg klar til å bruke Power BI

Det er noen få oppgaver du må gjøre før du kan begynne å bruke Power BI med [!INCLUDE[prod_short](includes/prod_short.md)].<!-- Some of the tasks are typically only done by administrators or super users.--> Oppgavene avhenger av din rolle i organisasjonen, og hva du vil gjøre med Power BI:

- Som en *forretningsbruker* ønsker du å vise Power BI-rapporter, enten i Power BI-tjenesten eller i Business Central
- Som *administrator* er du ansvarlig for å administrere innstillingene for hele organisasjonen, som styrer hvordan Business Central og Power BI fungerer.
- Som en *rapportoppretter* vil du lage egendefinerte Power BI-rapporter som du kan dele med andre brukere.

|Oppgave|Forretningsbruker|Administrator|Rapportoppretter|Mer informasjon|
|----|-------------|-------------|-----------------------|----------------|
|Få deg en Power BI-konto.|![enda en ny hake.](media/check.png)|![det er en hake](media/check.png)|![igjen en hake](media/check.png)|Gå til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Du registrerer deg for en konto ved å bruke e-postadressen og passordet for jobben din. <br /><br/>Registreringen krever at du har en lisens, men i de fleste tilfeller skal du allerede ha en gratis lisens. Hvis du vil ha mer informasjon, kan du se [Power BI-lisens](admin-powerbi-setup.md#license).|
|Skaff deg Power BI Desktop|||![igjen en hake.](media/check.png)|Hvis du vil laste ned, går du til [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Hvis du vil ha mer informasjon, kan du se [Få Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).
|Eksponer Business Central-data til Power BI||![det er en hake.](media/check.png)|![igjen en hake](media/check.png)|[Eksponer data gjennom API-sider eller OData-nettjenester](admin-powerbi-setup.md#exposedata)
|Aktiver Power BI-integrering<br />(bare lokalt)||![det er en hake.](media/check.png)||[Konfigurer Business Central lokalt for Power BI-integrering](across-working-with-business-central-in-powerbi.md#setup)|


## Neste trinn

- Hvis du er administrator som må konfigurere Power BI i [!INCLUDE[prod_short](includes/prod_short.md)], går du til [Aktiver Power BI-integrering](admin-powerbi-setup.md).
- Hvis Power BI allerede er definert og du vil prøve funksjonene, går du til [Arbeid med Power BI-rapporter i Business Central](across-working-with-powerbi.md).

## Se også

[Oversikt over analyse](reports-bi-reporting.md)   
[Spor nøkkelindikatorer med Power BI-måleverdier](track-kpis-with-power-bi-metrics.md)   
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-dokumentasjon](/power-bi/)  
[Hva er Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Innføring i datatorg](/power-bi/transform-model/datamarts/datamarts-overview)  
[Innføring i dataflyter og selvbetjent dataklargjøring](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
