---
title: Selge lagervarer i monter-til-ordre-flyter
description: Monter-til-ordre-varer settes sammen for ordrer gjennom en monteringsordre.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# Salg av lagervarer i montere til ordre-flyter

Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare inneholder **Monter til ordre**, forutsetter ordreprosess at varen ikke er på lager og må monteres for denne bestemte ordrene. Når du legger til varen på en linje på en ordre, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] en monteringsordre som kobles til ordren. Hvis du vil finne ut mer om hvordan du selger monter-til-ordre-varer, kan du gå til [Selg varer montert til ordre](assembly-how-to-sell-items-assembled-to-order.md). Hvis noe av ordreantallet allerede er tilgjengelig i beholdningen, kan du redusere monteringsordreantallet ved å endre feltet **Ant. som skal monteres til ordre** på ordrelinjen.  

Det er relativt sjeldne for selskaper å selge lagervarer som monter-til-ordre-varer. Monter-til-ordre-varer er vanligvis ikke standard. De er tilpasset for å dekke bestemte kundekrav. Du kan imidlertid ha antall for monter-til-ordre-varer på lageret på grunn av returer eller ordrekanselleringer. Antallet skal plukkes og selges før nye monteres.  

> [!NOTE]  
> Hvis du vil kontrollere om det finnes monter-til-ordre-varer allerede er tilgjengelige for monteringsordrer, bruker du faktaboksen **Salgslinjedetaljer** på ordren.  

Du kan gjøre lignende ting når du selger monteringsvarer fra lageret, og noe av eller hele antallet ikke er tilgjengelig. Du kan angi det manglende antallet i en monteringsordre. Hvis du vil finne ut mer om å selge lager og monteringsvarer, kan du gå til [Selg montere-til-ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Det finnes regler som gjelder feltet **Levere (antall)** på ordrelinjer som inneholder en kombinasjon av monter-til-ordre-antall og lagerantall. Hvis du vil ha mer informasjon om reglene, kan du gå til [Kombinasjonsscenarioer](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

I denne fremgangsmåten erstatter du montere-til-ordre-antall med lagerantall på en ordrelinje. Følgende fremgangsmåte gir en oversikt:

1. Fastslå tilgjengelighet.
2. Reduser antallet fra den koblede monteringsordren.
3. Tilbakefør lagerantallet for å sikre at det er plukket og levert for ordren.  

## Selge lagervarer i montere til ordre-flyter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ordre. Hvis du vil finne ut mer om oppretting av ordrer, kan du gå til [Selg produkter](sales-how-sell-products.md).  
3. På en ordrelinje som inneholder en montere-til-ordre-vare angir du antall i feltet **Antall**.  
4. Finn ut om alt eller noe av behovsantallet er disponibelt, i faktaboksen **Salgslinjedetaljer**.  
5. Trekk fra disponibelt antall i feltet **Ant. som skal monteres til ordre**, slik at bare det ikke-disponible antallet monteres til ordren. **Reservert antall**-feltet reduseres tilsvarende for å gjenspeile at koblingen for ordre-til-ordre eller reservasjon bare gjelder for antallet som skal monteres.  
6. På hurtigfanen **Linjer** velger du **Funksjoner** og deretter **Reserver**.  
7. Velg varepostlinjen eller -linjene som inneholder det disponible antallet på **Reservasjon**-siden, velg **Reserver fra gjeldende linje**, og klikk deretter **OK**.  

    På **Ordre**-siden viser **Reservert antall**-feltet nå at hele antallet for ordrelinjen er reservert. Feltet **Ant. som skal monteres til ordre** gjenspeiler antallet som skal monteres.  

8. Frigi ordren for å gjøre varer tilgjengelige for plukking av varene og for montering av de utilgjengelige varene. Hvis du vil finne ut mer om montering av varer, går du til [Monter varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> **Hyllekode**-feltet på ordren kan inneholde verdien fra feltet **Hyllek. lev. fra m. til ordre** eller **Fra Hyllekode for montering** på lokasjonskortet. Hvis det gjør det, er kanskje **Hyllekode**-feltet på ordrelinjen feil for denne kombinasjonen av montere-til-ordre- og montere-til-lager-antall. Det er en god idé å dobbeltsjekke at hyllen i **Hyllekode**-feltet fungerer for alle antall. Du kan også angi to forskjellige antall på separate ordrelinjer.  

## Se relatert [Microsoft-opplæring](/training/modules/assemble-to-order-dynamics-365-business-central/)

## Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
