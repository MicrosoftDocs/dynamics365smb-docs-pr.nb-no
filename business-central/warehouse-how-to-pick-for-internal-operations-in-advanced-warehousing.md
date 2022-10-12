---
title: Plukk for interne operasjoner i avansert lageroppsett
description: Hvis lokasjonene bruker plukking og levering, plukker du komponenter for produksjons-, monterings- og prosjektaktiviteter på siden Lagerplukking.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607557"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Plukke for produksjon, montering eller jobber i avanserte lageroppsett

I avansert lageroppsett der lokasjonen er definert slik at plukking og levering brukes, kan du plukke komponenter for produksjons- og monteringsaktiviteter på **Plukk**-siden.  

Du kan også bruke siden **Flytteforslag** til å spontant flytte varer mellom hyller uten referanse til et kildedokument. Hvis du vil ha mer informasjon, kan du se [Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Hvis du vil ha mer informasjon om plukking av varer i grunnleggende lagerlokasjoner som er definert for bare plukking, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).  

> [!NOTE]
> Du kan ikke opprette et lagerplukkdokument fra grunnen av fordi en plukkaktivitet alltid er en del av en arbeidsflyt, enten i et pull- eller push-scenario.  

Du kan opprette lagerplukkdokumentet på en push-måte ved å velge **Opprett plukk** i kildedokumentet, for eksempel en frigitt monteringsordre eller lagerlevering. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Du kan også opprette et lagerplukkdokument på en hente-måte ved å bruke **Plukkforslag**-siden til å finne plukkforespørsler. Denne metoden er nyttig for forsendelser og interne operasjoner. Deretter kan du opprette de nødvendige lagerplukkdokumentene.  

Fremgangsmåten nedenfor forklarer et plukkescenario der du plukker komponenter for en frigitt produksjonsordre via siden **Plukkforslag**. Fremgangsmåten gjelder også for en monteringsordre.  

Hvis du vil opprette plukkforespørsler, må de aktuelle kildedokumentene frigis både for plukk- og skyvscenarier. Frigi kildedokumenter for interne operasjoner på følgende måter.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produksjonsordre|Endre ordretypen til frigitt produksjonsordre.|  
|Monteringsordre|Endre status til Frigitt.|
|Prosjekter | Endre status til Åpen.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>Slik plukker du komponenter ved hjelp av plukkforslaget

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Plukkforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Hent lagerdokumenter**, og velg deretter komponentlinjene fra den frigitte produksjonsordren.  
3. Sorter linjene for å sikre effektiv plukking. Du vil kanskje kombinere linjer for å spare tid for ansatte.  
4. Velg handlingen **Opprett plukk**.  
5. Definer hvordan lagerplukkdokumenter skal opprettes og hvordan plukklinjer skal sorteres, ved å fylle ut felt på siden **Opprett plukk**.  
6. Velg **OK**. Lagerplukkdokumenter opprettes med plukklinjer for hver komponent som kreves i den interne operasjonen.  

Operasjonsområder, for eksempel produksjonsutførelse, kan ha en standardhylle for komponentene de trenger. Hvis dette er tilfellet, legges standard hyllekode til i lagerplukkdokumentet for å angi hvor varene skal plasseres. Hvis du vil ha mer informasjon, kan du se verktøytipsene for feltene **Til-Hyllekode for produksjon** eller **Til-Hyllekode for montering**.

## <a name="filling-the-consumption-bin"></a>Fylle forbrukshyllen

Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

![Flytskjema for hylle.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
