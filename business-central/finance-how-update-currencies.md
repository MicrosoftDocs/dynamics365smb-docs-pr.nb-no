---
title: Oppdatere valutakurser (inneholder video)
description: 'Hvis du sporer beløp i ulike valutaer, kan du la Business Central hjelpe deg med å justere FX-valutakurser for bokførte poster med en ekstern service.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a>Oppdatere valutakurser

Du kan definere forskjellige valutaer i [!INCLUDE [prod_short](includes/prod_short.md)], for eksempel hvis du handler i andre valutaer enn din lokale valuta. Hvis du vil hjelpe deg med å holde oversikt over endringer i valutakurser, kan du håndtere valutaene manuelt, eller du kan definere en valutakurstjeneste.

## <a name="currencies"></a><a name="currencies"></a><a name="currencies"></a>Valutaer

> [!TIP]  
> Hvis du ser etter sanntidsinformasjon om utenlandsk valutakurser (FX) eller historiske kurser i [!INCLUDE[prod_short](includes/prod_short.md)], finner du den referert til som valuta. I tillegg til denne artikkelen kan du også se [Definer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du angir valutakodene i **Valutaer**-listen, inkludert tilleggsinformasjon og innstillinger som er nødvendige for hver valutakode. Hvis du vil ha mer informasjon, kan du se [Valutaer](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en kundevalutatransaksjon

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a><a name="exchange-rates"></a><a name="exchange-rates"></a>Valutakurser

Valutakursene er verktøyet for å beregne den lokale valutaverdien (LV) for hver valutatransaksjon. Siden **Valutakurser** inneholder følgende felter:

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

## <a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a>Justere valutakurser

Ettersom valutakursene varierer konstant, må tilleggsvalutaangivelser i systemet justeres jevnlig. Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i NOK i Finans, være villedende. I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt.

Kjørselen **Juster valutakurser** brukes til å justere valutakursene manuelt for bokførte kunde-, leverandør- og bankkontoposter. Den kan også oppdatere tilleggsrapporteringsvalutabeløp i finansposter.  

> [!TIP]
> Du kan bruke en tjeneste til å oppdatere valutakurser i systemet automatisk. Hvis du vil ha mer informasjon, kan du se [Slik konfigurerer du en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Dette justerer imidlertid ikke valutakursene i transaksjoner som allerede er bokført. Hvis du vil oppdatere valutakurser i bokførte poster, bruker du kjørselen **Juster valutakurser**.

Du kan forhåndsvise effekten som en justering vil ha ved bokføring, før du faktisk bokfører ved å velge **Forhåndsvis** på siden **Juster valutakurser**. I tillegg kan du velge om finansbokføringen skal være detaljert (per post) eller summert (per valuta) ved å velge **Summer poster**. Du kan også angi hvordan du vil håndtere dimensjoner for urealiserte tap- og gevinstbokføringer ved å velge ett av følgende alternativer i feltet **Overfør dimensjonsverdier**:  

- **Kildepost**: Finansposter for urealisert agio og disagio vil få dimensjonsverdier overført fra den justerte posten.
- **Etter finanskonto**: Finansposter for urealisert agio og disagio vil ha dimensjonsverdier overført fra postens kildeinnstilling for finanskontoens urealisert agio og disagio.
- **Ingen overføring**: Finansposter for urealisert agio og disagio har ikke dimensjonsverdier.

### <a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a>Innvirkning på kunder og leverandører

For kunde- og leverandørkonti justerer kjørselen valutaen ved å bruke valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte valutabalansene og bokfører beløpene til finanskontoen angitt i feltet **Konto for urealisert agio** eller feltet **Konto for urealisert disagio** på siden **Valuta**. Motposteringer bokføres automatisk på samlekontoen i Finans.

Kjørselen behandler aller åpne kundeposter og leverandørposter. Hvis det finnes en valutadifferanse for en post, oppretter kjørselen en ny detaljert kunde- eller leverandørpost som gjenspeiler de justerte beløpene på kunde- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensjoner på kunde- og leverandørposter

Justeringspostene tilordnes dimensjonene fra kunde- eller leverandørpostene, og justeringene bokføres av dimensjonsverdiene.

### <a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a>Innvirkning på bankkonti

For bankkonti justerer kjørselen valutaen med valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte bankkontiene som har en valutakode, og bokfører beløpene til finanskontoen som er angitt i feltet **Kto. for realisert agio** eller feltet **Konto for realisert disagio** på siden **Valuta**. Motposter bokføres automatisk på finanskontiene som er angitt i bankbokføringsgruppene. Kjørselen beregner én post per valuta, per bokføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a>Dimensjoner på bankkontoposter

Justeringspostene for bankkontoens finanskonto, og for tap/vinning-kontoen tilordnes bankkontoens standarddimensjon.

### <a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a>Innvirkning på finanskonti
Hvis du bokfører i en tilleggsrapporteringsvaluta, kan du få kjørselen til å opprette nye finansposter for valutajusteringer mellom LV og tilleggsrapporteringsvalutaen. Kjørselen beregner forskjellene for hver finanspost og justerer finansposten i henhold til innholdet i feltet **Valutakursjustering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a>Dimensjoner på finanskontoposter
Justeringspostene tilordnes standarddimensjonene fra kontiene de bokføres på.

> [!Important]
> Før du kan bruke kjørselen, må du angi justeringskursene som brukes til å justere valutasaldoen. Du gjør dette på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a>Slik konfigurerer du en valutakurstjeneste
Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert, for eksempel FloatRates. 

> [!NOTE]
> De fleste valutakurstjenester tilbyr data som er kompatible med importprosessen i [!INCLUDE[prod_short](includes/prod_short.md)]. Noen ganger er imidlertid dataene formatert på en annen måte, og du må tilpasse importprosessen. Du kan bruke datautvekslingsrammeverket til å gjøre dette ved å legge til en egen codeunit. Du trenger sannsynligvis litt hjelp fra en utvikler for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenester for valutakurs**, og velg deretter den tilknyttede koblingen.
2. Velg handlingen **Ny**.
3. På siden **Valutakurstjeneste** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktiver alternativet **Aktivert** for å aktivere tjenesten.

> [!NOTE]
> Den følgende videoen viser et eksempel på hvordan du kan koble til en valutakurstjeneste ved hjelp av Den europeiske sentralbank som eksempel. I segmentet som beskriver hvordan du definerer felttilordninger, returnerer innstillingen i kolonnen **Kilde** for den **overordnede noden for valutakode** bare den første valutaen som blir funnet. Innstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a>Oppdatere valutakurser via en tjeneste
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Valutaer** og velg den relaterte koblingen.
2. Velg **Oppdater valutakurser**.

Verdien i **Valutakurs**-feltet på **Valutaer**-siden oppdateres med den nyeste valutakursen.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Valutaer i Business Central](finance-currencies.md)  
[Definer valutaer](finance-set-up-currencies.md)  
[Definer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
