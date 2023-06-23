---
title: Designdetaljer – Gjennomsnittskost
description: Gjennomsnittskosten for en vare beregnes med et periodisk avveid gjennomsnitt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '8645,'
ms.date: 06/06/2023
ms.author: bholtorf
---
# Utformingsdetaljer: Gjennomsnittskost

Gjennomsnittskosten for en vare beregnes med et periodisk avveid gjennomsnitt. Gjennomsnittet er basert på gjennomsnittskostperioden som er definert i [!INCLUDE[prod_short](includes/prod_short.md)].  

Verdisettingsdatoen angis automatisk.  

## Konfigurere beregning av gjennomsnittskost

Tabellen nedenfor beskriver de to feltene på **Lageroppsett**-siden som må fylles ut hvis du vil aktivere beregning av gjennomsnittskost.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Gjennomsnittskostperiode**|Angir hvilken periode gjennomsnittskosten beregnes i. Følgende alternativer finnes:<br /><br /> - **Dag**<br />- **Uke**<br />- **Måned**<br />- **Regnskapsperiode**<br /><br /> Reduksjoner i lager som bokføres i gjennomsnittskostperioden, får gjennomsnittskosten beregnet for perioden.|  
|**Beregningstype for gjennomsnittskost**|Angir hvordan gjennomsnittskosten beregnes. Følgende alternativer finnes:<br /><br /> - **Vare**<br />- **Vare, Variant og Lokasjon**<br /> Med dette alternativet beregnes gjennomsnittskosten for hver vare, for hver lokasjon og for hver variant av varen. Gjennomsnittskosten for denne varen bestemmes av hvor den er lagret og varianten du velger, for eksempel farge.|  

> [!NOTE]  
> Du kan bare bruke én gjennomsnittskostperiode og én beregningstype for gjennomsnittskost i et regnskapsår.  
>
> Siden **Regnskapsperiode** viser hvilken gjennomsnittskostperiode og hvilken beregningstype for gjennomsnittskost som brukes i denne perioden, for hver regnskapsperiode.  

## Beregne gjennomsnittskost

 Når du bokfører en transaksjon for en vare som bruker lagermetoden Gjennomsnitt, opprettes en post i tabellen **Utgangspunkt for justering av gjennomsnittskost**. Denne posten inneholder transaksjonens varenummer, variantkode og lokasjonskode. I tillegg inneholder posten feltet **Verdisettingsdato**, som angir den siste datoen i gjennomsnittskostperioden som transaksjonen ble bokført i.  

> [!NOTE]  
> Dette feltet må ikke forveksles med feltet **Verdisettingsdato** i **Verdipost**-tabellen, som viser datoen når verdien trer i kraft, og brukes til å fastsette gjennomsnittskostperioden som verdiposten hører til i.  

 Gjennomsnittskosten for en transaksjon beregnes når varens kost justeres. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostjustering](design-details-cost-adjustment.md). Kostjustering bruker postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** til å identifisere hvilke varer (eller varer, lokasjoner og varianter) som gjennomsnittskost skal beregnes for. Kostjusteringen bruker følgende for å fastsette gjennomsnittskost for hver post med en kost som ikke er justert:  

- Fastsetter kostbeløpet for varen i begynnelsen av gjennomsnittskostperioden.  
- Legger til summen av inngående kost som ble bokført i løpet av gjennomsnittskostperioden. Disse omfatter kjøp, ordrereturer, positive justeringer og produksjons- og monteringsavganger.  
- Trekker fra summen av kostbeløpene for utgående transaksjoner som ble fast utlignet mot mottak i gjennomsnittskostperioden. Dette kan vanligvis inkludere bestillingsreturer og negative avganger.  
- Deler på samlet lagerantall for slutten av gjennomsnittskostperioden. Utelater lagerreduksjoner som blir verdisatt.  

 Den beregnede gjennomsnittskosten utlignes deretter mot lagerreduksjonene for varen (eller varen, lokasjonen og varianten) med bokføringsdatoer i gjennomsnittskostperioden. For lagerøkninger som er fast utlignet mot lagerreduksjoner i gjennomsnittskostperioden, videresender [!INCLUDE [prod_short](includes/prod_short.md)] den beregnede gjennomsnittskost fra økningen til reduksjonen.  

### Eksempel: Gjennomsnittskostperiode = Dag

Følgende eksempel viser resultatet av å beregne gjennomsnittskost basert på en gjennomsnittskostperiode på én dag. Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett** er satt til **Vare**.  

Tabellen nedenfor viser varepostene for eksemplet på en gjennomsnittskostvare, VARE1, før kjørselen **Juster kostverdi – vareposter** er kjørt.  

| **Bokføringsdato** | **Vareposttype** | **Antall** | **Kostbeløp (faktisk)** | **Oppføringsnr.** |
|--|--|--|--|--|
| 01.01.23 |   Kjøp | 1 | 20.00 | 1 |
| 01.01.23 |   Kjøp | 1 | 40.00 | 2 |
| 01.01.23 |   Salg | -1 | -20,00 | 3 |
| 01.02.23 |   Salg | -1 | -40,00 | 4 |
| 02.02.23 |   Kjøp | 1 | 100.00 | 5 |
| 03.02.23 |   Salg | -1 | -100,00 | 6 |

> [!NOTE]  
> Fordi kostjustering ikke er utfør ennå, vil verdiene i feltet **Kostbeløp (faktisk)** for lager bli redusert tilsvarende lagerøkningene de utlignes mot.  

 Tabellen nedenfor viser postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** som gjelder verdiposter som er et resultat av varepostene i tabellen ovenfor.  

| **Varenr.** | **Variantkode** | **Lokasjonskode** | **Verdisettingsdato** | **Kost er justert** |
|--|--|--|--|--|
| VARE1 |  | OSLO | 01.01.23 |   Nei |
| VARE1 |  | OSLO | 01.02.23 |   Nei |
| VARE1 |  | OSLO | 02.02.23 |   Nei |
| VARE1 |  | OSLO | 03.02.23 |   Nei |

 Tabellen nedenfor viser de samme varepostene etter at kjørselen **Juster kostverdi - vareposter** er kjørt. Gjennomsnittskosten per dag beregnes og utlignes mot lagerreduksjonene.  

| **Bokføringsdato** | **Vareposttype** | **Antall** | **Kostbeløp (faktisk)** | **Oppføringsnr.** |
|--|--|--|--|--|--|
| 01.01.23 |   Kjøp | 1 | 20.00 | 1 |
| 01.01.23 |   Kjøp | 1 | 40.00 | 2 |
| 01.01.23 |   Salg | -1 | -30,00 | 3 |
| 01.02.23 |   Salg | -1 | -30,00 | 4 |
| 02.02.23 |   Kjøp | 1 | 100.00 | 5 |
| 03.02.23 |   Salg | -1 | -100,00 | 6 |

### Eksempel: Gjennomsnittskostperiode = Måned

 Dette eksempelet viser resultatet av å beregne gjennomsnittskost basert på en gjennomsnittskostperiode på én måned. Feltet **Beregn.type for gj.snittskost** på siden **Lageroppsett** er satt til **Vare**.  

 Hvis gjennomsnittskostperioden er én måned, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] én oppføring for hver kombinasjon av varenummer, variantkode, lokasjonskode og verdisettingsdato.  

 Tabellen nedenfor viser varepostene for eksemplet på en gjennomsnittskostvare, VARE1, før kjørselen **Juster kostverdi – vareposter** er kjørt.  

| **Bokføringsdato** | **Vareposttype** | **Antall** | **Kostbeløp (faktisk)** | **Oppføringsnr.** |
|--|--|--|--|--|
| 01.01.23 |   Kjøp | 1 | 20.00 | 1 |
| 01.01.23 |   Kjøp | 1 | 40.00 | 2 |
| 01.01.23 |   Salg | -1 | -20,00 | 3 |
| 01.02.23 |   Salg | -1 | -40,00 | 4 |
| 02.02.23 |   Kjøp | 1 | 100.00 | 5 |
| 03.02.23 |   Salg | -1 | -100,00 | 6 |

> [!NOTE]  
> Fordi kostjustering ikke er utført ennå, vil verdiene i feltet **Kostbeløp (faktisk)** for lager bli redusert tilsvarende lagerøkningene de utlignes mot.  

Tabellen nedenfor viser postene i tabellen **Utgangspunkt for justering av gjennomsnittskost** som gjelder verdiposter som er et resultat av varepostene i tabellen ovenfor.  

| **Varenr.** | **Variantkode** | **Lokasjonskode** | **Verdisettingsdato** | **Kost er justert** |
|--|--|--|--|--|
| VARE1 |  | OSLO | 31.01.23 |   Nei |
| VARE1 |  | OSLO | 28.02.23 |   Nei |

> [!NOTE]  
> Verdisettingsdatoen settes til siste dag i gjennomsnittskostperioden, som i dette tilfellet er siste dag i måneden.  

Tabellen nedenfor viser de samme varepostene etter at kjørselen **Juster kostverdi - vareposter** er kjørt. Gjennomsnittskosten per måned beregnes og utlignes mot lagerreduksjonene.  

|**Bokføringsdato** | **Vareposttype** | **Antall** | **Kostbeløp (faktisk)** | **Oppføringsnr.** |
|--|--|--|--|--|
| 01.01.23 | Kjøp | 1 | 20.00 | 1 |
| 01.01.23 | Kjøp | 1 | 40.00 | 2 |
| 01.01.23 | Salg | -1 | -30,00 | 3 |
| 01.02.23 | Salg | -1 | -65,00 | 4 |
| 02.02.23 | Kjøp | 1 | 100.00 | 5 |
| 03.02.23 | Salg | -1 | -65,00 | 6 |

Gjennomsnittskosten for løpenummer 3 beregnes i gjennomsnittskostperioden for januar. Gjennomsnittskosten for løpenumre 4 og 6 beregnes i gjennomsnittskostperioden for februar.  

For å få gjennomsnittskosten for februar legger [!INCLUDE [prod_short](includes/prod_short.md)] gjennomsnittskosten for varen som er mottatt på lageret (100,00), til gjennomsnittskosten i begynnelsen av perioden (30,00). Summen (130,00) deles deretter på det totale antallet i lageret (2). Denne beregningen gir den resulterende gjennomsnittskosten for varen i februar-perioden (65,00). Gjennomsnittskosten tilordnes til lagerreduksjonene i perioden (post 4 og 6).  

## Angi datoen for verdisetting

 Feltet **Verdisettingsdato** i **Verdipost**-tabellen fastsetter gjennomsnittskostperioden der en lagerreduksjon hører til. Denne innstillinger gjelder også VIA-beholdning (varer i arbeid).  

 Tabellen nedenfor viser kriteriene som brukes til å angi verdisettingsdatoen.  

| Scenario | Bokføringsdato | Verdisatt antall | Revaluering | Verdisettingsdato |
|--|--|--|--|--|
| 1 |  | Positiv | Nei | Bokføringsdato for varepost |
| 2 | Senere enn siste verdisettingsdatoen for utlignede verdiposter | Negativt | Nei | Bokføringsdato for varepost |
| 3 | Tidligere enn siste verdisettingsdatoen for utlignede verdiposter | Positivt | Nei | Siste verdisettingsdatoen for utlignede verdiposter |
| 4 |  | Negativt | Ja | Bokføringsdato for revalueringspost |

### Eksempel

Tabellen med verdiposter nedenfor illustrerer de forskjellige scenariene.  

| Scenario | Bokføringsdato | Vareposttype | Verdisettingsdato | Verdisatt antall | Kostbeløp (faktisk) | Varepostnr. | Postnr. |
|--|--|--|--|--|--|--|--|
| 1 | 01.01.20 | Kjøp | 01.01.20 | 2 | 20.00 | 1 | 1 |
| 2 | 15.01.20 | (Varegebyr) | 01.01.20 | 2 | 8,00 | 1 | 2 |
| 3 | 01.02.20 | Salg | 01.02.20 | -1 | -14,00 | 2 | 3 |
| 4 | 01.03.20 | (Revaluering) | 01.03.20 | 1 | -4,00 | 1 | 4 |
| 5 | 01.02.20 | Salg | 01.03.20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> Løpenummer 5 i den foregående tabellen, har brukeren skrevet inn en ordre med en bokføringsdato (01.02.20) som kommer før den siste verdisettingsdatoen for utlignede verdiposter (01.03.20). Hvis den tilsvarende verdien i feltet **Kostbeløp (faktisk)** for denne datoen (02-01-20) ble brukt for oppføringen, ville den vært 14,00. Dette fører til en situasjon der lagerantallet er null, men lagerverdien er -4,00.  
>
> For å unngå en slik uoverensstemmelse mellom antall og verdi angis samme dato for verdisettingsdatoen og den siste verdisettingsdatoen for de utlignede verdipostene (01.03.20). Verdien i feltet **Kostbeløp (faktisk)** blir 10,00 (etter revaluering), som betyr at beholdningsantallet er null, og lagerverdien er også null.  

> [!CAUTION]  
> Siden rapporten **Lagerverdisetting** er basert på bokføringsdato, vil rapporten gjenspeile alle uoverensstemmelser mellom antall og verdi i scenarier som i eksemplet ovenfor. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerverdisetting](design-details-inventory-valuation.md).  

Hvis antallet på lager er mindre enn null etter at du bokfører lagerreduksjonen, blir verdisettingsdatoen satt til bokføringsdatoen for lagerreduksjonen. Du kan endre denne når lagerøkningen tas i bruk, i samsvar med reglene som er beskrevet i merknaden tidligere i denne delen.  

## Beregne gjennomsnittskost på nytt

Verdisatte lagerreduksjoner når et vektet gjennomsnitt er enkelt i flere scenarioer:

- Innkjøp faktureres alltid før salg.
- Bokføringer blir aldri bakoverdatert.
- Du har aldri gjort feil.

Virkeligheten er imidlertid forskjellig.  

Som eksemplene i denne artikkelen viser, er verdisettingsdatoen angitt som datoen som verdiposten er inkludert i beregningen av gjennomsnittskosten. Med denne innstillingen kan du gjøre flere ting for varer med lagermetoden Gjennomsnitt:  

- Fakturer for salget av en vare før du fakturerer kjøpet.  
- Tilbakedatere en postering.  
- Gjenopprette en feil bokføring.  

> [!NOTE]  
> En annen årsak til denne fleksibiliteten er fast utligning. Hvis du vil ha mer informasjon om fast utligning, se [Designdetaljer: Vareutligning](design-details-item-application.md).  

På grunn av denne fleksibiliteten må du kanskje beregne gjennomsnittskost etter bokføring. Hvis du for eksempel bokfører en lagerøkning eller -reduksjon med en Verdisettingsdato som er før en lagerreduksjon. Omberegningen av gjennomsnittskosten skjer automatisk når du kjører kjørselen **Juster kostverdi - vareposter** manuelt eller automatisk.  

Du kan endre verdisettingsgrunnlaget for beholdningen i en regnskapsperiode, ved å endre verdiene i feltene **Gjennomsnittskostperiode** og **Beregn.type for gj.snittskost**. Vi anbefaler imidlertid at du bruker forsiktighet og kontakter revisoren.  

### Eksempel på omberegnet gjennomsnittskost

Dette eksemplet viser hvordan [!INCLUDE [prod_short](includes/prod_short.md)] omberegner gjennomsnittskosten når du bokfører på en dato som er før en lagerreduksjon. Eksemplet er basert på gjennomsnittskostperioden **Dag**.  

Tabellen nedenfor viser verdipostene som finnes for varen før bokføringen innføres.  

| Verdisettingsdato | Antall | Kostbeløp (faktisk) | Postnr. |
|--|--|--|--|
| 01.01.20 | 1 | 10.00 | 1 |
| 02.01.20 | 1 | 20.00 | 2 |
| 15.02.20 | -1 | -15,00 | 3 |
| 16.02.20 | -1 | -15,00 | 4 |

Brukeren bokfører en lagerøkning (post nummer 5) med en verdisettingsdato (03.01.20) som kommer før en lagerreduksjon. For å balansere lageret må gjennomsnittskosten beregnes på nytt og justeres til 17,00.  

Tabellen nedenfor viser verdipostene som finnes for varen etter at post nummer 5 er innført.  

| Verdisettingsdato | Antall | Kostbeløp (faktisk) | Postnr. |
|--|--|--|--|
| 01.01.20 | 1 | 10.00 | 1 |
| 02.01.20 | 1 | 20.00 | 2 |
| 03.01.20 | 1 | 21.00 | 5 |
| 15.02.20 | -1 | -17,00 | 3 |
| 16.02.20 | -1 | -17,00 | 4 |

## Se også

[Utformingsdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Utformingsdetaljer: Lagermetoder](design-details-costing-methods.md)  
[Utformingsdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  
[Utformingsdetaljer: Vareutligning](design-details-item-application.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ordliste over termer i Dynamics 365-forretningsprosesser](/dynamics365/guidance/business-processes/glossary)  
[Definer oversikt over produkt- og tjenestekostnader](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
