---
title: Forsyningsplanlegging| Microsoft-dokumentasjon
description: "Forbered en detaljert og utførbar plan og produksjonsplan for sluttmontering for salgs- og produksjonsbehov."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 849ea09fb84e2cf52971b582920debf89ca7c2b0
ms.contentlocale: nb-no
ms.lasthandoff: 11/22/2018

---
# <a name="planning"></a>Planlegging
Produksjonsoperasjonene som kreves for å transformere tilgang til ferdigvarer, må planlegges daglig eller ukentlig, avhengig av produktenes volum og beskaffenhet. [!INCLUDE[d365fin](includes/d365fin_md.md)] har funksjoner for å dekke forventet og faktisk behov fra salg, montering og produksjon, i tillegg til funksjoner for distribusjonsplanlegging ved hjelp av lagerføringsenheter og lokasjonsoverføringer.

> [!NOTE]
> Dette emnet beskriver hovedsakelig planlegging for selskaper som er involvert i produksjons- eller monteringsstyring der de resulterende forsyningsordrene kan være produksjon, montering, overføring eller bestillinger. Hovedgrensesnittet for dette planleggingsarbeidet er siden **Planleggingsforslag**.

> [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter også forsyningsplanlegging for engrosselskaper der de resulterende forsyningsordrene bare kan være overføringsordrer og bestillinger. Hovedgrensesnittet for dette planleggingsarbeidet er siden **Bestillingsforslaget**, som beskrives indirekte i dette emnet siden det meste av planleggingsfunksjonaliteten gjelder for begge forslag.

Før du kan planlegge og utføre produksjonsordrer, må du konfigurere produksjonskapasitet, for eksempel opprette produksjonskalendere, ruter, produksjonsstykklister og produksjonsressurser. Hvis du vil ha mer informasjon, kan du se [Definere produksjon](production-configure-production-processes.md).

Planlegging kan ses på som nødvendig klargjøring for forsyningsordrene i produksjons- eller produksjonsavdelingene for å dekke behovet. Hvis du vil ha mer informasjon, kan du se [Monteringsstyring](assembly-assemble-items.md) og [Produksjon](production-manage-manufacturing.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Få en kort innføring i hvordan planleggingssystemet kan brukes til å avdekke og prioritere behov og foreslå en konsolidert, balansert forsyningsplan for MPS eller MRP.|[Om planleggingsfunksjonalitet](production-about-planning-functionality.md)|
|Forstå hvordan alle aspekter av planleggingssystemet fungerer, og hvordan du justerer algoritmer for å oppfylle krav i forskjellige miljøer.|[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)|
|Lære hvordan planleggingslogikken skiller mellom behov i lokasjoner i henhold til LFE-oppsettet, og behov uten lokasjonskoder.|Se [Planlegge med/uten lokasjoner](production-planning-with-without-locations.md).|
|Prognose for behov presentert av forventede salgs- og produksjonskomponenter.|[Opprette en behovsprognose](production-how-to-create-a-forecast.md)|  
|Opprette én-til-én-produksjonsordrer automatisk fra en ordre for å dekke det nøyaktige behovet for den aktuelle ordrelinjen.|[Opprette produksjonsordrer fra ordrer](production-how-to-create-production-orders-from-sales-orders.md)|
|Opprette en prosjektproduksjonsordre direkte fra en flerlinjers ordre som representerer et produksjonsprosjekt.|[Planlegge prosjektordrer](production-how-to-plan-project-orders.md)|
|Bruk **Ordreplanlegging**-siden til manuell planlegging av salgs- eller produksjonsbehov ett produksjonsstykklistenivå om gangen.|[Planlegge for nytt behov bestilling for bestilling](production-how-to-plan-for-new-demand.md)|
|Bruk siden **Planleggingsforslag** til å kjøre både MPS- og MRP-alternativet for automatisk å opprette en forsyningsplan på høyt nivå eller en detaljert forsyningsplan på alle varenivåer.|[Kjøre full planlegging, MPS eller MRP](production-how-to-run-mps-and-mrp.md)|
|Kjøre bestillingsforslaget for automatisk å opprette en detaljert forsyningsplan for å dekke behovet for varer som bare etterfylles ved hjelp av kjøp eller overføring.|**Bestillingsforslag**-siden|  
|Opprette eller oppdatere en produksjonsordre som grovplanlagte operasjoner i hovedproduksjonsplanen.|[Planlegge på nytt eller fornye produksjonsordrer direkte](production-how-to-replan-refresh-production-orders.md)|
|Omberegne arbeidssenter- eller produksjonsressurskalendere som følge av planleggingsendringer.|Delen Beregne en arbeidssenterkalender i [Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md)|
|Spore ordrebehovet (sporet antall), prognosen, rammebestillingen eller planleggingsparameteren (ikke-sporet antall) som har forårsaket den aktuelle planleggingslinjen.|[Spore relasjoner mellom behov og forsyning](production-how-track-demand-supply.md)|
|Vise en vares anslåtte disponible beholdning etter ulike visninger og se hvordan den påvirkes over tid av bruttobehov, planlagte ordremottak og annet.|[Vise tilgjengeligheten av varer](inventory-how-availability-overview.md)|  
|Utfør valgte planleggingsaktiviteter, for eksempel endre eller legge til planleggingsforslagslinjer, i en grafisk visning av forsyningsplanen.|[Endre planleggingsforslag i en grafisk visning](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Se også
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

