---
title: Konfigurer varesporing med serie-, parti- og pakkenumre
description: Konfigurer varesporing med serienumre, partinumre og pakkenumre
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/31/2021
ms.author: edupont
ms.openlocfilehash: c298903d62da4cfd346a46ff1978ab91644fb13f
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533271"
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Konfigurer varesporing med serie-, parti- og pakkenumre

Holde oversikt over lagervarer selv i komplekse lagerkonfigurasjoner med numre som er spesifikke for hver vare, enten som et individuelt objekt, for eksempel et parti, eller som en pakke. Ved hjelp av varesporing kan du spore varer på tvers av interne lagerflyttinger, og utgående og inngående dokumenter.

Varer med serie- og partinumre kan spores både bakover og fremover i forsyningskjeden. Dette er nyttig for generell kvalitetskontroll og tilbakekalling av proukter. Hvis du vil ha mer informasjon, kan du se [Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> I lanseringsbølge 1 for 2021 og nyere aktiverer du oppdatering av funksjonen *Bruk sporing etter pakkenummer i reservasjons- og sporingssystem* hvis du vil arbeide med pakkenumre samt serie-og partinumre. Hvis du vil ha mer informasjon, kan du se [Aktivere kommende funksjoner på forhånd](admin-feature-management.md). Når funksjonen er aktivert, kan du tilordne pakkenumre til utgående og inngående dokumenter, på samme måte som du kan arbeide med partinumre.  

## <a name="numbers-and-item-tracking"></a>Numre og varesporing

Som en del av lagerprosessene, kan du pakke lageret i pakker, bokser, beholdere og så videre. Men for å holde orden på varene, tilordner du unike tall som identifikasjon. Det kan for eksempel være at du produserer og selger en stol som har varenummer *1900-S*. Hver stol har et serienummer, *1001*, men du kan også bunte fire stoler i et parti, *LOT0001*, og du leverer stolene i en beholder med pakkenummeret *CONTAINER010*, som også inkluderer andre varer, for eksempel *LOT0100* med nattbord og *LOT200* med lamper.  

Avhengig av konfigurasjonen kan du bruke disse ulike numrene til å holde oversikt over beholdningen i [!INCLUDE [prod_short](includes/prod_short.md)] ved de forskjellige stadiene for innkjøps-, salgs-, lageroperasjoner og så videre.

## <a name="to-set-up-item-tracking-codes"></a>Slik definerer du en varesporingskode

En varesporingskode viser hvordan et selskap bruker serie- og partinumre til å holde styr på varer på forskjellige steder i lageret.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I feltene **Serienr.**, **Partinr.** og **Packagenr.** -hurtigfanene definerer du hvordan varesporing etter henholdsvis serie-, parti- eller pakkenumre skal foregå.  

> [!NOTE]  
> Hvis du vil spore bestemte varer eller bestemte partier i levetiden, må du velge feltet **Sporing basert på s.nr.** og **Sporing basert på parti** henholdsvis. Resultatet blir at ved håndtering av en utgående enhet for en vare med denne varesporingskoden, må du alltid angi hvilket eksisterende serienummer eller hvilket eksisterende partinummer som skal håndteres. Når du selger en enhet av varen, innebærer dette at serienummeret må utlignes mot et bestemt sett med serienumre eller et bestemt partinummer på lager. Et serienummer eller partinummer som tilordnes varen når du registrerer den på lager, må med andre ord følge denne varetypen ut fra lageret.

Fordi dette oppsettfeltet dekker alle mulige transaksjoner i forbindelse med varen, velges også de enkelte inngående/utgående feltene. De enkelte inngående/utgående feltene har imidlertid ingen tilknytning til lagermodulen -de definerer bare selskapets arbeidsflyt i forbindelse med tilordning av varesporingsnumre.  

> [!NOTE]  
>  Hvis du vil tilordne varesporingsnumre i lageraktiviteter, må feltene **Lagers.nr. - sporing** og **Lagerparti - sporing** være valgt på kortet for varesporingskode for varen.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Slik setter du opp utløpsregler for serie-/partinumre

Du ønsker kanskje å opprette bestemte utløpsdatoer og -regler for enkelte varer i varesporingskoden. Denne funksjonaliteten gjør at du kan holde orden på når serie- og partinumrene utløper.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.
2. Velg en eksisterende varesporingskode, og velg deretter **Rediger**-handlingen.  
3. På hurtigfanen **Diverse** merker du følgende felter:  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bruk ikke etter utløpsdato**|Angir at en utløpsdato av varesporingsnummeret ved inngang til lageret, og denne utløpsdatoen må det tas hensyn til ved utgang fra lageret.|  
    |**Krev utløpsdatooppføring**|Angir at du må angi en utløpsdato på varesporingslinjen.|  
    |**Bruk utløpsdatoer**|Angir at du vil beregne utløpsdatoer. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Slik setter du opp garantier for serie-/partinumre

Du ønsker kanskje å opprette bestemte garantier for enkelte varer i varesporingskoden. Denne funksjonen gjør det mulig å holde oversikt over når garantiene for bestemte serie- eller partinumre i lageret utløper.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.  
2. Velg en eksisterende varesporingskode, og velg deretter **Rediger**-handlingen.  
3. På hurtigfanen **Div.** fyller du ut feltet **Garantidatoformel** og velger feltene som følger:  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Garantidatoformel**|Angir den siste garantidagen for varen.|  
    |**Krev garantidatooppføring**|Angir at du må angi en garantidato på varesporingslinjen manuelt.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Slik definerer du varer for sporing med de riktige varesporingskodene

Hvis du vil aktivere varesporing, må du først tilordne varesporingskodene til en vare. Du kan legge til varesporingskoder på to måter, ved å velge koden fra en forhåndsdefinert liste eller ved å tilordne en ny unik kode. Hold markøren over feltene for å lese en kort beskrivelse.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vare** og velg den relaterte koblingen.
2. Velg en eksisterende vare fra listen, og åpne **Varekort**-siden.  
3. På hurtigfanen **Varesporing** tilordner du de aktuelle varesporingskodene og velger **Varesporingskode**, **Serienr.** og **Partinr.**.
    1. Du kan også opprette en ny varesporingskode ved å velge **Ny**-handlingen.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a>Se også

[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Varesporing](design-details-item-tracking.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
