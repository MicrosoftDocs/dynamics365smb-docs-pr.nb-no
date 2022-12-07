---
title: Synkroniser varer og lager
description: Konfigurer og kjør synkroniseringer av varer mellom Shopify og Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30116, 30117, 30126, 30127,
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: a14e81932ab2cc02c691d6dfe8a9a1c4fe326410
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802960"
---
# <a name="synchronize-items-and-inventory"></a>Synkroniser varer og lager

**Varene** i [!INCLUDE[prod_short](../includes/prod_short.md)] tilsvarer *produktene* i Shopify, som inkluderer fysiske varer, digitale nedlastinger, tjenester og gavekort du kan selge. Det er to hovedgrunner til å synkronisere varene:

1. Databehandling utføres først og fremst i [!INCLUDE[prod_short](../includes/prod_short.md)]. Du må eksportere alle eller noen data derfra til Shopify og gjøre dem synlige. Du kan eksportere varenavn, beskrivelse, bilde, priser, tilgjengelighet, varianter, leverandørdetaljer og strekkode. Når du har eksportert, kan du se gjennom varene eller gjøre dem synlige umiddelbart.
2. Når en ordre fra Shopify importeres, er informasjonen om varer viktig for ytterligere behandling av dokumentbehandling i [!INCLUDE[prod_short](../includes/prod_short.md)].

De to foregående scenarioene er alltid aktivert.

Et tredje scenario er å behandle data i Shopify, men importere disse varene i bulk til [!INCLUDE[prod_short](../includes/prod_short.md)]. Dette scenarioet kan være nyttig for dataoverføringshendelser, som når du vil koble en eksisterende nettbutikk med et nytt [!INCLUDE[prod_short](../includes/prod_short.md)]-miljø.

## <a name="define-item-synchronizations"></a>Definer varesynkroniseringer

1. Velg søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Åpne butikken du vil konfigurere varesynkronisering for.
2. Velg ønsket alternativ i feltet **Synkroniser vare**.

   Tabellen nedenfor viser alternativene.

|Alternativ|Description|
|------|-----------|
|**Tom**| Produkter importeres sammen med import av ordrer. Produkter eksporteres til Shopify hvis en bruker kjører **Legg til vare**-handlingen fra siden **Shopify-produkter**. Dette er standardprosessen.|
|**Til Shopify**| Velg dette alternativet hvis du planlegger å oppdatere produkter manuelt ved å bruke **Synkroniser produkt**-handlingen eller med jobbkøen for regelmessige oppdateringer etter første synkronisering er utløst av **Legg til vare**-handlingen. Husk å aktivere feltet **Kan oppdatere Shopify-produkt**. Hvis den ikke er aktivert, er det lik alternativet **Tom** (standard prosess). Finn ut mer i delen [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify).|
|**Fra Shopify**| Velg dette alternativet hvis du har tenkt å importere produkter fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser produkt**-handlingen eller med jobbkøen for regelmessige oppdateringer. Finn ut mer i delen [Importer varer fra Shopify](synchronize-items.md#import-items-from-shopify).|

## <a name="import-items-from-shopify"></a>Importer varer fra Shopify

Først importerer du fra Shopify samtidig eller sammen med ordrer for å legge dem til i tabellene **Shopify-produkt** og **Shopify-variant**. Tildel deretter importerte produkter og varianter til varer og varianter i [!INCLUDEprod_short]. Administrer prosessen med følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Opprett ukjente varer automatisk**|Når Shopify-produkter og -varianter importeres til [!INCLUDE[prod_short](../includes/prod_short.md)], prøver [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjonen alltid å finne tilsvarende post i varelisten. **SKU-tildeling** påvirker hvordan samsvaret utføres og oppretter en ny vare eller varevariant. Aktiver dette alternativet hvis du vil opprette en ny vare eller når det ikke finnes en samsvarende post. Den nye varen opprettes ved hjelp av importerte data og **varemalkode**. Hvis dette alternativet ikke er aktivert, må du opprette en vare manuelt og bruke **Produkttildeling**-handlingen på siden **Shopify-produkter**.|
|**Varemalkode**|Bruk denne sammen med vekslebryteren **Opprett ukjente kunder automatisk**.<br>Velg malen du vil bruke for automatisk opprettede varer.|
|**SKU-tilordning**|Velg hvordan du vil bruke **SKU**-verdien som er importert fra Shopify, under vare/variant-tildeling og -oppretting. Finn ut mer i delen [Effekten av SKU-er og strekkoder for Shopify-produkt på tildeling og oppretting av varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**SKU-skilletegn**|Bruk denne sammen med **Tildeling for lagerføringsenhet** angitt til alternativet **[Varenr. + variantkode](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Definer et skilletegn som skal brukes til å dele SKU-en.<br>Hvis du oppretter varianten med SKU-en 1000/001 i Shopify, skriver du inn / i feltet **SKU-skilletegn** for å hente varenummeret i [!INCLUDE[prod_short](../includes/prod_short.md)] som 1000 og varevariantkoden som 001.|
|**Variantprefiks**|Bruk sammen med **SKU-tildeling** satt til **Variantkode** eller alternativene **Varenr. + variantkode** som en reservefunksjon når SKU-en som kommer fra Shopify, er tom.<br>Hvis du vil opprette varevarianten i [!INCLUDE[prod_short](../includes/prod_short.md)] automatisk, må du angi en verdi i **Kode**. Som standard brukes verdien som er definert i SKU-feltet som ble importert fra Shopify. Hvis SKU er tom, vil det imidlertid generere en kode som begynner med definert variantprefiks og 001.|
|**Shopify kan oppdatere vare**|Velg dette alternativet hvis du vil oppdatere varer eller varianter automatisk.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Effekten av SKU-er og strekkoder definert i Shopify-produkt på tildeling og oppretting av varer og varianter i Business Central

Når produkter importeres fra Shopify til tabellene **Shopify-produkter** og **Shopify-varianter**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å finne eksisterende poster.

Tabellen nedenfor viser forskjellene mellom alternativene i feltet **SKU-tildeling**.

|Alternativ|Innvirkning på tildeling|Innvirkning ved oppretting|
|------|-----------------|------------------|
|**Tom**|SKU-feltet brukes ikke i varetildelingsrutinen.|Ingen innvirkning på oppretting av varen.<br>Dette alternativet hindrer oppretting av varianter. Når det gjelder ordre, brukes bare hovedvare. En variant kan fremdeles tildeles manuelt på siden **Shopify-produkt**.|
|**Varenr.**|Velg hvis SKU-feltet inneholder varenummeret|Ingen innvirkning på oppretting av en vare uten varianter. For en vare med varianter opprettes hver variant som en separat vare.<br>Hvis Shopify har et produkt med to varianter, og deres SKU-er er 1000 og 2000 i [!INCLUDE[prod_short](../includes/prod_short.md)], opprettes to varer med tallene 1000 og 2000.|
|**Variantkode**|SKU-feltet brukes ikke i varetildelingsrutinen.|Ingen innvirkning på oppretting av varen. Når det opprettes en varevariant, brukes verdien i SKU-feltet som en kode. Hvis SKU er tom, genereres det en kode ved hjelp av feltet **Variantprefiks**.|
|**Varenr. + variantkode**|Velg dette hvis SKU-feltet inneholder et varenummer og varevariantkoden, atskilt med verdien som er definert i feltet felt **SKU-skilletegn**.|Når du oppretter en vare, blir den første delen av verdien i feltet SKU angitt som **Nr.**. Hvis SKU-feltet er tomt, genereres et varenummer med nummerserien definert i feltet **Varemalkode** eller **Varenr.** på siden **Lageroppsett**.<br>Når du oppretter en vare, bruker variantfunksjonen den andre delen av verdien i feltet SKU som **Kode**. Hvis SKU-feltet er tomt, genereres det en kode ved hjelp av feltet **Variantprefiks**.|
|**Leverandørs varenr.**|Velg hvis SKU-feltet inneholder leverandørvarenummeret. I dette tilfellet blir ikke **Leverandørvarenr.** brukt på siden **Varekort**, i stedet brukes **Leverandørvarenr.** fra **Leverandørens varekatalog**. Hvis posten *Vareleverandørkatalog* inneholder en variantkode, brukes denne koden til å tildele Shopify-varianten.|Hvis det finnes en tilsvarende leverandør i [!INCLUDE[prod_short](../includes/prod_short.md)], blir lagerføringsenhetsverdien brukt som **Leverandørs varenr.** på siden **Varekort** og som **varereferanse** av *leverandørtypen*. <br>Forhindrer oppretting av varianter. Det er nyttig når du bare vil bruke hovedvare i ordren. Du kan fremdeles tildele en variant manuelt fra siden **Shopify-produkt**.|
|**Strekkode**|Velg hvis SKU-feltet inneholder en strekkode. Det utføres et søk mellom **varereferanser** av *strekkodetypen*. Hvis varereferanseposten inneholder en variantkode, brukes denne variantkoden til å tildele Shopify-varianten.|Ingen innvirkning på oppretting av varen. <br>Forhindrer oppretting av varianter. Det er nyttig når du bare vil bruke hovedvare i ordren. Du kan fremdeles tildele en variant manuelt fra siden **Shopify-produkt**.|

Tabellen nedenfor gir en oversikt over innvirkningen til feltet **Strekkode**.

|Innvirkning på tildeling|Innvirkning ved oppretting|
|-----------------|------------------|
|Det utføres et søk mellom **varereferanser** som har en strekkodetype for verdien som er definert i **Strekkode**-feltet i Shopify. Hvis varereferanseposten inneholder en variantkode, brukes denne variantkoden til å tildele Shopify-varianten.|Strekkoden lagres som **varereferanse** for varen og varevarianten.|

> [!NOTE]  
> Du kan utløse tildeling av de valgte produktene/variantene ved å velge **Prøv søk etter produkttildeling** eller alle importerte ikke-tildelte produkter ved å velge **Prøv å finne tildelinger**.

## <a name="export-items-to-shopify"></a>Eksporter varer til Shopify

Velg varene fra varelisten som skal eksporteres til Shopify. Bruk handlingen **Legg til vare** på siden **Shopify-produkter** for å legge til varer i Shopify-produktlisten.

Du administrerer prosessen med å eksportere varer ved å bruke følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Kundeprisgruppe**|Bestemme prisen for en vare i Shopify. Salgsprisen for denne kundeprisgruppen tas. Hvis ingen gruppe angis, brukes prisen på varekortet.|
|**Kunderabattgruppe**|Bestemme rabatten som skal brukes til å beregne prisen på en vare i Shopify. Rabatterte priser lagres i **Pris**-feltet, og hele prisen er lagret i feltet **Sammenlign med pris**.|
|**Synkroniser utvidet tekst for vare**|Velg dette for å synkronisere den utvidede teksten for varen. Den kan inneholde HTML-kode slik den blir lagt til i feltet *Beskrivelse*. |
|**Synkroniser vareattributter**|Velg dette for å synkronisere vareattributter. Attributter formateres som en tabell og inkluderes i *Beskrivelse*-feltet i Shopify.|
|**Språkkode**|Velg dette hvis du ønsker de oversatte versjonene til tittel, attributter og utvidet tekst.|
|**SKU-tilordning**|Velg hvordan du vil fylle ut feltet for lagerføringsenhet i Shopify. Støttede alternativer er:<br> - **Varenr.** for å bruke varenr. for både produkter og varianter.<br> - **Varenr. + variantkode** for å opprette en lagerføringsenhet ved å sette sammen verdier fra to felter. For varer uten varianter brukes bare varenummeret.<br>- **Leverandørs varenr.** for å bruke vareleverandørnummeret som er definert på *varekortet* for både varer og varianter.<br> - **Strekkode** for å bruke strekkodetypen **Varereferanse**. Dette alternativet respekterer varianter.|
|**SKU-skilletegn**|Definer et skilletegn for alternativet **Varenr. + variantkode**.|
|**Lager sporet**| Velg hvordan systemet skal fylle ut feltet **Spor lager** for produkter som er eksportert til Shopify. Du kan oppdatere tilgjengelighetsinformasjon fra [!INCLUDE[prod_short](../includes/prod_short.md)] for produkter i Shopify der spor lager er aktivert. Finn ut mer i delen [Lager](synchronize-items.md#sync-inventory-to-shopify).|
|**Standard lagerpolicy**|Velg *Avslå* for å unngå negativ beholdning på Shopify-siden.|
|**Kan oppdatere Shopify-produkter**|Definer dette hvis [!INCLUDE[prod_short](../includes/prod_short.md)] kan bare opprette varer eller kan oppdatere varer også. Velg dette alternativet hvis du planlegger å oppdatere produkter manuelt ved å bruke **Synkroniser produkt**-handlingen eller med jobbkøen for regelmessige oppdateringer etter første synkronisering er utløst av **Legg til vare**-handlingen. Husk å velge **Til Shopify** i feltet **Varesynkronisering**.|
|**Kundemalkode**|Velg standardmalen som skal brukes under prisberegningen. Finn ut mer under [Definer avgifter](setup-taxes.md).|

### <a name="fields-mapping-overview"></a>Oversikt over felttildeling

|Shopify|Kilde når den eksporteres fra [!INCLUDE[prod_short](../includes/prod_short.md)]|Mål når det importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|I henhold til feltet **Status for opprettede produkter** på **Shopify-butikkortet**. Finn ut mer in delen [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Ikke i bruk.|
|Tittel | **Beskrivelse**. Hvis språkkoden er definert og en tilsvarende vareoversettelse eksisterer, blir vareoversettelse brukt i stedet for beskrivelse.|**Beskrivelse**|
|Description|Kombinerer utvidede tekster og attributter hvis tilsvarende veksler på Shopify-butikkortet er aktivert. Overholder språkkode.|Ikke i bruk.|
|SEO-sidetittel|Fast verdi: tom. Finn ut mer in delen [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Ikke i bruk.|
|SEO-metabeskrivelse|Fast verdi: tom. Finn ut mer in delen [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Ikke i bruk.|
|Medium|**Bilde**. Finn ut mer i delen [Synkroniser varebilder](synchronize-items.md#sync-item-images)|**Bilde**|
|Pris|Beregningen av sluttkundepris omfatter vareprisgruppe, varerabattgruppe, valutakode og kundemalkode.|**Enhetspris**|
|Sammenlign i prisen|Beregningen av prisen uten rabatt omfatter vareprisgruppe, varerabattgruppe, valutakode og kundemalkode.|Ikke i bruk.|
|Kostnad per vare|**Enhetskost**|**Enhetskost**|
|LFE|Finn ut mer om dette under **SKU-tildeling** i delen [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify).|Finn ut mer om dette i delen [Effekten av SKU-er og strekkoder for Shopify-produkt på tildeling og oppretting av varer og varianter i Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Strekkode|**Varereferanser** av strekkodetypen.|**Varereferanser** av strekkodetypen.|
|Spor antall|I henhold til feltet **Lager sporet** på siden **Shopify-butikkort**. Finn ut mer i delen [Lager](synchronize-items.md#sync-inventory-to-shopify).|Ikke i bruk.|
|Fortsett å selge når tomt på lager|I henhold til **Standard lagerpolicy** på **Shopify-butikkortet**. Ikke importert.|Ikke i bruk.|
|Type|**Beskrivelse** av **Varekategorikode**. Hvis typen ikke er angitt i Shopify, blir den lagt til som en egendefinert type.|**Varekategorikode**. Tildeling etter beskrivelse.|
|Leverandør|**Navn** på leverandør fra **Leverandørnr.**|**Leverandørnr.**-tildeling etter navn.|
|Vekt|**Bruttovekt**.|Ikke i bruk.|
|Avgiftspliktig|Fast verdi: aktivert.|Ikke i bruk.|
|Avgiftskoder|**Mva-gruppekode**. Bare relevant for merverdiavgift. Finn ut mer under [Definer avgifter](setup-taxes.md).|Ikke i bruk.|

### <a name="tags"></a>Koder

Gå gjennom de importerte kodene i **Koder**-faktaboksen på siden **Shopify-produkt**. Velg handlingen **Koder** på den samme siden for å redigere koder.
Hvis alternativet **Til Shopify** er valgt i feltet **Synkroniser vare**, eksporteres tildelte koder til Shopify ved neste synkronisering.

## <a name="run-item-synchronization"></a>Kjør varesynkronisering

Fullstendig eller delvis varesynkronisering kan utføres på mange forskjellige måter.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Første synkronisering av varer fra Business Central til Shopify

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Legg til varer**.
3. I feltet **Butikkode** angir du koden. Hvis du åpner vinduet **Shopify-produkt** fra siden **Butikkort**, fylles butikkoden ut automatisk.
4. Definer filtre for varer etter behov. Du kan for eksempel filtrere etter varenr. eller varekategorikode.
5. Velg **OK**.

De resulterende varene opprettes automatisk i Shopify med priser, men bilder og lagernivåer inkluderes ikke. Operasjonen kan ta litt tid hvis et stort antall varer legges til.

### <a name="sync-products-from-shopify-to-business-central"></a>Synkroniser produkter fra Shopify til Business Central

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser produkter**.

Du kan også bruke handlingen **Synkroniser produkter** på siden **Shopify-produkter** eller søk etter den satsvise jobben **Synkroniser produkter**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Ad hoc-oppdateringer av Shopify-produkter

Når postene oppdateres i tabellen **Shopify-produkt**, synkroniseres følgende endringer med Shopify.

Oppdater:

* **Status** – du kan velge mellom aktiv, arkivert eller kladd.
* **SEO-tittel**
* **SEO-beskrivelse**

Sletting:

Avhengig av verdien i **Handling for fjernede produkter** på siden **Shopify-butikkort**, blir produktet oppdatert i Shopify når posten slettes fra siden **Shopify-produkt**.

* **Tom** – ingenting skjer. Om nødvendig må du utføre den nødvendige handlingen fra **Shopify-administratoren**.
* **Status til utkast** – status av produktet i Shopify er satt til *utkast*.
* **Status til arkivert** – produktet arkiveres i Shopify.

## <a name="sync-item-images"></a>Synkroniser varebilder

Synkronisering av bilder kan konfigureres for synkroniserte varer. Velg blant følgende alternativer:

* **Deaktivert** – bildesynkronisering er deaktivert.
* **Til Shopify** – bilder av varer eksporteres til Shopify.
* **Fra Shopify** – bilder fra Shopify importeres til [!INCLUDE[prod_short](../includes/prod_short.md)].

Bildesynkronisering kan startes på de to måtene beskrevet nedenfor.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Synkroniser produktbilder fra siden Shopify-butikk

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere bilder med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser produktbilder**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Synkroniser produktbilder fra siden Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser produktbilder**.

### <a name="image-synchronization-remarks"></a>Bildesynkroniseringsmerknader

* Når du eksporterer bilder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, legges de nye bildene til i Shopify, noe som gjør at gamle bilder beholdes. Hvis et bilde blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)], må du slette gamle bilder i **Shopify-administratoren**.
* Bilder som eksporteres til Shopify som ikke samsvarer med kravene som er definert av Shopify, importeres ikke. Finn ut mer om [produktmedietyper på help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Synkroniser priser med Shopify

Priser for synkroniserte varer kan eksporteres på de to måtene som er beskrevet nedenfor.

### <a name="sync-prices-from-the-shopify-products-page"></a>Synkroniser priser fra siden Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser priser til Shopify**.

### <a name="price-calculation-remarks"></a>Prisberegningsmerknader

* Ved prisberegning er det viktig å ha en verdi i feltet **Standard kundemal**. Finn ut mer under [Definer avgifter](setup-taxes.md).
* Angi en **valutakode** bare hvis nettbutikken bruker en annen valuta enn lokal valuta (LV). Den angitte valutaen må ha valutakurser konfigurert. Hvis nettbutikken bruker samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], lar du feltet stå tomt.
* Når du skal fastsette en pris, bruker [!INCLUDE[prod_short](../includes/prod_short.md)] laveste pris-logikk. Dette betyr at hvis enhetsprisen som er definert på varekortet, er lavere enn det som er angitt i prisgruppen, brukes enhetsprisen fra varekortprisen.

## <a name="sync-inventory-to-shopify"></a>Synkroniser lager til Shopify

Lagersynkronisering kan konfigureres for allerede synkroniserte varer. Det finnes to betingelser som må oppfylles:

1. Lagersporing må være aktivert for et produkt i Shopify. Hvis varer eksporteres til Shopify, bør du vurdere å aktivere **Lager sporet** på siden **Shopify-butikk**. Finn ut mer i delen [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify).
2. Lagersynkronisering må være aktivert for **Shopify-lokasjoner**.

### <a name="to-enable-inventory-sync"></a>Slik aktiverer du lagersynkronisering

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere lager med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
4. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Du finner dem i innstillingene [**Lokasjoner**](https://www.shopify.com/admin/settings/locations) i **Shopify-administratoren**.
5. I feltet **Lokasjonsfilter** legger du til lokasjoner hvis du bare vil ta med lager fra bestemte lokasjoner. Du kan skrive inn *ØST|VEST* for å gjøre lageret fra bare disse to lokasjonene tilgjengelig for salg via nettbutikken.
6. Fjern merket for **Deaktivert** for å aktivere lagersynkronisering for valgte Shopify-lokasjoner.

Du kan starte lagersynkronisering på de to måtene beskrevet nedenfor.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Synkroniser lager fra siden Shopify-butikk

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere lager med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser lager**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Synkroniser lager fra siden Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser lager**.

### <a name="inventory-remarks"></a>Lagermerknader

* Koblingen beregner **Beregnet disponibel saldo** på nåværende dato og eksporterer den til Shopify.
* Du kan kontrollere lagerinformasjonen mottatt fra Shopify på siden **Shopify-lagerfaktaboks**. I denne faktaboksen får du en oversikt over Shopify-lageret og det siste beregnede lageret i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes én post per lokasjon.
* Hvis lagerinformasjonen i Shopify er forskjellig fra **Beregnet disponibel saldo** i [!INCLUDE[prod_short](../includes/prod_short.md)], blir lageret oppdatert i Shopify.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Eksempel på beregning av beregnet disponibel beholdning

Det finnes 10 stykker av varen A tilgjengelig på lager og to utestående ordrer. En for mandag med antall *én* og en for torsdag med antall *to*. Avhengig av når du synkroniserer lageret, vil systemet oppdatere lagernivået i Shopify med ulike antall:

|Når synkronisering av lageret kjøres|Verdi som brukes til å oppdatere lagernivå|Merknad|
|------|-----------------|-----------------|
|Tirsdag|9|Lager 10 minus ordre angitt til forsendelse på mandag|
|Fredag|7|Lager 10 minus begge ordrer|

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
