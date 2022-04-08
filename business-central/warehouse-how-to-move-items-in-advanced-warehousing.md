---
title: Flytte varer i avanserte lageroppsett
description: Dette emnet forklarer hvordan en senioransatt kan ordne flytting av varer i avanserte lageroppsett – gjelder lokasjoner med lagerstyring.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7351
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 02a96b48049207d2272c62b008148c000cf676e0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520581"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Flytte varer i avanserte lageroppsett
I avanserte lageroppsett, det vil si lokasjoner med lagerstyring, utføres lagerflyttinger mellom hyller av en overordnet ansatt som klargjør lagerflyttinger i flytteforslaget, og deretter oppretter lagerflyttingene som ansatte på lageret utfører.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Flytte varer med lagerflytteforslaget
**Flytteforslag**-siden har to funksjoner som kan hjelpe til med automatisk utfylling på linjene. Den første er funksjonen **Beregn etterfylling av hylle**. Denne funksjonen bruker hylleprioriteringene til å foreslå etterfylling til høyt prioriterte hyller fra hyller med lav prioritering. Den andre er funksjonen **Hent hylleinnhold**, som fyller ut forslagslinjene med hele hylleinnholdet i hyllen eller hyllene du angir.

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Flytteforslag**, og velg deretter den relaterte koblingen.  
2.  Skriv inn aktuelle opplysninger om lagerflyttingen på forslagslinjene.  
3. Velg handlingen **Opprett flytting** for å opprette et lagerflyttingsdokument som deretter kan registreres når lagerflyttingen er ferdig.  

### <a name="to-register-the-warehouse-movement"></a>Slik registrerer du lagerflyttingen  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Flyttinger**, og velg deretter den relaterte koblingen.  
2.  Åpne lagerflyttingen du vil behandle.  
3.  På linjer av handlingstype **Plasser** angir du hvor, hvilke, og når den aktuelle varen skal flyttes ved å redigere feltene **Sonekode**, **Hyllekode**, **Ant. som skal håndt.** eller **Forfallsdato**.  

    Hvis lageret er definert slik at hyllekodene følger strukturen i lageret, kan du ta flere varer fra påfølgende hyller med store enheter, og plassere dem i hyller for forhåndsplukking, som også kan være plassert nær hverandre.  
4.  På linjer av handlingstype **Hent** angir du i feltet **Ant. som skal håndt.** et delantall av hylleinnholdet som du vil flytte. Alle andre felt på linjer for handlingstypen **Hent** er skrivebeskyttet.  
5.  Hvis du vil flytte alle foreslåtte antall som er angitt i **Antall**-feltet, velger du handlingen **Autoutfyll ant som skal håndt**.  
6. Velg handlingen **Registrer**.  

> [!NOTE]  
>  Hvis lokasjonen bruker lagerstyring, kan du ikke manuelt flytte varer til eller fra hyller av hylletypen MOTTA, fordi varer som er i slike hyller må registreres som plassert før de blir en del av det tilgjengelige lageret.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>Slik registrerer du vareflytting som allerede har funnet sted  
Hvis lokasjonen bruker lagerstyring og du trenger å flytte varer til andre hyller uten at det finnes en eksisterende plassering, plukking eller flytting, kan du registrere den riktige plasseringen av varene i lageret ved hjelp av **Lagerreklassifiseringskladd**.

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerreklassifiseringskladd** og velg den relaterte koblingen.  
2.  Fyll ut feltene **Varenr.**, **Fra sone-kode**, **Fra hylle-kode**, **Til sone-kode**, **Til hylle-kode**.  
3.  Velg handlingen **Registrer**.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]