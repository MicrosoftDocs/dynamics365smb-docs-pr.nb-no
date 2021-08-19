---
title: Oppdatere valutakurser
description: Spor beløp i ulike valutaer ved hjelp av valutakoder, la Business Central hjelpe deg med å justere FX-valutakurser for bokførte poster med en ekstern service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates, FX rates
ms.date: 07/23/2021
ms.author: edupont
ms.openlocfilehash: c4072e0371499982fc86d6c16b4d614552bc4533
ms.sourcegitcommit: e904da8dc45e41cdd1434111c15e2a9d9edd3fa2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2021
ms.locfileid: "6660184"
---
# <a name="update-currency-exchange-rates"></a>Oppdatere valutakurser

Ettersom selskaper har drift i stadig flere land/regioner, blir det viktigere at de kan handle og rapportere finansinformasjon i mer enn én valuta. Den lokale valutaen (NOK) er definert på siden **Finansoppsett** som beskrevet i artikkelen [Konfigurer finans](finance-setup-finance.md). Når den lokale valutaen (NOK) er definert, vises den som en tom valuta, så når feltet **Valuta** er tomt, betyr det at valutaen er i NOK.  

Deretter må du definere valutakoder for hver valuta du bruker, hvis du kjøper eller selger i andre valutaer enn den lokale valutaen (NOK). Bankkonti kan også opprettes ved hjelp av valutaer. Det er mulig å registrere finanstransaksjoner i ulike valutaer, men finanstransaksjonen vil alltid bokføres i lokal valuta (NOK).

> [!Important]
> Du må ikke opprette den lokale valuta koden **Finansoppsett** og på siden **Valutaer**. Dette vil skape forvirring mellom den tomme valutaen og den lokale valutakoden i valutatabellen, og bankkonti, kunder eller leverandører kan opprettes ved en feiltakelse, noen med den tomme valutaen og noen med den lokale valutakoden.

Finans er definert til å bruke den lokale valutaen (NOK), men du kan definere at den skal bruke en annen valuta med en valutakurs tilordnet. Når du angir en ny valuta som en såkalt tilleggsrapporteringsvaluta, registrerer [!INCLUDE[prod_short](includes/prod_short.md)] beløp automatisk i både NOK og denne tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md). Tilleggsrapporteringsvalutaen brukes oftest til å gjøre det enklere å tilrettelegge finansrapportering til eiere som bor i land/områder som bruker andre valutaer enn den lokale valutaen (NOK).  

> [!IMPORTANT]
> Hvis du vil bruke en tilleggsrapporteringsvaluta for finansrapportering, må du kontrollere at du har forstått begrensningene. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Valutaer

> [!NOTE]  
> Hvis du ser etter sanntidsinformasjon om utenlandsk valutakurser (FX) eller historiske kurser i [!INCLUDE[prod_short](includes/prod_short.md)], finner du den referert til som valuta. I tillegg til denne artikkelen kan du også se [Definer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

Du angir valutakodene i **Valutar**, inkludert tilleggsinformasjon og innstillinger som er nødvendige for hver valutakode.

> [!TIP]
> Opprett valutaene med den internasjonale ISO-koden som kode for å forenkle arbeidet med valutaen i fremtiden.

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
|**Konvertering av NOK-avrunding – debetkonto**|Angir konverteringsinformasjon som også må inneholde en debetkonto, hvis du vil sette inn korreksjonslinjer for avrundingsdifferanser i finanskladdene ved hjelp av handlingen **Sett inn konv.avrund.linjer – NOK**.|
|**Konvertering av NOK-avrunding – kreditkonto**|Angir konverteringsinformasjon som også må inneholde en kreditkonto, hvis du vil sette inn korreksjonslinjer for avrundingsdifferanser i finanskladdene ved hjelp av handlingen **Sett inn konv.avrund.linjer – NOK**.|
|**Justert den**|Datoen for den siste valutajusteringen.|
|**Endret den**|Datoen for endringen av valutaens oppsett.|
|**Betalingstoleranse %**|Maksimum betalingstoleranseprosent som er angitt for denne valutaen. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Maks. betalingstoleransebeløp**|Maksimum betalingstoleransebeløp som er angitt for denne valutaen. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valutafaktor**|Angir forholdet mellom valutaen og den lokale valutaen som bruker den faktiske valutakursen.|
|**Kto. for real. agio - t.val.**|Angir finanskontoen som brukes til å bokføre agio for kursjusteringer mellom den lokale valutaen (NOK) og tilleggsrapporteringsvalutaen. Agio beregnes når den satsvise jobben Juster valutakurser kjøres for å justere finanskonti. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Kto. for real. disagio - t.val**|Angir finanskontoen som brukes til å bokføre disagio for kursjusteringer mellom den lokale valutaen (NOK) og tilleggsrapporteringsvalutaen. Agio beregnes når den satsvise jobben Juster valutakurser kjøres for å justere finanskonti. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Konto for restagio**|Angir finanskontoen som brukes til å bokføre restagiobeløp (avrundingsdifferanser) når en tilleggsrapporteringsvaluta brukes i modulen Finans. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Konto for restdisagio**|Angir finanskontoen som brukes til å bokføre restdisagiobeløp (avrundingsdifferanser) når en tilleggsrapporteringsvaluta brukes i modulen Finans. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Maks. tillatte mva-differanse**|Maksimumsbeløpet som er tillatt for mva-forskjeller i denne valutaen. Hvis du vil ha mer informasjon, kan du se [Korriger mva-beløp manuelt i salgs- og kjøpsdokumenter](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|
|**Mva-avrundingstype**|Angir avrundingsmetoden for å korrigere mva-beløp manuelt i salgs- og kjøpsdokumenter. Dette feltet er kanskje ikke synlig som standard. Den kan hentes ved å tilpasse siden.|

### <a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en kundevalutatransaksjon

Når du mottar en faktura fra et selskap i utenlandsk valuta, er det ganske enkelt å beregne den lokale valutaverdien (NOK) for fakturaen basert på dagens valutakurs. Fakturaen leveres imidlertid ofte med betalingsbetingelser, slik at du kan forsinke betalingen til en senere dato, som innebærer en mulig annen valutakurs. Dette problemet i kombinasjon med at valutakurser alltid avviker fra de offisielle valutakursene gjør det umulig å forutse det nøyaktige beløpet i den lokale valutaen (NOK) som kreves for å dekke fakturaen. Hvis fakturaens forfallsdato går til neste måned, må du kanskje også revaluere det lokale valutabeløpet (NOK) på slutten av måneden. Du må definere valutajusteringen fordi den nye NOK-verdien som kreves for å dekke fakturabeløpet, kan være forskjellig, og selskapets gjeld for leverandøren er muligens endret. Det nye beløpet i NOK kan være høyere eller lavere enn det forrige beløpet, og representerer derfor en gevinst eller et tap. Men siden fakturaen ikke er betalt ennå, regnes gevinst eller som *urealisert*. Senere betales fakturaen, og banken har returnert den med den faktiske valutakursen for betalingen. Det er ikke før nå *realisert* gevinst eller tap er beregnet. Urealisert gevinst eller tap tilbakeføres deretter, og faktisk gevinst eller tap bokføres i stedet.

I eksemplet nedenfor er en faktura mottatt den 1. januar med valutabeløpet på 1 000. På tidspunktet er valutakursen er 1,123.

|Dato|Handling|Valutabeløp|Dokumentsats|NOK-beløp på dokument|Justeringssats|Beløp for urealisert agio|Betalingssats|Beløp for realisert disagio|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturering**|1000|1,123|1123|||||
|1/31|**Justering**|1000||1125|1,125|2|||
|2/15|**Justeringstilbakeføring på betaling**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1,120|–3|

På slutten av måneden utføres det en valutajustering der justeringsvalutakursen er satt til 1,125, som utløser en urealisert agio på 2.

På betalingstidspunktet viser den faktiske valutakursen som er registrert på banktransaksjonen, en valutakurs på 1,120.

Her finnes en urealisert transaksjon, og derfor blir den tilbakeført sammen med betalingen.

Til slutt registreres betalingen, og det faktiske tapet blir postert til kontoen for realisert disagio.

## <a name="available-currency-functions"></a>Tilgjengelige valutafunksjoner

Følgende tabell beskriver nøkkelhandlinger på siden **Valutaer**. Noen av handlingene forklares i de neste avsnittene.  

|Meny|Handling|Beskrivelse|
|-------------|--------------|------------------------------|
|**Behandle**|**Foreslå konti**|Bruk konti fra andre valutaer. De mest brukte kontiene blir satt inn.|
||Endre betalingstoleranse|Endre én av eller både den maksimale betalingstoleransen eller betalingstoleranseprosenten og filter etter valuta. Hvis du vil ha mer informasjon, kan du se [Betalingstoleranse og toleransegrense for kontantrabatt](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Valutakurser**|Vis oppdaterte valutakurser for valutaene du bruker.|
||**Juster valutakurser**|Juster finans-, kunde-, leverandør- og bankkontoposter slik at de gjenspeiler en mer oppdatert saldo hvis valutakursen har endret seg siden postene ble bokført.|
||**Journal for justering av valutakurs**|Vis resultatet av å kjøre den satsvise jobben **Juster valutakurser**. Det opprettes én linje for hver valuta eller hver kombinasjon av valuta og bokføringsgruppe som er med i justeringen.|
|**Valutakurstjeneste**|**Valutakurstjenester**|Vis eller rediger oppsettet av tjenestene som er konfigurert til å hente oppdaterte valutakurser når du velger handlingen **Oppdater valutakurser**.|
||**Oppdater valutakurser**|Få de siste valutakursene fra en tjenesteleverandør.|
|**Rapporter**|**Valutaoppgjør**|Vis saldoene for alle kunder og leverandører i både utenlandsk og lokal valuta (NOK). Rapporten viser to saldoer i NOK. Den ene er valutaoppgjøret konvertert til NOK med gjeldende kurs på transaksjonstidspunktet. Den andre er saldo for fremmed valuta omgjort til NOK med gjeldende kurs på arbeidsdatoen.|

## <a name="exchange-rates"></a>Valutakurser

Valutakursene er verktøyet for å beregne den lokale valutaverdien (NOKk) for hver valutatransaksjon. Siden **Valutakurser** inneholder følgende felter:

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Startdato**|Datoen da valutakursen ble effektuert|  
|**Valutakode**|Valutakoden som er knyttet til denne valutakursen|  
|**Tilhørende valutakode**|Hvis denne valutaen er en del av en triangulær valutaberegning, kan den tilhørende valutakoden defineres her|  
|**Valutakurs**|Valutakursbeløpet er kursen som skal brukes for valutakoden som er valgt på linjen. Vanligvis 1 eller 100|  
|**Tilhørende valutakursbeløp**|Tilhørende valutakursbeløp er knyttet til kursen som skal brukes for den tilhørende valutakoden|  
|**Justering valutakursbeløp**|Justeringsvalutakursen er satsen som skal brukes for valutakoden som er valgt på linjen for bruk av den satsvise jobben **Juster valutakurser**|  
|**Tilhør. just. valutakursbeløp**|Den tilhørende justeringsvalutakursen er satsen som skal brukes for valutakoden som er valgt på linjen for bruk av den satsvise jobben **Juster valutakurser**|  
|**Fast valutakursbeløp**|Angir om valutakursen kan endres på fakturaer og kladdelinjer.|  

Verdiene i feltene **Valutakurs** og **Tilhørende valutakurs** brukes som standard valutakurs i alle nye samle dokumenter som opprettes fremover. Dokumentet tilordnes valutakursen i henhold til gjeldende arbeidsdato.  

> [!Note]
> Den faktiske valutakursen blir beregnet ved hjelp av denne formelen:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Justeringsvalutakursen eller den tilhørende valutakursen blir brukt til å oppdatere alle åpne bank-, kunde- eller leverandørtransaksjoner.  

> [!Note]
> Den faktiske valutakursen blir beregnet ved hjelp av denne formelen:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Justere valutakurser

Ettersom valutakursene varierer konstant, må tilleggsvalutaangivelser i systemet justeres jevnlig. Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i NOK i Finans, være villedende. I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt.

Kjørselen **Juster valutakurser** brukes til å justere valutakursene manuelt for bokførte kunde-, leverandør- og bankkontoposter. Den kan også oppdatere tilleggsrapporteringsvalutabeløp i finansposter.  

> [!TIP]
> Du kan bruke en tjeneste til å oppdatere valutakurser i systemet automatisk. Hvis du vil ha mer informasjon, kan du se [Slik konfigurerer du en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Dette justerer imidlertid ikke valutakursene i transaksjoner som allerede er bokført. Hvis du vil oppdatere valutakurser i bokførte poster, bruker du kjørselen **Juster valutakurser**.

### <a name="effect-on-customers-and-vendors"></a>Innvirkning på kunder og leverandører

For kunde- og leverandørkonti justerer kjørselen valutaen ved å bruke valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte valutabalansene og bokfører beløpene til finanskontoen angitt i feltet **Konto for urealisert agio** eller feltet **Konto for urealisert disagio** på siden **Valuta**. Motposteringer bokføres automatisk på samlekontoen i Finans.

Kjørselen behandler aller åpne kundeposter og leverandørposter. Hvis det finnes en valutadifferanse for en post, oppretter kjørselen en ny detaljert kunde- eller leverandørpost som gjenspeiler de justerte beløpene på kunde- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensjoner på kunde- og leverandørposter

Justeringspostene tilordnes dimensjonene fra kunde- eller leverandørpostene, og justeringene bokføres av dimensjonsverdiene.

### <a name="effect-on-bank-accounts"></a>Innvirkning på bankkonti

For bankkonti justerer kjørselen valutaen med valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte bankkontiene som har en valutakode, og bokfører beløpene til finanskontoen som er angitt i feltet **Kto. for realisert agio** eller feltet **Konto for realisert disagio** på siden **Valuta**. Motposter bokføres automatisk på finanskontiene som er angitt i bankbokføringsgruppene. Kjørselen beregner én post per valuta, per bokføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensjoner på bankkontoposter

Justeringspostene for bankkontoens finanskonto, og for tap/vinning-kontoen tilordnes bankkontoens standarddimensjon.

### <a name="effect-on-gl-accounts"></a>Innvirkning på finanskonti
Hvis du bokfører i en tilleggsrapporteringsvaluta, kan du få kjørselen til å opprette nye finansposter for valutajusteringer mellom NOK og tilleggsrapporteringsvalutaen. Kjørselen beregner forskjellene for hver finanspost og justerer finansposten i henhold til innholdet i feltet **Valutakursjustering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensjoner på finanskontoposter
Justeringspostene tilordnes standarddimensjonene fra kontiene de bokføres på.

> [!Important]
> Før du kan bruke kjørselen, må du angi justeringskursene som brukes til å justere valutasaldoen. Du gjør dette på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Slik konfigurerer du en valutakurstjeneste
Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert, for eksempel FloatRates.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenester for valutakurs**, og velg deretter den tilknyttede koblingen.
2. Velg handlingen **Ny**.
3. På siden **Valutakurstjeneste** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktiver alternativet **Aktivert** for å aktivere tjenesten.

> [!NOTE]
> Den følgende videoen viser et eksempel på hvordan du kan koble til en valutakurstjeneste ved hjelp av Den europeiske sentralbank som eksempel. I segmentet som beskriver hvordan du definerer felttilordninger, returnerer innstillingen i kolonnen **Kilde** for den **overordnede noden for valutakode** bare den første valutaen som blir funnet. Innstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Oppdatere valutakurser via en tjeneste
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Valutaer** og velg den relaterte koblingen.
2. Velg **Oppdater valutakurser**.

Verdien i **Valutakurs**-feltet på **Valutaer**-siden oppdateres med den nyeste valutakursen.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Definere en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
