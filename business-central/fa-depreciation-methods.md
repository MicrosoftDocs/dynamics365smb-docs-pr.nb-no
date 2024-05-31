---
title: Avskrivningsmetoder for aktiva
description: Få informasjon om de ulike innebygde metodene for avskrivning eller nedskrivning av aktiva.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'write down, depreciate, depreciation'
ms.search.form: '5629, 5633'
ms.date: 03/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="depreciation-methods-for-fixed-assets"></a>Avskrivningsmetoder for aktiva

[!INCLUDE [prod_short](includes/prod_short.md)] støtter åtte ulike avskrivningsmetoder for aktiva:

* Lineær
* Saldo 1
* Saldo 2
* Saldo 1/Lineær
* Saldo 2/Lineær
* Halvårsavskrivning
* Manuell
* Brukerdefinert avskrivning

## <a name="straight-line-depreciation"></a>Lineær avskrivning

Med lineær avskrivning avskriver du aktivaverdien med en fast årlig prosentsats eller med et fast årlig beløp over avskrivningsperioden. Når du bruker denne metoden, må du angi ett av følgende alternativer i aktivaavskrivningstablået:  

* Avskrivningsperioden (år eller måneder) eller en sluttdato for avskrivning  
* En fast årlig prosentsats  
* Et fast årlig beløp  
* Avskrivningsperiode  

### <a name="depreciation-period"></a>Avskrivningsperiode

Hvis du angir avskrivningsperioden (antall avskrivningsår, avskrivningsmåneder eller sluttdato for avskrivningen), bruker programmet denne formelen til å beregne avskrivningsbeløpet:  

* Avskrivningsbeløp = ((Bokført verdi - Skrapverdi) X Antall avskrivningsdager) / Resterende avskrivningsdager*  

De resterende avskrivningsdagene beregnes som antall avskrivningsdager minus antall dager mellom startdatoen for avskrivningen og siste aktivapostdato.  

Den bokførte verdien kan reduseres av bokført oppskrivning, nedskriving eller egendefinerte 1- eller 2-beløp, avhengig av om feltet **Inkluder i avskr.beregning** er deaktivert og om feltet **Del av bokført verdi** er aktivert på siden **Aktivabokf.type – oppsett**. Hvis du bruker denne beregningen, avskrives aktivaet fullstendig på sluttdatoen for avskrivningen.  

### <a name="fixed-yearly-percentage"></a>Fast årlig prosentsats

Hvis du angir en fast årlig prosentsats, bruker [!INCLUDE [prod_short](includes/prod_short.md)] følgende formel til å beregne avskrivningsbeløpet:  

* Avskrivningsbeløp = (Lineær-% x Avskrivningsgrunnlag x Antall avskrivningsdager) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a>Fast årlig beløp

Hvis du angir et fast årlig beløp, bruker [!INCLUDE [prod_short](includes/prod_short.md)] følgende formel til å beregne avskrivningsbeløpet:  

* Avskrivningsbeløp = (Fast avskrivningsbeløp x Antall avskrivningsdager) / 360*  

### <a name="example---straight-line-depreciation"></a>Eksempel – lineær avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Den anslåtte levetiden er åtte år. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Aktivaposten ser for eksempel slik ut:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| ---- | --------------- | ---- | ------ | ---------- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning |180 |-6 250,00 |93,750.00 |
| 12/31/20 |Avskrivning |180 |-6 250,00 |87,500.00 |
| 06/30/21 |Avskrivning |180 |-6 250,00 |81,250.00 |
| 12/31/21 |Avskrivning |180 |-6 250,00 |75,000.00 |
| ...      |             |    |          |          |
| 06/30/27 |Avskrivning |180 |-6 250,00 |6,250.00  |
| 12/31/27 |Avskrivning |180 |-6 250,00 |0         |

## <a name="declining-balance-1-depreciation"></a>Saldo 1-avskrivning

Denne avskrivningsmetoden fordeler den største delen av aktivumets kostnad til de tidlige årene av den effektive aktivalevetiden. Hvis du bruker denne metoden, må du angi en fast årlig prosentsats.  

Følkgemde formel beregner avskrivningsbeløp:  

* Avskrivningsbeløp = (Saldo-% x Antall avskrivningsdager x Avskrivningsgrunnlag ) / (100 x 360)*  

Avskrivningsgrunnlaget beregnes som bokført verdi ved årets begynnelse. Antall avskrivningsdager er antall dager mellom bokføringsdatoen og den siste avskrivningsdatoen. [!INCLUDE [prod_short](includes/prod_short.md)] beregner avskrivning under forutsetning av at eventuell avskrivning som er utført i regnskapsåret, utføres med denne formelen.  

Det bokførte avskrivningsbeløpet kan inneholde poster med ulike bokføringstyper (nedskriving, egendef. 1 og egendef. 2) som er bokført etter startdatoen for det inneværende regnskapsåret. Disse bokføringstypene inkluderes i det bokførte avskrivningsbeløpet hvis det er satt en hake i feltene **Avskrivningstype** og **Del av bokført verdi** på siden **Aktivabokf.type - oppsett**.  

### <a name="example-1---declining-balance-1-depreciation"></a>Eksempel 1 – Saldo 1-avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Verdien i feltet **Saldo-%** er 25. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

Tabellen nedenfor viser hvordan aktivapostene ser ut.  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| ---- | --------------- | ---- | ------ | ---------- |
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
| ...      |             |    |          |          |

Beregningsmetode:  

* År 1: *25 % av 100 000 = 25 000 = 12 500 + 12 500*
* År 2: *25 % av 75 000 = 18 750 = 9375 + 9375*
* År 3: *25 % av 56 250 = 14 062,50 = 7031,25 + 7031,25*
* ...

Beregningen fortsetter til den bokførte verdien tilsvarer sluttavrundingsbeløpet eller skrapverdien du angav.  

### <a name="example-2---declining-balance-1-depreciation"></a>Eksempel 2 – Saldo 1-avskrivning

Et aktivums bokførte verdi er 100 000 den 31.12.2022. Du bokfører en avskrivning på 1778 den 02.02.23, som er det forventede (proporsjonale) beløpet for årets avskrivning per 32 dager. Hvis du kjører avskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 8222, fordi det er 148 dager fra 02.02.2023 til 30.06.2023. Forventet restavskrivning for 30.06.2023 beregnes etter følgende formel:

* *148/360 x 0,20 x 100 000 = 8222*

### <a name="example-3---declining-balance-1-depreciation"></a>Eksempel 3 – Saldo 1-avskrivning

Hvis du bokfører et beløp som ikke samsvarer med avskrivningsmetoden Saldo 1-avskriving, for eksempel 5000, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] resten av det forventede beløpet.

Et aktivums bokførte verdi er 100 000 den 31.12.2022. Du bokfører en avskrivning på 5000 den 02.02.2023, som er høyere enn forventet (proporsjonalt) beløp 02.02.2023 på 32 dager. Hvis du kjører avskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 8222, fordi det er 148 dager fra 02.02.2023 til 30.06.2023. Forventet restavskrivning for 30.06.2023 beregnes etter følgende formel:

* *148/360 x 0,20 x 100 000 = 8222*

### <a name="example-4---declining-balance-1-depreciation"></a>Eksempel 4 – Saldo 1-avskrivning

Et aktivums bokførte verdi er 100 000 den 31.12.2023. Du bokfører en avskrivning på 95 000 den 02.02.2023, som overstiger tillatt avskrivningsbeløp for året. Hvis du kjører avskrivning den 30.06.2023, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] 5000, fordi det er 148 dager fra 02.02.2023 til 30.06.2023. Forventet restavskrivning for 30.06.2023 beregnes etter følgende formel: 

* *148/360 x 0,20 x 100 000 = 8222*

Den gjenværende bokførte verdien er imidlertid bare 5000, så [!INCLUDE [prod_short](includes/prod_short.md)] foreslår 5000 fordi en bokført verdi ikke kan være negativ.

## <a name="declining-balance-2-depreciation"></a>Saldo 2-avskrivning

Metodene Saldo 1 og Saldo 2 beregner det samme totale avskrivningsbeløpet for hvert år. Hvis du imidlertid utfører kjørselen **Beregn avskrivning** mer enn én gang i året, gir Saldo 1-metoden like avskrivningsbeløp for hver avskrivningsperiode. Saldo 2-metoden resulterer derimot i avskrivningsbeløp som avtar for hver periode.  

### <a name="example---declining-balance-2-depreciation"></a>Eksempel – saldo 2-avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. Verdien i feltet **Saldo-%** er 25. Kjørselen **Beregn avskrivninger** kjøres hvert halvår. Aktivapostene ser slik ut:  

| Dato     | Aktivabokf.type  | dager                       | Beløp    | Bokført verdi |
| -------- | ---------------- | -------------------------  | --------- | ---------- |
| 01/01/20 |Anskaffelseskostnader |(Startdato for avskrivning)|100,000.00 |100,000.00 |
| 06/30/20 |Avskrivning      |180                         |13 397,46 | 86,602.54 |
| 12/31/20 |Avskrivning      |180                         |-11 602,54 | 75,000.00 |
| 06/30/21 |Avskrivning      |180                         |-10 048,09 | 64,951.91 |
| 12/31/21 |Avskrivning      |180                         |8 701,91  | 56,250.00 |
| ...      |                  |                            |           |           |

Beregningsmetode:  

* *BV* = bokført verdi  
* *AD* = antall avskrivningsdager  
* *SP* = saldoprosent  
* *P* = *SP*/100  
* *D* = *AD*/360  

Formelen for å beregne avskrivningsbeløp er følgende:  

* *DA* = *BV* x (1 – (1 –P)<sup>D</sup>)

Avskrivningsverdiene er:  

| Dato     | Beregning                                                |
| -------- | -----------                                                |
| 06/30/20 |AB = 100 000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 13 397,46 |
| 12/31/20 |AB = 86 602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11 602,54 |
| 06/30/21 |AB = 75 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10 048,09 |
| 12/31/21 |AB = 64 951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8 701,91  |
| ...      |                                                            |

## <a name="db1sl-depreciation"></a>Saldo 1 / lineær avskrivning

PS1/L er en forkortelse for Saldo 1 og Lineær. Beregningen fortsetter til den bokførte verdien tilsvarer sluttavrundingsbeløpet eller skrapverdien du angav.  

Kjørselen **Beregn avskrivning** beregner et lineært beløp og et saldobeløp, men det er bare det største beløpet av disse to som overføres til kladden.  

Du kan bruke ulike prosentsatser til å beregne saldo.  

Hvis du bruker denne metoden, bruker du siden **Aktivaavskrivningstablå** til å angi hvilken effektiv levetid som er anslått, og en prosentsats for saldo.  

> [!NOTE]
> Hvis du bruker noen av avskrivningsmetodene for saldo og vil kjøre avskrivning i flere år, må du kjøre hvert års avskrivning separat. Hvis du kjører avskrivning for hele perioden fra anskaffelsesdatoen til slutten av siste regnskapsår eller siste regnskapsperiode, er det sannsynlig at resultatet blir feil. Det kan for eksempel hende at du vil kjøre det i flere år hvis du har importert eldre data og bruker de faktiske anskaffelsesdatoene for aktivaene og vil ta igjen akkumulert avskrivning. For saldometoder beregner [!INCLUDE [prod_short](includes/prod_short.md)] tillatt avskrivning per år, og tar utgangspunkt i den registrerte bokførte verdien for hvert år. Den kan ikke utføre en flerårig avskrivning i ett trinn.
>
> Rapporten **Aktiva - forventet verdi** kan projisere avskrivninger for flerårsperioder, noe som kan være forvirrende sammenlignet med resultatene du får hvis du kjører avskrivninger i flere år ved hjelp av en av metodene for degressiv avskrivning. 

### <a name="example---db1-sl-depreciation"></a>Eksempel – saldo 1 / lineær avskrivning

Et aktiva har en anskaffelseskost på NOK 100 000. På siden **Aktivaavskrivningstablå** inneholder feltene **Saldoprosent** og **Antall avskrivningsår** en prosentsats på henholdsvis 25 og **8**. Kjørselen **Beregn avskrivninger** kjøres hvert halvår.  

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

`SL` etter den bokførte verdien betyr at lineær avskrivningsmetode ble brukt.  

Beregningsmetode:  

* År 1 (2020):  

    *Saldobeløp: 25 % av 100 000 = 25 000=12 500+12 500*  

    *Lineært beløp = 100 000/8=12 500=6 250+6 250*  

    Saldobeløpet brukes fordi det er det største beløpet.  
* ...
* År 5 (2025):  

    *Saldobeløp: 25 % av 23 730,46 = 4 943,85= 2 471,92+2 471,92*  

    *Lineært beløp = 23 730,46/3 = 7 910,15=3 995,07+3 995,08*  

    Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="half-year-convention-depreciation"></a>Halvårsavskrivning

Metoden for halvårsavskriving brukes bare hvis du aktiverer veksleknappen **Bruk halvårsavskriving** for aktivaet på siden **Aktivakort**.  

Du kan bruke denne avskrivningsmetoden med følgende avskrivningsmetoder:  

* Lineær  
* Saldo 1  
* Saldo 1/Lineær  

Når du bruker metoden for halvårsavskrivning, avskrives aktivumet på seks måneder i det første regnskapsåret, uavhengig av innholdet i feltet **Startdato for avskrivning**.  

> [!NOTE]  
> Den anslåtte aktivalevetiden som gjenstår etter det første regnskapsåret, vil alltid være et halvt år når halvårsavskrivningsmetoden brukes. For at metoden for halvårsavskrivning skal fungere som den skal, må det alltid være en dato i feltet **Sluttdato for avskrivning** på siden **Aktivaavskrivningstablå**. Denne datoen må komme nøyaktig seks måneder før avslutningsdatoen i det regnskapsåret som aktivaet blir fullt avskrevet i.  

### <a name="example---half-year-convention-depreciation"></a>Eksempel – Halvårsavskrivning

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

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Eksempel – PS1/L-avskrivning ved hjelp av halvårsavskrivning

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

`SL` etter den bokførte verdien betyr at lineær avskrivningsmetode ble brukt.  

Beregningsmetode:  

* År 1:  

    *Saldobeløp = Beløp for et helt år = 40 % av 100 000 = 40 000.* For et halvt år er derfor beløpet 40 000 / 2 = 20 000  

    *Lineært beløp = Beløp for et helt år = 100 000 / 5 = 20 000.* For et halvt år er derfor beløpet = 20 000 / 2 =10 000  

    Saldobeløpet brukes fordi det er det største beløpet.  
* ...
* År 5 (2024):  

    *Saldobeløp = 40 % av 17 280,00 = 6912,00*  

    *Lineært beløp = 28 800/1,5 = 11 520,00*  

    Det lineære beløpet brukes fordi det er det største beløpet.  

## <a name="duplicate-entries-to-other-depreciation-books"></a>Dupliser poster til andre avskrivningstablåer

Hvis du har tre avskrivningstablåer, T1, T2 og T3, og vil duplisere poster fra T1 til T2 og T3, kan du aktivere vekslebryteren **Del av duplikasjonsoversikt** på avskrivningstablåkortene for T2 og T3. Denne innstillingen er for eksempel nyttig i følgende situasjoner:

* Avskrivningstablå T1 integreres med finans og bruker aktivafinanskladden.
* Avskrivningstablåene T2 og T3 integreres ikke med finans og bruker aktivakladden.  

Når du gjør en post i T1 i aktivafinanskladden og aktiverer vekslebryteren **Del av duplikatoversikt**, dupliserer [!INCLUDE [prod_short](includes/prod_short.md)] posten i tablå T2 og T3 i aktivakladden når du bokfører posten.  

> [!NOTE]  
> Du kan ikke duplisere i den samme kladden som du dupliserer fra. Hvis du bokfører poster i aktivafinanskladden, kan du duplisere postene i aktivakladden eller i aktivafinanskladden ved hjelp av en annen kladd.  

> [!NOTE]  
> Du kan ikke bruke den samme nummerserien i aktivafinanskladden og aktivakladden. Når du bokfører poster i aktivafinanskladden, må du la feltet **Bilagsnr.** stå tomt. Hvis du angir et tall i feltet, blir nummeret duplisert i anleggsmiddeljournalen. Du må endre bilagsnummeret manuelt før du kan bokføre kladden.  

## <a name="manual-depreciation"></a>Manuell avskrivning

Du den manuelle metoden for aktiva som ikke skal avskrives, for eksempel tomter. Du må angi avskrivning i aktivafinanskladden. Kjørselen **Beregn avskrivninger** utelater aktiva som avskrives etter den manuelle metoden.

## <a name="user-defined-depreciation"></a>Brukerdefinert avskrivning

Hvis de innebygde avskrivningsmetodene ikke oppfyller dine behov, kan du definere din egen avskrivningsmetode ved hjelp av avskrivningstabeller. Hvis du vil finne ut mer om hvordan du bruker en brukerdefinert avskrivningsmetode, kan du gå til [Slik definerer du brukerdefinerte avskrivningsmetoder](fa-how-setup-user-defined-depreciation-method.md).

## <a name="see-also"></a>Se også

[Oversikt over aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
