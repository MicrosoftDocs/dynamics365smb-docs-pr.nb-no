---
title: "Designdetaljer – Laste inn lagerprofiler | Microsoft-dokumentasjon"
description: "For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d2a2ee196be4562f62604afd4faed608ff07411f
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-loading-the-inventory-profiles"></a>Designdetaljer: Laste inn lagerprofiler
For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler.  

 De vanlige typene behov og forsyning med forfallsdatoer på eller etter den planlagte startdatoen lastes inn i hver beholdningsprofil. Når de er lastet inn, sorteres de ulike behovs og forsyningstypene i henhold til generelle prioriteter, for eksempel forfallsdato, lavnivåkoder, lokasjon og variant. I tillegg brukes ordreprioriteter på de forskjellige typene for å sikre at det viktigste behovet oppfylles først. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Prioritere ordrer](design-details-prioritizing-orders.md).  

 Behov kan også være negative, som nevnt tidligere. Dette betyr at det må behandles som forsyning. I motsetning til vanlige typer forsyning regnes imidlertid negativt behov som fast forsyning. Planleggingssystemet kan ta det med i betraktningen, men foreslår ingen endringer av det.  

 Planleggingssystemet tar vanligvis hensyn til alle forsyningsordrer etter den planlagte startdatoen som kan endres for å dekke behovet. Så snart et antall er bokført fra en ordre, kan den imidlertid ikke lenger endres av planleggingssystemet. Følgende forskjellige ordrer kan derfor ikke planlegges på nytt:  

-   Frigitte produksjonsordrer der forbruk eller avgang er bokført.  

-   Monteringsordre der forbruk eller avgang er bokført.  

-   Overføringsordrer der leveringen er bokført.  

-   Bestillinger der mottaket er bokført.  

 I tillegg til å laste inn behovs- og forsyningstyper, blir bestemte typer lastet inn med oppmerksomhet på spesialregler og avhengigheter som er beskrevet nedenfor.  

## <a name="item-dimensions-are-separated"></a>Varedimensjoner atskilles  
 Forsyningsplanen må beregnes per kombinasjon av varedimensjonene, for eksempel variant og lokasjon. Det er imidlertid ingen grunn til å beregne teoretisk kombinasjoner. Bare kombinasjonene som inneholder behov og/eller forsyning må beregnes.  

 Planleggingssystemet kontrollerer dette ved å kjøre gjennom beholdningsprofilen. Når det blir funnet en ny kombinasjon, oppretter programmet en intern kontrollpost som inneholder den faktiske kombinasjonsinformasjonen. Programmet setter inn LFEen som kontrollpost eller ytre løkke. Derfor angis riktige planleggingsparametre i henhold til en kombinasjon av variant og lokasjon, og programmet kan fortsette til den indre løkken.  

> [!NOTE]  
>  Programmet krever ikke at brukerne angir en LFE-post når de registrerer behov og/eller forsyning for en bestemt kombinasjon av variant og lokasjon. Hvis det ikke finnes en LFE for en bestemt kombinasjon, oppretter derfor programmet sin egen midlertidige LFE-post basert på varekortdataene. Hvis Lokasjon obligatorisk er satt til Ja i vinduet Lageroppsett, må du opprette en SKU, eller Komponenter ved lokasjon må være satt til Ja. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Behov på tom lokasjon](design-details-demand-at-blank-location.md).  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/partinumre lastes inn etter spesifikasjonsnivå  
 Attributter i form av serie-/ partinumre lastes inn i lagerprofiler sammen med behovet og forsyningen som de er tilordnet.  

 Behovs- og forsyningsattributter ordnes etter prioritet og spesifikasjonsnivå. Siden treff for serie-/partinumre gjenspeiler spesifikasjonsnivået, vil mer spesifikke behov, for eksempel et partinummer valgt spesielt for en salgslinje, søke samsvar før mindre spesifikke behov, for eksempel et salg fra et hvilken som helst valgt partinummer.  

> [!NOTE]  
>  Det finnes ingen egne prioriteringsregler for serie-/partinummerert behov og forsyning utenom spesifikasjonsnivået som defineres av kombinasjonen av serie- og partinumre for dem og varesporingsoppsettet for de involverte varene.  

 Under balansering betrakter planleggingssystemet forsyning med serie-/partinumre som ufleksibel, og vil ikke prøve å øke eller planlegge slike forsyningsordrer på nytt (med mindre de brukes i en ordre for ordre-relasjon). Se Ordre-til-ordre-koblinger brytes aldri). Dette beskytter forsyningen mot mottak av flere, kanskje motstridende, handlingsmeldinger når en forsyning har ulike attributter, for eksempel en samling med ulike serienumre.  

 En annen årsak til at serie-/partinummerert forsyning ikke er fleksible, et at serie-/partinumre vanligvis tilordnes så sent i prosessen at det kan være forvirrende hvis det foreslås endringer.  

 Balanseringen av serie-/partinumre tar ikke hensyn til den [frosne sonen](design-details-dealing-with-orders-before-the-planning-starting-date.md). Hvis behov og forsyning ikke er synkronisert, vil planleggingssystemet foreslå endringer eller foreslå nye ordrer, uavhengig av den planlagte startdatoen.  

## <a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-koblinger brytes aldri  
 Når en ordre-til-ordre-vare planlegges, kan ikke den koblede forsyningen brukes til noe annet behov enn det den opprinnelig var ment for. Det koblede behovet må ikke dekkes av en annen tilfeldig forsyning, selv om den er tilgjengelig i tid og antall i den aktuelle situasjonen. En monteringsordre som er koblet til en ordre i et monter-til-ordre-scenario, kan for eksempel ikke brukes til å dekke andre behov.  

 Ordre-til-ordre-behov og -forsyning må være i nøyaktig balanse. Planleggingssystemet sikrer forsyningen under alle omstendigheter uten å ta hensyn til ordreskaleringsparametere, modifikatorer og antall på lager (bortsett fra antall knyttet til de koblede ordrene). Av samme årsak vil systemet foreslå å redusere overflødige forsyninger hvis det koblede behovet reduseres.  

 Denne balanseringen påvirker også tidsberegningen. Det tas ikke hensyn til den begrensede horisonten som gis av tidsperioden. Forsyningen tidsplanlegges på nytt hvis tidsberegningen for behovet er endret. Avdempningstiden blir overholdt, og denne hindrer at ordre-til-ordre-forsyninger planlegges ut, med unntak av interne forsyninger for en flernivås produksjonsordre (prosjektordre).  

> [!NOTE]  
>  Serie-/partinumre kan også angis i ordre-til-ordre-behov. I slike tilfeller betraktes ikke forsyningen som ufleksible som standard, noe som vanligvis er tilfelle for serie-/partinumre. I slike tilfeller vil systemet øke/redusere i henhold til behovsendringer. Hvis ett behov har varierende serie-/partinumre tall, for eksempel flere partinumre, foreslås også én forsyningsordre per parti.  

> [!NOTE]  
>  Prognoser skal ikke føre til oppretting av forsyningsordrer som er bundet av en ordre-til-ordre-kobling. Hvis prognosen brukes, bør den bare brukes som en generator for konkrete behov i et produksjonsmiljø.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov blir lastet inn i henhold til produksjonsordreendringer  
 Ved håndtering av produksjonsordrer må planleggingssystemet overvåke de nødvendige komponentene før det laster dem inn i behovsprofilen. Komponentlinjer som skyldes en endret produksjonsordre erstatter linjene i den opprinnelige ordren. Dette betyr at planleggingssystemet sikrer at planleggingslinjer for komponentbehov aldri blir duplisert.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Sikkerhetslager kan forbrukes  
 Sikkerhetslagerantallet er først og fremst en behovstype og lastes derfor inn i beholdningsprofilen på den planlagte startdatoen.  

 Sikkerhetslager er et lagerantall som er lagt til side for å kompensere for usikkerheter i behovet i etterfyllingsleveringstiden. Dette kan imidlertid brukes hvis det er nødvendig å ta fra det å oppfylle et behov. I slike tilfeller sikrer planleggingssystemet at sikkerhetslageret raskt erstattes, ved å foreslå en forsyningsordre for å etterfylle sikkerhetslagerantallet på datoen den forbrukes. Denne planleggingslinjen viser et unntaksadvarselsikon som informerer planleggeren om at sikkerhetslageret er delvis eller helt forbrukt med en unntaksordre for det manglende antallet.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognosebehov blir redusert av ordrer  
 Produksjonsprognosen uttrykker forventet fremtidig behov. Når faktisk behov registreres, vanligvis som ordrer for produserte varer, forbruker det prognosen.  

 Selve prognosen reduseres faktisk ikke av ordrer. Den forblir den samme. Prognoseantallet som brukes i planleggingsberegningen, blir imidlertid redusert (med salgsordreantall) før det gjenværende antallet, hvis det finnes, registreres i beholdningsprofilen for behov. Når planleggingssystemet undersøker faktisk salg i en periode, blir både åpne ordrer og vareposter fra leverte salg tatt med, med mindre de er avledet fra en rammeordre.  

 Det kreves at en bruker angir en gyldig prognoseperioden. Datoen på prognoseantallet angir begynnelsen på perioden, og datoen på neste prognose angir slutten av perioden.  

 Prognosen for perioder før planleggingsperioden brukes ikke, uavhengig av om den ble forbrukt eller ikke. Det første prognosetallet av interesse er enten samme dato som den planlagte startdatoen eller nærmeste dato før den planlagte startdatoen.  

 Prognosen kan være for uavhengig behov, for eksempel ordrer, eller avhengig behov, for eksempel produksjonsordrekomponenter (modulprognose). En vare kan ha begge typer prognoser. Under planleggingen foregår forbruket separat, først for uavhengige behov og deretter for avhengige behov.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammebestillingsbehov blir redusert av ordrer  
 Prognosen suppleres av rammeordren som et middel for å angi fremtidige behov fra en bestemt kunde. Som med prognosen (uspesifisert), må faktisk salg bruke den forventede etterspørselen, og det gjenværende antallet bør angi beholdningsprofilen for behov. Forbruket reduserer ikke rammebestillingen.  

 Planleggingsberegningen tar hensyn til åpne ordrer som er knyttet til den bestemte rammeordrelinjen, men tar ikke hensyn til gyldige tidsperioder. Det tas heller ikke hensyn til bokførte ordrer, siden bokføringen allerede har redusert det utestående rammeordreantallet.  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
 [Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
 [Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)

