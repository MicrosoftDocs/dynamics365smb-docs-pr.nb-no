---
title: Selge lagervarer i monter-til-ordre-flyter | Microsoft-dokumentasjon
description: Hvis varen er definert for et kort for en Monter til ordre, forutsetter standard ordreprosess at varen ikke er på lager og må monteres for denne bestemte ordren. Det blir derfor automatisk opprettet en monteringsordre når du legger varen til på en ordrelinje.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 188df39e5381f331da338aec1284b44f4e329977
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "931821"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Selge lagervarer i monter-til-ordre-flyter
Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare inneholder **Monter til ordre**, forutsetter standard ordreprosess at varen ikke er på lager og må monteres for denne bestemte ordren. Det blir derfor automatisk opprettet en monteringsordre når du legger varen til på en ordrelinje. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md). Hvis en del av (eller hele) ordreantallet allerede er tilgjengelig i beholdningen, kan du redusere monteringsordreantallet ved å endre feltet **Ant. som skal monteres til ordre** på ordrelinjen.  

Dette scenariet er sjeldent fordi montere-til-ordre-varer forventes å alltid være tilpasset, og sjansen for at de er på lager i konfigurasjonen som er forespurt av en annen kunde, er lav. Hvis et selskap imidlertid har montere-til-ordre-antall i beholdningen på grunn av returer eller ordrekanselleringer, må disse antallene plukkes og selges før nye monteres.  

> [!NOTE]  
>  Det finnes ingen funksjonalitet på salgsordrer som varsler automatisk eller hjelper deg med å trekke fra monteringsordreantallet som allerede er tilgjengelig. Du må overvåke tilgjengelighetsinformasjonen, for eksempel i faktaboksen **Salgslinjedetaljer** i stedet.  

Det finnes lignende funksjonalitet når du selger monteringsvarer fra beholdningen og en del av eller hele antallet er utilgjengelig og kan forsynes av en monteringsordre. Hvis du vil ha mer informasjon, kan du se [Selge montere-til-ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Visse regler gjelder for feltet **Levere (antall)** på ordrelinjer som inneholder en kombinasjon av monter-til-ordre-antall og lagerantall. Hvis du vil ha mer informasjon, kan du se delen Kombinasjonsscenarier i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

I denne fremgangsmåten erstatter du montere-til-ordre-antall med lagerantall på en ordrelinje. Trinnene inkluderer å finne ut om det er tilgjengelighet, trekke fra dette antallet fra den koblede monteringsordren og deretter reservere lagerantallet for å sikre at det blir plukket og levert for ordren.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Selge lagervarer i montere til ordre-flyter  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Opprett en ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  
3.  På en salgsordrelinje for en montere-til-ordre-vare angir du forespurt antall i feltet **Antall**.  
4.  Finn ut om alt eller noe av behovsantallet er disponibelt, i faktaboksen **Salgslinjedetaljer**.  
5.  Trekk fra disponibelt antall i feltet **Ant. som skal monteres til ordre**, slik at bare det ikke-disponible antallet monteres til ordren. **Reservert antall**-feltet reduseres tilsvarende for å gjenspeile at koblingen for ordre-til-ordre eller reservasjon bare gjelder for antallet som skal monteres.  
6.  På hurtigfanen **Linjer** velger du **Funksjoner** og deretter **Reserver**.  
7.  Velg varepostlinjen eller -linjene som inneholder det disponible antallet på **Reservasjon**-siden, velg **Reserver fra gjeldende linje**, og klikk deretter **OK**.  

    På **Ordre**-siden viser **Reservert antall**-feltet at hele antallet på ordrelinjen er reservert. Feltet **Ant. som skal monteres til ordre** gjenspeiler fortsatt delantallet som skal monteres.  

8.  Frigi ordren for plukking av lagervarene og for montering av de utilgjengelige varene. Hvis du vil ha mer informasjon, kan du se [Montere varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  **Hyllekode**-feltet på ordren kan bli forhåndsutfylt i henhold til feltet **Hyllek. lev. fra m. til ordre** eller **Fra Hyllekode for montering** på lokasjonskortet. I dette tilfellet er kanskje **Hyllekode**-feltet på ordrelinjen feil i denne kombinasjonen av montere-til-ordre- og montere-til-lager-antall. Det er en god idé å se i **Hyllekode**-feltet og sikre at plasseringen fungerer for alle antall. Du kan også angi to forskjellige antall på separate ordrelinjer.  

## <a name="see-also"></a>Se også  
[Monteringsstyring](assembly-assemble-items.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeide med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
