---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305034"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt
Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.

> [!NOTE]
> I tillegg til Microsoft Flow kan du bruke arbeidsflytfunksjonaliteten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Legg merke til at selv om de er to separate arbeidsflytsystemer, legges en flytmal som du oppretter med Microsoft Flow, til i listen over arbeidsflyter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
> Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.
2. Velg **Mine Flow-er** fra båndet øverst på siden.
3. Du kan opprette en flyt på tre måter: **Start fra mal**, **Begynn med tom**og **Start fra en kobling**. En mal er en forhåndsdefinert flyt som er opprettet for deg. Hvis du vil bruke en mal, bare velger du den og oppretter en kobling for hver tjeneste malen bruker. Med alternativene **Begynn med tom** og **Start fra en kobling** kan du opprette en ny flyt fullstendig fra grunnen av.
4. Når du skal opprette fra en tom, går du til siden **Mine flyter** og velger alternativene **Opprett fra tom** og **Automatisk flyt**.
5. Søk etter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** connector.
6. Definer et navn og velg utløseren du vil bruke for flyten.
7. Fra listen over tilgjengelige utløsere velger du én av de tilgjengelige [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne:  
    
    *Det bes om godkjenning av en leverandør*,    
    *Det bes om godkjenning av en finanskladdelinje*,    
    *Når en post slettes*,    
    *Når en post endres*,    
    *Når en post opprettes*,    
    *Når en post endres*,    
    *Det bes om godkjenning av en finanskladd*.   
    *Det bes om godkjenning av en kunde*,   
    *Det bes om godkjenning av en vare*.    
    *Det bes om godkjenning av et kjøpsdokument* eller     
     *Det bes om godkjenning av et salgsdokument*.
     
8. Flow ber deg om å velge et miljø eller selskap i din [!INCLUDE[d365fin](includes/d365fin_md.md)]-leier, samt eventuelle forhold i dataene du vil lytte til.

> [!NOTE]  
>   Kontakten [!INCLUDE[d365fin](includes/d365fin_md.md)] for Microsoft Flow støtter flere produksjons- og sandkassemiljøer. Hvis du ikke har opprettet flere produksjons- eller sandkassemiljøer, er **Produksjon** det eneste tilgjengelige alternativet du kan velge. 

Nå har du koblet til Business Central-dataene og er klar til å begynne å bygge din flyt.

9. Når du skal opprette fra en mal, velger du **Start fra mal**.
10. Søk etter **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-maler.
11. Fra listen over tilgjengelige maler velger du én av malene, og deretter velger du **Opprett**.  

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
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladden* eller    
    *Be om godkjenning for Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-finanskladdelinjer*,  
12. Flyten vil vise en liste over tjenester som brukes i flytmalen, og vil forsøke å koble automatisk til disse tjenestene. Hvis du ikke tidligere har koblet til en tjeneste, blir du bedt om å logge deg på hver av tjenestene du må koble til. En grønn hake vises ved siden av hver tjeneste når en tilkobling er opprettet. Velg **Fortsett**.
13. Flow ber deg om å velge et miljø og selskap i din [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-leier. Siden hvert trinn i flyten er uavhengig av neste, kan det hende at du må definere miljøet og selskapet flere ganger når du bruker en [!INCLUDE[d365fin_md](includes/d365fin_md.md)]-flytmal.

Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](/flow/getting-started).

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Arbeidsflyt](across-workflow.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)   
[Administrer arbeidsflyter for [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Brukeroppsett for godkjenning](across-how-to-set-up-approval-users.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
