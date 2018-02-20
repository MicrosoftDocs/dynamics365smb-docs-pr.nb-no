---
title: Arbeide med dimensjoner | Microsoft-dokumentasjon
description: "Du bruker dimensjoner til å kategorisere poster, for eksempel etter avdeling eller prosjekt, slik at du enkelt kan spore og analysere data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f9a6d577138fcffa338ce51f0abaa45c63c520f7
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

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

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Dimensjoner**, og velg deretter den relaterte koblingen.  
2.  Velg den relevante dimensjonen i vinduet **Dimensjoner**, og velg deretter handlingen **Kontotypens standarddim.**.  
4.  Fyll ut en linje for hver ny standarddimensjon du vil definere. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Hvis du vil gjøre en dimensjon nødvendig, men uten å tilordne en standardverdi til dimensjonen, lar du feltet **Dimensjonsverdikode** være tomt, og deretter velger du **Obligatorisk kode** i feltet **Verdibokføring**.  

> [!WARNING]  
>  Hvis en konto brukes i kjørselen **Juster valutakurser** eller i **Bokfør lagerkost i Finans**, må du ikke velge **Obligatorisk kode** eller **Samme kode**. Disse kjørslene kan ikke bruke dimensjonskoder.  

> [!NOTE]  
>  Hvis det må tilordnes andre dimensjoner til en konto enn den standarddimensjonen som allerede er opprettet for kontotypen, må du opprette en standarddimensjon for denne kontoen. Standarddimensjonen for den enkelte kontoen erstatter da standarddimensjonen for kontotypen.  

### <a name="to-set-up-default-dimension-priorities"></a>Slik setter du opp standard dimensjonsprioriteringer  
Ulike kontotyper, for eksempel en kundekonto og en varekonto, kan ha ulike standarddimensjoner. Følgelig kan en post ha mer enn én alternativ standarddimensjon for en dimensjon. For å unngå en slik konflikt, kan du sette opp prioriteringsregler for de ulike kildene.  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Standarddimensjonsprioriteter**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Standarddimensjonsprioriteter**, i **Kildekode**-feltet, angir du kildesporet for posttabellen som standarddimensjonsprioriteter skal gjelde for.  
3.  Fyll ut en linje for hver standarddimensjonsprioritet du vil bruke for det valgte kildesporet.
4.  Gjenta prosedyren for hvert kildespor du vil definere standarddimensjonsprioriteter for.  

> [!IMPORTANT]  
>  Hvis du definerer to tabeller med samme prioritet for samme kildespor, velger [!INCLUDE[d365fin](includes/d365fin_md.md)] alltid tabellen med lavest tabell-ID.  

### <a name="to-set-up-dimension-combinations"></a>Slik definerer du dimensjonskombinasjoner  
For å unngå å bokføre poster med mostridende eller uaktuelle dimensjoner, kan du sperre eller begrense bestemte kombinasjoner av to dimensjoner. Hvis en dimensjonskombinasjon sperres, kan du ikke bokføre begge dimensjoner på samme post uansett hva dimensjonsverdiene er. En dimensjonskombinasjon lar deg bokføre begge dimensjonene på samme post, men bare for bestemte kombinasjoner av dimensjonsverdier.

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Dimensjonskombinasjoner**, og velg deretter den relaterte koblingen.  
2.  Velg feltet for dimensjonskombinasjonen i vinduet **Dimensjonskombinasjoner**, og velg ett av alternativene nedenfor.  

    |Felt|Description|
    |----------------------------------|---------------------------------------|  
    |**Ingen begrensning**|Denne dimensjonskombinasjonen har ingen begrensninger. Alle dimensjonsverdiene er tillatt.|  
    |**Begrenset**|Denne dimensjonskombinasjonen har begrensninger som avhenger av hvilke dimensjonsverdier du angir. Du må definere begrensningene i vinduet **Dimensjonsverdikombinasjoner**.|  
    |**Sperret**|Denne dimensjonskombinasjonen er ikke tillatt.|  

3.  Hvis du valgte alternativet **Begrenset**, må du definere hvilke kombinasjoner av dimensjonsverdier som skal sperres. Hvis du vil gjøre dette, velger du feltet for å definere dimensjonskombinasjonen.  
4.  Velg nå en dimensjonsverdikombinasjon som er sperret, og angi **Sperret** i feltet. Hvis feltet er tomt, betyr dette at dimensjonsverdikombinasjonen er tillatt. Gjenta hvis flere kombinasjoner er sperret.  

> [!NOTE]  
>  De samme dimensjonene vises i både rader og kolonner og derfor vises alle dimensjonskombinasjoner to ganger. [!INCLUDE[d365fin](includes/d365fin_md.md)] viser automatisk innstillingene i begge felt. Du kan ikke velge noe i feltene fra øverst til høyre og nedover fordi disse feltene har de samme dimensjonene i både rader og kolonner.  
>   
>  Det alternativet du har valgt vises ikke før du går ut av feltet.  
>   
>  Hvis du vil vise navnet på dimensjonene i stedet for koden, velger du feltet **Vis kolonnenavn**.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Få en oversikt over dimensjoner som brukes flere ganger
Vinduet **Standarddimensjoner – flere** angir hvordan en kontogruppe bruker dimensjoner og dimensjonsverdier. Dette gjør du ved å utheve flere konti, og deretter angi standarddimensjoner og dimensjonsverdier for alle kontiene du har uthevet i kontooversikten. Når du angir standarddimensjoner for de uthevede kontiene, foreslår programmet disse dimensjonene og dimensjonsverdiene når én av disse kontiene er i bruk, for eksempel på en kladdelinje. Dette gjør det lettere for brukeren å bokføre poster, siden dimensjonsfeltene fylles ut automatisk. Dimensjonsverdiene som foreslås, kan imidlertid endres på for eksempel kladdelinjer.

Vinduet **Standarddimensjoner – flere** inneholder følgende felt:
|Felt|Description|
|----------------------------------|---------------------------------------|  
|**Dimensjonskode**|Viser alle dimensjonene som er opprettet som standarddimensjoner i én eller flere av de uthevede kontiene. Ved å velge feltet kan du se en oversikt over alle tilgjengelige dimensjoner. Hvis du velger en dimensjon, defineres den valgte dimensjonen som standarddimensjon for alle uthevede konti.|
|**Dimensjonsverdikode**|Viser enten en enkelt dimensjonsverdi eller betingelsen (Konflikt). Hvis en dimensjonsverdi vises i feltet, har alle uthevede konti samme standarddimensjonsverdi for en dimensjon. Hvis betingelsen (Konflikt) vises i feltet, har ikke alle de uthevede kontiene samme standarddimensjonsverdi for en dimensjon. Du kan se en oversikt over alle tilgjengelige dimensjonsverdier for en dimensjon ved å velge feltet. Hvis du velger en dimensjonsverdi, defineres den valgte dimensjonsverdien som en standarddimensjonsverdi for alle uthevede konti.|
|**Verdibokføring**|Viser enten en enkelt regel for verdibokføring eller betingelsen (Konflikt). Hvis en verdibokføringsregel vises i feltet, har alle konti som er merket samme verdibokføringsregel for en dimensjonsverdi. Hvis betingelsen (Konflikt) vises i feltet, har ikke alle de merkede kontiene samme verdibokføringsregel for en dimensjonsverdi. Du kan se en oversikt over verdibokføringsregler ved å velge feltet Verdibokføring. Hvis du velger en verdibokføringsregel, brukes den på alle uthevede kontoer.|

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

## <a name="to-view-global-dimensions-in-ledger-entry-windows"></a>Slik viser du globale dimensjoner i postvinduer  
Globale dimensjoner er alltid definerte og navngitt i henhold til selskap. Du viser de globale dimensjonene for selskapet ditt ved å åpne vinduet **Finansoppsett**.  

I et postvindu kan du se om det finnes globale dimensjoner for postene. De to globale dimensjonene skiller seg fra resten av dimensjonene ved at de kan brukes som filter over alt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Kontoplan** velger du handlingen **Poster**.  
3.  Hvis du bare vil vise relevante poster, angir du ett eller flere filtre i vinduet.  
4.  Hvis du vil vise alle dimensjonene for en post, velger du posten og klikker deretter på handlingen **Dimensjoner**.  

> [!NOTE]  
>  Vinduet **Postdimensjoner** viser alle dimensjonene for én post om gangen. Når du blar gjennom postene, endres innholdet i vinduet **Postdimensjoner** fortløpende.  

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

