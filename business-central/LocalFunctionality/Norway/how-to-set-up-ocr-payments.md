---
title: 'Konfigurer OCR-betalinger [NO]'
description: Du kan behandle elektroniske betalinger fra kunder i henhold til en forhåndsdefinert betalings-ID i den norske versjonen. Dette blir ofte referert til som en OCR-betaling (optisk tegngjenkjenning).
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 15000100
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-ocr-payments"></a>Opprette OCR-betalinger
Du kan behandle elektroniske betalinger fra kunder i henhold til en forhåndsdefinert betalings-ID. Dette blir ofte referert til som en OCR-betaling (optisk tegngjenkjenning). Betalings-ID-en brukes med elektroniske betalingstransaksjoner. Kunder kan vise til denne ID-en når de foretar betalinger. Betalings-IDen brukes også til å identifisere importerte betalingstransaksjoner og anvende importerte betalingsdata automatisk.  

## <a name="to-set-up-ocr-payments"></a>Slik oppretter du OCR-betalinger

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **OCR-oppsett** og velg den relaterte koblingen.  
2.  I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Format**|Velg et OCR-betalingsfilformat. Formater inkluderer **BBS** og **Datadialog**.|  
    |**Filnavn**|Skriv inn hele banen til OCR-betalingsfilen.|  
    |**Slett returfil**|Velg dette alternativet for å gi filen nytt navn etter import og forhindre at filen importeres mer enn én gang.|  

3.  I hurtigfanen **Finans** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Motkontotype**|Velg en motkontotype. Motkontotyper inkluderer **Finanskonto** og **Bankkonto**.|  
    |**Motkontonr.**|Velg et motkontonummer.|  
    |**Maks. differanse**|Angi høyeste differanseverdi. Hvis differansen i en betaling er mindre enn eller lik den angitte verdien, bokføres differansebeløpet automatisk. Hvis ikke, blir beløpet ikke bokført automatisk. I begge tilfeller vises en advarsel i innbetalingskladden ved import av OCR-girobetalinger.|  
    |**Kontonr. differanse**|Angi avvikkontonummeret det skal bokføres på.|  
    |**Kladdemalnavn**|Velg navnet på kladdemalen som skal motta de importerte OCR-girobetalingene.|  
    |**Kladdenavn**|Velg navnet på kladden som skal motta de importerte OCR-girobetalingene.<br /><br /> Hvis feltene **Kladdemalnavn** og **Kladdenavn** er tomme, kan du importere OCR-girobetalinger til en hvilken som helst kladd. Ellers må du importere OCR-girobetalingene til den angitte kladden.|  

4.  Velg **OK**.  

> [!NOTE]  
>  OCR-betalinger kan bare bokføres i innbetalingskladder når feltet **Avstem per bilag** er tomt i tabellen **Finanskladdemal**. Hvis du vil ha mer informasjon, kan du se Finanskladdemal.  

## <a name="see-also"></a>Se også
 [Elektroniske banktjenester i Norge](electronic-banking-in-norway.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)   
 [Importere og bokføre OCR-betalinger](how-to-import-and-post-ocr-payments.md)   
 [Skrive ut rapporten OCR-kladd - test](how-to-print-the-ocr-journal-test-report.md)   
 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
