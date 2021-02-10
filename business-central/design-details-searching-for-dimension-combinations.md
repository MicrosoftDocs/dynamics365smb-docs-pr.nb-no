---
title: Designdetaljer – Søke etter dimensjonskombinasjoner | Microsoft-dokumentasjon
description: Når du lukker en side etter å ha redigert et sett med dimensjoner, undersøker Business Central om det redigerte settet med dimensjoner finnes. Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c3867c45f659f054a3bdee1605f2d8541e72dec1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751133"
---
# <a name="design-details-searching-for-dimension-combinations"></a>Designdetaljer: Søke etter dimensjonskombinasjoner
Når du lukker en side etter å ha redigert et sett med dimensjoner, undersøker [!INCLUDE[prod_short](includes/prod_short.md)] om det redigerte settet med dimensjoner finnes. Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert.  

## <a name="building-search-tree"></a>Bygge søketre  
 Tabell 481 **Trenode for dimensjonssett** brukes når [!INCLUDE[prod_short](includes/prod_short.md)] vurderer om et sett med dimensjoner allerede finnes i tabell 480 **Dimensjonssettpost**. Evalueringen utføres ved å traversere søketreet rekursivt fra det øverste nivået, som har fått nummeret 0. Det øverste nivået 0 representerer et dimensjonssett uten dimensjonssettposter. De underordnede elementene for dette dimensjonssettet representerer dimensjonssett med bare én dimensjonssettpost. De underordnede elementene for disse dimensjonssettene representerer dimensjonssett med to underordnede elementer og så videre.  

### <a name="example-1"></a>Eksempel 1  
 Diagrammet nedenfor representerer et søketre med seks dimensjonssett. Bare den spesielle dimensjonssettposten vises i diagrammet.  

 ![Eksempel på dimensjonstrestruktur](media/nav2013_dimension_tree.png "Eksempel på dimensjonstrestruktur")  

 Tabellen nedenfor beskriver en fullstendig liste over dimensjonssettpostene som utgjør hvert dimensjonssett.  

|Dimensjonssett|Dimensjonssettposter|  
|--------------------|---------------------------|  
|Sett 0|Ingen|  
|Sett 1|AREA 30|  
|Sett 2|AREA 30, DEPT ADM|  
|Sett 3|AREA 30, DEPT PROD|  
|Sett 4|AREA 30, DEPT ADM, PROJ VW|  
|Sett 5|AREA 40|  
|Sett 6|AREA 40, PROJ VW|  

### <a name="example-2"></a>Eksempel 2  
 Dette eksemplet viser hvordan [!INCLUDE[prod_short](includes/prod_short.md)] vurderer om det finnes et dimensjonssett som består av dimensjonssettpostene AREA 40, DEPT PROD.  

 Først oppdaterer [!INCLUDE[prod_short](includes/prod_short.md)] også tabellen **Trenode for dimensjonssett** for å sikre at søketreet ser ut som diagrammet nedenfor. Dimensjonssett 7 blir dermed underordnet dimensjonssett 5.  

 ![Eksempel på dimensjonstrestruktur i NAV 2013](media/nav2013_dimension_tree_example2.png "Eksempel på dimensjonstrestruktur i NAV 2013")  

### <a name="finding-dimension-set-id"></a>Finne dimensjonssett-ID  
 På et grunnleggende nivå vil **Overordnet ID**, **Dimensjon** og **Dimensjonsverdi** i søketreet, kombineres og brukes som primærnøkkel fordi [!INCLUDE[prod_short](includes/prod_short.md)] går gjennom treet i samme rekkefølge som dimensjonspostene. GET-funksjonen (post) brukes til å søke etter dimensjonssett-ID. Følgende kodeeksempel viser hvordan du finner dimensjonssett-IDen når det finnes tre dimensjonsverdier.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

For å beholde muligheten for [!INCLUDE[prod_short](includes/prod_short.md)] til å gi nytt navn til både en dimensjon og en dimensjonsverdi, utvides imidlertid tabell 349, **Dimensjonsverdi**, med et heltallsfelt, **Dimensjonsverdi-ID**. Denne tabellen konverterer feltparet, **Dimensjon** og **Dimensjonsverdi**, til en heltallsverdi. Når du gir dimensjonen og dimensjonsverdien nytt navn, endres ikke heltallsverdien.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se også  
 [GET-funksjonen (post)](/dynamics-nav/GET-Function--Record-)    
 [Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md)   
 [Dimensjonssettposter – oversikt](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 
