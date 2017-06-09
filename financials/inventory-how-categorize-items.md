---
title: Kategorise varer| Microsoft-dokumentasjon
description: Beskriver hvordan du organiserer varer i kategorier.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 06f50a356ddc3a501c28fe34891213b55a12e3fd
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-categorize-items"></a>Kategorisere varer
For å holde oversikt over varene og hjelpe deg med å sortere og søke etter varer, er det nyttig å kunne organisere dem i varekategorier.

Hvis du vil søke etter varer etter egenskaper, kan du tilordne vareattributter til varer og også varekategorier. Hvis du vil ha mer informasjon, kan du se [Arbeide med vareattributter](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Slik oppretter du en varekategori:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varekategorier**, og deretter velger du den beslektede koblingen.
2. I vinduet **Varekategorier** velger du handlingen **Ny**.
3. Fyll ut følgende felt på hurtigfanen **Generelt** i vinduet **Varekategorikort** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I **Attributter**-hurtigfanen angir du hvilke som helst vareattributter for varekategorien. Hvis du vil ha mer informasjon, se "Slik tilordner du vareattributter til en varekategori" i [Arbeide med vareattributter](inventory-how-work-item-attributes.md).

**Merk**: Hvis varekategorien har en overordnet varekategori, som angitt av **Overordnet kategori**-feltet, blir vareattributter som er tilordnet til denne overordnede varekategorien, forhåndsutfylt på **Attributter**-hurtigfanen.

**Merk:**: Vareattributter som du tilordner til en varekategori, vil automatisk brukes på varen som varekategorien er tilordnet til.

## <a name="to-assign-an-item-category-to-an-item"></a>Slik tilordner du en varekategori til en vare:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for varen som du vil tilordne til en varekategori.
3. Velg oppslagsknappen i feltet **Varekategorikode** og velg en eksisterende varekategori. Du kan også velge **Ny**-handlingen for å opprette en ny varekategori først, som forklart under "Slik oppretter du en varekategori".

## <a name="see-also"></a>Se også
[Arbeide med vareattributter](inventory-how-work-item-attributes.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

