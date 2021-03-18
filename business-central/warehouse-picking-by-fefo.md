---
title: Aktivere plukking etter FEFO | Microsoft-dokumentasjon
description: FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ae07bc4f1d9f348f08f591e5e4341938ec4b5f16
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382207"
---
# <a name="enable-picking-items-by-fefo"></a>Aktivere plukking av varer etter FEFO
FEFO (først utløpt, først ut) er en sorteringsmetode som sikrer at de eldste elementene, det vil si de med de tidligste utløpsdato, plukkes først.  

 Denne funksjonaliteten fungerer bare når følgende kriterier er oppfylt:  

-   Varen må ha et serie-/partinummer.  
-   På varens varesporingskodeoppsett må feltet **Lagers.nr. - sporing** eller feltet **Lagerparti - sporing** velges.  
-   Varen må bokføres til lager med en utløpsdato.  
-   Det må merkes av for **Plukk nødv.** på lokasjonskortet.  
-   Det må merkes av for **Plukk i henhold til FEFO** på lokasjonskortet.  
-   Det må merkes av for **Hylle obligatorisk** på lokasjonskortet.  

 Når alle kriteriene er oppfylt, sorteres serie-/partinummererte varer som skal plukkes, med de eldste først i alle plukk og flyttinger, unntatt for varer som bruker SN-spesifikk eller partispesifikk sporing.  

> [!NOTE]  
> Hvis enkelte serie-/partinummererte varer bruker spesifikk sporing, har disse førsteprioritet, og under disse vises de gjenstående, ikke-spesifikke serie-/partinumrene i henhold til FEFO.
<br /><br />
Hvis to serie-/partinummererte varer har samme utløpsdato, velges varen med lavest serie- eller partinummer.
<br /><br />
Når du plukker serie-/partinummererte varer i lokasjoner definert for lagerstyring, blir bare antall i hyller av typen *Plukk* plukket i henhold til FEFO.  
<br /><br />
Når du skal aktivere flyttinger i henhold til FEFO, må du la **Fra hylle**-feltet stå tomt på siden **Lagerflytting** eller **Flytteforslag**.  
<br /><br />
Hvis feltet **Bruk ikke etter utløpsdato** er valgt, inkluderes bare varer som ikke er utløpt, i plukkingen. Dette gjelder selv om du ikke bruker plukk i henhold til FEFO.

## <a name="see-also"></a>Se også  
[Plukke varer](warehouse-pick-items.md)   
[Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]