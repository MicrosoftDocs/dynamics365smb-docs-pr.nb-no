---
title: "Korrigere eller annullere en bokført salgsfaktura | Microsoft-dokumentasjon"
description: "Beskriver hvordan du korrigerer, angrer eller annullerer en bokført salgsfaktura og utligner en salgskreditnota."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e8e5a4762564d036ac8c0e7bdaf9e13b448d37f4
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Korrigere eller annullere ubetalte salgsfakturaer
Du kan korrigere eller annullere en bokført salgsfaktura. Dette er nyttig hvis du gjør en feil eller hvis kunden ber om en endring tidlig.

> [!NOTE]  
>   Etter at en bokført salgsfaktura er delvis eller helt betalt, kan du ikke korrigere eller annullere den fra den bokførte salgsfakturaen. I stedet må du manuelt opprette en salgskreditnota for å annullere salget og refundere kunden, eventuelt behandlet med en ordreretur. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

I vinduet **Bokført salgsfaktura** kan du velge handlingen **Korriger** eller **Avbryt** for å utføre handlingene som er beskrevet i tabellen nedenfor.

| Handling | Beskrivelse |
| --- | --- |
| **Korriger** |Den bokførte salgsfakturaen er annullert. Det opprettes en ny salgsfaktura med samme informasjon. Du kan foreta korrigeringen og deretter fortsette salgsprosessen. Nye salgsfakturaen har et annet nummer enn den opprinnelige salgsfakturaen. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt. |
| **Avbryt** |Den bokførte salgsfakturaen er annullert. En korrigerende salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. På den første bokførte salgsfakturaen er det merket av for Annullert og Betalt. |

Når du korrigerer eller annullerer en bokført salgsfaktura, utlignes den korrigerende salgskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige salgsfakturaen ble bokført. Dette tilbakefører den bokførte salgsfakturaen i finanspostene og etterlater den korrigerende bokførte salgskreditnotaen for revisjonssporingen.

## <a name="to-correct-a-posted-sales-invoice"></a>Slik korrigerer du en bokført salgsfaktura:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil rette.

    > [!NOTE]  
>   Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte salgsfakturaen fordi den allerede er korrigert eller annullert.
3. I vinduet **Bokført salgsfaktura** velger du handlingen **Korriger**.  
4. Det opprettes en ny salgsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen.
5. Velg handlingen **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

## <a name="to-cancel-a-posted-sales-invoice"></a>Slik annullerer du en bokført salgsfaktura:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte salgsfakturaen du vil avbryte.

    > [!NOTE]  
>   Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte salgsfakturaen fordi den allerede er annullert eller korrigert.
3. I vinduet **Bokført salgsfaktura** velger du handlingen **Annuller**.

    En salgskreditnota opprettes og bokføres automatisk for å annullere den første bokførte salgsfakturaen. Feltet **Kansellert** i den første bokførte salgsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte salgskreditnotaen som annullerer den første bokførte salgsfakturaen.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

