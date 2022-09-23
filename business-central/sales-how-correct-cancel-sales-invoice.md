---
title: Korrigere eller annullere en bokført salgsfaktura
description: Dette emnet beskriver hvordan du korrigerer, angrer eller annullerer en bokført salgsfaktura og utligner en salgskreditnota.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 95cf36a9f48b3452bcc28e049c12ae310c58e2ee
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531030"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigere eller annullere ubetalte salgsfakturaer

Du kan korrigere eller annullere en ubetalt bokført salgsfaktura, forutsatt at den ikke er fullstendig levert. Dette er nyttig hvis du gjør en feil, eller hvis kunden ber om en endring før leveringen er fullført. I alle andre scenarioer anbefales det at du oppretter en korrigert salgskreditnota direkte. Hvis du vil ha mer informasjon, kan [Opprette en ny salgskreditnota fra en bokført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Etter at en bokført salgsfaktura er delvis eller helt betalt, kan du ikke korrigere eller annullere den fra den bokførte salgsfakturaen. I stedet må du manuelt opprette en salgskreditnota for å annullere salget og refundere kunden, eventuelt behandlet med en ordreretur. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Forskjellen mellom å annullere eller korrigere en bokført salgsfaktura som ikke er betalt eller levert, er beskrevet i tabellen nedenfor.

| Handling | Beskrivelse |
| --- | --- |
| **Avbryt** |Den bokførte salgsfakturaen er annullert. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for **Annullert** og **Betalt**. |
| **Korriger** |Den bokførte salgsfakturaen er annullert. Det opprettes en ny salgsfaktura med de samme opplysningene, med mindre den bokførte ordren ble bokført fra en ordre. Vi foreslår i så fall at du annullerer den bokførte salgsfakturaen i stedet, og deretter foretar korrigeringen og fortsetter salgsprosessen fra den opprinnelige ordren. <br/><br/>Nye salgsfakturaen har et annet nummer enn den opprinnelige salgsfakturaen. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for **Annullert** og **Betalt**. |

Når du korrigerer eller annullerer en bokført salgsfaktura, utlignes den korrigerende salgskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige salgsfakturaen ble bokført. Dette tilbakefører den bokførte salgsfakturaen i finanspostene og etterlater den korrigerende bokførte salgskreditnotaen for revisjonssporingen.  

> [!TIP]
> Hvis du har bokført en forskuddsfaktura for en salgsfaktura som du deretter retter opp eller kansellerer, må du også korrigere eller kansellere forskuddet. Hvis du vil ha mer informasjon, kan du se [Korrigere forskudd](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Slik annullerer du en bokført salgsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil avbryte.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte salgsfakturaen fordi den allerede er annullert eller korrigert.
3. På siden **Bokført salgsfaktura** velger du handlingen **Avbryt**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

### <a name="partial-invoice-posting-also-supported"></a>Delvis fakturabokføring støttes også

Hvis annulleringen er knyttet til en delvis fakturabokføring, oppdateres den opprinnelige ordrelinjen for å gjenspeile det annullerte fakturerte antallet. Feltene **Ant. som skal fakt.** og **Ant. fakturert** på den tilknyttede ordrelinjen tilbakestilles til verdiene før den delvise bokføringen.

## <a name="to-correct-a-posted-sales-invoice"></a>Slik korrigerer du en bokført salgsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil rette.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte salgsfakturaen fordi den allerede er korrigert eller annullert.
3. På siden **Bokført salgsfaktura** velger du handlingen **Korriger**.  

    > [!NOTE]
    > Hvis salgsfakturaen ble bokført fra en ordre, anbefaler vi at du *annullerer* denne salgsfakturaen og deretter håndterer korrigeringen på nytt fra den opprinnelige ordren. Hvis den opprinnelige ordren er slettet, for eksempel hvis den er fullstendig levert, kan du opprette en ny ordre ved hjelp av handlingen **Kopier dokument**. Hvis du vil ha mer informasjon, kan [Opprette en salgskreditnota ved å kopiere en bokført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Det opprettes en ny salgsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.
5. Velg handlingen **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
