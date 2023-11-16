---
title: Definere avgifter for Shopify-forbindelse
description: Hvordan du definerer avgifter i Shopify og Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="set-up-taxes-for-the-shopify-connection"></a>Definere avgifter for Shopify-forbindelse

I denne artikkelen skal vi undersøke hvordan ulike innstillinger i Shopify påvirker butikkpriser og avgifter som vises for kunder. Vi skal også dekke hvordan du konfigurerer [!INCLUDE[prod_short](../includes/prod_short.md)] for å støtte innstillingene i Shopify. Denne artikkelen er ikke ment å være en omfattende avgiftsveiledning. Hvis du vil lære mer, kontakter du den lokale skattemyndigheten eller skatteansvarlig.  

Artikkelen antar at du er forpliktet til å betale skatt ved salg av varer lokalt eller internasjonalt.

## <a name="if-you-sell-domestically"></a>Hvis du selger hjemme

Etter at du har konfigurert Shopify til å samle inn avgifter i landet eller regionen innenlands, kan du bestemme hvordan du vil vise prisene i butikken.

Du angir om du skal ta med mva. i priser ved å slå av eller på bryteren **Alle prisene inkluderer mva.** i [**Avgifter**](https://www.shopify.com/admin/settings/taxes)-innstillinger i **Shopify-administratoren**.

Vekslebryteren er vanligvis aktivert for følgende land/områder:

* Australia
* Østerrike
* Belgia
* Den tsjekkiske republikk
* Danmark
* Finland
* Frankrike
* Tyskland
* Island
* Italia
* Nederland
* New Zealand
* Norge
* Spania
* Sverige
* Sveits
* Storbritannia. 

I markeder som dette, inneholder for eksempel en pris på 100 EUR som er definert på produktkortet, allerede merverdiavgift (mva.). Prisen, inkludert mva., vises for kunden i butikken og ved betaling.  

I USA og Canada forventer ikke kundene at prisene er inkludert mva. Mva. legges til ved betaling, så vekslebryteren **Alle priser inkluderer mva.** er vanligvis slått av. I dette tilfellet representerer prisen $ 100 som er definert på produktkortet, prisen uten mva. Ved betaling blir avgifter lagt til prisen.

Hvis du vil ha støtte for scenarioet der **Alle priser inkluderer mva.** er valgt, fyller du ut følgende felter på siden **Shopify-butikkort** i [!INCLUDE[prod_short](../includes/prod_short.md)]:  

1. Slå på vekslebryteren **Priser inkludert mva.**.  
2. Angi bokføringsgruppen du bruker for innenlandske kunder, i feltet **Mva-firmabokføringsgruppe**.  

Definer deretter varepriser i feltene **Varekort** eller **Salgsprislist**, med eller uten mva. Når priser eksporteres til Shopify, inkluderer [!INCLUDE [prod_short](../includes/prod_short.md)] innenlands avgifter i den beregnede prisen og viser prisen for produktet i Shopify.

[!Note]
> Disse innstillingene påvirker eksporten av priser. Når du importerer ordrer fra Shopify, kommer innstillingen for feltet **Priser inkl. mva.** fra **kundemalen** på Shopify-butikkortet eller kundemalen per land/område. Selv om du bruker standardkunden for importerte ordrer, må du fylle ut **kundemalkoden**.

## <a name="if-you-sell-internationally"></a>Hvis du selger internasjonalt

Denne delen utforsker innstillinger for scenarioer der du må samle inn skatter ved salg til et annet land/område, for eksempel andre land/områder i EU.

Shopify-koblingen lar deg for øyeblikket bare eksportere én pris. Shopify bruker automatisk lokale avgifter, valutaer og avrunding. **Alle prisene inkludert avgift** veksler resultat i i handlingene beskrevet i følgende underdeler.

### <a name="all-prices-include-tax-is-selected"></a>Alle priser inkl. mva velges

|-|Innenlandssalg|Utenlandsk land/område der du samler inn mva|Utenlandsk land/område der du ikke samler inn mva|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1200|1200|1200|
|Avgiftssatsprosenten|20|25|0|
|Pris ved utsjekking|1200|1200|1200|

Prisen for at kunden skal holde seg intakt, uavhengig av lokasjonens posisjon, men marginen er berørt på grunn av mva-satser som er forskjellig per land/område.

### <a name="all-prices-include-tax-is-not-selected"></a>Alle priser inkl. mva velges ikke

|-|Innenlandssalg|Utenlands der du samler inn mva|Utenlands der du ikke samler inn mva|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1 000|1 000|1 000|
|Avgiftssatsprosenten|20|25|0|
|Pris ved utsjekking|1200|1250|1 000|

Shopify legger til lokale avgifter i prisen som er definert på produktkortet basert på hvor varene sendes til.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynamisk mva-inklusiv pris

Land/områder har forskjellige behov for å inkludere mva. i priser. Hvis du vil at prisene skal inkludere mva. automatisk, kan du aktivere [Dynamisk mva-inklusiv pris](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) i Shopify.

I **Shopify-administratoren** velger du **Inkluder eller ekskluder merverdiavgiftsbasert på kundens land** i delen **Andre markeder - innstillinger** i [**Markeder**](https://www.shopify.com/admin/settings/markets)-innstillingene.  

> [!NOTE]
> Denne innstillingen påvirker priser i innenlandske markeder, som styres av **Alle priser inkluderer avgifter**.

### <a name="all-prices-include-tax-is-selected-1"></a>Alle priser inkl. mva velges

|-|Innenlandssalg|Utenlandsk land/område der mva. er inkludert i prisen|Utenlandsk land/område der mva. er ekskludert|
|------------------------|---------------|---------------|--------|
|Pris vist i Storefront|1200|1250|1 000|
|Avgiftssatsprosenten|20|25|10|
|Pris ved utsjekking|1200|1250|1100|

Prisen for hver kunde endres avhengig av lokasjonen.

### <a name="all-prices-include-tax-is-not-selected-1"></a>Alle priser inkl. mva velges ikke

|-|Innenlandssalg|Utenlandsk land/område der mva. er inkludert i prisen|Utenlandsk land/område der mva. er ekskludert|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1 000|1250|1 000|
|Avgiftssatsprosenten|20|25|10|
|Pris ved utsjekking|1200|1250|1100|

> [!NOTE]
> **Alle priser inkludert mva.** endrer ikke hvordan prisene vises for internasjonale kunder.

## <a name="if-you-sell-to-eu-customers"></a>Hvis du selger til EU-kunder

Forskjellige EU-land/-områder har forskjellige lokale mva-satser. Men hvis du befinner deg i EU og selger til andre EU-land/-områder, kan du bruke den lokale mva-satsen i noen tilfeller.  

I **Shopify-administratoren** merker du av boksen **Innhent mva.** i delen **EU** i innstillingene [**Avgifter**](https://www.shopify.com/admin/settings/taxes).

|Innhent mva|Mva-sats|
|-|-|
|Micro-forretningsfritak|Bruk mva-sats for alt salg innenfor EU|
|Ett sentralt sted eller lands-/områdespesifikk registrering|Bruk mva-satsen for kundens land/område|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Samle inn mva-registrering til registrering på ett sentralt sted

I eksemplet nedenfor er **Alle priser inkludert mva** slått på. Prisen på produktkortet er satt til *1200*.

|-|Innenlandssalg|Utenlandsk land/område|
|------------------------|--------|--------|
|Pris vist i Storefront|1200|1250|
|Avgiftssatsprosenten|20|25|
|Pris ved utsjekking|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption"></a>Samle inn mva-sett til Micro-Business-fritak

I eksemplet nedenfor er **Alle priser inkludert mva** slått på. Prisen på produktkortet er satt til *1200*.

|-|Innenlandssalg|Utenlandsk land/område med lokal mva-sats på 25 prosent.|
|------------------------|--------|--------|
|Pris vist i Storefront|1200|1200|
|Avgiftssatsprosenten|20|20|
|Pris ved utsjekking|1200|1200|

Shopify bruker innenlands avgiftssats og ignorerer avgiftssatsen i utenlandsk land/område når den beregner endelige priser.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Importere Shopify-bestillinger solgt til internasjonale kunder

Hvis du samler inn avgifter fra flere land/områder, må du definere en lands/områdes spesifikk innstilling i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det er en grunn til at denne innstillingen ikke er nødvendig. Når en ordre opprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], beregner [!INCLUDE [prod_short](../includes/prod_short.md)] avgifter i stedet for å bruke avgiftene importer fra Shopify på nytt.

Du angir land-/områdespesifikke innstillinger på siden **Shopify-kundemal**. Du kan definere **Standard kundenr.** eller **Kundemalnr.**. I begge tilfeller må du kontrollere at den valgte kunden eller malen har følgende felt fylt ut:

1. **Generell firmabokføringsgrupper** (brukt for utenlandskunder).
2. **Mva-bokføringsgruppe - firma** (brukt for utenlandskunder).
3. **Priser inkl. mva** (justeres med innstillinger på Shopify-siden):

* Velg **Ja** hvis **Alle priser inkl. mva** er aktivert og **Inkluder eller utelat mva basert på kundens land** er deaktivert.
* Velg **Nei** hvis **Alle priser inkl. mva** er deaktivert og **Inkluder eller utelat mva basert på kundens land** er deaktivert.
* Velg **Ja** hvis **Inkluder eller utelat merverdiavgift basert på kundens land** er aktivert, og landet eller regionen er oppført i [Mva-inklusive land/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Velg **Nei** hvis **Inkluder eller utelat merverdiavgift basert på kundens land** er aktivert, og landet/området ikke er oppført i [Mva-inklusive land/områder](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> Innstillingen for feltet **Priser inkl. mva** kommer fra malen, ikke fra den bestemte kunden. Det er viktig å definere kundemalen.

## <a name="other-tax-remarks"></a>Andre avgiftsmerknader

Når den importerte Shopify-ordren inneholder informasjon om avgifter, beregnes avgiftene på nytt når du oppretter salgsdokumentet. Omberegningen betyr at det er viktig at mva-/avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)].

* Flere produktavgifter eller mva-satser. Noen produktkategorier er for eksempel ansvarlig for reduserte mva-satser. Du kan bruke funksjonen for [avgiftsoverstyring](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) i Shopify. Når du importerer og oppretter varer i [!INCLUDE[prod_short](../includes/prod_short.md)], brukes mva-oppsettet angitt på varemalkoden i Shopify-butikken. Før du importerer ordrer med slike varer, må du oppdatere mva-varebokføringsgruppen.  
* Adresseavhengige mva-satser. Bruk feltet **Prioritet for avgiftsområde** sammen med tabellen **Kundemaler** til å overskrive standard logikk som fyller ut **mva-områdekoden** i salgsdokumentet. Feltet **Mva-områdekode** angir prioriteten om hvor funksjonen skal hente informasjon om land/område og delstat/provins. Deretter identifiseres tilsvarende post i Shopify-kundemalene og **mva-områdekoden**, **skyldig mva.** og **mva.-bokføringsgruppe for firma** brukes når et salgsdokument opprettes.  

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
