---
title: Bokføre betalinger med SEPA Direct Debit | Microsoft-dokumentasjon
description: Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 6c646575ba803358aa00309ce02742423bcc7de8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "930758"
---
# <a name="post-sepa-direct-debit-payment-receipts"></a>Bokføre kvitteringer for SEPA Direct Debit
Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene. Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  

Du kan bokføre kvittering direkte fra siden **Direct Debit\-oppkrevinger** eller siden **Poster for Direct Debit-oppkreving**. Du kan også overføre arbeidet til en annen bruker ved klargjøre de relaterte kladdelinjene.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a>Slik bokfører du en kvittering for direct debit fra siden Direct Debit-samlinger  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Direct Debit-oppkrevinger**, og velg deretter den relaterte koblingen.  
2. Velg en linje for en direct debit-samling som er eksportert til en bankfil og behandlet av banken. Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
3. Velg handlingen **Bokfør kvitteringer**.  
4. På siden **Bokfør Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit-oppkrevingsnr.**|Angi direct debit-samlingen du vil bokføre kvittering for.|  
    |**Finanskladdemal**|Angi hvilken finanskladdemal som skal brukes til bokføring av kvitteringen, for eksempel malen for innbetalinger.|  
    |**Finanskladdenavn**|Angi hvilken finanskladd som skal brukes til bokføring av kvitteringen.|  
    |**Opprett bare kladd**|Merk av for dette alternativet hvis du ikke vil bokføre kvitteringen når du velger **OK**. Kvitteringen blir klargjort i den angitte kladden, og blir ikke bokført før noen bokfører de aktuelle kladdelinjene.|  

5. Velg **OK**.  

## <a name="see-also"></a>Se også  
 [Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)   
 [Salg](sales-manage-sales.md)
