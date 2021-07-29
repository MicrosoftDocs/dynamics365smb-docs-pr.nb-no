---
title: Spore varesporede varer
description: Du kan vise hvor en varesporet vare er brukt, inkludert hvordan og når den ble mottatt, produsert eller returnert med funksjonene Varesporing og Finn enheter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: a511cc2496d32f2feee7c684d073395db2ef8c5e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445629"
---
# <a name="trace-item-tracked-items"></a>Spore varesporede varer
Du kan vise hvor en varesporet vare er brukt, inkludert hvordan og når den ble mottatt eller produsert, overført, solgt, forbrukt eller returnert. Du kan også finne alle gjeldende forekomster av et bestemt serie- eller partinummer i databasen. Dette gjør du ved hjelp av funksjonene Varesporing og [Søk etter poster](ui-find-entries.md).  

Disse funksjonene kan være spesielt nyttige i kvalitetskontroll når du må finne ut hvilke kunder som mottok produkter fra et bestemt partinummer, eller når du må finne ut hvilket parti en defekt komponent kom fra.  

 På siden **Varesporing** kan du spore fremover og bakover i en sekvens med bokførte lagertransaksjoner for serie- eller partinummeret.  

 Du kan ikke se transaksjonssekvensen på siden **Søk etter poster**, men du kan se alle postene for serie- eller partinummeret, både bokførte poster og åpne poster.  

 De to funksjonene kan brukes i kombinasjon ved å overføre et sporet serie- eller partinummer på siden **Søk etter poster** hvis du vil fullføre et fullstendig sporingsscenario. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Slik sporer du varesporede varer  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporing** og velg den relaterte koblingen.  
2.  Angi de bestemte varenumrene eller et filter på varenumrene du vil spore, i filterfeltene øverst på siden.  
3.  Velg om du også vil vise hvor komponentene for varen kommer fra, i feltet **Vis komponenter**. Alternativene i dette feltet er som følger.  

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Nei**|Velg dette alternativet hvis du ikke vil vise noen komponenter.|  
    |**Bare varesporet**|Velg dette alternativet hvis du bare vil vise komponenter som har parti- eller serienumre.|  
    |**Alle**|Velg dette alternativet hvis du vil vise alle komponentene.|  

4.  Velg metoden du vil bruke til å spore varen, i feltet **Sporingsmetode**. Du kan velge mellom følgende alternativer  

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Forbruk->opprinnelse**|Denne metoden sporer varen fra der den ble brukt, til der den kom fra. Hvis en produsert vare for eksempel ble solgt til en kunde, vises dette på siden **Varesporing** med følgeseddellinjen først, som du deretter kan utvide for å vise hvilken produksjonsordre den kom fra.|  
    |**Opprinnelse->forbruk**|Denne metoden sporer varen fra der den kom inn på lageret, til der den ble brukt. Hvis en produsert vare ble solgt til en kunde, vises dette på siden **Varesporing** med den ferdige produksjonsordren først, som du deretter kan utvide for å vise følgeseddellinjer der varen ble brukt.|  

5.  Velg **Spor** for å kjøre sporingen.  

> [!NOTE]  
>  Hvis du har mottatt samme parti i flere transaksjoner, vises kanskje ikke alle transaksjonene på siden **Varesporing**. Det vises bare utlignede transaksjoner.  

> [!NOTE]  
>  Hvis ytterligere transaksjonshistorikk under en varesporingslinje allerede er sporet av en annen linje ovenfor, er det merket av for **Allerede sporet**. For en enklere visning vises ikke slike underliggende linjer.  
>   
>  Når du skal søke etter varesporingslinjer der transaksjonsloggen allerede er sporet, velger du knappen **Gå til allerede sporet**. Den aktuelle varesporingslinjen velges, og alle underliggende linjer utvides.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Slik søker du etter varesporede varer med Søk etter poster:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Finn enheter**, og velg deretter den relaterte koblingen.  
2. Velg **Handlinger** > **Finn etter** > **Finn etter varereferanse**.
3. I feltene **Serienr.** og **Partinr.** angir du varesporingsnumrene du vil spore.  
4. Velg **Søk** for å finne alle forekomster av serie- eller partinummeret i databasen.  

## <a name="see-also"></a>Se også

[Lager](inventory-manage-inventory.md)  
[Arbeide med serie-, parti- og pakkenumre](inventory-how-work-item-tracking.md)  
[Designdetaljer: Varesporing](design-details-item-tracking.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Søk etter poster](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]