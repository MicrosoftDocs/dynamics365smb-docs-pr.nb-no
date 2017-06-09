---
title: Arbeide med vareattributter| Microsoft-dokumentasjon
description: Beskriver hvordan du konfigurerer vareattributter og tilordner dem til varer og varekategorier.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/20/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 82fee2e5b1ae3e87e607cd930973a8be32045e71
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-item-attributes"></a>Arbeide med vareattributter
Når en kunde sender en forespørsel om en vare, enten i korrespondanse eller i en integrert nettbutikk, kan kunden spørre om eller søke etter i henhold til egenskaper, for eksempel høyde og modellår. Hvis du vil levere denne kundeservicen, kan du tilordne varen attributtverdier av forskjellige typer, som deretter kan brukes ved søk etter varer.

Du kan også tilordne vareattributter til varekategorier, som deretter brukes på varene som bruker varekategoriene. Hvis du vil ha mer informasjon, kan du se [Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-create-item-attributes"></a>Slik oppretter du vareattributter:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Vareattributter**, og deretter velger du den beslektede koblingen.
2. I vinduet **Vareattributter** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov i vinduet **Vareattributt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Merk**: Hvis du velger **Alternativ** i **Type**-feltet, kan du deretter velge handlingen **Verdier for vareattributt** for å opprette verdier for vareattributtet. Hvis du vil ha mer informasjon, kan du se avsnittet "Slik oppretter du verdier for vareattributter av typen Alternativ".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Slik oppretter du verdier for vareattributter av typen Alternativ:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Vareattributter**, og deretter velger du den beslektede koblingen.
2. I vinduet **Vareattributter** velger du et vareattributt av typen **Alternativ** som du vil opprette verdier for, og deretter velger du handlingen **Verdier for vareattributt**.
3. Fyll ut feltene etter behov i vinduet **Verdier for vareattributt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Slik tilordner du vareattributter til varer:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. I vinduet **Varer** velger du vareattributtet du vil tilordne vareattributter til, og deretter velger du handlingen **Attributter**.
3. I vinduet **Verdier for vareattributt** velger du handlingen **Ny**.
4. I **Attributt**-feltet velger du oppslagsknappen og velger et eksisterende vareattributt. Du kan også velge **Ny**-handlingen for å opprette et nytt vareattributt først, som forklart under "Slik oppretter du vareattributter".
5. I **Verdi**-feltet angir du vareattributtverdien, for eksempel "2010" for attributtet **Modellår**.
6. For vareattributter av typen **Alternativ** velger du oppslagsknappen i **Verdi**-feltet og velger en verdi for vareattributtet. Du kan også velge **Ny**-handlingen for å opprette en ny vareattributtverdi først, som forklart under "Slik oppretter du verdier for vareattributter av typen Alternativ".
7. Gjenta trinn 4 til 6 for alle vareattributter du vil tilordne varen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Slik tilordner du vareattributter til varekategorier:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varekategorier**, og deretter velger du den beslektede koblingen.
2. I vinduet **Varekategorier** velger du varekategorien du vil tilordne vareattributter til, og deretter velger du handlingen **Rediger**.
3. I **Varekategorikort**-vinduet på **Attributter**-hurtigfanen velger du handlingen **Ny**.
4. I **Attributt**-feltet velger du oppslagsknappen og velger et eksisterende vareattributt. Du kan også velge **Ny**-handlingen for å opprette et nytt vareattributt først, som forklart under "Slik oppretter du et vareattributt".
5. I **Standardverdi**-feltet velger du oppslagsknappen og velger en verdi for vareattributtet.
6. Gjenta trinn 4 og 5 for alle vareattributter du vil tilordne varekategorien.

**Merk**: Vareattributter for overordnede varekategorier arves til underordnede varekategorier. Dette angis av **Arvet fra**-feltet på **Attributter**-hurtigfanen. Hvis du vil ha mer informasjon, kan du se [Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Slik filtrerer du etter vareattributter:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. I vinduet **Varer** velger du handlingen **Filtrer etter attributter**.
3. I vinduet **Filtrer varer etter attributt** velger du oppslagsknappen i **Attributt**-feltet og et vareattributt.
4. I **Verdi**-feltet velger du oppslagsknappen og velger en eksisterende attributtverdi å filtrere varer etter.

    **Merk**: Du kan bare velge verdier direkte for vareattributter som har faste verdier, for eksempel farge. For vareattributter med variable verdier, for eksempel bredde, må du angi verdien for vareattributtet ved først å velge en betingelse. Se trinn 5.
5. I **Verdi**-feltet for et variabelt vareattributt velger du oppslagsknappen.
6. I **Betingelse**-feltet i vinduet **Angi filterverdi** velger du rullegardinpilen og velger en betingelse.
7. I **Verdi**-feltet angir du en attributtverdi å filtrere varer etter.

    **Eksempel**: Hvis du vil filtrere på varer der materialbeskrivelsen begynner med "blå", fyller du ut feltene som følger: **Attributt**-feltet: Materialbeskrivelse, **Betingelse**-feltet: Begynner med, **Verdi**-felt: blå.
8. Velg **OK**-knappen.   

Varene i vinduet **Varer** er filtrert etter de angitte verdiene for vareattributt.

## <a name="see-also"></a>Se også
[Kategorisere varer](inventory-how-categorize-items.md)    
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

