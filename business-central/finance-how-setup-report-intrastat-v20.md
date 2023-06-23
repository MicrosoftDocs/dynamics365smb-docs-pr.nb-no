---
title: Konfigurere og rapportere Intrastat
description: Lær hvordan du konfigurerer Intrastat rapporteringsfunksjoner, og hvordan til å rapportere handel med selskaper i andre EU-land.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077
ms.date: 05/23/2022
ms.author: bholtorf
ms.openlocfilehash: 5b54581c14d960b5cc52a896b41e7d7a864ee38d
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608232"
---
# <a name="set-up-and-report-intrastat" /><a name="set-up-and-report-intrastat"></a>Konfigurere og rapportere Intrastat

Alle selskaper i EU må rapportere handel med andre EU-land/-regioner. Varebevegelsen må hver måned rapporteres til statistikkmyndighetene i landet/regionen du bor i, og rapporten må leveres til skattemyndighetene. Dette kalles Intrastat-rapportering. Du bruker siden **Intrastatkladd** til å fylle ut jevnlige Intrastat-rapporter.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups" /><a name="required-and-optional-setups"></a>Nødvendige og valgfrie oppsett

> [!IMPORTANT]
> Kundekort og leverandørkort inneholder et felt, **Intrastat-partnertype** som har samme alternativverdier som feltet **Partnertype**: *"" (tom)*, *Selskap* og *Person*. Feltet **Intrastat-partnertype** har erstattet feltet **Partnertype** i Intrastat-rapportering. **Partnertype** brukes i SEPA til å definere SEPA Direct Debit Scheme (Core eller B2B). **Intrastat-partnertype** brukes bare til Intrastat-rapportering. På denne måten kan du angi ulike verdier for de to feltene, hvis du trenger det.
>
> Vær imidlertid oppmerksom på at hvis feltet **Intrastat-partnertype** er tomt, brukes verdien fra feltet **Partnertype** til Intrastat-rapportering.

Før du kan bruke Intrastat-kladden til å rapportere Intrastat-informasjon, må du konfigurere flere ting:  

* **Oppsett - Intrastat**: Siden Oppsett - Intrastat brukes til å aktivere Intrastat-rapportering og angi standarder for den. Du kan angi om du må rapportere Intrastat fra forsendelser (utsendelser), mottak (ankomster) eller begge deler, avhengig av terskler som er angitt i dine lokale forskrifter. Du kan også angi standard transaksjonstyper for vanlige dokumenter og returdokumenter, som brukes til transaksjonsrapportering.
* **Intrastat-kladdemaler**: Du må konfigurere Intrastat-kladdemalene og kjørslene du vil bruke. Siden Intrastat blir rapportert månedlig, må du opprette 12 kjørsler for Intrastat-kladder som er basert på den samme malen.  
* **Varekoder**: Toll- og skattemyndighetene har laget numeriske koder som klassifiserer varer og tjenester. Du angie disse kodene for varene.
* **Koder for type transaksjon**: Land og regioner har forskjellige koder for Intrastat-transaksjonstyper, for eksempel vanlig kjøp, salg, utveksling av returnerte varer og utveksling av ikke-returnerte varer. Definer alle kodene som gjelder for landet/regionen. Du bruker disse kodene på hurtigfanen **Utenrikshandel** på salgs- og kjøpsdokumenter, og når du behandler returer.

    > [!NOTE]
    > Fra og med januar 2022 krever Intrastat forskjellig transaksjonskode for fordeling til private enkeltpersoner eller ikke-mva-registrerte selskaper og mva-registrerte selskaper. For å overholde dette kravet anbefaler vi at du ser gjennom eller legger til nye transaksjonskoder på siden **Transaksjonstyper** i henhold til kravene i ditt land. Du bør også se gjennom og oppdatere feltet **Intrastat-partnertype** til *Personer* for private eller ikke-mva-selskapers kunder på den relevante **Kunde**-siden. Hvis du er usikker på hvilken Intrastat-partnertype eller transaksjonstype som er riktig å bruke, anbefaler vi at du spør en ekspert i landet eller området ditt.

* **Transportmåter**: Det finnes sju koder med ett siffer for Intrastat-transportmåter. **1** for båt, **2** for jernbane, **3** for bil, **4** for fly, **5** for post **7** for faste installasjoner og **9** for egen fremdrift (for eksempel transportere en bil ved å kjøre den). [!INCLUDE[prod_short](includes/prod_short.md)] trenger ikke disse kodene, men vi anbefaler at beskrivelsene formidler en lignende betydning.  
* **Transaksjonsspesifikasjoner**: Bruk disse til å supplere beskrivelsene fra transaksjonstypene.  
* **Opprinnelsesland**: Bruk de to bokstavers ISO alfa-kodene for landet der varen gode ble anskaffet eller produsert. Hvis varen ble produsert i mer enn ett land, er opprinnelseslandet det siste landet der det ble behandlet betraktelig.
* **Mva-nummer for partneroperatøren i medlemslandet for importen**: Dette er mva-ID-nummeret til partneroperatøren i medlemslandet til importen. Mva-ID-en brukes også i utvekslingen av data i mellom EU-eksport mellom medlemsland, og tillater at medlemsland fordeler de mottatte dataene til importselskapet i sitt eget land. Rapporteringsenheter må rapportere mva-ID-en til selskapet som deklarerer den intra-unionhenting av varer i medlemslandet for import.

> [!NOTE]
> Hvilken firmapartner-ID som skal brukes, kan variere, avhengig av forretningstilfellet. ID-en som skal brukes, er for eksempel forskjellige for scenarioer som kjedesalg, der en leverandør selger et produkt til et annet land, og deretter selger selskapet varen til et annet firma i samme land, trekanthandel og så videre. Hvis du er usikker på hvilken mva-ID-en som er riktig å bruke, anbefaler vi at du spør en ekspert i landet eller området ditt.

Du kan også konfigurere følgende:

* **Områder**: Bruk disse til å supllere informasjonen om land og regioner.  
* **Inn-/utpunkt**: Bruk disse til å angi lokasjonene der du leverer eller mottar varer til eller fra andre land. Oslo Lufthavn Gardermoen er et eksempel på et inn-/utpunkt. Du angir inn-/utpunkt på hurtigfanen **Utenrikshandel** i salgs- og kjøpsdokumenter. Denne informasjonen blir også kopiert fra varepostene når du oppretter Intrastat-kladden.  

### <a name="to-set-up-intrastat-templates-and-batches" /><a name="to-set-up-intrastat-templates-and-batches"></a>Slik definerer du Intrastat-maler og -kjørsler

Intrastat-kjørslene inkluderer bare vareposter, ikke finansposter. Hvis du har finansposter som er kvalifisert for intrastatrapportering, må du angi dem manuelt. Hvis du for eksempel kjøper en datamaskin fra et annet EU-land eller en annen region, plasseres ikke datamaskinen i beholdningen, men bokføres på en finanskonto. Du må angi denne typen poster manuelt i intrastatkladden.  

Du kan eksportere postene til en fil som du kan sende til Intrastat-myndighetene. Du kan også skrive ut en rapport, manuelt angi informasjonen på skjemaene fra myndighetene og deretter sende opplysningene.

> [!NOTE]
> Vi anbefaler at du oppretter en Intrastat-kladdebunke for hver måned.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Intrastatkladdemaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Opprett en mal for hvert Intrastat-skjema du bruker.  
3. Velg **Kladder**-handlingen for å opprette kladder.  
4. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Opprett en mal for hvert Intrastat-skjema du bruker.

> [!NOTE]
> I **Statistikkperiode**-feltet angir du statistikkperioden med et firesifret tall, der de to første sifrene angir år og de to neste sifrene angir måned. Angi for eksempel 1706 for juni 2017.

### <a name="to-set-up-transport-methods" /><a name="to-set-up-transport-methods"></a>Slik definerer du transportmåter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Transportmåter**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory" /><a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Slik setter du opp hvilke felt som er obligatoriske i en Intrastat-rapport

I noen land, for eksempel Spania og Storbritannia, krever skattemyndighetene at Intrastat-rapporter for eksempel må inkludere leveringsmåten for kjøp eller enkelte andre verdier ved salg over en viss grense. På siden **Oppsett - Intrastat** kan du velge **Oppsett for Intrastat-sjekkliste** for å konfigurere obligatoriske felt på **Intrastatkladd**-siden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Intrastat-oppsett** og velger den relaterte koblingen.
2. Velg handlingen **Oppsett for Intrastat-sjekkliste**.
3. På siden **Oppsett for Intrastat-sjekkliste** velger du i **Feltnavn** for å velge felt i Intrastat-rapporten du vil gjøre obligatorisk.

### <a name="czechia" /><a name="czechia"></a>Tsjekkia

Spesielt for tsjekkiske selskaper må du også definere varekoder og transaksjonsartkoder.  

#### <a name="to-set-up-commodity-codes" /><a name="to-set-up-commodity-codes"></a>Slik definerer du varekoder

Alle varer du kjøper eller selger, må ha en varetype.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varekoder**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil tilordne en varekode til en vare, går du til **Varekort**-siden, utvider hurtigfanen **Kost og bokføring** og angir deretter koden i **Varekode**-feltet.

### <a name="italy" /><a name="italy"></a>Italia

Spesielt for italienske selskaper må du også definere varekoder og transaksjonsartkoder.  

#### <a name="to-set-up-transaction-nature-codes" /><a name="to-set-up-transaction-nature-codes"></a>Slik definerer du koder for type transaksjon

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Koder for type transaksjon**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Hvis du ofte bruker en bestemt kode for en type transaksjon, kan du gjøre den standard. Hvis du vil gjøre dette, kan du gå til siden **Intrastat-oppsett** og velge koden.

## <a name="to-report-intrastat" /><a name="to-report-intrastat"></a>Slik rapporterer du Intrastat

Når du har fylt ut Intrastat-kladden, kan du kjøre handlingen **Sjekkliste** for å være sikker på at all informasjon i kladden er riktig. Obligatoriske felter du har angitt på siden **Oppsett for Intrastat-sjekkliste** som mangler verdier, vises i faktaboksen Feil og advarsler på siden **Intrastat-kladd**. Du kan deretter ut skrie ut en Intrastat-rapport som et skjema eller opprette en fil som skal sendes til skattemyndighetene i landet/regionen.  

### <a name="to-fill-in-intrastat-journals" /><a name="to-fill-in-intrastat-journals"></a>Slik fyller du ut Intrastat-kladder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Intrastatkladd** og velger den relaterte koblingen.  
2. På siden **Intrastatkladd** i feltet **Bunkenavn** velger du den relevante kladdebunken og velger deretter **OK**.  
3. Velg handlingen **Foreslå linjer**. Feltene **Startdato** og **Sluttdato** inneholder allerede datoene som er angitt for statistikkperioden på kladden.  
4. I feltet **Kostregulerings-%** kan du angi en prosentandel som skal dekke transport og forsikring. Hvis du angir en prosent, blir innholdet i feltet **Statistikkverdi** i kladden proporsjonalt høyere.  
5. Velg **OK** når du vil starte den satsvise jobben.  

Kjørselen henter alle varepostene i statistikkperioden og setter dem inn som linjer i intrastatkladden. Du kan redigere linjene om nødvendig.  

> [!IMPORTANT]  
> Kjørselen henter bare postene som inneholder en lands-/regionkode som det er angitt en intrastatkode for, på siden **Land/regioner**. Derfor må du angi intrastatkoder for lands-/regionkodene du vil bruke kjørselen for. Kjørselen setter feltet **Mva-ID for partner** til *QV999999999999* for private enkeltpersoner eller ikke-mva-selskaper (kunder som har feltet **Intrastat-partnertype** satt til *Person*) og bruker verdien til feltet **Transaksjonstype** i den bokførte vareposten eller prosjektposten.

### <a name="to-modify-intrastat-journals-lines" /><a name="to-modify-intrastat-journals-lines"></a>Slik endrer du Intrastatkladdelinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Intrastatkladd** og velg den relaterte koblingen.  
2. På siden **Intrastatkladd** i feltet **Bunkenavn** velger du den relevante kladdebunken og velger deretter **OK**.  
3. Bruk filterruten til å filtrere Intrastat-kladdelinjer basert på noen kriterier. Filtrer for eksempel på feltene **Mva-ID for partner** med verdien *QV999999999999*.
4. Velg **Del**-ikonet ![Del en side i en annen app.](media/share-icon.png) og velg **Rediger i Excel**
5. I Excel endrer du Intrastatkladdelinjer som du filtrerte ut. Du kan for eksempel endre feltverdier for **Transaksjonstype**.  
6. Publiser endringene du har gjort i Excel, tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)]-versjoner som ikke støtter [**Rediger i Excel**](across-work-with-excel.md#edit-in-excel) for kladder, kan du opprette konfigurasjonspakker for å eksportere og importere Intrastatkladdelinjer til Excel. Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet.

### <a name="report-intrastat-on-a-form-or-a-file" /><a name="report-intrastat-on-a-form-or-a-file"></a>Rapportere Intrastat i et skjema eller en fil

For å skaffe de opplysningene som trengs til Intrastat-blanketten fra statistikkmyndighetene, må du skrive ut rapporten **Intrastat - blankett**. Før du kan gjøre dette, må du forberede Intrastat-kladden og fylle den ut. Hvis du har både salgs- og kjøpstransaksjoner, må du fylle ut én blankett for hver type, slik at du må skrive ut rapporten to ganger.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Intrastatkladder** og velger den relaterte koblingen.  
2. På siden **Intrastatkladd** velger du den aktuelle kladden i **Bunkenavn**-feltet.  
3. Hvis du ikke allerede har gjort dette, fyller du ut kladden manuelt eller velger **Foreslå linjer**.  
4. Velg handlingen **Skriver ut Intrastatkladd**.  
5. På hurtigfanen **Intrastatkladdelinje** legger du til et **Type**-filter og angir om det er et **Mottak** eller en **Levering**.  
6. Velg **Send til** for å skrive ut rapporten.  

### <a name="report-intrastat-in-a-file" /><a name="report-intrastat-in-a-file"></a>Rapportere Intrastat i en fil

Du kan sende inn Intrastat-rapporten som en fil. Før du oppretter filen kan du skrive ut en sjekkliste som inneholder de samme opplysningene som skal være i filen.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Intrastatkladd** og velg den relaterte koblingen.  
2. På siden **Intrastatkladd** velger du den aktuelle kladden i **Bunkenavn**-feltet.  
3. Hvis du ikke allerede har gjort dette, fyller du ut kladden manuelt eller velger **Foreslå linjer**.  
4. Velg handlingen **Opprett fil**.  
5. Velg **OK**-knappen på kjørselssiden.  
6. Velg **Lagre**.  
7. Bla til plasseringen der du vil lagre filen, skriv inn filnavnet, og velg deretter **Lagre**.

> [!NOTE]
> Når en linje i Intrastat-rapporten har en supplerende enhet, vil ikke vekten av varen vises, ettersom denne verdien ikke er nødvendig.

## <a name="reorganize-intrastat-journals" /><a name="reorganize-intrastat-journals"></a>Omorganisere Intrastat-kladder

Fordi du må levere en Intrastat-rapport hver måned, og du oppretter en ny kladd for hver rapport, må du til slutt mange kladder. Kladdelinjene slettes ikke automatisk. Det kan være nødvendig å omorganisere kladdenavnene periodisk. Det gjør du ved å slette de kladdene du ikke trenger. Kladdelinjene i disse kladdene slettes også.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Intrastatkladder** og velger den relaterte koblingen.  
2. Velg **Bunkenavn**-feltet for å vise alternativene.  
3. Velg kladdebunkene som skal slettes, og velg deretter **Slett**.  

## <a name="tariff-numbers" /><a name="tariff-numbers"></a>Tariffnumre

I mange land lager toll- og skattemyndighetene 8-sifrede varekoder for ulike varer. For at vareposter skal inneholde den nødvendige informasjonen når programmet leser dem inn på en Intrastatkladdelinje, må du allerede ha skrevet inn informasjon om tariffnummeret på siden **Tariffnummer**. Finn kodene for varene som selskapet ditt handler med, og angi dem på **Tariffnumre**-siden.

På siden **Tariffnummer** kan du legge til alle kodene du bruker. Du må skrive inn kodene på varekortet før du begynner å bokføre. Når du har definert kodene, setter du dem inn i **Tariffnr.** -feltet på varekortet. Du må også fylle ut feltet **Nettovekt** på varekortet.

## <a name="see-related-training-at-microsoft-learnlearnmodulesprocess-intrastat-dynamics-365-business-centralindex" /><a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also" /><a name="see-also"></a>Se også

[Økonomistyring](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
