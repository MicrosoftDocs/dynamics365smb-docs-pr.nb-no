---
title: Opprette analyserapporter
description: 'Beskriver hvordan du oppretter nye analyserapporter for salg, kjøp og beholdning, og definerer analysemaler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# Opprette analyserapporter

Salgssjefer må analysere omsetning, bruttofortjeneste og andre viktige salgsytelsesindikatorer regelmessig. Innkjøpere er mer interessert i dynamikken rundt innkjøpsvolum, leverandørenes ytelse og kjøpspriser. Logistikk-/lagersjefer trenger derimot opplysninger om vareomsetning, analyse av lagerflytting og statistikk for lagerverdi. Derfor finnes det ingen analyserapport som passer for alt.

Du kan tilpasse analyserapportene basert på poster med de bokførte transaksjonene, for eksempel salg, kjøp, overføring og lagerjusteringer. I en tilpassbar rapport kan kildedataene, som utledes fra varepostene (med tilknyttede verdiposter), kombineres, sammenlignes og presenteres på relevante, brukerdefinerte måter. På denne måten er analyserapporten svært lik en pivottabellrapport i Microsoft Excel.  

Du kan for eksempel opprette en personlig rapport som fokuserer på nøkkelkontiene når det gjelder total produktomsetning i beløp og solgte verdier, bruttofortjeneste og bruttofortjenesteprosent i løpet av denne måneden. Deretter kan du få den til å sammenligne disse tallene med resultatene fra tidligere måneder eller den samme måneden i fjor, og beregne avvik. Alt dette kan gjøres i én og samme visning, med muligheten til å navigere til årsaken til identifiserte problemområder og til og med velge rullegardin for å vise detaljer helt ned til nivået for enkelttransaksjoner.  

Analyserapporten består av objektene du vil analysere (for eksempel kunder, kundegrupper, selgere og så videre, representert som linjer) og analyseparameterne, det vil si hvordan du vil analysere objektet (som beregning av fortjeneste, periodevise sammenligninger av salgsbeløp og -volum, eller periodevise sammenligninger av faktiske og budsjetterte tall, representert som kolonner). 

I tillegg til analyserapporter kan du opprette og vise lignende informasjon i analysevisninger (basert på dimensjonene). Lær mer på [Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md).

## Eksempel

Du kan opprette disse linjene (objektene du vil analysere):  

- Datamaskiner  
- Skjermer  
- Reservedeler  

Deretter kan du opprette disse kolonnene (hvordan du vil analysere objektene):  

- Salg inneværende måned  
- Salg forrige måned  
- Salg i prosent forrige måned  

## Definere linje- og kolonneoppsett

På **Analyserapport**-siden kan du vise forskjellige linje- og kolonneoppsett som du definerer på:

* Siden **Maler for analyselinje**, der du definerer navnet på rapporten og objektene du vil vise på linjene i rapporten, og
* **Maler for analysekolonne**-siden, der du definerer navnet på kolonnemalen og analyseparameterne som vises som kolonner i rapporten. Hver linje på siden representerer en kolonne i rapporten. 

Merk at analyselinjer og analysekolonner er uavhengige av hverandre.  

Basert på linjene og kolonnene du har definert, vil [!INCLUDE[prod_short](includes/prod_short.md)] samle resultatene av rapporten på siden **Analyserapport**, som vist i tabellen nedenfor.  

|- |Salg inneværende måned|Salg forrige måned|Salg i prosent forrige måned|  
|-|-|-|-|  
|Datamaskiner| | | |  
|Skjermer| | | |  
|Reservedeler| | | |  
|Sum| | | |  

Du kan for eksempel definere en gruppe med linje- og flere grupper med kolonneoppsett for å vise henholdsvis månedlige og årlige rapporter.

## Definere en analysekolonnemaler

Følgende fremgangsmåte er basert på salgsanalysevisninger. Fremgangsmåten er lignende for kjøps- og lageranalysevisninger.

En analysekolonnemal som består av et sett med linjer, som representerer en analysekolonne du vil ha i analyserapporten. For å kunne definere en kolonne må du tilordne en analysetypekode til en linje. Denne analysetypekoden bestemmer typen kildedata i varepostene som analysen baseres på. Kildedata kan inkludere kostnader, salgsbeløp eller antall, og deres tilknyttede verdiposter. Du kan definere så mange kolonnemaler du vil og deretter bruke dem til å opprette nye analyserapporter.    

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskolonnemaler**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Kolonner**.  
4. Fyll ut feltene for å angi hvilke kolonner du vil inkludere i analyserapporten på siden **Analysekolonner**.  

    > [!NOTE]  
    > For å kunne definere en kolonne må du fylle ut feltet **Analysetypekode** for alle kolonnetyper med unntak av **Formel**. Definer analysetypekoder på **Analysetyper**-siden.  
    
    I **Posttype**-feltet kopieres også de faktiske tallene fra vareposten hvis du velger **Vareposter**. Hvis du velger **Varebudsjettposter**, kopieres budsjetterte tall fra budsjettet.  
5. Velg **OK** for å lagre endringene.  

## Definere analyselinjemaler

Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

En analyselinjemal som består av et sett med linjer, som representerer en analyselinje du vil ha i analyserapporten. En linje kan angi én eller flere varer, kunder, leverandører eller grupper. Du kan også opprette en formel på en linje for å summere de andre linjene. Du kan definere så mange linjemaler du vil og deretter bruke dem til å opprette nye analyserapporter.   

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgslinjemaler**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Linjer**.  
4. Opprett linjer for varene, kundene, leverandørene eller selgerne du vil vise tall for i analyserapporten, på **Analyselinje**-siden. Du må fylle ut feltene **Type**, **Fra/til** og **Beskrivelse**.  

> [!NOTE]  
> Hvis du vil opprette mange individuelle linjer for hver vare, kunde og så videre, kan du velge riktig innsettingsalternativ for å fylle ut alle de relevante feltene på linjen. Hvis du må, kan du deretter redigere linjene manuelt. Når du skal sette inn linjer, velger du handlingen **Sett inn elementer** eller **Sett inn varegrupper**.  

## Opprette en ny salgsanalyserapport

Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

Med analyserapporter kan du analysere dynamikken for salg i forhold til viktige indikatorer for salgsprestasjon du velger, for eksempel salgsomsetning i både beløp og antall, bidragsmargin eller fremdrift for faktisk salg mot budsjettet. Du kan også bruke analyserapporter til å analysere gjennomsnittlig salgspris og evaluere salgsprestasjonen for salgskorpset.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsanalyserapporter**, og velg deretter den relaterte koblingen.  
2. På siden **Analyserapport - salg** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg handlingen **Rediger analyserapport**.
5. På siden **Salgsanalyserapport** velger du handlingen **Vis matrise**.  

> [!NOTE]  
> Det er valgfritt å bygge kombinasjoner av linje- og kolonnemaler for å opprette rapporter og tilordne dem unike navn. Hvis du gjør dette trenger du ikke å velge linje- og kolonnemaler på siden **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du endre linje- og kolonnemaler uavhengig av hverandre og deretter velge rapportnavnet på nytt for å gjenopprette den opprinnelige kombinasjonen.

## Se også

[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
