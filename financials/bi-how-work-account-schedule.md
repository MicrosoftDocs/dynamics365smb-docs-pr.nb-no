---
title: Arbeide med kontoskjemaer | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker kontoskjemaer til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0284e419280be2d1faba4ac2bf40dac6f78823ed
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-account-schedules"></a>Arbeide med kontoskjemaer
Du kan bruke kontoskjemaer til å få innsikt i de økonomiske dataene som er lagret i kontoplanen. Kontoskjemaer analyserer tall på finanskonti og sammenligner faktiske finansposter med finansbudsjettposter. Resultatene vises i diagrammene på startsiden, for eksempel Kontantstrøm-diagrammet.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder et par eksempler på kontoskjemaer som du kan bruke med én gang, eller du kan definere dine egne rader og kolonner for å angi tallene som skal sammenlignes. Du kan for eksempel opprette kontoskjemaer for å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. Du kan opprette så mange egendefinerte regnskapsrapporter du vil.  

Oppretting av kontoskjemaer krever en forståelse av de økonomiske dataene i kontoplanen. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene. Dette krever at budsjetter opprettes. Hvis du vil ha mer informasjon, kan du se [Opprette budsjetter](finance-how-create-budgets.md).

> [!NOTE]  
>   Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).

## <a name="account-categories-and-account-schedules"></a>Kontokategorier og kontoskjemaer
Du kan bruke kontokategoriene til å endre oppsettet for regnskapsoppgjørene. Når du har definert kontokategoriene i vinduet **Finanskontokategorier** og du velger handlingen **Generer kontoskjemaer**, oppdateres de underliggende kontoskjemaene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel saldoutdrag, legges ny totaler og underoppføringer til, basert på endringene. Hvis du vil ha mer informasjon, kan du se [Finans og kontoplanen](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Slik oppretter du nye kontoskjemaer  
 Du bruker kontoskjemaer til å analysere tall på finanskonti eller til å sammenligne faktiske finansposter med finansbudsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.  
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

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
2. Velg et kontoskjema i vinduet **Kontoskjemanavn**.  
3. Velg handlingen **Rediger kontoskjema** for å definere en kontoskjemarad som skal brukes til å beregne summen prosentene skal baseres på.  
4. Sett inn en linje like over den første raden som du vil vise en prosentdel for.  
5. Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**. Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
6. Velg handlingen **Rediger oppsett for kolonneutforming** for å definere en kolonne.  
7. Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av %, i **Formel**-feltet. Hvis kolonnenummeret N for eksempel inneholder bevegelsen, angir du **N %**.  
8. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## <a name="to-set-up-account-schedules-with-overviews"></a>Slik setter du opp kontoskjemaer med oversikter  
Du kan bruke et kontoskjema til å opprette en oppgave som sammenligner finanstall og finansbudsjettall.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontoskjemaer**, og velg deretter den relaterte koblingen.
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

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

