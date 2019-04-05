---
title: Designdetaljer – Håndtere ordrer før den planlagte startdatoen | Microsoft-dokumentasjon
description: Dette emnet beskriver reglene som planlegging gjelder for bestillinger i den frosne sonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 9fee9eff60b441ef2d4782a77a6fbbbe8b01af03
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803289"
---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Designdetaljer: Håndtere ordrer før den planlagte startdatoen
For å unngå at en leveringsplan viser umulige og dermed ubrukelige forslag, regner planleggingssystemet perioden frem til den planlagte startdatoen som en frossen sone der ingenting er planlagt. Følgende regel gjelder den frosne sonen:  

Alle tilbud og etterspørsel før startdatoen for planleggingsperioden blir betraktet som en del av beholdningen eller levert.  

Planleggingssystemet vil derfor ikke, med noen få unntak, foreslå endringer for forsyningsordrer i den frosne sonen, og ingen koblinger for ordresporing opprettes eller vedlikeholdes for denne perioden.  

Unntakene fra denne regelen er som følger:  

* Hvis forventet disponibel beholdning, inkludert summen av forsyning og behov i den frosne sonen, er under null.  
* Hvis serie-/partinumre er nødvendige på tilbakedaterte ordre(r).  
* Hvis forsyningsbehovsettet er koblet til et ordre-til-ordre-prinsipp.  

Hvis den første disponible beholdningen er under null, foreslår planleggingssystemet en kritisk ordre på dagen før planleggingsperioden, for å dekke antallet som mangler. Forventet og tilgjengelige beholdning vil derfor alltid være minst null når planlegging for den fremtidige perioden begynner. Planleggingslinjen for denne forsyningsordren har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag.  

## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/partinumre og ordre-til-ordre-koblinger er fritatt fra den frosne sonen  
Hvis serie-/partinumre er nødvendige eller det finnes en ordre-til-ordre-kobling, vil planleggingssystemet se bort fra den frosne sonen og inkludere slike antall som er tilbakedaterte fra startdatoen og potensielt foreslå korrigerende handlinger hvis behov og forsyning ikke er synkronisert. Forretningsårsaken til dette prinsippet er at slike bestemte sett med behov/forsyning må samsvare for å sikre at dette bestemte behovet dekkes.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
