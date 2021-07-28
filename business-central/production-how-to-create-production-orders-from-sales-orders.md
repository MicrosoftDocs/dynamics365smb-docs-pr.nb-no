---
title: Opprette produksjonsordrer fra ordrer
description: Lær de ulike måtene for å opprette produksjonsordrer for produserte varer direkte fra ordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: a432b8f00a24771578716a1b51678904d2e29ec5
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438630"
---
# <a name="create-production-orders-from-sales-orders"></a>Opprette produksjonsordrer fra ordrer
Du kan opprette produksjonsordrer for produserte varer direkte fra ordrer.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Slik oppretter du en produksjonsordre fra en ordre  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg ordren du vil opprette en produksjonsordre for.  
3.  Velg handlingen **Planlegging**. På **Ordreplanlegging**-siden kan du se tilgjengeligheten til ordrevaren.  
4.  Velg handlingen **Opprett prod.ordre**.  
5.  Angi status og ordretype.  
6.  Velg knappen **Ja** for å opprette en eller flere produksjonsordrer for linjene med **Prod.ordre** i feltet **Etterfyllingssystem**.


> [!NOTE]  
> Behovslinjer i den opprettede produksjonsordren som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer. Når du har generert disse produksjonsordrene, må du huske å identifisere eventuelle komponentbehov som ikke er oppfylt, for dem ved å bruke siden **Ordreplanlegging** eller funksjonen **Planlegg på nytt** fra opprettede ordrer. 

## <a name="order-type"></a>Ordretype  
Du kan velge mellom to måter å opprette produksjonsordrer på, som beskrevet i tabellen nedenfor.

|Alternativ|Beskrivelse|
|------|-----------|
|Vareordre|Det opprettes en produksjonsordre for hver nødvendige ordre for produksjonsordren som representeres av en linje i **Ordreplanlegging**-vinduet.|
|Prosjektordre|Det opprettes en produksjonsordre for alle nødvendige ordrer for produksjonsordren som representeres av linjer i **Ordreplanlegging**-vinduet. |

Når du bruker prosjektordrer, inneholder feltet **Kildetype** i produksjonsordren **Salgshode**, og ordren har flere linjer, en for hver salgslinjevare som må produseres.  


## <a name="see-also"></a>Se også  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
