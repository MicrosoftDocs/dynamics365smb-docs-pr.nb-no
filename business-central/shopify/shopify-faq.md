---
title: Vanlige spørsmål for tekniske detaljer
description: Implementeringsdetaljer knyttet til Shopify-koblingen.
ms.date: 05/01/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Vanlige spørsmål for tekniske detaljer

Denne artikkelen svarer på vanlige spørsmål om Shopify-koblingen.

## Hva er Shopify?

Shopify er et abonnementsbasert program som gjør det mulig for alle å opprette en nettbutikk og selge produkter. Shopify-plattformen tilbyr nettforhandlere for en rekke tjenester for innbetalinger, markedsføring, levering og kundeengasjement.

## Hva er Microsoft Dynamics 365 Business Central Shopify-koblingen?

Med Shopify-koblingen kan virksomheter koble Shopify-butikkene sammen med [!INCLUDE[prod_short](../includes/prod_short.md)] for å maksimere produktiviteten. Ved å bruke Shopify-koblingen kan de få tilgang til og administrere innsikt fra virksomheten og Shopify-nettbutikken som én enhet.

### Funksjoner

- Støtte for mer enn én Shopify-butikk
  - Hver butikk har sitt eget oppsett, inkludert en samling produkter og lokasjoner som brukes til å beregne lager og prislister.  
- Toveissynkronisering av varer eller produkter
  - Koblingen synkroniserer bilder, varevarianter, strekkoder, leverandørvarenumre, utvidede tekster, markedsføringstekster og koder.  
  - Eksporter vareattributter til Shopify.  
  - Bruk valgte kundeprisgrupper og rabatter til å definere priser som er eksportert til Shopify.
  - Definer priser og rabatter for produktkataloger knyttet til B2B-selskaper.
  - Angi om varer kan opprettes automatisk, eller bare tillat oppdateringer av eksisterende produkter.
- Synkronisering av lagernivåer
  - Velg noen av eller alle de tilgjengelige lokasjonene i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Oppdater lagernivåer på flere lokasjoner i Shopify.  
- Toveissynkronisering av kunder og selskaper
  - Kartlegg kunder smart per telefon og e-post.  
  - Bruk land-/områdespesifikke maler når du oppretter kunder, noe som bidrar til å sikre at avgiftsinnstillingene er riktige.  
- Importer ordrer fra Shopify
  - Ta med ordrer som er opprettet i ulike salgskanaler, for eksempel nettbutikk, **Shopify-salgssted** eller **B2B**.
  - Leveringskostnader, gavekort, tips, leverings- og betalingsmåter, transaksjoner og risiko for svindel.  
  - Under import kan du automatisk opprette kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller velge å håndtere kundene i Shopify.  
  - Motta utbetalingsopplysninger fra Shopify Payments.
- Spor oppfyllelsesinformasjon
  - Du kan eventuelt velge å overføre varesporingsinformasjon fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.
- Hodeløs integrasjon
  - Aktiver automatisk synkronisering av produkter, lager, ordrer, oppfyllelser og mer.

## Hvorfor har Microsoft og Shopify laget dette partnerskapet?

[!INCLUDE[prod_short](../includes/prod_long.md)] slår seg sammen med Shopify for å hjelpe kundene med å skape en bedre handleopplevelse. Shopify tilbyr forhandlere en brukervennlig handelsløsning, og [!INCLUDE[prod_short](../includes/prod_short.md)] tilbyr omfattende administrasjon på tvers av økonomi, salg, service og drift. Bruk effektiv forbindelse mellom programmene til å synkronisere ordre-, lager- og kundeopplysninger for å oppfylle ordrer raskere og bedre betjene kunder.

## Hvilke Microsoft-produkter fungerer med Shopify-koblingen?

Koblingen er bare tilgjengelig for nettversjonen av [!INCLUDE[prod_short](../includes/prod_short.md)], fra og med versjon 20.1. Den er ikke tilgjengelig for lokale distribusjoner. Koblingen er forhåndsinstallert for nye miljøer. Organisasjoner med eksisterende miljøer kan laste ned og installere koblingen fra AppSource. Organisasjonen må ha både en [!INCLUDE [prod_short](../includes/prod_short.md)]-lisens og en Shopify-lisens for å kunne bruke koblingen. Hvis du vil finne ut mer om støttede land/områder, språk og utgaver av [!INCLUDE[prod_short](../includes/prod_short.md)], går du til [Shopify-kobling i AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-koblingen fungerer ikke for [innebygd app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), der nettadressen for klienten har formatet `https://[application name].bc.dynamics.com`.

Shopify-koblingen fungerer ikke med andre produkter i Dynamics 365-porteføljen.

## Hva slags støtte tilbys for Shopify-koblingen?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-koblingen er dekket av nåværende støttemodell. Finn ut mer på [Teknisk støtte](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (bare på engelsk).

Få hjelp fra en konsulent som kjenner Shopify-koblingen for [!INCLUDE[prod_short](../includes/prod_short.md)] for å dekke dine unike forretningsspesifikke krav. Søk i [konsulenttjenester](https://aka.ms/BCShopifyConsultant).

### Shopify

Få hjelp med Shopify fra [Generelt Shopify-hjelpesenter](https://help.shopify.com/) eller fra [Døgnstøtte for butikken som Shopify-forhandler](https://help.shopify.com/questions#/).

Du kan også utforske [Ekspertmarkedsplassen](https://experts.shopify.com/) for å finne de riktige ekspertene som tilbyr tjenester for Shopify-forhandlere.

## Funksjoner som for øyeblikket ikke støttes, men som vi sporer og kan vurdere å legge til

- Markeder
  - Flere oversettelser av hoveddataene. Du kan velge ett språk som skal brukes ved eksport av produktinformasjon.
  - Priser per land/område. Det finnes én pris liste for den valgte valutaen. Shopify håndterer konverteringen til andre valutaer.
- Lag utkast til ordrer

## Kan Shopify-koblingen utvides?

Ja, Shopify-koblingenen kan utvides. Kontroller GitHub for å få tilgang til [oversikten over utvidelsespunkter](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) og se nærmere på [eksempler](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify).

## Er Shopify-koblingen åpen for bidrag?

Denne utvidelsen er åpen for bidrag fra fellesskapet. Du finner [kildekoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i tilleggsrepositoriet for Microsoft Al-programmer.

## Bygg din versjon av Shopify-koblingen

Hvis du vil bygge og publisere en koblingsapp på Shopify-markedsplassen som har som hovedformål å overføre eller dele selgerdata til en tredjepart ([!INCLUDE [prod_short](../includes/prod_short.md)]), må du ifølge Shopify ha skriftlig samtykke fra Shopify. Som en del av denne prosessen må du innhente samtykke fra Microsoft i skjemaet for bekreftelse for sluttmottakerdata. Vi må be deg om å håndtere saken med Shopify fordi Microsoft ikke kan signere tredjepartsavtaler.

### Hva som skal gjøres

Sjekk Shopify-kravene fordi du fortsatt kan ha en app som ikke er oppført.

Alternativt får Shopify-koblingen for [!INCLUDE [prod_short](../includes/prod_short.md)] stadig nye funksjoner og nye kunder. Hvis du oppdager et spesifikt avvik, bør du vurdere å [sende inn et produktforslag](https://aka.ms/bcideas) eller et kodebidrag til [!INCLUDE [prod_short](../includes/prod_short.md)]. For krav som kanskje ikke er relevante for et flertall av kundene, og som ikke enkelt kan løses av den nåværende utvidelsesmodellen, kan du kontakte [!INCLUDE [prod_short](../includes/prod_short.md)]-utviklingsteamet for å diskutere brukstilfellet. Vi skal kunne finne en gjennomførbar løsning.

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
