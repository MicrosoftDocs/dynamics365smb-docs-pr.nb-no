---
title: Feilsøking av Shopify- og Business Central-synkronisering
description: Lær hva du gjør hvis noe går galt under synkroniseringen av data mellom Shopify og Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4ccbe8ac97eba568ff82d965f24b86ab58c95f81
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317249"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Feilsøking av Shopify- og Business Central-synkronisering

Det er mulig å støte på situasjoner der du må feilsøke problemer når du synkroniserer data mellom Shopify og [!INCLUDE[prod_short](../includes/prod_short.md)]. Denne siden definerer trinnene for å feilsøke enkelte vanlige scenarioer som kan oppstå.

## <a name="logs"></a>Logger

Hvis en synkroniseringsoppgave mislykkes, kan du aktivere loggføring ved å aktivere/deaktiver **Loggposter** på **Shopify-butikkortet**. Utløs synkroniseringen av oppgaver og se gjennom logger manuelt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-loggposter**. Velg deretter den relaterte koblingen.
2. Velg den tilknyttede loggposten, og åpne vinduet **Shopify-loggpost**.
3. Gå gjennom forespørsel, statuskode og beskrivelse og svar.

Husk å slå av logging senere for å unngå negativ innvirkning på ytelsen og øke størrelsen på databasen.

Fra vinduet **Shopify-loggposter** kan du utløse slettingen av alle loggposter eller de som er eldre enn sju dager.

## <a name="data-capture"></a>Dataregistrering

Uavhengig av innstillingene **Logg aktivert** blir noen svar fra Shopify alltid loggførte slik at du kan undersøke eller laste ned ved hjelp av vinduet **Dataregistreringsliste**.

Velg handlingen **Hentede Shopify-data** på en av følgende sider:

- **Shopify-ordre**
- **Shopify-ordreoppfyllelse**
- **Shopify-ordreleveringskostnader**
- **Shopify-ordretransaksjoner**
- **Shopify-utbetalinger**
- **Shopify-betalingstransaksjoner**
- **Shopify-transaksjoner**

## <a name="reset-sync"></a>Tilbakestill synkronisering

For optimal ytelse importerer koblingen bare kunder, produkter og ordrer som er opprettet eller endret siden siste synkronisering. På **Shopify-butikkortet** finnes det funksjoner som kan brukes til å endre dato/klokkeslett for siste synkronisering, eller tilbakestille den fullstendig. Denne funksjonen sikrer at alle data synkroniseres og ikke bare endringer siden forrige synkronisering, når synkroniseringen kjøres.

Denne funksjonen gjelder bare synkroniseringer fra Shopify til [!INCLUDE[prod_short](../includes/prod_short.md)] og kan være nyttig hvis du må gjenopprette slettede data, for eksempel produkter, kunder eller slettede ordrer.

## <a name="request-the-access-token"></a>Be om tilgangstokenet

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke kan koble til Shopify-kontoen, kan du prøve å be om tilgangstokenet fra Shopify. Denne forespørselen kan være nødvendig hvis det er en rotasjon av sikkerhetsnøkler eller endringer i nødvendige tillatelser (omfang).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil hente tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen.

**Har tilgangsnøkkel**-veksleknappen blir aktivert.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Kontroller og aktiver tillatelser for å foreta HTTP-forespørsler når du kjører i et ikke-produksjonsmiljø

Shopify-koblingsutvidelsen krever tillatelse til å utføre HTTP-forespørsler for å fungere skikkelig. Når du tester i sandkasser, er HTTP-forespørslene forbudt for alle utvidelser.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utvidelsesbehandling**, og velg deretter den relaterte koblingen.
2. Velg utvidelsen *Shopify-kobling*.
3. Velg handlingen **Konfigurer** for å åpne siden **Utvidelsesinnstilling**.
4. Kontroller at vekslebryteren **Tillat HTTPClient-forespørsler** er aktivert.

## <a name="rotate-the-shopify-access-key"></a>Rotere Shopify-tilgangsnøkkelsen

De følgende fremgangsmåtene beskriver hvordan du roterer tilgangstokenet som brukes av Shopify-koblingen for å få tilgang til Shopify-nettbutikken.

### <a name="in-shopify"></a>I Shopify

1. Fra **Shopify-administrator** går du til [Apper](https://www.shopify.com/admin/apps).
2. I raden med **Dynamics 365 Business Central** velger du **Slett**.
3. Velg **Slett** i meldingen som vises.

### <a name="in-prod_short"></a>I [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikker** og velger den relaterte koblingen.
2. Velg butikken du vil rotere tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Be om tilgang**.
4. Hvis du blir bedt om det, logger du deg på Shopify-kontoen, ser gjennom personvern og tillatelser, og deretter velger du knappen **Installer app**.

## <a name="known-issues"></a>Kjente problemer

### <a name="gen-bus-posting-group-must-have-a-value-in-customer-it-cannot-be-zero-or-empty"></a>Finans- Bokførings gruppe må ha en verdi hos kunden. Den kan ikke være null eller tom.

Fyll ut feltet **Kundemalkode** i vinduet **Shopify-butikkortet** med malen som har **Bokføringsgruppe - firma** fylt ut. Kundemal brukes ikke bare til oppretting av kunder, men også for beregning av salgspris og oppretting av salgsdokumenter.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Import av data til Shopify-butikk er ikke aktivert. Gå til butikkortet for å aktivere det.

I vinduet **Shopify-butikkort** aktiverer du veksleknappen **Tillat datasynkronisering til Shopify**.  Denne vekslingen er ment å beskytte nettbutikken fra å motta demodata fra [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
