---
title: Skrive inn data i felt | Microsoft-dokumentasjon
description: "Det er mange generelle funksjoner du kan bruke til å skrive inn data raskt og enkelt. De generelle funksjonene for å skrive inn data beskrives i dette emnet."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a>Skrive inn data
Det er mange generelle funksjoner du kan bruke til å skrive inn data raskt og enkelt. De generelle funksjonene for å skrive inn data beskrives i denne artikkelen.  

Eksemplene i denne artikkelen bruker demonstrasjonsdataene.

## <a name="mandatory-fields"></a>Obligatoriske felt
Når du angir data på sider, merkes bestemte felt med en rød stjerne. Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.  

Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden. Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.  


## <a name="finding-data-as-you-type"></a>Finne data mens du skriver  
 Når du begynner å skrive inn tegn i et felt, åpnes en rullegardinliste med mulige feltverdier. Innholdet i listen endres etter hvert som du skriver inn flere tegn, og du kan velge ønsket verdi når den vises.  

 Mange felt har en pil-ned-knapp som du kan velge. Du velger pilen for å få frem en liste over data som kan settes inn i feltet. Knappen har to funksjoner, avhengig av felttype:  

-   Oppslag - viser informasjon fra en annen tabell som du kan sette inn i feltet. Du kan velge én datadel om gangen.  

-   Rullegardin - viser settet med alternativer som finnes for feltet. Du kan bare velge ett av alternativene.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Angi antall ved beregning  
 Når du setter inn tall i antallfelt, for eksempel **Antall**-feltet på en varekladdlinje, kan du angi formelen i stedet for summen.  

## <a name="examples"></a>Eksempler  

-   Hvis du skriver inn 19+19, beregnes feltet til 38.  

-   Hvis du skriver inn 41-9, beregnes feltet til 32.  

-   Hvis du skriver inn 12*4, beregnes feltet til 48.  

-   Hvis du skriver inn 12/4, beregnes feltet til 3.  

## <a name="entering-negative-numbers"></a>Skrive inn negative tall
Du kan angi negative tall på to måter. Tallet -20,5 kan angis som:  

-   -20,5  

    eller
-   20,5-  

 I begge tilfeller registreres beløpet som -20,5.  

 Hvis det siste tegnet i uttrykket er en **++** eller en **--**, blir hele uttrykket registrert med dette tegnet. Eksempel: **10-20+** resulterer i 10 og ikke -10.  

## <a name="entering-dates-and-times"></a>Angi datoer og klokkeslett
Du kan sette inn datoer og klokkeslett i alle felt som er spesifikt tilordnet til datoer (datofelt). Datoene kan skrives inn med eller uten skilletegn.

> [!NOTE]  
> Hvordan du angir dato og klokkeslett på, avhenger av dine **Område**-innstillinger. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Sette inn datoer  
 I et datofelt kan du angi to, fire, seks eller åtte tall:  

-   Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.  

-   Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.  

-   Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.  

 Du kan også angi en dato som en ukedag etterfulgt av et ukenummer og, hvis du vil, et år (for eksempel Man25 eller man25 betyr mandag i uke 25).  

 I stedet for å skrive inn en bestemt dato, kan du skrive inn én av to koder.  

| - kode|Resultat|  
|--------------|----------------|  
|i|Dette er dagens dato (systemdatoen for datamaskinen).|  
|a|Dette er arbeidsdatoen som er satt opp i programmet. Du kan endre arbeidsdatoen ved å se [Endre grunnleggende innstillinger](ui-change-basic-settings.md). Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a>Angi klokkeslett  
 Et vilkårlig skilletegn kan settes inn mellom tidsinndelingene, men det er ikke obligatorisk. Du behøver ikke å skrive inn minutter eller sekunder.  

 Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.  

|Angivelse|Tolkning|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Du må angi to sifre for hver tidsenhet dersom du ikke setter inn et skilletegn.  

## <a name="entering-datetimes"></a>Angi datoer og klokkeslett  
 Når du angir dato og klokkeslett, må du sette inn et mellomrom mellom datoen og klokkeslettet.  

 Tabellen nedenfor viser de forskjellige måtene du kan angi dato og klokkeslett på, og hvordan de tolkes.  

|Post|Tolkning|  
|---------------|------------------------|  
|131202 132455|13.12.02 13.24.55|  
|1.12.02 10|01.12.02 10:00:00|  
|1.12.02 5|12.01.02 05:00:00|  
|1.12.02|01.12.02 00.00.00|  
|11 12|11 - inneværende måned - inneværende år 12.00.00|  
|1112 12|11-12 - inneværende år 12.00.00|  
|i eller i dag|dagens dato 00:00:00|  
|i klokkeslett|dagens dato og klokkeslett|  
|i 10.30|dagens dato 10:30:00|  
|i 3.3.3|dagens dato 03.03.03|  
|a eller arbeidsdag|arbeidsdatoen 00.00.00|  
|m eller mandag|mandag i inneværende uke 00.00.00|  
|ti eller tirsdag|tirsdag i inneværende uke 00:00:00|  
|o eller onsdag|onsdag i inneværende uke 00.00.00|  
|to eller torsdag|torsdag i inneværende uke 00.00.00|  
|f eller fredag|fredag i inneværende uke 00.00.00|  
|l eller lørdag|lørdag i inneværende uke 00.00.00|  
|s eller søndag|søndag i inneværende uke 00.00.00|  
|ti 10.30|tirsdag i inneværende uke 10:30:00|  
|ti 3.3.3|tirsdag i inneværende uke 03.03.03|  

## <a name="entering-duration"></a>Angi varighet  
 Du angir en varighet som et tall etterfulgt av enheten.  

 Her er noen eksempler.  

|Varighet|Enhtet**|  
|------------------|-------------------------|  
|2t|2 timer|  
|6t 30 m|6 timer 30 min|  
|6,5t|6 timer 30 min|  
|90m|1 t 30 min|  
|2d 6t 30m|2 dager 6 timer 30 min|  
|2d 6t 30m 56s 600ms|2 dager 6 timer 30 min 56 sek 600 msek|  

 Du kan også angi et tall, og det blir automatisk konvertert til et tidsintervall. Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.  

 Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.  

 Tallet 5 konverteres til 5 timer hvis enheten er timer.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Bruke datoformler  
 En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer. Du kan angi datoformler i forskjellige datoberegningsfelt og i gjentakende intervallfelt i gjentakende kladder.  

> [!NOTE]  
>  Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag. Hvis du for eksempel angir 1U, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert. Hvis du vil angi en periode på sju dager (én sann uke), inkludert periodens startdato, må du angi 6D eller 1U-1D.  

 Her kommer det noen eksempler på hvordan datoformler kan brukes:  

-   Datoformelen i det gjentakende intervallfeltet i gjentakende kladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.  

-   Datoformelen i feltet Respittid for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen (eller fra forrige purringsdato) før det kan opprettes en purring.  

-   Datoformelen i feltet Beregning av forfallsdato angir hvordan forfallsdatoen i purringen beregnes.  

 Formelen for datoberegning kan inneholde opptil 20 tegn, både tall og bokstaver. Du kan bruke følgende bokstaver, som er forkortelser for tidsangivelser:  

|||  
|-|-|  
|L|Løpende|  
|D|Dag(er)|  
|U|Uke(r)|  
|M|Måned(er)|  
|K|Kvartal(er)|  
|Å|År|  

 Du kan opprette datoformler på tre måter.  

 Eksempelet nedenfor viser løpende pluss en tidsangivelse.  

|||  
|-|-|  
|LU|Løpende uke|  
|LM|Løpende måned|  

 Eksempelet nedenfor viser et tall og en tidsangivelse. Et tall kan ikke være større enn 9999.  

|||  
|-|-|  
|10D|10 dager fra i dag|  
|2U|2 uker fra i dag|  

 Eksempelet nedenfor viser en tidsangivelse og et tall.  

|||  
|-|-|  
|D10|Den neste 10. dag av en måned|  
|UD4|Neste 4. dag av en uke (torsdag)|  

 Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.  

|||  
|-|-|  
|LM+10D|Løpende måned + 10 dager|  

 Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.  

|||  
|-|-|  
|-1Å|1 år siden fra i dag|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Se også  
 [Søke etter, filtrere og sortere data](ui-enter-criteria-filters.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

