---
title: 'Importer og bokfør OCR-betalinger [NO]'
description: 'Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre noen forberedelser i den norske versjonen av Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15000100, 255'
ms.date: 12/06/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Importer og bokfør OCR-betalinger
Før du kan motta OCR-betalinger (optisk tegngjenkjenning), må du gjøre følgende forberedelser:  

- Opprette en innbetalingskladdemal for å balansere OCR-transaksjoner i henhold til bilagsnummeret i stedet for bilagstypen.  
- Lese inn og bokføre OCR-betalingsfiler i en innbetalingskladd.  

## Slik leser du inn OCR-betalinger  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Innbetalingskladder** og velg den relaterte koblingen.  
2.  Velg en kladd i feltet **Bunkenavn**.  

    > [!NOTE]  
    >  OCR-betalinger kan bare bokføres i en innbetalingskladd som ikke benytter en motkonto i feltet **Motkontonr.** på linjen Innbetalingskladd.  

3.  Velg handlingen **Importer betalinger**.  
4.  På siden **OCR-betaling - BBS** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Filnavn**|Skriv inn hele banen til importfilen.|  

5.  Velg **OK** for å lese inn betalingsfilen i kladden.  

## Slik bokfører du OCR-betalinger  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Innbetalingskladder** og velg den relaterte koblingen.  
2.  Velg handlingen **Bokfør**.  

OCR-betalingsfilene bokføres i innbetalingskladden.  

## Se også  
 [Elektroniske banktjenester i Norge](electronic-banking-in-norway.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)   
 [Opprette OCR-betalinger](how-to-set-up-ocr-payments.md)   
 [Arbeide med finanskladder](../../ui-work-general-journals.md)   
 [Skrive ut rapporten OCR-kladd - test](how-to-print-the-ocr-journal-test-report.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]