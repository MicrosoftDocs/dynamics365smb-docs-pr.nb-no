---
title: Angi datointervaller i Business Central | Microsoft-dokumentasjon
description: "Finn ut hvordan du får en rapport til å vise data fra bestemte tidsperioder ved å bruke datointervaller i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: nb-no
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Sette inn datointervaller
Du kan angi filtre som inneholder en startdato og en sluttdato, for å vise bare dataene innenfor dette datointervallet eller tidsintervallet. Særlige regler gjelder for angivelse av datointervaller. La oss ta **Kunde - ti på topp** som eksempel:

![Angi et datointervall på forespørselssiden for Kunde - ti på topp-listen](./media/ui-enter-date-ranges/customer-top10-list.png)

Her kan du begrense rapporten til et datointervall, for eksempel de to siste ukene eller totalt seks uker, eller et hvilket som helst intervall du vil bruke. Du angir datointervaller ved å angi datoene og deretter bruke **..** eller **|** til å angi intervallet. Hvis du vil vise de ti beste kundene for de to første ukene i mai i eksemplet vårt, setter du datofilteret til *05 01 17..05 14 17*.
Her er noen andre eksempler:

| Betyr | Eksempel | Tar med poster |
|---|---|---|
|Lik| 12 15 16 |Bare de som er bokført 15. desember 2016.|
|Intervall| 12 15 16..01 15 17<br /><br />..12 15 16|De som er bokført på datoer mellom og inkludert 15. desember 2016 og 15. januar 2017.<br /><br />De som er bokført 15. desember 2016 eller tidligere.|
|Enten/eller|12 15 16&#124;12 16 16|De som er bokført 15. eller 16. desember 2016. Hvis det er bokført poster begge dagene, vises alle postene.|

Grunnformene kan også kombineres innbyrdes.

| Eksempel | Tar med poster |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Poster som enten er bokført 15. desember 2016 eller på datoer mellom og inkludert 1. desember 2016 og 31. mai 2017. |
|..12 14 16&#124;12 30 16.. | Poster som er bokført 14. desember eller tidligere, eller poster som er bokført 30. desember eller senere, det vil si alle poster unntatt de som er bokført på datoer mellom og inkludert 15. og 29. desember. |

Vær oppmerksom på at vi har brukt det amerikanske datoformatet MMDDÅÅ her. Etter hvert som [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tilgjengelig på andre markeder, kan du bruke formatene du er vant med.

## <a name="using-date-formulas"></a>Bruke datoformler
En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer. Du kan angi datoformler i forskjellige datoberegningsfelt og i gjentakende intervallfelt i gjentakende kladder.

> [!NOTE]
>  Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag. Hvis du for eksempel angir **1U**, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert. Hvis du vil angi en periode på sju dager (én sann uke), inkludert periodens startdato, må du angi **6D** eller **1U\-1D**.

Her kommer det noen eksempler på hvordan datoformler kan brukes:

-   Datoformelen i gjentakelsesintervallfeltet i gjentakelseskladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.

-   Datoformelen i feltet **Respittid** for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen (eller fra forfallsdato for forrige purring) før det kan opprettes en purring.

-   Datoformelen i feltet **Beregning av forfallsdato** angir hvordan forfallsdatoen i purringen beregnes.

Formelen for datoberegning kan inneholde opptil 20 tegn, både tall og bokstaver. Du kan bruke følgende bokstaver, som er forkortelser for tidsangivelser:

|  Bokstav  |  Tidsspesifisering  |
|----------|----------------------|
|U|Løpende|
|D|Dag\(er\)|
|V|Uke\(r\)|
|M|Måned\(er\)|
|K|Kvartal\(er\)|
|Å|År\(\)|

Du kan opprette datoformler på tre måter.

Eksempelet nedenfor viser hvordan **C** brukes, for løpende, og en tidsangivelse.

|  Uttrykk  |  Betyr  |
|--------------|-----------|
|LU|Løpende uke|
|NM|Løpende måned|

Eksempelet nedenfor viser hvordan et tall og en tidsangivelse brukes. Et tall kan ikke være større enn 9999.

|  Uttrykk  |  Betyr  |
|--------------|-----------|
|10D|10 dager fra i dag|
|2U|2 uker fra i dag|

Eksempelet nedenfor viser hvordan et en tidsangivelse og et tall brukes.

|  Uttrykk  |  Betyr  |
|--------------|-----------|
|D10|Den neste 10. dag av en måned|
|UD4|Neste 4. dag av en uke \(torsdag\)|

Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.

|  Uttrykk  |  Betyr  |
|--------------|-----------|
|LM\+10D|Løpende måned \+10 dager|

Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.

|  Uttrykk  |  Betyr  |
|--------------|-----------|
|-1Å|1 år siden fra i dag|

> [!IMPORTANT]
>  Hvis plasseringen bruker en hovedkalender, tolkes datoformelen du angir, for eksempel i feltet **Leveringstid**, i henhold til arbeidsdager fra kalenderen. For eksempel betyr **1U** sju virkedager.

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md)  
[Angi vilkår i filtre](ui-enter-criteria-filters.md)  

