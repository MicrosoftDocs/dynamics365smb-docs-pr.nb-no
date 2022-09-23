---
title: Kombinere mottak på én faktura
description: Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen Kombinere mottak.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 136, 145, 146, 9308
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: dc1fa2e308ce0920815a5766d4e077a2eb0ce62a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534538"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Kombinere mottak på én faktura

Hvis du vil fakturere mer enn et kjøp om gangen, kan du velge flere mottakslinjer på kjøpsfakturaen.  

Før du kan opprette et kombinert kjøpsmottak, må du bokføre mer enn ett mottak for den samme leverandøren i samme valuta. Du må med andre ord ha fylt ut minst to bestillinger og bokført disse som mottatt, men ikke fakturert.  

Når kjøpsmottak kombineres i en faktura og bokføres, opprettes det en bokført kjøpsfaktura for fakturert(e) linje(r). **Fakturert (antall)**-feltet på den opprinnelige bestillingen eller rammebestillingen oppdateres basert på det fakturerte antallet. Dette opprinnelige kjøpsdokumentet slettes imidlertid ikke, selv om det er fullstendig mottatt og fakturert, og derfor må du slette kjøpsdokumentet.  

> [!NOTE]
> Den resulterende kjøpsfakturaen kan senere ikke rettes eller kanselleres. Hvis du vil endre en kjøpsfaktura som er opprettet på denne måten, må du bruke kjøpskreditnotaer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>Slik kombinerer du mottak

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).  
3. På hurtigfanen **Linjer** velger du handlingen **Hent mottakslinjer**.  
4. Velg flere mottakslinjer du vil inkludere på fakturaen.  

    Hvis feil mottakslinje ble merket eller du vil begynne på nytt, kan du ganske enkelt slette linjene på kjøpsfakturaen og deretter bruke funksjonen **Hent mottakslinje** på nytt.  
5. Velg handlingen **Bokfør** for å bokføre fakturaen.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Fjerne åpne bestillinger etter kombinert mottaksbokføring

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Slett fakturerte bestillinger**, og velg den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Velg **OK**.  

Du kan også slette de individuelle ordrene manuelt.

Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel bestillinger.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
