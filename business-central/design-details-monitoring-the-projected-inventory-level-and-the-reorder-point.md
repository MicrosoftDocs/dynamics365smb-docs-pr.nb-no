---
title: "Designdetaljer – Overvåke forventet lagernivå og gjenbestillingspunkt | Microsoft-dokumentasjon"
description: "Lær hvordan lagerplanlegging skiller mellom forventet lagernivå og forventet disponibelt lagernivå."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ee71f3c0a677115bba920e4b6d25eee6342e87e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Designdetaljer: Overvåke forventet lagernivå og gjenbestillingspunkt
Beholdning er en type forsyning, men for lagerplanlegging skiller planleggingssystemet mellom to lagernivåer:  

* Beregnet beholdning  
* Forventet disponibel beholdning  

## <a name="projected-inventory"></a>Beregnet lager  
I utgangspunktet er den beregnede beholdningen antallet bruttobeholdning, inkludert forsyning og behov i fortiden, selv om det ikke er bokført, når du starter planleggingen. I fremtiden blir dette et glidende beregnet beholdningsnivå som vedlikeholdes av bruttoantallene fra fremtidig forsyning og behov, fordi de innføres langs tidslinjen (reservert eller tildelt på andre måter).  

Den beregnede beholdningen brukes av planleggingssystemet til å overvåke gjenbestillingspunktet, og til å bestemme gjenbestillingsantallet når gjenbestillingsprinsippet Maks.ant. brukes.  

## <a name="projected-available-inventory"></a>Forventet disponibel beholdning  
Den forventede disponible beholdningen er delen av den beregnede beholdningen som på et gitt tidspunkt er disponibelt for å dekke behov. Den forventede disponible beholdningen brukes av planleggingsmotoren ved overvåking av sikkerhetslagernivået.  

Den forventede disponible beholdningen brukes av planleggingssystemet til å overvåke sikkerhetslagernivået, siden sikkerhetslageret alltid må være disponibelt for å dekke uventet behov.  

## <a name="time-buckets"></a>Tidsperioder  
Det er svært viktig å ha god kontroll over det beregnede lagernivået for å oppdage når gjenbestillingspunktet nås eller overskrides og for å beregne riktig ordreantall gjenbestillingsprinsippet Maks.ant. brukes.  

Som nevnt tidligere, blir forventet lagernivå beregnet ved starten av planleggingsperioden. Det er et bruttonivå som ikke tar hensyn til reservasjoner og lignende fordelinger. For å overvåke dette beholdningsnivået i løpet av planleggingssekvensen overvåker systemet de aggregerte endringene gjennom en tidsperiode. Systemet sikrer at tidsperioden er minst én dag, siden dette er den mest nøyaktige tidsenheten for en behovs- eller forsyningshendelse.  

## <a name="determining-the-projected-inventory-level"></a>Fastslå forventet beholdningsnivå  
Følgende sekvens beskriver hvordan det forventede beholdningsnivået fastsettes:  

* Når en forsyningshendelse, for eksempel en bestilling er helt planlagt, økes den beregnede beholdningen på forfallsdatoen.  
* Når en behovshendelse er fullstendig dekket, reduserer den ikke den beregnede beholdningen med en gang. I stedet bokføres en reduksjonspåminnelse, som er en intern post som inneholder dato og antall for bidrag til den beregnede beholdningen.  
* Når en påfølgende forsyningshendelse planlegges og plasseres på tidslinjen, undersøkes de bokførte reduksjonspåminnelsene enkeltvis frem til den planlagte datoen for forsyningen samtidig som den beregnede beholdningen oppdateres. Under denne prosessen kan det hende at gjenbestillingspunktnivået for påminnelsen om intern økning nås eller passeres.  
* Hvis en ny forsyningsordre blir introdusert, kontrollerer systemet om det er angitt før gjeldende forsyning. Hvis det er tilfelle, blir den nye forsyningen gjeldende forsyning og balanseringen starter på nytt.  

Nedenfor vises en grafisk illustrasjon av dette prinsippet:  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. Forsyning **Sa** med 4 (fast) lukker behov **Da** med -3.  
2. CloseDemand: Opprett en reduksjonspåminnelse med verdien -3 (vises ikke).  
3. Forsyning **Sa** lukkes med et overskudd på 1 (det finnes ikke mer behov).  

     Dermed økes det beregnede beholdningsnivået til + 4, mens den forventede **disponible** beholdningen blir -1.  

4. Den neste forsyningen **Sb** 2 (en annen ordre) er allerede plassert på tidslinjen.  
5. Systemet kontrollerer om det kommer en reduksjonspåminnelse før **Sb** (det gjør det ikke, så ingen handling utføres).  
6. Systemet lukker forsyning **Sb** (det finnes ikke mer behov), ved å A: redusere den til 0 (annullere) eller B: la den være som den er.  

     Dette øker det beregnede beholdningsnivået (A: +0 => +4 eller B: +2 = +6).  

7. Systemet foretar en sluttkontroll: Finnes det noen reduksjonspåminnelse? Ja, det er en på datoen for **Da**.  
8. Systemet legger til reduksjonspåminnelsen på -3 i det beregnede beholdningsnivået, enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I A-tilfeller oppretter systemet en fremoverplanlagt ordre på datoen **Da**.  

     I B-tilfeller nås gjenbestillingspunktet, og det opprettes en ny ordre.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

