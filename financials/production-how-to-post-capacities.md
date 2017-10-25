---
title: "Bokføre kapasiteter | Microsoft-dokumentasjon"
description: "I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4b0bb12f86a8984ca4a87d679bc22a0e34e51c88
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-capacities"></a>Bokføre kapasiteter
I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.  

## <a name="to-post-capacities"></a>Slik bokfører du kapasiteter  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kapasitetskladder**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene **Bokføringsdato** og **Bilagsnr.**.  
3.  I feltet **Type** angir du kapasitetstypen, enten **Produksjonsressurs** eller **Arbeidssenter**, du bokfører.  
4.  I feltet **Nr.** angir du nummeret på produksjonsressursen eller arbeidssenteret.  
5.  Skriv inn relevante opplysninger i de andre feltene, for eksempel **Starttidspunkt**, **Sluttidspunkt**, **Antall** og **Vrak**.  
6.  Velg handlingen **Bokfør** for å bokføre kapasitetene.  

## <a name="to-view-work-center-ledger-entries"></a>Slik viser du arbeidssenterposter:  
I vinduet **Arbeidssenterkort** og **Maskinsenterkort** kan du vise bokførte kapasiteter som et resultat av ferdige produksjonsordrer.    
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.  
2.  Åpne det aktuelle **Arbeidssenter**-kortet fra listen, og velg handlingen **Kapasitetsposter**.  

**Kapasitetsposter**-vinduet viser de bokførte postene fra arbeidssenteret i den rekkefølgen de ble bokført.   

## <a name="see-also"></a>Se også  
[Produksjon](production-manage-manufacturing.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

