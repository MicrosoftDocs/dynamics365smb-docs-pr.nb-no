---
title: Oversikt over komponent og arkitektur for Power BI-integrering for Business Central | Microsoft Docs
description: Få informasjon om de ulike aspektene ved Power BI-integrering med Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 9ce0b5232a0629bb6248eaaaade69b7c7ebceb02
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012344"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]

I denne artikkelen får du informasjon om de forskjellige aspektene ved Power BI-integrering med [!INCLUDE[prod_short](includes/prod_short.md)] for å gjøre det enklere å forstå hvordan du implementerer og bruker den.

## <a name="components"></a>Komponenter

Tabellen nedenfor beskriver de hovedkomponentene som er involvert i Power BI-integrering.

|Komponent|Beskrivelse|
|---------|-----------|
|Power BI|En skybasert tjeneste for drifting og administrasjon av rapporter.|
|Power BI Desktop|Et redigeringsverktøy du bruker til å bygge rapporter og instrumentbord, og gjør at du kan kjøre rapporter. Det er tilgjengelig som en gratis nedlasting i Microsoft Store og installeres lokalt.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online eller lokal løsning med koblinger som er eksponert for Power BI, og kan bygge inn en Power BI-del.|

## <a name="whats-available-from-the-start"></a>Hva som er tilgjengelig fra begynnelsen

Tabellen nedenfor beskriver tilgjengelige funksjoner.

|Funksjon|Støtte for [!INCLUDE[prod_short](includes/prod_short.md)] Online eller lokalt|
|-------|---------------------|
|Power BI-koblinger|Begge deler. Ulike koblinger for Online og lokalt. Samme kobling brukes for Power BI Desktop og Power BI-tjeneste. |
|Innebygd opplevelse for visning av en gitt rapport i en faktaboks i [!INCLUDE[prod_short](includes/prod_short.md)]|Begge deler. Må konfigureres for å kunne vise rapporter for den lokale versjonen.|
|Power BI-rapportadministrasjon fra [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Standard Power BI-rapporter for rollesentre distribueres til Power BI|Online|
|Power BI-apper i Microsoft AppSource|Online|

## <a name="architecture"></a>Arkitektur

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med Power BI via en kobling som bruker OData. Datakilden for Power BI-rapporter eksponeres som API-sider og OData-nettjenester.

![Power BI-arkitektur for integrering med Business Central.](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Generell flyt

Diagrammet nedenfor viser den grunnleggende arbeidsflyten for brukere når du kobler [!INCLUDE[prod_short](includes/prod_short.md)] til Power BI.

![Power BI-arbeidsflyt for integrering med Business Central.](./media/power-bi-flow.png)

1. Brukeren registrerer seg for en Power BI-konto.
2. Brukeren kobler seg til Power BI fra [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer lisensen.
4. [!INCLUDE[prod_short](includes/prod_short.md)] distribuerer standardrapporter til Power BI-tjenesten. Dette trinnet skjer bare for [!INCLUDE[prod_short](includes/prod_short.md)] Online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gjør rapporter i Power BI tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)]. Standardrapporter vises automatisk i Power BI-deler.
6. Brukeren oppretter en rapport i Power BI Desktop.
7. Brukeren publiserer rapporten til Power BI-tjenesten. Rapportene blir deretter tilgjengelige for valg i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Business Central og Power BI](admin-powerbi.md)  
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