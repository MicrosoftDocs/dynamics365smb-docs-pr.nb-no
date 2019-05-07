---
title: Designdetaljer – Rollen til gjenbestillingspunktet | Microsoft-dokumentasjon
description: Dette emnet belyser viktigheten av å angi et gjenbestillingspunkt, slik at du vet når du må bestille mer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 836da35166d947de8c37128d9ed8807914594c55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "924190"
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
