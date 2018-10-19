---
title: Slik kombinerer du mottak | Microsoft-dokumentasjon
description: "Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen Kombinere mottak."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="combine-receipts-on-a-single-invoice"></a>Kombinere mottak på én faktura
Hvis du vil fakturere mer enn et kjøp om gangen, kan du bruke funksjonen **Kombinere mottak**.  

Før du kan opprette et kombinert kjøpsmottak, må du bokføre mer enn ett mottak for den samme leverandøren i samme valuta. Du må med andre ord ha fylt ut minst to bestillinger og bokført disse som mottatt, men ikke fakturert.  

Når kjøpsmottak kombineres i en faktura og bokføres, opprettes det en bokført kjøpsfaktura for fakturert(e) linje(r). **Fakturert (antall)**-feltet på den opprinnelige bestillingen eller rammebestillingen oppdateres basert på det fakturerte antallet. Dette opprinnelige kjøpsdokumentet slettes imidlertid ikke, selv om det er fullstendig mottatt og fakturert, og derfor må du slette kjøpsdokumentet.  

## <a name="to-combine-receipts"></a>Slik kombinerer du mottak  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).  
3. På hurtigfanen **Linjer** velger du handlingen **Hent mottakslinjer**.  
4. Velg flere mottakslinjer du vil inkludere på fakturaen.  

    Hvis feil mottakslinje ble merket eller du vil begynne på nytt, kan du ganske enkelt slette linjene på kjøpsfakturaen og deretter bruke funksjonen **Hent mottakslinje** på nytt.  
5. Velg handlingen **Bokfør** for å bokføre fakturaen.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Fjerne åpne bestillinger etter kombinert mottaksbokføring  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett fakturerte bestillinger**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Velg **OK**.  

Du kan også slette de individuelle ordrene manuelt.

Gjenta trinn 1 til 3 for eventuelle andre berørte dokumenter, for eksempel bestillinger.

## <a name="see-also"></a>Se også  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

