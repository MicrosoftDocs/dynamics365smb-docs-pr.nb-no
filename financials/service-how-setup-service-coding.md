---
title: Definere koder for standardservice | Microsoft-dokumentasjon
description: "Finn ut hvordan du kan definere koder for serviceaktiviteter som utføres ofte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8a31e312fc12d75d4eb75a191b2b82bf9a6ff3c5
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-standard-service-codes"></a>Definere standard servicekoder
Når du utfører typisk service, må du ofte opprette servicedokumenter som bruker servicelinjer som inneholder omtrent samme opplysninger. Hvis du vil gjøre det enkelt å opprette disse linjene, kan du definere standard servicekoder som er et forhåndsdefinert sett med servicelinjer. Når du velger koden i et servicedokument, angis linjene automatisk. Du kan angi så mange standard servicekoder du vil, og hver kode kan ha et ubegrenset antall servicelinjer av ulike typer, inkludert vare, ressurs, kostnad eller standardtekst, knyttet til seg. Det kan opprettes servicelinjer for hver standard servicekode i korter **Standard servicekode**. Du tilordner deretter standard servicekoder til servicevaregrupper på siden **Standard servicevaregruppekoder**. Senere, når du oppretter et servicedokument, kan du bruke handlingen **Hent standard servicekoder** for å legge til servicelinjer.  
  
> [!Tip]
>  Du kan bruke samme metode for å opprette linjer i salgs- og kjøpsdokumenter. Hvis du vil ha mer informasjon, se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>Slik definerer du standard servicekoder    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Standard servicekoder**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Fyll ut servicelinjene som er koblet til denne servicekoden.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Slik knytter du en standard servicekode til en servicevaregruppe
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Servicevaregrupper**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyll ut servicelinjene som er koblet til denne servicekoden.  

## <a name="see-also"></a>Se også
[Servicehåndtering](service-service.md)
