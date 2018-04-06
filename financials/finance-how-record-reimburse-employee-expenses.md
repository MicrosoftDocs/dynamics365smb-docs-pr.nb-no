---
title: Registrere og refundere ansattes firmarelaterte utgifter | Microsoft-dokumentasjon
description: "Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c12561f4851cd75bdc4098e506c113e50d3bc3be
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="record-and-reimburse-employees-expenses"></a>Registrere og refundere ansattes utgifter
[!INCLUDE[d365fin](includes/d365fin_md.md)] støtter transaksjoner for en ansatt på lignende måte som for leverandører. Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.

> [!NOTE]  
> Ansattes transaksjoner kan bare bokføres i den lokale valutaen. Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.

Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte. Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.

## <a name="to-record-an-employees-expense"></a>Slik registrerer du utgifter for en ansatt
Du bokfører utgifter for de ansatte i vinduet **Finanskladd**.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Åpne den relevante finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.

    > [!TIP]  
    > Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden i vinduet **Finanskladder**. Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.
5. Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.

## <a name="to-reimburse-an-employee"></a>Slik refunderer du en ansatt
Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer i vinduet **Utbetalingskladd**.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.
2. Åpne den relevante kjørselen for utbetalingskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).
4. Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.
5. Velg handlingen **Bokfør** for å registrere refusjonen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Slik avstemmer du refusjoner med finansposter for ansatte
Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel vinduet **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan også utligne manuelt i vinduet **Ansattposter**. Hvis du vil ha mer informasjon, kan du se det relaterte emnet [Avstemme leverandørbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se også
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

