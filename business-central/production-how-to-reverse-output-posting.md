---
title: Tilbakeføre avgangsbokføring
description: Det hender at avgangsbokføring må tilbakeføres. Dette emnet beskriver fremgangsmåten for tilbakeføring av avgangsbokføring.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: ed45facfc64dda670d0e1e4d7dd9b396b4c11fae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132788"
---
# <a name="reverse-output-posting"></a>Tilbakeføre avgangsbokføring

Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.  

## <a name="to-reverse-an-output-posting"></a>Tilbakeføre en avgangsbokføring

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ferdigmeldingskladd** og velg den relaterte koblingen. Velg kjørselen.  
2. Fyll ut feltene etter behov. Hvis du vil ha mer informasjon, se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md).
3. Velg den tilknyttede vareposten i **Utligningspost**-feltet. Dermed tilbakeføres kapasitets- og varepostene.  
4. Bokfør tilbakeføringen ved bokføring av kladden.  

Postene i ferdigmeldingskladden bokføres i vareposten som en oppjustering.  

## <a name="see-also"></a>Se også

 [Produksjon](production-manage-manufacturing.md) [Definere produksjon](production-configure-production-processes.md)  
 [Planlegging](production-planning.md)  
 [Lager](inventory-manage-inventory.md)  
 [Innkjøp](purchasing-manage-purchasing.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]