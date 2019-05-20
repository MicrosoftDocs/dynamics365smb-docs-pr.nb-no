---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 1652c4bc22425bd6df4ac303a96a2ab1b28bfaf9
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241099"
---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt
Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.

> [!NOTE]
> I tillegg til Microsoft Flow kan du bruke arbeidsflytfunksjonaliteten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Legg merke til at selv om de er to separate arbeidsflytsystemer, legges en flytmal som du oppretter med Microsoft Flow, til i listen over arbeidsflytmaler i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.
2. Velg **Mine Flow-er** fra båndet øverst på siden.
3. Det er 2 måter å opprette en flyt på: **Opprett fra mal** og **Opprett fra tom**. En mal er en forhåndsdefinert flyt som er opprettet for deg.  Hvis du vil bruke en mal, bare velger du den og oppretter en kobling for hver tjeneste malen bruker. Med en tom mal kan du opprette en ny flyt helt fra begynnelsen.
4. Når du skal opprette fra en tom, går du til siden **Mine flyter** og velger **Opprett fra tom**.
5. Søk etter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** connector.
6. Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne:  
    *Det bes om godkjenning av en kunde*,  
    *Det bes om godkjenning av en finanskladd*.  
    *Det bes om godkjenning av en finanskladdelinje*,  
    *Det bes om godkjenning av en vare*.  
    *Det bes om godkjenning av et kjøpsdokument*,  
    *Det bes om godkjenning av et salgsdokument* eller  
    *Det bes om godkjenning av en leverandør*.
7. Flow ber deg om å velge et selskap i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-leier, samt eventuelle forhold i dataene du vil lytte til.

Nå har du koblet til Business Central-dataene og er klar til å begynne å bygge din flyt.

8. Når du skal opprette fra en mal, velger du **Opprett fra mal**.
9. Søk etter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-maler.
10. Fra listen over tilgjengelige maler velger du én av malene.  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-ordren*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-tilbudet*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgsfakturaen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-salgskreditnotaen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kunden*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-bestillingen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kjøpsfakturaen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-kjøpskreditnotaen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-varen*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leverandøren*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladden*,  
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdelinjer*,  
11. Flow ber deg om å velge et annet selskap i din [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-leier. Siden hvert trinn i flyten er uavhengig av neste, kan det hende at må definere selskapet flere ganger når du bruker en [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-flytmal.

Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://docs.microsoft.com/en-us/flow/getting-started).

For å feilsøke Microsoft Flow kan du se [Feilsøke integrering med Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Arbeidsflyt](across-workflow.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)   
[Administrer arbeidsflyter for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Brukeroppsett for godkjenning](across-how-to-set-up-approval-users.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
