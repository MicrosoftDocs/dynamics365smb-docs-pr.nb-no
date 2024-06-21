---
title: Definer kundeprisgrupper
description: Lær hvordan du definerer kundeprisgrupper og oppretter salgspriser for disse gruppene.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'customer price groups, discounts, sales prices'
ms.date: 09/30/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Definer kundeprisgrupper
  
Salgsprisene kan gjøres avhengig av kundegruppene du selger til. Disse gruppene kalles kundeprisgrupper.

Før du definerer kundeprisgrupper, må du bestemme hvor mange grupper du vil ha, og hvilke kunder som skal tilhøre de enkelte gruppene.  

## Opprett salgspriser for en kundegruppe  

Når det er nådd enighet om den prisen som kundegruppen skal betale for bestemte varer, registrerer du hva som er avtalt for de enkelte varene på linjene på **Salgspris**-siden.

### Slik oppretter du salgspriser for en kundegruppe

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kundeprisgrupper**, og velg deretter den relaterte koblingen.  

2. Velg linjen for kundeprisgruppen. Hvis det ikke allerede finnes noen linje, kan du opprette en ny linje. Velg **Ny** for å opprette en ny enhet og gi den et navn.  
    
    For den valgte linjen kontrollerer du innholdet i feltene **Tillat linjerabatt**, **Tillat fakturarabatt**, **Pris inkl. mva.** og **Mva-bokf.gruppe – firma (pris)**. 
  
3. Velg **Naviger**-handlingen, og velg **Salgspriser**. Siden **Salgspriser** åpnes. Feltet **Salgstype** fylles ut med **Kundeprisgruppe**.  
  
4. Fyll ut **salgskoden** med den salgskoden du valgte på forrige side.  
  
5. Fyll ut feltene på linjene med **Varenr.**, **Enhetskode** og avtalt **Salgspris**. Du kan også vise kolonnen **Variantkode** og spesifisere **variantkoden** hvis det er flere varianter av varen.  
  
6. Hvis kundegruppen må kjøpe et minimumsantall av varen for å oppnå den avtalte prisen, fyller du ut feltet **Minimumsantall**.  

7. Om nødvendig legger du inn **Startdato** og **Sluttdato** for prisavtalen.  
  
8. Hvis det er aktuelt, kan du også fylle ut **Valutakode**-feltet.

Gjenta trinnene 4 til 8 for hver vare du vil opprette en salgspris for.

## Angi kundeprisgruppekoder på kundekort  

Når du har definert kundeprisgruppene, kan du angi kundeprisgruppekodene på kundekortene.

### Slik angir du kundeprisgruppekoder på et kundekort  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  

2. Åpne det aktuelle **kundekortet** for en kunde du vil skal være del av en kundeprisgruppe.  

3. Velg koden **Kundeprisgruppe** i feltet **Kundeprisgruppe** på hurtigfanen **Fakturering**.  


## Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Registrer spesielle salgspriser og rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  
[Konfigurering av kunderabattgrupper](sales-how-to-set-up-customer-discount-groups.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
