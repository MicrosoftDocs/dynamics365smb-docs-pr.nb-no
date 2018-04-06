---
title: "Bokføre betalinger med SEPA Direct Debit | Microsoft-dokumentasjon"
description: "Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0031017c96172dca76b50542e52c6a437c01427a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Bokføre kvitteringer for SEPA Direct Debit
Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene. Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

Du kan bokføre kvittering direkte fra vinduet **Direct Debit\-oppkrevinger** eller vinduet **Poster for Direct Debit-oppkreving**. Du kan også overføre arbeidet til en annen bruker ved klargjøre de relaterte kladdelinjene.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Slik bokfører du en kvittering for direct debit- fra vinduet Direct Debit-samlinger  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Direct Debit-oppkrevinger**, og velg deretter den relaterte koblingen.  
2. Velg en linje for en direct debit-samling som er eksportert til en bankfil og behandlet av banken. Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
3. Velg handlingen **Bokfør kvitteringer**.  
4. I vinduet **Bokfør Direct Debit\-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit-oppkrevingsnr.**|Angi direct debit-samlingen du vil bokføre kvittering for.|  
    |**Finanskladdemal**|Angi hvilken finanskladdemal som skal brukes til bokføring av kvitteringen, for eksempel malen for innbetalinger.|  
    |**Finanskladdenavn**|Angi hvilken finanskladd som skal brukes til bokføring av kvitteringen.|  
    |**Opprett bare kladd**|Merk av for dette alternativet hvis du ikke vil bokføre kvitteringen når du velger **OK**. Kvitteringen blir klargjort i den angitte kladden, og blir ikke bokført før noen bokfører de aktuelle kladdelinjene.|  

5. Velg **OK**.  

## <a name="see-also"></a>Se også  
 [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)   
 [Salg](sales-manage-sales.md)

