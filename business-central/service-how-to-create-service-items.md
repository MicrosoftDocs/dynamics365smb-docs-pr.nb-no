---
title: Opprette servicevarer | Microsoft-dokumentasjon
description: Når du mottar en uregistrert vare til service, kan du registrere den som en servicevare.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5f7a95b297ef494cc3607f4550b6a0e58b18839d
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2020
ms.locfileid: "2992172"
---
# <a name="create-service-items"></a>Opprette servicevarer
I [!INCLUDE[d365fin](includes/d365fin_md.md)] refererer betegnelsen "servicevare" til utstyr eller varer som trenger service. Når du oppretter en serviceordre, kan du angi varene som trenger service. I ordren kan du knytte en servicevare til en vare på lageret eller i en servicevaregruppe.    

Når du mottar en vare som trenger service, kan du registrere den som en servicevare. Det er flere måter å gjøre dette på. Du kan for eksempel oppretter en servicevare på siden **Servicevarer** eller som en del av en annen prosess, for eksempel når du arbeider med en serviceordre.   

## <a name="to-create-a-service-item"></a>Slik oppretter du en servicevare  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevarer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Slik oppretter du servicevarer i en serviceordre  
Når du mottar varer for service som du registrere som servicevarer, kan du opprette dem som servicevarer på sidene **Serviceordre** eller **Servicetilbud**.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Opprett servicevare**.  

    Et tall blir tilordnet til servicevaren, og et servicevarekort opprettes. Feltet **Servicevarenr.** fylles ut med nummeret på den nye servicevaren.

## <a name="to-create-a-service-item-when-shipping-items"></a>Slik oppretter du en servicevare når du leverer varer  
Når du leverer varer ved å bokføre ordrer eller salgsfakturaer, registreres de leverte varene automatisk som servicevarer hvis følgende betingelse gjelder: Varene må tilhøre en servicevaregruppe med en avmerking i **Opprett servicevare**-boksen. Hvis varene har serienumre registrert på siden Varesporingslinjer, kopieres denne informasjonen automatisk til **Serienr**-feltet på servicevarekortet når du oppretter servicevarer.  

Følgende fremgangsmåte viser hvordan du oppretter servicevarer når du leverer varer i ordrer.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne den aktuelle ordren.  
3. Velg handlingen **Bokfør** eller **Bokfør og skriv ut**.  
4. Velg handlingen **Lever** eller **Lever og fakturer**.  
5. Servicevarene opprettes automatisk for varene i ordren, forutsatt at disse tilhører en servicevaregruppe du har definert for å opprette servicevarer. Hvis du har registrert bestemte serienumre på siden **Varesporingslinjer**, tilordnes de til disse servicevarene.  

> [!NOTE]  
>  Hvis en vare er en stykkliste og du har utvidet stykklisten, behandles de utvidede stykklistevarene på samme måte som vanlige varer. Servicevarer opprettes basert på betingelsen for servicevaregrupper og eventuelt betingelsen for serienumre. Hvis det opprettes en servicevare for en utvidet stykklistevare som består av andre stykklistekomponenter, opprettes dessuten disse varene som servicevarekomponenter for den utvidede stykklisteservicevaren.  
>   
>  Hvis en vare er en stykklistevare og du ikke har utvidet stykklisten, opprettes det en servicevare for den basert på betingelsen for servicevaregruppen og eventuelt betingelsen for serienumre.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Slik setter du inn et startgebyr for en servicevare
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Arbeidsordre**.
3. Velger servicelinjen, og velg deretter handlingen **Handlinger**, **Funksjoner** og deretter **Sett inn startgebyr**.  

    En servicelinje av typen **Kostnad** settes inn med startgebyret. Startgebyret gjelder for den valgte servicevaren.

## <a name="see-also"></a>Se også  
[Definere servicevarer og servicevarekomponenter](service-how-setup-service-items.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicebehandling](service-service.md)  
