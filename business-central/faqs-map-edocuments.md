---
title: Vanlige spørsmål om tildelinger av e-dokumenter med bestillinger
description: 'Disse vanlige spørsmålene om ansvarlig kunstig intelligens gir informasjon om KI-teknologien som brukes i Business Central, sammen med viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den ble testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# Vanlige spørsmål om å tildele e-dokumenter med bestillinger ved hjelp av Copilot (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for funksjonen **Samsvarshjelp for e-dokumenter** i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Hva er samsvarshjelp for e-dokument?

Elektroniske dokumenter (e-dokumenter) fungerer som grunnlaget for moderne forretningstransaksjoner. De representerer viktig papirarbeid som fakturaer og kvitteringer som flyter i begge retninger gjennom levering og mottak. Du kan generere og overføre elektroniske fakturaer digitalt i et strukturert format som forenkler automatisert fakturabehandling. Håndtering av innkommende digitale fakturaer kan imidlertid være mer komplisert for leverandørteam.  

I små og mellomstore bedrifter spiller regnskapssteamet en sentral rolle i nøyaktig sporing av leverandørforpliktelser. Hovedansvaret deres er å registrere innkommende fakturaer nøyaktig. Det kan kreve innsats å oppnå presisjon, spesielt når de avstemmer eksterne fakturaer fra leverandører med eksisterende bestillinger. Avvik i koder, beskrivelser og måleenheter byr ofte på utfordringer fordi disse elementene kanskje ikke samsvarer på tvers av ulike systemer og selskaper. Uventede kostnader, for eksempel transportgebyrer, kan også vises som separate linjeelementer som må justeres manuelt. Regnskapsførere må også inkludere fakturanummer og -datoer i dokumentene. Det er viktig å merke seg at relasjonen mellom bestillinger og eksterne fakturaer ikke alltid er én-til-én. Du kan motta flere eksterne fakturaer for den samme bestillingen.

Historisk sett kunne [!INCLUDE [prod_short](includes/prod_short.md)] generere nye kjøpsfakturaer basert på mottatte elektroniske fakturaer. Manuell samsvaring av fakturaer med eksisterende bestillinger var imidlertid en tidkrevende prosess utsatt for feil.

**Samsvarshjelp for e-dokumenter** bruker generativ kunstig intelligens til å effektivisere denne prosessen ved å automatisere analysen av eksterne elektroniske fakturaer. Funksjonen gjør det mulig for regnskapsførere å be Copilot om å samsvare linjer på innkommende elektroniske fakturaer med linjer på bestillinger i [!INCLUDE [prod_short](includes/prod_short.md)].

## Hva er funksjonene i samsvarshjelpen for e-dokumenter?

Copilot gir hjelp drevet av kunstig intelligens for å samsvare mottatt digital faktura med eksisterende bestillinger i [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot samsvarer linjer basert på følgende:

- Likhet i beskrivelser
- Enheter
- Tilgjengelig antall for fakturering
- Beløp

Copilot identifiserer lignende beskrivelser hvis de har riktig enhet og priser, men kan også finne samsvar i mer komplekse tilfeller. Den kan for eksempel identifisere om en elektronisk faktura har to linjer med en variant av samme vare, og bare én linje i bestillingen. [!INCLUDE [prod_short](includes/prod_short.md)] samsvarer disse linjene så lenge beskrivelsene er like og prisene er de samme.

Copilot kobler ikke til endepunkttjenesten for e-dokumenter for å hente eller sende digitale bilag. Denne oppgaven er helt innenfor din kontroll og er en forutsetning for å kunne bruke Copilots hjelp. Dette gjelder uavhengig av om de digitale dokumentene legges til i [!INCLUDE [prod_short](includes/prod_short.md)] ved hjelp av en tilkobling til en endepunktstjeneste eller angis manuelt.  

## Hva er den tiltenkte bruken av samsvarshjelp for e-dokumenter?  

Målet med funksjonen **Samsvarshjelp for e-dokumenter** er å hjelpe leverandørteamet med å samsvare eksisterende bestillinger med innkommende elektroniske fakturaer. Mye av denne aktiviteten dreier seg om strengsamsvar. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyr en funksjon som automatiserer noe av denne aktiviteten, og store språkmodeller har blitt identifisert som en mulighet til å supplere denne funksjonen og ytterligere redusere manuell innsats.  

## Hvordan ble samsvarshjelp for e-dokumenter evaluert? Hvilke målinger brukes til å måle ytelse?

Denne funksjonen ble testet ved hjelp av kombinasjoner av følgende informasjon:

- Beskrivelser av eksterne varer
- Enheter
- Antall og beløp
- Standard varebeskrivelser
- Ulike språk
- Andre parametere som dekker vanlige variasjoner og datagrenser for hvert felt 

Testdata representerer både typisk bruk og bruk av dårlige aktører. Ytelsen ble målt sammenlignet med manuelt samsvar av de samme dataene i elektroniske fakturaer og bestillinger.

## Hva er begrensningene til samsvarshjelpen for e-dokumenter? Hvordan kan brukere minimere virkningen av begrensninger for samsvarshjelp for e-dokumenter når de bruker systemet?

**Samsvarshjelp for e-dokumenter** fungerer best når eksterne varebeskrivelser (e-faktura) og interne varebeskrivelser ([!INCLUDE [prod_short](includes/prod_short.md)]) og enheter er på samme språk. Blandede språk eller blandet språk i varebeskrivelser resulterer ofte i færre treff og forslag.  

Foreslått samsvar mellom varer fra e-fakturaer og varer i bestillinger fungerer best på engelsk. Selv om du kan bruke denne funksjonen på alle språk som [!INCLUDE [prod_short](includes/prod_short.md)] støtter, kan du oppleve færre varetreff på andre språk.

## I hvilke geografiske områder og på hvilke språk er samsvarshjelp for e-dokumenter tilgjengelig? 

Denne funksjonen er tilgjengelig for alle land-/områdemiljøer og på alle brukerspråk med unntak av Canada. På grunn av begrenset språkstøtte er funksjonen i utgangspunktet ikke tilgjengelig for kanadiske kunder fordi den ikke oppfyller regelverket for språkoverholdelse. 

For kundemiljøer i land/områder der Azure OpenAI-tjenesten ikke er tatt i bruk, må administratorer først samtykke til å tillate flytting av data over grenser for at [!INCLUDE [prod_short](includes/prod_short.md)] skal koble til Azure OpenAI-tjenesten og for at denne funksjonen skal være tilgjengelig.  

Hvis du vil ha mer informasjon om språk, kan du gå til [Hva er begrensningene for samsvarshjelp for e-dokumenter? Hvordan kan brukere minimere virkningen av begrensningene for samsvarshjelp for e-dokumenter når de bruker systemet?](#what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system).   

## Hvilke driftsfaktorer og innstillinger gjør at det går an å bruke funksjonen på en effektiv og ansvarlig måte?

Copilot supplerer tildelingsalgoritmen som [!INCLUDE [prod_short](includes/prod_short.md)] allerede gir og tildeler linjene som algoritmen ikke gjorde.

### Hva forventes av sluttbrukere når de bruker samsvarshjelp for e-dokumenter?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Når du har tildelt innkommende elektroniske fakturaer med bestillinger, må du tildele linjene i dokumentene.

Siden **Bestillingstildeling** viser alle linjene fra begge dokumentene. Her kan du gjøre tildelingen manuelt, noe som kan være vanskelig hvis det er mange linjer.

Du kan bruke **Samsvarshjelp for e-dokumenter** til å tildele linjer basert på følgende kriterier:

- Likhet i beskrivelsene
- Enheter
- Tilgjengelig antall for fakturering
- Beløp

Copilots treff kan være feil eller ufullstendige. Du bør alltid vurdere nøyaktigheten før du velger å beholde dem. Copilots treff og forslag lagres i [!INCLUDE [prod_short](includes/prod_short.md)] når du velger **Behold det** og avslutter Copilot. Du kan redigere og korrigere eventuelle treff eller forslag før du velger å beholde dem. 

### Hva forventes av administratorer og sluttbrukere når de bruker samsvarshjelp for e-dokumenter?

Sluttbrukere, for eksempel regnskapsførere eller andre som mottar e-fakturaer, bør alltid vurdere nøyaktigheten av samsvar og forslag fra Copilot før de velger å beholde dem. Vi anbefaler at du ser gjennom bestillingslinjene for å kontrollere nøyaktigheten og finne eventuelle avvik. Du bestemmer selv om du vil bruke **samsvarshjelpen for e-dokumenter**. Selv når **samsvarshjelpen for e-dokumenter** er aktivert av administratorer og tilgjengelig, kan du fortsatt velge å bruke den alltid, noen ganger eller aldri.  

Det er administratorene som avgjør om Copilot i [!INCLUDE [prod_short](includes/prod_short.md)] skal brukes. Hvis de aktiverer Copilot, bør administratorer sørge for at de gir tilgang til de riktige.

> [OBS!]
> - Vi støtter ikke funksjonen for [!INCLUDE [prod_short](includes/prod_short.md)] lokalt eller i private skyer.
> - Partnere kan ikke utvide denne funksjonen. Partnerutviklere kan ikke endre, erstatte eller utvide denne funksjonen. 

## Er Copilot den eneste måten å samsvare e-dokumenter med bestillinger på?  

Nei, det er opp til deg om du bruker Copilot. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyr ikke-KI-drevne metoder for å samsvare varer fra mottatt elektronisk faktura med varer i bestillinger i [!INCLUDE [prod_short](includes/prod_short.md)]. Organisasjoner kan også bruke begge tilnærmingene samtidig.  

## Hvordan gir jeg tilbakemelding om KI-generert innhold?  

Hver gang Copilot gir treff eller forslag, kan du gi tilbakemelding til Microsoft direkte fra Copilot-vinduet, ved hjelp av Liker- og Liker ikke-kontrollene. Din tilbakemelding er anonym, og vi bruker disse dataene til å forbedre kvaliteten på tjenesten.  

## Se også

[Oversikt over e-dokumenter](finance-edocuments-overview.md)
[Tildel e-dokumenter til bestillingslinjer med Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
