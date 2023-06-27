---
title: Organisere varer i kategorier (inneholder video) | Microsoft Docs
description: For å gjøre det enklere å søke etter og finne varer kan du tilordne vareattributter og organisere varer i kategorier.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'category, search, attribute, facet'
ms.search.form: '5730, 5733, 5401'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="categorize-items" />Kategorisere varer

For å holde oversikt over varene og hjelpe deg med å sortere og søke etter varer, er det nyttig å kunne organisere dem i varekategorier.

Hvis du vil søke etter varer etter egenskaper, kan du tilordne vareattributter til varer og også varekategorier. Hvis du vil ha mer informasjon, kan du se [Arbeide med vareattributter](inventory-how-work-item-attributes.md).
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category" />Slik oppretter du en varekategori:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekategorier** og velg den relaterte koblingen.
2. På siden **Varekategorier** velger du handlingen **Ny**.
3. Fyll ut følgende felt på hurtigfanen **Generelt** på siden **Varekategorikort** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I **Attributter**-hurtigfanen angir du hvilke som helst vareattributter for varekategorien. Hvis du vil ha mer informasjon, kan du se [Slik tilordner du vareattributter til varekategorier](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Hvis varekategorien har en overordnet varekategori, som angitt av feltet **Overordnet kategori**, blir vareattributter som er tilordnet til denne overordnede varekategorien, forhåndsutfylt i hurtigfanen **Attributter**.

> [!NOTE]  
> Vareattributter du tilordner til en varekategori, brukes automatisk på varen som varekategorien er tilordnet til.

Hvis du ombestemmer deg om en varekategori, kan du slette den. Hvis den imidlertid allerede er tilordnet til en vare, må du fjerne denne tilordningen før du kan slette varekategorien.

## <a name="to-assign-an-item-category-to-an-item" />Slik tilordner du en varekategori til en vare:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne kortet for varen som du vil tilordne til en varekategori.
3. Velg oppslagsknappen i feltet **Varekategorikode** og velg en eksisterende varekategori. Du kan også velge **Ny**-handlingen for å opprette en ny varekategori først, som forklart under [Slik oppretter du en varekategori](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants" />Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-related-microsoft-training" />Se relatert [Microsoft-opplæring](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Arbeid med vareattributter](inventory-how-work-item-attributes.md)  
[Behandle produktvarianter](inventory-item-variants.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
