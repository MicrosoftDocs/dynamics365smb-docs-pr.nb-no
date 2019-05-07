---
title: Designdetaljer – Prioritere ordrer | Microsoft-dokumentasjon
description: Les mer om hvordan du prioriterer for å dekke både behov og forsyningskrav.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 06eb5221369d8777330ae844adfb5d87658d591d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "924213"
---
# <a name="design-details-prioritizing-orders"></a>Designdetaljer: Prioritere ordrer
I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i neste uke. I tillegg til denne generelle prioriteten vil planleggingssystemet også foreslå hvilken type behov som må være oppfylt før andre behov oppfylles. Det vil foreslå hvilken forsyningskilde som skal brukes før du bruker andre forsyningskilder. Dette gjøres i henhold til ordreprioriteter.  

Innlastet behov og forsyning bidrar til en profil for den beregnede beholdningen i henhold til følgende prioriteter:  

## <a name="priorities-on-the-demand-side"></a>Prioriteter på behovssiden  
1. Allerede levert: Varepost  
2. Bestillingsretur  
3. Ordre  
4. Serviceordre  
5. Produksjonskomponentbehov  
6. Monteringsordrelinje  
7. Utgående overføringsordre  
8. Rammebestilling (som ikke allerede er brukt av tilknyttede salgsordrer)  
9. Prognose (som ikke allerede er brukt av andre salgsordrer)  

> [!NOTE]  
>  Bestillingsreturer tas vanligvis ikke med i forsyningsplanlegging. De skal alltid reserveres fra partiet som skal returneres. Hvis den ikke er reservert, spiller bestillingsreturer en rolle i tilgjengeligheten og er høyt prioritert for å unngå at planleggingssystemet foreslår at en forsyningsordre bare skal fungere som en bestillingsretur.  

## <a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden  
1. Allerede på lager: Varepost (planleggingsfleksibilitet = ingen)  
2. Ordreretur (Planleggingsfleksibilitet = Ingen)  
3. Inngående overføringsordre  
4. Produksjonsordre  
5. Monteringsordre  
6. Bestilling  

## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet som er knyttet til statusen for behov og forsyning  
I tillegg til prioriteter som er angitt av behov og forsyning, definerer den nåværende ordretilstanden i utføringsprosessen, en prioritet. Lageraktiviteter har for eksempel innvirkning, og det tas hensyn til statusen for salgs-, kjøps-, overførings-, monterings- og produksjonsordrer:  

1. Delvis behandlet (Planleggingsfleksibilitet = Ingen)  
2. Allerede i prosessen i lageret (planleggingsfleksibilitet = ingen)  
3. Frigitt – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)  
4. Fast planlagt produksjonsordre (planleggingsfleksibiliteten = ubegrenset)  
5. Planlagt/åpen – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)  

## <a name="see-also"></a>Se også  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
