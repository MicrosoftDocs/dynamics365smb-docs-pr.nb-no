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

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a><a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a>Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Denne artikkelen bruker spørsmål og svar for å forklare viktige forhold om KI-teknologien bak Copilot og teksten den genererer.

## [Generelt](#tab/general)

### <a name="what-is-copilot"></a><a name="what-is-copilot"></a>Hva er Copilot?

Copilot inneholder tekstforslag genererte med kunstig intelligens for varer i Business Central. Det er ment for brukere som skriver markedsføringstekst for varer, slik at de kan produsere engasjerende og overbevisende innhold. Noen av de viktigste fordelene omfatter:

- Reduserer tiden som brukes på kopiskriving, noe som kan øke leveringstiden for varer som selges i nettbutikker.
- Låser opp kreativitet for å gi mer engasjerende produktbeskrivelser.
- Forbedrer konsekvensen i markedsføringsmateriale for produktserier.

Brukere bør vurdere teksten generert med kunstig intelligens som et forslag som må gjennomgås og redigeres for nøyaktighet før den er offentlig tilgjengelig.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a><a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a>Hvorfor er ikke Copilot tilgjengelig for markedsføringstekst på varene mine i Business Central?

Følgende forutsetninger må være oppfylt for at Copilot skal være tilgjengelig:

- Språket du bruker i Business Central må være engelsk. Alle tilgjengelige engelske nasjonale innstillinger fungerer, for eksempel engelsk (USA), engelsk (Storbritannia) eller engelsk (Sør-Afrika).

  Hvis du vil endre språket, velger du **Innstillinger**-ikonet øverst til venstre ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") > **Mine innstillinger** > **Språk**. Hvis du vil ha mer informasjon, kan du gå til [Endre grunnleggende innstillinger](ui-change-basic-settings.md#language).
- Du må bruke Business Central Online, versjon 22 eller nyere (hvis du er eksisterende kunde) eller en prøveversjon.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Hvis du vil kontrollere versjonen, merker du spørsmålstegnet øverst til høyre og velger deretter **Hjelp og kundestøtte**. Se etter programversjonen under **Feilsøking**. Hvis du vil ha mer informasjon om hvordan du får den riktige forhåndsversjonen, går du til [Kom i gang med en Business Central-forhåndsversjon](ai-preview-getstarted.md).
- Funksjonen **Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot** må være aktivert.

   Hvis du vil ha mer informasjon, kan du gå til [Aktiver eller deaktiver funksjonen Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- En administrator har samtykket i vilkårene.

   Hvis du vil ha mer informasjon, går du til [Samtykk i eller avvis vilkårene for forhåndsversjon og personvern for alle brukere](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises"></a><a name="is-copilot-available-for-preview-in-business-central-on-premises"></a>Er Copilot tilgjengelig for forhåndsversjon i Business Central lokalt?

Nei, dette støttes for øyeblikket ikke i Business Central lokalt.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a><a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a>Hvordan fungerer Copilot, hvor kommer den foreslåtte teksten fra?

Copilot bruker [Microsofts Azure OpenAI-tjeneste](/azure/cognitive-services/openai/overview) til å få tilgang til kraftige språkmodeller som analyserer og genererer naturlig språk. Disse modellene er kalibrert på et bredt datasett med brødtekst. Resultatet er at Copilot kan generere foreslåtte, personlige svar på engelske basert minimal mengde inndata, for eksempel en vares attributter, kategori eller beskrivelse. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot"></a><a name="whats-the-quality-of-the-text-suggested-by-copilot"></a>Hva er kvaliteten på teksten som blir foreslått av Copilot?

Siden den underliggende teknologien bak Copilot bruker kunstig intelligens som er kalibrert i et stort utvalg av kilder, er ikke det genererte innholdet alltid fakta eller passende. Noen forslag kan også omfatte tvilsomt eller upassende innhold. Det er ditt ansvar å gå gjennom og redigere genererte forslag for å sikre at det er nøyaktig og relevant.

Hvis du vil ha informasjon om upassende forslag, kan du gå til [Hva gjøres med grove og skadelige tekstforslag?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a><a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a>Hvordan kan jeg forbedre forslagene jeg får fra Copilot?

Det er et par ting du kan gjøre for å få mest mulig utbytte forslag fra Copilot:

- Legg til flere attributter i en vare for å forfremme bestemte funksjoner og egenskaper du er interessert i.
- Endre alternativene for ordlyd og fremhev kvalitet som tilsvarer dine personlige innstillinger.
- Forbedre varens beskrivelse.
- Kontroller at varen er tildelt den mest egnede kategorien.

Hvis du vil ha mer informasjon, kan du til [Forbedre og skreddersy tekstforslag](item-marketing-text.md#improve-and-tailor-text-suggestions).

### <a name="what-if-im-not-satisfied-with-the-generated-text"></a><a name="what-if-im-not-satisfied-with-the-generated-text"></a>Hva om jeg ikke er fornøyd med den genererte teksten?

Velg **Er dette et godt forslag?** for å hjelpe oss med å forbedre teksten på siden **Opprett med Copilot**, som du kan svare med tommel opp (jeg liker det) eller tommel ned (trenger forbedring).

![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how"></a><a name="can-admins-disable-copilot-if-so-how"></a>Kan administratorer deaktivere Copilot? Hvis det er tilfellet, hvordan?

Business Central tilbyr administratorer to måter å deaktivere Copilot på i forhåndsversjon:

- Ikke samtykke til personvernerklæringen til Azure OpenAI for alle brukere.

  eller

- Deaktiver funksjonen **Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot** på siden for **Funksjonsstyring**.

Hvis du vil ha mer informasjon, kan du gå til [Konfigurere varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot som administrator](enable-ai.md).

## [Riktighet](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english"></a><a name="does-copilot-work-with-languages-other-than-english"></a>Fungerer Copilot med andre språk enn engelsk?

For øyeblikket støtter Copilot bare engelsk. Unøyaktige svar kan bli gitt når brukere snakker med systemet på andre språk enn engelsk.

## [Menneskelig oversikt](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions"></a><a name="whats-done-about-abusive-and-harmful-text-suggestions"></a>Hva gjøres i forbindelse med grove og skadelige tekstforslag?

Azure OpenAI-tjenesten lagrer ledetekster og fullføringer fra tjenesten som skal overvåkes for krenkende bruk, og til å utvikle og forbedre kvaliteten på Azure OpenAIs innholdsbehandlingssystemer. [Finn ut mer om innholdsadministrasjon og filtrering.](/azure/cognitive-services/openai/concepts/content-filter)

Godkjente Microsoft-ansatte kan få tilgang til ledetekst- og fullføringsdata som har utløst automatiserte systemer med formål om å undersøke og kontrollere potensiell misbruk. For kunder som har distribuert Azure OpenAI-tjenesten i EU, vil de godkjente Microsoft-ansatte være plassert i EU. Disse dataene kan brukes til å forbedre systemene for innholdsbehandling. Hvis et policybrudd er bekreftet, kan vi be deg om å utføre en umiddelbar handling for å løse problemet for å unngå ytterligere misbruk. Hvis problemet ikke løses, kan det føre til utestengelse eller avslutning av Azure OpenAI-ressurstilgang.

Hvis du vil ha mer informasjon, kan du se [Data, personvern og sikkerhet for Azure OpenAI-tjenesten](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process"></a><a name="can-i-opt-out-of-the-logging-and-human-review-process"></a>Kan jeg velge bort loggingen og prosessen for menneskelig gjennomgang?

Som en del av å tilby forhåndsversjonen av Azure OpenAI, vil Microsoft behandle og lagre kundedata som sendes til tjenesten, i tillegg til et utdatainnhold, for eksempel til overvåking for og hindring av krenkende eller skadelig bruk av tjenesten, og til utvikling, testing og forbedring av funksjoner som er utviklet for å hindre grove bruk av eller skadelige utdata fra tjenesten. 

Godkjent Microsoft-personell kan gå gjennom data som har utløst de automatiserte systemene, for å undersøke og bekrefte potensielle misbruk, og det kan føre til begrenset vilkårlig utvalg av termer som ikke rapporteres av de automatiserte systemene, for å sikre at systemene fungerer Godkjent Microsoft-personell kan også få tilgang til og bruke disse dataene til å forbedre systemene som overvåker og forhindrer eller skadelig bruk eller utdata fra tjenesten. Les mer om [vilkår for forhåndsversjon](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Personvern](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a><a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Hvilke data samler funksjonen inn? Hvordan brukes dataene?

Funksjonen samler inn svaret ditt på spørsmålet **Er dette et godt forslag?** på siden **Opprett med Copilot**, som enten kan være tommel opp (jeg liker det) eller tommel ned (trenger forbedring).

Vi bruker disse dataene til å evaluere og forbedre kvaliteten på funksjonen. Du finner mer informasjon om hvilke data som samles inn, i [vilkårene for forhåndsversjonen](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also"></a><a name="see-also"></a>Se også

[Oversikt over varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-overview.md)  
[Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot som administrator](enable-ai.md)  
[Opprett markedsføringstekst til varer ved hjelp av Copilot](item-marketing-text.md)  

