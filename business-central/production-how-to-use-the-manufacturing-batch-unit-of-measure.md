---
title: Bruke produksjonsbunkeenheten | Microsoft-dokumentasjon
description: Hvis en vare lagerføres i én enhet, men produseres i en annen, må produksjonsordren bruke en produksjonsbunkeenhet til å beregne riktig antall komponenter. Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9abad1ccc89ef8d47d1d3fe19077814b03668db6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787680"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Arbeide med produksjonsbunkeenhet
Hvis en vare lagerføres i én enhet, men produseres i en annen, opprettes en produksjonsordre som bruker en produksjonsbunkeenhet til å beregne riktig antall komponenter mens kjørselen **Forny produksjonsordre** kjøres. Ett eksempel på beregning med produksjonsbunkeenhet er når en produsert vare lagerføres i stykker, men produseres i tonn.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Slik oppretter du en produksjonsstykkliste ved å bruke en produksjonsbunkeenhet  
1.  Produksjonsbunkeenheten defineres som en alternativ enhet på **Vareenheter**-siden for varen som skal produseres. Bunkeenheten erstatter ikke lagerenheten for varen.  
2.  Opprett en produksjonsstykkliste for varen som er definert med produksjonsbunkeenheten. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsstykklister](production-how-to-create-production-boms.md).  
3.  I **Enhetskode**-feltet velger du den relevante produksjonsbunkeenheten.  
4.  Angi antallet av komponentvaren som trengs for å opprette denne bunkeenheten, i **Antall per**-feltet for hver linje i produksjonsstykklisten.  
5.  Åpne **varekortet** for den relaterte varen.  

    På hurtigfanen **Etterfylling**, i feltet **Produksjonsstykklistenr.**, velger du produksjonsstykklisten du opprettet ovenfor.  
6.  Opprett et produksjonsordrehode ved å bruke varen som er definert med produksjonsbunkeenheten. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsordrer](production-how-to-create-production-orders.md).  
7.  Velg **Forny**-handlingen, og velg deretter **OK**-knappen.  

På hurtigfanen **Linjer** velger du **Linje**-handlingen, og deretter **Komponenter**-handlingen for å vise resultatet. Programmet beregner det riktige antallet av komponentene som trengs for å oppfylle produksjonsstykklisten, basert på produksjonsbunkeenheten.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Slik beregner du en produksjonsbunkeenhet i en produksjonsordre  
1.  Opprett et produksjonsordrehode ved å bruke varen som er definert med produksjonsbunkeenheten.  
2.  Skriv inn det samme varenummeret som brukes i hodet, i feltet **Varenr.** på produksjonsordrelinjen.  
3.  Angi samme antall som brukes i hodet, i **Antall**-feltet.  
4.  I **Enhetskode**-feltet velger du den relevante enhetskoden for produksjonsbunken.  
5.  Velg handlingen **Oppdater**.
6.  Fjern merket for **Linjer** på hurtigfanen **Beregn**.  
7.  Velg **OK**.  
8.  På hurtigfanen **Linjer** velger du **Linje**-handlingen, og deretter **Komponenter**-handlingen for å vise resultatet. Det riktige antallet av komponentene som trengs for å oppfylle produksjonsstykklisten, beregnes basert på produksjonsbunkeenheten.  

## <a name="see-also"></a>Se også  
[Opprette ruter](production-how-to-create-routings.md)  
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)     
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]