---
title: Monteringsstyring | Microsoft-dokumentasjon
description: Støtt selskaper som leverer produkter til kundene ved å kombinere komponenter i enkle prosesser, uten behov for produksjonsfunksjonalitet, men med funksjoner for å montere varer som integreres med eksisterende funksjoner, for eksempel salg, planlegging, reservasjoner og lagerstyring.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b734d867401697b1c554f321d5b153f093dd5cd8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753237"
---
# <a name="assembly-management"></a>Monteringsstyring
For å kunne støtte selskaper som leverer produkter til kundene ved å kombinere komponenter i enkle prosesser, uten behov for produksjonsfunksjonalitet, har [!INCLUDE[prod_short](includes/prod_short.md)] funksjoner for å montere varer som integreres med eksisterende funksjoner, for eksempel salg, planlegging, reservasjoner og lagerstyring.  

 En monteringsvare er definert som en salgbar vare som inneholder en monteringsstykkliste. Hvis du vil ha mer informasjon, kan du se [Arbeide med stykklister](inventory-how-work-BOMs.md).

 Monteringsordrer er interne ordrer, akkurat som produksjonsordrer, som brukes til å håndtere monteringsprosessen og knytte sammen salgskravene med de involverte lageraktivitetene. Monteringsordrer er forskjellige fra andre ordretyper fordi de inkluderer både avgang og forbruk under bokføring. Monteringsordrehodet fungerer på samme måte som en ferdigmeldingskladdelinje, og monteringsordrelinjene fungerer på samme måte som forbrukskladdelinjer.  

 Hvis du vil støtte en JIT-lagerstrategi (Just In Time) og muligheten til å tilpasse produkter til kundens ønsker, kan monteringsordrer opprettes og kobles automatisk så snart ordrelinjen opprettes. Koblingen mellom salgsbehovet og monteringsforsyningen gjør det mulig for salgsordrebehandlere å tilpasse monteringsvaren på et øyeblikk, bekrefte leveringsdatoer i henhold til komponenttilgjengelighet og bokføre avgang og levering av den monterte varen direkte fra salgsordregrensesnittet. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Du kan selge et antall som er tilgjengelig og som må plukkes fra lager sammen med et antall som må monteres til ordren på én salgsordrelinje. Det finnes visse regler for å styre distribusjonen av slike antall for å sørge for at monter til ordre-antall har prioritet over lagerantall ved delvis levering. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Det finnes spesiell funksjonalitet for å styre leveringen av monter-til-ordre-antall. Når et montere-til-ordre-antall er klart til å leveres, bokfører den overordnede lagermedarbeideren en lagerplukking for den/de aktuelle ordrelinjen(e). Deretter blir det opprettet en lagerflytting for komponentene, og monteringsavgangen og ordreforsendelsen blir bokført. Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Lære mer om forskjellen mellom montering av varer rett før levering av salgsordrer og montering av varer som er ment for lagring.|[Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Fyll ut felt på lokasjonskort og i lageroppsett for å definere hvordan varene flyter til og fra monteringsavdelingen.|[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Tilpass en monteringsvare i henhold til en kundeforespørsel under salgsprosessen, konverter til salg når den er godtatt.|[Gi tilbud på et montere-til-ordre-salg](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombiner komponenter for å opprette en vare i en enkel prosess, til bestilling eller til lager.|[Montere elementer](assembly-how-to-assemble-items.md)|  
|Selg monteringsvarer som ikke er tilgjengelige for øyeblikket, ved å opprette koblet monteringsordre for å levere hele eller en del av ordreantallet.|[Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Når noen montere-til-ordre-varer allerede er på lager, kan du trekke dette antallet fra monteringsordren og reservere det fra beholdningen.|[Selge lagervarer i monter-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Når du selger monteringsvarer fra beholdningen og ikke alle varer er tilgjengelige, kan du starte en monteringsordre som automatisk forsyner en del av eller hele ordreantallet.|[Selge montere til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Opprett tilpassede monteringsvarer for rammeordrer før du med jevne mellomrom oppretter de faktiske ordrene i henhold til rammeordreavtalen.|[Opprette rammemonteringsordrer](assembly-how-to-create-blanket-assembly-orders.md)|
|Angre en bokført monteringsordre, for eksempel fordi ordren ble bokført med feil som må rettes.|[Angre monteringsbokføring](assembly-how-to-undo-assembly-posting.md)|
|Lære mer om forskjellen mellom monteringsstykklister og produksjonsstykklister og forskjeller i involverte prosesser.|[Arbeide med stykklister](inventory-how-work-BOMs.md)|
|Lær hvordan monteringsforbruk og avgang håndteres når du bokfører monteringsordrer og hvordan de avledede vare- og ressurskostnadene behandles og distribueres til finans.|[Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Arbeide med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
[Gjennomgang: planlegge forsyninger manuelt](walkthrough-planning-supplies-manually.md)  
[Gjennomgang: Selge, montere og levere sett](walkthrough-selling-assembling-and-shipping-kits.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
