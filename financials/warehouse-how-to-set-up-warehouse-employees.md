---
title: Definere lageransatte | Microsoft-dokumentasjon
description: "Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til én standardlokasjon og eventuelt flere ikke-standardlokasjoner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45a5f7e2140bffd192ecb586e45cc44894752656
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-warehouse-employees"></a>Definere lageransatte
Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til én standardlokasjon og eventuelt flere ikke-standardlokasjoner. Dette brukeroppsettet filtrerer alle lageraktiviteter i databasen etter den ansattes lokasjon slik at den ansatte bare kan utføre lageraktivitetene i standardlokasjonen. En bruker kan tilordnes til flere ikke-standardlokasjoner som den ansatte kan vise aktivitetslinjer for, men ikke utføre aktiviteter for.

## <a name="to-set-up-warehouse-employees"></a>Slik definerer du lageransatte  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg **Bruker-ID**-feltet, og velg deretter brukeren som skal legges til som lageransatt. Velg **OK**-knappen.  
6.  I feltet **Lokasjonskode** skriver du inn koden for lokasjonen der brukeren skal arbeide.  
7.  Merk av for **Standard** for å definere lokasjonen som den eneste lokasjonen der den ansatte kan utføre lageraktiviteter.  
8.  Gjenta disse trinnene for å tilordne andre ansatte til lokasjoner, eller for å tilordne ikke-standardlokasjoner til eksisterende lageransatte.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

