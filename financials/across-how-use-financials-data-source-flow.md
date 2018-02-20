---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt
Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.
2. Velg **Mine Flow-er** fra båndet øverst på siden.
3. I vinduet **Mine Flow-er** velger du **Opprett fra tom**.
4. Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne:  
    *Når en post opprettes*,  
    *Når en post slettes*,  
    *Når en post endres*,  
    *Det bes om godkjenning av en kunde*,  
    *Det bes om godkjenning av en finanskladd*.  
    *Det bes om godkjenning av en finanskladdelinje*,  
    *Det bes om godkjenning av en vare*.  
    *Det bes om godkjenning av et kjøpsdokument*,  
    *Det bes om godkjenning av et salgsdokument* eller  
    *Det bes om godkjenning av en leverandør*.
5. Flow vil be deg om informasjonen som kreves for å koble til [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene dine. Hvis du har valgt én av følgende utløsere: *Når en post opprettes*, *Når en post endres* eller *Når en post slettes*, må du velge en selskapsnavnet og tabellnavn. For alle andre utløsere kreves bare selskapsnavnet for å koble til.

   Flow vil vise en liste over selskaper og tabeller som er tilgjengelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse tabellene eller endepunktene, representerer alle web-tjenester som du har publisert fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.

Nå har du koblet til Finance and Operations, Business edition-dataene og er klar til å begynne å bygge flyten. Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).

Hvis du vil feilsøke Microsoft Flow, kan du se [Feilsøke integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

