---
title: Betalingstoleranse og toleransegrense for kontantrabatt | Microsoft-dokumentasjon
description: "Du kan konfigurere betalingstoleranse til å lukke en faktura når betalingen ikke fullt ut dekker fakturabeløpet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c6365507992b75d5fa264491bbc85bb1b4a8ed7a
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-work-with-payment-tolerances-and-payment-discount-tolerances"></a>Arbeide med betalingstoleranser og toleransegrenser for kontantrabatt
Du kan konfigurere en betalingstoleranse for å lukke en faktura når betalingen ikke fullt ut dekker fakturabeløpet. Du kan definere en kontantrabattoleranse til å gi rabatt etter at kontantrabattdatoen er passert.  

Du kan bruke betalingstoleranser slik at alle utestående beløp har en definert maksimalt tillatt betalingstoleranse. Hvis betalingstoleransen oppfylles, analyseres beløpet. Hvis beløpet er en underbetaling, lukkes utestående beløp helt av underbetalingen. En detaljert post bokføres til betalingsposten, slik at det ikke blir noe restbeløp igjen på den utlignede fakturaposten. Hvis beløpet er en overbetaling, bokføres en ny detaljert post i betalingsposten, slik at det ikke blir noe restbeløp igjen på betalingsposten.

Du kan bruke toleransegrenser for kontantrabatt slik at hvis du godtar kontantrabatt etter kontantrabattdatoen, så bokføres den alltid på kontantrabattkontoen eller en betalingstoleransekonto.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Bruke betalingstoleranse for flere dokumenter  
Et enkelt dokument har den samme betalingstoleransen enten det utlignes for seg selv eller sammen med andre dokumenter. Godkjenning av en forsinket kontantrabatt når du bruker betalingstoleranse på flere dokumenter, skjer automatisk for hvert dokument der følgende regel er sann:  

*kontantrabattdato < betalingsdato på den valgte posten <= betalingstoleransedato*  

Denne regelen gjelder også for å avgjøre om du vil vise advarsler når du bruker betalingstoleranse med flere dokumenter. Advarsel om betalingstoleranse vises for hver post som oppfyller datokriteriene. Hvis du vil ha mer informasjon, kan du se delen "Eksempel 2 – toleranseberegninger for flere dokumenter".

Du kan velge å vise en advarsel som er basert på ulike toleransesituasjoner.  

- Den første advarselen gjelder kontantrabattoleranse. Du blir informert om at du kan godta kontantrabatt ved sen betaling. Deretter kan du velge om det skal godtas toleranse på rabattdatoen.  
- Den andre advarselen gjelder betalingstoleranse. Du blir informert om at alle poster kan lukkes fordi differansen er innenfor summen av maksimum betalingstoleranse for de utlignede postene. Deretter kan du velge om det skal godtas toleranse på beløpet.

Hvis du vil ha mer informasjon, kan du se delen "Slik aktiverer eller deaktiverer du advarsler om betalingstoleranse".     

## <a name="to-set-up-tolerances"></a>Slik definerer du toleranser  
Med toleransegrenser for dager og beløp kan du lukke en faktura selv om betalingen ikke fullt ut dekker fakturabeløpet. Dette gjelder også for refusjoner og kreditnotaer.  

Når du skal definere toleranse, må du definere forskjellige toleransebeløp, angi både toleransegrense for kontantrabatt og bokføringsmetode for betalingstoleranse, og kjøre kjørselen **Endre betalingstoleranse**.  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2. I vinduet **Generelt bokføringsoppsett** definerer du en debet- og kredittoleransekonto for kontantbetaling ved salg, og en debet- og kreditkonto for kontantbetaling ved kjøp.  
3. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokføringsgrupper - kunde**, og velg deretter den relaterte koblingen.    
4. I vinduet **Bokføringsgrupper - kunde** definerer du en betalingstoleransekonto for debet og kredit. Hvis du vil ha mer informasjon, kan du se [Definere bokføringsgrupper](finance-posting-groups.md).  
5. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Generelt bokføringsoppsett**, og velg deretter den relaterte koblingen.  
6. I vinduet **Bokføringsgrupper - leverandør** definerer du en betalingstoleransekonto for debet og kredit.  
7. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finansoppsett**, og velg deretter den relaterte koblingen.  
8. Åpne **Finansoppsett**-vinduet.  
9. På hurtigfanen **Utligning** fyller du ut feltene **Bokf. av kont.rab.toleranse**, **Respittid for kontantrabatt** og **Betalingstoleransebokføring**.   
10. Velg **Endre betalingstoleranse**-handlingen.
11. I vinduet **Endre betalingstoleranse** fyller du ut feltene **Betalingstoleransepst.** og **Maks. betalingstoleransebeløp**, og deretter velger du **OK**-knappen.

> [!IMPORTANT]  
>  Du har nå definert bare toleranser for den lokale valutaen. Hvis du vil at [!INCLUDE[d365fin](includes/d365fin_md.md)] skal behandle betalingstoleranser for betalinger, kreditnotaer og refusjoner for fremmede valutaer, må du kjøre kjørselen **Endre betalingstoleranse** med en verdi i **Valutakode**-feltet.  

> [!NOTE]  
>  Hvis du vil motta en betalingstoleranseadvarsel hver gang du bokfører en utligning innenfor toleransen, må du aktivere betalingstoleranseadvarselen. Hvis du vil ha mer informasjon, kan du se delen "Slik aktiverer eller deaktiverer du advarsler om betalingstoleranse".  
>   
>  Hvis du vil deaktivere toleranse for en kunde eller en leverandør, må du sperre for toleranser på det aktuelle kunde- eller leverandørkortet. Hvis du vil ha mer informasjon, kan du se delen "Slik sperrer du for betalingstoleranse for kunder".  
>   
>  Når du definerer toleranse, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)] også om det er noen åpne poster, og beregner toleranse for disse postene.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Slik aktiverer eller deaktiverer du advarsler om betalingstoleranse
Melding om betalingstoleranse vises når du bokfører en utligning som har en saldo innenfor tillatt toleranse. Deretter kan du velge hvordan du vil bokføre og dokumentere saldoen.    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finansoppsett**, og velg deretter den relaterte koblingen.  
2. I **Finansoppsett**-vinduet, på hurtigfanen **Utligning**, merker du av for **Betalingstoleranse - advarsel** for å aktivere advarselen. Fjern merket når du skal deaktivere meldingen.  

> [!NOTE]  
>  Standardalternativet for vinduet **Betalingstoleranse - advarsel** er **La saldoen stå som restbeløp**. Standardalternativet for vinduet **Kont.rab.toleranse - advarsel** er **Ikke godta den forsinkede kontantrabatten**.

## <a name="to-block-payment-tolerance-for-customers"></a>Slik sperrer du for betalingstoleranse for kunder  
Standardinnstillingen for betalingstoleranse er tillatt. For å avvise bruk av betalingstoleranse for en bestemt kunde eller leverandør, må du sperre for toleranse på det respektive kunde- eller leverandørkortet. Nedenfor beskrives det hvordan du gjør det for en kunde. Trinnene er de samme for en leverandør.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.  
2. På hurtigfanen **Betalinger** merker du av for **Sperr for betalingstoleranse**.  

> [!NOTE]  
>  Hvis kunden eller leverandøren har åpne poster, må du først fjerne betalingstoleranse fra poster som for øyeblikket er åpne.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Eksempel 1 - toleranseberegninger for ett dokument
Nedenfor følger noen eksempelscenarier som viser de forventede toleranseberegningene og bokføringene som forekommer i forskjellige situasjoner.  

Vinduet **Finansoppsett** inneholder følgende oppsett:
- Respittid for kontantrabatt:    5D  
- Maks. betalingstoleranse:     5  

Scenarier med alternativ A eller B representerer følgende:  

- **A** – I dette tilfellet er advarselen om rabattoleranse deaktivert, ELLER brukeren har advarselen aktivert og har valgt å tillate kontantrabatten ved sen betaling (bokføre saldoen som betalingstoleranse).  
- **B** – I dette tilfellet har brukeren aktivert advarselen og har valgt ikke å tillate kontantrabatt ved sen betaling (la saldoen stå som restbeløp).  

[!div class="mx-tdBreakAll"]  
|—|Fakt.|Kont.rabatt|Maks. betalingstoleranse|Kont.rabattdato|Kont.rab.toler. Dato|Betalingsdato|Bet.|toleransetype|Alle poster lukket|Kont.rab.toler. GL/CL|Bet.toleranse Finans|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1 000|20|5|15.01.03|20.01.03|<=15.01.03|985|Bet.toleranse|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**15.01.03**|**20.01.03**|**<=15.01.03**|**980**|**Ingen**|**Ja**|**0**|**0**|  
|3|1 000|20|5|15.01.03|c|<=15.01.03|975|Bet.toleranse|Ja|0|5|  
|4A|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|1005|Kont.rab.tol.|Nei, 25 på Bet.|20/-20|0|  
|5A|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|1000|Kont.rab.tol.|Nei, 20 på Bet.|20/-20|0|  
|6A|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|995|Kont.rab.tol.|Nei, 15 på Bet.|20/-20|0|  
|4B|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|1005|Bet.toleranse|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15.01.03**|**20.01.03**|**16.01.03 – 20.01.03**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|6B|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|995|Bet.toleranse|Ja|0|5|  
|7|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|985|Kont.rab.tol. & Bet.tol.|Ja|20/-20|-5|  
|8|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|980|Kont.rab.tol.|Ja|20/-20|0|  
|9|1 000|20|5|15.01.03|20.01.03|16.01.03 – 20.01.03|975|Kont.rab.tol. & Bet.tol.|Ja|20/-20|5|  
|10|1 000|20|5|15.01.03|20.01.03|>20.01.03|1005|Bet.toleranse|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**15.01.03**|**20.01.03**|**>20.01.03**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|12|1 000|20|5|15.01.03|20.01.03|>20.01.03|995|Bet.toleranse|Ja|0|5|  
|13|1 000|20|5|15.01.03|20.01.03|>20.01.03|985|Ingen|Nei, 15 på fakturaen|0|0|  
|14|1 000|20|5|15.01.03|20.01.03|>20.01.03|980|Ingen|Nei, 20 på fakturaen|0|0|  
|15|1 000|20|5|15.01.03|20.01.03|>20.01.03|975|Ingen|Nei, 25 på fakturaen|0|0|  

### <a name="payment-range-diagrams"></a>Betalingsseriediagrammer  
I forhold til scenariet ovenfor, er diagrammene for betalingsserier slik:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalingsdato <=15.01.03 (scenariene 1-3)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for én betalingstoleranse &#40;før 03&#47;15&#41;](media/singlePmtTolRules(Pre1503).gif "singlePmtTolRules(Pre1503)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Betalingsdato er mellom 16.01.03 og 21.01.03 (scenariene 4-9)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for én betalingstoleranse rules &#40;respittid&#41;](media/singlePmtTolRules(GracePeriod).gif "singlePmtTolRules(GracePeriod)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Betalingsdato er etter 20.01.03 (Scenariene 10-15)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for én betalingstoleranse &#40;før 01&#47;20&#41;](media/singlePmtTolRules(Post0120).gif "singlePmtTolRules(Post0120)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Eksempel 2 - toleranseberegninger for flere dokumenter
Nedenfor følger noen eksempelscenarier som viser de forventede toleranseberegningene og bokføringene som forekommer i forskjellige situasjoner. Eksemplene er begrenset til bare scenarier som resulterer i at alle poster i utligningen blir lukket.  

Vinduet **Finansoppsett** inneholder følgende oppsett:
- Respittid for kontantrabatt    5D  
- Maks. betalingstoleranse                5  

Scenarier med alternativ A, B, C eller D representerer følgende:  

- **A** – I dette tilfellet er advarselen om rabattoleranse deaktivert, ELLER brukeren har advarselen aktivert og har valgt å tillate kontantrabatten ved sen betaling (bokføre som toleranse) for alle fakturaer.  
- **B** – I dette tilfellet har brukeren aktivert advarselen og har valgt ikke å tillate kontantrabatt ved sen betaling, for alle fakturaer.  
- **C** - I dette tilfellet har brukeren varslet påslått, og har valgt å tillate kontantrabatt ved sen betaling, for første faktura, men ikke den neste.  
- **D** – I dette tilfellet har brukeren varslet påslått, og har valgt å ikke tillate kontantrabatt ved sen betaling, for første faktura, men tillate det for den neste.  

[!div class="mx-tdBreakAll"]  

|—|Fakt.|Kont.rab.|Maks. betalingstoleranse|Kont.rabattdato|Kont.rab.toler. Dato|Betalingsdato|Bet.|toleransetype|Alle poster lukket|Kont.rab.toler. GL/CL|Bet.toleranse Finans|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|<=15.01.03|1920|Bet.toleranse|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.03** <br />**01/17/03**|**20.01.03** <br />**01/22/03**|**<=15.01.03**|**1910**|**Ingen**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|<=15.01.03|1900|Bet.toleranse|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|16.01.03 – 17.01.03|1980|Bet.toleranse|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.03** <br />**01/17/03**|**20.01.03** <br />**01/22/03**|**16.01.03 – 17.01.03**|**1970**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|16.01.03 – 17.01.03|1960|Bet.toleranse|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|16.01.03 – 17.01.03|1920|Kont.rab.tol. & Bet.tol.|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|16.01.03 – 17.01.03|1910|Kont.rab.tol.|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|16.01.03 – 17.01.03|1900|Kont.rab.tol. & Bet.tol.|Ja|60/60|5 <br />5|  
|10B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|2010|Bet.toleranse|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.03** <br />**01/17/03**|**20.01.03** <br />**01/22/03**|**18.01.03 – 20.01.03**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1990|Bet.toleranse|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1980|Kont.rab.tol. & Bet.tol.|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1970|Kont.rab.tol.|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1960|Kont.rab.tol. & Bet.tol.|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1950|Kont.rab.tol. & Bet.tol.|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1940|Kont.rab.tol.|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1930|Kont.rab.tol. & Bet.tol.|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1920|Kont.rab.tol. & Bet.tol.|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1910|Kont.rab.tol.|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|18.01.03 – 20.01.03|1900|Kont.rab.tol. & Bet.tol.|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|21.01.03 – 22.01.03|2010|Bet.toleranse|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.03** <br />**01/17/03**|**20.01.03** <br />**01/22/03**|**21.01.03 – 22.01.03**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|21.01.03 – 22.01.03|1990|Bet.toleranse|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|21.01.03 – 22.01.03|1980|Kont.rab.tol. & Bet.tol.|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|21.01.03 – 22.01.03|1970|Kont.rab.tol.|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|21.01.03 – 22.01.03|1960|Kont.rab.tol. & Bet.tol.|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|>22.01.03|2010|Bet.toleranse|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15.01.03** <br />**01/17/03**|**20.01.03** <br />**01/22/03**|**>22.01.03**|**2000**|**Ingen**|**Ja**|**0**|**0**|  
|30|1 000 <br />1 000|60 <br />30|5 <br />5|15.01.03 <br />17.01.03|20.01.03 <br />22.01.03|>22.01.03|1990|Bet.toleranse|Ja|0|5|  

### <a name="payment-range-diagrams"></a>Betalingsseriediagrammer  
I forhold til scenariet ovenfor, er diagrammene for betalingsserier slik:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalingsdato <=15.01.03 (scenariene 1-3)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for flere betalingstoleranser &#40;før 03&#47;15&#41;](media/multiplePmtTolRules(Pre1503).gif "multiplePmtTolRules(Pre1503)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Betalingsdato er mellom 16.01.03 og 17.01.03 (scenariene 4-9)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for flere betalingstoleranser &#40;respittid&#41;](media/multiplePmtTolRules(GracePeriodInv1).gif "multiplePmtTolRules(GracePeriodInv1)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Betalingsdato er mellom 18.01.03 og 20.01.03 (scenariene 10-21)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for flere betalingstoleranser &#40;respittid&#41;](media/multiplePmtTolRules(GracePeriodInv1-2).gif "multiplePmtTolRules(GracePeriodInv1-2)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Betalingsdato er mellom 21.01.03 og 22.01.03 (scenariene 22-27)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for flere betalingstoleranser &#40;respittid&#41;](media/multiplePmtTolRules(GracePeriodInv2).gif "multiplePmtTolRules(GracePeriodInv2)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Betalingsdato er etter 22.01.03 (scenariene 28-30)  
Restbeløp per  

Vanlige utligningsregler  

![Regler for flere betalingstoleranser &#40;etter 01&#47;22&#41;](media/multiplePmtTolRules(Post0122).gif "multiplePmtTolRules(Post0122)")  

(1) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes med eller uten toleranse.  

(2) Hvis betalinger faller innenfor disse områdene, kan alle utligningsposter lukkes, selv med toleranse.

## <a name="see-also"></a>Se også  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

