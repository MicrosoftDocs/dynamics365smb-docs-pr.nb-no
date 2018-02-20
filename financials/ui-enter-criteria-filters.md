---
title: "Søke etter data og angi filterkriterier | Microsoft-dokumentasjon"
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
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Søke etter, filtrere og sortere data
Det finnes et par ting du kan gjøre som hjelper deg med å finne og skanne poster i en oversikt. Dette omfatter sortering, søk og filtrering.

Når du vil søke etter data, for eksempel kundenavn, adresser eller produktgrupper, må du angi kriterier. I søkekriteriene kan du bruke alle tallene og bokstavene du vanligvis kan bruke i det spesifikke feltet. I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere. Det er to måter å søke på: bruke hurtigfilteret eller kolonnefiltre.

## <a name="sorting"></a>Sortering
Sortering gjør det enkelt å få et raskt overblikk over dataene. Hvis du har mange kunder, kan du for eksempel velge å sortere dem etter **Kundenr.**, **Bokføringsgruppe - kunde**, **Valutakode**, **Lands-/regionkode** eller **Mva-organisasjonsnummer** for å få nødvendig oversikt.

Hvis du vil sortere en liste, kan du enten velge en kolonneoverskriftstekst og veksle mellom stigende og synkende rekkefølge, eller velge den lille nedpilen i kolonneoverskriften og deretter velge **Stigende** eller **Synkende**.  

> [!NOTE]  
>   Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.  

## <a name="searching-by-using-the-quick-filter"></a>Søke ved hjelp av hurtigfilteret
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

## <a name="searching-by-using-column-filters"></a>Søke ved hjelp av kolonnefiltre
Du kan legge til et filter på én eller flere kolonner i listen. Filtrering på kolonner er mer fleksibelt og avansert enn hurtigfilteret. 

### <a name="to-add-a-filter-on-a-column"></a>Slik legger du til et filter på en kolonne
1.  Før du legger til et filter, velger du ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre")-ikonet for å bytte til listevisningen.
2. Velg den nedoverpilen i kolonneoverskriften, og deretter velger du **Filter**.
3. Gjør ett av følgende: 
  -  Velg *...* ved siden av feltet for å velge en verdi i listen.
  -  Angi filterkriterier i feltet. Du kan se neste del for detaljer.
4. Velg **OK**.

## <a name="filter-criteria-and-symbols"></a>Filterkriterier og symboler
Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet. I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere. Tabellene nedenfor viser hvilke symboler som kan brukes i filtre.  
  
> [!IMPORTANT]  
>  Det kan være tilfeller der feltverdiene inneholder disse symbolene og du vil filtrere på dem. Hvis du vil gjøre dette, må du ta med filteruttrykket som inneholder symbolet, i anførselstegn (''). Hvis du for eksempel vil filtrere på poster som begynner med teksten *salg*, er filteruttrykket **'salg*'**.  
  
### <a name="-interval"></a>(..) Intervall  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|1100..2100|Tall fra og med 1100 til og med 2100|  
|..2500|Tall til og med 2500|  
|..12 31 00|Datoer til og med 31.12.00|  
|P8..|Opplysninger for regnskapsperiode 8 og fremover|  
|..23|Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59|  
|23..|Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid|  
|22..23|Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59|  
  
### <a name="124-eitheror"></a>(&#124;) Enten/eller  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|1200&#124;1300|Tall med 1200 eller 1300|  
  
### <a name="-not-equal-to"></a>(<>) Ikke lik med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<>0|Alle tall unntatt 0<br /><br /> I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk. <>A* betyr for eksempel ikke lik noen tekst som begynner med A.|  
  
### <a name="-greater-than"></a>(>) Større enn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>1200|Tall som er større enn 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Større enn eller lik med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>=1200|Tall som er større enn eller lik 1200|  
  
### <a name="-less-than"></a>(<) Mindre enn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<1200|Tall som er mindre enn 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Mindre enn eller lik med  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|<=1200|Tall som er mindre enn eller lik 1200|  
  
### <a name="-and"></a>(&) Og  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|>200&<1200|Numre som er større enn 200, men mindre enn 1 200.|  
  
### <a name="-an-exact-character-match"></a>('') Finne et nøyaktig tegntreff  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|'man'|Tekst som samsvarer nøyaktig med man og skiller mellom store og små bokstaver.|  
  
### <a name="-case-insensitive"></a>(@) Skiller ikke mellom små og store bokstaver  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|@man*|Tekst som begynner med man og skiller mellom store og små bokstaver.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Et ubegrenset antall ukjente tegn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|*A/S*|Tekst som inneholder A/S og skiller mellom små og store bokstaver.|  
|*A/S|Tekst som slutter med A/S og skiller mellom små og store bokstaver.|  
|A/S*|Tekst som begynner med A/S og skiller mellom små og store bokstaver.|  
  
### <a name="-one-unknown-character"></a>(?) Ett ukjent tegn  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|Hans?n|Tekst som for eksempel Hansen eller Hanson|  
  
### <a name="combined-format-expressions"></a>Kombinerte formatuttrykk  
  
|Eksempel|Viste poster|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Nummer 5999 og numrene fra og med 8100 til og med 8490.|  
|..1299&#124;1400..|Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).|  
|>50&<100|Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).|  
 
## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

