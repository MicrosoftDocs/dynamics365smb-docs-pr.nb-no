---
title: Importere og bokføre OCR-betalinger
description: Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre noen forberedelser.
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
ms.author: sgroespe
ms.openlocfilehash: d6b8ce498d4eadc430790c7c37a31c89b8756c48
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181031"
---
# <a name="import-and-post-ocr-payments"></a>Importere og bokføre OCR-betalinger
Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre følgende forberedelser:  

- Opprette en innbetalingskladdemal for å balansere OCR-transaksjoner i henhold til bilagsnummeret i stedet for bilagstypen.  
- Lese inn og bokføre OCR-betalingsfiler i en innbetalingskladd.  

## <a name="to-import-ocr-payments"></a>Slik leser du inn OCR-betalinger  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.  
2.  Velg en kladd i feltet **Bunkenavn**.  

    > [!NOTE]  
    >  OCR-betalinger kan bare bokføres i en innbetalingskladd som ikke benytter en motkonto i feltet **Motkontonr.** på linjen Innbetalingskladd.  

3.  Velg handlingen **Importer betalinger**.  
4.  På siden **OCR-betaling - BBS** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Filenavn**|Skriv inn hele banen til importfilen.|  

5.  Velg **OK** for å lese inn betalingsfilen i kladden.  

## <a name="to-post-ocr-payments"></a>Slik bokfører du OCR-betalinger  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Innbetalingskladder**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Bokfør**.  

OCR-betalingsfilene bokføres i innbetalingskladden.  

## <a name="see-also"></a>Se også  
 [Elektroniske banktjenester i Norge](electronic-banking-in-norway.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)   
 [Opprette OCR-betalinger](how-to-set-up-ocr-payments.md)   
 [Arbeide med finanskladder](../../ui-work-general-journals.md)   
 [Skrive ut rapporten OCR-kladd - test](how-to-print-the-ocr-journal-test-report.md)
