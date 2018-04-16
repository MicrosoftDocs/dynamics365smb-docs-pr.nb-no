---
title: Analysere data etter dimensjoner | Microsoft-dokumentasjon
description: Beskriver hvordan du analyserer ulike forretningsdata etter dimensjoner.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ec3210e019da3369971d3aef6a4e38f4dcf1f530
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
#  <a name="analyze-data-by-dimensions"></a>Analysere data etter dimensjoner
I finansanalyse er en dimensjon data du kan legge til i en post som et slags merke. Disse dataene brukes til å gruppere poster med de samme egenskapene, for eksempel kunder, regioner, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Dimensjoner kan brukes på poster i kladder, dokumenter og budsjetter. Begrepet dimensjon beskriver hvordan analyser utføres. En todimensjonal analyse er for eksempel salg per område. Hvis du imidlertid bruker mer enn to dimensjoner når du oppretter en post, kan du utføre en mer omfattende analyse, for eksempel salg per salgskampanje per kundegruppe per område. Hvis du vil ha mer informasjon, kan du se [Arbeide med dimensjoner](finance-dimensions.md).

Analyse av data etter dimensjoner gir deg større innsikt i forretningsdriften, slik at du kan evaluere informasjon om hvor godt ting fungerer, hva som er bra og hva som er dårlig, og hvor det er behov for flere ressurser.

> [!TIP]
> Som en rask måte å analysere transaksjonsdata etter dimensjoner, kan du filtrere totalene i kontoplanen og postene i alle **Poster**-vinder per dimensjon. Se etter handlingen **Angi dimensjonsfilter**.

## <a name="to-set-up-an-analysis-view"></a>Slik setter du opp en analysevisning  
En analyse per dimensjoner viser et utvalg kombinasjoner av dimensjoner. Du kan lagre og hente fram hver analyse du har opprettet. Informasjonen som brukes til å definere en analyse, er lagret på et **Analysevisning**-kort for å forenkle fremtidige analyser.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Analysevisninger**, og velg deretter den relaterte koblingen.  
2. I vinduet **Analysevisningsoversikt** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du vil legge til flere dimensjonskoder i tillegg til de fire kodene i hurtigfanen **Dimensjoner**, velger du handlingen **Filtrer**, og deretter velger du **OK**.  
5. Du oppdaterer visningen ved å velge handlingen **Oppdater**.

## <a name="to-analyze-by-dimensions"></a>Analysere etter dimensjoner
Du kan bruke matrisen **Analyse per dimensjon** til å vise beløpene i Finans ved å bruke analysevisningene du allerede har definert. Du fyller ut vinduet **Analyse per dimensjon** for å definere hva som skal vises i matrisen, og deretter velger du handlingen **Vis matrise** for å vise matrisen.  

- Kolonnene ytterst til venstre inneholder informasjon som er basert på det du har valgt i feltet **Vis som linjer** i hodet.  
- Kolonnene lengst til høyre inneholder informasjon som er basert på det du har valgt i feltet **Vis som kolonner** i hodet.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Analyse per dimensjon**, og velg deretter den relaterte koblingen.  
2. Velg den relevante analysevisningen, og velg deretter handlingen **Rediger analysevisning**.
3. Øverst i vinduet **Analyse per dimensjon** fyller du ut feltene for å definere det som skal vises.
4. 5. Hvis du vil vise en spesifisering av et beløp som vises i matrisevinduet, velger du beløpet.  

> [!IMPORTANT]  
>   Du kan ikke velge en periodelengde som er kortere enn perioden som er spesifisert for datokomprimering på **Analysevisning**-kortet. Kommandoene **Neste sett** og **Forrige sett** er inaktive hvis du har valgt **Periode** i feltet **Vis som linjer** eller **Vis som kolonner**.  

> [!NOTE]  
>   Du kan bruke rapporten **Dimensjoner - detaljert** til å vise en detaljert klassifisering over hvordan dimensjoner er brukt i poster i løpet av en valgt periode. Du kan bruke rapporten **Dimensjoner - totalt** til å vise bare totalbeløp.  

> [!TIP]  
>   Du kan også endre visningen ved å endre innholdet i feltene **Vis som linjer** og **Vis som kolonner**. Hvis du vil tilbakeføre en visningsinnstilling, velger du handlingen **Reverser linjer og kolonner**.

## <a name="to-update-an-analysis-view"></a>Slik oppdaterer du en analysevisning  
Beløpene som vises i vinduet **Analyse per dimensjon**, gir deg oversikt over selskapets status ved siste oppdatering. Hvis du vil få et bilde av gjeldende tilstand, må du oppdatere analysevisningen ved å kjøre oppdateringsfunksjonen.

Følgende fremgangsmåte gjelder hvis du vil oppdatere en analysevisning fra vinduet **Analyse per dimensjoner**. Fremgangsmåten ligner den fra vinduene **Analysevisningskort** og **Analysevisningsoversikt**.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Analyse per dimensjon**, og velg deretter den relaterte koblingen.  
2. I vinduet **Analyse per dimensjon** velger du feltet **Analysevisningskode**.  
3. Velg linjen med den relevante analysevisningen.  
4. Velg handlingen **Oppdater**.  

> [!TIP]  
>   Hvis du merker av for **Oppdater ved bokføring** på et analysevisningskort, oppdateres visningen automatisk når en involvert transaksjon bokføres.

> [!NOTE]  
>   Hvis du vil oppdatere noen av eller alle analysevisningene samtidig, må du bruke kjørselen **Oppdater analysevisninger**.  

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

