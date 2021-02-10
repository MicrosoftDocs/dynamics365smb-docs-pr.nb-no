---
title: Designdetaljer – Gjennomsnittskost | Microsoft-dokumentasjon
description: Gjennomsnittskosten for en vare beregnes med et periodisk avveid gjennomsnitt basert på gjennomsnittskostperioden som er definert i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6a716b25f3dfb25d2011fd12ed388fed5e1e98f9
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751833"
---
# <a name="design-details-average-cost"></a>Designdetaljer: Gjennomsnittskost
Gjennomsnittskosten for en vare beregnes med et periodisk avveid gjennomsnitt basert på gjennomsnittskostperioden som er definert i [!INCLUDE[prod_short](includes/prod_short.md)].  

 Verdisettingsdatoen angis automatisk.  

## <a name="setting-up-average-cost-calculation"></a>Konfigurere beregning av gjennomsnittskost  
 Tabellen nedenfor beskriver de to feltene på **Lageroppsett**-siden som må fylles ut hvis du vil aktivere beregning av gjennomsnittskost.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Gjennomsnittskostperiode**|Angir hvilken periode gjennomsnittskosten beregnes i. Følgende alternativer finnes:<br /><br /> -   **Dag**<br />-   **Uke**<br />-   **Måned**<br />-   **Regnskapsperiode**<br /><br /> Alle lagerreduksjoner som bokføres i gjennomsnittskostperioden, får gjennomsnittskosten beregnet for perioden.|  
|**Beregn.type for gj.snittskost**|Angir hvordan gjennomsnittskosten beregnes. Følgende alternativer finnes:<br /><br /> -   **Vare**<br />-   **Vare, Variant og Lokasjon**<br />     Med dette alternativet beregnes gjennomsnittskosten for hver vare, for hver lokasjon og for hver variant av varen. Dette innebærer at gjennomsnittskosten for denne varen bestemmes av hvor den er lagret og hvilken variant du har valgt av varen, for eksempel farge.|  

> [!NOTE]  
>  Du kan bare bruke én gjennomsnittskostperiode og én beregningstype for gjennomsnittskost i et regnskapsår.  
>   
>  Siden **Regnskapsperiode** viser hvilken gjennomsnittskostperiode og hvilken beregningstype for gjennomsnittskost som brukes i denne perioden, for hver regnskapsperiode.  

## <a name="calculating-average-cost"></a>Beregne gjennomsnittskost  
 Når du bokfører en transaksjon for en vare som bruker lagermetoden Gjennomsnitt, opprettes en post i tabellen **Utgangspunkt for justering av gjennomsnittskost**. Denne posten inneholder transaksjonens varenummer, variantkode og lokasjonskode. I tillegg inneholder posten feltet **Verdisettingsdato**, som angir den siste datoen i gjennomsnittskostperioden som transaksjonen ble bokført i.  

> [!NOTE]  
>  Dette feltet må ikke forveksles med feltet **Verdisettingsdato** i **Verdipost**-tabellen, som viser datoen når verdien trer i kraft, og brukes til å fastsette gjennomsnittskostperioden som verdiposten hører til i.  

 Gjennomsnittskosten for en transaksjon beregnes når varens kost justeres. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostjustering](design-details-cost-adjustment.md). Kostjustering bruker postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** til å identifisere hvilke varer (eller varer, lokasjoner og varianter) som gjennomsnittskost skal beregnes for. Kostjusteringen bruker følgende for å fastsette gjennomsnittskost for hver post med en kost som ikke er justert:  

-   Fastsetter kostbeløpet for varen i begynnelsen av gjennomsnittskostperioden.  
-   Legger til summen av inngående kost som ble bokført i løpet av gjennomsnittskostperioden. Disse omfatter kjøp, ordrereturer, positive justeringer og produksjons- og monteringsavganger.  
-   Trekker fra summen av kostbeløpene for utgående transaksjoner som ble fast utlignet mot mottak i gjennomsnittskostperioden. Dette kan vanligvis inkludere bestillingsreturer og negative avganger.  
-   Deler på samlet lagerantall på slutten av gjennomsnittskostperioden, unntatt lagerreduksjoner er som skal verdisettes.  

 Den beregnede gjennomsnittskosten utlignes deretter mot lagerreduksjonene for varen (eller varen, lokasjonen og varianten) med bokføringsdatoer i gjennomsnittskostperioden. Hvis det finnes lagerøkninger som ble fast utlignet mot lagerreduksjoner i gjennomsnittskostperioden, blir beregnet gjennomsnittskost videresendt fra økningen til reduksjonen.  

### <a name="example-average-cost-period--day"></a>Eksempel: Gjennomsnittskostperiode = Dag  
 Følgende eksempel viser resultatet av å beregne gjennomsnittskost basert på en gjennomsnittskostperiode på én dag. Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett** er satt til **Vare**.  

 Tabellen nedenfor viser varepostene for eksemplet på en gjennomsnittskostvare, VARE1, før kjørselen **Juster kostverdi – vareposter** er kjørt.  

|**Bokføringsdato**|**Vareposttype**|**Antall**|**Kostbeløp (faktisk)**|**Postnr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01.01.20|Kjøp|1|20.00|1|  
|01.01.20|Kjøp|1|40.00|2|  
|01.01.20|Salg|-1|-20,00|3|  
|01.02.20|Salg|-1|-40,00|4|  
|02.02.20|Kjøp|1|100,00|5|  
|03.02.20|Salg|-1|-100,00|6|  

> [!NOTE]  
>  Fordi kostjustering ikke er utfør ennå, vil verdiene i feltet **Kostbeløp (faktisk)** for lager bli redusert tilsvarende lagerøkningene de utlignes mot.  

 Tabellen nedenfor viser postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** som gjelder verdiposter som er et resultat av varepostene i tabellen ovenfor.  

|**Varenr.**|**Variantkode**|**Lokasjonskode**|**Verdisettingsdato**|**Kost er justert**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|VARE1||BLÅ|01.01.20|Nei|  
|VARE1||BLÅ|01.02.20|Nei|  
|VARE1||BLÅ|02.02.20|Nei|  
|VARE1||BLÅ|03.02.20|Nei|  

 Tabellen nedenfor viser de samme varepostene etter at kjørselen **Juster kostverdi - vareposter** er kjørt. Gjennomsnittskosten per dag beregnes og utlignes mot lagerreduksjonene.  

|**Bokføringsdato**|**Vareposttype**|**Antall**|**Kostbeløp (faktisk)**|**Postnr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01.01.20|Kjøp|1|20.00|1|  
|01.01.20|Kjøp|1|40.00|2|  
|01.01.20|Salg|-1|-30,00|3|  
|01.02.20|Salg|-1|-30,00|4|  
|02.02.20|Kjøp|1|100,00|5|  
|03.02.20|Salg|-1|-100,00|6|  

### <a name="example-average-cost-period--month"></a>Eksempel: Gjennomsnittskostperiode = Måned  
 Følgende eksempel viser resultatet av å beregne gjennomsnittskost basert på en gjennomsnittskostperiode på én måned. Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett** er satt til **Vare**.  

 Hvis gjennomsnittskostperioden er én måned, opprettes det bare én oppføring for hver kombinasjon av varenummer, variantkode, lokasjonskode og verdisettingsdato.  

 Tabellen nedenfor viser varepostene for eksemplet på en gjennomsnittskostvare, VARE1, før kjørselen **Juster kostverdi – vareposter** er kjørt.  

|**Bokføringsdato**|**Vareposttype**|**Antall**|**Kostbeløp (faktisk)**|**Postnr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01.01.20|Kjøp|1|20.00|1|  
|01.01.20|Kjøp|1|40.00|2|  
|01.01.20|Salg|-1|-20,00|3|  
|01.02.20|Salg|-1|-40,00|4|  
|02.02.20|Kjøp|1|100,00|5|  
|03.02.20|Salg|-1|-100,00|6|  

> [!NOTE]  
>  Fordi kostjustering ikke er utført ennå, vil verdiene i feltet **Kostbeløp (faktisk)** for lager bli redusert tilsvarende lagerøkningene de utlignes mot.  

 Tabellen nedenfor viser postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** som gjelder verdiposter som er et resultat av varepostene i tabellen ovenfor.  

|**Varenr.**|**Variantkode**|**Lokasjonskode**|**Verdisettingsdato**|**Kost er justert**|  
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
|VARE1||BLÅ|31.01.20|Nei|  
|VARE1||BLÅ|28.02.20|Nei|  

> [!NOTE]  
>  Verdisettingsdatoen settes til siste dag i gjennomsnittskostperioden, som i dette tilfellet er siste dag i måneden.  

 Tabellen nedenfor viser de samme varepostene etter at kjørselen **Juster kostverdi - vareposter** er kjørt. Gjennomsnittskosten per måned beregnes og utlignes mot lagerreduksjonene.  

|**Bokføringsdato**|**Vareposttype**|**Antall**|**Kostbeløp (faktisk)**|**Postnr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01.01.20|Kjøp|1|20.00|1|  
|01.01.20|Kjøp|1|40.00|2|  
|01.01.20|Salg|-1|-30,00|3|  
|01.02.20|Salg|-1|-65,00|4|  
|02.02.20|Kjøp|1|100,00|5|  
|03.02.20|Salg|-1|-65,00|6|  

 Gjennomsnittskosten for post nummer 3 beregnes i gjennomsnittskostperioden for januar, og gjennomsnittskosten for post 4 og 6 beregnes i gjennomsnittskostperioden for februar.  

 For å få gjennomsnittskosten for februar legges gjennomsnittskosten for stykket som er mottatt på lageret (100,00), til gjennomsnittskosten i begynnelsen av perioden (30,00). Summen av disse to (130,00) deles deretter på samlet antall på lager (2). Dette gir den resulterende gjennomsnittskosten for varen i februarperioden (65,00). Gjennomsnittskosten tilordnes til lagerreduksjonene i perioden (post 4 og 6).  

## <a name="setting-the-valuation-date"></a>Angi datoen for verdisetting  
 Feltet **Verdisettingsdato** i **Verdipost**-tabellen brukes til å fastsette hvilken gjennomsnittskostperiode en lagerreduksjon hører til i. Dette gjelder også VIA-beholdning (varer i arbeid).  

 Tabellen nedenfor viser kriteriene som brukes til å angi verdisettingsdatoen.  

|Scenario|Bokføringsdato|Verdisatt antall|Revaluering|Verdisettingsdato|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positiv|Nei|Bokføringsdato for varepost|  
|2|Senere enn siste verdisettingsdatoen for utlignede verdiposter|Negativt|Nei|Bokføringsdato for varepost|  
|3|Tidligere enn siste verdisettingsdatoen for utlignede verdiposter|Positivt|Nei|Siste verdisettingsdatoen for utlignede verdiposter|  
|4||Negativt|Ja|Bokføringsdato for revalueringspost|  

### <a name="example"></a>Eksempel  
 Tabellen med verdiposter nedenfor illustrerer de forskjellige scenariene.  

|Scenario|Bokføringsdato|Vareposttype|Verdisettingsdato|Verdisatt antall|Kostbeløp (faktisk)|Varepostnr.|Postnr.|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01.01.20|Kjøp|01.01.20|2|20.00|1|1|  
|2|15.01.20|(Varegebyr)|01.01.20|2|8,00|1|2|  
|3|01.02.20|Salg|01.02.20|-1|-14,00|2|3|  
|4|01.03.20|(Revaluering)|01.03.20|1|-4,00|1|4|  
|5|01.02.20|Salg|01.03.20|-1|-10,00|3|5|  

> [!NOTE]  
>  Løpenummer 5 i den foregående tabellen, har brukeren skrevet inn en ordre med en bokføringsdato (01.02.20) som kommer før den siste verdisettingsdatoen for utlignede verdiposter (01.03.20). Hvis den tilsvarende verdien i feltet **Kostbeløp (faktisk)** for denne datoen (02-01-20) ble brukt for oppføringen, ville den vært 14,00. Dette fører til en situasjon der lagerantallet er null, men lagerverdien er -4,00.  
>   
>  For å unngå en slik uoverensstemmelse mellom antall og verdi angis samme dato for verdisettingsdatoen og den siste verdisettingsdatoen for de utlignede verdipostene (01.03.20). Verdien i feltet **Kostbeløp (faktisk)** blir 10,00 (etter revaluering), som betyr at beholdningsantallet er null, og lagerverdien er også null.  

> [!CAUTION]  
>  Siden rapporten **Lagerverdisetting** er basert på bokføringsdato, vil rapporten gjenspeile alle uoverensstemmelser mellom antall og verdi i scenarier som i eksemplet ovenfor. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerverdisetting](design-details-inventory-valuation.md).  

 Hvis antallet på lager er mindre enn null etter bokføring av lagerreduksjonen, blir verdisettingsdatoen først satt til bokføringsdatoen for lagerreduksjonen. Denne datoen kan endres senere, i samsvar med reglene som er beskrevet i merknaden tidligere i denne delen, når lagerøkningen utlignes.  

## <a name="recalculating-average-cost"></a>Beregne gjennomsnittskost på nytt  
 Å verdisette lagerreduksjoner som et avveid gjennomsnitt hadde vært enkelt hvis kjøp alltid hadde blitt fakturert før salg ble fakturert, bokføringer aldri hadde blitt tilbakedatert og du aldri hadde gjort feil. Virkeligheten er imidlertid litt forskjellig fra dette.  

 Som vist i eksemplene i dette emnet, er verdisettingsdatoen angitt som datoen som verdiposten er inkludert i beregningen av gjennomsnittskosten. Dette gir deg fleksibiliteten til å gjøre følgende for varer som bruker lagermetoden Gjennomsnitt:  

-   Faktura for salget av en vare før kjøpet av varen er fakturert.  
-   Tilbakedatere en postering.  
-   Gjenopprette en feil bokføring.  

> [!NOTE]  
>  En annen årsak til denne fleksibiliteten er fast utligning. Hvis du vil ha mer informasjon om fast utligning, se [Designdetaljer: Vareutligning](design-details-item-application.md).  

 På grunn av denne fleksibiliteten må du kanskje beregne gjennomsnittskost etter at den relaterte bokføring er utført. Hvis du for eksempel bokfører en lagerøkning eller -reduksjon med en Verdisettingsdato som kommer før én eller flere lagerreduksjoner. Omberegningen av gjennomsnittskosten skjer automatisk når du kjører kjørselen **Juster kostverdi - vareposter** manuelt eller automatisk.  

 Det er mulig å endre verdisettingsgrunnlaget for beholdningen i en regnskapsperiode, ved å endre feltet **Gjennomsnittskostperiode** og **Beregn.type for gj.snittskost**. Dette bør imidlertid gjøres med forsiktighet og i henhold til avtale med en revisor.  

### <a name="example"></a>Eksempel  
 Følgende eksempel illustrerer hvordan gjennomsnittskosten beregnes på nytt når en forsinket bokføring foretas på en dato som kommer før én eller flere lagerreduksjoner. Eksemplet er basert på gjennomsnittskostperioden **Dag**.  

 Tabellen nedenfor viser verdipostene som finnes for varen før bokføringen innføres.  

|Verdisettingsdato|Antall|Kostbeløp (faktisk)|Postnr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01.01.20|1|10.00|1|  
|02.01.20|1|20.00|2|  
|15.02.20|-1|-15,00|3|  
|16.02.20|-1|-15,00|4|  

 Brukeren bokfører en lagerøkning (post nummer 5) med en verdisettingsdato (03.01.20) som kommer før én eller flere lagerreduksjoner. For å balansere lageret må gjennomsnittskosten beregnes på nytt og justeres til 17,00.  

 Tabellen nedenfor viser verdipostene som finnes for varen etter at post nummer 5 er innført.  

|Verdisettingsdato|Antall|Kostbeløp (faktisk)|Postnr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01.01.20|1|10.00|1|  
|02.01.20|1|20.00|2|  
|03.01.20|1|21.00|5|  
|15.02.20|-1|-17,00|3|  
|16.02.20|-1|-17,00|4|  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)   
 [Designdetaljer: Kostmetoder](design-details-costing-methods.md)   
 [Designdetaljer: Kostjustering](design-details-cost-adjustment.md)   
 [Designdetaljer: Vareutligning](design-details-item-application.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)  
 [Finans](finance.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
