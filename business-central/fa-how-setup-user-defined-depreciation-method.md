---
title: Slik definerer du brukerdefinerte avskrivningsmetoder
description: I Business Central kan du bruke en brukerdefinert avskrivningsmetode til å definere avskrivningsmetoden for aktivumet på siden Aktivakort.
author: jill-kotel-andersson
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: bholtorf
---

# Slik definerer du aktiva med brukerdefinerte avskrivningsmetoder

Du kan bruke [!INCLUDE[prod_short](includes/prod_short.md)] til å definere de brukerdefinerte avskrivningsmetodene som beskrevet her.

For hver brukerdefinerte metode bruker du siden **Avskrivningstabeller** til å angi en prosentsats for avskrivning for hver enkelt periode (måned, kvartal, år og regnskapsperiode). Når du deretter tilordner et avskrivningstablå med en brukerdefinert metode til et aktivum, må du angi feltene **Første brukerdef. avskr.dato** og **Startdato for avskrivning** på siden **Aktivaavskrivningstablå** for det spesifikke aktivumet.  

Formelen for beregning av avskrivningsbeløp er følgende:  

*Avskrivningsbeløp = (Avskrivnings-% x Antall avskrivningsdager x Avskrivningsgrunnlag ) / (100 x 360)*


> [!NOTE]  
> Mens det er datoen i feltet **Første brukerdef. avskr.dato** som brukes til å bestemme tidsintervallet, er det **Startdato for avskrivning** som brukes til å bestemme antall avskrivningsdager. Hvis verdien i feltet **Første brukerdef. avskr.dato** kommer før verdien i feltet **Startdato for avskrivning**, blir prosentsatsen for den første perioden i avskrivningstabellen bare delvis brukt når programmet beregner den første avskrivningen. Dette betyr at aktivumet blir fullstendig avskrevet innen slutten av den siste perioden.

## Slik tilordner du et avskrivningstablå til et aktivum med en brukerdefinert avskrivningsmetode

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet som du vil definere et aktivaavskrivningstablå for.
3. Velg handlingen **Tilknyttet**, og velg deretter **Aktiva** og **Avskrivningstablåer**. Dette åpner siden **Aktivaavskrivningstablå**.

   Som standard er noen av feltene som må fylles ut per instruksjonene nedenfor, skjult slik at du må vise dem. Du må tilpasse siden for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).
4. Velg **Brukerdefinert** i feltet **Avskrivningsmetode**.
5. Velg **avskrivningstabellen** du vil bruke, i feltet **Tabellkode for avskrivning**.
6. I feltet **Startdato for avskrivning** velger du startdato for avskrivningsberegningen.
7. Når du bruker en brukerdefinert metode, må feltet **Første brukerdef. avskr.dato** settes til en dato som er den samme eller tidligere enn feltet **Startdatoen for avskrivning**. Hvis du har valgt en verdi i feltet **Periodelengde** i avskrivningstabellen, må datoen i feltet **Første brukerdef. avskr.dato** være startdatoen for en regnskapsperiode.
8. Du må fylle ut feltet **Antall avskrivningsår** eller feltet **Sluttdato for avskrivning**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## Slik definerer du brukerdefinerte avskrivningsmetoder

På **Avskrivningstabell**-siden kan du opprette brukerdefinerte avskrivningsmetoder. Du kan for eksempel definere avskrivning basert på antall enheter.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstabeller**, og velg deretter den relaterte koblingen.  
2. På siden **Avskrivningstabell - oversikt** velger du handlingen **Ny**.  
3. På siden **Avskrivningstabellkort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Bruk funksjonen **Opprett sum av sifre - tabell** til å definere en avskrivningstabell basert på metoden *Sum av sifre*.

Hvis et aktivum avskrives over 4 år med metoden *Sum av sifre*, blir avskrivningen for hvert år beregnet på følgende måte:

Sum av sifre = 1 + 2 + 3 + 4 = 10 avskrivning:

* År 1 = 4/10  
* År 2 = 3/10  
* År 3 = 2/10  
* År 4 = 1/10  

### Avskrivning etter antall enheter

Denne brukerdefinerte metoden kan også anvendes til avskrivning som er basert på antall enheter, for eksempel hvis du har produksjonsmaskiner med fastlagt levetidskapasitet. På siden **Avskrivningstabeller** kan du angi hvor mange enheter som kan produseres i hver periode (måned, kvartal, år eller regnskapsperiode).  

### Eksempel – brukerdefinert avskrivning

Bruk en avskrivningsmetode som gjør det mulig å foreta en hurtig avskrivning av aktiva på grunn av skattemessige årsaker.  

For aktiva med en levetid på tre år bruker du av skattemessige årsaker følgende avskrivningssatser:  

* År 1: 25 %  
* År 2: 38 %  
* År 3: 37 %  

Anskaffelseskostnadene er LV 100 000, og avskrivningslevetiden er fem år. Avskrivningen beregnes årlig.  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |360 |-25 000,00 |75,000.00 |
| 12/31/21 |Avskrivning |360 |-38 000,00 |37,000.00 |
| 12/31/22 |Avskrivning |360 |-37 000,00 |0 |
| 12/31/23 |Avskrivning |Ingen |Ingen |0 |
| 12/31/24 |Avskrivning |Ingen |Ingen |0 |

I det forrige eksemplet ville både feltet **Første brukerdef. avskr.dato** og **Startdato for avskrivning** blitt satt til 01/01/20 på siden **Aktivaavskrivningstablå** for det spesifikke aktivumet. Hvis feltet **Første brukerdef. avskr.dato** imidlertid inneholdt 01/01/20 og feltet **Startdato for avskrivning** inneholdt 04/01/20, ville resultatet vært følgende:  

| Dato | Aktivabokf.type | dager | Beløp | Bokført verdi |
| --- | --- | --- | --- | --- |
| 01/01/20 |Anskaffelseskost |(Startdato for avskrivning) |100,000.00 |100,000.00 |
| 12/31/20 |Avskrivning |270 |-18 750,00 |81,250.00 |
| 12/31/21 |Avskrivning |360 |-38 000,00 |42,250.00 |
| 12/31/22 |Avskrivning |360 |-37 000,00 |6,250.00 |
| 12/31/23 |Avskrivning |90 |-6 250,00 |0 |
| 12/31/24 |Avskrivning |Ingen |Ingen |0 |


## Se også
[Definere aktiva](fa-setup.md)  
[Aktiva](fa-manage.md)  
[Definere avskrivning for aktiva](fa-how-setup-depreciation.md)  
[Avskrivningsmetoder for aktiva](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
