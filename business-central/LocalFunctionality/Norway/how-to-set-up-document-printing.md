---
title: Definere dokumentutskrift
description: I Business Central kan du skrive ut salgsrapportene som bruker de nødvendige girospesifikasjonene, ved bruk av forskjellige papirtyper og -skuffer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5586c8cbff247296483210fe4e772d49123b4202
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181025"
---
# <a name="set-up-document-printing"></a>Definere dokumentutskrift
I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du skrive ut salgsrapportene som bruker de nødvendige girospesifikasjonene, ved bruk av forskjellige papirtyper og -skuffer.  

Du må vurdere hvordan skriveren og skriverdriveren tolker denne informasjonen når du bruker skuffnumre og papirkilder for norske salgsdokumenter. Du må kanskje angi andre skuffnumre for din spesifikke skriver.  

> [!NOTE]  
>  KID-informasjon skrives også ut der giroopplysningene skrives ut.  

Følgende dokumenter krever en utskrevet giro:  

- Fakturaer  
- Kreditnotaer  
- Rentenotaer  
- Purringer  

Den norske versjonen av [!INCLUDE[d365fin](../../includes/d365fin_md.md)] inneholder følgende sett med salgsdokumenter.  

|**Valg**|Description|  
|-------------|---------------------------------------|  
|1|Standard [!INCLUDE[d365fin](../../includes/d365fin_md.md)]-dokumenter. Ingen giroinformasjon skrives ut.|  
|2|Giroen skrives ut på hver side. Den siste siden skriver ut girosummen.|  

## <a name="to-set-up-paper-trays"></a>Slik definerer du papirskuffer:  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Skrivervalg**, og velg deretter den relaterte koblingen.  
2.  Velg rapporten.  
3.  Velg handlingen **Salgsdok.arkskuff - oppsett**.  
4.  Velg en papirkilde i **Første side - papirkilde**-feltet.  
5.  Feltet **Første side - skuffnr.** viser automatisk den valgte papirkilden. Du kan også angi et skuffnummer manuelt.  

    > [!IMPORTANT]  
    >  Ikke alle skrivere har samme papirkildenavn. Du kan angi et nummer i feltet **Skuffnr.**. Nummeret kan tilsvare en papirkilde. Du finner nummeret som en bestemt skriver bruker, i den tekniske dokumentasjonen for skriveren.  

    Feltet **Andre sider** og **Giroside** defineres på samme måte.  

6.  Velg **OK**.  

## <a name="see-also"></a>Se også  
  [Norsk giro og OCR-B-skrift](norwegian-giro-and-ocr-b-font.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)
