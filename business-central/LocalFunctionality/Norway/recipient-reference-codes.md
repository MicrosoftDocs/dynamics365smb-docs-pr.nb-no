---
title: Referansekoder for mottaker
description: Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren. Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5d6e8d8ab985ded26a159a7e02713f26d298b3ec
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777897"
---
# <a name="recipient-reference-codes"></a>Referansekoder for mottaker
Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren. Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen. Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.  

Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder. Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut, **Betaling av faktura nr. 10000**.  

Mottakerreferansekodene blir beskrevet i tabellen nedenfor.  

|**Kode**|Description|  
|--------------|---------------------------------------|  
|**%1**|Bilagstypen. Enten faktura eller kreditnota.|  
|**%2**|Leverandørens fakturanummer.|  
|**%3**|Feltet **Vårt kontonr.** på siden **Leverandørkort**. Dette er vanligvis kundenummeret som brukes av leverandøren.|  
|**%4**|Faktura- eller kreditnotanummeret.|  
|**%5**|Beskrivelsen fra leverandørposten.|  
|**%6**|Det opprinnelige beløpet fra leverandørpostene. Beløpet vises med positivt fortegn.|  
|**%7**|Det resterende beløpet fra leverandørpostene. Beløpet vises med positivt fortegn.|  
|**%8**|Beløpet fra leverandørposten i lokal valuta. Beløpet vises med positivt fortegn.|  
|**%9**|Valutakoden fra leverandørposten.|  
|**%10**|Forfallsdatoen fra leverandørposten.|  
|**%11**|Kunde ID-nummeret fra leverandørposten.|  

## <a name="see-also"></a>Se også  
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)
