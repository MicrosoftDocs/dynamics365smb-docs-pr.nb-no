---
title: "Definere søkekriterier i filtre | Microsoft-dokumentasjon"
description: "Beskriver hvordan du arbeider med filtre, for eksempel hurtigfilter, for å begrense resultatene du får når du søker etter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Angi vilkår i filtre
Når du vil søke etter data, for eksempel kundenavn, adresser eller produktgrupper, må du angi kriterier. I søkekriteriene kan du bruke alle tallene og bokstavene du vanligvis kan bruke i det spesifikke feltet. I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere.

## <a name="searching-using-the-quick-filter"></a>Søke ved hjelp av hurtigfilteret
Du kan legge til filtre på alle sider ved hjelp av hurtigfilteret. Hurtigfilteret aktiveres ved å velge forstørrelsesikonet i øvre høyre hjørne på siden. Denne filtreringstypen brukes for rask angivelse av kriterier.

> [!IMPORTANT]  
>   Hurtigfilteret gjør det enkelt å filtrere data ved å skrive inn ren tekst, men gir også mange alternativer når det gjelder søkekriterier. Virkemåten for hurtigfilteret er avhengig av om du skriver inn ren tekst eller tekst som inneholder symboler.  

* Hvis du skriver inn ren tekst i søkevilkåret, tolkes søkekriteriene som et søk som ikke skiller mellom store og små bokstaver og som inneholder en bestemt tekst.  
* Hvis du skriver inn tekst med symboler i søkekriteriene, tolkes søkekriteriene nøyaktig slik du skrev det inn, og søket skiller mellom store og små bokstaver.

### <a name="quick-filter-criteria"></a>Kriterier for hurtigfilter
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Søkekriterier</TH>
    <TH>Tolkes som ...</TH>
    <TH>Returnerer ...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alle poster som inneholder teksten <b>mann</b> og som ikke skiller mellom små og store bokstaver.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Alle poster som inneholder teksten <b>se</b> og som ikke skiller mellom små og store bokstaver.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Begynner med <b>Man</b>, og skiller mellom små og store bokstaver.</TD>
    <TD>Alle poster som starter med teksten <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>En nøyaktig tekst som skiller mellom små og store bokstaver.</TD>
    <TD>Alle poster som samsvarer nøyaktig med <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Begynner med, og skiller ikke mellom små og store bokstaver.</TD>
    <TD>Alle poster som starter med <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Slutter med, og skiller ikke mellom små og store bokstaver.</TD>
    <TD>Alle poster som slutter med <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Du kan ikke bruke et jokertegn når du filtrerer på felt for opplisting, for eksempel feltet **Status** i ordrer. Hvis du vil angi et filter for denne typen felt, kan du angi den numeriske verdien som en parameter for filtrering. I feltet **Status** på en ordre som har verdiene **Åpen**, **Frigitt**, **Venter på godkjenning** og **Venter på forskudd**, må du bruke verdiene **0**, **1**, **2** og **3** for å filtrere etter disse alternativene.  

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

