---
title: Analysere data etter dimensjoner
description: Denne artikkelen beskriver hvordan du kan analysere forretningsdata etter dimensjoner for å få bedre innsikt i virksomheten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# <a name="analyze-data-by-dimensions"></a>Analysere data etter dimensjoner

I finansanalyse er en dimensjon data du kan legge til i en post som et slags merke. Disse dataene brukes til å gruppere poster med de samme egenskapene, for eksempel kunder, regioner, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Dimensjoner kan brukes på poster i kladder, dokumenter og budsjetter. 

Hver dimensjon beskriver fokuset for analyse. Så en todimensjonal analyse er for eksempel salg per område. Hvis du bruker mer enn to dimensjoner når du oppretter en post, kan du utføre en mer omfattende analyse, for eksempel salg per salgskampanje per kundegruppe per område. Det gir deg større innsikt i forretningsdriften, for eksempel hvordan bra forretningen fungerer, hva som er bra og hva som er dårlig, og hvor det er behov for flere ressurser, slik at du kan gjøre mer informerte beslutninger fremover. Finn ut mer under [Arbeide med dimensjoner](finance-dimensions.md).

> [!TIP]
> Som en rask måte å analysere transaksjonsdata etter dimensjoner, kan du filtrere totalene i kontoplanen og postene i alle **Poster**-sider per dimensjon. Se etter handlingen **Angi dimensjonsfilter**.

> [!NOTE]
> Hvis du oppdager at en feil dimensjonsverdi er blitt brukt i bokførte finansposter, kan du korrigere den og oppdatere analysevisningene. Lær mer i delen [Feilsøke og korrigere dimensjoner](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view"></a>Sette opp en analysevisning

En analyse per dimensjoner bruker et utvalg kombinasjoner av dimensjoner. Du lagrer, henter og oppdaterer dimensjonssettet ved å opprette et **Analysevisning**-kort. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Analysevisninger**, og velg deretter den relaterte koblingen.  
2. På siden **Analysevisningsoversikt** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du vil legge til flere dimensjonskoder i tillegg til de fire kodene i hurtigfanen **Dimensjoner**, velger du handlingen **Filtrer**, og deretter velger du **OK**.  
5. Du oppdaterer visningen ved å velge handlingen **Oppdater**.

## <a name="analyze-by-dimensions"></a>Analysere etter dimensjoner

Bruk analysevisningene du allerede har definert med matrisen **Analyse per dimensjon**, til å vise beløpene i Finans.   

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Analysevisninger**, og velg deretter den relaterte koblingen.  
2. Velg den relevante analysevisningen, og velg deretter handlingen **Analyse per dimensjon**.
3. På siden **Analyse per dimensjon** fyller du ut feltene for å definere dataene som skal vises, og hvordan.
4. Velg handlingen **Vis matrise** for å åpne den respektive matrisesiden for den definerte analysevisningen.
5. Hvis du vil vise en spesifisering av et beløp som vises på matrisesiden, velger du beløpet for detaljer.  

- Kolonnene ytterst til venstre inneholder informasjon som er basert på det du har valgt i feltet **Vis som linjer** i hodet.  
- Kolonnene lengst til høyre inneholder informasjon som er basert på det du har valgt i feltet **Vis som kolonner** i hodet.

> [!IMPORTANT]  
> Du kan ikke velge en periodelengde som er kortere enn perioden som er spesifisert for datokomprimering på **Analysevisning**-kortet. Kommandoene **Neste sett** og **Forrige sett** er inaktive hvis du har valgt **Periode** i feltet **Vis som linjer** eller feltet **Vis som kolonner**.  

> [!NOTE]  
> Du kan bruke rapporten **Dimensjoner - detaljert** til å vise en detaljert klassifisering over hvordan dimensjoner er brukt i poster i løpet av en valgt periode. Du kan bruke rapporten **Dimensjoner - totalt** til å vise bare totalbeløp.  

> [!TIP]  
> Du kan også endre visning ved å endre innholdet i feltene **Vis som linjer** og **Vis som kolonner**. Hvis du vil tilbakeføre en visningsinnstilling, velger du handlingen **Reverser linjer og kolonner**.

## <a name="update-an-analysis-view"></a>Oppdatere en analysevisning

Beløpene som vises på siden **Analyse per dimensjon**, gir deg oversikt over selskapets status ved siste oppdatering. Hvis du vil få et bilde av gjeldende tilstand, må du oppdatere analysevisningen ved å kjøre oppdateringsfunksjonen.

Bruk følgende fremgangsmåte til å oppdatere en analysevisning fra siden **Analyse per dimensjoner**. Fremgangsmåten ligner på de for oppdatering av sidene **Analysevisningskort** og **Analysevisningsoversikt**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Analysevisninger**, og velg deretter den relaterte koblingen.
2. Velg den relevante analysevisningen, og velg deretter handlingen **Analyse per dimensjon**.
3. På siden **Analyse per dimensjon** velger du feltet **Analysevisningskode**.  
4. Velg linjen med den relevante analysevisningen.  
5. Velg analysevisningen på **Analysevisninger**-siden, og velg deretter handlingen **Oppdater**.  

> [!TIP]  
> Hvis du merker av for **Oppdater ved bokføring** på et analysevisningskort, oppdateres visningen automatisk når en tilknyttet transaksjon bokføres.

> [!NOTE]  
> Hvis du vil oppdatere noen av eller alle analysevisningene samtidig, må du bruke kjørselen **Oppdater analysevisninger**.  

## <a name="see-also"></a>Se også

[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
