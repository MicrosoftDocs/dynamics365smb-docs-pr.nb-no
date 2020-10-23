---
title: Korrigere eller annullere en bokført salgsfaktura | Microsoft-dokumentasjon
description: Beskriver hvordan du korrigerer, angrer eller annullerer en bokført salgsfaktura og utligner en salgskreditnota.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3803ce840569d1b1668db64879e68395ee6f3a65
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926300"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigere eller annullere ubetalte salgsfakturaer

Du kan korrigere eller annullere en bokført salgsfaktura. Dette er nyttig hvis du gjør en feil eller hvis kunden ber om en endring tidlig.

> [!NOTE]  
> Etter at en bokført salgsfaktura er delvis eller helt betalt, kan du ikke korrigere eller annullere den fra den bokførte salgsfakturaen. I stedet må du manuelt opprette en salgskreditnota for å annullere salget og refundere kunden, eventuelt behandlet med en ordreretur. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

På siden **Bokført salgsfaktura** kan du velge handlingen **Korriger** eller **Avbryt** for å utføre handlingene som er beskrevet i tabellen nedenfor.

| Handling | Beskrivelse |
| --- | --- |
| **Korriger** |Den bokførte salgsfakturaen er annullert. Det opprettes en ny salgsfaktura med samme informasjon. Du kan foreta korrigeringen og deretter fortsette salgsprosessen. Nye salgsfakturaen har et annet nummer enn den opprinnelige salgsfakturaen. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt. |
| **Avbryt** |Den bokførte salgsfakturaen er annullert. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt. |

Når du korrigerer eller annullerer en bokført salgsfaktura, utlignes den korrigerende salgskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige salgsfakturaen ble bokført. Dette tilbakefører den bokførte salgsfakturaen i finanspostene og etterlater den korrigerende bokførte salgskreditnotaen for revisjonssporingen.  

> [!TIP]
> Hvis du har bokført en forskuddsfaktura for en salgsfaktura som du deretter retter opp eller kansellerer, må du også korrigere eller kansellere forskuddet. Hvis du vil ha mer informasjon, kan du se [Korrigere forskudd](finance-how-to-correct-prepayments.md).

## <a name="to-correct-a-posted-sales-invoice"></a>Slik korrigerer du en bokført salgsfaktura:

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil rette.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte salgsfakturaen fordi den allerede er korrigert eller annullert.
3. På siden **Bokført salgsfaktura** velger du handlingen **Korriger**.  
4. Det opprettes en ny salgsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.
5. Velg handlingen **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

## <a name="to-cancel-a-posted-sales-invoice"></a>Slik annullerer du en bokført salgsfaktura:

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil avbryte.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte salgsfakturaen fordi den allerede er annullert eller korrigert.
3. På siden **Bokført salgsfaktura** velger du handlingen **Avbryt**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

### <a name="partial-invoice-posting-also-supported"></a>Delvis fakturabokføring støttes også

Hvis annulleringen er knyttet til en delvis fakturabokføring, oppdateres den opprinnelige ordrelinjen for å gjenspeile det annullerte fakturerte antallet. Feltene **Ant. som skal fakt.** og **Ant. fakturert** på den tilknyttede ordrelinjen tilbakestilles til verdiene før den delvise bokføringen.

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
