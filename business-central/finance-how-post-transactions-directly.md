---
title: Registrere utgifter og inntekter direkte i Finans | Microsoft-dokumentasjon
description: Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i Financials, for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer på Finanskladd-siden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f0c1efcee7db0239efa739dd0ea8d8ce45e2dbd7
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183959"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a>Bokføre transaksjoner direkte i Finans

Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.  

Vanlig bruk av finanskladden er å bokføre ansattes utgifter av egne penger under forretningsaktiviteter for senere refusjon. Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti. Bokføring med en finanskladd oppretter alltid poster på finanskonti. Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe. Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

I motsetning til poster som bokføres med dokumenter, som krever en kreditnotaprosess, kan du foreta riktig tilbakeføring av poster som bokføres med finanskladden. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a>Bokføre en transaksjon direkte på en finanskonto

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Åpne den relevante finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Gjenta trinn 3 for alle separate transaksjoner du vil bokføre.

    > [!TIP]  
    > Hvis du for eksempel vil angi flere transaksjonslinjer ovenfor én motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**. Deretter fylles **Beløp**-feltet på motkontolinjen automatisk ut med verdien som kreves for å balansere transaksjonene.
5. Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.

## <a name="see-also"></a>Se også

[Arbeide med finanskladder](ui-work-general-journals.md)  
[Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md)  
[Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
