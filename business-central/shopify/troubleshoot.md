---
title: Feilsøking av Shopify- og Business Central-synkronisering
description: Lær hva du gjør hvis noe går galt under synkroniseringen av data mellom Shopify og Business Central
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Feilsøking av Shopify- og Business Central-synkronisering

Du kan støte på situasjoner der du må feilsøke problemer når du synkroniserer data mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne siden definerer feilsøkingstrinnene for noen vanlige scenarioer.

## Kjør oppgaver i forgrunnen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil feilsøke for å åpne siden **Shopify-butikkort**.
3. Slå av vekslebryteren **Tillat bakgrunnssynkroniseringer**.

Når synkroniseringshandlingen utløses nå, vil synkroniseringshandlingen kjøres i forgrunnen og hvis det oppstår en feil, vises en feildialogboks med **Kopier detaljer**-kobling. Bruk denne koblingen til å kopiere tilleggsinformasjon til et tekstredigeringsprogram for ytterligere analyse.

## Logger

Hvis en synkroniseringsoppgave mislykkes, kan du slå på vekslebryteren **Logg aktivert** på siden **Shopify-butikkort** for å aktivere loggføring. Deretter kan du manuelt utløse synkroniseringen av oppgaver og se gjennom logger.

### Slik aktiverer du loggføring

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil feilsøke for å åpne siden **Shopify-butikkort**.
3. Slå på vekslebryteren **Logg aktivert**.

### Sli ser du gjennom logger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-loggposter**. Velg deretter den relaterte koblingen.
2. Velg den tilknyttede loggposten, og åpne siden **Shopify-loggpost**.
3. Gå gjennom forespørsel, statuskode og beskrivelse og svarverdier. Du kan laste ned forespørselen og svarverdiene som filer i et tekstformat.

Husk senere å slå av logging for å unngå negativ innvirkning på ytelsen og øke størrelsen på databasen.

Fra siden **Shopify-loggposter** kan du utløse sletting av alle loggposter eller de som er eldre enn sju dager.

## Dataregistrering

Uavhengig av innstillingene **Logg aktivert** blir noen Shopify-svar alltid loggførte slik at du kan undersøke eller laste dem ned ved hjelp av siden **Dataregistreringsliste**.

Velg handlingen **Hentede Shopify-data** på en av følgende sider:

- **Shopify-ordre**
- **Shopify-ordreoppfyllelse**
- **Shopify-ordreleveringskostnader**
- **Shopify-ordretransaksjoner**
- **Shopify-utbetalinger**
- **Shopify-betalingstransaksjoner**
- **Shopify-transaksjoner**

## Tilbakestill synkronisering

For optimal ytelse importerer koblingen bare kunder, produkter og ordrer som er opprettet eller endret siden siste synkronisering. På siden **Shopify-butikkort** finnes det funksjoner som endrer dato/klokkeslett for siste synkronisering, eller tilbakestille den fullstendig. Denne funksjonen sikrer at alle data synkroniseres i stedet for bare endringer siden forrige synkronisering, når synkroniseringen kjøres.

Denne funksjonen gjelder bare synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)]. Den kan være nyttig hvis du må gjenopprette slettede data, for eksempel produkter, kunder eller slettede ordrer.

## Be om tilgangstokenet

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke vil koble til Shopify-kontoen, kan du prøve å be om tilgangstokenet fra Shopify. Denne forespørselen kan være nødvendig hvis det er en rotasjon av sikkerhetsnøkler eller endringer i nødvendige tillatelser (omfang).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil hente tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen.

**Har tilgangsnøkkel**-veksleknappen blir aktivert.

### Kontroller og aktiver tillatelser for å foreta HTTP-forespørsler når du kjører i et ikke-produksjonsmiljø

Shopify-koblingsutvidelsen krever tillatelse til å utføre HTTP-forespørsler for å fungere skikkelig. Når du tester i en sandkasse, er HTTP-forespørslene forbudt for alle utvidelser.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **utvidelsesbehandling**, og velg den relaterte koblingen.
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

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikker**. Velg den relaterte koblingen.
2. Velg butikken du vil rotere tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvern og tillatelser, og deretter velger du knappen **Installer app**.

## Kjente problemer

### Feil: Salgshodet finnes ikke. Identifikasjonsfelter og -verdier: Dokumenttype='Quote',No.='YOU SHOPIFY STORE'

Hvis du vil beregne priser, oppretter Shopify-koblingen midlertidig salgsdokument (tilbud) for midlertidig kunde (butikkode) og lar standard prisberegningslogikk gjøre jobben sin. Det er vanlig scenario når en tredjepartsutvidelse abonnerer på hendelser i salgslinjen, men ikke kontrollerer at posten er midlertidig, slik at hodet kanskje ikke er tilgjengelig. Vi anbefaler at du kontakter leverandøren av utvidelsen og ber vedkommende endre koden for å kontrollere om postene er midlertidige. I noen tilfeller er det å legge til `IsTemporary`-metoden på riktig plass nok. Gå til [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method) for å lære mer om IsTemporary. 

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

### Feil: Firmabokføringsgruppe må ha en verdi hos kunden: 'YOU SHOPIFY STORE'. Den kan ikke være null eller tom

På siden **Shopify-butikkort** fyller du ut feltet **Kundemalkode** med malen som har **Bokføringsgruppe – firma** fylt ut. Kundemalen brukes ikke bare til oppretting av kunder, men også for beregning av salgspris og oppretting av salgsdokumenter.

### Feil: Import av data til Shopify-butikk er ikke aktivert. Gå til butikkortet for å aktivere det

I vinduet **Shopify-butikkort** aktiverer du veksleknappen **Tillat datasynkronisering til Shopify**. Denne vekslingen er ment å beskytte nettbutikken fra å motta demodata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

### Feil: Oauth-feilen invalid_request: Finner ikke Shopify API-program med api_key

Det ser ut til at du bruker [Bygg inn-appen](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) der klientnettadressen har formatet: `https://[application name].bc.dynamics.com`. Shopify-koblingen fungerer ikke for innebygde apper. Hvis du vil ha mer informasjon, kan du se [Hvilke Microsoft-produkter er Shopify-koblingen tilgjengelig for?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)
