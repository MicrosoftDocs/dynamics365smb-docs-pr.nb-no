---
title: Oppdater valutakurser
description: Finn ut hvordan du bruker Business Central til å justere valutakurser for beløp i ulike valutaer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="update-currency-exchange-rates"></a>Oppdater valutakurser

Hvis du handler i forskjellige valutaer, må du holde styr på endringene i valutakursene. [!INCLUDE [prod_short](includes/prod_short.md)] hjelper deg må administrere og oppdatere valutakursene manuelt eller automatisk og sette opp en valutakurstjeneste.

## <a name="currencies"></a>Valutaer

> [!TIP]  
> I [!INCLUDE[prod_short](includes/prod_short.md)] finner du sanntidsinformasjon om utenlandsk valutakurser (FX) eller historiske kurser under begrepet valuta. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du kan angi valutakodene i **Valutaer**-listen, inkludert tilleggsinformasjon og innstillinger som er nødvendige for hver valutakode. Hvis du vil ha mer informasjon, kan du se [Valutaer](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en kundevalutatransaksjon

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Valutakurser

Valutakursene er verktøyet for å beregne den lokale valutaverdien (LV) for hver valutatransaksjon. Siden **Valutakurser** inneholder følgende felter:

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Startdato**|Datoen da valutakursen var gyldig.|  
|**Valutakode**|Valutakoden som er knyttet til denne valutakursen.|  
|**Tilhørende valutakode**|Hvis denne valutaen er en del av en triangulær valutaberegning, kan du konfigurere den tilhørende valutakoden her.|  
|**Valutakurs**|Valutakursbeløpet er kursen for valutakoden som er valgt på linjen. Vanligvis 1 eller 100.|  
|**Tilhørende valutakursbeløp**|Tilhørende valutakursbeløp er knyttet til kursen som skal brukes for den tilhørende valutakoden.|  
|**Justering valutakursbeløp**|Satsen for valutakoden som er valgt på linjen, for bruk av kjørselen **Juster valutakurser**.|  
|**Tilhør. just. valutakursbeløp**|Satsen for valutakoden som er valgt på linjen, for bruk av kjørselen **Juster valutakurser**.|  
|**Fast valutakursbeløp**|Angir om valutakursen kan endres på fakturaer og kladdelinjer.|  

Verdiene i feltene **Valutakurs** og **Tilhørende valutakurs** brukes som standard valutakurs i alle nye samle dokumenter som opprettes fremover. Dokumentet tilordnes valutakursen i henhold til gjeldende arbeidsdato.  

> [!Note]
> Den faktiske valutakursen beregnes ved hjelp av denne formelen:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Justeringsvalutakursen eller den tilhørende valutakursen oppdaterer alle åpne bank-, kunde- eller leverandørtransaksjoner.  

> [!Note]
> Den faktiske valutakursen beregnes ved hjelp av denne formelen:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjust-exchange-rates"></a>Juster valutakurser

Ettersom valutakursene varierer konstant, må du justere andre valutaangivelser jevnlig. Hvis du ikke gjør det, kan beløp du konverterte fra utenlandske (eller andre) valutaer og bokførte i finans i lokal valuta, være feil. Du må også oppdatere daglige poster som bokføres, før du angir en daglig valutakurs.

Du kan bruke kjørselen **Juster valutakurser** til å justere valutakursene manuelt for bokførte kunde-, leverandør- og bankkontoposter. Kjørselen kan også oppdatere andre rapporteringsvalutabeløp i finansposter.  

> [!TIP]
> Du kan bruke en tjeneste til å oppdatere valutakurser i systemet automatisk. Hvis du vil ha mer informasjon, kan du se [Slik konfigurerer du en valutakurstjeneste](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Dette justerer imidlertid ikke valutakursene i transaksjoner som allerede er bokført. Hvis du vil oppdatere valutakurser i bokførte poster, bruker du kjørselen **Juster valutakurser**.

Du kan også angi hvordan justeringen håndterer dimensjoner for urealiserte tap- og gevinstbokføringer ved å velge ett av følgende alternativer i feltet **Dimensjonsbokføring**:  

* **Kildepostdimensjoner**: Overfør dimensjonsverdier for finans for urealisert agio og disagio fra oppføringen du justerer.  
* **Ingen dimensjoner**: Ikke overfør dimensjonsverdier for urealisert agio og disagio til finansposter. [!INCLUDE [prod_short](includes/prod_short.md)] bruker fortsatt standarddimensjonsinnstillinger, for eksempel **Obligatorisk kode**, **Samme kode** eller **Ingen kode**. Hvis kildetransaksjonspostene har dimensjonsverdier, oppretter justeringen poster uten dimensjonsverdier.  
* **Finanskontodimensjoner**: Overfør dimensjonsverdier fra postens kildeinnstilling for finanskontoens urealisert agio og disagio til finansposter.

> [!NOTE]
> Hvis du vil bruke forhåndsvisningsfunksjonen, må du aktivere **Funksjonsoppdatering: Aktivere bruk av ny utvidbar valutakursjustering, inkludert bokføringsforhåndsvisning** på **[Funksjonsbehandling](https://businesscentral.dynamics.com/?page=2610)**-siden.

> [!IMPORTANT]
> På grunn av lokale krav i Sveits anbefaler vi ikke at du aktiverer **Funksjonsoppdatering: Aktiver bruk av ny utvidbar justering av valutakurser, deriblant bokføringsforhåndsvisning** i den sveitsiske (CH)-landsversjonen.

## <a name="preview-the-effect-of-an-adjustment"></a>Forhåndsvise effekten av en justering

Du kan forhåndsvise effekten som en valutakursjustering har ved bokføring, før du faktisk bokfører, ved å velge handlingen **Forhåndsvis bokføring** på forespørselssiden for rapporten **Valutakursjustering** (Rapport 596). På forespørselssiden kan du angi hva som skal inkluderes i forhåndsvisningen:

* Få en detaljert bokføring til finans etter oppføring.
* Få et sammendrag av bokføring etter valuta. Bare velg feltet **Juster per post** i rapporten **Valutakursjustering**.

### <a name="effect-on-customers-and-vendors"></a>Innvirkning på kunder og leverandører

For kunde- og leverandørkonti bruker den satsvise jobben valutakursen som gjelder på bokføringsdatoen som er angitt for kjørselen til å justere valutaen. Kjørselen beregner differansene for de enkelte valutabalansene og bokfører beløpene til finanskontoen angitt i feltet **Konto for urealisert agio** eller feltet **Konto for urealisert disagio** på siden **Valuta**. Motposteringer bokføres automatisk på samlekontoen i Finans.

Kjørselen behandler aller åpne kundeposter og leverandørposter. Hvis det finnes en valutadifferanse for en post, oppretter kjørselen en ny detaljert kunde- eller leverandørpost. Den nye posten gjenspeiler det justerte beløpet i kunde- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensjoner på kunde- og leverandørposter

[!INCLUDE [prod_short](includes/prod_short.md)] tilordner dimensjonene fra kunde- eller leverandørpostene, til justeringspostene og bokfører justeringene for hver kombinasjon av dimensjonsverdiene.

### <a name="effect-on-bank-accounts"></a>Innvirkning på bankkonti

For bankkonti justerer kjørselen valutaen med valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte bankkontiene som har en valutakode, og bokfører beløpene til finanskontoen som er angitt i feltet **Kto. for realisert agio** eller feltet **Konto for realisert disagio** på siden **Valuta**. Motposter bokføres automatisk på finanskontiene som er angitt i bankbokføringsgruppene. Kjørselen beregner én post per valuta, per bokføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensjoner på bankkontoposter

Justeringspostene for bankkontoens finanskonto og tap/vinning-kontoen tildeles bankkontoens standarddimensjon.

### <a name="effect-on-gl-accounts"></a>Innvirkning på finanskonti

Hvis du bokfører i en annen rapporteringsvaluta, kan du få kjørselen til å opprette nye finansposter for valutajusteringer mellom lokal valuta og den andre rapporteringsvalutaen. Kjørselen beregner forskjellene for hver finanspost. Den justerer finansposten i henhold til innholdet i feltet **Valutakursjustering** for hver finanskonto.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensjoner på finanskontoposter

Justeringspostene tilordnes standarddimensjonene fra kontiene de bokføres på.

> [!Important]
> Før du kan bruke kjørselen, må du angi justeringskursene som brukes til å justere valutasaldoen. Du gjør dette på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="set-up-a-currency-exchange-rate-service"></a>Konfigurer en valutakurstjeneste

Du kan bruke en ekstern tjeneste til å holde valutakursene oppdatert.

> [!NOTE]
> De fleste valutakurstjenester tilbyr data som er kompatible med importprosessen i [!INCLUDE[prod_short](includes/prod_short.md)]. Noen ganger er imidlertid dataene formatert på en annen måte, og du må tilpasse importprosessen. Du kan bruke datautvekslingsrammeverket til å gjøre dette ved å legge til en egen codeunit. Du trenger sannsynligvis litt hjelp fra en utvikler for å gjøre dette. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tjenester for valutakurs**, og velg deretter den tilknyttede koblingen.
2. Velg handlingen **Opprett**.
3. På siden **Valutakurstjeneste** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Tilordne feltene fra XML-filen til tabellen for valutakurser i kildefeltet.
5. Bruk eventuelle nødvendige transformasjonsregler.
6. Aktiver alternativet **Aktivert** for å aktivere tjenesten.

> [!NOTE]
> Den følgende videoen viser hvordan du kan koble til en valutakurstjeneste ved hjelp av Den europeiske sentralbank som eksempel. I segmentet som beskriver hvordan du definerer felttilordninger, returnerer innstillingen i kolonnen **Kilde** for den **overordnede noden for valutakode** bare den første valutaen som blir funnet. Innstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="update-currency-exchange-rates-through-a-service"></a>Oppdater valutakurser via en tjeneste

Følg fremgangsmåten gitt for å oppdatere valutakursene gjennom en tjeneste:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Valutaer** og velg den relaterte koblingen.
2. Velg handlingen **Oppdater valutakurser**.

## <a name="correct-mistakes"></a>Korriger feil

Nå og da må du kanskje korrigere en feil i en betalingstransaksjon som er knyttet til justeringer av fortjeneste og tap i utenlandsk valuta. Du kan bruke handlingen **Tilbakefør transaksjon** på sidene **Bankposter**, **Kundeposter** og **Leverandørposter** til å oppheve og tilbakeføre betalingstransaksjonen.

> [!NOTE]
> Når du opphever utligningen og tilbakefører en betaling for en post som hadde valutakursjusteringer tilknyttet, bokfører tilbakeføringspostene for justeringene. Du må kanskje kjøre justeringen av valutakursen på nytt for å få riktig nåværende saldo.

## <a name="see-also"></a>Se også

[Valutaer i Business Central](finance-currencies.md)  
[Definer valutaer](finance-set-up-currencies.md)  
[Konfigurer en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
