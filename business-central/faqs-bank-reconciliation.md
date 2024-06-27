---
title: Vanlige spørsmål om bankkontoavstemmingshjelp med Copilot
description: 'Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes til å avstemme bankkontoer og kontoutdrag i Business Central. De omfatter viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den er testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Vanlige spørsmål om bankkontoavstemmingshjelp med Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Disse vanlige spørsmålene beskriver KI-effekten av Microsoft Copilot-hjelp med bankkontoavstemming i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Hva er bankkontoavstemmingshjelp?

Bankavstemming er en vanlig regnskapsoppgave der organisasjoner går gjennom bankkontoutdragene for å identifisere transaksjoner som skal registreres i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne oppgaven vil for eksempel bli brukt til å identifisere periodiske bankgebyrer eller små ansattutgifter.

Bankavstemming er vanligvis en prosess med flere trinn. Først importeres kontoutskrifter til [!INCLUDE[prod_short](includes/prod_short.md)]. Deretter avstemmes transaksjoner med poster. Til slutt bokføres nye poster for å gjenspeile eventuelle gjenværende transaksjoner som tidligere ikke var kjent for finansmodulene.

Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] reduserer manuelt arbeid ved å matche flere transaksjoner og foreslå finanskonti du kan bokføre til.

## <a name="what-are-the-capabilities-of-bank-reconciliation-assist"></a>Hva er funksjonene til bankavstemmingshjelpen?

Copilot gir KI-drevet assistanse med to forskjellige oppgaver:

- Forbedret samsvaring av transaksjoner med poster

    [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr automatiserte regler som automatisk samsvarer mange banktransaksjoner med poster. Disse reglene er imidlertid lite fleksible og resulterer ofte i mange transaksjoner uten samsvar som hver krever manuell inspeksjon og sammenligning. Copilot bruker KI-teknologi til å inspisere ikke-avstemte transaksjoner og identifisere flere treff basert på datoer, beløp og beskrivelser. Hvis for eksempel en kunde betalte flere fakturaer som ett engangsbeløp, avstemmer Copilot den ene bankkontoutdragslinjen med flere fakturaposter.

- Foreslåtte finanskonti

    For gjenværende banktransaksjoner som ikke kunne samsvares med noen poster, bruker Copilot KI-teknologi til å sammenligne transaksjonsbeskrivelsen med finanskontonavn og foreslår deretter den mest sannsynlige finanskontoen å bokføre til. Hvis transaksjoner uten avstemming har informasjonen *Drivstoffstopp 24*, kan Copilot foreslå at du bokfører dem på *Transport*-kontoen.

Copilot kobler seg ikke til banken din for å hente eller sende transaksjoner. Denne oppgaven forblir helt innenfor din kontroll. Den er en forutsetning for å begynne å bruke Copilot-assistansen, enten transaksjonene legges til [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av en digital bankforbindelse, importeres fra en bankkontoutdragsfil eller angis manuelt.

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Hva er den tiltenkte bruken av bankavstemmingshjelp?

Hjelp til bankkontoavstemming er utformet for å forbedre nøyaktigheten i postene ved å hjelpe kunder med å identifisere nye transaksjoner som de bør gjøre rede for i [!INCLUDE[prod_short](includes/prod_short.md)]. Det aktiviteten er ikke ment for å oppdage svindel eller identifisere om kunder har betalt i tide.

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan ble bankavstemmingshjelp evaluert? Hvilke målinger brukes til å måle ytelse?

Bankkontoavstemmingshjelpen ble testet ved hjelp av kombinasjoner av syntetiske banktransaksjonsdata og lignende finanskontoer og poster som dekker vanlige variasjoner og datagrenser for hvert felt og på forskjellige språk. Testdata representerer både typisk bruk og bruk av dårlige aktører. Ytelse ble målt i forhold til manuell avstemming av de samme dataene.

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-these-limitations-when-they-use-the-system"></a>Hva er begrensningene til bankavstemmingshjelpen? Hvordan kan brukere minimere virkningen av disse begrensningene når de bruker systemet?

Bankkontoavstemmingshjelp fungerer best når finanskontonavn, postbeskrivelser og banktransaksjonsbeskrivelser er på samme språk. Blandede språk eller blandet språk i transaksjonsbeskrivelser resulterer ofte i færre treff og forslag.

Foreslåtte finanskonti fungerer best på ett av språkene som støttes (se neste del for en liste over språk). Brukere kan oppleve færre transaksjonstreff og færre foreslåtte finanskontoer på andre språk.

## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>I hvilke geografiske områder og på hvilke språk er bankavstemmingshjelp tilgjengelig?

- Tilgjengelige geografiske områder

  Bankkontoavstemmingshjelpen er tilgjengelig i alle støttede [land/områder i Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). For kundemiljøer i land/områder der Azure OpenAI-tjenesten ikke er tatt i bruk, må administratorer samtykke til å tillate flytting av dataene over grenser for at [!INCLUDE [prod_short](includes/prod_short.md)] skal koble til Azure OpenAI-tjenesten. Finn ut mer på [Copilot-dataflytting på tvers av geografiske områder](ai-copilot-data-movement.md).

- Tilgjengelige språk

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Hvis du vil ha mer informasjon om språk, kan du se forrige spørsmål om begrensninger.

## <a name="what-is-expected-of-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Hva forventes av systembrukere når de bruker bankkontoavstemmingshjelpen?

### <a name="during-bank-account-reconciliation"></a>Under en bankkontoavstemming

KI-drevne treff og forslag kan noen ganger være feil eller ufullstendige. Brukere av bankkontoavstemmingshjelpen må gjennomgå nøyaktigheten av treffene og forslagene fra Copilot før de velger å beholde dem. Copilots treff og forslag lagres ikke i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen før du velger **Behold den**-knappen og lukker Copilot-vinduet. Du kan redigere og korrigere eventuelle treff eller forslag før du velger å beholde dem.

### <a name="after-bank-account-reconciliation-is-completed"></a>Etter at bankkontoavstemming er fullført

Vi anbefaler at brukerne også kontrollerer nøyaktigheten og retter opp eventuelle avvik etter at de har lukket Copilot-vinduet. Denne prosessen bør omfatte følgende aktiviteter:

- Se gjennom avstemmingstestrapporten.
- Sørg for at organisasjonen har de riktige gjennomgangs- og revisjonsprosessene på plass.
- Åpne eventuelle bokførte avstemminger på nytt ved hjelp av **Angre**-funksjonen.
- Korriger eventuelle feilaktige poster gjennom omvendt bokføring av poster.

## <a name="what-is-expected-of-administrators-and-system-users-when-they-operate-bank-account-reconciliation-assist"></a>Hva forventes av administratorer og systembrukere når de bruker bankkontoavstemmingshjelpen?

Systembrukere, for eksempel regnskapsførere, kasserere eller andre som jobber med forretningsregnskap, bør alltid vurdere nøyaktigheten av samsvar og forslag fra Copilot før de velger å beholde dem. Etter avstemming med Copilot anbefaler vi at disse brukerne går gjennom avstemmingstestrapporten for å bekrefte nøyaktigheten og identifisere eventuelle avvik.

Administratorer bør sørge for at de riktige regnskapsbrukerne har fått tilgang til denne funksjonen.

## <a name="is-copilot-the-only-means-of-completing-bank-account-reconciliation"></a>Er Copilot den eneste måten å fullføre bankkontoavstemming på?

Nr. Bruk av Copilot er valgfritt. [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr tradisjonelle, ikke-KI-drevne metoder for import av bankkontoutdrag, kjøring av forhåndsdefinerte samsvarsregler og manuell bruk av treff og bokføring på aktuelle finanskontoer. Både den tradisjonelle tilnærmingen og Copilot kan brukes samtidig i en organisasjon.

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvordan gir jeg tilbakemelding om KI-generert innhold?

Hver gang Copilot gir treff eller forslag, kan du gi tilbakemelding til Microsoft direkte fra Copilot-vinduet, ved hjelp av Liker- (tommel opp) og Liker ikke-kontrollene (tommel ned). Din tilbakemelding er anonym, og vi bruker disse dataene til å forbedre kvaliteten på tjenesten.

## <a name="see-also"></a>Se også

[Avstemme bankkontoer med Copilot (forhåndsversjon)](bank-reconciliation-with-copilot.md)
