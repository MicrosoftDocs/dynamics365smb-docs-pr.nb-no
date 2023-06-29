---
title: Opprette produksjonsordrehoder
description: 'Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9325, 99000815, 99000829, 9900083'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="create-production-order-headers"></a><a name="create-production-order-headers"></a>Opprette produksjonsordrehoder

Du kan opprette en produksjonsordre manuelt, og første trinn er å opprette et produksjonsordrehode.

Produksjonsordrer opprettes vanligvis automatisk etter en planleggingsfunksjonen for å dekke et kjente behov. Hvis du vil ha mer informasjon , kan du se [Planlegging](production-planning.md).  

I fremgangsmåten nedenfor opprettes det en fast planlagt produksjonsordre. Du kan også opprette produksjonsordrer med en annen status.  

## <a name="to-create-a-production-order-header"></a><a name="to-create-a-production-order-header"></a>Slik oppretter du et produksjonsordrehode

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagte prod.ordrer** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. I feltet **Nr.** -feltet setter du inn neste nummer i serien.  
4. I feltet **Kildetype** velger du produksjonsordrens kilde.

    Her kan du velge å produsere for en rekke varer. Hvis du vil ha mer informasjon, kan du se [Arbeide med produksjonsfamilier](production-how-work-family.md).
5. I feltet **Kildenr.** velger du varenummer, familie eller salgshode for produksjonsordren som skal genereres.  
6. Fyll ut feltene **Antall** og **Forfallsdato** i henhold til dine spesifikasjoner.  

Når produksjonskrav endres, for eksempel komponenter eller operasjoner, kan du raskt planlegge produksjonsordren på nytt. Hvis du vil ha mer informasjon, se [Planlegge på nytt eller fornye produksjonsordrer direkte](production-how-to-replan-refresh-production-orders.md).  

## <a name="see-also"></a><a name="see-also"></a>Se også

[Produksjon](production-manage-manufacturing.md)
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
