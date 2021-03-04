---
title: Lage økonomirapporter med kontoskjemaer
description: Beskriver hvordan du bruker kontoskjemaer til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 58bc5001400a1a6ed03f5780a71b2f1ab96c43bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752158"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Klargjøre Financial Reporting med kontoskjemaer og kontokategorier

Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter. Resultatet vises i diagrammer i rollesenteret, for eksempel ut Kontantstrøm-diagrammet, og i rapporter, for eksempel rapporten Resultatregnskap og Balanse.

Du får tilgang til disse to rapportene for eksempel med handlingen **Årsregnskap** i rollesentrene for forretningsleder og regnskapsfører.  

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes. Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. Du kan opprette så mange egendefinerte regnskapsrapporter du vil.  

Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene. Dette krever at budsjetter opprettes. Hvis du vil ha mer informasjon, kan du se [Opprette finansbudsjetter](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Kontoskjemaer

Kontoskjemaer brukes til å organisere konti som er oppført i kontoplanen, på måter som egner seg for å presentere informasjon om disse kontiene. Du kan definere ulike oppsett for å velge hvilken informasjon du vil trekke ut fra kontoplanen. En av hovedfunksjonene med kontoskjemaer er å tilby et sted for beregninger som ikke kan gjøres direkte i kontoplanen, for eksempel oppretting av delsummer for kontogrupper, som kan inkluderes i nye summer og deretter brukes i andre totalsummer. Brukere kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. I tillegg kan finansposter og finansbudsjettposter filtreres, for eksempel etter bevegelse eller debetbeløp.

Du kan også sammenligne to eller flere kontoskjemaer og kolonneoppsett ved hjelp av formler. Denne typen sammenligning gir muligheter for følgende:

* Opprette tilpassede finansrapporter.
* Opprette så mange kontoskjemaer som nødvendig, med unike navn.
* Definere ulike rapportoppsett og skrive ut rapportene med gjeldende tall.

## <a name="gl-account-categories"></a>Finanskontokategorier

Du kan bruke finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene. Når du har definert kontokategoriene på siden **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel **saldoutdrag**, legges ny totaler og underoppføringer til, basert på endringene.

> [!NOTE]
> Kontokategoriene på øverste nivå, for eksempel **Gjeld**-noden, er faste, og du kan ikke legge til dine egne. Du kan imidlertid slette og legge til kontokategorier på lavere nivåer og endre strukturen for å definere hvordan det tilhørende kontoskjemaet skal vises i rapporter.
>
> Det anbefales at du oppretter og strukturerer dine egne finanskontokategorier på lavere nivå fra bunnen av, om nødvendig i et hierarki, i stedet for å prøve å omorganisere de eksisterende. Du kan for eksempel omstrukturere **Gjeld**-noden slik at den inneholder en ny **Egenkapital**-node etterfulgt av nodene **Kortsiktig gjeld** og **Langsiktig gjeld**.

## <a name="to-create-a-new-account-schedule"></a>Opprette et nytt kontoskjema

Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

Kontoskjemaene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] er grunnlaget for standard finansrapporter som kanskje ikke oppfylle kravene til virksomheten. Hvis du raskt vil opprette dine egne finansrapporter, kan du begynne med å kopiere et eksisterende kontoskjema. Se trinn 3 nedenfor.

Siden **Kto.skjemaoversikt** er der du kan forhåndsvise den økonomiske rapporten som kontoskjemaet definerer. I det følgende er det viktig å forstå at det du definerer som kontoskjemarader og -kolonner, bare kan ses og valideres på siden **Kto.skjemaoversikt**, som du åpner fra et kontoskjema ved å velge **Oversikt**-handlingen. Selve **Kontoskjema**-siden er bare et oppsettsområde.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** på siden **Kontoskjemaer** for å opprette et nytt kontoskjemanavn.
3. Du kan også velge handlingen **Kopier kontoskjema**, fylle ut de to feltene, og deretter velge **OK**.
4. Fyll ut feltene etter behov. I feltet **Standard kolonneoppsett** velger du et eksisterende oppsett. Det kan endres senere om du vil.

    Du bruker kolonneoppsett til å definere kolonner for ulike parametere som finansielle data i radene vises etter. Du kan for eksempel utforme et kolonneoppsett for å sammenligne bevegelse og saldo for samme periode i år og i fjor, med fire kolonner. Hvis du vil ha mer informasjon, kan du se [Redigere et kolonneoppsett](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Velg handlingen **Rediger kontoskjema**.
6. Opprett en rad for hvert økonomiske element som du vil skal vises i rapporten, for eksempel en rad for gjeldende aktiva og en ny rad for aktiva. For inspirasjon kan du se eksisterende kontoskjemaer i demoselskapet CRONUS.
7. Velg handlingen **Oversikt** for å se den resulterende økonomiske rapporten.
8. På siden **Kto.skjemaoversikt** i feltet **Navn på kolonneoppsett** velger du et annet kolonneoppsett for å vise økonomiske data etter andre parametere.
9. Velg **OK**.

Du har nå definert grunnlaget for kontoskjemaet, radene med økonomiske data som skal vises, og et eksisterende kolonneoppsett for å vise dataene i radene per ulike parametere. Hvis standardkolonneoppsettet du valgte i trinn 4, ikke dekker behovet ditt, følger du fremgangsmåten nedenfor.

### <a name="to-edit-a-column-layout"></a>Redigere et kolonneoppsett

Du bruker kolonneoppsett til å angi hvilke kolonner som skal være med i den resulterende rapporten. Du kan for eksempel sammenligne bevegelse og saldo for samme periode i år og i fjor.

> [!NOTE]
> En utskrifts-/forhåndsvisnings-/lagret versjon av et kontoskjema kan vise maksimalt fem kolonner. Hvis kontoskjemaet bare er beregnet for analyse på siden **Kto.skjemaoversikt**, kan du opprette så mange kolonner du vil.

1. På **Kontoskjemaer**-siden velger du det aktuelle kontoskjemaet, og velger deretter **Rediger oppsett for kolonneutforming**-handlingen.
2. På siden **Kolonneoppsett** oppretter du en rad for hver kolonne som økonomiske data skal vises etter i den økonomiske rapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg **OK**.
4. Åpne siden **Kto.skjemaoversikt** med jevne mellomrom for å kontrollere at det nye kolonneoppsettet fungerer som forventet.

> [!NOTE]
> Kolonnene som du definerer på hver rad, representerer kolonner 3 og oppover på **Kto.skjemaoversikt**-siden. De to første kolonnene, **Radnr.** og **Beskrivelse**, er faste.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Slik oppretter du en kolonne som beregner prosentdeler

Noen ganger vil du kanskje ta med en kolonne i et kontoskjema for å beregne prosentdeler av en sum. Hvis du for eksempel har et antall rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg hver rad representerer.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
2. Velg et kontoskjema på siden **Kontoskjemanavn**.  
3. Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.  
4. Sett inn en linje like over den første raden som du vil vise en prosentdel for.  
5. Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**. Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
6. Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.  
7. Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet. Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.  
8. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## <a name="to-set-up-account-schedules-with-overviews"></a>Slik setter du opp kontoskjemaer med oversikter

Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
2. Velg et kontoskjema på siden **Kontoskjemanavn**.  
3. Velg handlingen **Rediger kontoskjema**.  
4. Velg standard kontoskjemanavn i **Navn**-feltet på **Kontoskjema**-siden.
5. Velg handlingen **Sett inn konti**.  
6. Velg kontiene du vil ta med i oppgaven , og klikk deretter **OK**-knappen.

    Kontiene settes nå inn i kontoskjemaet. Hvis du vil, kan du også endre kolonneoppsettet.  
7. Velg handlingen **Oversikt**.  
8. På hurtigfanen **Dimensjonsfiltre** på **Kto.skjemaoversikt**-siden setter du budsjettfilteret til ønsket filternavn.  
9. Velg **OK**.  

Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskapsperioder ved hjelp av periodeformler

Kontoskjemaet kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor. Dette gjør du ved å åpne **Kolonneoppsett**-siden og tilpasse den ved å legge til feltet **Formel - periodesammenligning** som en kolonne. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md). Deretter kan du sette dette feltet til en periodeformel.  

En regnskapsperiode trenger ikke å sammenfalle med kalenderen, men regnskapsåret må ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruker periodeformelen til å beregne beløpet fra sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapportforespørselen. Sammenligningsperioden er basert på perioden for startdatoen i datofilteret. Periodene forkortes slik:

| Forkortelse | Beskrivelse                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode                                                                                |
| SP           | Siste periode av et regnskapsår, et halvår eller kvartal.                                   |
| IP           | Inneværende periode av et regnskapsår, et halvår eller kvartal. Bruk IP i formlar for å oppgi perioden som skal starte eller avslutte formelen. For eksempel angir RÅ\[1.. IP\] tiden fra begynnelsen av gjeldende regnskapsår til gjeldende periode.|
| RÅ           | Regnskapsår. Eksempelvis viser RÅ\[1..3\] første kvartal av inneværende regnskapsår |

Eksempler på formler:

| Formel         | Beskrivelse                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Inneværende periode                                                                                  |
| \-1P            | Forrige periode                                                                                 |
| \-1RÅ\[1..SP\]  | Hele forrige regnskapsår                                                                     |
| \-1RÅ           | Inneværende periode i forrige regnskapsår                                                          |
| \-1RÅ\[1..3\]   | Første kvartal av forrige regnskapsår                                                           |
| \-1RÅ\[1..IP\]  | Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår, inkludert begge perioder |
| \-1RÅ\[IP..SP\] | Fra inneværende periode i forrige regnskapsår til siste periode i forrige regnskapsår, inkludert begge perioder   |

Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet. Hvis feltet eksempelvis er satt til -1Å, foretar [!INCLUDE [prod_short](includes/prod_short.md)] en sammenligning med samme periode 1 år tidligere.

> [!NOTE]
> Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i dataene i kontoplanen. Du oppretter for eksempel et kontoskjema der du vil sammenligne denne perioden med samme periode i fjor, så du setter **Datoformel - sammenligning**-feltet til *-1RÅ*. Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar. Dermed sammenligner kontoskjemaet januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.  

Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]