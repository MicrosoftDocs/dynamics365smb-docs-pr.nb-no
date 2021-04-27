---
title: Sette opp leveringsmåter
description: Du kan sette opp en kode for hver av leveringsmåtene du tilbyr, og angi informasjon om dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778575"
---
# <a name="set-up-shipment-methods"></a>Sette opp leveringsmåter

Leveringsmåter avhenger ofte av varene, kundene og leverandørene. Hvis kunden for eksempel bor på en øy, kan han/hun velge om varene skal sendes med fly eller båt. Noen kunder kan be om levering neste dag. Noen ønsker kanskje å hente ordren. På kunde- og leverandørkortene kan du angi hvilken leveringsmåte du ønsker.

Du definerer beskrivelsen og koden for hver leveringsmåte på siden **Leveringsmåter**. Du kan for eksempel sette opp koden FOB og skrive inn Fritt om bord i **Beskrivelse**-feltet. Deretter kan du angi koden i **Leveringsmåtekode**-feltet andre steder i systemet, for eksempel på et kundekort. Når dette er gjort og du oppretter nye ordrer, fakturaer, kredittnotaer og så videre, angir systemet beskrivelsen representert av koden. Du kan endre den i dokumentet etter behov.

## <a name="to-set-up-a-shipment-method"></a>Slik definerer du leveringsmåter

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leveringsmåter**, og velg deretter den relaterte koblingen.
2. På siden **Leveringsmåter** velger du **Ny**-handlingen.
3. Angi en kode og en beskrivelse for leveringsmåten på den nye linjen.

> [!TIP]
> Hvis du bruker Incoterms, må du definere leveringsmåter for å representere de aktuelle Incoterms-reglene.  

## <a name="see-also"></a>Se også

[Sett opp transportører](sales-how-to-set-up-shipping-agents.md)  
[Spore pakker](sales-how-track-packages.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms på iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]