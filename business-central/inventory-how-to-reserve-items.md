---
title: Slik reserverer du varer
description: 'Lær mer om reservering av varer for ordrer, bestillinger og produksjonsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 05/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Reservere varer

Du kan reservere varer for ordrer, bestillinger, serviceordrer, monteringsordrer, overføringsordrer og produksjonsordrer. Du kan også reservere varer på lager eller inngående på åpne dokument- eller kladdelinjer. Dette gjør du på siden **Reservasjon**.

Hver linje du åpner for å reservere varer på **Reservasjon**-siden, viser informasjon om én type linje (salg, kjøp eller kladd) eller lagerpost. Linjene beskriver hvor mange varer som kan reserveres fra hver linje- eller posttype.

> [!TIP]
> Basert på antallet du har reservert på lageret, viser [!INCLUDE [prod_short](includes/prod_short.md)] en status i dokumentene, slik at du raskt blir klar over neste trinn. For eksempel for å angi at du kan levere en ordre eller begynne å arbeide med et prosjekt, en montering eller en produksjonsordre. Statusen bidrar også til å redusere risikoen for utilsiktede delvise forsendelser eller forsinkelser på grunn av manglende lager for produksjons- og monteringsordrer.
>
> Feltet **Reservert fra lager** kan hjelpe deg med å forstå om du kan levere eller plukke for en bestemt ordre eller ordrelinje. For linjer er feltet Reservert fra lager tilgjengelig i faktabokser. Hvis du vil ha tilgang til informasjonen for hele ordren, er feltet på **Statistikk**-siden.

## Reserver varer for salg

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

## Reserver varer for produksjonsordrelinjer

Du kan reservere varer for produksjonsordrer. Du må skille mellom produksjonsordrelinjer, som betyr den overordnede varen, og produksjonsordrekomponenter.

I fremgangsmåten nedenfor brukes det en fast planlagt produksjonsordre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Fast planlagt prod.ordre** og velg den relaterte koblingen.  
2. Åpne den fast planlagte produksjonsordren du vil reservere overordnede varer for.  
3. Velg den aktuelle produksjonsordrelinjen.  
4. Velg handlingen Reserver i Funksjoner-gruppen **på** hurtigfanen Linjer **.**  **·** 
5. På **Reservasjon-siden** Velg du Salgslinje, Ordrelinje, og deretter velger du handlingen **Reserver fra gjeldende linje** .  

Antallet du angav på den fast planlagte produksjonsordrelinjen, er nå reservert.

## Reserver varer for produksjonsordrekomponenter

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

## Reservere varer samtidig

Bruk siden **Reservasjonsforslag** til å reservere og fordele innkommende varer samtidig. Massereservasjoner kan for eksempel bidra til å sikre at antall er tilgjengelige for salgs- og produksjonsordrene. Du kan ha flere bunker til ulike formål. Du kan for eksempel tildele produksjonsordrer på ukentlig basis, men reservere daglig for salg.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Reservasjonsforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen Hent **etterspørsel** . Siden **Hent etterspørsel etter å reservere** åpnes.
1. På **siden Hent behov som skal reserveres** angir du hvilken type behov du vil reservere fra tilgjengelig lager.
1. Fyll ut filtrene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
1. Valgfritt: Hvis du vil fordele varene med en gang, velger du handlingen **Tildel**.
1. På siden **Fordelingspolicy** velger du en policy for hvert trinn.

   |Fordelingspolicy  |Description  |
   |---------|---------|
   |Grunnleggende (ingen konflikter)     | Fordeler lager til et behov hvis det ikke er noen konflikter og behovet kan dekkes fullt ut. Du har for eksempel ordre A med antallet 10 og et prosjekt med et antall på 7. Hvis du har 20 på lager, får begge kravene full mengde. Hvis lager er 12, tildeles ingen aksjer. Du må tildele antallet manuelt.        |
   |Lik    | Distribuerer tilgjengelig lager etter behov likt. Du har for eksempel en ordre med antallet 10 og et prosjekt med et antall på 7. Hvis lagernivået ditt er 20, vil begge kravene få fullt antall. Hvis aksjen din er 12, vil begge kravene få 6.        |
   |Etter kundeprioritet|Distribusjon basert på **Prioritet**-feltet på **Kundekort**-siden. Når det gjelder lave lagerantall, forsyner Business Central kunder med høyeste prioritet først.|

6. Hvis du vil reservere alle linjer der **Godta** er aktivert, velger du handlingen **Reserver**.
    
## Endre en reservasjon

Du kan endre en varereservasjon.

1. Fra dokumentlinjen som du gjorde reservasjonen fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. På **Reservasjon**-siden velger du handlingen **Reservasjonsposter**.
3. På siden **Reservasjonsposter** oppdaterer du **Antall**-feltet på linjen du vil endre.
4. Bekreft meldingen som vises, ved å velge **OK**-knappen.

## Kanseller en reservasjon

Du kan avbryte en varereservasjon.

1. Fra dokumentlinjen som du ønsker å avbryte en reservasjon fra, på hurtigfanen **Linjer**, velger du **Reserver**-handlingen.  
2. På **Reservasjon-siden** velger du handlingen **Reservasjonsposter** på **hurtigfanen Linjer** .  
3. På **Reservasjon**-siden velger du handlingen **Kanseller reservasjon**.  
4. Bekreft meldingen som vises, ved å velge **Ja**-knappen.  

## Reserver et spesifikt serie- eller partinummer

Fra utgående dokumenter for varesporede varer, for eksempel ordrer eller produksjonskomponentlister, kan du reservere bestemte serie- eller partinumre. Det kan for eksempel være nyttig å reservere bestemte serie- eller partinumre i følgende situasjoner:

* Hvis du trenger produksjonskomponenter fra et bestemt parti for å sikre konsistens med tidligere produksjonsbatcher.
* Fordi en kunde har bedt om et bestemt serienummer. 

Finn ut mer under [Arbeid med serie- og partinumre](inventory-how-work-item-tracking.md).

Denne praksisen kalles en bestemt reservasjon fordi du reserverer fra antallet av vare X som tilhører parti X. Hvis du derimot bare reserverer fra antall varer X, er det ganske enkelt en vanlig, ikke-spesifikk reservasjon. Finn ut mer under [Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md).

Følgende fremgangsmåte er basert på en ordre.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ordrelinje for en varesporet vare.  
3. Tilordne serie- eller partinumre til ordrelinjen. Finn ut mer under [Arbeid med serie- og partinumre](inventory-how-work-item-tracking.md).
4. Velg handlingen **Reserver** på ordrelinjen.  
5. Velg **Ja**-knappen for å reservere bestemte serie- eller partinumre.  
6. Velg serie- og partinummerkombinasjonen du har tildelt, på siden **Varesporingsoversikt**.  
7. Velg **OK**-knappen for å åpne siden **Reservasjon**, som bare viser det angitte varesporingsnummeret. Hvis det finnes ikke-spesifikke reservasjoner for noen av varesporingsnumrene du har angitt for denne linjen, får du beskjed om antallet som allerede er reservert.  
8. Velg **Auto-reserver** eller **Reserver fra gjeldende linje** for å opprette reservasjonen for de spesifikke varesporingsnumrene.

## Se også

[Lager](inventory-manage-inventory.md)  
[Utformingsdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
