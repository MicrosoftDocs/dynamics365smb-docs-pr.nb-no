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
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42939e97d121bd3a2abff91671d9f9571faffbfd
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakilde for Power BI for å bygge rapporter
Du kan gjøre [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgjengelig som en datakilde i Power BI og bygge kraftige rapporter om status for din bedrift.  

> [!NOTE]  
> Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. I **Hent Data**-vinduet velger du **Online Services**, velg **Dynamics 365 Business Central**, og velg deretter **Koble til**-knappen.
3. Power BI viser en veiviser som veileder deg gjennom [tilkoblingsprosessen](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Det første trinnet er å logge på servicen. Velg **Logg på** og kontoen du vil logge på som. Dette må være samme konto som du bruker til å logge på [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Velg **Koble til**-knappen for å fortsette. Veiviseren for Power BI viser en liste over [!INCLUDE[d365fin](includes/d365fin_md.md)]-selskaper og -datakilder. Disse datakildene representerer alle webtjenester som du har publisert fra hvert selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.
6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI-datamodellen.

> [!NOTE]  
> Når du er koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)], blir du ikke bedt på nytt om å logge på.

Når dataene er lastet inn, vil de vises i høyre navigering på siden. Nå har du koblet til Business Central-dataene og er klar til å begynne å bygge din Power BI-rapport. Hvis du ønsker mer informasjon, se [Power BI-dokumentasjonen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finans](finance.md)  
[Koble Power BI til [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

