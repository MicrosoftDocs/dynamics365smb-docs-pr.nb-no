---
title: Oppdatere valutakurser | Microsoft-dokumentasjon
description: Arbeide med flere valutaer
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Oppdatere valutakurser
Du må definere en kode for hver valuta du bruker hvis du kjøper eller selger i andre valutaer enn din lokale valuta, har kundekonti eller leverandørkonti i andre valutaer, eller registrerer finanstransaksjoner i forskjellige valutaer.  

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).

Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert. Tjenesten Yahoo-valutakurser er forhåndsinstallert og klar til å aktiveres.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Slik konfigurerer du en valutakurstjeneste
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Valutakurstjenester**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**.
3. I vinduet **Valutakurstjeneste** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Merk av for **Aktivert** for å aktivere tjenesten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Oppdatere valutakurser via en tjeneste
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Valutaer**, og deretter velger du den beslektede koblingen.
2. Velg **Oppdater valutakurser**.

Verdien i **Valutakurs**-feltet i **Valutaer**-vinduet oppdateres med den nyeste valutakursen.

## <a name="see-also"></a>Se også
[Avslutt år og perioder](year-close-years-periods.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

