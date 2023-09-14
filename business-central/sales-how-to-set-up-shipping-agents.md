---
title: Definere transportører
description: Lær hvordan du definerer en kode for hver enkelt transportør og angir beskrivende informasjon om hver av dem og hvilke tjenester de tilbyr.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="set-up-shipping-agents"></a>Definere transportører
Du kan definere en kode for hver enkelt transportør og angi opplysninger om dem.  

Hvis du oppgir en internettadresse til transportøren, og vedkommende tilbyr pakkesporingsservice på Internett, kan du bruke funksjonen for automatisk sporing av pakker. Hvis du vil ha mer informasjon, kan du se [Spore pakker](sales-how-track-packages.md).

Når du definerer transportører i ordrene, kan du også angi hvilken service den enkelte transportør tilbyr.  
Du kan definere et ubegrenset serviceantall for hver transportør, og angi en leveringstid for den enkelte service som utføres.  

Når du har tilordnet en transportørservice til en ordrelinje, tas leveringstiden for servicen med i beregningen av ordrebekreftelsen for denne linjen. Hvis du vil ha mer informasjon, kan du se [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Slik definerer du transportører
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transportører**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3.  Velg handlingen **Transportørservice**.
4. I vinduet **Transportørservice** fyller du ut feltene etter behov.

> [!NOTE]  
>  Hvis du sletter transportøren på ordrelinjen, slettes også transportørservicekoden. Innholdet i feltene som var delvis basert på transportørservice, beregnes på nytt.  

## <a name="see-also"></a>Se også
[Sette opp leveringsmåter](sales-how-set-up-shipment-methods.md)  
[Spore pakker](sales-how-track-packages.md)    
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
