---
title: Definer kundeprisgrupper
description: Lær hvordan du definerer kundeprisgrupper og oppretter salgspriser for disse gruppene.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer price groups, discounts, sales prices
ms.date: 09/30/2021
ms.author: edupont
ms.openlocfilehash: d7c658dea40441791a2dc8adda1ca2a8d745c973
ms.sourcegitcommit: 428ba6385cb27475e8803c2a8967daa22cfe8879
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/29/2021
ms.locfileid: "7724509"
---
# <a name="set-up-customer-price-groups"></a>Definer kundeprisgrupper
  
Salgsprisene kan gjøres avhengig av kundegruppene du selger til. Disse gruppene kalles kundeprisgrupper.

Før du definerer kundeprisgrupper, må du bestemme hvor mange grupper du vil ha, og hvilke kunder som skal tilhøre de enkelte gruppene.  

## <a name="how-to-create-sales-prices-for-a-group-of-customers"></a>Opprett salgspriser for en kundegruppe  

Når det er nådd enighet om den prisen som kundegruppen skal betale for bestemte varer, registrerer du hva som er avtalt for de enkelte varene på linjene på **Salgspris**-siden.

### <a name="to-create-sales-prices-for-a-group-of-customers"></a>Slik oppretter du salgspriser for en kundegruppe

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

## <a name="how-to-enter-customer-price-group-codes-on-customer-cards"></a>Angi kundeprisgruppekoder på kundekort  

Når du har definert kundeprisgruppene, kan du angi kundeprisgruppekodene på kundekortene.

### <a name="to-enter-customer-price-group-codes-on-a-customer-card"></a>Slik angir du kundeprisgruppekoder på et kundekort  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  

2. Åpne det aktuelle **kundekortet** for en kunde du vil skal være del av en kundeprisgruppe.  

3. Velg koden **Kundeprisgruppe** i feltet **Kundeprisgruppe** på hurtigfanen **Fakturering**.  


## <a name="see-also"></a>Se også

[Registrere spesielle salgspriser og rabatter](sales-how-record-sales-price-discount-payment-agreements.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
