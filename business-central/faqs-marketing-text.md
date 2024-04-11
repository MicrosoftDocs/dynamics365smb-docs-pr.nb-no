---
title: Vanlige spørsmål om markedsføringstekstforslag
description: 'Disse vanlige spørsmålene om ansvarlig kunstig intelligens gir informasjon om KI-teknologien som brukes i Business Central, sammen med viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den ble testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# Vanlige spørsmål om markedsføringstekstforslag med Copilot

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for funksjonen [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] i [!INCLUDE[prod_short](includes/prod_short.md)].

## Hva er forslag til varemarkedsføringstekst?

Copilot tilbyr skrivehjelp til brukere som er ansvarlige for å skrive markedsføringstekst (også kjent som kopi) på elementer i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funksjonen er kjent som [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-funksjonen tilbyr skrivehjelp til brukere som er ansvarlige for å skrive markedsføringstekst (også kjent som *kopi*) på elementer i [!INCLUDE[prod_short](includes/prod_short.md)].

Funksjonen er tilgjengelig på alle varekort i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil bruke det, åpner du bare et element og velger deretter **Markedsføringstekst** > **Opprett utkast med Copilot**. Denne handlingen genererer automatisk et tekstforslag som er engasjerende, kreativt og spesifikt for elementet som vises. Forslagene er basert på ulike inndata, inkludert:

- Varens attributter, kategori og navn.
- Innstillinger for personlig skrivestil, som ordlyd, fremhevet kvalitet, format og lengde.

Du kan endre verdien på disse inndatavalgene til å påvirke utfallet av teksten generert av kunstig intelligens. Før du lagrer et forslag, kan du enkelt se gjennom og redigere det for nøyaktighet eller prøve et annet forslag.

Noen viktige fordeler med denne funksjonen inkluderer:

- Reduserer tiden som brukes på kopiskriving, noe som kan øke leveringstiden for varer som selges i nettbutikker.
- Låser opp kreativitet for å gi mer engasjerende produktbeskrivelser.
- Forbedrer konsekvensen i markedsføringsmateriale for produktserier.

## Hvilke funksjoner har systemet?

[!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-funksjonen bruker [Microsofts Azure OpenAI-tjeneste](/azure/cognitive-services/openai/overview) til å få tilgang til kraftige språkmodeller som analyserer og genererer naturlig språk. Disse modellene er kalibrert på et bredt datasett med brødtekst. Resultatet er at Copilot kan generere foreslåtte, personlige svar på engelske basert minimal mengde inndata, for eksempel en vares attributter, kategori eller beskrivelse. 

## Hva er systemets tiltenkte bruk?

Denne funksjonen er ment å hjelpe brukere med å opprette markedsføringstekst for varer i [!INCLUDE[prod_short](includes/prod_short.md)]. Forfattere bruker funksjonen til raskt å få overbevisende og engasjerende tekstforslag, som deretter gjennomgås og redigeres for nøyaktighet. 

## Hvordan ble varemarkedsføringsteksten evaluert? Hvilke målinger brukes til å måle ytelse?

- Funksjonen har gjennomgått omfattende testing, der mange tekster på forskjellige språk er evaluert av språkeksperter mot ulike kriterier. Testingen var basert på [!INCLUDE[prod_short](includes/prod_short.md)]-demonstrasjonsdata og andre fiktive produktkataloger.
- Denne funksjonen er bygget i samsvar med Microsoft-standarden for ansvarlig kunstig intelligens. [Finn ut mer om ansvarlig kunstig intelligens fra Microsoft](https://aka.ms/RAI).

## Hvordan overvåker Microsoft kvaliteten på generert innhold?

Microsoft har ulike systemer på plass for å sikre at Copilot-funksjonene forblir operative og genererer innhold av høyeste kvalitet.

- Brukere har mulighet til å gi tilbakemelding for å rapportere upassende innhold og forbedre funksjonaliteten.

  - Hvis du støter på upassende generert innhold, rapporterer du det til Microsoft ved hjelp av dette tilbakemeldingsskjemaet: [Rapporter misbruk](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft kan deaktivere Copilot-drevne funksjoner for utvalgte kunder hvis det oppdages misbruk av funksjonaliteten. 

  - Vi sporer tilbakemeldinger fra brukere om [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] for å hjelpe oss med å forbedre forslag. 

    Du gir tilbakemelding ved å bruke ikonet for liker (tommel opp) eller misliker (tommel ned) på **Copilot**-siden [!INCLUDE[prod_short](includes/prod_short.md)]. Vi samler inn telemetrien til disse bevegelsene for hver KI-utdata du sender tilbakemelding for.

    ![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot-window-feedback.svg)

- Azure OpenAI-tjenesten lagrer ledetekster og fullføringer fra tjenesten som skal overvåkes for krenkende bruk, og til å utvikle og forbedre kvaliteten på Azure OpenAIs innholdsbehandlingssystemer. [Finn ut mer om innholdsadministrasjon og filtrering.](/azure/cognitive-services/openai/concepts/content-filter). Bedriftsdataene dine brukes ikke til å lære opp KI-modeller i Azure-tjenesten OpenAI.

   Godkjente Microsoft-ansatte kan få tilgang til ledetekst- og fullføringsdata som har utløst automatiserte systemer med formål om å undersøke og kontrollere potensiell misbruk. For kunder som bruker [!INCLUDE[prod_short](includes/prod_short.md)] i EU, vil de godkjente Microsoft-ansatte være plassert i EU. Disse dataene kan brukes til å forbedre systemene for innholdsbehandling. Hvis et policybrudd er bekreftet, kan vi be deg om å utføre en umiddelbar handling for å løse problemet for å unngå ytterligere misbruk. Hvis problemet ikke løses, kan det føre til utestengelse eller avslutning av Azure OpenAI-ressurstilgang.

   Hvis du vil ha mer informasjon, kan du se [Data, personvern og sikkerhet for Azure OpenAI-tjenesten](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## Finnes det en loggførings- og manuell gjennomgangsprosess som en del av Azure OpenAI Service, og kan jeg i så fall melde meg ut?  

Som en del av å tilby forhåndsversjonen av Azure OpenAI-tjenesten, vil Microsoft behandle og lagre kundedata som sendes til tjenesten, i tillegg til et utdatainnhold, for eksempel til overvåking for og hindring av krenkende eller skadelig bruk av tjenesten, og til utvikling, testing og forbedring av funksjoner som er utviklet for å hindre grove bruk av eller skadelige utdata fra tjenesten. 

Godkjent Microsoft-personell kan gå gjennom data som har utløst de automatiserte systemene, for å undersøke og bekrefte potensielle misbruk, og det kan føre til begrenset vilkårlig utvalg av termer som ikke rapporteres av de automatiserte systemene, for å sikre at systemene fungerer Godkjent Microsoft-personell kan også få tilgang til og bruke disse dataene til å forbedre systemene som overvåker og forhindrer eller skadelig bruk eller utdata fra tjenesten. Les mer om [vilkår for forhåndsversjon](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

For at Microsoft skal kunne beskytte tjenesten og kundene, er det ikke mulig å reservere seg mot loggføring og prosesser for manuell gjennomgang.

## Hvilke data samler funksjonen inn? Hvordan brukes dataene?

Funksjonen for markedsføringstekstforslag samler inn minimumsdataene som kreves av Business Central for å tilby tjenesten. Hvis du vil ha mer informasjon, kan du se [Dynamics 365-vilkår for Azure OpenAI-drevne funksjoner](https://go.microsoft.com/fwlink/?linkid=2236010).

Funksjonen samler også inn data fra tilbakemeldingen brukeren kan gi ved hjelp av ikonene liker (tommel opp) eller misliker (tommel ned) øverst på **Copilot**-siden . Dataene er anonyme og inkluderer valgene liker eller misliker, misliker-grunnen hvis oppgitt, og Copilot-funksjonen tilbakemeldingen gjelder. Vi bruker disse dataene til å evaluere og forbedre kvaliteten på funksjonen.

## Hva er begrensningene for [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? Hvordan kan brukere minimere virkningen av [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]-begrensninger når de bruker systemet?

- Siden den underliggende teknologien bak funksjonen bruker kunstig intelligens som er kalibrert i et stort utvalg av kilder, er ikke det genererte innholdet alltid fakta eller passende. Noen forslag kan også omfatte tvilsomt eller upassende innhold. Det er ditt ansvar å gå gjennom og redigere genererte forslag for å sikre at det er nøyaktig og relevant.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Unøyaktige svar kan bli gitt når brukere samhandle med systemet på andre språk enn de støttede språkene. Det kan også genereres unøyaktig tekst når brukerens språk og primære dataspråk i databasen [!INCLUDE[prod_short](includes/prod_short.md)] ikke er identiske.

## Hvilke driftsfaktorer og innstillinger gjør at det går an å bruke systemet på en effektiv og ansvarlig måte?

Det er et par ting du kan gjøre for å få mest mulig utbytte av funksjonen:

- Legg til flere attributter i en vare for å forfremme bestemte funksjoner og egenskaper du er interessert i.
- Endre alternativene for ordlyd og fremhev kvalitet som tilsvarer dine personlige innstillinger.
- Forbedre varens beskrivelse.
- Kontroller at varen er tildelt den mest egnede kategorien.

Hvis du vil ha mer informasjon, kan du til [Forbedre og skreddersy tekstforslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Gå alltid gjennom forslagene for nøyaktighet før du lagrer dem og publiserer dem for offentlig forbruk.


## Se også

- [Forslag til markedsføringstekst](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]