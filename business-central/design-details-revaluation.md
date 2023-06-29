---
title: Designdetaljer – Revaluering
description: Du kan revaluere lageret basert på verdisettingsgrunnlaget som mest nøyaktig gjenspeiler lagerverdien.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-revaluation"></a><a name="design-details-revaluation"></a>Designdetaljer: Revaluering
Du kan revaluere lageret basert på verdisettingsgrunnlaget som mest nøyaktig gjenspeiler lagerverdien. Du kan også tilbakedatere en revaluering, slik at solgte varers kost (VAREFORBRUK) oppdateres riktig for varer som allerede er solgt. Varer som bruker lagermetoden Standard, og som ikke er fullstendig fakturert, kan også revalueres.  

I [!INCLUDE[prod_short](includes/prod_short.md)] støttes følgende fleksibilitet med hensyn til revaluering:  

-   Antallet som kan revalueres, kan beregnes for en hvilken som helst dato, også tilbake i tid.  
-   Forventede kostposter inkluderes i revaluering for varer som bruker lagermetoden Standard.  
-   Det registreres lagerreduksjoner som er påvirket av revaluering.  

## <a name="calculating-the-revaluable-quantity"></a><a name="calculating-the-revaluable-quantity"></a>Beregne antall som kan revalueres
 Antallet som kan revalueres, er restantallet på lager som er tilgjengelig for revaluering på en gitt dato. Dette beregnes som summen av antallet for fullstendig fakturerte vareposter med en bokføringsdato som er lik eller tidligere enn bokføringsdatoen for revaluering.  

> [!NOTE]  
>  Varer som bruker lagermetoden Standard, behandles forskjellig ved beregning av antall som kan revalueres per vare, lokasjon og variant. Antallene for og verdiene til vareposter som ikke er fullstendig fakturert, tas med i antallet som kan revalueres.  

Etter at en revaluering er bokført, kan du bokføre en lagerøkning eller -reduksjon med en bokføringsdato som kommer før bokføringsdatoen for revaluering. Dette antallet påvirkes imidlertid ikke av revalueringen. For å balansere lageret tas bare det opprinnelige antallet som kan revalueres, med i betraktningen.  

Siden revaluering kan gjøres på alle datoer, må du ha konvensjoner for når en vare er en del av beholdningen fra et økonomisk synspunkt. Eksempel: Når varer er på lager og når varen er i arbeid (VIA).  

### <a name="example"></a><a name="example"></a>Eksempel
Følgende eksempel illustrerer når en VIA-vare går over til å bli en del av beholdningen. Eksemplet er basert på produksjon av en kjede med 150 ledd.  

![VIA-beholdning og revaluering.](media/design_details_inventory_costing_10_revaluation_wip.png "VIA-beholdning og revaluering")  

**1K**: Brukeren posterer kjøpte koblinger som mottatt. Tabellen nedenfor viser den resulterende vareposten.  

|Bokføringsdato|Vare|Posttype|Antall|Løpenr.|  
|------------------|----------|----------------|--------------|---------------|  
|01.01.20|KOBLING|Kjøp|150|1|  

> [!NOTE]  
>  En vare med lagermetoden Standard er nå tilgjengelig for revaluering.  

**1V**: Brukeren posterer kjøpte koblinger som fakturert, og koblingene blir en del av beholdningen, fra et økonomisk synspunkt. Tabellen nedenfor viser de resulterende verdipostene.  

|Bokføringsdato|Posttype|Verdisettingsdato|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15.01.20|Kjøpspris/prod.kost|01.01.20|150,00|1|1|  

 **2K + 2V**: Brukeren posterer kjøpte koblinger som forbrukes i produksjonen av jernkjeden. Fra et økonomisk synspunkt blir koblingene del av VIA-beholdningen.  Tabellen nedenfor viser den resulterende vareposten.  

|Bokføringsdato|Vare|Posttype|Antall|Løpenr.|  
|------------------|----------|----------------|--------------|---------------|  
|01.02.20|KOBLING|Forbruk|-150|1|  

Tabellen nedenfor viser den resulterende verdiposten.  

|Bokføringsdato|Posttype|Verdisettingsdato|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01.02.20|Kjøpspris/prod.kost|01.02.20|-150,00|2|2|  

Verdisettingsdatoen settes til datoen for forbruksbokføring (01.02.20) som en vanlig lagerreduksjon.  

**3K**: Brukeren posterer kjeden som utdata og fullfører produksjonsordren. Tabellen nedenfor viser den resulterende vareposten.  

|Bokføringsdato|Vare|Posttype|Antall|Postnr.|  
|------------------|----------|----------------|--------------|---------------|  
|15.02.20|KJEDE|Vis|1|3|  

**3V**: Brukeren kjører den satsvise jobben **Juster kostverdi - vareposter** som posterer kjeden som fakturert for å angi at all materialforbruk er fullstendig fakturert. Fra et økonomisk synspunkt er ikke koblingene lenger del av VIA-beholdningen når utdataene er fullstendig fakturert og justert. Tabellen nedenfor viser de resulterende verdipostene.  

|Bokføringsdato|Posttype|Verdisettingsdato|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15.01.20|Kjøpspris/prod.kost|01.01.20|150,00|2|2|  
|01.02.20|Kjøpspris/prod.kost|01.02.20|-150,00|2|2|  
|15.02.20|Kjøpspris/prod.kost|15.02.20|150,00|3|3|  

## <a name="expected-cost-in-revaluation"></a><a name="expected-cost-in-revaluation"></a>Forventet kostnad i revaluering
Antallet som kan revalueres, beregnes som summen av antallet for fullstendig fakturerte vareposter med en bokføringsdato som er lik eller tidligere enn revalueringsdatoen. Dette betyr at når noen varer mottas/leveres, men ikke faktureres, kan ikke lagerverdien deres beregnes. Varer som bruker lagermetoden Standard er ikke begrenset på dette området.  

> [!NOTE]  
>  En annen type forventede kostnader som kan revalueres i henhold til bestemte regler, er via-beholdning. Hvis du vil ha mer informasjon, kan du se [Revaluering av VIA-beholdning](design-details-revaluation.md#wip-inventory-revaluation).  

Når antallet som kan revalueres, beregnes for varer som bruker lagermetoden Standard, blir vareposter som ikke er fullstendig fakturert, tatt med i beregningen. Disse postene revalueres deretter når du bokfører revalueringen. Når du fakturerer den revaluerte posten, opprettes følgende verdiposter:  

-   Den vanlige fakturerte verdiposten med posttypen **Kjøpspris/prod.kost**. Kostbeløpet i denne posten er den direkte kostnaden fra kildelinjen.  
-   En verdipost med posttypen **Avvik**. Denne posten registrerer differansen mellom fakturert kost og revaluert standardkost.  
-   En verdipost med posttypen **Revaluering**. Denne posten registrerer tilbakeføringen av revaluering av forventet kost.  

### <a name="example-1"></a><a name="example-1"></a>Eksempel
Følgende eksempel, som er basert på produksjonen av kjeden i forrige eksempel, illustrerer hvordan tre posttyper opprettes. Dette er basert på følgende scenario:  

1.  Brukeren bokfører de kjøpte leddene som mottatt med en enhetskost på LV 2,00.  
2.  Brukeren bokfører deretter en revaluering av leddene med en ny enhetskost på LV 3,00, slik at standardkosten oppdateres til LV 3,00.  
3.  Brukeren bokfører det opprinnelige kjøpet av leddene som fakturert, som gjør at følgende opprettes:  

    1.  En fakturerte verdipost med posttypen **Kjøpspris/prod.kost**.  
    2.  En verdipost med posttypen **Revaluering** for å registrere tilbakeføringen av revaluering av forventede kostnader.  
    3.  En verdipost med oppføringstypen Avvik, registrerer differansen mellom fakturert kostnad og revaluert standardkostnad.  
Tabellen nedenfor viser de resulterende verdipostene.  

|Trinn|Bokføringsdato|Posttype|Verdisettingsdato|Kostbeløp (forventet)|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15.01.20|Kjøpspris/prod.kost|15.01.20|300,00|0,00|1|1|  
|2.|20.01.20|Revaluering|20.01.20|150,00|0,00|1|2|  
|3.a.|15.01.20|Kjøpspris/prod.kost|15.01.20|-300,00|0,00|1|3|  
|3.b.|15.01.20|Revaluering|20.01.20|-150,00|0,00|1|4|  
|3.c.|15.01.20|Avvik|15.01.20|0.00|450,00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation"></a><a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation"></a>Fastslå om en lagerreduksjon påvirkes av revaluering
Datoen for bokføringen eller revalueringen brukes til å fastslå om en lagerreduksjon påvirkes av en revaluering.  

Tabellen nedenfor viser kriteriene som brukes for en vare som ikke bruker lagermetoden Gjennomsnitt.  

|Scenario|Løpenr.|Tidsberegning|Påvirket av revaluering|  
|--------------|---------------|------------|-----------------------------|  
|A|Tidligere enn revalueringsoppføringsnummer|Tidligere enn bokføringsdato for revaluering|Nei|  
|B|Tidligere enn revalueringsoppføring nr.|Er lik bokføringsdato for revaluering|Nei|  
|L|Tidligere enn revalueringsoppføring nr.|Senere enn bokføringsdato for revaluering|Ja|  
|D|Senere enn revalueringsoppføring nr.|Tidligere enn bokføringsdato for revaluering|Ja|  
|E|Senere enn revalueringsoppføring nr.|Er lik bokføringsdato for revaluering|Ja|  
|F|Senere enn revalueringsoppføring nr.|Senere enn bokføringsdato for revaluering|Ja|  

### <a name="example-2"></a><a name="example-2"></a>Eksempel
Følgende eksempel, som illustrerer revaluering av en vare som bruker lagermetoden FIFO, er basert på følgende scenario:  

1.  Brukeren bokfører salg av seks enheter 01.01.20.  
2.  Brukeren bokfører salg av én enhet 01.02.20.  
3.  Brukeren bokfører salg av én enhet 01.03.20.  
4.  Brukeren bokfører salg av én enhet 01.04.20.  
5.  Brukeren beregner lagerverdien for varen 01.03.20, og bokfører en revaluering av varens kostpris fra LV 10,00 til LV 8,00.  
6.  Brukeren bokfører salg av én enhet 01.02.20.  
7.  Brukeren bokfører salg av én enhet 01.03.20.  
8.  Brukeren bokfører salg av én enhet 01.04.20.  
9. Brukeren kjører kjørselen **Juster kostverdi - vareposter**.  

Tabellen nedenfor viser de resulterende verdipostene.  

|Scenario|Bokføringsdato|Posttype|Verdisettingsdato|Verdisatt antall|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01.01.20|Kjøp|01.01.20|6|60,00|1|1|  
||01.03.20|Revaluering|01.03.20|4|-8,00|1|5|  
|A|01.02.20|Salg|01.02.20|-1|-10,00|2|2|  
|B|01.03.20|Salg|01.03.20|-1|-10,00|3|3|  
|L|01.04.20|Salg|01.04.20|-1|-10,00|4|4|  
||01.04.20|Salg|01.04.20|-1|2,00|4|9|  
|D|01.02.20|Salg|01.03.20|-1|-10,00|5|6|  
||01.02.20|Salg|01.03.20|-1|2,00|5|10|  
|E|01.03.20|Salg|01.03.20|-1|-10,00|6|7|  
||01.03.20|Salg|01.03.20|-1|2,00|6|11|  
|F|01.04.20|Salg|01.04.20|-1|-10,00|7|8|  
||01.04.20|Salg|01.04.20|-1|2,00|7|12|  

## <a name="wip-inventory-revaluation"></a><a name="wip-inventory-revaluation"></a>Revaluering av VIA-beholdning
Revaluering av VIA-beholdning innebærer revaluering av komponenter som er registrert som en del av VIA-beholdning da revalueringen ble utført.  

Med hensyn til dette er det viktig å opprette konvensjoner som angir når en vare regnes som en del av VIA-beholdningen, fra et økonomisk synspunkt. I [!INCLUDE[prod_short](includes/prod_short.md)] finnes følgende konvensjoner:  

-   En innkjøpt komponent blir en del av råvarebeholdningen fra tidspunktet for postering av en bestilling som fakturert.  
-   En komponent som er kjøpt / satt sammen av halvfabrikater blir en del av VIA-beholdning fra posteringstidspunktet for forbruket i forbindelse med en produksjonsordre.  
-   En komponent som er kjøpt / satt sammen av halvfabrikater forblir en del av VIA-beholdning til en produksjonsordre (produsert vare) blir fakturert.  

Måten verdisettingsdatoen for verdiposten for forbruk angis på, følger de samme reglene som for ikke-VIA-beholdning. Hvis du vil ha mer informasjon, kan du se [Fastslå om en lagerreduksjon påvirkes av revaluering](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

VIA-beholdning kan revalueres så lenge revalueringsdatoen ikke kommer etter bokføringsdatoen for de tilsvarende varepostene av typen Forbruk, og så lenge den tilsvarende produksjonsordren ikke er fakturert ennå.  

> [!CAUTION]  
>  Rapporten **Lagerverdisetting – VIA** viser verdien til bokførte produksjonsordreposter og kan derfor være litt forvirrende for VIA-varer som er revaluert.  

## <a name="see-also"></a><a name="see-also"></a>Se også
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
 [Designdetaljer: Lagerverdisetting](design-details-inventory-valuation.md) [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
