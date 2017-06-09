---
title: "Sette opp markedsføringskampanjer i Finacials | Microsoft-dokumentasjon"
description: "Beskriver hvordan du kan sette opp og utføre markedsføringskampanjer i Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Administrere markedsføringskampanjer
Ved å ha en solid markedsføringsplan kan du identifisere, trekke til deg og beholde kunder. En markedsføringsplan består av forskjellige kampanjer og andre samhandlinger i forbindelse med salgs- og markedsføringsaktiviteter. Når du planlegger en kampanje, må du bestemme deg for hvilke kontakter du skal rette deg mot, hvilken type kampanje du vil kjøre (for eksempel salgsmesse eller direktereklame), og hvilke selgere som skal utføre hver oppgave.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Definere enkeltkampanjer
Før du kan opprette en kampanje, må du definere *statuskoder for kampanjen*. Ved hjelp av disse kodene kan du kontrollere kampanjen ved å tilordne en status til den. Når du arbeider deg gjennom fasene i en kampanje, kan du se på hvilket trinn en kampanje befinner seg, og hvilket trinn som følger. Du definererer koder for kampanjestatus i vinduet **Kampanjestatus**.

Du kan opprette et *kampanjekort* for hver kampanje du vil følge. Du kan også vise disse kampanjekortene for å vise generell informasjon om kampanjene.
Du kan slette kampanjeposter hvis for eksempel posten registrerer en handling som er kansellert. Du kan bare slette kansellerte kampanjeposter.

### <a name="selecting-the-target-audience"></a>Velge målgruppen
Når du har opprettet en kampanje, kan du begynne å opprette segmenter som angir målgruppen til kampanjen. Hvis du vil ha mer informasjon, kan du se [Håndtere segmenter](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Registrere rabattprosenter
Når du har definert kampanjen, bestemt hvilke segmenter du vil kampanjen skal dekke, og angitt startdatoen og sluttdatoen, registrerer du rabattprosenten som kunden vil få for de individuelle varene, på linjene i vinduet **Salgslinjerabatter**. Du kan også registrere salgsprisene for de individuelle varene på linjene i **Salgspriser**-vinduet. Du kan få tilgang til begge vinduene fra kampanjekortet.

 Når du har definert salgsprisene/linjerabattene og segmentene på kampanjekortet, må du aktivere dem slik at kampanjeprisene/-rabattene gjenspeiles på linjene.

> [!NOTE]  
>  For å kunne aktivere salgsprisene/linjerabattene, må du angi om hele segmentet eller bare noen kontakter er mål for kampanjen. Hvis salgsprisene/linjerabattene dekker alle kontaktene i segmentet, merker du av for **Kampanjemål**-feltet på hurtigfanen **Kampanje** på **Segment**-kortet.
Hvis salgsprisene/linjerabattene ikke skal tilbys alle kontaktene i segmentet, kan du fjerne merket for **Kampanjemål**-feltet for de relavante kontaktene. Hvis du ikke ser dette feltet, kan du legge det til i visningen. Hvis du vil ha mer informasjon, kan du se [Brukertilpasning](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Håndtere segmenter](marketing-segments.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeide med Financials](ui-work-product.md)  

