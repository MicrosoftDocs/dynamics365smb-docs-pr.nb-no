---
title: Avskrivningsmetoder| Microsoft-dokumentasjon
description: Få informasjon om de ulike metodene for avskrivning eller nedskrivning av aktiva.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6f349d7a77078536b7a61e14b5dcd4169ba0f9b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749496"
---
# <a name="depreciation-methods"></a>Avskrivningsmetoder
Det finnes åtte ulike avskrivningsmetoder som du kan bruke:  

* Lineær  
* Saldo 1  
* Saldo 2  
* Saldo 1/Lineær  
* Saldo 2/Lineær  
* Brukerdefinert  
* Manuell  

  > [!NOTE]  
  >   Du bruker denne metoden for aktiva som ikke skal avskrives, for eksempel tomter. Du må angi avskrivning i aktivafinanskladden. Kjørselen **Beregn avskrivninger** utelater aktiva som avskrives etter denne avskrivningsmetoden.  
* Halvårsavskrivning  

  > [!NOTE]  
  >    Når du bruker denne metoden, avskrives aktivumet med samme beløp hvert år.  

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

Avskrivningsbeløp = (Lineær-% x Avskrivningsgrunnlag x Antall avskrivningsdager) / (100 x 360)  

### <a name="fixed-yearly-amount"></a>Fast årlig beløp
Hvis du angir en fast årlig beløp, bruker programmet denne formelen til å beregne avskrivningsbeløpet:  

Avskrivningsbeløp = (Fast avskrivningsbeløp x Antall avskrivningsdager) / 360  

### <a name="example---straight-line-depreciation"></a>Eksempel – lineær avskrivning
Et aktiva har en anskaffelseskost på NOK 100 000. Den anslåtte levetiden er åtte år. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Aktivaposten ser for eksempel slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anskaffelseskost |* |100,000.00 |100,000.00 |
| 30.06.10 |Avskrivning |180 |-6 250,00 |93,750.00 |
| 31.12.10 |Avskrivning |180 |-6 250,00 |87,500.00 |
| 30.06.11 |Avskrivning |180 |-6 250,00 |81,250.00 |
| 31.12.11 |Avskrivning |180 |-6 250,00 |75,000.00 |
| 30.06.17 |Avskrivning |180 |-6 250,00 |6,250.00 |
| 31.12.17 |Avskrivning |180 |-6 250,00 |0 |

* Startdato for avskrivning  

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
| 01.01.10 |Anskaffelseskostnader |* |100,000.00 |100,000.00 |
| 30.06.10 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 31.12.10 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 30.06.11 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 31.12.11 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 30.06.12 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 31.12.12 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 30.06.13 |Avskrivning |180 |5 273,44 |36,914.06 |
| 31.12.13 |Avskrivning |180 |5 273,44 |31,640.62 |
| 30.06.14 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 31.12.14 |Avskrivning |180 |-3 955,08 |23,730.46 |

* Startdato for avskrivning  

    Beregningsmetode:  

    *1. år: 25 % av 100 000 = 25 000 = 12 500 +12 500*

    *2. år: 25 % av 75 000 = 18 750 = 9 375 +9 375*

    *3. år: 25 % av 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

    Beregningen fortsetter til den bokførte verdien tilsvarer sluttavrundingsbeløpet eller skrapverdien du angav.   

## <a name="declining-balance-2-depreciation"></a>Saldo 2-avskrivning
Metodene Saldo 1 og Saldo 2 beregner det samme totale avskrivningsbeløpet for hvert år. Hvis du imidlertid utfører kjørselen **Beregn avskrivning** mer enn én gang i året, gir Saldo 1-metoden like avskrivningsbeløp for hver avskrivningsperiode. Saldo 2-metoden resulterer derimot i avskrivningsbeløp som avtar for hver periode.  

### <a name="example---declining-balance-2-depreciation"></a>Eksempel – saldo 2-avskrivning
Et aktiva har en anskaffelseskost på NOK 100 000. Verdien i feltet **Saldo-%** er 25. Kjørselen **Beregn avskrivninger** kjøres hvert halvår. Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anskaffelseskostnader |* |100,000.00 |100,000.00 |
| 30.06.10 |Avskrivning |180 |13 397,46 |86,602.54 |
| 31.12.10 |Avskrivning |180 |-11 602,54 |75,000.00 |
| 30.06.11 |Avskrivning |180 |-10 048,09 |64,951.91 |
| 31.12.11 |Avskrivning |180 |8 701,91 |56,250.00 |

* Startdato for avskrivning  

Beregningsmetode:  

* BV = bokført verdi  
* AD = Antall avskrivningsdager  
* SP = Saldoprosent  
* P = SP/100  
* D = AD/360  

Formelen for beregning av avskrivningsbeløp er følgende:  

*AB = BV x (1 – (1 –P)<sup>D<sup>*  

Avskrivningsverdiene er:  

| Dato | Beregning |
| --- | --- |
| 30.06.10 |AB = 100 000,00 x (1 -(1 - 0,25)<sup>0,5<sup>) = 13 397,46 |
| 31.12.10 |AB = 86 602,54 x (1 - (1 - 0,25)<sup>0,5<sup>) = 11 602,54 |
| 30.06.11 |AB = 75 000,00 x (1 - (1 - 0,25)<sup>0,5<sup>) = 10 048,09 |
| 31.12.11 |AB = 64 951,91 x (1 - (1 - 0,25)<sup>0,5<sup>) = 8 701,91 |

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
| 01.01.10 |Anskaffelseskostnader |* |100,000.00 |100,000.00 |
| 30.06.10 |Avskrivning |180 |-12 500,00 |87,500.00 |
| 31.12.10 |Avskrivning |180 |-12 500,00 |75,000.00 |
| 30.06.11 |Avskrivning |180 |-9 375,00 |65,625.00 |
| 31.12.11 |Avskrivning |180 |-9 375,00 |56,250.00 |
| 30.06.12 |Avskrivning |180 |-7 031,25 |49,218.75 |
| 31.12.12 |Avskrivning |180 |-7 031,25 |42,187.50 |
| 30.06.13 |Avskrivning |180 |5 273,44 |36,914.06 |
| 31.12.13 |Avskrivning |180 |5 273,44 |31,640.62 |
| 30.06.14 |Avskrivning |180 |-3 955,08 |27,685.54 |
| 31.12.14 |Avskrivning |180 |-3 955,08 |23,730.46 |
| 30.06.15 |Avskrivning |180 |-3 955,08 |19 775,38 L |
| 31.12.15 |Avskrivning |180 |-3 955,08 |15 820,30 L |
| 30.06.16 |Avskrivning |180 |-3 955,08 |11 865,22 L |
| 31.12.16 |Avskrivning |180 |-3 955,07 |7 910,15 L |
| 30.06.17 |Avskrivning |180 |-3 955,08 |3 955,07 L |
| 31.12.17 |Avskrivning |180 |-3 955,07 |0,00 L |

* Startdato for avskrivning  

"L" etter den bokførte verdien betyr at det er brukt lineær avskrivningsmetode.  

Beregningsmetode:  

år:  

*Saldobeløp: 25 % av 100 000 = 25 000=12 500+12 500*  

*Lineært beløp = 100 000/8=12 500=6 250+6 250*  

Saldobeløpet brukes fordi det er det største beløpet.  

år (2015):  

*Saldobeløp: 25 % av 23 730,46 = 4 943,85= 2 471,92+2 471,92*  

*Lineært beløp = 23 730,46/3 = 7 910,15=3 995,07+3 995,08*  

Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="user-defined-depreciation"></a>Brukerdefinert avskrivning
Programmet gjør det mulig å definere brukerdefinerte avskrivningsmetoder.  

Hvis du velger en slik metode, bruker du siden **Avskrivningstabeller** til å angi en prosentsats for avskrivning for hver enkelt periode (måned, kvartal, år og regnskapsperiode).  

Formelen for beregning av avskrivningsbeløp er følgende:  

Avskrivningsbeløp = (Avskrivnings-% x Antall avskrivningsdager x Avskrivningsgrunnlag ) / (100 x 360)  

### <a name="depreciation-based-on-number-of-units"></a>Avskrivning etter antall enheter
Denne brukerdefinerte metoden kan også anvendes til avskrivning som er basert på antall enheter, for eksempel hvis du har produksjonsmaskiner med fastlagt levetidskapasitet. På siden **Avskrivningstabeller** kan du angi hvor mange enheter som kan produseres i hver periode (måned, kvartal, år eller regnskapsperiode).  

### <a name="to-set-up-user-defined-depreciation-methods"></a>Slik definerer du brukerdefinerte avskrivningsmetoder
På **Avskrivningstabell**-siden kan du opprette brukerdefinerte avskrivningsmetoder. Du kan for eksempel definere avskrivning basert på antall enheter.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Avskrivningstabeller**, og velg deretter den relaterte koblingen.  
2. På siden **Avskrivningstabell - oversikt** velger du handlingen **Ny**.  
3. Fyll ut feltene etter behov på siden **Avskrivningstabellkort**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="example---user-defined-depreciation"></a>Eksempel – brukerdefinert avskrivning
Bruk en avskrivningsmetode som gjør det mulig å foreta en hurtig avskrivning av aktiva på grunn av skattemessige årsaker.  

For aktiva med en levetid på tre år bruker du av skattemessige årsaker følgende avskrivningssatser:  

* 1. år: 25%  
* 2. år: 38%  
* 3. år: 37%  

Anskaffelseskostnadene er NOK 100 000, og avskrivningslevetiden er fem år. Avskrivningen beregnes årlig.  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anskaffelseskost |* |100,000.00 |100,000.00 |
| 31.12.10 |Avskrivning |360 |-25 000,00 |75,000.00 |
| 31.12.11 |Avskrivning |360 |-38 000,00 |37,000.00 |
| 31.12.12 |Avskrivning |360 |-37 000,00 |0 |
| 31.12.13 |Avskrivning |Ingen |Ingen |0 |
| 31.12.14 |Avskrivning |Ingen |Ingen |0 |

* Startdato for avskrivning  

Hvis du bruker en brukerdefinert metode, må du fylle ut feltene **Første brukerdef. avskr.dato** og **Startdato for avskrivning** på siden **Aktivaavskrivningstablå**. Feltet **Første brukerdef. avskr.dato** og innholdet i feltet **Periodelengde** på siden **Avskrivningstabeller** brukes til å angi hvilke tidsintervall som skal brukes i beregning av avskrivninger. Dette sikrer at programmet begynner å bruke den angitte prosenten på samme dag for alle aktiva. Feltet **Startdato for avskrivning** brukes til å beregne antall avskrivningsdager.  

I forrige eksempel inneholder feltene **Første brukerdef. avskr.dato** og **Startdato for avskrivning** 01.01.01. Hvis imidlertid feltet **Første brukerdef. avskr.dato** inneholdt 01.01.10 og feltet **Startdato for avskrivning** inneholdt 01.04.11, hadde resultatet blitt følgende:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.01.10 |Anskaffelseskost |* |100,000.00 |100,000.00 |
| 31.12.10 |Avskrivning |270 |-18 750,00 |81,250.00 |
| 31.12.11 |Avskrivning |360 |-38 000,00 |42,250.00 |
| 31.12.12 |Avskrivning |360 |-37 000,00 |6,250.00 |
| 31.12.13 |Avskrivning |90 |-6 250,00 |0 |
| 31.12.14 |Avskrivning |Ingen |Ingen |0 |

* Startdato for avskrivning  

## <a name="half-year-convention-depreciation"></a>Halvårsavskrivning
Metoden for halvårsavskrivning brukes bare hvis du har satt en hake i feltet **Bruk halvårsavskrivning** på siden **Aktivaavskrivningstablå**.  

Denne avskrivningsmetoden kan brukes i forbindelse med følgende avskrivningsmetoder i programmet:  

* Lineær  
* Saldo 1  
* Saldo 1/Lineær  

Når du bruker halvårsavskrivning, avskrives aktivaet på seks måneder i det første regnskapsåret, uavhengig av innholdet i feltet **Startdato for avskrivning**.  

> [!NOTE]  
>   Den anslåtte aktivalevetiden som gjenstår etter det første regnskapsåret, vil alltid være et halvt år når halvårsavskrivningsmetoden brukes. For at metoden for halvårsavskrivning skal fungere som den skal, må det alltid være en dato i feltet **Sluttdato for avskrivning** på siden **Aktivaavskrivningstablå**. Denne datoen må komme nøyaktig seks måneder før avslutningsdatoen i det regnskapsåret som aktivaet blir fullt avskrevet i.  

### <a name="example---half-year-convention-depreciation"></a>Eksempel: Halvårsavskrivning
Et aktiva har en anskaffelseskost på NOK 100 000. **Startdato for avskrivning** er 01.03.10. Den anslåtte levetiden er fem år, noe som innebærer at **Sluttdato for avskrivning** må være 30.06.15. Kjørselen **Beregn avskrivning** kjøres årlig. Dette eksempelet baserer seg på et kalenderår i regnskapet.  

Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.03.10 |Anskaffelseskost |* |100,000.00 |100,000.00 |
| 31.12.10 |Avskrivning |270 |10 000,00 |90,000.00 |
| 31.12.11 |Avskrivning |360 |-20 000,00 |70,000.00 |
| 31.12.12 |Avskrivning |360 |-20 000,00 |50,000.00 |
| 31.12.13 |Avskrivning |360 |-20 000,00 |30,000.00 |
| 31.12.14 |Avskrivning |360 |-20 000,00 |10,000.00 |
| 31.12.15 |Avskrivning |180 |10 000,00 |0.00 |

* Startdato for avskrivning  

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Eksempel: PS1/L-avskrivning ved hjelp av halvårsavskrivning
Et aktiva har en anskaffelseskost på NOK 100 000. **Startdato for avskrivning** er 01.11.10. Den anslåtte levetiden er fem år, noe som innebærer at **Sluttdato for avskrivning** må være 30.06.15. På siden **Aktivaavskrivningstablå** er prosentsatsen i feltet **Saldo-%** 40. Kjørselen **Beregn avskrivning** kjøres årlig. Dette eksempelet baserer seg på et kalenderår i regnskapet.  

Aktivapostene ser slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01.11.10 |Anskaffelseskost |* |100,000.00 |100,000.00 |
| 31.12.10 |Avskrivning |60 |-20 000,00 |80,000.00 |
| 31.12.11 |Avskrivning |360 |-32 000,00 |48,000.00 |
| 31.12.12 |Avskrivning |360 |-19 200,00 |28,800.00 |
| 31.12.13 |Avskrivning |360 |-11 520,00 |17,280.00 |
| 31.12.14 |Avskrivning |360 |-11 520,00 |5 760,00 L |
| 31.12.15 |Avskrivning |180 |-5 760,00 |0,00 L |

* Startdato for avskrivning  

"L" etter den bokførte verdien betyr at det er brukt lineær avskrivningsmetode.  

Beregningsmetode:  

år:  

*Saldobeløp = beløp for et helt år = 40 % av 100 000 = 40 000. For et halvt år er derfor beløpet 40 000 / 2 = 20 000*  

*Lineært beløp = beløp for et helt år = 100 000 / 5=20 000. For et halvt år er derfor beløpet = 20 000 / 2 =10 000*  

Saldobeløpet brukes fordi det er det største beløpet.  

5. år (2004):  

*Saldobeløp = 40 % av 17 280,00 = 6912,00*  

*Lineært beløp = 28 800/1,5 = 11 520,00*  

Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="duplicating-entries-to-more-depreciation-books"></a>Duplisere poster til flere avskrivningstablåer
Hvis du har tre avskrivningstablåer, T1, T2 og T3, og vil duplisere poster fra T1 til T2 og T3, kan du sette en hake i feltet **Del av duplikasjonsoversikt** på avskrivningstablåkortene for T2 og T3. Dette kan være nyttig hvis avskrivningstablå T1 er integrert med Finans og bruker aktivafinanskladden, og avskrivningstablåene T2 og T3 ikke er integrert med Finans og bruker aktivakladden.  

Når du angir en post i T1 i aktivafinanskladden og setter en hake i feltet **Bruk duplikatoversikt**, dupliseres posten i tablå T2 og T3 i aktivakladden når posten bokføres.  

> [!NOTE]  
>   Du kan ikke duplisere i den samme kladden som du dupliserer fra. Hvis du bokfører poster i aktivafinanskladden, kan du duplisere postene i aktivakladden eller i aktivafinanskladden ved hjelp av en annen kladd.  

> [!NOTE]  
>   Du kan ikke bruke den samme nummerserien i aktivafinanskladden og aktivakladden. Når du bokfører poster i aktivafinanskladden, må du la feltet **Bilagsnr.** stå tomt. Hvis du angir et tall i feltet, blir nummeret duplisert i anleggsmiddeljournalen. Du må endre bilagsnummeret manuelt før du kan bokføre kladden.  

## <a name="see-also"></a>Se også
[Anleggsmidler](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]