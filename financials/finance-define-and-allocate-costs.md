---
title: Definere og fordele kostnader | Microsoft-dokumentasjon
description: "Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Du kan definere så mange fordelinger som du trenger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 04e5a95b7a926528cc26c254390d08e3bce6ad8a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a>Definere og fordele kostnader
Kostfordelinger flytter kostnader og inntekter mellom kosttyper, kostsentre og kostobjekter. Du kan definere så mange fordelinger som du trenger. Hver fordeling består av:  

-   En fordelingskilde.  
-   Ett eller flere tildelingsmål.  

Fordelingskilde fastsetter hvilke kostnader må fordeles, og fordelingsmålene avgjør hvor kostnadene må fordeles. En fordelingskilde kan for eksempel være kostnadene for kostnadstypen Elektrisitet og oppvarming. Du tilordner alle elektrisitets- og oppvarmingskostnader til tre kostsentre: Workshop, Produksjon og Salg. Disse kostsentrene er fordelingsmålene dine.  

For hver fordelingskilde kan du definere du et fordelingsnivå, en gyldighetsperiode og en variant som grupperingsidentifikator. Du kan bruke en kjørsel til å definere filtre for å velge fordelingsdefinisjoner, og deretter kjøre kostfordelinger automatisk.  

For hvert fordelingsmål kan du definere et fordelingsgrunnlag. Fordelingsgrunnlaget kan være statisk eller dynamisk.  

-   Statiske fordelingsgrunnlag er basert på en bestemt verdi, for eksempel kvadratmeter eller et fastsatt fordelingsforhold, for eksempel 5:2:4.  
-   Grunnlaget for dynamisk fordeling avhenger av verdier som kan endres, for eksempel antall ansatte i et kostsenter eller salgsinntekten av et kostobjekt i løpet av en bestemt tidsperiode.  

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

|Til|Se|  
|--------|---------|  
|Definere fordelingskilde og kildens mål.|[Definere fordelingskilde og -mål](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Definere ulike filtre for dynamiske fordelingsgrunnlag.|[Angi filtre for dynamisk fordelingsgrunnlag](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Se et eksempel på hvordan du definerer en statisk fordeling.|[Eksempelscenario: Definere statiske fordelinger basert på fordelingsgrad](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Se et eksempel på hvordan du definerer en dynamisk fordeling.|[Eksempelscenario: Definere dynamiske fordelinger basert på solgte varer](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Se også  
 [Definere kost.regnskap](finance-set-up-cost-accounting.md)   
 [Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md)   
 [Gjøre rede for kostnader](finance-manage-cost-accounting.md)   
 [Terminologi i kostregnskap](finance-terminology-in-cost-accounting.md)   
 [Om kostregnskap](finance-about-cost-accounting.md)

