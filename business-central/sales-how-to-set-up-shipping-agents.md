---
title: Definere transportører | Microsoft-dokumentasjon
description: Du kan definere en kode for hver enkelt transportør og angi opplysninger om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d6a4bac4d540a65cc164029b23b063c8c9dbc1fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192660"
---
# <a name="set-up-shipping-agents"></a>Definere transportører
Du kan definere en kode for hver enkelt transportør og angi opplysninger om dem.  

Hvis du oppgir en internettadresse til transportøren, og vedkommende tilbyr pakkesporingsservice på Internett, kan du bruke funksjonen for automatisk sporing av pakker. Hvis du vil ha mer informasjon, kan du se [Spore pakker](sales-how-track-packages.md).

Når du definerer transportører i ordrene, kan du også angi hvilken service den enkelte transportør tilbyr.  
Du kan definere et ubegrenset serviceantall for hver transportør, og angi en leveringstid for den enkelte service som utføres.  

Når du har tilordnet en transportørservice til en ordrelinje, tas leveringstiden for servicen med i beregningen av ordrebekreftelsen for denne linjen. Hvis du vil ha mer informasjon, kan du se [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Slik definerer du transportører  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Transportører**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Velg handlingen **Transportørservice**.
4. I vinduet **Transportørservice** fyller du ut feltene etter behov.

> [!NOTE]  
>  Hvis du sletter transportøren på ordrelinjen, slettes også transportørservicekoden. Innholdet i feltene som var delvis basert på transportørservice, beregnes på nytt.  

## <a name="see-also"></a>Se også
[Sette opp leveringsmåter](sales-how-set-up-shipment-methods.md)  
[Spore pakker](sales-how-track-packages.md)    
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
