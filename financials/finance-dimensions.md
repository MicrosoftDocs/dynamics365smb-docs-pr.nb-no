---
title: Dimensjoner| Microsoft-dokumentasjon
description: "Bruke dimensjoner til å analysere data."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensjoner
Hvis du vil gjøre det enklere å utføre analyser på dokumenter, for eksempel salgsordrer, kan du bruke dimensjoner. Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

Deretter kan du bruke for eksempel dimensjoner i stedet for å definere separate finanskonti for hver avdeling og hvert prosjekt. Dette gir en rik mulighet for analyse, uten å opprette en komplisert kontoplan.  

Et annet eksempel er å definere en dimensjon som kalles *Avdeling* og bruker denne dimensjonen når du bokfører salgsdokumenter. Dermed kan du bruke verktøyene for forretningsanalyse til å se hvilken avdeling hvilke varer som er solgt.
Jo flere dimensjoner du bruker, jo mer detaljerte rapporter kan du basere dine forretningsavgjørelser på. En enkelt salgspost kan for eksempel inkludere flere dimensjonsopplysninger som:  

* Kontoen varesalget er bokført til  
* Hvor varen ble solgt
* Hvem som solgte den
* Hva slags kunde som kjøpte den  

Du kan opprette så mange dimensjoner med så mange verdier du vil.  

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).

## <a name="using-dimensions"></a>Bruke dimensjoner
I et dokument, for eksempel en ordre, kan du legge til dimensjonsinformasjon om én enkelt dokumentlinje og selve dokumentet. I vinduet **Ordre** kan du for eksempel angi dimensjonsverdier for de to første snarveisdimensjonene direkte på de enkelte salgslinjene, og du kan legge til mer dimensjonsinformasjon hvis du velger knappen **Dimensjoner**.  

Hvis du i stedet arbeider i en kladd, kan du legge til dimensjonsinformasjon i en post på samme måte, forutsatt at du har opprettet snarveisdimensjoner som felt direkte i kladdelinjer.  

Du kan definere standarddimensjoner for konti eller kontotyper, slik at dimensjoner og dimensjonsverdier fylles ut automatisk.  

## <a name="dimension-sets"></a>Dimensjonssett
Et dimensjonssett er en unik kombinasjon av dimensjonsverdier. Det lagres som dimensjonssettposter i databasen. Hver dimensjonssettpost representerer én enkelt dimensjonsverdi. Dimensjonssettet identifiseres av en felles dimensjonssett-ID som tilordnes hver dimensjonssettpost som tilhører dimensjonssettet.  

Når du oppretter en kladdelinje, et dokumenthode eller en dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier. I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Opprette dimensjoner](finance-setup-dimensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

