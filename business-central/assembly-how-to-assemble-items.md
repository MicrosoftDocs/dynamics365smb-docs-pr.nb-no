---
title: Montere elementer
description: Finn ut mer om Monter til ordre- og Monter til lager-prosesser i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Montere elementer

Hvis feltet **Etterfyllingssystem** på varekortet inneholder **Montering**, er standardmetoden for å forsyne varen å montere den i henhold til en monteringsstykkliste og muligens av en bestemt ressurs. Finn ut mer under [Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md). Finn ut mer om hvordan du definerer en monteringsvare under [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

Du kan konfigurerer monteringsvarer for to ulike monteringsprosesser.

|Behandle  |Description  |
|---------|---------|
|Monter til lager     | Varer som du monterer og lagrer for fremtidig salg. Det kan for eksempel være pakker for en forestående salgskampanje. Varene er ikke knyttet til en ordre, i det minste ikke ennå. Disse varene tilpasses vanligvis ikke til kundeforespørsler.        |
|Monter til ordre     | Varer som du ikke vil lagre. For eksempel fordi de er tilpasset basert på kundeordrer eller for å redusere kostnaden av lagerbeholdningen. |
  
Denne artikkelen beskriver standardinnstillingene for montering til lager. Det kan være andre måter som er bedre egnet for virksomheten din. Finn ut mer under [Selg lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) og [Selg montere-til-ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Monteringskomponenter håndteres på en spesiell måte i enkle lagerkonfigurasjoner. Finn ut mer under [Håndter montere-til-ordre-varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## Slik monterer du en vare til lager

Følg fremgangsmåten nedenfor for å montere en vare til lager. Hvis du vil lære mer om å montere til ordre, kan du gå til [Selg varer montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Monteringsordrer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Ny monteringsvare** åpnes.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg varen du vil montere, i **Varenr.**-feltet. Du kan velge varer som er definert for montering og har en monteringsstykkliste, eller varer uten en monteringsstykkliste. Sistnevnte er nyttig for ikke-planlagte samlinger eller scenarioer når du vil bruke ny klassifisering av varer og spore kostnader.  
5. Angi hvor mange enheter av varen du vil ha montert, i **Antall**-feltet.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter er tilgjengelige for å oppfylle antallet på forfallsdatoen, åpnes siden **Monteringstilgjengelighet**. Siden viser hvor mange monteringsvarer som kan monteres på grunnlag av komponenttilgjengelighet. Finn ut mer under [Vis tilgjengeligheten av varer](inventory-how-availability-overview.md). Når du lukker siden, opprettes monteringsordren med tilgjengelighetsvarsler på linjene til de berørte komponentene.  

    Linjene inneholder innholdet i monteringsstykklisten og de angitte antallene.  

    > [!NOTE]  
    >  Hvis siden **Montering – tilgjengelighet** ble åpnet da du fylte ut monteringsordrehodet, inneholder hver påvirkede monteringsordrelinje **Ja** i feltet **Tilgj. advarsel** med en kobling til detaljert tilgjengelighetsinformasjon. <!--check whether this field help is useful For more information, see Check Availability.--> Du kan løse et problem med komponenttilgjengelighet ved å gjøre følgende:

    > * utsette startdatoen
    > * erstatte komponenten med en annen vare
    > * velge en tilgjengelig erstatning hvis den er definert  

6. Angi hvor mange enheter av monteringsvaren du vil bokføre som avgang neste gang du bokfører monteringsordren, i feltet **Antall å montere**. Dette antallet kan være lavere enn verdien i **Antall**-feltet for å gjenspeile en delvis avgangsbokføring.  

    > [!NOTE]  
    >  For å sikre at komponentforbruksbokføring samsvarer med avgangsbokføring for monteringsvarer justeres antallsfeltene i monteringsvarelinjene automatisk til verdien du angir i feltet **Antall å montere**.  
7. På monteringsordrelinjer av typen **Vare** eller **Ressurs** angir du i feltet **Antall som skal forbrukes** hvor mange enheter du vil bokføre som forbrukt neste gang du bokfører monteringsordren.
8. Når du er klar til å bokføre delvis eller fullstendig, velger du **Bokfør**-handlingen.  

    > [!NOTE]  
    >  Hvis det fortsatt er advarsler i monteringsordrelinjene, kan du ikke bokføre ordren. Det vises en melding om komponentene som ikke er på lageret.  

Etter vellykket bokføring, bokføres monteringsvaren som avgått til lokasjonskoden og den potensielle hyllekoden som er definert i monteringsordren. For manuelt opprettede monteringsordrer kan kan lokasjonen kopieres fra oppsettfeltet **Standardlokasjon for ordrer**. Når det gjelder montere-til-ordre-flyter, kan du kopiere lokasjonskoden fra ordrelinjen.  

## Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
