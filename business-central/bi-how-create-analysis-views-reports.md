---
title: Opprette analyserapporter | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter nye analyserapporter for salg, kjøp og beholdning, og definerer analysemaler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 11b90a7aa48927d68d4e32845343dddc56ba77c1
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786640"
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
 På siden **Analyserapport** kan du vise ulike linje- og kolonneoppsett i henhold til linjene eller linjemalene du definerer på siden **Maler for analyselinje**. Du kan definere navnet på rapporten og objektene du vil vise på linjene i rapporten. Du definerer kolonnene dine på siden **Maler for analysekolonne**. Du kan definere navnet på kolonnemalen og analyseparameterne du vil vise som kolonner i rapporten. Hver linje representerer en kolonne i rapporten på siden **Maler for analysekolonne**. Merk at analyselinjer og analysekolonner er uavhengige av hverandre.  

Basert på linjene og kolonnene du har definert, vil [!INCLUDE[prod_short](includes/prod_short.md)] samle resultatene av rapporten på siden **Analyserapport**, som vist i tabellen nedenfor.  

|- |Salg inneværende måned|Salg forrige måned|Salg i prosent forrige måned|  
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

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Maler for salgskolonne**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Kolonner**.  
4. Fyll ut feltene for å angi hvilke kolonner du vil inkludere i analyserapporten på siden **Analysekolonner**.  

    > [!NOTE]  
    >   For å kunne definere en kolonne må du fylle ut feltet **Analysetypekode** for alle kolonnetyper med unntak av **Formel**. Definer analysetypekoder på **Analysetyper**-siden.  
    I **Posttype**-feltet kopieres også de faktiske tallene fra vareposten hvis du velger **Vareposter**. Hvis du velger **Varebudsjettposter**, kopieres budsjetterte tall fra budsjettet.  
5.  Velg **OK** for å lagre endringene.  

## <a name="to-set-up-analysis-line-templates"></a>Slik definerer du analyselinjemaler  
Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

I en analyserapport vises analyseobjektene på linjene. Du kan definere linjene du vil inkludere i analyserapporten, ved å definere maler for analyselinjen.  

En mal består av et sett med linjer som representerer analyselinjene du ser i analyserapporten. En linje kan angi én eller flere varer, kunder, leverandører eller grupper. Du kan også opprette en formel på en linje for å summere de andre linjene. Du kan definere så mange linjemaler du vil og deretter bruke dem til å opprette nye analyserapporter.    

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Maler for salgslinje**, og velg deretter den relaterte koblingen.  
2. Velg den første tomme linjen, og fyll deretter ut feltene etter behov.
3. Velg handlingen **Linjer**.  
4. Opprett linjer for varene, kundene, leverandørene eller selgerne du vil vise tall for i analyserapporten, på **Analyselinje**-siden. Du må fylle ut feltene **Type**, **Fra/til** og **Beskrivelse**.  

> [!NOTE]  
>   Hvis du vil opprette mange individuelle linjer for hver vare, kunde og så videre, kan du velge riktig innsettingsalternativ for å fylle ut alle de relevante feltene på linjen. Hvis du må, kan du deretter redigere linjene manuelt. Når du skal sette inn linjer, velger du handlingen **Sett inn elementer** eller **Sett inn varegrupper**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Slik oppretter du en ny salgsanalyserapport
Følgende fremgangsmåte er basert på analyserapporter for salg. Fremgangsmåten er lignende for kjøps- og lageranalyserapporter.

Du kan bruke analyserapporter til å analysere dynamikken for salg i forhold til viktige indikatorer for salgsprestasjon du velger, for eksempel salgsomsetning i både beløp og antall, bidragsmargin eller fremdrift for faktisk salg mot budsjettet. Du kan også bruke rapporten til å analysere gjennomsnittlig salgspris og evaluere salgsprestasjonen for salgskorpset.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsanalyserapporter**, og velg deretter den relaterte koblingen.  
2. På siden **Analyserapport - salg** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg handlingen **Rediger analyserapport**.
5. På siden **Salgsanalyserapport** velger du handlingen **Vis matrise**.  

> [!NOTE]  
>   Det er valgfritt å bygge kombinasjoner av linje- og kolonnemaler for å opprette rapporter og tilordne dem unike navn. Hvis du gjør dette, vil valg av et rapportnavn bety at du ikke trenger å velge linje- og kolonnemaler på siden **Salgsanalyserapport**. Når du har valgt et rapportnavn, kan du endre linje- og kolonnemaler uavhengig av hverandre og deretter velge rapportnavnet på nytt for å gjenopprette den opprinnelige kombinasjonen.

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]