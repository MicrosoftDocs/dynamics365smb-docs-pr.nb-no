---
title: "Korrigere eller annullere ubetalte kjøpsfakturaer| Microsoft-dokumentasjon"
description: "Korrigere eller annullere ubetalte kjøpsfakturaer"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-purchase-invoices"></a>Korrigere eller annullere ubetalte kjøpsfakturaer
Du kan korrigere eller annullere en bokført kjøpsfaktura. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen.

Hvis du allerede har betalt for produkter på den bokførte kjøpsfakturaen, kan du ikke rette eller avbryte den fra den bokførte kjøpsfakturaen. I stedet må du manuelt opprette en kjøpskreditnota for å reversere innkjøpet. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

I vinduet **Bokført kjøpsfaktura** kan du velge knappen **Korriger** eller **Annuller**. Når du korrigerer eller annullerer en bokført kjøpsfaktura, utlignes den korrigerende kjøpskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige kjøpsfakturaen ble bokført. Dette tilbakefører den bokførte kjøpsfakturaen i finanspostene og etterlater den korrigerende bokførte kjøpskreditnotaen for revisjonssporingen. Nedenfor beskrives bruk av **Korriger** og **Annuller**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Slik korrigerer du en bokført kjøpsfaktura:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokførte kjøpsfakturaer**, og deretter velger du den beslektede koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil korrigere.  

    **Merk**: Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte kjøpsfakturaen fordi den allerede er korrigert eller annullert.
3. I vinduet **Bokført kjøpsfaktura** velger du **Korriger**.

    Det opprettes en ny kjøpsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md). Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Slik annullerer du en bokført kjøpsfaktura:
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokførte kjøpsfakturaer**, og deretter velger du den beslektede koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil avbryte.

    **Merk**: Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte kjøpsfakturaen fordi den allerede er annullert eller korrigert.
3. I vinduet **Bokført kjøpsfaktura** velger du **Annuller**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen. Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

