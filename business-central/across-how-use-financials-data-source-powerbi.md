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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528465"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Bruke [!INCLUDE[prodlong](includes/prodlong.md)] som datakilde for Power BI for å bygge rapporter

Gjør [!INCLUDE[prodlong](includes/prodlong.md)]-dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.  

Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop

1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. På siden **Hent Data** velger du **Online Services**, **Microsoft Dynamics 365 Business Central** og deretter **Koble til**-knappen.
3. Power BI viser en veiviser som veileder deg gjennom tilkoblingsprosessen, inkludert pålogging til [!INCLUDE[prodshort](includes/prodshort.md)]. Velg **Logg på**, og velg deretter den relevante kontoen. Bruk den samme kontoen som du bruker til å logge på [!INCLUDE[prodshort](includes/prodshort.md)].
4. Velg **Koble til**-knappen for å fortsette. Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøer, -selskaper og -datakilder. Disse datakildene representerer alle web-tjenester som du har publisert fra [!INCLUDE[prodshort](includes/prodshort.md)].

    Du kan også opprette en ny URL-adresse for [!INCLUDE[prodshort](includes/prodshort.md)] i stedet. Velg én av de følgende metodene.

      - Bruke handlingen **Opprett datasett** på **Webtjenester**-siden
      - Bruke veiledningen Assistert oppsett for **Konfigurere rapportering**
      - Velge handlingen **Rediger i Excel** i alle typer lister

5. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
6. Gjenta de forrige trinnene for å legge til flere [!INCLUDE[prodshort](includes/prodshort.md)] eller andre data i Power BI-datamodellen.

> [!NOTE]  
> Når du er koblet til [!INCLUDE[prodshort](includes/prodshort.md)], blir du ikke bedt på nytt om å logge på.

Når dataene er lastet inn, kan du se dem i høyre navigering på siden. Du har koblet til [!INCLUDE[prodshort](includes/prodshort.md)]-dataene, og du kan begynne å bygge din Power BI-rapport.  

Før du lager rapporten, anbefales det at du importerer [!INCLUDE[prodshort](includes/prodshort.md)]-teamfilen.  Temafilen oppretter en fargepalett slik at du kan lage rapporter med samme fargestil som [!INCLUDE[prodshort](includes/prodshort.md)]-appene uten at du må definere egendefinerte farger for hver visuell effekt.

Hvis du vil ha mer informasjon, kan du se [Power BI-dokumentasjon](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Aktivere forretningsdata for Power BI](admin-powerbi.md)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
