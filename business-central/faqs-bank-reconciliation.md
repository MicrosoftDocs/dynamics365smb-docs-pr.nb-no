---
title: Vanlige spørsmål om bankkontoavstemmingshjelp (forhåndsversjon) med Copilot
description: 'Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes til å avstemme bankkontoer og kontoutdrag i Business Central. De omfatter viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den er testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 11/07/2023
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

# <a name="faq-for-bank-account-reconciliation-assist-preview-with-copilot"></a>Vanlige spørsmål om bankkontoavstemmingshjelp (forhåndsversjon) med Copilot

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Disse vanlige spørsmålene beskriver KI-effekten av Copilot-hjelp med bankkontoavstemming i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-bank-reconciliation-assist"></a>Hva er bankkontoavstemmingshjelp?

Bankavstemming er en vanlig regnskapsoppgave der organisasjoner går gjennom bankkontoutdragene for å identifisere transaksjoner som skal registreres i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne oppgaven vil for eksempel bli brukt til å identifisere periodiske bankgebyrer eller små ansattutgifter. Denne oppgaven er vanligvis en flertrinnsprosess, som starter med å importere bankkontoutdrag til [!INCLUDE[prod_short](includes/prod_short.md)], etterfulgt av samsvarende transaksjoner med poster, og bokføring av nye poster for å gjenspeile eventuelle gjenværende transaksjoner som ikke tidligere var kjent i postene. Copilot i [!INCLUDE[prod_short](includes/prod_short.md)] reduserer manuelt arbeid ved å matche flere transaksjoner og foreslå finanskonti du kan bokføre til. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Hva er funksjonene til bankavstemmingshjelpen?

Copilot gir KI-drevet assistanse med to forskjellige oppgaver: 

- Forbedret samsvaring av transaksjoner med poster 

   [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr automatiserte regler som automatisk samsvarer mange banktransaksjoner med poster. Disse reglene er imidlertid lite fleksible og resulterer ofte i mange transaksjoner uten samsvar som hver krever manuell inspeksjon og sammenligning. Copilot bruker KI-teknologi til å inspisere gjenværende transaksjoner og identifisere flere treff basert på datoer, beløp og beskrivelser. Hvis for eksempel flere fakturaer ble betalt som ett engangsbeløp av en kunde, avstemmer Copilot den ene bankkontoutdragslinjen med flere fakturaposter. 
 
- Foreslåtte finanskontoer 

   For gjenværende banktransaksjoner som ikke kunne samsvares med noen poster, bruker Copilot KI-teknologi til å sammenligne transaksjonsbeskrivelsen med finanskontonavn og foreslår den mest sannsynlige finanskontoen å bokføre til. Copilot kan for eksempel foreslå at transaksjonen med informasjonen «Drivstoffstopp 24» bokføres til «Transport»-kontoen. 

Copilot kobler seg ikke til banken din for å hente eller sende transaksjoner. Denne oppgaven er helt innenfor din kontroll og er en forutsetning for å begynne å bruke Copilot-assistansen, enten disse transaksjonene legges til [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av en digital bankforbindelse, importeres fra en bankkontoutdragsfil eller angis manuelt. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Hva er den tiltenkte bruken av bankavstemmingshjelp?

Hjelp til bankkontoavstemming er utformet for å bidra til å identifisere nye transaksjoner som kunder bør gjøre rede for [!INCLUDE[prod_short](includes/prod_short.md)], slik at de kan forbedre nøyaktigheten i postene. Denne aktiviteten er ikke ment for å oppdage svindel eller identifisere om kunder har betalt i tide.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan ble bankavstemmingshjelp evaluert? Hvilke målinger brukes til å måle ytelse?

Denne funksjonaliteten ble testet ved hjelp av kombinasjoner av syntetiske banktransaksjonsdata og lignende finanskontoer og poster som dekker vanlige variasjoner og datagrenser for hvert felt og på forskjellige språk. Testdata representerer både typisk bruk og bruk av dårlige aktører. Ytelse ble målt i forhold til manuell avstemming av de samme dataene. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Hva er begrensningene til bankavstemmingshjelpen? Hvordan kan brukere minimere virkningen av bankavstemmingsbegrensninger når de bruker systemet?

Bankkontoavstemmingshjelp fungerer best når finanskontonavn, postbeskrivelser og banktransaksjonsbeskrivelser er på samme språk. Blandede språk eller blandet språk i transaksjonsbeskrivelser resulterer ofte i færre treff og forslag. 

Foreslåtte finanskonti fungerer best på engelsk. Selv om denne funksjonen kan brukes på hvilket som helst av de tilgjengelige [!INCLUDE[prod_short](includes/prod_short.md)]-språkene, kan brukere oppleve færre transaksjonstreff og færre foreslåtte finanskontoer på andre språk. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>I hvilke geografiske områder og på hvilke språk er bankavstemmingshjelp tilgjengelig?

Denne funksjonen er tilgjengelig for alle land-/områdemiljøer og på alle brukerspråk. For kundemiljøer i land/områder der Azure OpenAI-tjenesten ikke er tatt i bruk, må administratorer først samtykke til å tillate flytting av data over grenser for at [!INCLUDE[prod_short](includes/prod_short.md)] skal koble til Azure OpenAI-tjenesten og for at denne funksjonen skal være tilgjengelig. 

Hvis du vil ha mer informasjon om språk, kan du se forrige spørsmål om begrensninger.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Hva forventes av sluttbrukere når de bruker bankkontoavstemmingshjelpen?

### <a name="while-using-bank-account-reconciliation"></a>Under bruk av bankkontoavstemming

KI-drevne treff og forslag kan noen ganger være feil eller ufullstendige. Brukere av bankkontoavstemmingshjelpen må gjennomgå nøyaktigheten av treff og forslag fra Copilot før de velger å beholde dem. Copilots treff og forslag lagres ikke i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen før du velger Behold den-knappen og går ut av Copilot-vinduet. Du kan også redigere og korrigere eventuelle treff eller forslag før du velger å beholde det. 

### <a name="after-completing-bank-account-reconciliation"></a>Etter at bankkontoavstemming er fullført

Det anbefales at brukerne også kontrollerer nøyaktigheten og retter opp eventuelle avvik etter å ha gått ut av Copilot-vinduet, inkludert følgende aktiviteter: 

- Se gjennom avstemmingstestrapporten. 
- Sørg for at organisasjonen har de riktige gjennomgangs- og revisjonsprosessene på plass. 
- Åpne eventuelle bokførte avstemminger på nytt ved hjelp av Angre-funksjonen. 
- Korriger eventuelle feilaktige poster gjennom omvendt bokføring av poster. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Hva forventes av administratorer og sluttbrukere når de bruker bankkontoavstemmingshjelpen?

Sluttbrukere, for eksempel regnskapsførere, kasserere eller andre som jobber med forretningsregnskap, bør alltid vurdere nøyaktigheten av samsvar og forslag fra Copilot før de velger å beholde dem. Når du har avstemt med Copilot, anbefaler vi at du går gjennom avstemmingstestrapporten for å bekrefte nøyaktigheten og identifisere eventuelle avvik. 

Administratorer bør sørge for at de riktige regnskapsbrukerne har fått tilgang til denne funksjonen. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Er Copilot den eneste måten å fullføre bankkontoavstemming på?

Nei – bruk av Copilot er valgfritt. [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr tradisjonelle, ikke-KI-drevne metoder for import av bankkontoutdrag, kjøring av forhåndsdefinerte samsvarsregler og manuell bruk av treff og bokføring på aktuelle finanskontoer. Både den tradisjonelle tilnærmingen og Copilot kan brukes samtidig i en organisasjon. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvordan gir jeg tilbakemelding om KI-generert innhold?

Hver gang Copilot gir treff eller forslag, kan du gi tilbakemelding til Microsoft direkte fra Copilot-vinduet, ved hjelp av liker- og misliker-kontrollene. Din tilbakemelding er anonym, og vi bruker disse dataene til å forbedre kvaliteten på tjenesten.


## <a name="see-also"></a>Se også

[Avstemme bankkontoer ved hjelp av bankkontoavstemmingshjelpen (forhåndsversjon)](bank-reconciliation-with-copilot.md)
