---
title: Opprette KID-numre for salgsdokumenter
description: Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren.
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
ms.openlocfilehash: 1f309906c04f9a165451677f01ea4d9ae45bd587
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301226"
---
# <a name="set-up-kid-numbers-on-sales-documents"></a>Opprette KID-numre på salgsdokumenter
Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren. Du kan opprette KID-numre på salgsdokumenter for å identifisere bilags- og kundeinformasjon ved elektroniske banktransaksjoner.  

## <a name="to-set-up-kid-numbers-on-sales-documents"></a>Slik oppretter du KID-numre på salgsdokumenter  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.  
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
 [Norske salgsdokumenter](norwegian-sales-documents.md)
