---
title: "Designdetaljer – Fast gjenbest.ant. | Microsoft-dokumentasjon"
description: "Prinsippet Fast gjenbest.ant. er knyttet til lagerplanlegging av vanlige C-varer (lav lagerkost, lav risiko for foreldelse og/eller mange varer). Dette prinsippet brukes vanligvis i forbindelse med et gjenbestillingspunkt som gjenspeiler forventet behov i løpet av leveringstiden for varen."
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
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5084c8a49972ea51600867d90acedc2698609732
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-fixed-reorder-qty"></a>Designdetaljer: Fast gjenbest.ant.
Prinsippet Fast gjenbest.ant. er knyttet til lagerplanlegging av vanlige C-varer (lav lagerkost, lav risiko for foreldelse og/eller mange varer). Dette prinsippet brukes vanligvis i forbindelse med et gjenbestillingspunkt som gjenspeiler forventet behov i løpet av leveringstiden for varen.  

## <a name="calculated-per-time-bucket"></a>Beregnet per tidsperiode  
 Hvis planleggingssystemet oppdager at gjenbestillingspunktet er nådd eller overskredet i en gitt tidsperiode (gjenbestillingssyklusen), over eller på gjenbestillingspunktet i begynnelsen av perioden og under eller på gjenbestillingspunktet på slutten av perioden, vil det foreslå å opprette en ny forsyningsordre med angitt bestillingsantall og planlegge det fremover fra den første datoen etter slutten av tidsperioden.  

 Begrepet om periodebasert gjenbestillingspunkt reduserer antall forsyningsforslag. Dette gjenspeiler den manuelle fremgangsmåten der du ofte går gjennom lageret for å sjekke det faktiske innholdet på de ulike hyllene.  

## <a name="creates-only-necessary-supply"></a>Oppretter bare nødvendig forsyning  
 Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om forsyningen allerede er bestilt for mottak i varens leveringstid. Hvis en eksisterende forsyningsordre vil løse problemet ved å bringer det beregnede beholdningen til eller over gjenbestillingspunktet i leveringstiden, vil ikke systemet foreslå en ny forsyningsordre.  

 Forsyningsordrer som utelukkende opprettes for å dekke et gjenbestillingspunkt, utelates fra vanlig forsyningsbalansering, og blir ikke på noen måte endret etterpå. Hvis en vare med gjenbestillingspunkt skal avvikles (ikke etterfylles), er det derfor tilrådelig å kontrollere utestående forsyningsordrer manuelt eller endre gjenbestillingsprinsippet for parti for parti. Da vil systemet redusere eller avbryte overflødig forsyning.  

## <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
 Ordremodifikatorene Min. bestillingsantall, Maks. bestillingsantall og Bestillingsfaktor skal ikke spille en stor rolle når prinsippet Fast gjenbest.ant. brukes. Planleggingssystemet tar fremdeles hensyn til disse modifikatorene, og vil redusere antallet til det angitte maksimumsordreantallet (og opprette to eller flere forsyninger for å nå totalt ordreantall), øke ordren til det angitte minimumsordreantallet, eller runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor.  

## <a name="combines-with-calendars"></a>Kombinerer med kalendere  
 Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om ordren er planlagt for en fridag, i henhold til kalendere som er definert i feltet **Hovedkalenderkode** i vinduene **Selskapsopplysninger** og **Lokasjonskort**.  

 Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdato. Dette kan resultere i en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller enkelte spesifikke behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.  

## <a name="should-not-be-used-with-forecast"></a>Bør ikke brukes med prognose  
 Siden det forventede behovet allerede er uttrykt i bestillingspunktnivået, er det ikke nødvendig å inkludere en prognose i planleggingen av en vare ved hjelp av et gjenbestillingspunkt. Hvis det er relevant å basere planen på en prognose, må du bruke parti for parti-prinsippet.  

## <a name="must-not-be-used-with-reservations"></a>Må ikke brukes med reservasjoner  
 Hvis brukeren har reservert et antall, for eksempel et antall på lager for fremtidig behov, vil planleggingsgrunnlaget forstyrres. Selv om det beregnede beholdningsnivået er akseptabelt i relasjon til gjenbestillingspunktet, er antallene kanskje ikke disponible. Systemet kan prøve å kompensere for dette ved å opprette unntaksordrer. Det anbefales imidlertid at Aldri angis for Reserver-feltet for varer som planlegges ved hjelp av et gjenbestillingspunkt.  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
 [Designdetaljer: Maks.ant.](design-details-maximum-qty.md)   
 [Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
 [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

