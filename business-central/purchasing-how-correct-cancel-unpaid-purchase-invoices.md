---
title: Endre eller annullere ubetalte kjøpsfakturaer (inneholder video)
description: 'Forklarer hvordan du korrigerer, annullerer eller angrer en bokført kjøpsfaktura og oppretter en kjøpskreditnota automatisk.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Korriger eller annuller ubetalte kjøpsfakturaer

Du kan korrigere eller annullere en bokført kjøpsfaktura. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen.

Hvis du allerede har betalt for produkter på den bokførte kjøpsfakturaen, kan du ikke rette eller avbryte den fra den bokførte kjøpsfakturaen. I stedet må du manuelt opprette en kjøpskreditnota for å tilbakeføre kjøpet, eventuelt behandlet med en bestillingsretur. Det samme gjelder hvis du vil endre en bokført kjøpsfaktura som er basert på kombinerte kjøpsmottak. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

På siden **Bokført kjøpsfaktura** kan du velge knappen **Korriger** eller **Annuller**. Når du korrigerer eller annullerer en bokført kjøpsfaktura, utlignes den korrigerende kjøpskreditnotaen mot alle finans- og lagerposter som ble opprettet da den opprinnelige kjøpsfakturaen ble bokført. Dette tilbakefører den bokførte kjøpsfakturaen i finanspostene og etterlater den korrigerende bokførte kjøpskreditnotaen for revisjonssporingen. Videoen beskriver bruken av **Korriger** og **Annuller**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a>Slik korrigerer du en bokført kjøpsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil korrigere.  

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke korrigere den bokførte kjøpsfakturaen fordi den allerede er korrigert eller annullert.
3. På siden **Bokført kjøpsfaktura** velger du **Korriger**.

    Det opprettes en ny kjøpsfaktura med den samme informasjonen, der du kan foreta korrigeringen. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md). Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Slik annullerer du en bokført kjøpsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg den bokførte kjøpsfakturaen du vil avbryte.

    > [!NOTE]  
    >   Hvis det er merket av for **Annullert**, kan du ikke annullere den bokførte kjøpsfakturaen fordi den allerede er annullert eller korrigert.
3. På siden **Bokført kjøpsfaktura** velger du **Annuller**.

    En kjøpskreditnota opprettes og bokføres automatisk for å annullere den første bokførte kjøpsfakturaen. Feltet **Kansellert** i den første bokførte kjøpsfakturaen endres til **Ja**.
4. Velg **Vis korrigerende kreditnota** for å vise den bokførte kjøpskreditnotaen som annullerer den første bokførte kjøpsfakturaen.

### <a name="partial-invoice-posting-also-supported"></a>Delvis fakturabokføring støttes også

Hvis annulleringen er knyttet til en delvis fakturabokføring, oppdateres den opprinnelige bestillingslinjen for å gjenspeile det annullerte fakturerte antallet. Feltene **Ant. som skal fakt.** og **Antall fakturert** på den tilknyttede bestillingslinjen tilbakestilles til verdiene før den delvise bokføringen.

## <a name="see-also"></a>Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Registrer kjøp](purchasing-how-record-purchases.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
