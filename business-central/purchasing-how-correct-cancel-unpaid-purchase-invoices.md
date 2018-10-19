---
title: "Endre eller annullere ubetalte kjøpsfakturaer | Microsoft-dokumentasjon"
description: "Forklarer hvordan du korrigerer, annullerer eller angrer en bokført kjøpsfaktura og oppretter en kjøpskreditnota automatisk."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 2ed3520b3724f9703fca128a2d20c28183795a93
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Korrigere eller annullere ubetalte kjøpsfakturaer
Du kan korrigere eller annullere en bokført kjøpsfaktura. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen.

Hvis du allerede har betalt for produkter på den bokførte kjøpsfakturaen, kan du ikke rette eller avbryte den fra den bokførte kjøpsfakturaen. I stedet må du manuelt opprette en kjøpskreditnota for å tilbakeføre kjøpet, eventuelt behandlet med en bestillingsretur. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

I vinduet **Bokført kjøpsfaktura** kan du velge knappen **Korriger** eller **Annuller**. Når du korrigerer eller annullerer en bokført kjøpsfaktura, utlignes den korrigerende kjøpskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige kjøpsfakturaen ble bokført. Dette tilbakefører den bokførte kjøpsfakturaen i finanspostene og etterlater den korrigerende bokførte kjøpskreditnotaen for revisjonssporingen. Nedenfor beskrives bruk av **Korriger** og **Annuller**.

## <a name="to-correct-a-posted-purchase-invoice"></a>Slik korrigerer du en bokført kjøpsfaktura:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil korrigere.  

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte kjøpsfakturaen fordi den allerede er korrigert eller annullert.
3. I vinduet **Bokført kjøpsfaktura** velger du **Korriger**.

    Det opprettes en ny kjøpsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md). Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Slik annullerer du en bokført kjøpsfaktura:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil avbryte.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte kjøpsfakturaen fordi den allerede er annullert eller korrigert.
3. I vinduet **Bokført kjøpsfaktura** velger du **Annuller**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen. Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

