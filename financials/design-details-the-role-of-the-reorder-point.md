---
title: "Designdetaljer – Rollen til gjenbestillingspunktet | Microsoft-dokumentasjon"
description: "Dette emnet belyser viktigheten av å angi et gjenbestillingspunkt, slik at du vet når du må bestille mer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-the-role-of-the-reorder-point"></a>Designdetaljer: Rollen til gjenbestillingspunktet
I tillegg til generell balansering av tilbud og etterspørsel må systemet også overvåke lagernivåer for de berørte varene for å overholde angitte gjenbestillingsprinsipper.  
  
Et gjenbestillingspunkt representerer etterspørselen i løpet av leveringstiden. Når den beregnede beholdningen går under lagernivået som defineres av gjenbestillingspunktet, er det på tide å bestille mer. I mellomtiden forventes det at beholdningen gradvis reduseres og kanskje blir null (eller sikkerhetslagernivået) til etterfyllingen kommer.  
  
Planleggingssystemet vil foreslå en fremoverplanlagt forsyningsordre når den forventede beholdning blir lavere enn gjenbestillingspunktet.  
  
Gjenbestillingspunktet gjenspeiler et bestemt beholdningsnivå. Lagernivåer kan imidlertid endre seg betydelig i tidsperioden, og planleggingssystemet må derfor konstant overvåke beregnet disponibel beholdning.  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
