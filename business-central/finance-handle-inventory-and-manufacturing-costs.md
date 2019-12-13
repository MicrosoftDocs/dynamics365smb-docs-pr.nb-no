---
title: Håndtere lager- og produksjonskost | Microsoft-dokumentasjon
description: Selv om mange av funksjonene for kostredegjøring er uttrykt i underliggende prosesser uten brukerhandling, for eksempel postutligning og automatisk kostjustering, er mange felt, sider og rapporter rettet inn mot brukere som direkte eller indirekte håndterer vare- eller driftskost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8eceae6e325d4b5c1cf5cc4b0ba509c4624dd9f4
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879779"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Håndtere lager- og produksjonskost
Selv om mange av funksjonene for kostredegjøring er uttrykt i underliggende prosesser uten brukerhandling, for eksempel postutligning og automatisk kostjustering, er mange felt, sider og rapporter rettet inn mot brukere som direkte eller indirekte håndterer vare- eller driftskost.  

 Tilordning av varegebyrer til kjøpsdokumenter er et eksempel på en indirekte kostredegjørelsesoppgave. Oppdatering av enhetskost for en monterings- eller produksjonsstykklistevare er et eksempel på en mer direkte kostredegjørelsesoppgave.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Jevnlig eller automatisk oppdatere enhetskost for én eller flere varer for å videreføre eventuelle kostendringer fra inngående poster, for eksempel poster for kjøp eller produksjonsresultat, til de relaterte utgående postene, for eksempel forbruk eller overføring.|[Justere varekost](inventory-how-adjust-item-costs.md)|  
|Få innsikt i dynamikken for gjennomsnittskost for å ta prisavgjørelser eller spore kostendringer som skyldes feil i dataregistreringen.|[Registrere nye varer](inventory-how-register-new-items.md)|  
|Opprette standardkost for en produksjonsvare ved å registrere de tre kostelementene: materialkost, kapasitetskost og underleverandørkost.|[Om beregning av standardkost](finance-about-calculating-standard-cost.md)|  
|Beregne enhetskost for en stykklistevare basert på enhetskost for de underliggende komponentene.|[Arbeide med stykklister](inventory-how-work-BOMs.md)|  
|Fullføre livssyklusen for kostberegning for en produsert vare ved å justere kost og avstemme verdipostene mot Finans.|[Om fullførte produksjonsordrekostnader](finance-about-finished-production-order-costs.md)|  
|Endre verdien for en vare på lager eller verdien for en varepost, for eksempel en kjøpstransaksjon.|[Revaluere beholdning](inventory-how-revalue-inventory.md)|
|Manuelt angre en vareutligning eller utligne vareposter som er opprettet i programmet, på nytt.|[Fjerne varefinansposter og utligne dem på nytt](finance-how-to-remove-and-reapply-item-entries.md)|  
|Bruk feltet **Utlignet fra-post** i varekladden til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen.|[Lukke åpne vareposter som er resultat av fast utligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Se også  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)
