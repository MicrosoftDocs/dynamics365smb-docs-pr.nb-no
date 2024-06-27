---
title: Konfigurer betalingsmåter
description: 'Du bruker betalingsmåter, for eksempel sjekk, bankoverføring, kontanter eller PayPal, til å definere hvordan salgs- og kjøpsfakturaer skal betales.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.search.form: '427,'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-payment-methods"></a>Konfigurer betalingsmåter

Betalingsmåter definerer hvordan du foretrekker at kunder betaler deg, og hvordan du vil betale leverandørene. Metoden kan variere for hver kunde eller leverandør. Eksempler på typiske betalingsmåter er **bank**, **kontant**, **sjekk** eller **konto**.

Du kan knytte en betalingsmåte til kunder og leverandører slik at den samme metoden alltid brukes på salgs- og kjøpsdokumenter du oppretter for dem. Hvis det er nødvendig, kan du endre metoden på salgs- eller kjøpsdokumentet. Hvis du for eksempel vil betale en bestemt kjøpsfaktura kontant i stedet for med sjekk. Dette endrer ikke standard betalingsmåten som er knyttet til leverandøren.

Samme betalingsmåter brukes for salgs- og kjøpsdokumenter. For eksempel en _kontant_ betalingsmåte brukes både når du foretar betalinger og når du mottar dem. [!INCLUDE[prod_short](includes/prod_short.md)] vet at når du oppretter en salgsfaktura, forventer du å motta betaling, og motsatt for kjøpsfakturaer.

Kreditnotaer for returer er imidlertid unntak fordi penger flyter i motsatte retninger, fra deg til leverandøren og fra leverandøren til deg. En standard betalingsmåte tilordnes derfor ikke til kreditnotaer. Det finnes imidlertid en løsning. Du kan angi betalingsbetingelser for kunden eller leverandøren. Selv om feltet **Beregn kontantrab. for kred.nota** ikke er beregnet for denne løsningen, hvis du velger å merke av i boksen på **Betalingsbetingelser**, legges en standard betalingsmåte til når du oppretter en kreditnota. <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a>Slik definerer du betalingsmåter

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder noen betalingsmåter som bedrifter bruker ofte. Du kan imidlertid legge til så mange du trenger.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsmåter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Du kan eventuelt legge til betalingsbetingelser til betalingsmåten. Hvis du vil ha mer informasjon, kan du se [Definer betalingsbetingelser](finance-payment-terms.md).  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Slik tilordner du en betalingsmåte til en kunde eller leverandør

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunde** eller **Leverandør** og velg den relaterte koblingen.
2. I **Betalingsmåte - kode**-feltet velger du metoden som skal brukes som standard for kunden eller leverandøren.

## <a name="see-also"></a>Se også

[Registrer nye kunder](sales-how-register-new-customers.md)  
[Konfigurer betalingsbetingelser](finance-payment-terms.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
