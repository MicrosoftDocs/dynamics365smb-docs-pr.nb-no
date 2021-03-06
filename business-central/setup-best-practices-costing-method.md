---
title: Anbefalte fremgangsmåter for oppsett - lagermetode
description: Lagermetode på varekortet definerer varekostnadsflyten, og om en faktisk eller budsjettert verdi kapitaliseres og brukes i kostnadsberegningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 87c3616a4d680f94a0997d503aa1569fd871bc9f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778075"
---
# <a name="setup-best-practices-costing-method"></a>Anbefalte fremgangsmåter for oppsett: lagermetode

**Lagermetode** på varekortet definerer varekostnadsflyten, og om en faktisk eller budsjettert verdi kapitaliseres og brukes i kostnadsberegningen.  

 Det er viktig å angi riktig lagermetode i henhold til varetype og forretningsmiljø for å sikre økonomisk beholdninger.  

 Tabellen nedenfor gir nyttige tips om hvordan du setter opp **Lagermetode**-feltet. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).  

|Oppsettsalternativ|Anbefalt fremgangsmåte|Merknad|  
|------------------|-------------------|-------------|  
|FIFO|Bruk der produktkost er stabil.<br /><br /> Bruk for varer med en begrenset holdbarhet, fordi de eldste varene må selges før de overskrider siste salgsdato.|Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av FIFO-regelen.<br /><br /> I lagerverdisetting antas det at de første varene som plasseres på lager, selges først. **Obs!** Når prisene stiger, viser balansen større verdi. Dette betyr at skatteforpliktelser økes, men kredittverdigheten og mulighetene til å låne penger blir bedre.|  
|LIFO|Bruk der nivåer av beholdninger er konsekvent opprettholdt eller øker over tid.|Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av LIFO-regelen.<br /><br /> I lagerverdisetting antas det at de siste varene som plasseres på lager, selges først. **Obs!** Når prisene stiger, reduseres verdien i resultatregnskapet. Dette betyr at skatteforpliktelser reduseres, men mulighetene til å låne penger blir mindre. **Viktig!**  Ikke tillatt i mange land/områder, siden det kan brukes til å redusere fortjeneste.|  
|Gjennomsnitt|Bruk der produktkost er ustabil.<br /><br /> Bruk der beholdninger er stablet eller blandet sammen og ikke kan kan differensieres, for eksempel kjemikalier.|Enhetskosten for en vare beregnes som den gjennomsnittlige enhetskostnaden på hvert tidspunkt etter et kjøp.<br /><br /> For lagerverdi antas det at alle beholdninger selges samtidig.|
|Serienummer|Bruk i produksjon av eller handel med lett gjenkjennelige varer med relativt høy enhetskost.<br /><br /> Bruk for varer som er underlagt regulering.<br /><br /> Bruk for varer med serienummer.|Enhetskosten for en vare er den nøyaktige kosten da den bestemte enheten ble mottatt.|
|Standard|Bruk der kostnadskontroll er kritisk.<br /><br /> Bruk i gjentatt produksjon for å verdsette kostnadene for direkte materialer, direkte arbeid og indirekte produksjon.<br /><br /> Bruk der det er disiplin og ansatte for å opprettholde standardene.|Enhetskosten for en vare er forhåndsinnstilt basert på estimert kostnad.<br /><br /> Når de faktiske kostnadene senere realiseres, må standardkosten justeres til faktisk kost gjennom avviksverdier.|  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]