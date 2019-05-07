---
title: Designdetaljer – Ordre | Microsoft-dokumentasjon
description: Dette emnet gir informasjon om ordre-til-ordre koblinger i et produser-til-ordre-miljø.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 3a0014a80bd4f1f6c786638ddec23a1852c9a635
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "913851"
---
# <a name="design-details-order"></a>Designdetaljer: Ordre
I et produser-til-ordre-miljø blir en vare utelukkende kjøpt eller produsert for å dekke et spesifikt behov. Vanligvis er dette knyttet til A-varer, og motivasjon for å velge gjenbestillingsprinsippet Ordre kan være at behovet er sjeldent, leveringstiden er ubetydelig eller de nødvendige attributtene varierer.  

Programmet oppretter en ordre-til-ordre-kobling, som fungerer som en innledende forbindelse mellom forsyningen, en forsyningsordre eller beholdning, og behovet det skal dekke.  

I tillegg til bruk av ordrepolicy, kan ordre-til-ordre-koblingen brukes under planleggingen på følgende måter:  

* Når produksjonsprinsippet Produser til ordre brukes til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre).  
* Når funksjonen Ordreplanlegging brukes til å opprette en produksjonsordre fra en ordre.  

Selv om et produksjonsselskap anser seg selv som et miljø som produser til ordrer, kan det være best å bruke gjenbestillingsprinsippet parti for parti hvis varene er helt standard uten variasjon i attributter. Resultatet blir at systemet bruker en endring i beholdningsnivået som ikke er planlagt, og akkumulerer bare ordrer med samme leveringsdato eller innenfor en angitt tidsperiode.  

## <a name="order-to-order-links-and-past-due-dates"></a>Odre-til-ordre-koblinger og tidligere forfallsdatoer  
I motsetning til de fleste sett med forsyning/behov planlegger systemet fullstendig for koblede ordrer med forfallsdatoer som kommer før den planlagte startdatoen. Forretningsårsaken til dette unntaket er at bestemte sett med behov/forsyning må synkroniseres helt frem til utførelse. Hvis du vil ha mer informasjon om den frosne sonen som gjelder de fleste behovs-/forsyningstyper, kan du se [Designdetaljer: Håndtere ordrer før den planlagte startdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).  

## <a name="see-also"></a>Se også  
[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
