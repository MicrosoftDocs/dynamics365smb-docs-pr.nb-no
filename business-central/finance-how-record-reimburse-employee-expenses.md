---
title: Registrer og refunder ansattes firmarelaterte utgifter
description: Bokfør de ansattes utgifter med finanskladden til kontoen for den ansatte, og bokfør senere en betaling til den ansattes bankkonto for å refundere for den firmarelaterte utgiften.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184402"
---
# <a name="record-and-reimburse-employees-expenses"></a>Registrere og refundere ansattes utgifter

[!INCLUDE[prod_short](includes/prod_short.md)] støtter transaksjoner for ansatte på lignende måte som for leverandører. Derfor finnes det bokføringsgrupper for de ansatte for å sikre at de ansattes finansposter bokføres til de relevante kontiene i Finans.

> [!NOTE]  
> Ansattes transaksjoner kan bare bokføres i den lokale valutaen. Refusjonsutbetalinger til de ansatte støtter ikke rabatter og betalingstoleranser.

Hvis ansatte bruker egne penger under forretningsaktiviteter, kan du bokføre utgifter til kontoen for den ansatte. Deretter kan du refundere den ansatte ved å foreta en betaling til den ansattes bankkonto, på samme måte som når du betaler leverandører.  

> [!TIP]
> Denne artikkelen forklarer hvordan du registrerer utgiftene i bøkene og hvordan du refunderer den ansatte. Organisasjonen kan ha en portal eller app der ansatte kan sende reiseregninger.

[!INCLUDE [prod_short](includes/prod_short.md)] er fleksibel nok til å dekke mange forskjellige rutiner. De nøyaktige kontonumrene som skal brukes, avhenger av organisasjonens konfigurasjon og prosesser.  

## <a name="to-record-an-employees-expense"></a>Slik registrerer du utgifter for en ansatt

Du bokfører utgifter for de ansatte på siden **Finanskladd**.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.  
2. Åpne den relevante finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Gjenta trinn 3 for alle utgifter som er påløpt for den ansatte.

    > [!TIP]  
    > Hvis du vil angi flere utgiftslinjer ovenfor én motkontolinje for den ansattes bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**. Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere utgiftene.
5. Velg **Bokfør**-handlingen for å registrere utgifter på kontoen for den ansatte.

## <a name="to-reimburse-an-employee"></a>Slik refunderer du en ansatt

Du refunderer ansatte ved bokføring av betalinger til deres bankkontoer på siden **Utbetalingskladd**.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.
2. Åpne den relevante kjørselen for utbetalingskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).
4. Du kan også velge handlingen **Betalingsforslag - ansatt** for å automatisk sette inn kladdelinjer for ventende refusjoner for ansatte.
5. Velg handlingen **Bokfør** for å registrere refusjonen.  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a>Slik avstemmer du refusjoner med finansposter for ansatte

Du utligner ansattes utbetalinger til de relaterte åpne finanspostene for de ansatte på samme måte som for leverandørbetalinger, for eksempel på siden **Betalingsavstemmingskladd**, basert på de relaterte bankkontoutdragspostene. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md). Du kan også utligne manuelt på siden **Ansattposter**. Hvis du vil ha mer informasjon, kan du se relatert [Avstemme leverandørbetalinger med utbetalingskladd eller fra leverandørposter](payables-how-apply-purchase-transactions-manually.md).  

## <a name="see-also"></a>Se også

[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]