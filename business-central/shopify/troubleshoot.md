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
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Feilsøking av Shopify- og Business Central-synkronisering

Du kan støte på situasjoner der du må feilsøke problemer når du synkroniserer data mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne siden definerer feilsøkingstrinnene for noen vanlige scenarioer.

## <a name="run-tasks-in-the-foreground"></a>Kjør oppgaver i forgrunnen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil feilsøke for å åpne siden **Shopify-butikkort**.
3. Slå av vekslebryteren **Tillat bakgrunnssynkroniseringer**.

Når synkroniseringshandlingen utløses nå, kjøres oppgaven i forgrunnen. Hvis det oppstår en feil, vises det en feildialogboks med en **Kopier detaljer**-kobling. Bruk koblingen til å kopiere informasjon til et tekstredigeringsprogram for ytterligere analyse.

## <a name="logs"></a>Logger

Loggingsfunksjonene kan gjøre det enklere å identifisere hvorfor det oppstod en feil. På siden **Shopify-butikkort** i feltet **Loggføringsmodus** kan du angi detaljnivået du vil registrere om feil. Feltet inneholder følgende alternativer:

- **Deaktivert** - Ikke logg informasjon om feil.
- **Bare feil**  - Logg bare feilmeldingen, uten forespørsel/svarpar. Denne innstillingen er standard for nye butikker.
- **Alle** - Logg forespørsels-/svarparene for alle transaksjoner, inkludert de som var vellykkede.

> [!NOTE]
> Logging av feil kontinuerlig kan senke [!INCLUDE [prod_short](../includes/prod_short.md)]. For å unngå dette kan du aktivere logging etter at du har funnet en feil i synkroniseringen. Du kan utløse synkroniseringen manuelt på nytt og deretter se gjennom loggen for å finne ut hva som gikk galt.

### <a name="manage-log-entry-data"></a>Administrere loggoppføringsdata

For å holde størrelsen på databasen under kontroll, er loggoppføringer inkludert i en dataoppbevaringspolicy kalt **Loggpost for Shopify**. Med oppbevaringspolicyer kan du angi hvor lenge du vil lagre ulike typer data. Som standard beholdes Shopify-loggoppføringer i én måned. Hvis du vil finne ut mer om oppbevaringspolicyer, kan du gå til [Definer oppbevaringspolicyer](../admin-data-retention-policies.md).

Og på siden **Shopify-loggposter** kan du slette alle loggposter eller bare poster som er eldre enn sju dager.

### <a name="to-review-logs"></a>Sli ser du gjennom logger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-loggposter**. Velg deretter den relaterte koblingen.
2. Velg den tilknyttede loggposten, og åpne siden **Shopify-loggpost**.
3. Gå gjennom forespørsel, statuskode og beskrivelse og svarverdier.

> [!TIP]
> Hvis du må kontakte Shopify-kundestøtte for å få hjelp med feilsøking, noterer du deg informasjonen i feltet **Forespørsels-ID** . Denne informasjonen kan bidra til å løse problemet raskere.

Du kan laste ned forespørselen og svarverdiene som filer i et tekstformat.

Vurder å slå av logging for å unngå innvirkning på ytelsen og størrelsen på databasen.

## <a name="data-capture"></a>Dataregistrering

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

## <a name="reset-sync"></a>Tilbakestill synkronisering

For optimal ytelse importerer koblingen bare kunder, produkter og ordrer som ble opprettet eller endret etter siste synkronisering. På siden **Shopify-butikkort** finnes det funksjoner som endrer dato/klokkeslett for siste synkronisering, eller tilbakestille den fullstendig. Denne funksjonen sikrer at alle data synkroniseres i stedet for bare endringer siden forrige synkronisering.

Denne funksjonen gjelder bare synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan være nyttig hvis du må gjenopprette slettede data, for eksempel produkter, kunder eller slettede ordrer.

## <a name="request-the-access-token"></a>Be om tilgangstokenet

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke vil koble til Shopify-kontoen, kan du prøve å be om tilgangstokenet fra Shopify. Du må kanskje be om et nytt token hvis det ble gjort endringer i sikkerhetsnøklene eller nødvendige tillatelser (omfang).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil hente tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen.

Veksleknappen **Has AccessKey** er slått på.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Kontroller og aktiver tillatelser for å foreta HTTP-forespørsler i et ikke-produksjonsmiljø

Shopify-koblingsutvidelsen krever tillatelse til å utføre HTTP-forespørsler for å fungere skikkelig. Når du kjører tester i et sandkassemiljø, er HTTP-forespørslene forbudt for alle utvidelser.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utvidelsesbehandling**, og velg deretter den relaterte koblingen.
2. Velg utvidelsen **Shopify-kobling**.
3. Velg handlingen **Konfigurer** for å åpne siden **Utvidelsesinnstilling**.
4. Kontroller at vekslebryteren **Tillat HTTPClient-forespørsler** er aktivert.

## <a name="rotate-the-shopify-access-token"></a>Roter Shopify-tilgangstokenet

De følgende fremgangsmåtene beskriver hvordan du roterer tilgangstokenet som brukes av Shopify-koblingen for å få tilgang til Shopify-nettbutikken.

### <a name="in-shopify"></a>I Shopify

1. Fra **Shopify-administratoren** går du til [Apper](https://www.shopify.com/admin/apps).
2. Velg **Slett** i raden med **Dynamics 365 Business Central**-appen.
3. Velg **Slett** i meldingen som vises.

### <a name="in-"></a>I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil rotere tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvern og tillatelser, og deretter velger du knappen **Installer app**.

## <a name="known-issues"></a>Kjente problemer

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Feil: Salgshodet finnes ikke. Identifikasjonsfelter og -verdier: Dokumenttype='Quote',No.='YOUR SHOPIFY STORE'

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

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Feil: Firmabokføringsgruppe må ha en verdi hos kunden: 'YOUR SHOPIFY STORE'. Den kan ikke være null eller tom

På siden **Shopify-butikkort** i feltet **Kundemalkode** velger du malen som har **Bokføringsgruppe – firma** fylt ut. Kundemalen brukes til å opprette kunder og beregne salgspriser for salgsdokumenter.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Feil: Import av data til Shopify-butikk er ikke aktivert. Gå til butikkortet for å aktivere det

På siden **Shopify-butikkort** aktiverer du veksleknappen **Tillat datasynkronisering til Shopify**. Denne innstillingen bidrar til å beskytte nettbutikken fra å motta demodata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Feil: Oauth-feilen invalid_request: Finner ikke Shopify API-program med api_key

Det ser ut til at du bruker [Bygg inn-appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) der klientnettadressen har formatet: `https://[application name].bc.dynamics.com`. Shopify-koblingen fungerer ikke for innebygde apper. Hvis du vil finne ut mer, kan du gå til [Hvilke Microsoft-produkter er Shopify-koblingen tilgjengelig for?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Feil: intern feil. Det ser til at noe gikk galt hos oss. Forespørsels-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Kontakt Shopify-kundestøtten innen sju dager når du får denne feilen, og oppgi forespørsels-ID-en. Hvis du vil ha mer informasjon, går du til [Kundestøttealternativer for Shopify](shopify-faq.md#shopify).

### <a name="error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app"></a>Feil: Oauth-feil invalid_request: Kontoen din har ikke tillatelse til å gi den forespurte tilgangen for denne appen.

Det ser ut til at brukere som ber om tilgang, ikke har rettigheter til å administrere apper (mulighet til å administrere og installere apper og kanaler samt potensielt godkjenne appgebyr). Du kan kanskje løse dette problemet ved å installere appen som kontoeier. Alternativt kan du kontrollere **apptillatelsen** for brukeren i innstillingen [**Bruker og tillatelser**](https://www.shopify.com/admin/settings/account) i **Shopify-administratoren**.  

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)
