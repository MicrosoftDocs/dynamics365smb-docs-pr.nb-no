---
title: Sette opp leveringsmåter | Microsoft Docs
description: Du kan sette opp en kode for hver av leveringsmåtene du tilbyr, og angi informasjon om dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 06/17/2019
ms.author: sgroespe
ms.openlocfilehash: 7248f49e92db98cec047d2035ce82d7caf84799f
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632786"
---
# <a name="set-up-shipment-methods"></a>Sette opp leveringsmåter
Leveringsmåter, også kalt "incoterms", avhenger ofte av varene, kundene og leverandørene. Hvis kunden for eksempel bor på en øy, kan han/hun velge om varene skal sendes med fly eller båt. Noen kunder kan be om levering neste dag. Noen ønsker kanskje å hente ordren. På kunde- og leverandørkortene kan du angi hvilken leveringsmåte du ønsker.

Du definerer beskrivelsen og koden for hver leveringsmåte på siden **Leveringsmåter**. Du kan for eksempel sette opp koden FOB og skrive inn Fritt om bord i **Beskrivelse**-feltet. Deretter kan du angi koden i **Leveringsmåtekode**-feltet andre steder i systemet, for eksempel på et kundekort. Når dette er gjort og du oppretter nye ordrer, fakturaer, kredittnotaer og så videre, angir systemet beskrivelsen representert av koden. Du kan endre den i dokumentet etter behov.

## <a name="to-set-up-a-shipment-code"></a>Slik setter du opp en leveringskode
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leveringsmåter** og velg deretter den relaterte koblingen.
2. På siden **Leveringsmåter** velger du **Ny**-handlingen.
3. Angi en kode og en beskrivelse for leveringsmåten på den nye linjen.

## <a name="see-also"></a>Se også
[Incoterms](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Definere transportører](sales-how-to-set-up-shipping-agents.md)  
[Spore pakker](sales-how-track-packages.md)    
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
