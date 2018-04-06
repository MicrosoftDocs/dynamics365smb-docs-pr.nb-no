---
title: "Anbefalte fremgangsmåter for oppsett – lagermetode | Microsoft-dokumentasjon"
description: "**Lagermetode** på varekortet definerer varekostnadsflyten, og om en faktisk eller budsjettert verdi kapitaliseres og brukes i kostnadsberegningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d4f533d42cc813d3ebc0ccbb00228a6c8e188c14
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-costing-method"></a>Anbefalte fremgangsmåter for oppsett: lagermetode
**Lagermetode** på varekortet definerer varekostnadsflyten, og om en faktisk eller budsjettert verdi kapitaliseres og brukes i kostnadsberegningen.  

 Det er viktig å angi riktig lagermetode i henhold til varetype og forretningsmiljø for å sikre økonomisk beholdninger.  

 Tabellen nedenfor gir nyttige tips om hvordan du setter opp **Lagermetode**-feltet. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).  

|Oppsettsalternativ|Anbefalt fremgangsmåte|Merknad|  
|------------------|-------------------|-------------|  
|FIFO|Bruk der produktkost er stabil.<br /><br /> Bruk for varer med en begrenset holdbarhet, fordi de eldste varene må selges før de overskrider siste salgsdato.|Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av FIFO-regelen.<br /><br /> I lagerverdisetting antas det at de første varene som plasseres på lager, selges først. **Obs!** Når prisene stiger, viser balansen større verdi. Dette betyr at skatteforpliktelser økes, men kredittverdigheten og mulighetene til å låne penger blir bedre.|  
|LIFO|Bruk der nivåer av beholdninger er konsekvent opprettholdt eller øker over tid.|Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av LIFO-regelen.<br /><br /> I lagerverdisetting antas det at de siste varene som plasseres på lager, selges først. **Obs!** Når prisene stiger, reduseres verdien i resultatregnskapet. Dette betyr at skatteforpliktelser reduseres, men mulighetene til å låne penger blir mindre. **Viktig!**  Ikke tillatt i mange land/områder, siden det kan brukes til å redusere fortjeneste.|  
|Gjennomsnitt|Bruk der produktkost er ustabil.<br /><br /> Bruk der beholdninger er stablet eller blandet sammen og ikke kan kan differensieres, for eksempel kjemikalier.|Enhetskosten for en vare er den nøyaktige kosten da den bestemte enheten ble mottatt.|  
|Serienummer|Bruk i produksjon av eller handel med lett gjenkjennelige varer med relativt høy enhetskost.<br /><br /> Bruk for varer som er underlagt regulering.<br /><br /> Bruk for varer med serienummer.|Enhetskosten for en vare beregnes som den gjennomsnittlige enhetskostnaden på hvert tidspunkt etter et kjøp.<br /><br /> For lagerverdi antas det at alle beholdninger selges samtidig.|  
|Standard|Bruk der kostnadskontroll er kritisk.<br /><br /> Bruk i gjentatt produksjon for å verdsette kostnadene for direkte materialer, direkte arbeid og indirekte produksjon.<br /><br /> Bruk der det er disiplin og ansatte for å opprettholde standardene.|Enhetskosten for en vare er forhåndsinnstilt basert på estimert kostnad.<br /><br /> Når de faktiske kostnadene senere realiseres, må standardkosten justeres til faktisk kost gjennom avviksverdier.|  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

