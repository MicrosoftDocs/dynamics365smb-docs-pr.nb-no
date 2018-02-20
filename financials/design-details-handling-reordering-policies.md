---
title: "Designdetaljer – Håndtere gjenbestillingsprinsipper | Microsoft-dokumentasjon"
description: "Oversikt over oppgaver for å definere en gjenbestillingspolicy ved forsyningsplanlegging."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a>Designdetaljer: Håndtere gjenbestillingsprinsipper
Det må angis et gjenbestillingsprinsipp for at en vare skal kunne delta i forsyningsplanlegging. Det finnes fire gjenbestillingsprinsipper:  
  
* Fast gjenbest.ant.  
* Maks.ant.  
* Bestilling  
* Parti for parti  
  
Prinsippene Fast gjenbest.ant., og Maks.ant. som er relatert til lagerplanlegging. Selv om lagerplanlegging teknisk sett er enklere enn fremgangsmåten for balansering, må disse policyene eksistere sammen med trinnvise balansering av forsynings- og ordresporing. For å styre integrasjonen mellom dem og gi innsikt i planleggingslogikken som er involvert, finnes det strenge regler som bestemmer hvordan gjenbestillingsprinsipper skal håndteres.  
  
## <a name="in-this-section"></a>I denne delen  
[Designdetaljer: Rollen til gjenbestillingspunktet](design-details-the-role-of-the-reorder-point.md)  
[Designdetaljer: Overvåke forventet lagernivå og gjenbestillingspunkt](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[Designdetaljer: Rollen til tidsperioden](design-details-the-role-of-the-time-bucket.md)  
[Designdetaljer: Holde seg under overflytnivået](design-details-staying-under-the-overflow-level.md)  
[Designdetaljer: Håndtere forventet negativ lagerbeholdning](design-details-handling-projected-negative-inventory.md)  
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
