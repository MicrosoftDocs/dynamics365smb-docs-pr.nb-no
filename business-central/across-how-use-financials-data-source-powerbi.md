---
title: Bygge rapporter i Power BI Desktop for å vise Business Central-data | Microsoft Docs
description: Gjør dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce1ce3039758d5991eb3a770713d2f1e273bbe0c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754520"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Bygge Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data

Gjør [!INCLUDE[prod_long](includes/prod_long.md)]-dataene tilgjengelige som en datakilde i Power BI Desktop, og bygg kraftige rapporter om status for din bedrift.

Denne artikkelen beskriver hvordan du kommer i gang med Power BI Desktop for å opprette rapporter som viser [!INCLUDE[prod_long](includes/prod_long.md)]-data.  Når du har opprettet rapporter, kan du publisere dem i Power BI-tjenesten eller dele dem med alle brukerne i organisasjonen. Når disse rapportene er i Power BI-tjenesten, kan brukerne som er konfigurert for den, vise rapportene i [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Gjøre deg klar

- Registrer deg for Power BI-tjenesten.

    Hvis du ikke allerede har registrert deg, går du til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du registrerer deg, bruker du e-postadressen og passordet for jobben din.

- Last ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop er et gratis program du kan installere på den lokale datamaskinen. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Kontroller at dataene du vil ha med i rapporten, er publisert som en webtjeneste.
    
    Mange webtjenester er publisert som standard. Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På **Webtjenester**-siden kontrollerer du at **Publiser**-feltet er valgt. Denne oppgaven er vanligvis en administrativ oppgave.
    
    Hvis du vil ha mer informasjon om publisering av webtjenester, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

- Hent følgende informasjon for [!INCLUDE[prod_short](includes/prod_short.md)] lokalt:

    - OData URL-adressen for [!INCLUDE[prod_short](includes/prod_short.md)]. Denne URL-adressen har vanligvis formatet `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for eksempel `https://localhost:7048/BC160/ODataV4`. Hvis du har en distribusjon med flere leietakere, tar du med leietakeren i URL-adressen, for eksempel `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Et brukernavn og en tilgangsnøkkel for webtjeneste for en [!INCLUDE[prod_short](includes/prod_short.md)]-konto.

      Power BI bruker enkel godkjenning til å hente data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Så du trenger et brukernavn og en tilgangsnøkkel for webtjeneste for å koble til. Kontoen kan være din egen brukerkonto, eller organisasjonen kan ha en bestemt konto for dette formålet.

- Last ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfritt).

    Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](#theme) i denne artikkelen.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop

Den første oppgaven i opprettelse av rapporter, er å legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop. Når den er tilkoblet, kan du begynne å bygge rapporten.

1. Start Power BI Desktop.
2. Velg **Hent data**.

    Hvis du ikke ser **Hent data**, velger du **Fil**-menyen og deretter **Hent data**.
2. På **Hent data**-siden velger du **Online Services**.
3. I **Online Services**-ruten gjør du ett av følgende:

    1. Hvis du kobler til [!INCLUDE [prod_short](includes/prod_short.md)] Online, velger du **Dynamics 365 Business Central** og deretter **Koble til**.
    2. Hvis du kobler til [!INCLUDE [prod_short](includes/prod_short.md)] lokalt, velger du **Dynamics 365 Business Central** (lokalt) og deretter **Koble til**.

4. Power BI viser en veiviser som veileder deg gjennom tilkoblingsprosessen, inkludert pålogging til [!INCLUDE [prod_short](includes/prod_short.md)].

    For Online velger du **Logg på** og deretter den relevante kontoen. Bruk den samme kontoen du bruker til å logge på [!INCLUDE [prod_short](includes/prod_short.md)].
    
    For den lokale versjonen angir du OData URL-adressen for [!INCLUDE[prod_short](includes/prod_short.md)] og eventuelt selskapsnavnet. Når du blir bedt om det, skriver du inn brukernavnet og passordet for kontoen du vil bruke til å koble til [!INCLUDE[prod_short](includes/prod_short.md)]. I **Passord**-boksen angir du tilgangsnøkkelen for webtjeneste.

    > [!NOTE]  
    > Når du er koblet til [!INCLUDE[prod_short](includes/prod_short.md)], blir du ikke bedt på nytt om å logge på.
    
5. Velg **Koble til** for å fortsette.

    Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]-miljøer, -selskaper og -datakilder. Disse datakildene representerer alle webtjenestene du har publisert fra [!INCLUDE [prod_short](includes/prod_short.md)].
6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere [!INCLUDE [prod_short](includes/prod_short.md)] eller andre data i Power BI-datamodellen.

Når dataene er lastet inn, kan du se dem i høyre navigering på siden. Nå har du koblet til [!INCLUDE[prod_short](includes/prod_short.md)]-dataene, og du kan begynne å bygge Power BI-rapporten.  

> [!TIP]
> Hvis du vil ha mer informasjon om hvordan du bruker Power BI Desktop, kan du se [Kom i gang med Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Opprette rapporter for å vise data tilknyttet en liste

Du kan opprette rapporter som vises i en faktaboks på en [!INCLUDE [prod_short](includes/prod_short.md)]-listeside. Rapportene kan inneholde data om posten som er valgt i listen. Du oppretter disse rapportene på lignende måte som andre rapporter, men det er enkelte ting du må gjøre for å sikre at rapportene vises som forventet. Hvis du vil ha mer informasjon, kan du se [Opprette Power BI-rapporter for visning av listedata i [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Bruke [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet (valgfritt)

Før du bygger rapporten, anbefales det at du laster ned og importerer [!INCLUDE [prod_short](includes/prod_short.md)]-teamfilen. Temafilen oppretter en fargepalett, slik at du kan lage rapporter med samme fargestil som [!INCLUDE [prod_short](includes/prod_short.md)]-appene uten å måtte definere egendefinerte farger for hver visualisering.

> [!NOTE]
> Denne oppgaven er valgfri. Du kan alltids opprette rapportene og deretter laste ned og bruke stilmalen senere.

### <a name="download-the-theme"></a>Laste ned temaet

Temafilen er tilgjengelig som en JSON-fil i temagalleriet i Microsoft Power BI-fellesskapet. Hvis du vil laste ned temafilen, gjør du følgende:

1. Gå til [Temagalleriet i Microsoft Power BI-fellesskapet for Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Velg nedlastingsvedlegget **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Importere temaet i en rapport

Etter at du har lastet ned [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet, kan du importere det til rapportene. Du importerer temaet ved å velge **Vis** > **Temaer** > **Bla gjennom etter temaer**. Hvis du vil ha mer informasjon, kan du se [Power BI Desktop – importere egendefinerte rapporttemaer](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Publisere rapporter

Når du har opprettet eller endret en rapport, kan du publisere den i Power BI-tjenesten og dele den med andre i organisasjonen. Når rapporten er publisert, vises den i Power BI. Rapporten blir også tilgjengelig for valg i [!INCLUDE[prod_short](includes/prod_short.md)].

Du publiserer en rapport ved å velge **Publiser** i **Hjem**-fanen på båndet eller **Fil**-menyen. Hvis du er logget på Power BI-tjenesten, publiseres rapporten til denne tjenesten. Hvis ikke blir du bedt om å logge på. 

## <a name="distribute-or-share-a-report"></a>Distribuere eller dele en rapport

Du kan sende rapporter til kolleger og andre på et par ulike måter:

- Distribuer rapporter som PBIX-filer.

    Rapporter lagres på datamaskinen som PBIX-filer. Du kan distribuere PBIX-rapportfilen til brukere, slik som alle andre filer. Deretter kan brukerne laste opp filen til Power BI-tjenesten. Se [Laste opp rapporter fra filer](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Når du distribuerer rapporter på denne måten, betyr det at data for rapporter oppdateres individuelt av hver bruker. Denne situasjonen kan påvirke ytelsen til [!INCLUDE[prod_short](includes/prod_short.md)].

- Del rapporter fra Power BI-tjenesten.

    Hvis du har en Power BI Pro-lisens, kan du dele rapporten med andre direkte fra Power BI-tjenesten. Hvis du vil ha mer informasjon, kan du se [Power BI – dele et instrumentbord eller en rapport](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere forretningsdata for Power BI](admin-powerbi.md)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]