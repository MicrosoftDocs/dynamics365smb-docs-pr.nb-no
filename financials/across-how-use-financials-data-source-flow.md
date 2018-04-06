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
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

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
    *Det bes om godkjenning av en kunde*,  
    *Det bes om godkjenning av en finanskladd*.  
    *Det bes om godkjenning av en finanskladdelinje*,  
    *Det bes om godkjenning av en vare*.  
    *Det bes om godkjenning av et kjøpsdokument*,  
    *Det bes om godkjenning av et salgsdokument* eller  
    *Det bes om godkjenning av en leverandør*.
5. Flow ber deg om å velge et annet selskap i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-leier. Siden hvert trinn i Flow er uavhengig av neste, kan det hende at må definere selskapet flere ganger når du bruker en [!INCLUDE[d365fin](includes/d365fin_md.md)]-mal.

Nå har du koblet til Finance and Operations, Business edition-dataene og er klar til å begynne å bygge flyten. Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).

Hvis du vil feilsøke Microsoft Flow, kan du se [Feilsøke integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

