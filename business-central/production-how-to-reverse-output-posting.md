---
title: Tilbakeføre avgangsbokføring | Microsoft-dokumentasjon
description: Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7ff9557d088bec5fb76e4bf673ad4afd244e08bf
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313159"
---
# <a name="reverse-output-posting"></a>Tilbakeføre avgangsbokføring
Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.  

## <a name="to-reverse-an-output-posting"></a>Tilbakeføre en avgangsbokføring  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen. Velg kjørselen.  
2. Fyll ut feltene etter behov. Hvis du vil ha mer informasjon, se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md).
3.  Velg den tilknyttede vareposten i **Utligningspost**-feltet. Dermed tilbakeføres kapasitets- og varepostene.  
4. Bokfør tilbakeføringen ved bokføring av kladden.  

Postene i ferdigmeldingskladden bokføres i vareposten som en oppjustering.  

## <a name="see-also"></a>Se også  
 [Produksjon](production-manage-manufacturing.md)    
 [Definere produksjon](production-configure-production-processes.md)  
 [Planlegging](production-planning.md)      
 [Lager](inventory-manage-inventory.md)  
 [Innkjøp](purchasing-manage-purchasing.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
