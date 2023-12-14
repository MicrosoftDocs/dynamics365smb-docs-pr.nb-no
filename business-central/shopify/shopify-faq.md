---
title: Vanlige spørsmål for tekniske detaljer
description: Implementeringsdetaljer knyttet til Shopify-koblingen.
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="faq-for-technical-details"></a>Vanlige spørsmål for tekniske detaljer

Denne artikkelen svarer på vanlige spørsmål om Shopify-koblingen.

## <a name="what-is-shopify"></a>Hva er Shopify?

Shopify er et abonnementsbasert program som gjør det mulig for alle å opprette en nettbutikk og selge produkter. Shopify-plattformen tilbyr nettforhandlere for en rekke tjenester for innbetalinger, markedsføring, levering og kundeengasjement.

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Hva er Microsoft Dynamics 365 Business Central Shopify-koblingen?

Med Shopify-koblingen kan virksomheter koble Shopify-butikken (eller butikkene) sammen med [!INCLUDE[prod_short](../includes/prod_short.md)] for å maksimere produktiviteten. Ved å bruke Shopify-koblingen kan de få tilgang til og administrere innsikt fra virksomheten og Shopify-nettbutikken som én enhet.

### <a name="capabilities"></a>Funksjoner

- Støtte for mer enn én Shopify-butikk
  - Hver butikk har sitt eget oppsett, inkludert en samling produkter og lokasjoner som brukes til å beregne lager og prislister.  
- Toveissynkronisering av varer eller produkter
  - Koblingen synkroniserer bilder, varevarianter, strekkoder, leverandørvarenumre, utvidede tekster og koder.  
  - Eksporter vareattributter til Shopify.  
  - Bruk valgte kundeprisgrupper og rabatter til å definere priser som er eksportert til Shopify.  
  - Angi om varer kan opprettes automatisk, eller bare tillat oppdateringer av eksisterende produkter.  
- Synkronisering av lagernivåer
  - Velg noen av eller alle de tilgjengelige lokasjonene i [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Oppdater lagernivåer på flere lokasjoner i Shopify.  
- Toveissynkronisering av kunder
  - Kartlegg kunder smart per telefon og e-post.  
  - Bruk land-/områdespesifikke maler når du oppretter kunder, noe som bidrar til å sikre at avgiftsinnstillingene er riktige.  
- Importer ordrer fra Shopify
  - Ta med ordrer som er opprettet i ulike salgskanaler, for eksempel nettbutikk eller **Shopify-salgssted**.
  - Leveringskostnader, gavekort, tips, leverings- og betalingsmåter, transaksjoner og risiko for svindel.  
  - Under import kan du automatisk opprette kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller velge å håndtere kundene i Shopify.  
  - Motta utbetalingsopplysninger fra Shopify Payments.
- Spor oppfyllelsesinformasjon
  - Du kan eventuelt velge å overføre varesporingsinformasjon fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Hvorfor har Microsoft og Shopify laget dette partnerskapet?

[!INCLUDE[prod_short](../includes/prod_long.md)] slår seg sammen med Shopify for å hjelpe kundene med å skape en bedre handleopplevelse. Shopify tilbyr forhandlere en brukervennlig handelsløsning, og [!INCLUDE[prod_short](../includes/prod_short.md)] tilbyr omfattende administrasjon på tvers av økonomi, salg, service og drift. Bruk effektiv forbindelse mellom programmene til å synkronisere ordre-, lager- og kundeopplysninger for å oppfylle ordrer raskere og bedre betjene kunder.

## <a name="which-microsoft-products-are-the-shopify-connector-available-for"></a>Hvilke Microsoft-produkter er Shopify-koblingen tilgjengelig for?

Denne funksjonen er bare tilgjengelig for nettversjonen av [!INCLUDE[prod_short](../includes/prod_short.md)], fra og med versjon 20.1. Den er ikke tilgjengelig for lokale distribusjoner. Koblingen er forhåndsinstallert for nye miljøer. Organisasjoner med eksisterende miljøer kan laste ned og installere koblingen fra AppSource. Organisasjonen må ha både en [!INCLUDE [prod_short](../includes/prod_short.md)]-lisens og en Shopify-lisens for å kunne bruke koblingen. Hvis du vil finne ut mer om støttede land/områder, språk og utgaver av [!INCLUDE[prod_short](../includes/prod_short.md)], går du til [Shopify-kobling i AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-koblingen fungerer ikke for [innebygd app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), der nettadressen for klienten har formatet `https://[application name].bc.dynamics.com`.

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Hva slags støtte tilbys for Shopify-koblingen?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-koblingen er dekket av nåværende støttemodell. Finn ut mer på [Teknisk støtte](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (bare på engelsk).

Få hjelp fra en konsulent som kjenner Shopify-koblingen for [!INCLUDE[prod_short](../includes/prod_short.md)] for å dekke dine unike forretningsspesifikke krav. Søk i [konsulenttjenester](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Få hjelp med Shopify fra [Generelt Shopify-hjelpesenter](https://help.shopify.com/) eller fra [Døgnstøtte for butikken som Shopify-forhandler](https://help.shopify.com/questions#/).

Du kan også utforske [Ekspertmarkedsplassen](https://experts.shopify.com/) for å finne de riktige ekspertene som tilbyr tjenester for Shopify-forhandlere.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them"></a>Funksjoner som for øyeblikket ikke støttes, men som vi sporer og kan vurdere å legge til

- B2B-funksjoner, inkludert selskaper, prislister for selskap og betalingsbetingelser
  - Det er for tiden mulig å importere ordrer opprettet via B2B. Hvis du har flere kjøpere knyttet til selskapet, bør du ikke aktivere automatisk oppretting av kunder, men koble hver Shopify-kjøper til en respektive kunde manuelt.
  - Du må vedlikeholde selskapets prislister i Shopify.
- Markeder
  - Flere oversettelser av hoveddataene. Du kan velge ett språk som skal brukes ved eksport av produktinformasjon.
  - Priser per land/område. Det finnes én pris liste for den valgte valutaen. Shopify håndterer konverteringen til andre valutaer.
- Lag utkast til ordrer

## <a name="is-the-shopify-connector-extensible"></a>Kan Shopify-koblingen utvides?

Ja, Shopify-koblingenen kan utvides. Kontroller GitHub for å få tilgang til [oversikten over utvidelsespunkter](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) og se nærmere på [eksempler](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## <a name="is-the-shopify-connector-open-for-contribution"></a>Er Shopify-koblingen åpen for bidrag

Ja, denne utvidelsen er åpen for bidrag fra fellesskapet. Du finner [kildekoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i tilleggsrepositoriet for Microsoft Al-programmer.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
