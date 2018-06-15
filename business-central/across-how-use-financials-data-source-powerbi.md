---
title: Definere rapportering for Business Central i Power BI | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-data tilgjengelig som en datakilde i Power BI og bygge kraftige rapporter om status for din bedrift."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/03/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: c7782d6f74a56f72b40dfb6cfd59a44ab4a33ae7
ms.contentlocale: nb-no
ms.lasthandoff: 05/17/2018

---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>Bruke [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som datakilde for Power BI for å bygge rapporter
Du kan gjøre [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-data tilgjengelig som en datakilde i Power BI og bygge kraftige rapporter om status for din bedrift.  

Du må ha en gyldig konto med [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. I **Hent Data**-vinduet velger du **Online Services**, velg **Microsoft Dynamics 365 Business Central**, og velg deretter **Koble til**-knappen.
3. Power BI viser en veiviser som veileder deg gjennom [tilkoblingsprosessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Du blir bedt om å logge på servicen. Velg **Logg på** og kontoen du vil logge på som. Dette må være samme konto som du bruker til å logge på [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Velg **Koble til**-knappen for å fortsette. Veiviseren for Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-selskaper og -datakilder. Disse datakildene representerer alle webtjenester som du har publisert fra hvert selskap i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.
6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] eller andre data i Power BI-datamodellen.

> [!NOTE]  
> Når du er koblet til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], blir du ikke bedt på nytt om å logge på.

Når dataene er lastet inn, vil de vises i høyre navigering på siden. Nå har du koblet til Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene og er klar til å begynne å bygge din Power BI-rapport. 

Før du lager rapporten, anbefales det at du importerer Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-teamfilen.  Temafilen oppretter en fargepalett slik at du kan lage rapporter med samme fargestil som Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene uten at du må definere egendefinerte farger for hver visuell effekt.

Hvis du ønsker mer informasjon, se [Power BI-dokumentasjonen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finans](finance.md)  
[Koble Power BI til [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

