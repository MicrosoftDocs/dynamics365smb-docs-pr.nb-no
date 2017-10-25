---
title: "Tilbakeføre avgangsbokføring | Microsoft-dokumentasjon"
description: "Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre."
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
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a>Tilbakeføre avgangsbokføring
Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.  

## <a name="to-reverse-an-output-posting"></a>Tilbakeføre en avgangsbokføring  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen. Velg kjørselen.  
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

