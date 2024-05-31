---
title: Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot
description: Få svar på vanlige spørsmål om tekstfunksjonene generert av kunstig intelligens med Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Denne artikkelen bruker spørsmål og svar for å forklare viktige forhold om KI-teknologien bak Copilot og teksten den genererer.

## [Generelt](#tab/general)

### Hva er Copilot?

Copilot inneholder tekstforslag genererte med kunstig intelligens for varer i Business Central. Det er ment for brukere som skriver markedsføringstekst for varer, slik at de kan produsere engasjerende og overbevisende innhold. Noen av de viktigste fordelene omfatter:

- Reduserer tiden som brukes på kopiskriving, noe som kan øke leveringstiden for varer som selges i nettbutikker.
- Låser opp kreativitet for å gi mer engasjerende produktbeskrivelser.
- Forbedrer konsekvensen i markedsføringsmateriale for produktserier.

Brukere bør vurdere teksten generert med kunstig intelligens som et forslag som må gjennomgås og redigeres for nøyaktighet før den er offentlig tilgjengelig.

### Hvorfor er ikke Copilot tilgjengelig for markedsføringstekst på varene mine i Business Central?

Følgende forutsetninger må være oppfylt for at Copilot skal være tilgjengelig:

- Språket du bruker i Business Central må være engelsk. Alle tilgjengelige engelske nasjonale innstillinger fungerer, for eksempel engelsk (USA), engelsk (Storbritannia) eller engelsk (Sør-Afrika).

  Hvis du vil endre språket, velger du **Innstillinger**-ikonet øverst til venstre ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") > **Mine innstillinger** > **Språk**. Hvis du vil ha mer informasjon, kan du gå til [Endre grunnleggende innstillinger](ui-change-basic-settings.md#language).
- Du må bruke Business Central Online, versjon 22 eller nyere (hvis du er eksisterende kunde) eller en prøveversjon.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Hvis du vil kontrollere versjonen, merker du spørsmålstegnet øverst til høyre og velger deretter **Hjelp og kundestøtte**. Se etter programversjonen under **Feilsøking**. Hvis du vil ha mer informasjon om hvordan du får den riktige forhåndsversjonen, går du til [Kom i gang med en Business Central-forhåndsversjon](ai-preview-getstarted.md).
- Funksjonen **Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot** må være aktivert.

   Hvis du vil ha mer informasjon, kan du gå til [Aktiver eller deaktiver funksjonen Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- En administrator har samtykket i vilkårene.

   Hvis du vil ha mer informasjon, går du til [Samtykk i eller avvis vilkårene for forhåndsversjon og personvern for alle brukere](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### Er Copilot tilgjengelig for forhåndsversjon i Business Central lokalt?

Nei, dette støttes for øyeblikket ikke i Business Central lokalt.

### Hvordan fungerer Copilot, hvor kommer den foreslåtte teksten fra?

Copilot bruker [Microsofts Azure-tjeneste OpenAI](/azure/cognitive-services/openai/overview) for å få tilgang til kraftige språkmodeller som analyserer og genererer naturlig språk. Disse modellene er kalibrert på et bredt datasett med brødtekst. Resultatet er at Copilot kan generere foreslåtte, personlige svar på engelske basert minimal mengde inndata, for eksempel en vares attributter, kategori eller beskrivelse. 

### Hva er kvaliteten på teksten som blir foreslått av Copilot?

Siden den underliggende teknologien bak Copilot bruker kunstig intelligens som er kalibrert i et stort utvalg av kilder, er ikke det genererte innholdet alltid fakta eller passende. Noen forslag kan også omfatte tvilsomt eller upassende innhold. Det er ditt ansvar å gå gjennom og redigere genererte forslag for å sikre at det er nøyaktig og relevant.

Hvis du vil ha informasjon om upassende forslag, kan du gå til [Hva gjøres med grove og skadelige tekstforslag?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Hvordan kan jeg forbedre forslagene jeg får fra Copilot?

Det er et par ting du kan gjøre for å få mest mulig utbytte forslag fra Copilot:

- Legg til flere attributter i en vare for å forfremme bestemte funksjoner og egenskaper du er interessert i.
- Endre alternativene for ordlyd og fremhev kvalitet som tilsvarer dine personlige innstillinger.
- Forbedre varens beskrivelse.
- Kontroller at varen er tildelt den mest egnede kategorien.

Hvis du vil ha mer informasjon, kan du til [Forbedre og skreddersy tekstforslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Hva om jeg ikke er fornøyd med den genererte teksten?

Velg **Er dette et godt forslag?** for å hjelpe oss med å forbedre teksten på siden **Opprett med Copilot**, som du kan svare med tommel opp (jeg liker det) eller tommel ned (trenger forbedring).

![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot-window-feedback.png)

### Kan administratorer deaktivere Copilot? Hvis det er tilfellet, hvordan?

Business Central tilbyr administratorer to måter å deaktivere Copilot på i forhåndsversjon:

- Godta personvernerklæringen for Azure OpenAI for alle brukere.

  eller

- Deaktiver funksjonen **Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot** på siden for **Funksjonsstyring**.

Hvis du vil ha mer informasjon, kan du gå til [Konfigurere varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot som administrator](enable-ai.md).

## [Riktighet](#tab/fairness)

### Fungerer Copilot med andre språk enn engelsk?

For øyeblikket støtter Copilot bare engelsk. Unøyaktige svar kan bli gitt når brukere snakker med systemet på andre språk enn engelsk.

## [Menneskelig oversikt](#tab/oversight)

### Hva gjøres i forbindelse med grove og skadelige tekstforslag?

Azure-tjenesten OpenAI lagrer meldinger og fullføringer fra tjenesten for å overvåke misbruk og for å utvikle og forbedre kvaliteten på Azures OpenAI innholdsstyringssystemer. [Finn ut mer om innholdsadministrasjon og filtrering.](/azure/cognitive-services/openai/concepts/content-filter)

Autoriserte Microsoft-ansatte kan få tilgang til dine hurtig- og fullføringsdata som har utløst de automatiserte systemene våre, for å undersøke og verifisere potensielt misbruk. for kunder som har distribuert Azure OpenAI Service i EU, vil de autoriserte Microsoft-ansatte være lokalisert i EU. Disse dataene kan brukes til å forbedre systemene for innholdsbehandling. Hvis et policybrudd er bekreftet, kan vi be deg om å utføre en umiddelbar handling for å løse problemet for å unngå ytterligere misbruk. Hvis problemet ikke løses, kan det føre til utestengelse eller avslutning av Azure OpenAI-ressurstilgang.

Hvis du vil ha mer informasjon, kan du se [Data, personvern og sikkerhet for Azure-tjenesten OpenAI](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### Kan jeg velge bort loggingen og prosessen for menneskelig gjennomgang?  

Som en del av å levere Azure-forhåndsversjonene OpenAI vil Microsoft behandle og lagre kundedata som sendes til tjenesten, samt utdatainnhold, for å overvåke og forhindre misbruk eller skadelig bruk eller utdata av tjenesten; og for å utvikle, teste og forbedre funksjoner som er utformet for å forhindre misbruk av eller skadelige utdata fra tjenesten. 

Godkjent Microsoft-personell kan gå gjennom data som har utløst de automatiserte systemene, for å undersøke og bekrefte potensielle misbruk, og det kan føre til begrenset vilkårlig utvalg av termer som ikke rapporteres av de automatiserte systemene, for å sikre at systemene fungerer Godkjent Microsoft-personell kan også få tilgang til og bruke disse dataene til å forbedre systemene som overvåker og forhindrer eller skadelig bruk eller utdata fra tjenesten. Les mer om [vilkår for forhåndsversjon](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Personvern](#tab/privacy)

### Hvilke data samler funksjonen inn? Hvordan brukes dataene?

Funksjonen samler inn svaret ditt på spørsmålet **Er dette et godt forslag?** på siden **Opprett med Copilot**, som enten kan være tommel opp (jeg liker det) eller tommel ned (trenger forbedring).

Vi bruker disse dataene til å evaluere og forbedre kvaliteten på funksjonen. Du finner mer informasjon om hvilke data som samles inn, i [vilkårene for forhåndsversjonen](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot-window-feedback.png)

---

## Se også

[Oversikt over varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-overview.md)  
[Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot som administrator](enable-ai.md)  
[Opprett markedsføringstekst til varer ved hjelp av Copilot](item-marketing-text.md)  

