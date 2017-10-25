---
title: "Forstå montere til ordre og montere til lager | Microsoft-dokumentasjon"
description: "Monteringsvarer kan leveres ved å montere dem når de bestilles, eller ved å montere dem og beholde dem på lageret før de er nødvendig i en ordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d5be31ebb84542e1762ffda9bc76a3aa38485095
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# Forstå montere til ordre og montere til lager
Monteringsvarer kan leveres i følgende to prosesser:  

-   Monter til ordre.  
-   Monter til lager.  

## Montere til ordre  
Vanligvis bruker du *Montere til ordre* for varer som du ikke vil ha på lager, fordi du planlegger å tilpasse dem etter kundeforespørsler eller fordi du vil minimere lagerføringskostnadene. Funksjonaliteten som støttes, inkluderer følgende:  

-   Muligheten til å tilpasse monteringsvarer når en ordre blir tatt.  
-   Oversikt over monteringsvarens og tilhørende komponenters tilgjengelighet.  
-   Muligheten til å reservere monteringskomponenter umiddelbart for å garantere ordreinnfrielse.  
-   Funksjon for å avgjøre lønnsomheten til den tilpassede ordren ved å opprullere pris og kostnad.  
-   Integrering med lageret for å forenkle montering og levering.  
-   Muligheten til å montere til ordre når et tilbud en rammeordre blir fremlagt.  
-   Muligheten til å kombinere lagerantall med monter til ordre-antall.  

I montere-til-ordre-prosessen monteres varen som svar på en ordre og med en én-til-én-relasjon mellom monteringsordren og ordren.  

Når du angir en montere-til-ordre-vare på en salgslinje, blir det automatisk opprettet en monteringsordre med et hode som er basert på salgslinjen og med linjer som er basert på varens monteringsstykkliste multiplisert med ordreantallet. Du kan bruke vinduet **Montere til ordre – linjer** for å se de tilknyttede monteringsordrelinjene for å støtte tilpasning av monteringsvaren, med en leveringsdato som er basert på informasjon om komponenttilgjengelighet. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Selv om det ikke er en del av standardprosessen, kan du selge lagerantall sammen med monter til ordre-antall. Hvis du vil ha mer informasjon, kan du se [Selge lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Når du skal aktivere denne prosessen, må **Monteringsprinsipp**-feltet på varekortet være **Monter til ordre**.  

## Montere til lager  
 Vanligvis bruker du *Montere til lager* for varer som du vil montere før salg (for eksempel for å forberede til en pakkekampanje) og beholde på lager inntil de bestilles. Disse varene er vanligvis standardvarer, for eksempel pakkede sett som du ikke tilbyr å tilpasse på forespørsel fra kunder.  

 I montere-til-lager-prosessen monteres varen uten umiddelbare salgsbehov og lagerføres på lageret som en lagervare for senere salg eller forbruk som en halvfabrikat. Hvis du vil ha mer informasjon, kan du se [Montere varer](assembly-how-to-assemble-items.md). Fra dette punktet plukkes og behandles varen som en enkeltvare og behandles som en ferdig produksjonsvare.  

 Når du angir en montere-til-lager-vare på en salgslinje, vises linjen på samme måte som for andre varer som er solgt fra lager. Disposisjon kontrolleres for eksempel bare for monteringsvaren.  

> [!NOTE]  
>  Selv om det ikke er en del av standardprosessen, kan du montere en vare til ordre selv om den er definert til å bli montert til lager. Hvis du vil ha mer informasjon, kan du se [Selge montere-til-ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Når du skal aktivere denne prosessen, må **Monteringsprinsipp**-feltet på varekortet være **Monter til lager**.  

## Kombinasjonsscenarier  
 Et generelt prinsipp i monteringsstyring er at når montere til ordre-antall er satt sammen på en ordrelinje, må de leveres før lagerantallene.  

 Hvis en monteringsordre er koblet til en ordrelinje, kopieres verdien i feltet **Ant. som skal monteres til ordre** på ordrelinjen til feltet **Antall å montere** via **Antall**-feltet i monteringsordrehodet. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 I tillegg er verdien i feltet **Antall å montere** knyttet til feltet **Levere (antall)** på ordrelinjen, og denne relasjonen styrer leveringen av montere-til-ordre-antall, både delvis og fullstendig. Dette gjelder både når hele salgslinjeantallet er montert til ordre og i kombinasjonsscenarioer der én del av salgslinjeantallet er montert til ordre og en annen del er levert fra lageret. I kombinasjonsscenariet har du imidlertid større fleksibilitet når du leverer delvis, i og med at du kan endre feltet **Antall å montere**, i henhold til forhåndsdefinerte regler, for å angi hvor mange enheter som skal leveres delvis fra lager, og hvor mange som skal leveres delvis ved å montere til ordre.  

 Hvis hele salgslinjeantallet må monteres til ordre og leveres, kopieres verdien i feltet **Levere (antall)** til feltet **Antall å montere** i den koblede monteringsordren når du endrer antallet som skal leveres. Dette sikrer at antallet som skal leveres forsynes fullstendig av monter-til-ordre-antallet.  

 I kombinasjonsscenarier kopieres imidlertid ikke hele verdien i feltet **Levere (antall)** til feltet **Antall å montere** på monteringsordrehodet. I stedet settes en standardverdi inn i feltet **Antall å montere**. Standardverdien beregnes basert på feltet **Levere (antall)** i henhold til en forhåndsdefinert regel som sikrer levering av montere-til-ordre-antallet først.  

 Hvis du vil avvike fra denne standardverdien, for eksempel fordi du bare vil montere flere eller færre av antallet i feltet **Levere (antall)**, kan du endre feltet **Antall å montere**, men bare i forhåndsdefinerte regler, som illustrert nedenfor.  

 Et eksempel på hvorfor du kan ønske å endre antallet som skal monteres, er at du vil bokføre levering av lagerantall delvis før monteringsavgangen kan leveres.  

 Følgende forklarer reglene som definerer minimums- og maksimumsverdiene som du kan angi manuelt i **Antall å montere** for å avvike fra standardverdien i et kombinasjonsscenario. Tabellen viser et kombinasjonsscenario der feltet **Levere (antall)** i den koblede ordrelinjen er endret fra 7 til 4, og **Antall å montere** er derfor som standard satt til 4.  

||Ordrelinje|Monteringsordrehode|  
|-|----------------------|---------------------------|  
||**Antall**|**Levere (antall)**|**Ant. som skal monteres til ordre**|**Levert (antall)**|**Antall**|**Antall å montere**|**Montert antall**|**Restantall**|  
|Første|10|7|7|0|7|7|0|7|  
|Endre||4||||4 (satt inn som standard)|||  

 Basert på situasjonen ovenfor kan du bare endre feltet **Antall å montere** som vist nedenfor:  

-   Minimumsantallet du kan angi, er 1. Dette er fordi du må montere minst én enhet for å kunne selge fire enheter, forutsatt at de gjenværende tre er tilgjengelig i lageret.  
-   Maksimumsantallet du kan angi, er 4. Dette sikrer at du ikke monterer flere montere-til-varer enn det som trengs på salget.  

## Se også  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeide med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

