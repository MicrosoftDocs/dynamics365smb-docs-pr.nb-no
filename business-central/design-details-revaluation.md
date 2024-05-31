---
title: Designdetaljer – Revaluering
description: Du kan revaluere lageret basert på verdisettingsgrunnlaget som mest nøyaktig gjenspeiler lagerverdien.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="design-details-revaluation"></a>Designdetaljer: Revaluering

Du kan revaluere lageret basert på verdisettingsgrunnlaget som mest nøyaktig gjenspeiler lagerverdien. Du kan også tilbakedatere en revaluering for å oppdatere solgte varers kost (VAREFORBRUK) på riktig måte for varer du allerede har solgt. Varer som bruker lagermetoden Standard, og som ikke er fullstendig fakturert, kan også revalueres.  

I [!INCLUDE[prod_short](includes/prod_short.md)] støttes følgende fleksibilitet med hensyn til revaluering:  

- Antallet som kan revalueres, kan beregnes for en hvilken som helst dato, også tilbake i tid.  
- Forventede kostposter inkluderes i revaluering for varer som bruker lagermetoden Standard.  
- Det registreres lagerreduksjoner som er påvirket av revaluering.  

## <a name="calculate-the-revaluable-quantity"></a>Beregn antall som kan revalueres

Antallet du kan revaluere, er restantallet på lager som er tilgjengelig på en gitt dato. Antallet er summen av ferdig fakturerte vareposter du bokfører på eller før revalueringsdatoen.  

> [!NOTE]  
>  Varer som bruker lagermetoden Standard, behandles forskjellig ved beregning av antall som kan revalueres per vare, lokasjon og variant. Antallene for og verdiene til vareposter som ikke er fullstendig fakturert, tas med i antallet som kan revalueres.  

Etter at en revaluering er bokført, kan du bokføre en lagerøkning eller -reduksjon med en bokføringsdato som kommer før bokføringsdatoen for revaluering. Dette antallet påvirkes imidlertid ikke av revalueringen. For å balansere lageret tas bare det opprinnelige antallet som kan revalueres, med i betraktningen.  

Siden du kan revaluere på alle datoer, må du ha konvensjoner for når du vurderer en vare som en del av lageret. Eksempel: Når varer er på lager og når varen er i arbeid (VIA).  

### <a name="example"></a>Eksempel

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
|15.02.20|Direkte kostnad|15.02.20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Forventet kostnad i revaluering

Antallet du kan revaluere, er summen av antallet for fullstendig fakturerte vareposter som du har bokført på eller før revalueringsdatoen. Når noen varer mottas eller leveres, men ikke faktureres, kan du ikke beregne lagerverdien deres. Varer som bruker lagermetoden Standard er ikke begrenset på denne måten.  

> [!NOTE]  
>  En annen type forventede kostnader som kan revalueres i henhold til bestemte regler, er via-beholdning. Hvis du vil ha mer informasjon, kan du se [Revaluering av VIA-beholdning](design-details-revaluation.md#wip-inventory-revaluation).  

Når du beregner antallet som kan revalueres, for varer som bruker lagermetoden Standard, inkluderer beregningen vareposter som ikke er fullstendig fakturert. Disse postene revalueres når du bokfører revalueringen. Når du fakturerer den revaluerte posten, kan du opprette følgende verdiposter:  

- Den vanlige fakturerte verdiposten med posttypen **Kjøpspris/prod.kost**. Kostbeløpet i denne posten er den direkte kostnaden fra kildelinjen.  
- En verdipost med posttypen **Avvik**. Denne posten registrerer differansen mellom fakturert kost og revaluert standardkost.  
- En verdipost med posttypen **Revaluering**. Denne posten registrerer tilbakeføringen av revaluering av forventet kost.

### <a name="example-1"></a>Eksempel

Eksemplet nedenfor er basert på produksjonen av kjeden i det forrige eksemplet. Dette eksemplet beskriver hvordan de tre posttypene opprettes, basert på følgende situasjon:  

1.  Du bokfører de kjøpte leddene som mottatt med en enhetskost på LV 2,00.  
2.  Du bokfører en revaluering av leddene med en ny enhetskost på LV 3,00, slik at standardkosten oppdateres til LV 3,00.  
3.  Du bokfører det opprinnelige kjøpet av kjedeleddene som fakturert, som oppretter følgende verdiposter:  

    1.  En fakturerte verdipost med posttypen **Kjøpspris/prod.kost**.  
    2.  En verdipost med posttypen **Revaluering** for å registrere tilbakeføringen av revaluering av forventede kostnader.  
    3.  En verdipost med oppføringstypen Avvik, registrerer differansen mellom fakturert kostnad og revaluert standardkostnad.  

Tabellen nedenfor viser resultatene.  

|Trinn|Bokføringsdato|Posttype|Verdisettingsdato|Kostbeløp (forventet)|Kostbeløp (faktisk)|Varepostnr.|Løpenr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15.01.20|Kjøpspris/prod.kost|15.01.20|300,00|0,00|1|1|  
|2.|20.01.20|Revaluering|20.01.20|150,00|0,00|1|2|  
|3.a.|15.01.20|Kjøpspris/prod.kost|15.01.20|-300,00|0,00|1|3|  
|3.b.|15.01.20|Revaluering|20.01.20|-150,00|0,00|1|4|  
|3.c.|15.01.20|Avvik|15.01.20|0.00|450.00|1|5|  

## <a name="determine-whether-revaluation-affects-an-inventory-decrease"></a>Fastslå om revalueringen påvirker lagerreduksjonen

Bruk datoen for bokføringen eller revalueringen til å fastslå om en lagerreduksjon påvirkes av en revaluering.  

Tabellen nedenfor viser kriteriene som brukes for en vare som ikke bruker lagermetoden Gjennomsnitt.  

|Scenario|Oppføringsnr.|Tidsberegning|Påvirket av revaluering|  
|--------------|---------------|------------|-----------------------------|  
|A|Tidligere enn revalueringsoppføringsnummer|Tidligere enn bokføringsdato for revaluering|Nei|  
|B|Tidligere enn revalueringsoppføring nr.|Er lik bokføringsdato for revaluering|Nei|  
|L|Tidligere enn revalueringsoppføring nr.|Senere enn bokføringsdato for revaluering|Ja|  
|D|Senere enn revalueringsoppføring nr.|Tidligere enn bokføringsdato for revaluering|Ja|  
|E|Senere enn revalueringsoppføring nr.|Er lik bokføringsdato for revaluering|Ja|  
|F|Senere enn revalueringsoppføring nr.|Senere enn bokføringsdato for revaluering|Ja|  

### <a name="example-2"></a>Eksempel

Følgende eksempel illustrerer revaluering av en vare som bruker lagermetoden FIFU. Eksempelet er basert på følgende scenario:  

1.  Du bokfører salg av seks enheter 01.01.20.  
2.  Du bokfører salg av én enhet 01.02.20.  
3.  Du bokfører salg av én enhet 01.03.20.  
4.  Du bokfører salg av én enhet 01.04.20.  
5.  Du beregner lagerverdien for varen 01.03.20, og bokfører en revaluering av varens kostpris fra LV 10,00 til LV 8,00.  
6.  Du bokfører salg av én enhet 01.02.20.  
7.  Du bokfører salg av én enhet 01.03.20.  
8.  Du bokfører salg av én enhet 01.04.20.  
9. Du kjører kjørselen **Juster kostverdi – vareposter**.  

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
||01.04.20|Salg|01.04.20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>Revaluering av VIA-beholdning

Beregning av VIA-lager betyr at du revaluer komponenter som er registrert som VIA-lager.  

Det er viktig å ha konvensjoner som kontrollerer når en vare er VIA-lager, fra et økonomisk synspunkt. I [!INCLUDE[prod_short](includes/prod_short.md)] finnes følgende konvensjoner:  

- En innkjøpt komponent blir en del av råvarebeholdningen når du bokfører en bestilling som fakturert.  
- En komponent som er kjøpt / satt sammen av halvfabrikater blir en del av VIA-beholdning når du bokfører forbruket med en produksjonsordre.  
- En komponent som er kjøpt / satt sammen av halvfabrikater forblir en del av VIA-beholdning til du fakturerer en produksjonsordre (produsert vare).  

Måten verdisettingsdatoen for verdiposten for forbruk angis på, følger de samme reglene som for ikke-VIA-lager. Hvis du vil finne ut mer, kan du gå til [Fastslå om revalueringen påvirker lagerreduksjonen](#determine-whether-revaluation-affects-an-inventory-decrease).  

Du kan revaluere VIA-lager under følgende betingelser:

- Revalueringsdatoen er før bokføringsdatoene for tilhørende vareposter av typen forbruk.
- Du har ikke fakturert produksjonsordren.  

> [!CAUTION]  
> Rapporten **Lagerverdisetting – VIA** viser verdien til bokførte produksjonsordreposter og kan være litt forvirrende for revaluert VIA-varer.  

## <a name="revaluate-items-with-the-average-costing-method"></a>Revaluer varer med lagermetoden Gjennomsnitt

Du kan bare revaluere varer som bruker lagermetoden Gjennomsnitt, hvis **Beregn per** er *Vare*.

Du kan bare beregne revaluering ved slutten av perioden som er valgt i feltet **Gjennomsnittskostperiode** på siden **Lageroppsett**.

Revaluering vil ikke påvirke negative transaksjoner i inneværende måned, noe som er grunnen til hvorfor fullstendig utlignede inngående poster ikke inkluderes heller.

### <a name="example-3"></a>Eksempel

Dette eksemplet viser hva som skjer når du beregner lagerverdien på siden **Varerevalueringskladd**. På siden **Lageroppsett** er **Vare** valgt i feltet **Beregn. av gjennomsnittskost** og **Måned** er valgt i feltet **Gjennomsnittskostperiode**.

Tabellen nedenfor viser varepostene for eksemplet gjennomsnittkostvare, VARE1.

|Bokføringsdato|Vareposttype|Antall|Kostbeløp (faktisk)|Oppføringsnr.|
|----|----|----|----|----|
25.04.23|Kjøp|5|5.00|1
26.04.23|Kjøp|3|3.00|2
27.04.23|Salg|-5|-5,00|3
28.04.23|Salg|-1|-1,00|4
13.05.23|Kjøp|2|20.00|5
17.06.23|Salg|-6|-22,00|6

Tabellen nedenfor viser resultatet av å kjøre rapporten **Beregn lagerverdi** med forskjellige bokføringsdatoer.

|Bokføringsdato|Antall|Merknad|
|---|---|-------------|
30.04.23|2|Inkluderer bare restantallet fra post 2. Post 1 brukes fullstendig før bokføringsdatoen, og post 5 er etter bokføringsdato.
31.05.23|4|Inkluderer restantallet fra post 2 og 13.
30.06.23|0|Ikke noe restantall på bokføringsdato.

Resultatet av følgende poster vil være 0, uavhengig av bokføringsdatoen.

|Bokføringsdato|Vareposttype|Antall|Kostbeløp (faktisk)|Oppføringsnr.|
|----|----|----|----|----|
13.05.23|Kjøp|5|5.00|1
26.04.23|Salg|-5|5.00|2

## <a name="see-also"></a>Se også

[Utformingsdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
[Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
[Utformingsdetaljer: Lagerverdisetting](design-details-inventory-valuation.md)
[Administrer lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
