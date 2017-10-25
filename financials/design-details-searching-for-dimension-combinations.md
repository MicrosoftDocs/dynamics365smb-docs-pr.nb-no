---
title: "Designdetaljer – Søke etter dimensjonskombinasjoner | Microsoft-dokumentasjon"
description: "Når du lukker et vindu etter å ha redigert et sett med dimensjoner, undersøker [!INCLUDE[d365fin](includes/d365fin_md.md)] om det redigerte settet med dimensjoner finnes. Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9e36a8a1a5eeede5023da32bcb40a06042173fb4
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-searching-for-dimension-combinations"></a>Designdetaljer: Søke etter dimensjonskombinasjoner
Når du lukker et vindu etter å ha redigert et sett med dimensjoner, undersøker [!INCLUDE[d365fin](includes/d365fin_md.md)] om det redigerte settet med dimensjoner finnes. Hvis gruppen ikke finnes, blir det opprettet et nytt sett, og det kombinasjon-IDen for dimensjonen blir returnert.  

## <a name="building-search-tree"></a>Bygge søketre  
 Tabell 481 **Trenode for dimensjonssett** brukes når [!INCLUDE[d365fin](includes/d365fin_md.md)] vurderer om et sett med dimensjoner allerede finnes i tabell 480 **Dimensjonssettpost**. Evalueringen utføres ved å traversere søketreet rekursivt fra det øverste nivået, som har fått nummeret 0. Det øverste nivået 0 representerer et dimensjonssett uten dimensjonssettposter. De underordnede elementene for dette dimensjonssettet representerer dimensjonssett med bare én dimensjonssettpost. De underordnede elementene for disse dimensjonssettene representerer dimensjonssett med to underordnede elementer og så videre.  

### <a name="example-1"></a>Eksempel 1  
 Diagrammet nedenfor representerer et søketre med seks dimensjonssett. Bare den spesielle dimensjonssettposten vises i diagrammet.  

 ![Dimensjonstrestruktur](media/nav2013_dimension_tree.png "NAV2013_Dimension_Tree")  

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
 Dette eksemplet viser hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] vurderer om det finnes et dimensjonssett som består av dimensjonssettpostene AREA 40, DEPT PROD.  

 Først oppdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] også tabellen **Trenode for dimensjonssett** for å sikre at søketreet ser ut som diagrammet nedenfor. Dimensjonssett 7 blir dermed underordnet dimensjonssett 5.  

 ![NAV2013&#95;Dimension&#95;Tree&#95;Example 2](media/nav2013_dimension_tree_example2.png "NAV2013_Dimension_Tree_Example2")  

### <a name="finding-dimension-set-id"></a>Finne dimensjonssett-ID  
 På et grunnleggende nivå vil **Overordnet ID**, **Dimensjon** og **Dimensjonsverdi** i søketreet, kombineres og brukes som primærnøkkel fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] går gjennom treet i samme rekkefølge som dimensjonspostene. GET-funksjonen (post) brukes til å søke etter dimensjonssett-ID. Følgende kodeeksempel viser hvordan du finner dimensjonssett-IDen når det finnes tre dimensjonsverdier.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 For å beholde muligheten for [!INCLUDE[d365fin](includes/d365fin_md.md)] til å gi nytt navn til en dimensjon og dimensjonsverdi, utvides imidlertid tabell 348 **Dimensjonsverdi**, med et heltallsfelt av **Dimensjonsverdi-ID**. Denne tabellen konverterer feltparet **Dimensjon** og **Dimensjonsverdi** til en heltallsverdi. Når du gir dimensjonen og dimensjonsverdien nytt navn, endres ikke heltallsverdien.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Se også  
 [GET-funksjonen (post)](https://msdn.microsoft.com/en-us/library/dd301056.aspx)    
 [Designdetaljer: Dimensjonssettposter](design-details-dimension-set-entries.md)   
 [Dimensjonssettposter – oversikt](design-details-dimension-set-entries-overview.md)   
 [Designdetaljer: Tabellstruktur](design-details-table-structure.md)   
 [Designdetaljer: Dimensjonsbehandling for kodeenhet 408](design-details-codeunit-408-dimension-management.md)   
 [Designdetaljer: Kodeeksempler på endrede mønstre i endringer](design-details-code-examples-of-changed-patterns-in-modifications.md)

