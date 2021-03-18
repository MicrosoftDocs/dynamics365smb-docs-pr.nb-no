---
title: Avskrivningsmetoder for aktiva
description: Lær om de ulike innebygde metodene for å avskrive eller nedskrive aktiva i standardversjonen av Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 02/22/2021
ms.author: edupont
ms.openlocfilehash: 59bf311e24f11e062a243026ec35ca4c7b779952
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493331"
---
# <a name="depreciation-methods-for-fixed-assets"></a>Avskrivningsmetoder for aktiva

Det er åtte tilgjengelige avskrivningsmetoder i standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Lineær  
* Saldo 1  
* Saldo 2  
* Saldo 1/Lineær  
* Saldo 2/Lineær  
* Brukerdefinert  

  > [!NOTE]  
  > Angi din egen avskrivningsmetode ved å definere avskrivningstabeller.
* Manuell  

  > [!NOTE]  
  > Du bruker denne metoden for aktiva som ikke skal avskrives, for eksempel tomter. Du må angi avskrivning i aktivafinanskladden. Kjørselen **Beregn avskrivninger** utelater aktiva som avskrives etter denne avskrivningsmetoden.  
* Halvårsavskrivning  

  > [!NOTE]  
  > Når du bruker denne metoden, avskrives aktivumet med samme beløp hvert år.  

## <a name="straight-line-depreciation"></a>Lineær avskrivning

Når du bruker denne metoden, må du angi ett av følgende alternativer i aktivaavskrivningstablået:  

* Avskrivningsperioden (år eller måneder) eller en sluttdato for avskrivning  
* En fast årlig prosentsats  
* Et fast årlig beløp  
* Avskrivningsperiode  

### <a name="depreciation-period"></a>Avskrivningsperiode

Hvis du angir avskrivningsperioden (antall avskrivningsår, avskrivningsmåneder eller sluttdato for avskrivningen), bruker programmet denne formelen til å beregne avskrivningsbeløpet:  

*Avskrivningsbeløp = ((Bokført verdi - Skrapverdi) x Antall avskrivningsdager) / Resterende avskrivningsdager*  

Resterende avskrivningsdager beregnes som antall avskrivningsdager minus antall dager mellom startdatoen for avskrivningen og siste aktivapostdato.  

Den bokførte verdien kan reduseres av bokført oppskrivning, nedskriving eller egendefinerte 1- eller 2-beløp, avhengig av om feltet **Inkluder i avskr.beregning** er deaktivert og om feltet **Del av bokført verdi** er aktivert på siden **Aktivabokf.type - oppsett**. Hvis du bruker denne beregningen, avskrives aktivaet fullstendig på sluttdatoen for avskrivningen.  

### <a name="fixed-yearly-percentage"></a>Fast årlig prosentsats

Hvis du angir en fast årlig prosentsats, bruker programmet følgende formel til å beregne avskrivningsbeløpet:  

*Avskrivningsbeløp = (Lineær-% x Avskrivningsgrunnlag x Antall avskrivningsdager) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a>Fast årlig beløp

Hvis du angir en fast årlig beløp, bruker programmet denne formelen til å beregne avskrivningsbeløpet:  

*Avskrivningsbeløp = (Fast avskrivningsbeløp x Antall avskrivningsdager) / 360*  

### <a name="example---straight-line-depreciation"></a>Eksempel – lineær avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Den anslåtte levetiden er åtte år. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Aktivaposten ser for eksempel slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning |180 |-6 250,00 |93,750.00 |
| 12/31/20 |Avskrivning |180 |-6 250,00 |87,500.00 |
| 06/30/21 |Avskrivning |180 |-6 250,00 |81,250.00 |
| 12/31/21 |Avskrivning |180 |-6 250,00 |75,000.00 |
| 06/30/27 |Avskrivning |180 |-6 250,00 |6,250.00 |
| 12/31/27 |Avskrivning |180 |-6 250,00 |0 |

## <a name="declining-balance-1-depreciation"></a>Saldo 1-avskrivning

Denne hurtige avskrivningsmetoden fordeler den største delen av aktivakostnaden til de tidlige årene av den effektive aktivalevetiden. Hvis du bruker denne metoden, må du angi en fast årlig prosentsats.  

Følkgemde formel beregner avskrivningsbeløp:  

*Avskrivningsbeløp = (Saldo-% x Antall avskrivningsdager x Avskrivningsgrunnlag ) / (100 x 360)*  

Avskrivningsgrunnlaget beregnes som den bokførte verdien minus bokført avskrivning siden startdatoen for det inneværende regnskapsåret.  

Det bokførte avskrivningsbeløpet kan inneholde poster med ulike bokføringstyper (nedskriving, egendef. 1 og egendef. 2) som er bokført etter startdatoen for det inneværende regnskapsåret. Disse bokføringstypene inkluderes i det bokførte avskrivningsbeløpet hvis det er satt en hake i feltene **Avskrivningstype** og **Del av bokført verdi** på siden **Aktivabokf.type - oppsett**.  

### <a name="example---declining-balance-1-depreciation"></a>Eksempel: Saldo 1-avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Verdien i feltet **Saldo-%** er 25. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Tabellen nedenfor viser hvordan aktivapostene ser ut.  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskostnader |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 12/31/20 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 06/30/21 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 12/31/21 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 06/30/22 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 12/31/22 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 06/30/23 |Avskrivning |180 |5 273,44 |36,914.06 |
| 12/31/23 |Avskrivning |180 |5 273,44 |31,640.62 |
| 06/30/24 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 12/31/24 |Avskrivning |180 |-3 955,08 |23,730.46 |

Beregningsmetode:  

* År 1: *25 % av 100 000 = 25 000 = 12 500 + 12 500*

* År 2: *25 % av 75 000 = 18 750 = 9375 + 9375*

* År 3: *25 % av 56 250 = 14 062,50 = 7031,25 + 7031,25*

Beregningen fortsetter til den bokførte verdien tilsvarer sluttavrundingsbeløpet eller skrapverdien du angav.  

## <a name="declining-balance-2-depreciation"></a>Saldo 2-avskrivning

Metodene Saldo 1 og Saldo 2 beregner det samme totale avskrivningsbeløpet for hvert år. Hvis du imidlertid utfører kjørselen **Beregn avskrivning** mer enn én gang i året, gir Saldo 1-metoden like avskrivningsbeløp for hver avskrivningsperiode. Saldo 2-metoden resulterer derimot i avskrivningsbeløp som avtar for hver periode.  

### <a name="example---declining-balance-2-depreciation"></a>Eksempel – saldo 2-avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Verdien i feltet **Saldo-%** er 25. Kjørselen **Beregn avskrivninger** kjøres hvert halvår. Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskostnader |(Startdato for avskrivning)|100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning |180 |13 397,46 |86,602.54 |
| 12/31/20 |Avskrivning |180 |-11 602,54 |75,000.00 |
| 06/30/21 |Avskrivning |180 |-10 048,09 |64,951.91 |
| 12/31/21 |Avskrivning |180 |8 701,91 |56,250.00 |

Beregningsmetode:  

* *BV* = bokført verdi  
* *AD* = antall avskrivningsdager  
* *SP* = saldoprosent  
* *P* = *SP*/100  
* *D* = *AD*/360  

Formelen for beregning av avskrivningsbeløp er følgende:  

*DA* = *BV* x (1 – (1 –P)<sup>D<sup> 

Avskrivningsverdiene er:  

| Dato | Beregning |
| --- | --- |
| 06/30/20 |AB = 100 000,00 x (1 -(1 - 0,25)<sup>0,5<sup>) = 13 397,46 |
| 12/31/20 |AB = 86 602,54 x (1 - (1 - 0,25)<sup>0,5<sup>) = 11 602,54 |
| 06/30/21 |AB = 75 000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 10 048,09 |
| 12/31/21 |AB = 64 951,91 x (1 - (1 - 0,25)<sup>0,5<sup>) = 8 701,91 |

## <a name="db1sl-depreciation"></a>Saldo 1 / lineær avskrivning

PS1/L er en forkortelse for Saldo 1 og Lineær. Beregningen fortsetter til den bokførte verdien tilsvarer sluttavrundingsbeløpet eller skrapverdien du angav.  

Kjørselen **Beregn avskrivning** beregner et lineært beløp og et saldobeløp, men det er bare det største beløpet av disse to som overføres til kladden.  

Du kan bruke ulike prosentsatser til å beregne saldo.  

Hvis du bruker denne metoden, bruker du siden **Aktivaavskrivningstablå** til å angi hvilken effektiv levetid som er anslått, og en prosentsats for saldo.  

### <a name="example---db1-sl-depreciation"></a>Eksempel – saldo 1 / lineær avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. På siden **Aktivaavskrivningstablå** inneholder feltene **Saldo-%** og **Antall avskrivningsår** en prosentsats på henholdsvis 25 og 8. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskostnader |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 12/31/20 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 06/30/21 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 12/31/21 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 06/30/22 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 12/31/22 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 06/30/23 |Avskrivning |180 |5 273,44 |36,914.06 |
| 12/31/23 |Avskrivning |180 |5 273,44 |31,640.62 |
| 06/30/24 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 12/31/24 |Avskrivning |180 |-3 955,08 |23,730.46 |
| 06/30/25 |Avskrivning |180 |-3 955,08 |19 775,38 L |
| 12/31/25 |Avskrivning |180 |-3 955,08 |15 820,30 L |
| 06/30/26 |Avskrivning |180 |-3 955,08 |11 865,22 L |
| 12/31/26 |Avskrivning |180 |-3 955,07 |7 910,15 L |
| 06/30/27 |Avskrivning |180 |-3 955,08 |3 955,07 L |
| 12/31/27 |Avskrivning |180 |-3 955,07 |0,00 L |

`SL` etter den bokførte verdien betyr at det er brukt lineær avskrivningsmetode.  

Beregningsmetode:  

* År 1:  

    *Saldobeløp: 25 % av 100 000 = 25 000=12 500+12 500*  

    *Lineært beløp = 100 000/8=12 500=6 250+6 250*  

    Saldobeløpet brukes fordi det er det største beløpet.  

* År 5 (2025):  

    *Saldobeløp: 25 % av 23 730,46 = 4 943,85= 2 471,92+2 471,92*  

    *Lineært beløp = 23 730,46/3 = 7 910,15=3 995,07+3 995,08*  

    Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="user-defined-depreciation"></a>Brukerdefinert avskrivning

Programmet gjør det mulig å definere brukerdefinerte avskrivningsmetoder.  

Hvis du velger en slik metode, bruker du siden **Avskrivningstabeller** til å angi en prosentsats for avskrivning for hver enkelt periode (måned, kvartal, år og regnskapsperiode). Når du deretter tilordner et avskrivningstablå med en brukerdefinert metode til et aktivum, må du angi feltene **Første brukerdef. avskr.dato** og **Startdato for avskrivning** på siden **Aktivaavskrivningstablå** for det spesifikke aktivumet.  

Formelen for beregning av avskrivningsbeløp er følgende:  

*Avskrivningsbeløp = (Avskrivnings-% x Antall avskrivningsdager x Avskrivningsgrunnlag ) / (100 x 360)*  

### <a name="depreciation-based-on-number-of-units"></a>Avskrivning etter antall enheter

Denne brukerdefinerte metoden kan også anvendes til avskrivning som er basert på antall enheter, for eksempel hvis du har produksjonsmaskiner med fastlagt levetidskapasitet. På siden **Avskrivningstabeller** kan du angi hvor mange enheter som kan produseres i hver periode (måned, kvartal, år eller regnskapsperiode).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Slik definerer du brukerdefinerte avskrivningsmetoder

På **Avskrivningstabell**-siden kan du opprette brukerdefinerte avskrivningsmetoder. Du kan for eksempel definere avskrivning basert på antall enheter.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Avskrivningstabeller**, og velg deretter den relaterte koblingen.  
2. På siden **Avskrivningstabell - oversikt** velger du handlingen **Ny**.  
3. Fyll ut feltene etter behov på siden **Avskrivningstabellkort**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Bruk funksjonen **Opprett sum av sifre - tabell** til å definere en avskrivningstabell basert på metoden *Sum av sifre*.

Hvis et aktivum avskrives over 4 år med metoden *Sum av sifre*, blir avskrivningen for hvert år beregnet på følgende måte:

Sum av sifre = 1 + 2 + 3 + 4 = 10 avskrivning:

* År 1 = 4/10  
* År 2 = 3/10  
* År 3 = 2/10  
* År 4 = 1/10  

### <a name="example---user-defined-depreciation"></a>Eksempel – brukerdefinert avskrivning

Bruk en avskrivningsmetode som gjør det mulig å foreta en hurtig avskrivning av aktiva på grunn av skattemessige årsaker.  

For aktiva med en levetid på tre år bruker du av skattemessige årsaker følgende avskrivningssatser:  

* År 1: 25 %  
* År 2: 38 %  
* År 3: 37 %  

Anskaffelseskostnadene er NOK 100 000, og avskrivningslevetiden er fem år. Avskrivningen beregnes årlig.  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |360 |-25 000,00 |75,000.00 |
| 12/31/21 |Avskrivning |360 |-38 000,00 |37,000.00 |
| 12/31/22 |Avskrivning |360 |-37 000,00 |0 |
| 12/31/23 |Avskrivning |Ingen |Ingen |0 |
| 12/31/24 |Avskrivning |Ingen |Ingen |0 |

Hvis du bruker en brukerdefinert metode, må du fylle ut feltene **Første brukerdef. avskr.dato** og **Startdato for avskrivning** på siden **Aktivaavskrivningstablå** for det spesifikke aktivumet. Feltet **Første brukerdef. avskr.dato** og innholdet i feltet **Periodelengde** på siden **Avskrivningstabeller** brukes til å angi hvilke tidsintervall som skal brukes i beregning av avskrivninger. Dette sikrer at programmet begynner å bruke den angitte prosenten på samme dag for alle aktiva. Feltet **Startdato for avskrivning** brukes til å beregne antall avskrivningsdager.  

I det forrige eksemplet ville både feltet **Første brukerdef. avskr.dato** og **Startdato for avskrivning** blitt satt til 01/01/20 på siden **Aktivaavskrivningstablå** for det spesifikke aktivumet. Hvis feltet **Første brukerdef. avskr.dato** imidlertid inneholdt 01/01/20 og feltet **Startdato for avskrivning** inneholdt 04/01/20, ville resultatet vært følgende:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |270 |-18 750,00 |81,250.00 |
| 12/31/21 |Avskrivning |360 |-38 000,00 |42,250.00 |
| 12/31/22 |Avskrivning |360 |-37 000,00 |6,250.00 |
| 12/31/23 |Avskrivning |90 |-6 250,00 |0 |
| 12/31/24 |Avskrivning |Ingen |Ingen |0 |

## <a name="half-year-convention-depreciation"></a>Halvårsavskrivning

Metoden for halvårsavskrivning brukes bare hvis du har satt en hake i feltet **Bruk halvårsavskrivning** på siden **Aktivaavskrivningstablå**.  

Denne avskrivningsmetoden kan brukes i forbindelse med følgende avskrivningsmetoder i programmet:  

* Lineær  
* Saldo 1  
* Saldo 1/Lineær  

Når du bruker halvårsavskrivning, avskrives aktivaet på seks måneder i det første regnskapsåret, uavhengig av innholdet i feltet **Startdato for avskrivning**.  

> [!NOTE]  
> Den anslåtte aktivalevetiden som gjenstår etter det første regnskapsåret, vil alltid være et halvt år når halvårsavskrivningsmetoden brukes. For at metoden for halvårsavskrivning skal fungere som den skal, må det alltid være en dato i feltet **Sluttdato for avskrivning** på siden **Aktivaavskrivningstablå**. Denne datoen må komme nøyaktig seks måneder før avslutningsdatoen i det regnskapsåret som aktivaet blir fullt avskrevet i.  

### <a name="example---half-year-convention-depreciation"></a>Eksempel: Halvårsavskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. **Startdato for avskrivning** er 03/01/20. Den anslåtte levetiden er fem år, noe som innebærer at **Sluttdato for avskrivning** må være 06/30/25. Kjørselen **Beregn avskrivning** kjøres årlig. Dette eksempelet baserer seg på et kalenderår i regnskapet.  

Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 03/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |270 |10 000,00 |90,000.00 |
| 12/31/21 |Avskrivning |360 |-20 000,00 |70,000.00 |
| 12/31/22 |Avskrivning |360 |-20 000,00 |50,000.00 |
| 12/31/23 |Avskrivning |360 |-20 000,00 |30,000.00 |
| 12/31/24 |Avskrivning |360 |-20 000,00 |10,000.00 |
| 12/31/25 |Avskrivning |180 |10 000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Eksempel: PS1/L-avskrivning ved hjelp av halvårsavskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. **Startdato for avskrivning** er 11/01/20. Den anslåtte levetiden er fem år, noe som innebærer at **Sluttdato for avskrivning** må være 06/30/25. På siden **Aktivaavskrivningstablå** er prosentsatsen i feltet **Saldo-%** 40. Kjørselen **Beregn avskrivning** kjøres årlig. Dette eksempelet baserer seg på et kalenderår i regnskapet.  

Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 11/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |60 |-20 000,00 |80,000.00 |
| 12/31/21 |Avskrivning |360 |-32 000,00 |48,000.00 |
| 12/31/22 |Avskrivning |360 |-19 200,00 |28,800.00 |
| 12/31/23 |Avskrivning |360 |-11 520,00 |17,280.00 |
| 12/31/24 |Avskrivning |360 |-11 520,00 |5 760,00 L |
| 12/31/25 |Avskrivning |180 |-5 760,00 |0,00 L |

`SL` etter den bokførte verdien betyr at det er brukt lineær avskrivningsmetode.  

Beregningsmetode:  

* År 1:  

    *Saldobeløp = Beløp for et helt år = 40 % av 100 000 = 40 000.* For et halvt år er derfor beløpet 40 000 / 2 = 20 000  

    *Lineært beløp = Beløp for et helt år = 100 000 / 5 = 20 000.* For et halvt år er derfor beløpet = 20 000 / 2 =10 000  

    Saldobeløpet brukes fordi det er det største beløpet.  

* År 5 (2024):  

    *Saldobeløp = 40 % av 17 280,00 = 6912,00*  

    *Lineært beløp = 28 800/1,5 = 11 520,00*  

    Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Duplisere poster til flere avskrivningstablåer

Hvis du har tre avskrivningstablåer, T1, T2 og T3, og vil duplisere poster fra T1 til T2 og T3, kan du sette en hake i feltet **Del av duplikasjonsoversikt** på avskrivningstablåkortene for T2 og T3. Dette kan være nyttig hvis avskrivningstablå T1 er integrert med Finans og bruker aktivafinanskladden, og avskrivningstablåene T2 og T3 ikke er integrert med Finans og bruker aktivakladden.  

Når du angir en post i T1 i aktivafinanskladden og setter en hake i feltet **Bruk duplikatoversikt**, dupliseres posten i tablå T2 og T3 i aktivakladden når posten bokføres.  

> [!NOTE]  
> Du kan ikke duplisere i den samme kladden som du dupliserer fra. Hvis du bokfører poster i aktivafinanskladden, kan du duplisere postene i aktivakladden eller i aktivafinanskladden ved hjelp av en annen kladd.  

> [!NOTE]  
> Du kan ikke bruke den samme nummerserien i aktivafinanskladden og aktivakladden. Når du bokfører poster i aktivafinanskladden, må du la feltet **Bilagsnr.** stå tomt. Hvis du angir et tall i feltet, blir nummeret duplisert i anleggsmiddeljournalen. Du må endre bilagsnummeret manuelt før du kan bokføre kladden.  

## <a name="see-also"></a>Se også

[Anleggsmidler](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]