---
title: Bruke Business Central i Power BI-rapporter | Microsoft Docs
description: Gjør dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755244"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Bruke [!INCLUDE [prodlong](includes/prodlong.md)] som datakilde for Power BI for å bygge rapporter

Gjør [!INCLUDE[prodlong](includes/prodlong.md)]-dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.  

Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop

1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. På siden **Hent Data** velger du **Online Services**, **Microsoft Dynamics 365 Business Central** og deretter **Koble til**-knappen.
3. Power BI viser en veiviser som veileder deg gjennom tilkoblingsprosessen. Du blir bedt om å logge på [!INCLUDE [prodshort](includes/prodshort.md)]. Velg **Logg på** og kontoen du vil logge på som. Dette må være samme konto som du bruker til å logge på [!INCLUDE [prodshort](includes/prodshort.md)].
4. Velg **Koble til**-knappen for å fortsette. Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-selskaper og -datakilder. Disse datakildene representerer alle webtjenester som du har publisert fra hvert selskap i [!INCLUDE [prodshort](includes/prodshort.md)].

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. Alternativt, opprette en ny web service URL i [!INCLUDE [prodshort](includes/prodshort.md)] ved hjelp av **Opprett datasett** på siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.
6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere [!INCLUDE [prodshort](includes/prodshort.md)] eller andre data i Power BI-datamodellen.

> [!NOTE]  
> Når du er koblet til [!INCLUDE [prodshort](includes/prodshort.md)], blir du ikke bedt på nytt om å logge på.

Når dataene er lastet inn, vil de vises i høyre navigering på siden. Nå har du koblet til [!INCLUDE [prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din Power BI-rapport.  

Før du lager rapporten, anbefales det at du importerer [!INCLUDE [prodshort](includes/prodshort.md)]-teamfilen.  Temafilen oppretter en fargepalett slik at du kan lage rapporter med samme fargestil som [!INCLUDE [prodshort](includes/prodshort.md)]-appene uten at du må definere egendefinerte farger for hver visuell effekt.

Hvis du vil ha mer informasjon, kan du se [Power BI-dokumentasjon](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Se også

[Aktivere forretningsdata for Power BI](admin-powerbi.md)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
