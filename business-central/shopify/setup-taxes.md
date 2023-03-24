---
title: Definere avgifter for Shopify-forbindelse
description: Hvordan du definerer avgifter i Shopify og Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Definere avgifter for Shopify-forbindelse

I denne artikkelen skal vi undersøke hvordan ulike innstillinger i Shopify påvirker storefront-priser og -avgifter som vises for kunden. Vi skal også se hvordan du konfigurerer [!INCLUDE[prod_short](../includes/prod_short.md)] for å støtte innstillingene i Shopify. Denne artikkelen er ikke ment å være en omfattende avgiftsveiledning. Hvis du vil lære mer, kontakter du den lokale skattemyndigheten eller skatteansvarlig.  

Artikkelen antar at du er forpliktet til å betale skatt ved salg av varer lokalt eller internasjonalt.

## Hvis du selger hjemme

Når du har konfigurert Shopify til å samle inn avgifter i landet eller regionen innenlands, kan du bestemme hvordan du vil vise prisene på Storefront.
Du kontrollerer dette ved å aktivere eller deaktivere vekslebryteren **Alle priser inkludert avgift** i [**Avgifter**](https://www.shopify.com/admin/settings/taxes)-innstillingene i **Shopify-administratoren**.

Dette er vanlig når du skal aktivere denne funksjonen for slike land som Australia, Østerrike, Belgia, Tsjekkia, Danmark, Finland, Frankrike, Tyskland, Island, Italia, Nederland, New Zealand, Norge, Spania, Sverige, Sveits og Storbritannia. I markeder som disse inneholder for eksempel prisen *100 EUR* som er definert i produktkortet, allerede merverdiavgift (mva), og denne prisen vises for kunden på Storefront og ved betaling.  

I USA og Canada forventer kundene å se produktpriser uten skatter, som legges til ved betaling. Feltet **Alle priser inkludert avgift** er vanligvis ikke er valgt. I dette tilfellet representerer prisen *$100* som er definert i produktkortet, prisen uten mva. Ved utsjekkingstrinnet legges det til avgifter på prisen for å komme frem til den totale betalingen.

Hvis du vil ha støtte for scenariet der **Alle priser inkludert mva.** er valgt på [!INCLUDE[prod_short](../includes/prod_short.md)]-siden, fyller ut feltet **Kundemalkode** på **Shopify-butikkortet**-siden for å få tilgang til malen med følgende felter definert:  

1. **Generell firmabokføringsgrupper**, brukt for innenlandskunder.  
2. **Mva-bokføringsgruppe - firma**, brukt for innenlandskunder.  
3. **Priser inkl. mva** er angitt til *Ja*.  

Definer deretter varepriser i feltet **Varekort** eller **Salgsprislist**, med eller uten mva. Når priser eksporteres til Shopify, beregnes prisen slik at den inkluderer innenlands avgifter, viser denne prisen på produkt kortet i Shopify.

> [!NOTE]
> Hvis du konfigurerte Shopify-koblingen for å opprette kunder automatisk, kan det hende du trenger flere felt i malen, for eksempel **Bokføringsgruppe - kunde**. Hvis du bruker standardkunden for importerte ordrer, må du kontrollere at kunden har de samme feltene som er fylt ut. Du må likevel fylle ut **Kundemalkode** som angitt over, fordi feltet **Priser inkl. mva.**/**Priser inkl. mva.** i de opprettede salgsdokumentet ikke er avhengig av kunden, men av **Kundemal** fra Shopify-butikkortet eller kundemalen per land.

## Hvis du selger internasjonalt

I dette avsnittet skal vi utforske innstillinger for scenarier der du må samle inn skatter ved salg til et annet land, for eksempel andre land i EU.

**Shopify-kobling**-utvidelsen støtter for øyeblikket bare eksport av én pris. Shopify bruker automatisk lokale avgifter, valutaer og avrunding. **Alle prisene inkludert avgift** veksler resultat i i handlingene beskrevet i følgende underdeler.

### *Alle priser inkl. mva* velges

|-|Innenlandssalg|Utenlands der du samler inn mva|Utenlands der du ikke samler inn mva|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1200|1200|1200|
|Avgiftssatsprosenten|20|25|0|
|Pris ved utsjekking|1200|1200|1200|

Pris for at kunden skal holde seg intakt, uavhengig av lokasjonens posisjon, men marginen er berørt på grunn av mva-satser som er forskjellig per land.

### *Alle priser inkl. mva* velges ikke

|-|Innenlandssalg|Utenlands der du samler inn mva|Utenlands der du ikke samler inn mva|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1 000|1 000|1 000|
|Avgiftssatsprosenten|20|25|0|
|Pris ved utsjekking|1200|1250|1 000|

Shopify legger til lokal mva på toppen av prisen som er definert på produktkortet basert på hvor varene sendes til.

## Dynamisk mva-inklusiv pris

Ettersom forskjellige land har forskjellige krav, avhengig av om du inkluderer mva i den viste prisen eller ikke, kan du slå på [dynamisk mva-inklusiv pris](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) i Shopify. Dette automatiserer funksjonen for mva-inkludering.

Velg **Inkluder eller ekskluder merverdiavgiftsbasert på kundens land** i delen **Andre markeder - innstillinger** i [**Markeder**](https://www.shopify.com/admin/settings/markets)-innstillingene i **Shopify-adm**.  

> [!NOTE]
> Denne innstillingen påvirker ikke visningen av priser i innenlandske markeder, som styres av **Alle priser inkluderer avgifter**.

### *Alle priser inkl. mva* velges

|-|Innenlandssalg|Utenlandsk land der mva. er inkludert i prisen|Utenlandsk land der mva. er ekskludert|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1200|1250|1 000|
|Avgiftssatsprosenten|20|25|10|
|Pris ved utsjekking|1200|1250|1100|

Prisen for hver kunde endres avhengig av lokasjonen.

### *Alle priser inkl. mva* velges ikke

|-|Innenlandssalg|Utenlandsk land der mva. er inkludert i prisen|Utenlandsk land der mva. er ekskludert|
|------------------------|--------|--------|--------|
|Pris vist i Storefront|1 000|1250|1 000|
|Avgiftssatsprosenten|20|25|10|
|Pris ved utsjekking|1200|1250|1100|

> [!NOTE]
> **Alle priser inkludert mva** endrer ikke hvordan prisene vises for internasjonale kunder.

## Hvis du selger til EU-kunder

Forskjellige EU-land har forskjellige lokale mva-satser. Men hvis du befinner deg i EU og selger til andre EU-land, kan du bruke den lokale mva-satsen i noen tilfeller.  

Merk av for boksen **Innhent mva** i delen **EU** i innstillingene [**Avgifter**](https://www.shopify.com/admin/settings/taxes) i **Shopify-adm**.

|Innhent mva|Mva-sats|
|-|-|
|Micro-forretningsfritak|Bruk mva-sats for alt salg innenfor EU|
|Ett sentralt sted eller landsspesifikk registrering|Bruk mva-satsen for kundens land|


### Samle inn mva-registrering til registrering på ett sentralt sted

I eksemplet nedenfor er **Alle priser inkludert mva** aktivert. Prisen på produktkortet er satt til *1200*.
        
|-|Innenlandssalg|Utenlandsk|
|------------------------|--------|--------|
|Pris vist i Storefront|1200|1250|
|Avgiftssatsprosenten|20|25|
|Pris ved utsjekking|1200|1250|       
        
### Samle inn mva-sett til Micro-Business-fritak

I eksemplet nedenfor er **Alle priser inkludert mva** aktivert. Prisen på produktkortet er satt til *1200*.
        
|-|Innenlandssalg|Utenlandsk land med lokal mva-sats på 25 prosent.|
|------------------------|--------|--------|
|Pris vist i Storefront|1200|1200|
|Avgiftssatsprosenten|20|20|
|Pris ved utsjekking|1200|1200|           
    
Shopify ignorerer mva-satsen i utenlands ved beregning av endelige priser, og bruker mva-satsen innenlands.

## Importere Shopify-bestillinger solgt til internasjonale kunder

Hvis du samler inn avgifter fra flere land, må du mest sannsynlig definere en lands spesifikk innstilling i [!INCLUDE[prod_short](../includes/prod_short.md)]. Dette kreves fordi når et salgsdokument blir opprettet i [!INCLUDE[prod_short](../includes/prod_short.md)], beregner systemet mva i stedet for å bruke Shopify på nytt.

Land-/områdespesifikke innstillinger velges i **Shopify-kundemal**. Der kan du definere **Standard kundenr.** eller **Kundemalnr.**. I begge tilfeller må du kontrollere at den valgte kunden eller malen har følgende felt definert:

1. **Generell firmabokføringsgrupper** (brukt for utenlandskunder).
2. **Mva-bokføringsgruppe - firma** (brukt for utenlandskunder).
3. **Priser inkl. mva** (justeres med innstillinger på Shopify-siden):
* Velg *Ja* hvis **Alle priser inkl. mva** er aktivert og **Inkluder eller utelat mva basert på kundens land** er deaktivert.
* Velg *Nei* hvis **Alle priser inkl. mva** er deaktivert og **Inkluder eller utelat mva basert på kundens land** er deaktivert.
* Velg *Ja* hvis **Inkluder eller utelat merverdiavgift basert på kundens land** er aktivert, og landet eller regionen er oppført i [Mva-inklusive land](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Velg *Nei* hvis **Inkluder eller utelat merverdiavgift basert på kundens land** er aktivert, og landet/regionen ikke er oppført i [Mva-inklusive land](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> Innstillingen for feltet **Priser inkl. mva** kommer fra malen, ikke fra den bestemte kunden. Det er derfor det er viktig å ha definert kundemalen.

## Andre avgiftsmerknader

Når den importerte Shopify-ordren inneholder informasjon om avgifter, beregnes avgiftene på nytt når du oppretter salgsdokumentet. Omberegningen betyr at det er viktig at mva-/avgiftsinnstillingene er riktige i [!INCLUDE[prod_short](../includes/prod_short.md)].

- Flere produktavgifter eller mva-satser. Noen produktkategorier er for eksempel ansvarlig for reduserte mva-satser. Du kan bruke funksjonen for [avgiftsoverstyring](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) i Shopify. Når varer leses inn og opprettes i [!INCLUDE[prod_short](../includes/prod_short.md)], brukes mva-oppsettet som er fylt ut på varemalkoden i Shopify-butikken. Før du importerer ordrer med slike varer, må du oppdatere mva-varebokføringsgruppen.  

- Adresseavhengige mva-satser. Bruk feltet **Prioritet for avgiftsområde** sammen med tabellen **Kundemaler** til å overskrive standard logikk som fyller ut **mva-områdekoden** i salgsdokumentet. Feltet **Mva-områdekode** angir prioriteten om hvor funksjonen skal hente informasjon om land/område og delstat/provins. Deretter identifiseres tilsvarende post i Shopify-kundemalene og **mva-områdekoden**, **skyldig mva.** og **mva.-bokføringsgruppe for firma** brukes når et salgsdokument opprettes.  

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
