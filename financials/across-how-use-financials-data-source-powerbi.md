---
title: Lage en datakilde for Power BI med Financials | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-data tilgjengelig som en datakilde i Power BI og bygge kraftige rapporter om status for din bedrift."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fc942b29859d2607577119fe13292078b872b05e
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="using-included365finincludesd365finmdmd-as-a-power-bi-data-source"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for Power BI
Du kan gjøre [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgjengelig som en datakilde i Power BI og bygge kraftige rapporter om status for din bedrift.  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Power BI Desktop
1. I Power BI Desktop, i den venstre navigasjonsruten, velger du **Hent Data**.
2. I **Hent Data**-vinduet velger du **Online Services**, velg **Dynamics 365 Business edition**, og velg deretter **Koble til**-knappen.

   Power BI viser en veiviser som leder deg gjennom tilkoblingsprosessen. Det første trinnet er å skrive inn en URL-adresse for OData og selskapsnavnet som er knyttet til din [!INCLUDE[d365fin](includes/d365fin_md.md)]-konto.  

   For *OData URL-adressen*, kan du kopiere OData V4 URL-adressen for web-tjenester som er oppført på siden **Web Services** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   For *Selskapsnavn*, bruk navnet som vises i **Navn**-feltet i vinduet **Selskapsopplysninger** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder flere selskaper, velger du det relevante selskapsnavnet fra listen i **Selskaper**-vinduet. I begge tilfeller må du kontrollere at navnet du angir i veiviseren for Power BI tilsvarer teksten som vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `My Company`.
3. Velg OK-knappen etter at du har angitt opplysningene. Det neste trinnet i veiviseren vil være å angi brukernavn og passord.

   > [!NOTE]  
>    Hvis det finnes andre godkjenningsalternativer i venstre navigasjon, velger du *Grunnleggende*.
4. Skriv inn brukernavn og passord. Du finner denne informasjonen i vinduet **Brukere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bruk **Internett-tilgangsnøkkelen** som passord.

   Ditt brukernavn er for eksempel *ADMIN*, og web service hurtigtast som fungerer som passordet ditt er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*.
5. Velg **Tilkobling**-knappen for å fortsette. Power BI-veiviseren viser en liste over [!INCLUDE[d365fin](includes/d365fin_md.md)]-datakilder. Disse datakildene representerer alle web-tjenester som du har publisert fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.

6. Angi hvilke data du vil legge til datamodellen, og velg deretter **Last inn**-knappen.
7. Gjenta de forrige trinnene for å legge til flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI-datamodellen.

   > [!NOTE]  
>    Når du har koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)], blir du ikke bedt om OData-URL-adressen, brukernavnet eller passordet på nytt.

Når dataene er lastet inn, vil de vises i høyre navigering på siden. Nå har du koblet til Dynamics 365-dataene og er klar til å begynne å bygge din Power BI-rapport. Hvis du ønsker mer informasjon, se [Power BI-dokumentasjonen](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

