---
title: Selge montere-til-ordre-varer og lagervarer sammen | Microsoft-dokumentasjon
description: Hvis en monteringsvare er definert for Monter til lager, forutsetter standard ordreprosess at varen allerede er montert og kan plukkes fra lager, hvis den er tilgjengelig. Men hvis det er en del av (eller hele) antallet som ikke er tilgjengelig, må du å opprette en monteringsordre for det gjenværende antallet direkte.
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
ms.openlocfilehash: 4581e1f21e87190d75aa0048e9f5aabf8dd85fe0
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "932530"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>Selge montere til ordre-varer og lagervarer sammen
Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare inneholder **Monter til lager**, forutsetter standard ordreprosess at varen allerede er montert og kan plukkes fra lager, hvis den er tilgjengelig. Ingen monteringsordre blir derfor automatisk opprettet og koblet til ordrelinjen. Hvis en del av (eller hele) antallet imidlertid ikke er tilgjengelig, kan du opprette en monteringsordre for restantallet ved å fylle ut feltet **Ant. som skal monteres til ordre** på ordrelinjen. Slik kan du montere varen til ordre selv om den er definert slik at den monteres til lager som standard.  

Det finnes en lignende fleksibilitet når du selger varer som skal monteres til ordre og en del av antallet, som du vil trekke fra monteringsordren, finnes på lager. Hvis du vil ha mer informasjon, kan du se [Selge lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
>  Visse regler gjelder for feltet **Levere (antall)** på ordrelinjer som inneholder en kombinasjon av monter-til-ordre-antall og lagerantall. Hvis du vil ha mer informasjon, kan du se delen Kombinasjonsscenarier i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  Følgende fremgangsmåte omfatter ikke standardtrinnene for ordrer som du må følge før du oppretter en monteringsordre for utilgjengelige antall.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>Selge montere til ordre-varer og lagervarer sammen  
1.  På en salgsordrelinje for en vare som er definert slik at den monteres til lager angir du et antall i feltet **Antall** som overskrider beholdningen. Siden **Kontroller tilgjengelighet** vises. Hvis du vil ha mer informasjon, kan du se [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).
2.  Noter verdien i feltet **Antall i alt** (en negativ verdi), som du vil angi i neste trinn.  
3.  Angi verdien fra forrige trinn i feltet **Ant. som skal monteres til ordre**.  
4.  Gjør eventuelle endringer i monteringskomponentene. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Fortsett med å frigi ordren, for å klargjøre den for plukking av lagervarer og for montering av de utilgjengelige varene. Hvis du vil ha mer informasjon om disse standardtrinnene for montering, kan du se [Montere varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  **Hyllekode**-feltet på ordren kan bli forhåndsutfylt i henhold til feltet **Hyllek. lev. fra m. til ordre** eller **Fra Hyllekode for montering** på lokasjonskortet. I dette tilfellet er kanskje **Hyllekode**-feltet på ordrelinjen feil i denne kombinasjonen av montere-til-ordre- og montere-til-lager-antall. Det er en god idé å undersøke **Hyllekode**-feltet og kontrollere at plasseringen fungerer for alle antall. Du kan også angi to forskjellige antall på separate ordrelinjer.  

## <a name="see-also"></a>Se også  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeide med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
