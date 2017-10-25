---
title: Sette opp et diagram med kosttyper | Microsoft-dokumentasjon
description: "Diagrammet med kosttyper ligner på kontoplanen i finans."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7598dbfbedf8faf7a80ac52469c2edcc4e2c1c66
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cost-types"></a>Definere kosttyper
Diagrammet med kosttyper ligner på kontoplanen i finans. Du kan definere diagrammet med kosttyper på følgende måter:  

-   Strukturen i oversikten over kosttyper ligner på resultatregnskapskontiene i finanskontoplanen. Du kan deretter overføre finanskontoplanen til diagrammet med kosttyper. Du kan foreta alle nødvendige justeringer etter overføringen.  
-   Opprett et nytt kosttypediagram, eller legg til nye kosttyper i det eksisterende kosttypediagrammet. Du må opprette hver enkelt nye kosttype individuelt.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>Slik overfører du finanskontoplanen til diagrammet med kosttyper:  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Hent kosttyper fra kontoplan**. Klikk **Ja**-knappen i dialogboksen for å bekrefte overføringen. Funksjonen bruker kontoplanen til å opprette et diagram med kosttyper.  

    Diagrammet over kostnadstypene inneholder nå alle resultatkontiene i finans og inkluderer overskrifter og delsummer. Du kan endre diagrammet med kosttyper etter behov. Du kan for eksempel slette eksisterende kosttypeduplikater.  

    > [!IMPORTANT]  
    >  Funksjonen **Registrer kosttyper i kontoplan** oppdaterer forholdet mellom kontoplanen og oversikten over kosttyper. **Nr.** -feltet er fylt ut og bekreftet for å forsikre at hver finanskonto er relatert til bare én kostnadstype. Funksjonen kjøres automatisk før overføring av finansposter til kostregnskap.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a>Slik definerer du nye kosttyper i vinduet Diagram med kosttyper:  
1.  Åpne vinduet **Diagram med kosttyper** i redigeringsmodus.  
2.  Fyll ut feltene som beskrevet etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Du kan definere og vedlikeholde kostnadstyper i vinduet **Kosttypekort** eller **Diagram med kosttyper**. I denne fremgangsmåten definerer du nye kosttyper i vinduet **Diagram med kosttyper**.

3.  Når du har opprettet alle kosttyper, velger du **Rykk inn kosttyper**. Klikk **Ja**-knappen i dialogboksen.  
4.  Koble nye kosttypen til den tilsvarende kontoen i finans.  

    > [!IMPORTANT]  
    >  Hvis du har angitt definisjoner i feltene **Sammentelling** for linjetypen **Til-sum** før du kjører funksjonen **Rykk inn kosttyper**, må du angi definisjonene på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-felt.  

## <a name="to-update-cost-types"></a>Slik oppdaterer du kosttyper:  
1.  Velg i vinduet **Kostregnskapsoppsett** hvis du vil at diagrammet med kosttypene skal oppdateres automatisk når kontoplanen endres.  
2.  I feltet **Juster finanskonto** kan du velge blant følgende alternativer:  

- **Ingen justering** – Det gjøres ingen tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.  
- **Automatisk** – en tilsvarende endring blir utført i diagrammet for kosttyper når du endrer kontoplanen.  
- **Spør** - Det vises en melding med spørsmål om du vil gjøre tilsvarende endring i diagrammet med kosttyper når du endrer kontoplanen.  

## <a name="see-also"></a>Se også  
[Gjøre rede for kostnader](finance-manage-cost-accounting.md)  
[Definere forholdet mellom kostnadstyper og finanskontoer](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
[Definere kostsentre og kostobjekter for kontoplanen](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Balanser mellom kosttype, kostsenter og kostobjekt](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Definere kost.regnskap](finance-set-up-cost-accounting.md)   
[Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
[Om kostregnskap](finance-about-cost-accounting.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

