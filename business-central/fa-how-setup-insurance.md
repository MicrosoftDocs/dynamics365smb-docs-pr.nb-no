---
title: Definere aktivaforsikring | Microsoft-dokumentasjon
description: Du definerer et forsikringskort og generell informasjon om forsikringspolise for å behandle forsikringsdekning for aktiva.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5c9af3a076647380e2f6bed8ef7d0a55c3d8efe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749296"
---
# <a name="set-up-fixed-asset-insurance"></a>Definere aktivaforsikring
Hvis du vil behandle forsikringsdekning for aktiva, må du først sette opp noen generelle forsikringsopplysninger og et forsikringskort per polise.

## <a name="to-set-up-general-insurance-information"></a>Slik definerer du generelle forsikringsopplysninger
Hvis du vil bruke forsikringsfunksjoner i [!INCLUDE[prod_short](includes/prod_short.md)], må du angi noen generelle forsikringsopplysninger.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktivaoppsett**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Slik definerer du forsikringstyper
Du kan gruppere forsikringspoliser i kategorier, for eksempel tyveriforsikring og brannforsikring. Forsikringstypene brukes på forsikringskortet.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringstyper**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-cards"></a>Slik definerer du forsikringskort
Du kan samle opplysninger om hver enkelt forsikringspolise på forsikringskortet.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikring**, og velg deretter den relaterte koblingen.  
2. Velg **Ny** for å opprette et nytt forsikringskort på **Forsikring**-siden.  
3. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-journal-templates"></a>Slik definerer du forsikringskladdemaler
[!INCLUDE[prod_short](includes/prod_short.md)] oppretter automatisk en forsikringskladdemal første gang du åpner **Forsikringskladd**-siden, men du kan definere flere kladdemaler. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-journal-batches"></a>Slik definerer du forsikringskladder
Du kan definere kladder i en forsikringskladdemal. Verdiene i kladden brukes som standardverdier hvis ikke feltene på kladdelinjene er fylt ut. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md)  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forsikringskladdemaler**, og velg deretter den relaterte koblingen.  
2. Velg en forsikringskladdemal, og velg deretter **Kladder**-handlingen.
3. På siden **Forsikringskladder** fyller du ut feltene etter behov.

> [!NOTE]  
>   Tall har en bestemt funksjon i kladdenavn. Hvis en kladdemal eller et kladdenavn inneholder et tall, øker tallet automatisk med én hver gang du bokfører en kladd. Hvis for eksempel HH1 er angitt i feltet **Navn**, endres kladdenavnet til HH2 etter at kladden HH1 er bokført.

## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Aktiva](fa-manage.md)  
[Finans](finance.md)  
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]