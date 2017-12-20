---
title: Konfigurere og rapportere Intrastat | Microsoft-dokumentasjon
description: "Lær hvordan du konfigurerer Intrastat rapporteringsfunksjoner, og hvordan til å rapportere handel med selskaper i andre EU-land."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: de6cbcdc8e7ca4aff06461192e2038831ba6b5b3
ms.openlocfilehash: 973c42642f88024de9d8924b675496015ce60983
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2017

---
# <a name="how-to-set-up-and-report-intrastat"></a>Konfigurere og rapportere Intrastat
Alle selskaper i EU må rapportere handel med andre EU-land/-regioner. Varebevegelsen må hver måned rapporteres til statistikkmyndighetene i landet/regionen du bor i, og rapporten må leveres til skattemyndighetene. Dette kalles Intrastat-rapportering. Du bruker siden **Intrastatkladd** til å fylle ut jevnlige Intrastat-rapporter.  

## <a name="required-and-optional-setups"></a>Nødvendige og valgfrie oppsett
Før du kan bruke Intrastat-kladden til å rapportere Intrastat-informasjon, må du konfigurere flere ting:  

* **Intrastat-kladdemaler**: Du må konfigurere Intrastat-kladdemalene og kjørslene du vil bruke. Siden Intrastat blir rapportert månedlig, må du opprette 12 kjørsler for Intrastat-kladder som er basert på den samme malen.  
* **Varekoder**: Toll- og skattemyndighetene har laget numeriske koder som klassifiserer varer og tjenester. Du angie disse kodene for varene.
* **Koder for type transaksjon**: Land og regioner har forskjellige koder for Intrastat-transaksjonstyper, for eksempel vanlig kjøp, salg, utveksling av returnerte varer og utveksling av ikke-returnerte varer. Definer alle kodene som gjelder for landet/regionen. Du bruker disse kodene på salgs- og kjøpsdokumenter, og når du behandler returer.  
* **Transportmåter**: Det finnes sju koder med ett siffer for Intrastat-transportmåter. **1** for båt, **2** for jernbane, **3** for bil, **4** for fly, **5** for post **7** for faste installasjoner og **9** for egen fremdrift (for eksempel transportere en bil ved å kjøre den). [!INCLUDE[d365fin](includes/d365fin_md.md)] trenger ikke disse kodene, men vi anbefaler at beskrivelsene formidler en lignende betydning.  

Du kan også konfigurere følgende:

* **Transaksjonsspesifikasjoner**: Bruk disse til å supplere beskrivelsene fra transaksjonstypene.  
* **Områder**: Bruk disse til å supllere informasjonen om land og regioner.  
* **Inn-/utpunkt**: Bruk disse til å angi lokasjonene der du leverer eller mottar varer til eller fra andre land. Oslo Lufthavn Gardermoen er et eksempel på et inn-/utpunkt. Du angir inn-/utpunkt på hurtigfanen **Utenrikshandel** i salgs- og kjøpsdokumenter. Denne informasjonen blir også kopiert fra varepostene når du oppretter Intrastat-kladden.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>Slik definerer du Intrastat-maler og -kjørsler
Intrastat-kjørslene inkluderer bare vareposter, ikke finansposter. Hvis du har finansposter som er kvalifisert for intrastatrapportering, må du angi dem manuelt. Hvis du for eksempel kjøper en datamaskin fra et annet EU-land eller en annen region, plasseres ikke datamaskinen i beholdningen, men bokføres på en finanskonto. Du må angi denne typen poster manuelt i intrastatkladden.  

Du kan eksportere postene til en fil som du kan sende til Intrastat-myndighetene. Du kan også skrive ut en rapport, manuelt angi informasjonen på skjemaene fra myndighetene og deretter sende opplysningene.

>  [!Note]
> Vi anbefaler at du oppretter en Intrastat-kladdebunke for hver måned.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intrastatkladdemaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Opprett en mal for hvert Intrastat-skjema du bruker.  
3. Hvis du vil opprette kladder, velger du **Naviger** og deretter **Kladder**.  
4. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Opprett en mal for hvert Intrastat-skjema du bruker.  

> [!Note]
> I **Statistikkperiode**-feltet angir du statistikkperioden med et firesifret tall, der de to første sifrene angir år og de to neste sifrene angir måned. Angi for eksempel 1706 for juni 2017.

### <a name="to-set-up-commodity-codes"></a>Slik definerer du varekoder
Alle varer du kjøper eller selger, må ha en varetype.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varekoder**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil tilordne en varekode til en vare, går du til **Varekort**-siden, utvider hurtigfanen **Kost og bokføring** og angir deretter koden i **Varekode**-feltet.   

### <a name="to-set-up-transaction-nature-codes"></a>Slik definerer du koder for type transaksjon
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Koder for type transaksjon**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Hvis du ofte bruker en bestemt kode for en type transaksjon, kan du gjøre den standard. Hvis du vil gjøre dette, kan du gå til siden **Intrastat-oppsett** og velge koden.

### <a name="to-set-up-transport-methods"></a>Slik definerer du transportmåter
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Transportmåter**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-report-intrastat"></a>Slik rapporterer du Intrastat
Når du har fylt ut intrastatkladden, kan du skrive ut **Sjekkliste**-rapporten for å være sikker på at at all informasjon i kladden er riktig. Du kan deretter ut skrie ut en Intrastat-rapport som et skjema eller opprette en fil som skal sendes til skattemyndighetene i landet/regionen.  

### <a name="to-fill-in-intrastat-journals"></a>Slik fyller du ut Intrastat-kladder  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intrastatkladd**, og velg deretter den relaterte koblingen.  
2. På siden **Intrastatkladd** i feltet **Bunkenavn** velger du den relevante kladdebunken og velger deretter **OK**.  
3. Velg handlingen **Foreslå linjer**. Feltene **Startdato** og **Sluttdato** inneholder allerede datoene som er angitt for statistikkperioden på kladden.  
4. I feltet **Kostregulerings-%** kan du angi en prosentandel som skal dekke transport og forsikring. Hvis du angir en prosent, blir innholdet i feltet **Statistikkverdi** i kladden proporsjonalt høyere.  
5. Velg **OK** når du vil starte den satsvise jobben.  

Kjørselen henter alle varepostene i statistikkperioden og setter dem inn som linjer i intrastatkladden. Du kan redigere linjene om nødvendig.  

> [!IMPORTANT]  
>  Kjørselen henter bare postene som inneholder en lands-/regionkode som det er angitt en intrastatkode for, på siden **Land/regioner**. Derfor må du angi intrastatkoder for lands-/regionkodene du vil bruke kjørselen for.  

### <a name="how-to-report-intrastat-on-a-form-or-a-file"></a>Rapportere Intrastat i et skjema eller en fil
For å skaffe de opplysningene som trengs til Intrastat-blanketten fra statistikkmyndighetene, må du skrive ut rapporten **Intrastat - blankett**. Før du kan gjøre dette, må du forberede Intrastat-kladden og fylle den ut. Hvis du har både salgs- og kjøpstransaksjoner, må du fylle ut én blankett for hver type, slik at du må skrive ut rapporten to ganger.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intrastatkladder**, og velg deretter den relaterte koblingen.  
2. På siden **Intrastatkladd** velger du den aktuelle kladden i **Bunkenavn**-feltet.  
3. Hvis du ikke allerede har gjort dette, fyller du ut kladden manuelt eller velger **Foreslå linjer**.  
4. Velg handlingen **Skriver ut Intrastatkladd**.  
5. På hurtigfanen **Intrastatkladdelinje** legger du til et **Type**-filter og angir om det er et **Mottak** eller en **Levering**.  
6. Velg **Send til** for å skrive ut rapporten.  

### <a name="how-to-report-intrastat-in-a-file"></a>Rapportere Intrastat i en fil
Du kan sende inn Intrastat-rapporten som en fil. Før du oppretter filen kan du skrive ut en sjekkliste som inneholder de samme opplysningene som skal være i filen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intrastatkladd**, og velg deretter den relaterte koblingen.  
2. I vinduet **Intrastatkladd** velger du den aktuelle kladden i **Bunkenavn**-feltet.  
3. Hvis du ikke allerede har gjort dette, fyller du ut kladden manuelt eller velger **Foreslå linjer**.  
4. Velg handlingen **Opprett fil**.  
5. Velg **OK** i kjørselsvinduet.  
6. Velg **Lagre**.  
7. Bla til plasseringen der du vil lagre filen, skriv inn filnavnet, og velg deretter **Lagre**.

## <a name="how-to-reorganize-intrastat-journals"></a>Omorganisere Intrastat-kladder
Fordi du må levere en Intrastat-rapport hver måned, og du oppretter en ny kladd for hver rapport, må du til slutt mange kladder. Kladdelinjene slettes ikke automatisk. Det kan være nødvendig å omorganisere kladdenavnene periodisk. Det gjør du ved å slette de kladdene du ikke trenger. Kladdelinjene i disse kladdene slettes også.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Intrastatkladder**, og velg deretter den relaterte koblingen.  
2. Velg **Bunkenavn**-feltet for å vise alternativene.  
3. Velg kladdebunkene som skal slettes, og velg deretter **Slett**.  

## <a name="see-also"></a>Se også
[Økonomistyring](finance.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

