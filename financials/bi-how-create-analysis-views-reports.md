---
title: Opprette analyserapporter | Microsoft-dokumentasjon
description: "Beskriver hvordan du oppretter nye analyserapporter for salg, kjøp og beholdning, og definerer analysemaler."
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
ms.openlocfilehash: 378c3d2b0429390c303c723dbfafd07c531b3958
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
#  <a name="create-analysis-reports"></a>Opprette analyserapporter
Salgssjefer må analysere omsetning, bruttofortjeneste og andre viktige salgsytelsesindikatorer regelmessig. Innkjøpere er mer interessert i dynamikken rundt innkjøpsvolum, leverandørenes ytelse og kjøpspriser. Logistikk-/lagersjefer trenger derimot opplysninger om vareomsetning, analyse av lagerflytting og statistikk for lagerverdi.  

Du kan bruke analyserapportene til å opprette tilpassede rapporter basert på poster med de bokførte transaksjonene, for eksempel salg, kjøp, overføring og lagerjusteringer. I en tilpassbar rapport kan kildedataene, som utledes fra varepostene (med tilknyttede verdiposter), kombineres, sammenlignes og presenteres på relevante, brukerdefinerte måter. På denne måten er analyserapporten svært lik en pivottabellrapport i Microsoft Excel.  

Du kan opprette en personlig rapport som fokuserer på de viktigste kundene, når det gjelder total omsetning både i beløp og salgsvolum, bruttofortjeneste og bruttofortjeneste i prosent i inneværende måned, og du kan sammenligne disse tallene med resultatene fra forrige måned eller samme måned i fjor og beregne avvik. Alt dette kan gjøres i én og samme visning, med muligheten til å navigere til årsaken til identifiserte problemområder ved å velge rullegardinknappen for å vise detaljer på nivået for enkelttransaksjoner.  

Analyserapporten består av objektene du vil analysere, for eksempel kunder, kundegrupper, selgere og så videre, representert som linjer, og analyseparameterne, det vil si hvordan du vil analysere objektet, representert som kolonner, for eksempel beregning av fortjeneste, periodevise sammenligninger av salgsbeløp og -volum, eller periodevise sammenligninger av faktiske og budsjetterte tall.

I tillegg til analyserapporter kan du opprette og vise lignende informasjon i analysevisninger, som er basert på dimensjonene. Hvis du vil ha mer informasjon, kan du se [Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Eksempel  
Du kan definere linjer som disse:  
- Datamaskiner  
- Skjermer  
- Reservedeler  

Deretter kan du definere kolonner som disse:  

- Salg inneværende måned  
- Salg forrige måned  
- Salg i prosent forrige måned  

## <a name="setting-up-line-and-column-layouts"></a>Definere linje- og kolonneoppsett  
 I **Analyserapport**-vinduet kan du vise forskjellige linje- og kolonneoppsett i henhold til hva du har definert. Du definerer linjer eller linjemaler i vinduet **Maler for analyselinje**. I dette vinduet kan du definere navnet på rapporten og objektene du vil vise på linjene i rapporten. Du definerer kolonnene dine i tabellen **Maler for analysekolonne**. I dette vinduet kan du definere navnet på kolonnemalen og analyseparameterne du vil vise som kolonner i rapporten. Hver linje representerer en kolonne i rapporten i vinduet **Maler for analysekolonne**. Merk at analyselinjer og analysekolonner er uavhengige av hverandre.  

Basert på linjene og kolonnene du har definert, vil programmet samle resultatene av rapporten i matrisevinduet **Analyserapport**, for eksempel slik som i dette eksemplet:  

| |Salg inneværende måned|Salg forrige måned|Salg i prosent forrige måned|  
|-|-|-|-|  
|Datamaskiner| | | |  
|Skjermer| | | |  
|Reservedeler| | | |  
|I alt| | | |  

 Du kan for eksempel definere ett sett med linje- og flere sett med kolonneoppsett for å vise henholdsvis månedlige og årlige rapporter.

 ## <a name="to-set-up-analysis-column-templates"></a>Slik definerer du en analysekolonnemaler
Følgende fremgangsmåte er basert på analysevisninger for salg. Fremgangsmåten er lignende for kjøps- og lageranalysevisninger.

I en analyserapport vises analyseparameterne som kolonner. Du kan definere kolonnene du vil inkludere i analyserapporten, ved å definere maler for analysekolonne.  

En mal består av et sett med linjer som representerer analysekolonnene du ser i analyserapporten. For å kunne definere en kolonne må du tilordne en analysetypekode til en linje. Denne analysetypekoden bestemmer typen kildedata i varepostene som analysen baseres på. Kildedataene inkluderer kostnader, salgsbeløp eller antall, og deres tilknyttede verdiposter. Du kan definere så mange kolonnemaler du vil og deretter bruke dem til å opprette nye analyserapporter.    

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Maler for salgskolonne**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Kolonner**.  
4. Fyll ut feltene for å angi hvilke kolonner du vil inkludere i analyserapporten i vinduet **Analysekolonner**..  

    > [!NOTE]  
>   For å kunne definere en kolonne må du fylle ut feltet **Analysetypekode** for alle kolonnetyper med unntak av **Formel**. Definer analysetypekoder i **Analysetyper**-vinduet.  

    **Merk**. I **Posttype**-feltet kopieres de faktiske tallene fra vareposten hvis du velger **Vareposter**. Hvis du velger **Varebudsjettposter**, kopieres budsjetterte tall fra budsjettet.  
5.  Velg **OK** for å lagre endringene.  

## <a name="to-set-up-analysis-line-templates"></a>Slik definerer du analyselinjemaler  
Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

I en analyserapport vises analyseobjektene på linjene. Du kan definere linjene du vil inkludere i analyserapporten, ved å definere maler for analyselinjen.  

En mal består av et sett med linjer som representerer analyselinjene du ser i analyserapporten. En linje kan angi én eller flere varer, kunder, leverandører eller grupper. Du kan også opprette en formel på en linje for å summere de andre linjene. Du kan definere så mange linjemaler du vil og deretter bruke dem til å opprette nye analyserapporter.    

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Maler for salgslinje**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Linjer**.  
4. Opprett linjer for varene, kundene, leverandørene eller selgerne du vil vise tall for i analyserapporten, i **Analyselinje**-vinduet. Du må fylle ut feltene **Type**, **Fra/til** og **Beskrivelse**.  

> [!NOTE]  
>   Hvis du vil opprette mange individuelle linjer for hver vare, kunde og så videre, kan du velge riktig innsettingsalternativ for å fylle ut alle de relevante feltene på linjen. Hvis du må, kan du deretter redigere linjene manuelt. Når du skal sette inn linjer, velger du handlingen **Sett inn elementer** eller **Sett inn varegrupper**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Slik oppretter du en ny salgsanalyserapport
Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

Du kan bruke analyserapporter til å analysere dynamikken for salg i forhold til viktige indikatorer for salgsprestasjon du velger, for eksempel salgsomsetning i både beløp og antall, bidragsmargin eller fremdrift for faktisk salg mot budsjettet. Du kan også bruke rapporten til å analysere gjennomsnittlig salgspris og evaluere salgsprestasjonen for salgskorpset.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsanalyserapporter**, og velg deretter den relaterte koblingen.  
2. I vinduet **Analyserapport - salg** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg handlingen **Rediger analyserapport**.
5. I vinduet **Salgsanalyserapport** velger du handlingen **Vis matrise**.  

> [!NOTE]  
>   Det er valgfritt å bygge kombinasjoner av linje- og kolonnemaler for å opprette rapporter og tilordne dem unike navn. Hvis du gjør dette, vil valg av et rapportnavn bety at du ikke trenger å velge linje- og kolonnemaler i vinduet **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du endre linje- og kolonnemaler uavhengig av hverandre og deretter velge rapportnavnet på nytt for å gjenopprette den opprinnelige kombinasjonen.

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

