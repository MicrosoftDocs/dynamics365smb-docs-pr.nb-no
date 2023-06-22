---
title: Monteringsstyring
description: Finn ut hvordan du leverer produkter til kundene ved å kombinere komponenter i enkle prosesser uten å bruke produksjonsfunksjoner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management" />Monteringsstyring

Selskaper kan leverer produkter til kundene ved å kombinere komponenter uten å bruke produksjonsfunksjoner. Funksjoner for å knytte sammen elementer integreres med relaterte funksjoner, for eksempel salg, planlegging, reservasjoner og lagerstyring.  

En monteringsvare er en salgbar vare som inneholder en monteringsstykkliste. Hvis du vil ha mer informasjon om monteringsstykklister, går du til [Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md).

Monteringsordrer er interne ordrer, på samme måte som produksjonsordrer. Bruk monteringsordrer til å håndtere monteringsprosessen og til å koble salgskrav til lageraktiviteter. Monteringsordrer omfatter både avgang og forbruk ved bokføring. Monteringsordrehoder ligner på ferdigmeldingskladdelinjer. Monteringsordrelinjer ligner på forbrukskladdelinjer.  

Du kan bruke en Just-in-time-strategi og tilpasse produkter for å oppfylle kundeforespørsler. Monteringsordrer kan opprettes automatisk og kobles til når du oppretter en ordrelinje. Koblingen mellom salgsbehovene og monteringsforsyningen åpner for flere salgsmuligheter når du behandler ordrer:

* Tilpass monteringsvarer på farten.
* Lov leveringsdatoer i henhold til komponenttilgjengelighet.
* Bokfør avgang og levering av den monterte varen direkte fra ordrene.

Hvis du vil finne ut mer om å selge monteringsvarer, kan du gå til [Selg varer montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Linjer i ordrer kan inneholde varer for plukking fra lager og varer som skal monteres for ordren. Monter-til-ordre-antallet til prioritet over lagerantall i delvis levering. Hvis du vil finne ut mer om å selge lager- og monteringsvarer, kan du gå til [Kombinasjonsscenarioer](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Når et montere-til-ordre-antall er klart til å leveres, kan en lageransatt bokføre et lagerplukk for ordrelinjene. Bokføring av et lagerplukk gjør et par ting:

* Opprett en lagerflytting for komponentene
* Bokfør monteringsavgang og ordreforsendelsen.

Hvis du vil finne ut mer om monter-til-ordrevarer og lagerplukk, kan du gå til [Håndter monter-til-ordrevarer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Finn ut mer om hvordan du monterer varer for ordrer og lagring.|[Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Bruk lokasjonskort og lageroppsettet for å definere hvordan varene flyter til og fra monteringen.|[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Tilby en kundemonteringsvare, og konverter tilbudet til et salg når kunden godtar det.|[Gi tilbud på et montere-til-ordre-salg](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombiner komponenter for å opprette en vare til bestilling eller til lager.|[Montere elementer](assembly-how-to-assemble-items.md)|  
|Selg monteringsvarer som ikke er tilgjengelige for øyeblikket, ved å opprette koblet monteringsordre for å levere hele eller en del av ordreantallet.|[Selg varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Når montere-til-ordre-varer allerede er på lager, kan du trekke antallet fra monteringsordren og reservere det fra beholdningen.|[Selge lagervarer i monter-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Når monteringsvarer ikke er på lager, bruker du en monteringsordre til å levere noe eller hele antallet.|[Selge montere til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Lag egendefinerte monteringsvarer for rammeordrer før du oppretter ordrene.|[Opprette rammemonteringsordrer](assembly-how-to-create-blanket-assembly-orders.md)|
|Angre en bokført monteringsordre, for eksempel fordi ordren ble bokført med feil.|[Angre monteringsbokføring](assembly-how-to-undo-assembly-posting.md)|
|Finn ut hvordan du arbeider med monteringsstykklister og hvordan de er forskjellige fra produksjonsstykklister.|[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)|
|Finn ut mer om bokføring av monteringsforbruk og -avgang, og hvordan [!INCLUDE [prod_short](includes/prod_short.md)] distribuerer vare- og ressurskostnader til finans.|[Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-trainingtrainingpathsassemble-items-dynamics--business-central" />Se relatert [Microsoft-opplæring](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Arbeid med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Utformingsdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
