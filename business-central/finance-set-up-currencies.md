---
title: Definere valutaer
description: Du må definere hver valuta hvis du kjøper eller selger i andre valutaer enn den lokale valutaen (LV) eller registrerer finanstransaksjoner i ulike valutaer.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-currencies"></a>Definere valutaer

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Bruk en ekstern tjeneste for å få de siste valutakursene i listen **Valutaer**. Hvis du vil ha mer informasjon, kan du se [Slik konfigurerer du en valutakurstjeneste](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="currencies"></a><a name="curr"></a>Valutaer

Tabellen nedenfor beskriver feltene i **Valutaer**-listen.

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Kode**|Identifikatoren for valutaen.|
|**Beskrivelse**|En fritekstbeskrivelse av valutaen.|
|**ISO-kode**|Den internasjonale koden som består av tre bokstav koden, til valutaen som er definert i ISO 4217.|
|**Numerisk ISO-kode**|Den internasjonale numeriske referansen til valutaen som er definert i ISO 4217.|
|**Valutakursdato**|Den seneste datoen for den faktiske valutakursen.|
|**ØMU-valuta**|Angir om valutaen er en ØUM-valuta (Economic and Monetary Union), for eksempel EUR.|
|**Konto for realisert agio**|Kontoen der den faktiske fortjenesten skal bokføres når du mottar betaling for salg eller registrerer den faktiske valutakursen for betalinger til leverandører. Hvis du vil ha et eksempel på en valutatransaksjon, kan du se eksemplet under denne tabellen. |
|**Konto for realisert disagio**|Kontoen der det faktiske tapet skal bokføres når du mottar betaling for salg eller registrerer den faktiske valutakursen for betalinger til leverandører. Hvis du vil ha et eksempel på en valutatransaksjon, kan du se eksemplet under denne tabellen. |
|**Konto for urealisert agio**|Kontoen der den teoretiske vinningen blir postert når du utfører en valutajustering.|
|**Konto for urealisert disagio**|Kontoen der det teoretiske tapet blir postert når du utfører en valutajustering.|
|**Avrundingspresisjon, beløp**|Noen valutaer har andre formater for fakturabeløp enn det som er definert på siden **Finansoppsett**. Hvis du endrer avrundingspresisjonen for en valuta, blir alle fakturabeløp i den valutaen avrundet med den oppdaterte presisjonen.|
|**Beløp, antall desimaler**|Noen valutaer har andre formater for fakturabeløp enn det som er definert på siden **Finansoppsett**. Hvis du endrer antall desimaler for en valuta, blir alle fakturabeløp i valutaen avrundet med de oppdaterte desimalene|
|**Fakturaavrundingstype**|Angir metoden som skal brukes hvis beløpene må avrundes. Alternativene er **Nærmest**, **Opp** og **Ned**.|
|**Avrundingspresisjon, pris**|Noen valutaer har andre formater for priser enn det som er definert på siden **Finansoppsett**. Hvis du endrer prisavrundingspresisjonen for en valuta, blir alle priser i den valutaen avrundet med den oppdaterte presisjonen.|
|**Pris, antall desimaler**|Noen valutaer har andre formater for priser enn det som er definert på siden **Finansoppsett**. Hvis du endrer antall desimaler for pris for en valuta, blir alle priser i valutaen avrundet med de oppdaterte desimalene.|
|**Avrundingspresisjon, utligning**|Angir størrelsen på intervallet som er tillatt som avrundingsdifferanse når du utligner poster i ulike valutaer med hverandre.|
|**Konvertering av LV-avrunding – debetkonto**|Angir konverteringsinformasjon som også må inneholde en debetkonto, hvis du vil sette inn korreksjonslinjer for avrundingsdifferanser i finanskladdene ved hjelp av handlingen **Sett inn konv.avrund.linjer – LV**.|
|**Konvertering av LV-avrunding – kreditkonto**|Angir konverteringsinformasjon som også må inneholde en kreditkonto, hvis du vil sette inn korreksjonslinjer for avrundingsdifferanser i finanskladdene ved hjelp av handlingen **Sett inn konv.avrund.linjer – LV**.|
|**Justert den**|Datoen for den siste valutajusteringen.|
|**Endret den**|Datoen for endringen av valutaens oppsett.|
|**Betalingstoleranse %**|Maksimum betalingstoleranseprosent som er angitt for denne valutaen. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Maks. betalingstoleransebeløp**|Maksimum betalingstoleransebeløp som er angitt for denne valutaen. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valutafaktor**|Angir forholdet mellom valutaen og den lokale valutaen som bruker den faktiske valutakursen.|
|**Kto. for real. agio - t.val.**|Angir finanskontoen som brukes til å bokføre agio for kursjusteringer mellom den lokale valutaen (LV) og tilleggsrapporteringsvalutaen. Agio beregnes når den satsvise jobben Juster valutakurser kjøres for å justere finanskonti. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Kto. for real. disagio - t.val**|Angir finanskontoen som brukes til å bokføre disagio for kursjusteringer mellom den lokale valutaen (LV) og tilleggsrapporteringsvalutaen. Agio beregnes når den satsvise jobben Juster valutakurser kjøres for å justere finanskonti. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Konto for restagio**|Angir finanskontoen som brukes til å bokføre restagiobeløp (avrundingsdifferanser) når en tilleggsrapporteringsvaluta brukes i modulen Finans. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Konto for restdisagio**|Angir finanskontoen som brukes til å bokføre restdisagiobeløp (avrundingsdifferanser) når en tilleggsrapporteringsvaluta brukes i modulen Finans. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Maks. tillatte mva-differanse**|Maksimumsbeløpet som er tillatt for mva-forskjeller i denne valutaen. Hvis du vil ha mer informasjon, kan du se [Korriger mva-beløp manuelt i salgs- og kjøpsdokumenter](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Mva-avrundingstype**|Angir avrundingsmetoden for å korrigere mva-beløp manuelt i salgs- og kjøpsdokumenter. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|

### <a name="available-currency-functions"></a>Tilgjengelige valutafunksjoner

Følgende tabell beskriver nøkkelhandlinger på siden **Valutaer**.  

|Meny|Handling|Beskrivelse|
|-------------|--------------|------------------------------|
|**Behandle**|**Foreslå konti**|Bruk konti fra andre valutaer. De mest brukte kontiene blir satt inn.|
||**Endre betalingstoleranse**|Endre én av eller både den maksimale betalingstoleransen eller betalingstoleranseprosenten og filter etter valuta. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Valutakurser**|Vis oppdaterte valutakurser for valutaene du bruker.|
||**Juster valutakurser**|Juster finans-, kunde-, leverandør- og bankkontoposter slik at de gjenspeiler en mer oppdatert saldo hvis valutakursen har endret seg siden postene ble bokført.|
||**Journal for justering av valutakurs**|Vis resultatet av å kjøre den satsvise jobben **Juster valutakurser**. Det opprettes én linje for hver valuta eller hver kombinasjon av valuta og bokføringsgruppe som er med i justeringen.|
|**Valutakurstjeneste**|**Valutakurstjenester**|Vis eller rediger oppsettet av tjenestene som er konfigurert til å hente oppdaterte valutakurser når du velger handlingen **Oppdater valutakurser**.|
||**Oppdater valutakurser**|Få de siste valutakursene fra en tjenesteleverandør.|
|**Rapporter**|**Valutaoppgjør**|Vis saldoene for alle kunder og leverandører i både utenlandsk og lokal valuta (LV). Rapporten viser to saldoer i LV. Den ene er valutaoppgjøret konvertert til LV med gjeldende kurs på transaksjonstidspunktet. Den andre er saldo for fremmed valuta omgjort til LV med gjeldende kurs på arbeidsdatoen.|

## <a name="lcy-and-other-currencies"></a>LV og andre valutaer

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## <a name="rounding-currencies"></a>Runde av valutaer

Når du skal behandle valutaer som ikke bruker desimaler, og unngå desimaler i utenlandsk valuta, kan du bruke to forskjellige avrundingsfunksjoner:

- Prisavrunding  

- Beløpsavrunding  

Disse funksjonene kan virke for seg eller sammen. I tillegg kan funksjonene virke i forbindelse med fakturaavrunding.

I motsetning til fakturaavrundingsfunksjonene påvirker beløpsavrundings- og prisavrundingsfunksjonene bare beløp i utenlandsk valuta - ikke de tilsvarende beløpene i NOK. Disse to funksjonene vil ikke føre til noen bokføringer til finanskonti. Ingen finanskontoer trenger heller ikke angis i bokføringsgrupper eller andre steder.

### <a name="unit-amount-rounding"></a>Prisavrunding

Prisavrundingsfunksjonen styrer hvordan salgspriser for varer og ressurser i utenlandske valutaer rundes av på salgs- og kjøpslinjer. Du må angi reglene for hver valuta for seg i feltet **Avrund.presisjon, pris** i **Valutaer**-listen.

Prisavrundingsfunksjonen brukes automatisk hver gang du registrerer en vare eller et ressursnummer på en salgslinje. Hvis fakturaen er for en kunde med en valutakode, regnes prisen på varen eller ressursen om til kundens valuta. Prisen rundes av i henhold til avrundingspresisjonen for valutaen.

### <a name="amount-rounding"></a>Beløpsavrunding

Beløpsavrundingsfunksjonen styrer hvordan beløp i utenlandske valutaer rundes av på finanskladdelinjer, salgslinjer og kjøpslinjer. Du må angi reglene for hver valuta for seg i feltet **Avrundingspresisjon, beløp** i **Valutaer**-listen.

Beløp i utenlandske valutaer rundes av når du fyller ut og bokfører finanskladdelinjer, salgslinjer og kjøpslinjer.

## <a name="exchange-rates"></a>Valutakurser

Du kan registrere valutakurser for hver valuta og angi hvilke datoer valutakursene gjelder fra. Du kan for eksempel registrere daglige valutakurser, månedlige valutakurser eller kvartalsmessige valutakurser for hver valuta.

Du kan beholde historiske valutakurser i **Valutakurser**-siden til referanse. Når du skal oppdatere valutakurser, kan du bruke knappen **Oppdatere valutakurser** for å få siste valutakurser fra en ekstern tjenesteleverandør.

## <a name="general-ledger-accounts"></a>Finanskontoer

Du kan ikke koble valutakoder til finanskontoer fordi beløp på finanskontoer er i NOK. Hvis du har et banklån i USD og foretar innskudd på en bankkonto i NOK, kan du holde oversikt over disse kontiene ved å definere bankkonti i USD og NOK. Med bokføringsgrupper kan du koble kontiene til de relevante finanskontiene. I finans vises verdien av beløpene i den lokale valutaen.

Du kan registrere en valutakode på en finanskladdelinje og bokføre linjen til en finanskonti. Den relevante valutakursen brukes til å regne om beløpet til NOK før det bokføres til finanskontoen.  

## <a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en kundevalutatransaksjon

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="see-also"></a>Se også

[Oppdatere valutakurser](finance-how-update-currencies.md)  
[Definere en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
