---
title: Arbeide med dimensjoner | Microsoft-dokumentasjon
description: "Du bruker dimensjoner til å kategorisere poster, for eksempel etter avdeling eller prosjekt, slik at du enkelt kan spore og analysere data."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 844668124df1897493737b28383a68a2a0a66d10
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-dimensions"></a>Arbeide med dimensjoner
Hvis du vil gjøre det enklere å utføre analyser på dokumenter, for eksempel salgsordrer, kan du bruke dimensjoner. Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra.  

Deretter kan du bruke for eksempel dimensjoner i stedet for å definere separate finanskonti for hver avdeling og hvert prosjekt. Dette gir en rik mulighet for analyse, uten å opprette en komplisert kontoplan. Hvis du vil ha mer informasjon, kan du se [Forretningsintelligens](bi.md).

Et annet eksempel er å definere en dimensjon som kalles *Avdeling* og bruker denne dimensjonen når du bokfører salgsdokumenter. Dermed kan du bruke verktøyene for forretningsanalyse til å se hvilken avdeling hvilke varer som er solgt.
Jo flere dimensjoner du bruker, jo mer detaljerte rapporter kan du basere dine forretningsavgjørelser på. En enkelt salgspost kan for eksempel inkludere flere dimensjonsopplysninger som:  

* Kontoen varesalget er bokført til  
* Hvor varen ble solgt
* Hvem som solgte den
* Hva slags kunde som kjøpte den  

> [!NOTE]  
>   Denne funksjonen krever at opplevelsen er satt til **Suite**. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analysere etter dimensjoner
Dimensjoner-funksjonen spiller en viktig rolle i forretningsintelligens, for eksempel når du definerer analysevisninger. Hvis du vil ha mer informasjon, kan du se [Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md).

> [!TIP]
> Som en rask måte å analysere transaksjonsdata etter dimensjoner, kan du filtrere totalene i kontoplanen og postene i alle **Poster**-vinder per dimensjon. Se etter handlingen **Angi dimensjonsfilter**.

## <a name="dimension-sets"></a>Dimensjonssett
Et dimensjonssett er en unik kombinasjon av dimensjonsverdier. Det lagres som dimensjonssettposter i databasen. Hver dimensjonssettpost representerer én enkelt dimensjonsverdi. Dimensjonssettet identifiseres av en felles dimensjonssett-ID som tilordnes hver dimensjonssettpost som tilhører dimensjonssettet.  

Når du oppretter en kladdelinje, et dokumenthode eller en dokumentlinje, kan du angi en kombinasjon av dimensjonsverdier. I stedet for at hver dimensjonsverdi lagres eksplisitt i databasen, tilordnes en dimensjonssett-ID til kladdelinjen, dokumenthodet eller dokumentlinjen for å angi dimensjonssettet.  

## <a name="setting-up-dimensions"></a>Opprette dimensjoner
Du kan definere dimensjonene og dimensjonsverdiene for å kategorisere i kladder og dokumenter, for eksempel salgsordrer og bestillinger. Du definerer dimensjoner i **Dimensjoner**-vinduet der du oppretter én linje for hver dimensjon, som *Prosjekt*, *Avdeling*, *Område* og *Selger*.

Du også definere verdier for dimensjoner. Verdier kan for eksempel være avdelinger i firmaet. Dimensjonsverdier kan defineres i en hierarkisk struktur som ligner på kontoplanen, slik at data kan brytes ned i ulike størrelsesnivåer, og delsett med dimensjonsverdier kan legges sammen. Du kan definere så mange dimensjoner og dimensjonsverdier som du trenger, og alle i firmaet kan bruke dem.

Du kan også definere globale dimensjoner og snarveisdimensjoner:  

* **Globale dimensjoner** brukes som filtre, for eksempel i rapporter og kjørsler. Du kan bruke bare to globale dimensjoner, så velge dimensjonene du vil bruke ofte.
* **Snarveisdimensjoner** er tilgjengelige som felt på journal- og dokumentlinjer. Du kan opprette opptil seks av disse.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Definere standarddimensjoner for kunder, leverandører og andre konti
Du kan tilordne en standarddimensjon for en spesifikk konto. Dimensjonen kopieres til kladden eller bilaget når du angi nummeret på en linje, men du kan slette eller endre koden på linjen, hvis aktuelt. Du kan også gjøre en dimensjon som er nødvendige for postering av en oppføring for en bestemt type konto.  

### <a name="translating-the-names-of-dimensions"></a>Oversette navn på dimensjoner
Når du oppretter en dimensjon, og spesielt en snarveisdimensjon, er hva du faktisk oppretter en egendefinert overskrift for feltet eller kolonnen. Hvis din bedrift er internasjonal, kan du gi oversettelser for navnet på dimensjonen. Dokumenter som inneholder dimensjonen skal bruke det oversatte navnet, der det er aktuelt.   

### <a name="example-of-dimension-setup"></a>Eksempel på dimensjonsoppsett
La oss si at selskapet ønsker å spore transaksjoner som er basert på organisasjonsstruktur og geografiske steder. Hvis du vil gjøre dette, kan du definere to dimensjoner i **Dimensjoner**-vinduet:

* **OMRÅDE**  
* **AVDELING**  

|  - kode | Name | Kodetekst | Filtertekst |
| --- | --- | --- | --- |
| DISTRIKT |Distrikt |Områdekode |Områdefilter |
| AVDELING |Avdeling |Avdelingskode |Avdelingsfilter |

For **OMRÅDE** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| 10 |Amerika |Fra-sum |
| 20 |Nord-Amerika |Standard |
| 30 |Stillehavet |Standard |
| 40 |Sør-Amerika |Standard |
| 50 |Amerika, totalt |Til-sum |
| 60 |Europa |Fra-sum |
| 70 |EU |Standard |
| 80 |Ikke-EU |Standard |
| 90 |Europa, totalt |Til-sum |

For de to viktigste geografiske områdene, Amerika og Europa, kan du legge til underkategorier for områder ved å rykke inn dimensjonsverdiene. Dette gjør at du kan rapportere på salg- eller utgifter i områder, og få totaler for større geografiske områder. Du kan også velge å bruke land eller regioner som dine dimensjonsverdier, eller regioner eller byer, avhengig av virksomheten din.  
> [!NOTE]  
>   Hvis du vil definere et hierarki, må kodene være i alfabetisk rekkefølge. Dette inkluderer kodene for dimensjonsverdiene som tilbys i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

For **AVDELING** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| ADMIN |Administrasjon |Standard |
| PROD |Produksjon |Standard |
| SALG |Salg |Standard |

Med dette satt opp, du deretter legge til de to dimensjonene som to globale dimensjoner i den **Finansoppsett** vindu. Dette betyr at du kan bruke område og avdeling som filtre for finansposter og alle rapporter og kontoskjemaer. Begge de globale dimensjonene blir også automatisk tilgjengelige til å brukes på postlinjer, i dokumenthoder og som snarveisdimensjoner.  

## <a name="using-dimensions"></a>Bruke dimensjoner
I et dokument, for eksempel en ordre, kan du legge til dimensjonsinformasjon om én enkelt dokumentlinje og selve dokumentet. I vinduet **Ordre** kan du for eksempel angi dimensjonsverdier for de to første snarveisdimensjonene direkte på de enkelte salgslinjene, og du kan legge til mer dimensjonsinformasjon hvis du velger knappen **Dimensjoner**.  

Hvis du i stedet arbeider i en kladd, kan du legge til dimensjonsinformasjon i en post på samme måte, forutsatt at du har opprettet snarveisdimensjoner som felt direkte i kladdelinjer.  

Du kan definere standarddimensjoner for konti eller kontotyper, slik at dimensjoner og dimensjonsverdier fylles ut automatisk.

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

