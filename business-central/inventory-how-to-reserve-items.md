---
title: Reserver varer
description: Du kan reservere varer for ordrer, bestillinger og produksjonsordrer. Du kan reservere også varer på lager eller inngående på åpne dokumentlinjer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 498, 497
ms.date: 08/11/2022
ms.author: edupont
ms.openlocfilehash: d727242c772d1eba2959747c2fcd151a7a330009
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361667"
---
# <a name="reserve-items"></a>Reservere varer

Du kan reservere varer for ordrer, bestillinger, serviceordrer, monteringsordrer, overføringsordrer og produksjonsordrer. Du kan også reservere varer på lager eller inngående på åpne dokument- eller kladdelinjer. Dette gjør du på siden **Reservasjon**.

Hver linje du åpner for å reservere varer på **Reservasjon**-siden, viser informasjon om én type linje (salg, kjøp eller kladd) eller lagerpost. Linjene beskriver hvor mange varer som kan reserveres fra hver linje- eller posttype.

## <a name="reserve-items-for-sales"></a>Reserver varer for salg

Fremgangsmåten nedenfor beskriver hvordan du reserverer varer fra en ordre. Fremgangsmåten er lignende for kjøps-, service-, overførings- og monteringsordrer.
  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Lukk ordren.
3. I hurtigfanen **Linjer**, velg **Reserver**. **Reservasjon**-siden åpnes.  
4. Velg linjen som inneholder varene du vil reservere.  
5. Velg en av de følgende handlingene.  

    |**Funksjon**|**Beskrivelse**|
    |------------------|---------------------|  
    |**Auto-reserver**|Hvis du vil reservere varer automatisk på **Reservasjon**-siden.|  
    |**Reserver fra gjeldende linje**|Hvis du vil reservere varene i dokumentet på den valgte linjen.|  
    |**Kanseller reservasjon fra gjeldende linje**|Hvis du vil kansellere reservasjonen av varene i dokumentet på linjen du valgte.|

> [!NOTE]  
> Hvis det finnes varesporingslinjer for ordren, blir du ledet gjennom spesielle trinn i reservasjonssystemet: Finn ut mer i delen [Reserver et spesifikt serie- eller partinummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line"></a>Reserver varer for produksjonsordrelinjer

Du kan reservere varer for produksjonsordrer. Du må skille mellom produksjonsordrelinjer, som betyr den overordnede varen, og produksjonsordrekomponenter.

I fremgangsmåten nedenfor brukes det en fast planlagt produksjonsordre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagt prod.ordre** og velg den relaterte koblingen.  
2. Åpne den fast planlagte produksjonsordren du vil reservere overordnede varer for.  
3. Velg den aktuelle produksjonsordrelinjen.  
4. I hurtigfanen **Linjer**, velg **Reserver**.
5. På **Reservasjon**-siden velger du linjen **Salgslinje, ordre**, og velger deretter handlingen **Reserver fra gjeldende linje**.  

Antallet du angav på den fast planlagte produksjonsordrelinjen, er nå reservert.

## <a name="reserve-items-for-production-order-components"></a>Reserver varer for produksjonsordrekomponenter

Du kan reservere varer for produksjonsordrer. Du må skille mellom produksjonsordrelinjer, som betyr den overordnede varen, og produksjonsordrekomponenter.

I fremgangsmåten nedenfor brukes det en fast planlagt produksjonsordre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagt prod.ordre** og velg den relaterte koblingen.  
2. Åpne den fast planlagte produksjonsordren du vil reservere komponentvarer for.  
3. Velg den aktuelle produksjonsordrelinjen.  
4. På hurtigfanen **Linjer** velger du **Linje**, og deretter **Komponenter**.  
5. Velg den aktuelle komponentlinjen.  
6. I hurtigfanen **Linjer**, velg **Reserver**.  
7. På **Reservasjon**-siden velger en linje, og velger deretter handlingen **Reserver fra gjeldende linje**.  

Antallet du angav på den fast planlagte produksjonskomponentlinjen, er nå reservert.

## <a name="change-a-reservation"></a>Endre en reservasjon

Noen ganger kan det hende du vil endre en varereservasjon.

1. Fra dokumentlinjen som du gjorde reservasjonen fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. På **Reservasjon**-siden velger du handlingen **Reservasjonsposter**.
3. På siden **Reservasjonsposter** oppdaterer du **Antall**-feltet på linjen du vil endre.
4. Bekreft meldingen som vises, ved å velge **OK**-knappen.

## <a name="cancel-a-reservation"></a>Kanseller en reservasjon

Noen ganger kan det hende du vil kansellere en varereservasjon.

1. Fra dokumentlinjen som du ønsker å avbryte en reservasjon fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. På **Reservasjon**-siden velger du handlingen **Reservasjonsposter**.  
3. På **Reservasjon**-siden velger du handlingen **Kanseller reservasjon**.  
4. Bekreft meldingen som vises, ved å velge **Ja**-knappen.  

## <a name="reserve-a-specific-serial-or-lot-number"></a>Reserver et spesifikt serie- eller partinummer

Fra utgående dokumenter for varesporede varer, for eksempel ordrer eller produksjonskomponentlister, kan du reservere bestemte serie- eller partinumre. Dette kan for eksempel være relevant hvis du trenger produksjonskomponenter fra et bestemt parti for å sikre konsekvens med tidligere produksjonspartier, eller fordi en kunde har bedt om et bestemt serienummer. Finn ut mer under [Arbeid med serie- og partinumre](inventory-how-work-item-tracking.md).

Denne fremgangsmåten kalles en spesifikk reservasjon, fordi du reserverer fra antallet av varen X som tilhører partiet X. Hvis du derimot reserverer bare fra antall av varen X, er dette en normal, ikke-spesifikk reservasjon. Finn ut mer under [Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md).

Følgende fremgangsmåte er basert på en ordre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ordrelinje for en varesporet vare.  
3. Tilordne serie- eller partinumre til ordrelinjen. Finn ut mer under [Arbeid med serie- og partinumre](inventory-how-work-item-tracking.md).
4. Velg handlingen **Reserver** på ordrelinjen.  
5. Velg **Ja**-knappen for å reservere bestemte serie- eller partinumre.  
6. Velg serie- og partinummerkombinasjonen du har tildelt, på siden **Varesporingsoversikt**.  
7. Velg **OK**-knappen for å åpne siden **Reservasjon**, som bare viser det angitte varesporingsnummeret. Hvis det finnes ikke-spesifikke reservasjoner for noen av varesporingsnumrene du har angitt for denne linjen, får du beskjed om antallet som allerede er reservert.  
8. Velg **Auto-reserver** eller **Reserver fra gjeldende linje** for å opprette reservasjonen for de spesifikke varesporingsnumrene.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/manage-outbound-serial-lot-numbers/)

## <a name="see-also"></a>Se også

[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
