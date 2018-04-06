---
title: Konfigurere produksjonsprosesser | Microsoft-dokumentasjon
description: "Hvis du vil konvertere materiale til produserte sluttvarer, må du definere produksjonsressursene, for eksempel stykkliste, rutinger, maskinoperatører og maskiner, i systemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f2d95dbb6d0336286f0fb657028970ce8a04cfda
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-manufacturing"></a>Definere produksjon
Hvis du vil konvertere materiale til produserte sluttvarer, må du definere produksjonsressursene, for eksempel stykkliste, rutinger, maskinoperatører og maskiner, i systemet.

Operatører og maskiner er representert i systemet som produksjonsressurser som kan organiseres i arbeidssentre og arbeidssentergrupper. Når disse ressursene er opprettet, kan de fylles med operasjoner i henhold til varens definerte materialstruktur (stykkliste) og prosesstruktur (ruting), og i henhold til produksjonsressurs- eller arbeidssenterkapasitet. Du kan også angi produksjonskapasitet for hver enkelt ressurs. Kapasitet defineres av tilgjengelig arbeidstid for produksjonsressurser og arbeidssentre, og styres av kalendere for hvert nivå. En arbeidssenterkalender angir virkedager eller arbeidstimer, skift, ferier og fravær, som igjen angir arbeidssenterets disponible kapasitet (vanligvis målt i minutter). Alt dette bestemmes av definerte effektivitets- og kapasitetsverdier.  

Når du har definert produksjonen, kan du planlegge og kjøre produksjonsordrer. Hvis du vil ha mer informasjon, kan du se [Planlegging](production-planning.md) og [Produksjon](production-manage-manufacturing.md).  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Konfigurere produksjonsfunksjoner, for eksempel definere produksjonsarbeidstimer og velge planleggingsprinsipper.|Siden **Produksjonsoppsett**.|  
|Definere en standard arbeidsuke i produksjonsavdelingen basert på start- og sluttidspunkt for hver virkedag samt relatert skiftarbeid.|[Opprette produksjonskalendere](production-how-to-create-work-center-calendars.md)|  
|Organiser faste verdier og krav for produksjonsressurser som arbeidssentre eller produksjonsressurser for å styre produksjonsavgangen eller produksjonen som utføre.|[Konfigurere arbeidssentre og produksjonsressurser](production-how-to-set-up-work-and-machine-centers.md)|
|Organiser produksjonsoperasjoner i nødvendig rekkefølge, og tilordne dem til arbeids- eller produksjonsressurser med nødvendige arbeidstidene.|[Opprette ruter](production-how-to-create-routings.md)|
|Organiser produksjonskomponenter eller delmonteringer under en overordnet produsert vare, og sertifiser stykklisten for kjøring i arbeidssentre.|[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)|
|Kontroller at riktig komponentantall er tilgjengelig når produserte varer lagerføres i én enhet, men produseres i en annen.|[Arbeide med produksjonsbunkeenhet](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definere familier av produksjonsvarer med like produksjonsprosesser for å spare forbruk. For eksempel kan fire enheter av samme vare produseres fra ett ark, samtidig med 10 enheter av en annen, forskjellig vare.|[Arbeide med produksjonsfamilier](production-how-work-family.md)|
|Bruk standardoppgaver til å forenkle opprettingen av ruter ved å knytte tilleggsinformasjon til gjentakende operasjoner raskt.|[Definere standard rutelinjer](production-how-set-up-standard-routing-lines.md)|  
|Kjargjør arbeidssentre og ruter til å representere underleveranse-produksjonsoperasjoner.|[Underleveranse av produksjon](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Se også
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

