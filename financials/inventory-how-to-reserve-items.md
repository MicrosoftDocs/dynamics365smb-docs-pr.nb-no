---
title: Reservere varer| Microsoft-dokumentasjon
description: "Du kan reservere varer for ordrer, bestillinger og produksjonsordrer. Du kan reservere varer på lager eller inngående på åpne dokumentlinjer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b03209b5681c264f7d788d3d731d32b60f1709b6
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reserve-items"></a>Reservere varer
Du kan reservere varer for ordrer, bestillinger, serviceordrer, monteringsordrer og produksjonsordrer. Du kan reservere varer på lager eller inngående på åpne dokument- eller kladdelinjer. Du utfører arbeidet i **Reservasjon**-vinduet.

Hver linje i **Reservasjon**-vinduet, som du åpner for å reservere varer, viser informasjon om én type linje (salg, kjøp, kladd) eller lagerpost. Linjene beskriver hvor mange varer som kan reserveres fra hver linje- eller posttype.

## <a name="to-reserve-items-for-sales"></a>Slik reserverer du varer for salg
Fremgangsmåten nedenfor beskriver hvordan du reserverer varer fra en ordre. Fremgangsmåten er lignende for kjøps- service- og monteringsordrer.  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  I en ordre, i hurtigfanen **Linjer** velger du **Reserver**-handlingen. **Reservasjon**-vinduet åpnes.  
3. Velg linjen som inneholder varene du vil reservere.  
4. Velg en av de følgende handlingene.  

    |**Funksjon**|**Beskrivelse**|
    |------------------|---------------------|  
    |**Auto-reserver**|Hvis du vil reservere varer automatisk i **Reservasjon**-vinduet.|  
    |**Reserver fra gjeldende linje**|Hvis du vil reservere varene i dokumentet på den valgte linjen.|  
    |**Kanseller reservasjon fra gjeldende linje**|Hvis du vil kansellere reservasjonen av varene i dokumentet på den valgte linjen.|

> [!NOTE]  
>  Hvis det finnes varesporingslinjer for ordren, blir du ledet gjennom spesielle trinn i reservasjonssystemet: Hvis du vil ha mer informasjon, kan du se delen "Reservere et spesifikt serie- eller partinummer".  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Slik reserverer du varer for produksjonsordrelinjer  
Du kan reservere varer for produksjonsordrer. Du må skille mellom produksjonsordrelinjer, som betyr den overordnede varen, og produksjonsordrekomponenter.

I fremgangsmåten nedenfor brukes det en fast planlagt produksjonsordre.   
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Fast planlagte prod.ordre**, og velg deretter den relaterte koblingen.  
2. Åpne den fast planlagte produksjonsordren du vil reservere overordnede varer for.  
3. Velg den aktuelle produksjonsordrelinjen.  
4. I hurtigfanen **Linjer**, velg **Reserver**.
5. I vinduet **Reservasjon**, velg linjen **Salgslinje, ordre**, og velg deretter handlingen **Reserver fra gjeldende linje**.  

Antallet du angav på den fast planlagte produksjonsordrelinjen, er nå reservert.

## <a name="to-reserve-items-for-production-order-components"></a>Slik reserverer du varer for produksjonsordrekomponenter  
Du kan reservere varer for produksjonsordrer. Du må skille mellom produksjonsordrelinjer, som betyr den overordnede varen, og produksjonsordrekomponenter.

I fremgangsmåten nedenfor brukes det en fast planlagt produksjonsordre.    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Fast planlagte prod.ordre**, og velg deretter den relaterte koblingen.  
2. Åpne den fast planlagte produksjonsordren du vil reservere komponentvarer for.  
3. Velg den aktuelle produksjonsordrelinjen.  
4. På hurtigfanen **Linjer** velger du **Linje**, og deretter **Komponenter**.  
5. Velg den aktuelle komponentlinjen.  
6. I hurtigfanen **Linjer**, velg **Reserver**.  
7. I vinduet **Reservasjon**, velg en linje, og velg deretter handlingen **Reserver fra gjeldende linje**.  

Antallet du angav på den fast planlagte produksjonskomponentlinjen, er nå reservert.

## <a name="to-change-a-reservation"></a>Slik endrer du en reservasjon  
Noen ganger kan det hende du vil endre en varereservasjon.   
1. Fra dokumentlinjen som du har reservert fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. I vinduet **Reservasjon** velger du handlingen **Reservasjonsposter**.
3. I vinduet **Reservasjonsposter** oppdaterer du **Antall**-feltet på linjen du vil endre.
4. Bekreft meldingen som vises, ved å velge **OK**-knappen.

## <a name="to-cancel-a-reservation"></a>Slik kansellerer du en reservasjon  
Noen ganger kan det hende du vil kansellere en varereservasjon.   
1. Fra dokumentlinjen som du ønsker å avbryte en reservasjon fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. I vinduet **Reservasjon** velger du handlingen **Reservasjonsposter**.  
3.  I vinduet **Reservasjonposter** velger du handlingen **Kanseller reservasjon**.  
4.  Bekreft meldingen som vises, ved å velge **OK**-knappen.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Reservere et spesifikt serie- eller partinummer  
Fra utgående dokumenter for varesporede varer, for eksempel ordrer eller produksjonskomponentlister, kan du reservere bestemte serie- eller partinumre. Dette kan for eksempel være relevant hvis du trenger produksjonskomponenter fra et bestemt parti for å sikre konsekvens med tidligere produksjonspartier, eller fordi en kunde har bedt om et bestemt serienummer. Hvis du vil ha mer informasjon, se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).

Dette kalles en spesifikk reservasjon, fordi du reserverer fra antallet av varen X som tilhører partiet X. Hvis du bare reserverer fra antall av varen X, er dette en normal, ikke-spesifikk reservasjon. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md).

Følgende fremgangsmåte er basert på en ordre.    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ordrelinje for en varesporet vare.  
3. Tilordne serie- eller partinumre til ordrelinjen. Hvis du vil ha mer informasjon, se [Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md).
4. Velg handlingen **Reserver** på ordrelinjen.  
5. Velg **Ja**-knappen for å reservere bestemte serie- eller partinumre.  
6. Velg serie- og partinummerkombinasjonen du nettopp har tilordnet, i vinduet **Varesporingsoversikt**.  
7. Velg **OK**-knappen for å åpne vinduet **Reservasjon**, som bare viser det angitte varesporingsnummeret. Hvis det finnes ikke-spesifikke reservasjoner for noen av varesporingsnumrene du har angitt for denne linjen, får du beskjed om antallet som allerede er reservert.  
8. Velg **Auto-reserver** eller **Reserver fra gjeldende linje** for å opprette reservasjonen for de spesifikke varesporingsnumrene.

## <a name="see-also"></a>Se også
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

