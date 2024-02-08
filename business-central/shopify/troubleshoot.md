---
title: Feilsøking av Shopify- og Business Central-synkronisering
description: Lær hva du gjør hvis noe går galt når du synkroniserer data mellom Shopify og Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
ms.service: dynamics-365-business-central
---

# Feilsøking av Shopify- og Business Central-synkronisering

Du kan støte på situasjoner der du må feilsøke problemer når du synkroniserer data mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne siden definerer feilsøkingstrinnene for noen vanlige scenarioer.

## Kjør oppgaver i forgrunnen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil feilsøke for å åpne siden **Shopify-butikkort**.
3. Slå av vekslebryteren **Tillat bakgrunnssynkroniseringer**.

Når synkroniseringshandlingen utløses nå, kjøres oppgaven i forgrunnen. Hvis det oppstår en feil, vises det en feildialogboks med en **Kopier detaljer**-kobling. Bruk koblingen til å kopiere informasjon til et tekstredigeringsprogram for ytterligere analyse.

## Logger

Loggingsfunksjonene kan gjøre det enklere å identifisere hvorfor det oppstod en feil. På siden **Shopify-butikkort** i feltet **Loggføringsmodus** kan du angi detaljnivået du vil registrere om feil. Feltet inneholder følgende alternativer:

- **Deaktivert** - Ikke logg informasjon om feil.
- **Bare feil**  - Logg bare feilmeldingen, uten forespørsel/svarpar. Denne innstillingen er standard for nye butikker.
- **Alle** - Logg forespørsels-/svarparene for alle transaksjoner, inkludert de som var vellykkede. Logging av alle feil kontinuerlig kan gjøre [!INCLUDE [prod_short](../includes/prod_short.md)] treg. Bruk denne modusen når datautvekslingen ikke resulterer i feil, men du ønsker å få mer innsikt om dataene som faktisk ble sendt og mottatt. Vær oppmerksom på at noen data alltid logges, uavhengig av om logging er aktivert. Hvis du vil ha mer informasjon, kan du se [Dataregistrering](#data-capture).

### Sli ser du gjennom logger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-loggposter**. Velg deretter den relaterte koblingen.
2. Velg den tilknyttede loggposten, og åpne siden **Shopify-loggpost**.
3. Gå gjennom forespørsel, statuskode og beskrivelse og svarverdier.

> [!TIP]
> Hvis du må kontakte Shopify-kundestøtte for å få hjelp med feilsøking, noterer du deg informasjonen i feltet **Forespørsels-ID** . Denne informasjonen kan bidra til å løse problemet raskere.

Du kan laste ned forespørselen og svarverdiene som filer i et tekstformat.

### Administrere loggoppføringsdata

For å holde størrelsen på databasen under kontroll, er loggoppføringer inkludert i en dataoppbevaringspolicy kalt **Loggpost for Shopify**. Med oppbevaringspolicyer kan du angi hvor lenge du vil lagre ulike typer data. Som standard beholdes Shopify-loggoppføringer i én måned. Hvis du vil finne ut mer om oppbevaringspolicyer, kan du gå til [Definer oppbevaringspolicyer](../admin-data-retention-policies.md).

Og på siden **Shopify-loggposter** kan du slette alle loggposter eller bare poster som er eldre enn sju dager.

## Dataregistrering

Uansett om logging er slått på, logges alltid noen Shopify-svar. Du kan undersøke eller laste ned loggene fra siden **Dataregistreringsliste**.

Velg handlingen **Hentede Shopify-data** på en av følgende sider:

- **Shopify-ordre**
- **Shopify-ordrelinje**
- **Shopify-oppfyllelser**
- **Shopify-ordreleveringskostnader**
- **Shopify-ordretransaksjoner**
- **Shopify-retur**
- **Shopify-returlinje**
- **Shopify-refusjon**
- **Shopify-refusjonslinje**
- **Shopify-utbetalinger**
- **Shopify-betalingstransaksjoner**
- **Shopify-transaksjoner**

## Tilbakestill synkronisering

For optimal ytelse importerer koblingen bare kunder, produkter og ordrer som ble opprettet eller endret etter siste synkronisering. På siden **Shopify-butikkort** finnes det funksjoner som endrer dato/klokkeslett for siste synkronisering, eller tilbakestille den fullstendig. Denne funksjonen sikrer at alle data synkroniseres i stedet for bare endringer siden forrige synkronisering.

Denne funksjonen gjelder bare synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan være nyttig hvis du må gjenopprette slettede data, for eksempel produkter, kunder eller slettede ordrer.

## Be om tilgangstokenet

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke vil koble til Shopify-kontoen, kan du prøve å be om tilgangstokenet fra Shopify. Du må kanskje be om et nytt token hvis det ble gjort endringer i sikkerhetsnøklene eller nødvendige tillatelser (omfang).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil hente tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen.

Veksleknappen **Has AccessKey** er slått på.

## Kontroller og aktiver tillatelser for å foreta HTTP-forespørsler i et ikke-produksjonsmiljø

Shopify-koblingsutvidelsen krever tillatelse til å utføre HTTP-forespørsler for å fungere skikkelig. Når du kjører tester i et sandkassemiljø, er HTTP-forespørslene forbudt for alle utvidelser.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utvidelsesbehandling**, og velg deretter den relaterte koblingen.
2. Velg utvidelsen **Shopify-kobling**.
3. Velg handlingen **Konfigurer** for å åpne siden **Utvidelsesinnstilling**.
4. Kontroller at vekslebryteren **Tillat HTTPClient-forespørsler** er aktivert.

## Roter Shopify-tilgangstokenet

De følgende fremgangsmåtene beskriver hvordan du roterer tilgangstokenet som brukes av Shopify-koblingen for å få tilgang til Shopify-nettbutikken.

### I Shopify

1. Fra **Shopify-administratoren** går du til [Apper](https://www.shopify.com/admin/apps).
2. Velg **Slett** i raden med **Dynamics 365 Business Central**-appen.
3. Velg **Slett** i meldingen som vises.

### I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil rotere tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvern og tillatelser, og deretter velger du knappen **Installer app**.

## Kjente problemer

### Feil: Salgshodet finnes ikke. Identifikasjonsfelter og -verdier: Dokumenttype='Quote',No.='YOUR SHOPIFY STORE'

Hvis du vil beregne priser, oppretter Shopify-koblingen et midlertidig salgsdokument (tilbud) for en midlertidig kunde (butikkode) og bruker standard prisberegningslogikk. Hvis en tredjepartsutvidelse abonnerer på hendelser i et midlertidig salgsdokument, kan det hende at toppteksten ikke er tilgjengelig. Vi anbefaler at du kontakter utvidelsesleverandøren. Be vedkommende endre koden for å se etter midlertidige poster. I noen tilfeller trenger leverandøren bare å legge til `IsTemporary`-metoden på riktig plass. Gå til [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method) for å finne ut mer om `IsTemporary`. 

Hvis du vil kontrollere om problemet er forårsaket av en tredjepartsutvidelse, bruker du koblingen **Kopier informasjon til utklippstavlen** i feilmeldingen og kopierer innholdet til tekstredigeringsprogrammet. Informasjonen inneholder en **Al-kallstakk**, der den øverste linjen er linjen der feilen oppstod. Nedenfor vises et eksempel på en AL-kallstakk.

AL-kallstakk:

```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Husk å dele AL-kallstakkinformasjonen med leverandøren av utvidelsen.

### Feil: Firmabokføringsgruppe må ha en verdi hos kunden: 'YOUR SHOPIFY STORE'. Den kan ikke være null eller tom

På siden **Shopify-butikkort** i feltet **Kundemalkode** velger du malen som har **Bokføringsgruppe – firma** fylt ut. Kundemalen brukes til å opprette kunder og beregne salgspriser for salgsdokumenter.

### Feil: Import av data til Shopify-butikk er ikke aktivert. Gå til butikkortet for å aktivere det

På siden **Shopify-butikkort** aktiverer du veksleknappen **Tillat datasynkronisering til Shopify**. Denne innstillingen bidrar til å beskytte nettbutikken fra å motta demodata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

### Feil: Oauth-feilen invalid_request: Finner ikke Shopify API-program med api_key

Det ser ut til at du bruker [Bygg inn-appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) der klientnettadressen har formatet: `https://[application name].bc.dynamics.com`. Shopify-koblingen fungerer ikke for innebygde apper. Hvis du vil finne ut mer, kan du gå til [Hvilke Microsoft-produkter er Shopify-koblingen tilgjengelig for?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Feil: intern feil. Det ser til at noe gikk galt hos oss. Forespørsels-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakt Shopify-kundestøtten innen sju dager når du får denne feilen, og oppgi forespørsels-ID-en. Hvis du vil ha mer informasjon, går du til [Kundestøttealternativer for Shopify](shopify-faq.md#shopify).

### Feil: Oauth-feil invalid_request: Kontoen din har ikke tillatelse til å gi den forespurte tilgangen for denne appen. 

Det ser ut til at brukere som ber om tilgang, ikke har rettigheter til å administrere apper (mulighet til å administrere og installere apper og kanaler samt potensielt godkjenne appgebyr). Du kan kanskje løse dette problemet ved å installere appen som kontoeier. Alternativt kan du kontrollere **apptillatelsen** for brukeren i innstillingen [**Bruker og tillatelser**](https://www.shopify.com/admin/settings/account) i **Shopify-administratoren**.  

### [{"message":"Ingen tilgang for FIELD-felt.","locations":[{"line":0,"column":0}],"path":["path"],"extensions":{"code":"ACCESS_DENIED","documentation":https://shopify.dev/api/usage/access-scopes}}]

Be om et nytt token fordi den oppdaterte versjonen av koblingen krever flere tillatelser (programomfang). Gå til [Be om tilgangstokenet](#request-the-access-token) for å finne ut mer.

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)
