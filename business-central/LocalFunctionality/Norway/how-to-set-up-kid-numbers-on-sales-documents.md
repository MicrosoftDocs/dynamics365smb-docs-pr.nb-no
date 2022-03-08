---
title: Opprette KID-numre for salgsdokumenter
description: Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 767bebf146dae7b2318b4783a88df03a058605cd
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778510"
---
# <a name="set-up-kid-numbers-on-sales-documents"></a>Opprette KID-numre på salgsdokumenter
Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren. Du kan opprette KID-numre på salgsdokumenter for å identifisere bilags- og kundeinformasjon ved elektroniske banktransaksjoner.  

## <a name="to-set-up-kid-numbers-on-sales-documents"></a>Slik oppretter du KID-numre på salgsdokumenter  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.  
2.  I hurtigfanen **Dokumenter** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**KID-oppsett**|Angir et KID-nummerformat.|  
    |**Bilagsnr.lengde**|Angi hvor mange sifre som skal brukes i bilagsnummeret.|  
    |**Kundenr.lengde**|Angi hvor mange sifre som skal brukes i kundenummeret.|  
    |**Bruk KID på rentenota**|Velg å skrive ut KID-numre på rentenotaer. **Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.|  
    |**Bruk KID på purring**|Velg å skrive ut KID-numre på purringer. **Obs!**  Hvis dette alternativet er valgt, må du også velge formatet **Bilagstype + bilagsnr.** i feltet **KID-oppsett**.|

3.  Velg **OK**-knappen.  

## <a name="see-also"></a>Se også  
 [Elektroniske banktjenester i Norge](electronic-banking-in-norway.md) 
