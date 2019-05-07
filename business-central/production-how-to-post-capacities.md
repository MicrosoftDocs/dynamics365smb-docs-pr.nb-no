---
title: Bokføre kapasiteter | Microsoft-dokumentasjon
description: I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 58005b8b4d401f5eab8a934d7b00b610b64b4281
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "928303"
---
# <a name="post-capacities"></a>Bokføre kapasiteter
I kapasitetskladden bokfører du brukte kapasiteter som ikke er tilordnet produksjonsordren. Vedlikeholdsarbeid må for eksempel tilordnes kapasitet, men ikke en produksjonsordre.  

## <a name="to-post-capacities"></a>Slik bokfører du kapasiteter  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kapasitetskladder**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene **Bokføringsdato** og **Bilagsnr.**.  
3.  I feltet **Type** angir du kapasitetstypen, enten **Produksjonsressurs** eller **Arbeidssenter**, du bokfører.  
4.  I feltet **Nr.** angir du nummeret på produksjonsressursen eller arbeidssenteret.  
5.  Skriv inn relevante opplysninger i de andre feltene, for eksempel **Starttidspunkt**, **Sluttidspunkt**, **Antall** og **Vrak**.  
6.  Velg handlingen **Bokfør** for å bokføre kapasitetene.  

## <a name="to-view-work-center-ledger-entries"></a>Slik viser du arbeidssenterposter:  
På sidene **Arbeidssenterkort** og **Maskinsenterkort** kan du vise bokførte kapasiteter som et resultat av ferdige produksjonsordrer.    
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidssentre**, og velg deretter den relaterte koblingen.  
2.  Åpne det aktuelle **Arbeidssenter**-kortet fra listen, og velg handlingen **Kapasitetsposter**.  

**Kapasitetsposter**-siden viser de bokførte postene fra arbeidssenteret i den rekkefølgen de ble bokført.   

## <a name="see-also"></a>Se også  
[Produksjon](production-manage-manufacturing.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
