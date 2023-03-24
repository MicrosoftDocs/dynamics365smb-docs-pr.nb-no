---
title: Selge montere til ordre-varer og lagervarer sammen
description: 'Hvis en del av en monter-til-lager-vare ikke er tilgjengelig, kan du opprette en monteringsordre for det gjenværende antallet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# Selge montere til ordre-varer og lagervarer sammen

Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare inneholder **Monter til lager**, forutsetter standard ordreprosess at varen allerede er montert og kan plukkes fra lager, hvis den er tilgjengelig. En monteringsordre blir derfor ikke automatisk opprettet og koblet til ordrelinjen. Hvis noe eller hele antallet ikke er tilgjengelig, kan du derimot opprette en monteringsordre for det gjenværende antallet. Det gjør du ved å fylle ut feltet **Ant. som skal monteres til ordre** på ordrelinjen. Med denne innstillingen kan du montere varen til ordre selv om den er definert slik at den monteres til lager.  

Du har lignende fleksibilitet når du selger monter-til-ordre-varer og noe av antallet allerede er på lager. Du bør trekke antallet fra monteringsordren. Hvis du vil finne ut mer om å selge lagervarer, kan du gå til [Selg lagervarer i montert-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Det finnes regler som gjelder feltet **Levere (antall)** på ordrelinjer som inneholder en kombinasjon av monter-til-ordre-antall og lagerantall. Hvis du vil ha mer informasjon om reglene, kan du gå til [Kombinasjonsscenarioer](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Følgende fremgangsmåte omfatter ikke trinnene for ordrer som du må følge før du oppretter en monteringsordre for utilgjengelige antall.

## Selge montere til ordre-varer og lagervarer sammen

1. På en salgsordrelinje for en monter-til-ordre-vare angir du et antall i feltet **Antall** som overskrider beholdningen. Siden **Kontroller tilgjengelighet** vises. Hvis du vil finne ut mer om varedisposisjon, går du til [Vis tilgjengeligheten for varene](inventory-how-availability-overview.md).
2. Angi verdien fra feltet **Totalt antall** i feltet **Ant. som skal monteres til ordre**.  
3. Gjør eventuelle endringer som treng i monteringskomponentene. Finn ut mer under [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  
4. Frigi ordren for å gjøre varer tilgjengelige for plukking av varene og for montering av de utilgjengelige varene. Hvis du vil finne ut mer om disse standardtrinnene for montering, kan du gå til [Monter varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> **Hyllekode**-feltet på ordren kan inneholde verdien fra feltet **Hyllek. lev. fra m. til ordre** eller **Fra Hyllekode for montering** på lokasjonskortet. Hvis det er det, er kanskje **Hyllekode**-feltet på ordrelinjen feil for denne kombinasjonen av montere-til-ordre- og montere-til-lager-antall. Det er en god idé å dobbeltsjekke at hyllen i **Hyllekode**-feltet fungerer for alle antall. Du kan også angi to forskjellige antall på separate ordrelinjer.  

## Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]