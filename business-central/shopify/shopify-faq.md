---
title: Vanlige spørsmål for tekniske detaljer
description: Implementeringsdetaljer knyttet til Shopify-koblingen.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 534b4aa47820bc3738a8ffc22a02151efef64863
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802906"
---
# <a name="faq-for-technical-details"></a>Vanlige spørsmål for tekniske detaljer

Denne artikkelen svarer på vanlige spørsmål om Shopify-koblingen.

## <a name="what-is-shopify"></a>Hva er Shopify? 

Shopify er en abonnementsbasert programvare som gjør det mulig for alle å opprette en nettbutikk og selge produktene sine. Shopify-plattformen tilbyr nettforhandlere for en rekke tjenester, inkludert verktøy for innbetalinger, markedsføring, levering og kundeengasjement. 

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Hva er Microsoft Dynamics 365 Business Central Shopify-koblingen? 

Med Shopify-koblingen kan virksomheter koble Shopify-butikken (eller butikkene) sammen med [!INCLUDE[prod_short](../includes/prod_short.md)] for å maksimere produktiviteten. Ved å bruke Shopify-koblingen kan de administrere og vise innsikt fra virksomheten og Shopify-nettbutikken som én enhet. 

### <a name="capabilities"></a>Funksjoner

- Støtte for mer enn én Shopify-butikk
  - Hver butikk har sitt eget oppsett, inkludert en samling produkter, lokasjoner som brukes til å beregne lager og prislister.  
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
  - Bruk landspesifikke maler når du oppretter kunder, noe som bidrar til å sikre at avgiftsinnstillingene er riktige.  
- Import av ordrer fra Shopify
  - Ta med ordrer som er opprettet i ulike salgskanaler, for eksempel nettbutikk eller **Shopify-salgssted**. 
  - Leveringskostnader, gavekort, tips, leverings- og betalingsmåter, transaksjoner og risiko for svindel.  
  - Under importen kan du automatisk opprette kunder i [!INCLUDE [prod_short](../includes/prod_short.md)] eller velge å håndtere kundene i Shopify.  
  - Motta utbetalingsopplysninger fra Shopify Payments. 
- Spor oppfyllelsesinformasjon
  - Du kan eventuelt velge å overføre varesporingsinformasjon fra [!INCLUDE [prod_short](../includes/prod_short.md)] til Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Hvorfor har Microsoft og Shopify laget dette partnerskapet? 

[!INCLUDE[prod_short](../includes/prod_long.md)] slår seg sammen med Shopify for å hjelpe kundene med å skape en bedre handleopplevelse. Shopify tilbyr forhandlere en brukervennlig handelsløsning, og [!INCLUDE[prod_short](../includes/prod_short.md)] tilbyr omfattende administrasjon på tvers av økonomi, salg, service og drift i ett brukervennlig program. Effektiv forbindelse mellom de to systemene synkroniserer ordre-, børs- og kundeopplysninger slik at forhandlere kan oppfylle ordrer raskere og bedre betjene kunder.

## <a name="what-microsoft-products-is-the-shopify-connector-available-for"></a>Hvilke Microsoft-produkter er Shopify-koblingen tilgjengelig for?

Denne funksjonen er bare tilgjengelig for nettversjonen av [!INCLUDE[prod_short](../includes/prod_short.md)], fra og med versjon 20.1. Den er ikke tilgjengelig for lokale distribusjoner. Appen med koblingen er forhåndsinstallert for nye miljøer. Organisasjoner med eksisterende miljøer kan laste ned og installere appen fra AppSource. Organisasjonen må ha både en Business Central-lisens og en Shopify-lisens for å kunne bruke koblingen. Finn ut mer om støttede land, språk og utgaver av [!INCLUDE[prod_short](../includes/prod_short.md)] på [Shopify-kobling i AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Shopify-koblingen fungerer ikke for [innebygd app](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), der nettadressen for klienten har formatet: `https://[application name].bc.dynamics.com`. 

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Hva slags støtte tilbys for Shopify-koblingen?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Shopify-koblingen er dekket av nåværende støttemodell. Finn ut mer på [Teknisk støtte](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (bare på engelsk). 

Få hjelp fra en konsulent som kjenner Shopify-koblingen for [!INCLUDE[prod_short](../includes/prod_short.md)] for å dekke dine unike forretningsspesifikke krav.
 
Søk i [konsulenttjenester](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Få hjelp med Shopify ved å starte med [Generelt Shopify-hjelpesenter](https://help.shopify.com/) eller [Døgnstøtte for butikken som Shopify-forhandler](https://help.shopify.com/questions#/). 

Du kan også utforske [Ekspertmarkedsplassen](https://experts.shopify.com/) for å finne de riktige ekspertene som tilbyr tjenester for Shopify-forhandlere.

## <a name="currently-not-supported-features-however-were-tracking-them-and-may-consider-adding-them-in-the-future"></a>Funksjoner som for øyeblikket ikke støttes, men som vi sporer og kan vurdere å legge dem til senere:

- B2B-funksjoner, inkludert selskaper, prislister for selskap, betalingsbetingelser
- Markeder
  - Flere oversettelser av hoveddataene. Du kan velge ett språk som skal brukes ved eksport av produktinformasjon.
  - Priser per land/område. Det finnes én pris liste for den valgte valutaen. Konverteringen til andre valutaer blir håndtert av Shopify.

## <a name="is-the-shopify-connector-extensible"></a>Kan Shopify-koblingen utvides?

Denne appen er for øyeblikket ikke-utvidbar med planer om å gjøre den utvidbar i 2023. 

## <a name="is-the-shopify-connector-open-for-contribution"></a>Er Shopify-koblingen åpen for bidrag

Ja, denne utvidelsen er åpen for bidrag av fellesskapet. Du finner [kildekoden](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) i tilleggsrepositoriet for Microsoft Al-programmer.


## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
