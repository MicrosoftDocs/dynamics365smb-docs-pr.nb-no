---
title: Definere lagerverdi og kostberegning
description: 'For å sikre at lagerkost registreres riktig, må du definere ulike felt og sider før du begynner å opprette varetransaksjoner.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 07/29/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Definere lagerverdi og kostberegning

For å sikre at lagerkost registreres riktig, må du definere ulike felt og sider før du begynner å opprette varetransaksjoner. Vanligvis velger bedrifter en bestemt lagermetode og bruker den på lagervarer, for eksempel for å hjelpe dem med å spore verdien av varer på lager.  

> [!TIP]
> Hvis du vil ha en innføring i kostberegning i [!INCLUDE [prod_short](includes/prod_short.md)], se [Om lagerkost](finance-learn-about-costing.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Angi en standard lagermetode for selskapet for å styre hvordan innkommende kost brukes til å vurdere lagerverdi og solgte varers kost.|[Definere generell informasjon om lagerbeholdning](inventory-how-setup-general.md)|  
|Angi en lagermetode for individuelle varer hvis de krever en annen lagermetode.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Sikre at kost automatisk bokføres mot Finans når en lagertransaksjons bokføres.|Feltet **Automatisk kostbokføring** på siden **Lageroppsett**|  
|Sikre at forventede kostnader bokføres i Finans for å se et estimat av skyldige beløp og solgte varers kost fra midlertidige finanskonti før de faktureres.|Feltet **Bokf. av forventet kost i Finans** på siden **Lageroppsett**|  
|Definere at systemet skal justeres automatisk for eventuelle kostendringer hver gang du bokfører lagertransaksjoner.|[Justere varekost](inventory-how-adjust-item-costs.md)|  
|Definere om gjennomsnittlig kost skal beregnes bare per vare, eller per vare for hver lagerføringsenhet og hver variant av varen.|Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett**|  
|Velg hvilken tidsperiode du vil bruke til å beregne vektet gjennomsnittlig kost for varer som bruker lagermetoden Gjennomsnitt.|Feltet **Gjennomsnittskostperiode** på siden **Lageroppsett**|  
|Definere lagerperioder for å kontrollere lagerverdi over tid ved å forby transaksjonsbokføring i lukkede lagerperioder.|[Arbeide med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Sikre at salgsreturer utlignes mot den opprinnelige utgående transaksjonen for å opprettholde lagerverdi.|Feltet **Bruk opprinnelig kostpris** på siden **Salg**|  
|Sikre at kjøpsreturer utlignes mot den opprinnelige inngående transaksjonen for å opprettholde lagerverdi.|Feltet **Bruk opprinnelig kostpris** på siden **Kjøp**|
|Definere avrundingsreglene som skal brukes ved justering av eller forslag om varepriser, og når standardkost skal justeres eller foreslås.|Siden **Avrundingsmetode**|  

## Se også

[Administrere lagerkostnader](finance-manage-inventory-costs.md)    
[Definere generell lagerinformasjon](inventory-how-setup-general.md)    
[Avstemme lagerkost mot Finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Anbefalte fremgangsmåter for oppsett: Lagermetode](setup-best-practices-costing-method.md)    
[Utformingsdetaljer: lagerkostnad](design-details-inventory-costing.md)    
[Utformingsdetaljer: Endre lagermetoden for varer](design-details-changing-costing-methods.md)    
[Arbeide med Business Central](ui-work-product.md)    
[Finans](finance.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]