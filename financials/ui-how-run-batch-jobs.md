---
title: "Utføre kjørsler | Microsoft-dokumentasjon"
description: "Lær hvordan kjørsler fungerer i Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1f4678ce0cfb18a746374226bb33020f70bf874d
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-run-batch-jobs"></a>Utføre kjørsler
Satsvise jobber er rutineoppgaver som behandler data bunkevis, for eksempel den satsvise jobben **Juster valutakurser**. Det finnes kjørsler som utfører periodiske regnskapsoppgaver, som for eksempel å avslutte resultatregnskapet på slutten av et regnskapsår. Mange kjørsler utfører beregninger, for eksempel beregning av renteinntekter/-utgifter, justering av valutakurser og utregning av salgspris.

En satsvis jobb ligner på en rapport, bortsett fra at den satsvise jobben bruker resultatet av det den gjør til å oppdatere informasjonen direkte, i stedet for å skrive ut resultatene.

## <a name="to-run-a-batch-job"></a>Slik kjører du en satsvis jobb
1. Hvis du vil åpne forespørselsvinduet for den relevante kjørselen, går du til øvre høyre hjørne, velger ikonet **Søk etter side eller rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), skriver inn navnet på kjørselen og velger deretter den relaterte koblingen.
2. Hvis kjørselen har hurtigfanen **Alternativer**, fyller du ut feltene for å bestemme hva kjørselen skal gjøre.
3. Vinduet kan inneholde én eller flere hurtigfaner med filtre som du kan bruke til å begrense hvilke data som skal inkluderes i kjørselen. Du kan legge inn kriterier i de foreslåtte filtrene eller legge til flere filtre.
4. Velg **OK**-knappen hvis du vil starte kjørselen.

## <a name="see-also"></a>Se også
[Angi vilkår i filtre](ui-enter-criteria-filters.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

