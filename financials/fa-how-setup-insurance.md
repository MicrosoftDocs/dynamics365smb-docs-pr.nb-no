---
title: Definere aktivaforsikring| Microsoft-dokumentasjon
description: Beskriver hvordan du setter opp systemet for forsikring av aktiva.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Definere aktivaforsikring
Hvis du vil behandle forsikringsdekning for aktiva, må du først sette opp noen generelle forsikringsopplysninger og et forsikringskort per polise.

## <a name="to-set-up-general-insurance-information"></a>Slik definerer du generelle forsikringsopplysninger
Hvis du vil bruke forsikringsfunksjoner i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi noen generelle forsikringsopplysninger.  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivaoppsett**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Slik definerer du forsikringstyper
Du kan gruppere forsikringspoliser i kategorier, for eksempel tyveriforsikring og brannforsikring. Forsikringstypene brukes på forsikringskortet.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forsikringstyper**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-cards"></a>Slik definerer du forsikringskort
Du kan samle opplysninger om hver enkelt forsikringspolise på forsikringskortet.  

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forsikring**, og deretter velger du den beslektede koblingen.  
2. Velg **Ny** for å opprette et nytt forsikringskort i **Forsikring**-vinduet.  
3. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-journal-templates"></a>Slik definerer du forsikringskladdemaler
[!INCLUDE[d365fin](includes/d365fin_md.md)] oppretter automatisk en forsikringskladdemal første gang du åpner **Forsikringskladd**-vinduet, men du kan definere flere kladdemaler. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forsikringskladdemaler**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-insurance-journal-batches"></a>Slik definerer du forsikringskladder
Du kan definere kladder i en forsikringskladdemal. Verdiene i kladden brukes som standardverdier hvis ikke feltene på kladdelinjene er fylt ut. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md)  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forsikringskladdemaler**, og deretter velger du den beslektede koblingen.  
2. Velg en forsikringskladdemal, og velg deretter **Kladder**-handlingen.
3. I vinduet **Forsikringskladder** fyller du ut feltene etter behov.

**Merk**: Tall har en bestemt funksjon i kladdenavn. Hvis en kladdemal eller et kladdenavn inneholder et tall, øker tallet automatisk med én hver gang du bokfører en kladd. Hvis for eksempel HH1 er angitt i feltet **Navn**, endres kladdenavnet til HH2 etter at kladden HH1 er bokført.

## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Anleggsmidler](fa-manage.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

