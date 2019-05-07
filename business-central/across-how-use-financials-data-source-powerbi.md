---
title: Definere rapportering for Business Central i Power BI | Microsoft Docs
description: Gjør dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 8dfedbc2685e086f9bdc63706d70327ebb95c2b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "919894"
---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Bruke [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som datakilde for Power BI for å bygge rapporter
Gjør [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene tilgjengelige som en datakilde i Power BI, og bygg kraftige rapporter om status for din bedrift.  

Du må ha en gyldig konto med [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. På siden **Hent Data** velger du **Online Services**, **Microsoft Dynamics 365 Business Central** og deretter **Koble til**-knappen.
3. Power BI viser en veiviser som veileder deg gjennom [tilkoblingsprosessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Du blir bedt om å logge på servicen. Velg **Logg på** og kontoen du vil logge på som. Dette må være samme konto som du bruker til å logge på [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Velg **Koble til**-knappen for å fortsette. Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-selskaper og -datakilder. Disse datakildene representerer alle webtjenester som du har publisert fra hvert selskap i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] ved hjelp av **Opprett datasett** på siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.
6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] eller andre data i Power BI-datamodellen.

> [!NOTE]  
> Når du er koblet til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], blir du ikke bedt på nytt om å logge på.

Når dataene er lastet inn, vil de vises i høyre navigering på siden. Nå har du koblet til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene og er klar til å begynne å bygge din Power BI-rapport. 

Før du lager rapporten, anbefales det at du importerer Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-teamfilen.  Temafilen oppretter en fargepalett slik at du kan lage rapporter med samme fargestil som Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene uten at du må definere egendefinerte farger for hver visuell effekt.

Hvis du vil ha mer informasjon, kan du se [Power BI-dokumentasjon](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finans](finance.md)  
[Koble Power BI til [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
