---
title: Synkroniser varer og lager
description: Konfigurer og kjør synkroniseringer av varer mellom Shopify og Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: c7aea0d0b3d9a8902e704a2d390d6a244e8cbbef
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317303"
---
# <a name="synchronize-items-and-inventory"></a>Synkroniser varer og lager

**Varene** i [!INCLUDE[prod_short](../includes/prod_short.md)] tilsvarer *produktene* i Shopify, som inkluderer fysiske varer, digitale nedlastinger, tjenester og gavekort du selger. Det er to hovedgrunner til å synkronisere varene:

1. Databehandlingen er primært utført i [!INCLUDE[prod_short](../includes/prod_short.md)], men du må eksportere alle data eller noen data Shopify og gjøre den synlig. Du kan eksportere varenavn, beskrivelse, bilde, priser, tilgjengelighet, varianter, leverandørdetaljer og strekkode. Når elementene er importert, kan de bli synlige med en gang, eller de kan gjennomgås og forbedres av en ansvarlig person først.
2. Når en ordre fra Shopify importeres, er informasjonen om varer nødvendig for ytterligere behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)].

Disse to scenarioene er alltid aktivert.

Et tredje scenario er å behandle data i Shopify, men importere disse varene i bulk til [!INCLUDE[prod_short](../includes/prod_short.md)]. Dette scenarioet kan være nyttig for dataoverføringshendelser når du vil koble en eksisterende nettbutikk med et nytt [!INCLUDE[prod_short](../includes/prod_short.md)]-miljø.

## <a name="to-define-item-synchronizations"></a>Slik definerer varesynkroniseringer

1. Velg søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Åpne et verksted du vil konfigurere varesynkronisering for.
2. Velg ønsket alternativ i feltet **Synkroniser vare**. <br>Tabellen nedenfor viser forskjellene mellom de ulike alternativene.

|Alternativ|Description|
|------|-----------|
|**Tom**| Produkter importeres sammen med import av ordrer. Produkter eksporteres til Shopify hvis en bruker kjører **Legg til vare**-handlingen fra siden **Shopify-produkter**. Denne prosessen er standard virkemåte. |
|**Til Shopify**| Velg dette alternativet hvis du planlegger å oppdatere produkter manuelt ved å bruke **Synkroniser produkt**-handling eller via jobbkø for regelmessige oppdateringer etter første synkronisering som er utløst av **Legg til vare**-handling. Husk å aktivere feltet **Kan oppdatere Shopify-produkt**. Hvis alternativet ikke er aktivert, er alternativet bare **tomt**. Hvis du vil ha mer informasjon, kan du se [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify)|
|**Fra Shopify**| Velg dette alternativet hvis du har tenkt å importere produkter fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser produkt**-handling eller via jobbkø for regelmessige oppdateringer. Hvis alternativet ikke er valgt, er det lik **tomt** alternativ. Hvis du vil ha mer informasjon om import av varer, kan du se [Importer varer fra Shopify](synchronize-items.md#import-items-from-shopify)|

## <a name="import-items-from-shopify"></a>Importer varer fra Shopify

Enten du importerer varer fra Shopify samtidig eller sammen med import av ordrer, legges disse varene til først i tabellene **-Shopifyprodukt** og **Shopify-variant**. Ved hjelp av disse innstillingene kan du behandle prosessen:

|Felt|Description|
|------|-----------|
|**Opprett ukjente varer automatisk**|Når Shopify-produkter og -varianter importeres til [!INCLUDE[prod_short](../includes/prod_short.md)], prøver [!INCLUDE[prod_short](../includes/prod_short.md)]-funksjonen alltid å finne tilsvarende post i varelisten først. **SKU-tildeling** påvirker hvordan samsvaret utføres og oppretter ny vare eller varevariant. Aktiver dette alternativet hvis du vil opprette en ny vare eller når det ikke finnes en samsvarende post. Den nye varen blir opprettet ved hjelp av importerte data og **varemalkode**. Hvis dette alternativet ikke er aktivert, må du opprette en vare manuelt og bruke **Produkttildeling**-handlingen fra siden **Shopify-produkter**.|
|**Varemalkode**|Brukes sammen med **Opprett ukjente kunder automatisk**. <br> Velg malen som skal brukes for automatisk opprettede varer.|
|**SKU-tilordning**|Velg hvordan du vil bruke **SKU**-verdien som er importert fra Shopify, under vare/variant-tildeling og -oppretting. Hvis du vil ha mer informasjon, kan du se [Hvordan SKU og strekkode definert i Shopify-produkt påvirker tildeling og oppretting av varer og varianter](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**SKU-skilletegn**|Brukes sammen med **SKU-tildeling** angitt til alternativet **Varenr. + variantkode**.<br> Definer et skilletegn som skal brukes til å dele SKU. <br>Hvis du for eksempel oppretter varianten med SKU-en 1000/001 i Shopify, skriver du inn / i feltet **SKU-skilletegn** for å hente varenummeret i [!INCLUDE[prod_short](../includes/prod_short.md)] som 1000 og varevariantkoden som 001.
|**Variantprefiks**|Brukes sammen med **SKU-tildeling** satt til **Variantkode** eller alternativene **Varenr. + variantkode** som en reservestrategi når SKU-en som kommer fra Shopify, er tom.<br>Hvis du vil opprette varevarianten i [!INCLUDE[prod_short](../includes/prod_short.md)] automatisk, må du angi en verdi i **Kode**. Som standard brukes verdien som er definert i SKU-feltet som ble importert fra Shopify. Hvis SKU er tom, vil det imidlertid generere en kode som begynner med definert variantprefiks og 001.|
|**Shopify kan oppdatere vare**| Velg dette alternativet hvis du vil oppdatere varer eller varianter automatisk.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Hvordan SKU-er og strekkoder definert i Shopify-produkt påvirker tildeling og oppretting av varer og varianter i Business Central

Når produkter importeres fra Shopify til tabellene **Shopify-produkter** og **Shopify-varianter**, prøver [!INCLUDE[prod_short](../includes/prod_short.md)] å finne eksisterende poster. Tabellen nedenfor viser forskjellene mellom de ulike alternativene i feltet **SKU-tildeling**.

|Alternativ|Innvirkning på tildeling|Innvirkning ved oppretting|
|------|-----------------|------------------|
|**Tom**|SKU-feltet brukes ikke i varetildelingsrutine.|Ingen innvirkning på oppretting av varen. <br>Forhindrer oppretting av varianter. Det er nyttig når det gjelder ordre, men bare hovedvare brukes. En variant kan fremdeles tildeles manuelt fra vinduet **Shopify-produkt**.|
|**Varenr.**|Velg hvis SKU-feltet inneholder varenr.|Ingen innvirkning på oppretting av vare uten varianter. For en vare med varianter opprettes hver variant som en separat vare.<br> Hvis Shopify for eksempel har et produkt med to varianter, og deres SKU-er er 1000 og 2000 i [!INCLUDE[prod_short](../includes/prod_short.md)]-system, opprettes to varer med tallene 1000 og 2000.|
|**Variantkode**|SKU-feltet brukes ikke i varetildelingsrutinen.|Ingen innvirkning på oppretting av varen. Når det opprettes en varevariant, brukes verdien i SKU-feltet som en kode. Hvis SKU er tom, genereres det en kode ved hjelp av feltet **Variantprefiks**.|
|**Varenr. + variantkode**| Velges hvis SKU-feltet inneholder et varenr. og varevariantkoden, atskilt med verdi som er definert i feltet felt **SKU-skilletegn**.|Når du oppretter en vare, blir den første delen av verdien i feltet SKU brukt som **Nr.**. Hvis SKU er tom, genereres et varenr. med nummerserie definert i **varemalkode** eller **Varenr.** i vinduet **Lageroppsett**.<br>Når du oppretter en vare, bruker variantfunksjonen den andre delen av verdien i feltet SKU som **Kode**. Hvis SKU er tom, genereres det en kode ved hjelp av feltet **Variantprefiks**.|
|**Leverandørs varenr.**| Velg om SKU-feltet inneholder leverandørs varenr. I dette tilfellet brukes ikke **Leverandørs varenr.** i vinduet **Varekort**, men **Leverandørs varenr.** fra **Leverandørs varekatalog**. Hvis posten *Vareleverandørkatalog* inneholder en variantkode, brukes denne variantkoden til å tildele Shopify-varianten.|Hvis det finnes en tilsvarende leverandør i [!INCLUDE[prod_short](../includes/prod_short.md)], blir SKU-verdien brukt som **Leverandørs varenr.** på **varekortet** og som **varereferanse** av typen leverandør. <br>Forhindrer oppretting av varianter. Det er nyttig når du bare vil bruke hovedvare i ordren. Du kan fremdeles tildele en variant manuelt fra vinduet **Shopify-produkt**.|
|**Strekkode**| Velg hvis SKU-feltet inneholder en strekkode. Det utføres et søk mellom **varereferanser** av typen leverandør. Hvis posten Varereferanse inneholder en variantkode, brukes denne variantkoden til å tildele Shopify-varianten.|Ingen innvirkning på oppretting av varen. <br>Forhindrer oppretting av varianter. Det kan være nyttig hvis bare hovedelementet brukes i ordren. En variant kan fremdeles tildeles manuelt fra vinduet **Shopify-produkt**.|

Tabellen nedenfor gir en oversikt over innvirkningen til feltet **Strekkode**.

|Innvirkning på tildeling|Innvirkning ved oppretting|
|-----------------|------------------|
|Det utføres et søk mellom **varereferanser** av typen strekkode for verdien som er definert i Strekkode-feltet i Shopify. Hvis varereferansepost inneholder en variantkode, brukes denne variantkoden til å tildele Shopify-varianten.|Strekkode lagres som **varereferanse** for vare og varevariant.|

> [!NOTE]  
> Du kan utløse tildeling for de valgte produktene/variantene eller alle importerte ikke-tildelte produkter ved å velge **Prøv søk etter produkttildeling** (for valgt) eller **Prøv å finne tildelinger** (for alle).

## <a name="export-items-to-shopify"></a>Eksporter varer til Shopify

Velg varene fra varelisten som skal eksporteres til Shopify. Bruk handlingen **Legg til vare** fra vinduet **Shopify-produkter** for å legge til varer i Shopify-produktlisten.

Ved hjelp av disse innstillingene kan du behandle prosessen med å eksportere varer:

|Felt|Description|
|------|-----------|
|**Kundeprisgruppe**|Bestemme prisen for en vare i Shopify. Salgsprisen for denne kundeprisgruppen tas. Hvis ingen gruppe angis, brukes prisen på varekortet.|
|**Kunderabattgruppe**|Bestemme rabatten som skal brukes til å beregne prisen på en vare i Shopify. Rabatterte priser lagres i **Pris**-feltet, og hele prisen er lagret i feltet **Sammenlign med pris**.|
|**Synkroniser utvidet tekst for vare**|Velg for å synkronisere den utvidede teksten for varen. Den kan inneholde HTML-kode slik den blir lagt til i *Beskrivelse*. |
|**Synkroniser vareattributter**|Velg for å synkronisere vareattributter. Attributter formateres som en tabell og inkluderes i *Beskrivelse*-feltet på Shopify.|
|**Språkkode**|Hvis dette alternativet er valgt, brukes de oversatte versjonene til tittel, attributter og utvidet tekst.|
|**SKU-tilordning**|Velg hvordan du vil fylle ut SKU-feltet i Shopify. Støttede alternativer er:<br> - **Varenr.** for å bruke varenr. for både produkter og varianter.<br> - **Varenr. + variantkode** for å opprette en SKU ved å sette sammen verdier fra to felter. For varer uten varianter brukes bare varenr.<br>- **Leverandørs varenr.** for å bruke vareleverandørnummeret som er definert på *varekortet* for både varer og varianter.<br> - **Strekkode** – bruker **varereferanse** for strekkodetypen. Dette alternativet respekterer varianter. |
|**SKU-skilletegn**|Definer et skilletegn for alternativ **Varenr. + variantkode**.|
|**Lager sporet**|Velg hvordan systemet skal fylle ut feltet **Spor lager** for produkter som er eksportert til Shopify. Du kan oppdatere tilgjengelighetsinformasjon fra [!INCLUDE[prod_short](../includes/prod_short.md)] for produkter i Shopify der spor lager er aktivert. Hvis du vil ha mer informasjon, kan du se [Lager](synchronize-items.md#sync-inventory-to-shopify).|
|**Standard lagerpolicy**|Velg *Avslå* for å unngå negativ beholdning av Shopify-siden. |
|**Kan oppdatere Shopify-produkter**|Definer hvis [!INCLUDE[prod_short](../includes/prod_short.md)] kan bare opprette varer eller kan oppdatere varer også. Velg dette alternativet hvis du planlegger å oppdatere produkter manuelt ved å bruke **Synkroniser produkt**-handling eller via jobbkø for regelmessige oppdateringer etter første synkronisering som er utløst av **Legg til vare**-handling. Husk å velge **Til Shopify** i feltet **Varesynkronisering**.|
|**Kundemalkode**|Velg standardmalen som skal brukes under prisberegningen. Hvis du vil ha mer informasjon, kan du se [salgsavgifter](setup-taxes.md).|


### <a name="fields-mapping-overview"></a>Oversikt over felttildeling

|Shopify|Kilde når den eksporteres fra [!INCLUDE[prod_short](../includes/prod_short.md)]|Mål når det importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|I henhold til **Status for opprettede produkter** på **Shopify-butikkortet**. Hvis du vil ha mer informasjon, kan du se [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products).|Ikke i bruk.|
|Tittel|**Beskrivelse**. Hvis språkkoden er definert og tilsvarende vareoversettelse eksisterer, blir vareoversettelse brukt i stedet for beskrivelse.|**Beskrivelse**|
|Description|Kombinerer utvidede tekster og attributter hvis tilsvarende veksler på Shopify-butikkortet er aktivert. Overholder språkkode.|Ikke i bruk.|
|SEO-sidetittel|Korriger verdi: tom, se [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ikke i bruk.|
|SEO-metabeskrivelse|Korriger verdi: tom, se [Ad hoc-oppdateringer av Shopify-produkter](synchronize-items.md#ad-hock-updates-of-shopify-products). |Ikke i bruk.|
|Medium|**Bilde**, se [Synkroniser varebilder](synchronize-items.md#sync-item-images) hvis du vil ha mer informasjon|**Bilde**|
|Pris|Beregningen av sluttkundepris omfatter vareprisgruppe, varerabattgruppe, valutakode og kundemalkode. |**Enhetspris**|
|Sammenlign i prisen|Beregningen av sluttkundepris uten rabatt omfatter vareprisgruppe, varerabattgruppe, valutakode og kundemalkode. |Ikke i bruk.|
|Kostnad per vare|**Enhetskost**|**Enhetskost**|
|LFE|Se **SKU-tildeling** i [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify)| Se [Hvordan SKU og strekkode definert i Shopify-produkt påvirker tildeling og oppretting av varer og varianter](synchronize-items.md#how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|Strekkode|**Varereferanser** av strekkodetype|**Varereferanser** av strekkodetype|
|Spor antall|I henhold til **lageret som er sporet** på **Shopify-butikkortet**. Hvis du vil ha mer informasjon, kan du se [Lager](synchronize-items.md#sync-inventory-to-shopify).|Ikke i bruk.|
|Fortsett å selge når tomt på lager|I henhold til **Standard lagerpolicy** på **Shopify-butikkortet**. Ikke importert.|Ikke i bruk.|
|Type|**Beskrivelse** av **Varekategorikode**. Hvis type ikke er angitt i Shopify, blir den lagt til som en egendefinert type.|**Varekategorikode**. Tildeling etter beskrivelse.|
|Leverandør|**Navn** på leverandør fra **Leverandørnr.** |**Leverandørnr.**-tildeling etter navn.|
|Vekt|**Bruttovekt**.|Ikke i bruk.|
|Avgiftspliktig|Fast verdi: aktivert.|Ikke i bruk.|
|Avgiftskoder|**Mva-gruppekode**. Bare relevant for merverdiavgift. Hvis du vil ha mer informasjon, kan du se [salgsavgifter](setup-taxes.md). |Ikke i bruk.|

### <a name="tags"></a>Koder

Gå gjennom de importerte kodene i **Koder**-faktaboksen på siden **Shopify-produkt**. Velg handlingen **Koder** på siden **Shopify-produkt** for å redigere koder.
Hvis alternativet **Til Shopify** er valgt i feltet **Synkroniser vare**, eksporteres tildelte koder til Shopify ved neste synkronisering.

## <a name="run-item-synchronization"></a>Kjør varesynkronisering

Fullstendig eller delvis synkronisering av varer kan utføres på mange forskjellige måter.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Første synkronisering av varer fra Business Central til Shopify

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Legg til varer**.
3. I feltet **Butikkode** angir du koden. Hvis du åpner vinduet **Shopify-produkt** fra vinduet **Butikkort**, fylles butikkoden ut automatisk.
4. Definer filtre for varer etter behov. Du kan for eksempel filtrere etter varenr. eller varekategorikode.
5. Velg **OK**.

De resulterende varene opprettes automatisk i Shopify med priser, men bilder og lagernivåer inkluderes ikke. Operasjonen kan ta litt tid hvis et stort antall varer legges til.

### <a name="sync-products-from-shopify-to-business-central"></a>Synkroniser produkter fra Shopify til Business Central

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser produkter**.

Du kan også bruke handlingen **Synkroniser produkter** i vinduet **Shopify-produkter** eller søk etter den satsvise jobben **Synkroniser produkter**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Hvis du vil ha mer informasjon, kan du se [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

### <a name="ad-hock-updates-of-shopify-products"></a>Ad hoc-oppdateringer av Shopify-produkter

Når postene oppdateres i tabellen **Shopify-produkt**, synkroniseres følgende endringer med Shopify.

Oppdater:

* **Status** – du kan velge mellom aktiv, arkivert eller kladd.
* **SEO-tittel**
* **SEO-beskrivelse**

Sletting:

Avhengig av verdien i **Handling for fjernede produkter** på **Shopify-butikkort**, blir produktet oppdatert i Shopify når posten slettes fra siden **Shopify-produkt**.

* **Tom** – ingenting skjer. Om nødvendig må brukeren utføre den nødvendige handlingen fra Shopify-administrator.
* **Status til utkast** – status av produkt i Shopify er satt til *utkast*.
* **Status til arkivert** – produktet arkiveres i Shopify.

## <a name="sync-item-images"></a>Synkroniser varebilder

Synkronisering av bilder kan konfigureres for synkroniserte varer. Du kan velge mellom følgende alternativer:

* **Tom** – bildesynkronisering er deaktivert.
* **Til Shopify** – bilder av varer eksporteres til Shopify
* **Fra Shopify** – bilder fra Shopify importeres til [!INCLUDE[prod_short](../includes/prod_short.md)]

Bildesynkronisering kan startes på to måter.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Synkroniser produktbilder fra vinduet Shopify-butikk

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere bilder med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser produktbilder**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Synkroniser produktbilder fra vinduet Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser produktbilder**.

### <a name="image-synchronization-remarks"></a>Bildesynkroniseringsmerknader

* Når du eksporterer bilder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, legges de nye bildene til i Shopify, noe som gjør at gamle bilder beholdes. Hvis et bilde blir oppdatert i [!INCLUDE[prod_short](../includes/prod_short.md)], må du slette gamle bilder i Shopify-administrator.
* Bilder som eksporteres til Shopify og ikke samsvarer med kravene som er definert av Shopify, importeres ikke. Hvis du vil ha mer informasjon, kan du se [Produktmedietyper på help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Synkroniser priser med Shopify

Priser kan eksporteres for synkroniserte varer på måtene som er beskrevet nedenfor.

### <a name="sync-prices-from-the-shopify-products-window"></a>Synkroniser priser fra vinduet Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser priser til Shopify**.

### <a name="price-calculation-remarks"></a>Prisberegningsmerknader

* Ved prisberegning er det viktig å ha en verdi i feltet **Standard kundemal**. Hvis du vil ha mer informasjon, kan du se [salgsavgifter](setup-taxes.md).
* Angi en **valutakode** hvis nettbutikken bruker annen valuta enn LV. Den angitte valutaen må ha valutakurser konfigurert. Hvis nettbutikken bruker samme valuta som [!INCLUDE[prod_short](../includes/prod_short.md)], lar du feltet stå tomt.
* Når du skal fastsette en pris, bruker [!INCLUDE[prod_short](../includes/prod_short.md)] laveste pris-logikk. Det betyr at hvis enhetspris som er definert på varekortet, er lavere enn det som er angitt i prisgruppen, brukes enhetsprisen fra varekortet.

## <a name="sync-inventory-to-shopify"></a>Synkroniser lager til Shopify

Lagersynkronisering kan konfigureres for allerede synkroniserte varer. Det finnes to betingelser som må oppfylles:

1. Lagersporing må være aktivert for et produkt i Shopify. Hvis varer eksporteres til Shopify, bør du vurdere å aktivere **Lager sporet** på kortet **Shopify-butikk**. Hvis du vil ha mer informasjon, kan du se [Eksporter varer til Shopify](synchronize-items.md#export-items-to-shopify).
2. Lagersynkronisering må være aktivert for **Shopify-lokasjoner**.

### <a name="to-enable-inventory-sync"></a>Slik aktiverer du lagersynkronisering

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere lager med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Lokasjoner** for å åpne **Shopify-butikklokasjoner**.
4. Velg handlingen **Hent Shopify-lokasjoner** hvis du vil importere alle lokasjonene som er definert i Shopify. Du finner dem i innstillingene [**Lokasjoner**](https://www.shopify.com/admin/settings/locations) i **Shopify-administratoren**.
5. I feltet **Lokasjonsfilter** legger du til lokasjoner, hvis du bare vil ta med lager fra bestemte lokasjoner. Du kan for eksempel skrive inn *ØST|VEST*, slik at beholdningen bare fra disse to lokasjonene er tilgjengelig for salg via nettbutikk.
6. Fjern merket for **Deaktivert** for å aktivere lagersynkronisering for valgte Shopify-lokasjoner.

Du kan starte lagersynkronisering på to måter.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Synkroniser lager fra vinduet Shopify-butikk

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere lager med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser lager**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Synkroniser lager fra vinduet Shopify-produkter

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-produkter**. Velg den relaterte koblingen.
2. Velg handlingen **Synkroniser lager**.

### <a name="inventory-remarks"></a>Lagermerknader

* Koblingen beregner **Beregnet disponibel saldo** og eksporterer den til Shopify.
* Du kan kontrollere lagerinformasjonen mottatt fra Shopify på siden **Shopify-lagerfaktaboks**. I denne faktaboksen får du en oversikt over Shopify-lageret og det siste beregnede lageret i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes en post per lokasjon.
* Hvis lagerinformasjonen i Shopify er forskjellig fra **Beregnet disponibel saldo** i [!INCLUDE[prod_short](../includes/prod_short.md)], blir lager oppdatert i Shopify.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
