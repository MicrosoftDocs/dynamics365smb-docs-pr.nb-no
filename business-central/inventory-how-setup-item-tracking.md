---
title: 'Konfigurer varesporing med serie-, parti- og pakkenumre'
description: 'Konfigurer varesporing med serienumre, partinumre og pakkenumre'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: bholtorf
---
# Konfigurer varesporing med serie-, parti- og pakkenumre

Holde oversikt over lagervarer selv i komplekse lagerkonfigurasjoner med numre som er spesifikke for hver vare, enten som et individuelt objekt, for eksempel et parti, eller som en pakke. Ved hjelp av varesporing kan du spore varer på tvers av interne lagerflyttinger, og utgående og inngående dokumenter.

Varer med serie- og partinumre kan spores både bakover og fremover i forsyningskjeden. Dette er nyttig for generell kvalitetskontroll og tilbakekalling av proukter. Hvis du vil ha mer informasjon, kan du se [Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> I lanseringsbølge 1 for 2021 og nyere aktiverer du oppdatering av funksjonen *Bruk sporing etter pakkenummer i reservasjons- og sporingssystem* hvis du vil arbeide med pakkenumre samt serie-og partinumre. Hvis du vil ha mer informasjon, kan du se [Aktivere kommende funksjoner på forhånd](admin-feature-management.md). Når funksjonen er aktivert, kan du tilordne pakkenumre til utgående og inngående dokumenter, på samme måte som du kan arbeide med partinumre.  

## Numre og varesporing

Som en del av lagerprosessene, kan du pakke lageret i pakker, bokser, beholdere og så videre. Men for å holde orden på varene, tilordner du unike tall som identifikasjon. Det kan for eksempel være at du produserer og selger en stol som har varenummer *1900-S*. Hver stol har et serienummer, *1001*, men du kan også bunte fire stoler i et parti, *LOT0001*, og du leverer stolene i en beholder med pakkenummeret *CONTAINER010*, som også inkluderer andre varer, for eksempel *LOT0100* med nattbord og *LOT200* med lamper.  

Avhengig av konfigurasjonen kan du bruke disse ulike numrene til å holde oversikt over beholdningen i [!INCLUDE [prod_short](includes/prod_short.md)] ved de forskjellige stadiene for innkjøps-, salgs-, lageroperasjoner og så videre.

## Slik definerer du en varesporingskode

En varesporingskode viser hvordan et selskap bruker serie- og partinumre til å holde styr på varer på forskjellige steder i lageret.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I feltene **Serienr.**, **Partinr.** og **Packagenr.** -hurtigfanene definerer du hvordan varesporing etter henholdsvis serie-, parti- eller pakkenumre skal foregå.  

> [!NOTE]  
> Hvis du vil spore bestemte varer eller bestemte partier i levetiden, må du velge feltet **Sporing basert på s.nr.** og **Sporing basert på parti** henholdsvis. Resultatet blir at ved håndtering av en utgående enhet for en vare med denne varesporingskoden, må du alltid angi hvilket eksisterende serienummer eller hvilket eksisterende partinummer som skal håndteres. Når du selger en enhet av varen, innebærer dette at serienummeret må utlignes mot et bestemt sett med serienumre eller et bestemt partinummer på lager. Et serienummer eller partinummer som tilordnes varen når du registrerer den på lager, må med andre ord følge denne varetypen ut fra lageret.

Fordi dette oppsettfeltet dekker alle mulige transaksjoner i forbindelse med varen, velges også de enkelte inngående/utgående feltene. De enkelte inngående/utgående feltene har imidlertid ingen tilknytning til lagermodulen -de definerer bare selskapets arbeidsflyt i forbindelse med tilordning av varesporingsnumre.  

> [!NOTE]  
> Hvis du vil tilordne varesporingsnumre i lageraktiviteter, må feltene **Lagers.nr. - sporing** og **Lagerparti - sporing** være valgt på kortet for varesporingskode for varen.  

## Slik setter du opp utløpsregler for serie-/partinumre

Du ønsker kanskje å opprette bestemte utløpsdatoer og -regler for enkelte varer i varesporingskoden. Denne funksjonaliteten gjør at du kan holde orden på når serie- og partinumrene utløper.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.
2. Velg en eksisterende varesporingskode, og velg deretter **Rediger**-handlingen.  
3. På hurtigfanen **Diverse** merker du følgende felter:  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bruk ikke etter utløpsdato**|Angir at en utløpsdato av varesporingsnummeret ved inngang til lageret, og denne utløpsdatoen må det tas hensyn til ved utgang fra lageret.|  
    |**Krev utløpsdatooppføring**|Angir at du må angi en utløpsdato på varesporingslinjen.|  
    |**Bruk utløpsdatoer**|Angir at du vil beregne utløpsdatoer. |  

## Slik setter du opp garantier for serie-/partinumre

Du ønsker kanskje å opprette bestemte garantier for enkelte varer i varesporingskoden. Denne funksjonen gjør det mulig å holde oversikt over når garantiene for bestemte serie- eller partinumre i lageret utløper.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporingskoder** og velg den relaterte koblingen.  
2. Velg en eksisterende varesporingskode, og velg deretter **Rediger**-handlingen.  
3. På hurtigfanen **Div.** fyller du ut feltet **Garantidatoformel** og velger feltene som følger:  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Garantidatoformel**|Angir den siste garantidagen for varen.|  
    |**Krev garantidatooppføring**|Angir at du må angi en garantidato på varesporingslinjen manuelt.|  


## Slik definerer du varer for sporing med de riktige varesporingskodene

Hvis du vil aktivere varesporing, må du først tilordne varesporingskodene til en vare. Du kan legge til varesporingskoder på to måter, ved å velge koden fra en forhåndsdefinert liste eller ved å tilordne en ny unik kode. Hold markøren over feltene for å lese en kort beskrivelse.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vare** og velg den relaterte koblingen.
2. Velg en eksisterende vare fra listen, og åpne **Varekort**-siden.  
3. På hurtigfanen **Varesporing** tilordner du de aktuelle varesporingskodene og velger **Varesporingskode**, **Serienr.** og **Partinr.**.
    1. Du kan også opprette en ny varesporingskode ved å velge **Ny**-handlingen.

## Slik angir du åpningssaldoer for varene du sporer

Du kan opprette åpningssaldoer for varene du følger opp. Siden du kan velge ulike lagerkonfigurasjoner, du kan velge mellom to alternativer:

* Aktiver bestemte kladder på siden **Varekladd** for å la andre angi serie-, parti-og pakkedata direkte på kladdelinjer.
* For lokasjoner der vekslebryteren **Lagerstyring** er aktivert, kan du bruke siden **Lageropptellingskladd** til å gjøre alle varesporingsfeltene tilgjengelige. Feltene som er tilgjengelige, inkluderer feltene **Garantidato** og **Utløpsdato**.

### Varekladder 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekladder** og velg den relaterte koblingen.
2. Velg feltet **Navn** for å åpne en liste over varekladdpartier.
3. Velg **Opprett** for å opprette en ny bunke, og slå på vekslebryteren **Varesporing på linjer**.
4. Velg **OK** for å velge bunken du opprettet.
5. Fyll ut feltene på varekladdlinjen etter behov. Legg merke til at feltene **Partinr.**, **Serienr.**, **Utløpsdato**, **Garantidato** og **Pakkesporingsnr.** er tilgjengelige (hvis funksjonen er aktivert).
6. Velg handlingen **Bokfør** til å justere lageret.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] har noen mindre valideringer når du angir eller importerer data. Det oppstår en mer omfattende kontroll når du bokfører eller overfører data fra kladdelinjer til **varesporingsvinduet**. Det siste skjer automatisk når du åpner siden **Varesporingsvindu** fra varekladdelinjen, eller hvis du velger handlingen **Oppdater varesporingslinjer**.

### Lagervareopptellingskladd for lokasjoner der lagerstyring er slått på  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervareopptellingskladd**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på varekladdlinjen etter behov. Legg merke til at feltene **Partinr.**, **Serienr.**, **Utløpsdato**, **Garantidato** og **Pakkesporingsnr.** er tilgjengelige (hvis funksjonen er aktivert).
3. Velg handlingen **Registrer** for å foreta lagerjusteringene. Husk at du må synkronisere de justerte lagerpostene med de tilhørende varepostene. Hvis du vil ha mer informasjon, går du til [Synkroniser de justerte lagerpostene](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

For masseImporter bruker du konfigurasjonspakker til å importere data til kladdene.

> [!NOTE]
> Du kan ikke bruke **Rediger i Excel** til å opprette kladdelinjer med sporingsinformasjon.

## Se også

[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Vare varesporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Varesporing](design-details-item-tracking.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
