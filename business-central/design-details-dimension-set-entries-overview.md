---
title: Dimensjonssettposter – oversikt | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 40f6a55adc0c2ade279638b43136475d81cb2c58
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751683"
---
# <a name="dimension-set-entries-overview"></a>Dimensjonssettposter – oversikt
Dette emnet beskriver hvordan dimensjonssettposter lagres og bokføres i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="dimension-sets"></a>Dimensjonssett  
Et dimensjonssett er en unik kombinasjon av dimensjonsverdier. Det lagres som dimensjonssettposter i databasen. Hver dimensjonssettpost representerer én enkelt dimensjonsverdi. Dimensjonssettet identifiseres av en felles dimensjonssett-ID som tilordnes hver dimensjonssettpost som tilhører dimensjonssettet.  

Eksempelet nedenfor viser et dimensjonssett som har tre dimensjonssettposter. Dimensjonssettet identifiseres av en dimensjonssett-ID, som er 108.  

|Dimensjonssett-ID|Dimensjonskode|Dimensjonsverdikode|Navn på dimensjonsverdi|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|OMRÅDE|70|Amerika – nord|  
|108|FIRMATYPE|HOME|Hjem|  
|108|AVDELING|SALG|Salg|  

## <a name="dimension-set-entries"></a>Dimensjonssettposter  
Dimensjonssett lagres i tabellen med **Dimensjonssettpost** som dimensjonssettposter med samme ID for dimensjonssett.  

![Flyt for dimensjonssettposter](media/dimensionentrynav7.png "Flyt for dimensjonssettposter")  

Når du oppretter en ny kladdelinje, et nytt dokumenthode eller en ny dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier. I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.  

Når du redigerer og lukker siden **Rediger dimensjonssettposter**, blir det utført en kontroll for å se om kombinasjonen av dimensjonsverdier eksisterer som et dimensjonssett i tabellen. Hvis kombinasjonen forekommer i tabellen, tilordnes den tilsvarende dimensjonssett-IDen til kladdelinjen, dokumenthodet eller dokumentlinjen. Ellers legges et nytt dimensjonssett til i tabellen, og den nye dimensjonssett-IDen tilordnes til kladdelinjen, dokumenthodet eller dokumentlinjen.

## <a name="codeunit-408-dimension-management"></a>Dimensjonsbehandling for codeunit 408
Codeunit 408, dimensjonsbehandling, er et funksjonsbibliotek som håndterer vanlige oppgaver som er knyttet til dimensjoner, for eksempel kopiering fra én tabell til en annen eller fra ett dokument til et annet.

## <a name="performance-improvement"></a>Ytelsesforbedring  
Ved å lagre dimensjonssett én gang i databasen beholdes databaseplassen, og den generelle ytelsen blir forbedret.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md)   
[Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
[Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]