---
title: "Lage økonomirapporter med kontoskjemaer"
description: "Beskriver hvordan du bruker kontoskjemaer til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: nb-no
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a>Arbeide med kontoskjemaer
Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter. Resultatene vises i diagrammene i rollesenteret, for eksempel Kontantstrøm-diagrammet.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes. Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. Du kan opprette så mange egendefinerte regnskapsrapporter du vil.  

Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene. Dette krever at budsjetter opprettes. Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Kontokategorier og kontoskjemaer
Du kan bruke kontokategoriene til å endre oppsettet for regnskapsoppgjørene. Når du har definert kontokategoriene i vinduet **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel saldoutdrag, legges ny totaler og underoppføringer til, basert på endringene. Hvis du vil ha mer informasjon, kan du se [Finans og kontoplanen](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Slik oppretter du nye kontoskjemaer  
 Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** i vinduet **Kontoskjemanavn** for å opprette et nytt kontoskjemanavn.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg handlingen **Rediger kontoskjema**.
5. Fyll ut feltene etter behov i vinduet **Kontoskjema**.  

    Når du har opprettet et nytt kontoskjema og definert radene, må du definere kolonner. Dette kan du gjøre manuelt eller ved hjelp av et forhåndsdefinert kolonneoppsett.
6. Velg handlingen **Rediger oppsett for kolonneutforming**.
7. I vinduet **Kolonneoppsett** fyller du ut feltene etter behov.

> [!NOTE]  
>   Hvis du ikke tilordnet et standard kolonneoppsett til kontoskjemaet, må du definere kolonnene manuelt.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Slik oppretter du en kolonne som beregner prosentdeler  
Noen ganger vil du kanskje ta med en kolonne i et kontoskjema for å beregne prosentdeler av en sum. Hvis du for eksempel har et antall rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg hver rad representerer.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
2. Velg et kontoskjema i vinduet **Kontoskjemanavn**.  
3. Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.  
4. Sett inn en linje like over den første raden som du vil vise en prosentdel for.  
5. Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**. Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
6. Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.  
7. Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet. Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.  
8. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## <a name="to-set-up-account-schedules-with-overviews"></a>Slik setter du opp kontoskjemaer med oversikter  
Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
2. Velg et kontoskjema i vinduet **Kontoskjemanavn**.  
3. Velg handlingen **Rediger kontoskjema**.  
4. Velg standawrd kontoskjemanavn i **Navn**-feltet i **Kontoskjema**-vinduet.
5. Velg handlingen **Sett inn konti**.  
6. Velg kontiene du vil ta med i oppgaven , og klikk deretter **OK**-knappen.

    Kontiene settes nå inn i kontoskjemaet. Hvis du vil, kan du også endre kolonneoppsettet.  
7. Velg handlingen **Oversikt**.  
8. På hurtigfanen **Dimensjonsfiltre** setter du budsjettfilteret til ønsket filternavn.  
9. Velg **OK**.  

Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskapsperioder ved hjelp av periodeformler
Kontoskjemaet kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor. For å gjøre dette må du legge til en kolonne med **Formel - periodesammenligning**-feltet, og deretter angi dette feltet som en periodeformel.  

En regnskapsperiode trenger ikke å sammenfalle med kalenderen, men regnskapsåret må ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] bruker periodeformelen til å beregne beløpet fra sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapportforespørselen. Sammenligningsperioden er basert på perioden for startdatoen i datofilteret. Periodene forkortes slik:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forkortelse</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periode</p></td>
</tr>
<tr class="even">
<td><p>SP</p></td>
<td><p>Siste periode av et regnskapsår, et halvår eller kvartal.</p></td>
</tr>
<tr class="odd">
<td><p>IP</p></td>
<td><p>Inneværende periode av et regnskapsår, et halvår eller kvartal.</p></td>
</tr>
<tr class="even">
<td><p>RÅ</p></td>
<td><p>Regnskapsår. Eksempelvis viser RÅ [1..3] til første kvartal av inneværende regnskapsår</p></td>
</tr>
</tbody>
</table>

Eksempler på formler:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Formel</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Tom&gt;</p></td>
<td><p>Inneværende periode</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Forrige periode</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..SP]</p></td>
<td><p>Hele forrige regnskapsår</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ</p></td>
<td><p>Inneværende periode i forrige regnskapsår</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[1..3]</p></td>
<td><p>Første kvartal av forrige regnskapsår</p></td>
</tr>
<tr class="even">
<td><p>-1RÅ[1..IP]</p></td>
<td><p>Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår</p></td>
</tr>
<tr class="odd">
<td><p>-1RÅ[IP..SP]</p></td>
<td><p>Fra inneværende periode i forrige regnskapsår til og med siste periode i forrige regnskapsår</p></td>
</tr>
</tbody>
</table>

Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet.

> [!NOTE]
> Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i dataene i kontoplanen. Du oppretter for eksempel et kontoskjema der du vil sammenligne denne perioden med samme periode i fjor, så du setter **Sammenligningsperiode - filter**-feltet til *-1RÅ*. Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar. Dermed sammenligner kontoskjemaet januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.  


## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

