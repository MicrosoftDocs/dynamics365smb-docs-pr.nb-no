---
title: "Designdetaljer – Håndtere gjenbestillingsprinsipper | Microsoft-dokumentasjon"
description: "Oversikt over oppgaver for å definere en gjenbestillingspolicy ved forsyningsplanlegging."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b273dedd269d8b86ba4fa7a9d9540c44b701a97e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

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
