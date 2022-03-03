---
title: Plukk for interne operasjoner i avansert lageroppsett
description: Hvis lokasjonene bruker plukking i tillegg til levering, plukker du komponenter for produksjons- og monteringsaktiviteter på siden Lagerplukking.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5df764b1ca184d1f70dd67c08abf0505833dc2aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139134"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Plukke for montering eller produksjon i avanserte lageroppsett
I avansert lageroppsett der lokasjonen er definert slik at plukking og levering brukes, kan du plukke komponenter for produksjons- og monteringsaktiviteter ved å bruke **Plukk**-siden.  

Du kan også bruke siden **Flytteforslag** til å flytte varer mellom hyller ad hoc, noe som betyr uten referanse til et kildedokument. Hvis du vil ha mer informasjon, kan du se [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Hvis du vil ha mer informasjon om plukking av varer for interne operasjoner i grunnleggende lagerlokasjoner som er definert for bare plukking, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

Du kan ikke opprette et lagerplukkdokument fra grunnen av fordi en plukkaktivitet alltid er en del av en arbeidsflyt, enten i et pull- eller push-scenario.  

Du kan opprette lagerplukkdokumentet på en push-måte ved å velge **Opprett plukk** i kildedokumentet, for eksempel en frigitt monteringsordre eller lagerlevering. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan også opprette plukkdokumentet på en hentemåte ved å bruke siden **Plukkforslag** til å oppdage plukkforespørsler, både for levering og interne operasjoner, og deretter opprette de nødvendige plukkdokumentene.  

Fremgangsmåten nedenfor forklarer et plukkescenario der du plukker komponenter for en frigitt produksjonsordre via siden **Plukkforslag**. Fremgangsmåten gjelder også for en monteringsordre.  

Hvis du vil opprette plukkforespørsler, må de aktuelle kildedokumentene frigis både for plukk- og skyvscenarier. Frigi kildedokumenter for interne operasjoner på følgende måter.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produksjonsordre|Endre ordretypen til frigitt produksjonsordre.|  
|Monteringsordre|Endre status til Frigitt.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Slik plukker du komponenter ved hjelp av plukkforslaget  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Hent lagerdokumenter**, og velg deretter komponentlinjene fra den frigitte produksjonsordren.  
3.  Inspiser linjene, sorter dem for å sikre en effektiv plukkrunde, og slå dem sammen med andre forslagslinjer om nødvendig for å utnytte arbeidstiden best mulig.  
4.  Velg handlingen **Opprett plukk**.  
5.  Definer hvordan lagerplukkdokumenter skal opprettes og hvordan plukklinjer skal sorteres, ved å fylle ut felt på siden **Opprett plukk**.  
6.  Velg **OK**. Lagerplukkdokumenter opprettes med plukklinjer for hver komponent som kreves i den interne operasjonen.  

Hvis det interne operasjonsområdet, for eksempel en produksjon, er opprettet med en standardhylle for plassering av komponenter som skal brukes i operasjonen, settes denne hyllekoden inn på Plasser-linjene i plukkdokumentet for å gi lagermedarbeidere beskjed om hvor de skal plassere varene. Hvis du vil ha mer informasjon, se feltet **Til-Hyllekode for produksjon** eller **Til-Hyllekode for montering**.

## <a name="filling-the-consumption-bin"></a>Fylle forbrukshyllen
Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

![Flytskjema for hylle.](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Se også
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]