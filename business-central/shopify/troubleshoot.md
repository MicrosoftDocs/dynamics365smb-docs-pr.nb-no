---
title: Feilsøking av Shopify- og Business Central-synkronisering
description: Lær hva du gjør hvis noe går galt under synkronisering av data mellom Shopify og Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 01ff5ab1c5e6f132098f914f6bfe97e097cc88b0
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768164"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Feilsøking av Shopify- og Business Central-synkronisering

Det er mulig å støte på situasjoner der du må feilsøke problemer. Denne siden definerer trinnene for å feilsøke enkelte vanlige scenarioer som kan oppstå.

## <a name="logs"></a>Logger

Hvis en synkroniseringsoppgave mislykkes, kan du aktivere loggføring ved å aktivere/deaktiver **Loggposter** på **Shopify-butikkortet**. Utløs synkronisering av oppgaver og se gjennom logger manuelt.

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-loggposter**. Velg deretter den relaterte koblingen.
2. Velg den tilknyttede loggposten, og åpne vinduet **Shopify-loggpost**.
3. Gå gjennom forespørsel, statuskode og beskrivelse og svar.

Husk å slå av logging for å unngå negativ innvirkning på ytelsen og øke størrelsen på databasen.

Fra vinduet **Shopify-loggposter** kan du utløse sletting av alle loggposter eller de som er eldre enn sju dager.

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

## <a name="update-the-access-token"></a>Oppdater tilgangstokenet

Hvis [!INCLUDE[prod_short](../includes/prod_short.md)] ikke kan koble til Shopify-kontoen, kan du prøve å tilbakestille tilgangstokenet.

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil hente tilgangstokenet for for å åpne siden **Shopify-butikkort**.
3. I feltet **Kode** angir du koden.  
4. Velg handlingen **Be om tilgang**.
5. Hvis du blir bedt om å logge deg på Shopify-kontoen.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
