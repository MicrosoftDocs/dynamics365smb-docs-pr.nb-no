---
title: Definere vareattributter og tilordne dem til varer | Microsoft-dokumentasjon
description: Beskriver hvordan du for eksempel definerer verdier for vareattributt som kan brukes som søkeord, og knytter dem til varer og varekategorier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5c927a5d182cf2e33620496ea07cbc599d7537e3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181895"
---
# <a name="work-with-item-attributes"></a>Arbeide med vareattributter
Når en kunde sender en forespørsel om en vare, enten i korrespondanse eller i en integrert nettbutikk, kan kunden spørre om eller søke etter i henhold til egenskaper, for eksempel høyde og modellår. Hvis du vil levere denne kundeservicen, kan du tilordne varen attributtverdier av forskjellige typer, som deretter kan brukes ved søk etter varer.

Du kan også tilordne vareattributter til varekategorier, som deretter brukes på varene som bruker varekategoriene. Hvis du vil ha mer informasjon, kan du se [Kategorisere varer](inventory-how-categorize-items.md).

> [!Tip]  
> Hvis du legge ved bilder for varer, kan Image Analyzer-utvidelsen registrere attributter i bildet og foreslå attributtene, slik at du kan bestemme om du vil tilordne dem. Utvidelsen er klar til bruk. Du trenger bare å aktivere den. Hvis du vil ha mer informasjon, se [Image Analyzer-utvidelsen](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Slik oppretter du vareattributter:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareattributter**, og velg deretter den relaterte koblingen.
2. På siden **Vareattributter** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov på siden **Vareattributt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Hvis du velger **Alternativ** i **Type**-feltet, kan du deretter velge handlingen **Verdier for vareattributt** for å opprette verdier for vareattributtet. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du verdier for vareattributter av typen Alternativ](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Slik oppretter du verdier for vareattributter av typen Alternativ:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vareattributter**, og velg deretter den relaterte koblingen.
2. På siden **Vareattributter** velger du et vareattributt av typen **Alternativ** som du vil opprette verdier for, og deretter velger du handlingen **Verdier for vareattributt**.
3. Fyll ut feltene etter behov på siden **Verdier for vareattributt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Slik tilordner du vareattributter til varer:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. På siden **Varer** velger du vareattributtet du vil tilordne vareattributter til, og deretter velger du handlingen **Attributter**.
3. På siden **Verdier for vareattributt** velger du handlingen **Ny**.
4. I **Attributt**-feltet velger du oppslagsknappen og velger et eksisterende vareattributt. Du kan også velge **Ny**-handlingen for å opprette et nytt vareattributt først, som forklart under [Slik oppretter du vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I **Verdi**-feltet angir du vareattributtverdien, for eksempel "2010" for attributtet **Modellår**.
6. For vareattributter av typen **Alternativ** velger du oppslagsknappen i **Verdi**-feltet og velger en verdi for vareattributtet. Du kan også velge **Ny**-handlingen for å opprette en ny vareattributtverdi først, som forklart under [Slik oppretter du verdier for vareattributter av typen Alternativ](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Gjenta trinn 4 til 6 for alle vareattributter du vil tilordne varen.

## <a name="to-assign-item-attributes-to-item-categories"></a>Slik tilordner du vareattributter til varekategorier:
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varekategorier**, og velg deretter den relaterte koblingen.
2. På siden **Varekategorier** velger du varekategorien du vil tilordne vareattributter til, og deretter velger du handlingen **Rediger**.
3. På siden **Varekategorikort** på **Attributter**-hurtigfanen velger du handlingen **Ny**.
4. I **Attributt**-feltet velger du oppslagsknappen og velger et eksisterende vareattributt. Du kan også velge **Ny**-handlingen for å opprette et nytt vareattributt først, som forklart under [Slik oppretter du vareattributter](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. I **Standardverdi**-feltet velger du oppslagsknappen og velger en verdi for vareattributtet.
6. Gjenta trinn 4 og 5 for alle vareattributter du vil tilordne varekategorien.

> [!NOTE]  
>   Vareattributter for overordnede varekategorier arves til underordnede varekategorier. Dette angis av **Arvet fra**-feltet på **Attributter**-hurtigfanen. Hvis du vil ha mer informasjon, kan du se [Kategorisere varer](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Slik filtrerer du etter vareattributter:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. På siden **Varer** velger du handlingen **Filtrer etter attributter**.
3. På siden **Filtrer varer etter attributt** velger du oppslagsknappen i **Attributt**-feltet og et vareattributt.
4. I **Verdi**-feltet velger du oppslagsknappen og velger en eksisterende attributtverdi å filtrere varer etter.

    > [!NOTE]  
    >   Du kan bare velge verdier direkte for vareattributter som har faste verdier, for eksempel farge. For vareattributter med variable verdier, for eksempel bredde, må du angi verdien for vareattributtet ved først å velge en betingelse. Se trinn 5.
5. I **Verdi**-feltet for et variabelt vareattributt velger du oppslagsknappen.
6. I **Betingelse**-feltet på siden **Angi filterverdi** velger du rullegardinpilen og velger en betingelse.
7. I **Verdi**-feltet angir du en attributtverdi å filtrere varer etter.

    **Eksempel**: Hvis du vil filtrere på varer der materialbeskrivelsen begynner med "blå", fyller du ut feltene som følger: **Attributt**-feltet: Materialbeskrivelse, **Betingelse**-feltet: Begynner med, **Verdi**-felt: blå.
8. Velg **OK**.   

Varene på siden **Varer** er filtrert etter de angitte verdiene for vareattributt.

## <a name="see-also"></a>Se også
[Kategorisere varer](inventory-how-categorize-items.md)    
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
