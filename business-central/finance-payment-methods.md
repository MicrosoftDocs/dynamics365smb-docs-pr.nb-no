---
title: Definere betalingsmåter | Microsoft-dokumentasjon
description: Du bruker betalingsmåter, for eksempel sjekk, bankoverføring, kontanter eller PayPal, til å definere hvordan salgs- og kjøpsfakturaer skal betales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 07/22/2019
ms.author: bholtorf
ms.openlocfilehash: 3f4741485a032dfef8b724ff4a18ed58c640778e
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796875"
---
# <a name="defining-payment-methods"></a>Definere betalingsmåter
Betalingsmåter definerer hvordan du foretrekker at kunder betaler deg, og hvordan du vil betale leverandørene. Metoden kan variere for hver kunde eller leverandør. Eksempler på typiske betalingsmåter er **bank**, **kontant**, **sjekk** eller **konto**.

Du kan knytte en betalingsmåte til kunder og leverandører slik at den samme metoden alltid brukes på salgs- og kjøpsdokumenter du oppretter for dem. Hvis det er nødvendig, kan du endre metoden på salgs- eller kjøpsdokumentet. Hvis du for eksempel vil betale en bestemt kjøpsfaktura kontant i stedet for med sjekk. Dette endrer ikke standard betalingsmåten som er knyttet til leverandøren.

Samme betalingsmåter brukes for salgs- og kjøpsdokumenter. For eksempel en _kontant_ betalingsmåte brukes både når du foretar betalinger og når du mottar dem. [!INCLUDE[d365fin](includes/d365fin_md.md)] vet at når du oppretter en salgsfaktura, forventer du å motta betaling, og motsatt for kjøpsfakturaer.

Kreditnotaer for returer er imidlertid unntak fordi penger flyter i motsatte retninger, fra deg til leverandøren og fra leverandøren til deg. En standard betalingsmåte tilordnes derfor ikke til kreditnotaer. Du kan imidlertid unngå dette hvis du har angitt betalingsbetingelser for kunden eller leverandøren. Selv om feltet **Beregn kontantrab. for kred.nota** ikke er beregnet for dette, hvis du velger å merke av i boksen på **Betalingsbetingelser**, legges en standard betalingsmåte til når du oppretter en kreditnota.

## <a name="to-set-up-a-payment-method"></a>Slik definerer du betalingsmåter
[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder noen betalingsmåter som bedrifter bruker ofte. Du kan imidlertid legge til så mange du trenger.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsmåter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Slik tilordner du en betalingsmåte til en kunde eller leverandør
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.
2. I **Betalingsmåte - kode**-feltet velger du metoden som skal brukes som standard for kunden eller leverandøren.

## <a name="see-also"></a>Se også
[Registrere nye kunder](sales-how-register-new-customers.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
