---
title: Skrive inn data i felt | Microsoft-dokumentasjon
description: Lære om generelle funksjoner som kan hjelpe deg med å registrere data i feltene.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/03/2019
ms.author: jswymer
ms.openlocfilehash: d0fac96313b41a0e41ea96ab4fedd25565498f12
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/06/2019
ms.locfileid: "1621163"
---
# <a name="entering-data"></a>Skrive inn data

Det finnes mange generelle funksjoner som kan hjelpe deg med å registrere data enklere, raskere og mer nøyaktig. De generelle funksjonene for å skrive inn data beskrives i denne artikkelen.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Hurtigtaster

Det finnes flere tastatursnarveier som lar deg jobbe uten musen og utføre raskere dataregistrering, særlig med oppføringer i stor skala og gjentakende tasteoppgaver.

Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigtaster](keyboard-shortcuts.md). Noen av hurtigtastene beskrives i denne artikkelen.

## <a name="QuickEntry"></a>Raskere dataregistrering ved hjelp av hurtigoppføring

Hurtigoppføring er en funksjon som er beregnet på dataregistrering når du bruker tastaturet. Hurtigoppføring fungerer på felt (som på kortsider) og i lister (rader og kolonner). Det er nyttig når du utfører gjentakende skriveoppgaver som krever oppretting av flere poster i rekkefølge, for eksempel en kjørsel for ordrer eller registrering av nye varer.

Det kan være du allerede er kjent med bruk av tabulatortasten for å navigere fra ett felt på en side til neste redigerbare felt. En ulempe ved bruk av tabulatoren er at den alltid går fortløpende til neste felt. <!-- even if the field is non-editable or seldom filled it in.-->Med Hurtigoppføring kan du endre denne banen. Med Hurtigoppføring kan du bruke Enter-tasten til å navigere gjennom feltene du er interessert i, og hoppe over ikke-redigerbare felt og felt du vanligvis ikke fyller ut. Du kan allerede ha oppdaget denne atferden på noen sider. Dette er fordi programmet allerede angir hvilke felt som skal tas med når det trykkes på Enter, og hvilke som skal hoppes over. Du kan tilpasse Hurtigoppføring ved å tilpasse arbeidsområdet og optimalisere hvordan du registrerer data på hver side.

### <a name="how-quick-entry-works"></a>Hvordan Hurtigoppføring fungerer

Alle felt kan merkes som *Ta med i hurtigoppføring* eller *Utelat fra hurtigoppføring*. Felt som er inkludert i hurtigoppføringen, inkluderes i banen når du trykker på Enter. Felt som er ekskludert fra hurtigoppføringen, inkluderes ikke.

Når du er ferdig med å registrere data i et felt, kan du ganske enkelt trykke Enter for å bekrefte endringene og gå til neste felt. Hvis du vil reversere retningen og gå til forrige felt, trykker du på Skift+Enter. Hvis du vil ha mer informasjon om snarveier, kan du se [Hurtigreferanse for tastatursnarveier for felt](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips og triks
Nedenfor finner du nyttig informasjon om hvordan du bruker Hurtigoppføring.

- Funksjonen er tilgjengelig for alle redigerbare felt.
- Den fungerer også i kolonner og rader.
- Den hindrer ikke tilgang til andre elementer på en side, for eksempel handlinger. Disse er fortsatt tilgjengelige ved hjelp av tabulatoren og Skift+Tab.  
- Hurtigfaner trenger ikke å utvides for at Hurtigoppføring skal fungere. Hvis det neste Hurtigoppføring-feltet befinner seg i en skjult hurtigfane, vil denne hurtigfanen utvides automatisk og fokusere på det valgte feltet.
- Hurtigoppføring fungerer uavhengig av om felt er obligatoriske. Derfor er det lurt å sikre at obligatoriske felt er inkludert i Hurtigoppføring.
- Som standard inkluderes de fleste feltene automatisk i Hurtigoppføring. Så i starten vil oppgaven din sannsynligvis eksludere felt fra Hurtigoppføring.

### <a name="how-to-change-quick-entry-fields"></a>Endre Hurtigoppføring-felt

Hvis du vil endre hvilke felt som inkluderes i eller utelates fra Hurtigoppføring på en side, kan du bruke tilpasning.

1. Start tilpasningen ved å velge ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikonet for rollesenteret"), og klikk deretter **Tilpass**.
2. Velg et felt som du vil endre, eller velg tilsvarende kolonneoverskrift i lister, og velg deretter **Ta med i hurtigoppføring** eller **Utelat fra hurtigoppføring**.

Hvis du vil ha mer informasjon om tilpasning, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Obligatoriske felt

Når du angir data på sider, merkes bestemte felt med en rød stjerne. Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.  

Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden. Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.  

## <a name="finding-data-as-you-type"></a>Finne data mens du skriver

 Når du begynner å skrive inn tegn i et felt, åpnes en rullegardinliste med mulige feltverdier. Innholdet i listen endres etter hvert som du skriver inn flere tegn, og du kan velge ønsket verdi når den vises.  

 Mange felt har en pil-ned-knapp som du kan velge. Du velger pilen for å få frem en liste over data som kan settes inn i feltet. Knappen har to funksjoner, avhengig av felttype:  

-   Oppslag - viser informasjon fra en annen tabell som du kan sette inn i feltet. Du kan velge én datadel om gangen.  

-   Rullegardin - viser settet med alternativer som finnes for feltet. Du kan bare velge ett av alternativene.  

## <a name="copying-and-pasting-fields-and-lines"></a>Kopiere og lime inn felt og linjer

Du kan kopiere en eller flere rader fra en oversikt eller ett enkelt felt på en side og deretter lime inn det du kopierte, på samme side, en annen side eller et eksternt dokument (som Microsoft Excel og Outlook-e-post). Kort sagt, for å kopiere trykker du CTRL+C (cmd+C i macOS) på tastaturet. For å lime inn trykker du CTRL+V (cmd+V i macOS).

Trykk på F8 i listen for å kopiere feltet i den samme kolonnen i raden over, og lim det inn i den gjeldende raden.

Hvis du vil ha mer informasjon, kan du se [Kopiere og lime inn i Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Fokusere på linjeelementer

Når du arbeider med dokumenter som inkluderer en linjeelementdel, som en ordre- eller fakturaside, kan du bytte visningen slik at fokus endres til bare linjeelementene, og hovedsakelig utvide linjeelementdelen, slik at den opptar så godt som hele arbeidsområdet og skjuler andre deler av siden bortsett fra handlingsområdet øverst. Dette gir deg bedre oversikt over linjelementene og gir mer plass til å arbeide med dem. Dette er særlig nyttig når du arbeider med store linjeelementlister og rask dataregistrering er ønskelig.

En annen fordel er at det også gir deg avanserte filtreringsmuligheter, som i andre oversikter, så sporing og søk gjennom linjeelementer blir enda enklere.

### <a name="switching-the-focus-on-and-off"></a>Bytte fokus på og av

Når du skal fokusere på linjeelementer, velger du hvor som helst i linjeelementdelen og velger deretter ![Fokusmodusikon](media/focus-mode.png "Fokusmodusikon") øverst til høyre, eller trykk på Ctrl+Skift+F12.

Hvis du vil gå tilbake til den normale visningen, kan du velge ![Fokusmodusikon](media/focus-mode.png "Fokusmodusikon"), eller trykk på Ctrl+Skift+F12 på nytt.

### <a name="filtering-the-line-items"></a>Filtrere linjeelementer

For å starte filtreringen kan du velge ![Filtreringsruteikon](media/open-filter-pane-icon.png "Filtreringsruteikon") øverst i oversikten eller trykke på **Skift+F3** for å åpne filtreringsruten. Du arbeider med filtreringsruten som i andre oversikter. Hvis du vil ha mer informasjon, kan du se [Filtrering](ui-enter-criteria-filters.md#Filtering).

Filtrere er spesielt nyttig når du viser og analysere lengre dokumenter. Tenk deg at du åpner en bokført salgsfaktura og filtrerer linjeelementene for å vise alle linjeelementer som har en individuell rabatt på mer enn 5 %, eller filtrer for å vise bare sykkeltilbehør med "pro" i navnet.

## <a name="entering-quantities-by-calculation"></a>Angi antall ved beregning

Når du setter inn tall i antallfelt, for eksempel **Antall**-feltet på en varekladdlinje, kan du angi formelen i stedet for summen.  

### <a name="examples"></a>Eksempler  

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

For datofelt kan du bruke datavelgeren, som lar deg velge en dato fra en kalender, eller du kan angi datoer manuelt. Denne delen inneholder en kort oversikt over hvordan du angir datoer. Hvis du vil ha mer informasjon, se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).

For manuell datoregistrering kan du angi to, fire, seks eller åtte tall:  

-   Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.  

-   Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.  

-   Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.  

Du kan også angi en dato som en ukedag etterfulgt av et ukenummer og, hvis du vil, et år (for eksempel Man25 eller man25 betyr mandag i uke 25).  

I stedet for å skrive inn en bestemt dato kan du skrive inn én av disse kodene.  

| - kode|Resultat|  
|--------------|----------------|  
|i|Dette angir dagens dato (systemdatoen for datamaskinen).|  
|P|Dette angir en regnskapsperiode der `p` betyr at den første regnskapsperioden, `p2` betyr den andre andre regnskapsperioden og så videre. |
|a|Dette angir arbeidsdatoen som er satt opp i programmet. Du kan endre arbeidsdatoen ved å se [Endre grunnleggende innstillinger](ui-change-basic-settings.md). Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.|
|c|Dette angir at datoen etter `c` er en avslutningsdato, for eksempel `C123101`.|  

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
|t eller i dag|dagens dato 00:00:00|  
|klokkeslett|dagens dato og klokkeslett|  
|k 10.30|dagens dato 10:30:00|  
|k 3.3.3|dagens dato 03.03.03|  
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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Se også  
 [Sortere, søke etter og filtrere oversikter](ui-enter-criteria-filters.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
