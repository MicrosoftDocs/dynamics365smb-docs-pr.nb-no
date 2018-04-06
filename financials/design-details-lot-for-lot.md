---
title: "Designdetaljer – Parti for parti | Microsoft-dokumentasjon"
description: "Lære hvordan du bruker parti for parti til å utligne ordreantall basert på behov."
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
ms.openlocfilehash: 2e0d1d18685f3395c31071ca9a2495c0091c564d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-lot-for-lot"></a>Designdetaljer: Parti for parti
Prinsippet Parti for parti er det mest fleksible fordi systemet bare reagerer på faktisk behov, samt at det fungerer på forventet behov fra prognose og rammeordrer, og avklarer deretter ordreantallet basert på behovet. Prinsippet Parti for parti er rettet mot A- og B-varer der beholdningen kan godtas, men bør unngås.  
  
Parti for parti-prinsippet er på mange måter lik ordreprinsippet, men det har en generell tilnærming til varer. Det kan godta antall i beholdningen, og det samler behov og tilsvarende forsyning i tidsperioder som er angitt av brukeren.  
  
Tidsperioden defineres i **Tidsperiode**-feltet. Systemet fungerer med en minste tidsperiode på én dag, siden dette er den minste tidsenheten for behovs- og forsyningshendelser i systemet (men i praksis kan tidsenheten for produksjonsordrer og komponentbehov være sekunder).  
  
Tidsperioden setter også begrensninger på når en eksisterende forsyningsordre kan planlegges på nytt for å dekke et bestemt behov. Hvis forsyningen er innenfor tidsperioden, det vil bli planlagt på nytt inn eller ut for å dekke behovet. Hvis dette er tidligere, vil det føre til unødvendig oppbygging av beholdning og bør avbrytes. Hvis det er plassert senere, vil det opprettes en ny ordre i stedet.  
  
Med dette prinsippet er det også mulig å definere et sikkerhetslager for å kompensere for mulige svingninger i forsyning, eller for å dekke plutselig behov.  
  
Siden forsyningsordreantallet er basert på det faktiske behovet, kan det være fornuftig å bruke ordremodifikatorer: runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor (eller kjøpsenhet for mål), reduser ordren til angitt maksimumsantall, eller reduser antallet til angitt maksimumsantall (og opprett dermed to eller flere forsyninger for å nå det totale nødvendige antallet).  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
