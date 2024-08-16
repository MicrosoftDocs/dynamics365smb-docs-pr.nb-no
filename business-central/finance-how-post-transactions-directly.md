---
title: Registrere utgifter og inntekter direkte i Finans
description: Du kan opprette transaksjoner på Finanskladd-siden for forretningsaktiviteter som ikke involverer et dokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'direct posting, general ledger'
ms.search.form: '39, 251'
ms.date: 08/06/2024
ms.service: dynamics-365-business-central
---

# Bokfør transaksjoner direkte i finans

Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti.  

Vanlig bruk av finanskladden er å bokføre ansattes utgifter under forretningsaktiviteter for refusjon. Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

Finanskladder bokfører finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti. Bokføring med en finanskladd oppretter poster på finanskonti. Poster opprettes selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe. Du kan tilpasse din versjon av en finanskladd ved å definere en kladd eller mal. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

Poster du bokfører med dokumenter, krever en kreditnotaprosess. Du kan imidlertid reversere poster du bokfører med finanskladden. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).

## Bokføre en transaksjon direkte på en finanskonto

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Åpne finanskladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov på en ny kladdelinje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Gjenta trinn 3 for alle transaksjoner du vil bokføre.

    > [!TIP]  
    > Hvis du for eksempel vil angi flere transaksjonslinjer før en motkontolinje for én bankkonto, merker du av for **Foreslå motkontobeløp** på linjen for kladden på siden **Finanskladder**. **Beløp**-feltet på motkontolinjen fylles automatisk ut med verdien som kreves for å balansere transaksjonene.
5. Velg handlingen **Bokfør** for å registrere transaksjonene på bestemte finanskonti.

## Se også

[Arbeide med finanskladder](ui-work-general-journals.md)    
[Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md)    
[Reversere kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md)    
[Finans](finance.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]