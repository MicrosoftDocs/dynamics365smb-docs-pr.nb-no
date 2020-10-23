---
title: Definere et lokasjonskort og definere overføringsruter | Microsoft-dokumentasjon
description: Du oppretter et lokasjonskort for hvert sted der du oppbevarer lagervarer, for eksempel et lager eller distribusjonssenter, og definerer ruter for å overføre varer mellom lokasjoner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 81ee1ad91bd4ec887d85e940152f18e99a6d464c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923773"
---
# <a name="set-up-locations"></a>Definer lokasjoner
Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.

Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner. Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="to-create-a-location-card"></a>Slik oppretter du et lokasjonskort
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gjenta trinn 2 og 3 for hver beholdninglokasjon.

> [!NOTE]  
> Mange felt på lokasjonskortet refererer til håndteringen av varer i inngående og utgående lagerprosesser. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Slik oppretter du overføringsruter
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overføringsruter**, og velg deretter den relaterte koblingen.
2. Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.
3. Velg handlingen **Ny**.
4. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nå kan du overføre lagervarer mellom to lokasjoner. Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Se også
[Håndtere lager](inventory-manage-inventory.md)  
[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)
