---
title: Organisere varer i kategorier | Microsoft-dokumentasjon
description: For å gjøre det enklere å søke etter og finne varer kan du tilordne vareattributter og organisere varer i kategorier.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: d75a24a065d87cee1b40149e1a30f2bc595eaa88
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182279"
---
# <a name="categorize-items"></a>Kategorisere varer
For å holde oversikt over varene og hjelpe deg med å sortere og søke etter varer, er det nyttig å kunne organisere dem i varekategorier.

Hvis du vil søke etter varer etter egenskaper, kan du tilordne vareattributter til varer og også varekategorier. Hvis du vil ha mer informasjon, kan du se [Arbeide med vareattributter](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Slik oppretter du en varekategori:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekategorier**, og velg deretter den relaterte koblingen.
2. På siden **Varekategorier** velger du handlingen **Ny**.
3. Fyll ut følgende felt på hurtigfanen **Generelt** på siden **Varekategorikort** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I **Attributter**-hurtigfanen angir du hvilke som helst vareattributter for varekategorien. Hvis du vil ha mer informasjon, kan du se [Slik tilordner du vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
>   Hvis varekategorien har en overordnet varekategori, som angitt av feltet **Overordnet kategori**, blir vareattributter som er tilordnet til denne overordnede varekategorien, forhåndsutfylt i hurtigfanen **Attributter**.

> [!NOTE]  
>   Vareattributter du tilordner til en varekategori, brukes automatisk på varen som varekategorien er tilordnet til.

## <a name="to-assign-an-item-category-to-an-item"></a>Slik tilordner du en varekategori til en vare:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for varen som du vil tilordne til en varekategori.
3. Velg oppslagsknappen i feltet **Varekategorikode** og velg en eksisterende varekategori. Du kan også velge **Ny**-handlingen for å opprette en ny varekategori først, som forklart under [Slik oppretter du en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="see-also"></a>Se også
[Arbeide med vareattributter](inventory-how-work-item-attributes.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
