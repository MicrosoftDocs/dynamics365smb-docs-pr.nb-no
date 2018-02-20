---
title: Registrere utgifter og inntekter direkte i Finans | Microsoft-dokumentasjon
description: "Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i Financials, for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer i Finanskladd-vinduet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6925c2ddb45973e060c7694a83bc03c7fbabcf41
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Bokføre transaksjoner direkte i Finans
De fleste finanstransaksjoner bokføres i Finans via dedikerte forretningsdokumenter, for eksempel kjøpsfakturaer eller ordrer. Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer i **Finanskladd**-vinduet.

Vanlig bruk av finanskladden er å bokføre ansattes utgifter av egne penger under forretningsaktiviteter for senere refusjon. Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti. Bokføring med en finanskladd oppretter alltid poster på finanskonti. Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe. Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

I motsetning til poster som bokføres med dokumenter, som krever en kreditnotaprosess, kan du foreta riktig tilbakeføring av poster som bokføres med finanskladden. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Bokføre en transaksjon direkte på en finanskonto
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Åpne den relevante finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. Gjenta trinn 3 for alle separate transaksjoner du vil bokføre.

    > [!TIP]  
    > Hvis du for eksempel vil angi flere transaksjonslinjer ovenfor én motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden i vinduet **Finanskladder**. Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere transaksjonene.
5. Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.

## <a name="see-also"></a>Se også
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md)  
[Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

