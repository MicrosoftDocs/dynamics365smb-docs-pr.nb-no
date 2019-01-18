---
title: "Designdetaljer – Gjenbestillingsprinsipper | Microsoft-dokumentasjon"
description: Dette emnet gir en oversikt over policyer for etterfylling av varen.
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 4aaef129da953596632b56716eaff2f0c47736f7
ms.contentlocale: nb-no
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-reordering-policies"></a>Designdetaljer: Gjenbestillingsprinsipper
Gjenbestillingsprinsipper angir hvor mye som skal bestilles når varen må etterfylles. Det finnes fire forskjellige gjenbestillingsprinsipper.  

## <a name="fixed-reorder-qty"></a>Fast gjenbest.ant.
Prinsippet Fast gjenbest.ant. er knyttet til lagerplanlegging av vanlige C-varer (lav lagerkost, lav risiko for foreldelse og/eller mange varer). Dette prinsippet brukes vanligvis i forbindelse med et gjenbestillingspunkt som gjenspeiler forventet behov i løpet av leveringstiden for varen.  

### <a name="calculated-per-time-bucket"></a>Beregnet per tidsperiode  
 Hvis planleggingssystemet oppdager at gjenbestillingspunktet er nådd eller overskredet i en gitt tidsperiode (gjenbestillingssyklusen), over eller på gjenbestillingspunktet i begynnelsen av perioden og under eller på gjenbestillingspunktet på slutten av perioden, vil det foreslå å opprette en ny forsyningsordre med angitt bestillingsantall og planlegge det fremover fra den første datoen etter slutten av tidsperioden.  

 Begrepet om periodebasert gjenbestillingspunkt reduserer antall forsyningsforslag. Dette gjenspeiler den manuelle fremgangsmåten der du ofte går gjennom lageret for å sjekke det faktiske innholdet på de ulike hyllene.  

### <a name="creates-only-necessary-supply"></a>Oppretter bare nødvendig forsyning  
 Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om forsyningen allerede er bestilt for mottak i varens leveringstid. Hvis en eksisterende forsyningsordre vil løse problemet ved å bringer det beregnede beholdningen til eller over gjenbestillingspunktet i leveringstiden, vil ikke systemet foreslå en ny forsyningsordre.  

 Forsyningsordrer som utelukkende opprettes for å dekke et gjenbestillingspunkt, utelates fra vanlig forsyningsbalansering, og blir ikke på noen måte endret etterpå. Hvis en vare med gjenbestillingspunkt skal avvikles (ikke etterfylles), er det derfor tilrådelig å kontrollere utestående forsyningsordrer manuelt eller endre gjenbestillingsprinsippet for parti for parti. Da vil systemet redusere eller avbryte overflødig forsyning.  

### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
 Ordremodifikatorene Min. bestillingsantall, Maks. bestillingsantall og Bestillingsfaktor skal ikke spille en stor rolle når prinsippet Fast gjenbest.ant. brukes. Planleggingssystemet tar fremdeles hensyn til disse modifikatorene, og vil redusere antallet til det angitte maksimumsordreantallet (og opprette to eller flere forsyninger for å nå totalt ordreantall), øke ordren til det angitte minimumsordreantallet, eller runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
 Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om ordren er planlagt for en fridag, i henhold til kalendere som er definert i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

 Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdato. Dette kan resultere i en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller enkelte spesifikke behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.  

### <a name="should-not-be-used-with-forecast"></a>Bør ikke brukes med prognose  
 Siden det forventede behovet allerede er uttrykt i bestillingspunktnivået, er det ikke nødvendig å inkludere en prognose i planleggingen av en vare ved hjelp av et gjenbestillingspunkt. Hvis det er relevant å basere planen på en prognose, må du bruke parti for parti-prinsippet.  

### <a name="must-not-be-used-with-reservations"></a>Må ikke brukes med reservasjoner  
 Hvis brukeren har reservert et antall, for eksempel et antall på lager for fremtidig behov, vil planleggingsgrunnlaget forstyrres. Selv om det beregnede beholdningsnivået er akseptabelt i relasjon til gjenbestillingspunktet, er antallene kanskje ikke disponible. Systemet kan prøve å kompensere for dette ved å opprette unntaksordrer. Det anbefales imidlertid at Aldri angis for Reserver-feltet for varer som planlegges ved hjelp av et gjenbestillingspunkt.

## <a name="maximum-qty"></a>Maks.ant.
Maksimumsantall-prinsippet er en måte å opprettholde beholdningen på ved hjelp av et gjenbestillingspunkt.  

Alt for prinsippet Fast gjenbest.ant. gjelder også for dette prinsippet. Den eneste forskjellen er antallet i forsyningen som foreslås. Når du bruker prinsippet om maksimumsantall, defineres gjenbestillingsantallet dynamisk basert på det beregnede beholdningsnivået og varierer derfor vanligvis fra bestilling til bestilling.  

### <a name="calculated-per-time-bucket"></a>Beregnet per tidsperiode  
Gjenbestillingsantallet fastsettes på tidspunktet (slutten av en tidsperiode) der planleggingssystemet oppdager at gjenbestillingspunktet er overskredet. Systemet måler nå avstanden fra gjeldende beregnede beholdningsnivået opp til angitt maksimal lagerbeholdning. Dette utgjør antallet som må bestilles. Systemet kontrollerer deretter om forsyning allerede er bestilt et annet sted og kommer til å mottas innen leveringstiden, og i så fall reduseres antallet i den nye forsyningsordren med antallet som allerede er bestilt.  

Systemet sikrer at den beregnede beholdningen minst når gjenbestillingspunktet, i tilfelle brukeren har glemt å angi en maksimumsbeholdning.  

### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Avhengig av oppsettet kan det være best å kombinere prinsippet for maksimumsantall med ordremodifikatorer for å sikre et minimumsordreantall, runde det opp til et heltall innkjøpsenheter, eller dele den inn i flere partier som er definert av maksimumsordreantallet.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om ordren er planlagt for en fridag, i henhold til kalendere som er definert i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdato. Dette kan resultere i en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller enkelte spesifikke behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.

## <a name="order"></a>Bestilling
I et produser-til-ordre-miljø blir en vare utelukkende kjøpt eller produsert for å dekke et spesifikt behov. Vanligvis er dette knyttet til A-varer, og motivasjon for å velge gjenbestillingsprinsippet Ordre kan være at behovet er sjeldent, leveringstiden er ubetydelig eller de nødvendige attributtene varierer.  

Programmet oppretter en ordre-til-ordre-kobling, som fungerer som en innledende forbindelse mellom forsyningen, en forsyningsordre eller beholdning, og behovet det skal dekke.  

I tillegg til bruk av ordrepolicy, kan ordre-til-ordre-koblingen brukes under planleggingen på følgende måter:  

* Når produksjonsprinsippet Produser til ordre brukes til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre).  
* Når funksjonen Ordreplanlegging brukes til å opprette en produksjonsordre fra en ordre.  

Selv om et produksjonsselskap anser seg selv som et miljø som produser til ordrer, kan det være best å bruke gjenbestillingsprinsippet parti for parti hvis varene er helt standard uten variasjon i attributter. Resultatet blir at systemet bruker en endring i beholdningsnivået som ikke er planlagt, og akkumulerer bare ordrer med samme leveringsdato eller innenfor en angitt tidsperiode.  

### <a name="order-to-order-links-and-past-due-dates"></a>Odre-til-ordre-koblinger og tidligere forfallsdatoer  
I motsetning til de fleste sett med forsyning/behov planlegger systemet fullstendig for koblede ordrer med forfallsdatoer som kommer før den planlagte startdatoen. Forretningsårsaken til dette unntaket er at bestemte sett med behov/forsyning må synkroniseres helt frem til utførelse. Hvis du vil ha mer informasjon om den frosne sonen som gjelder de fleste behovs-/forsyningstyper, kan du se [Designdetaljer: Håndtere ordrer før den planlagte startdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Parti for parti
Prinsippet Parti for parti er det mest fleksible fordi systemet bare reagerer på faktisk behov, samt at det fungerer på forventet behov fra prognose og rammeordrer, og avklarer deretter ordreantallet basert på behovet. Prinsippet Parti for parti er rettet mot A- og B-varer der beholdningen kan godtas, men bør unngås.  

Parti for parti-prinsippet er på mange måter lik ordreprinsippet, men det har en generell tilnærming til varer. Det kan godta antall i beholdningen, og det samler behov og tilsvarende forsyning i tidsperioder som er angitt av brukeren.  

Tidsperioden defineres i **Tidsperiode**-feltet. Systemet fungerer med en minste tidsperiode på én dag, siden dette er den minste tidsenheten for behovs- og forsyningshendelser i systemet (men i praksis kan tidsenheten for produksjonsordrer og komponentbehov være sekunder).  

Tidsperioden setter også begrensninger på når en eksisterende forsyningsordre kan planlegges på nytt for å dekke et bestemt behov. Hvis forsyningen er innenfor tidsperioden, det vil bli planlagt på nytt inn eller ut for å dekke behovet. Hvis dette er tidligere, vil det føre til unødvendig oppbygging av beholdning og bør avbrytes. Hvis det er plassert senere, vil det opprettes en ny ordre i stedet.  

Med dette prinsippet er det også mulig å definere et sikkerhetslager for å kompensere for mulige svingninger i forsyning, eller for å dekke plutselig behov.  

Siden forsyningsordreantallet er basert på det faktiske behovet, kan det være fornuftig å bruke ordremodifikatorer: runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor (eller kjøpsenhet for mål), reduser ordren til angitt maksimumsantall, eller reduser antallet til angitt maksimumsantall (og opprett dermed to eller flere forsyninger for å nå det totale nødvendige antallet).

## <a name="see-also"></a>Se også  
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

