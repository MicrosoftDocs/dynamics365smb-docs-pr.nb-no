---
title: Oversikt over forslag til markedsføringstekst med Copilot
description: Få en oversikt over funksjonene for innholdsgenerering med kunstig intelligens i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# Oversikt over forslag til markedsføringstekst med Copilot

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Denne artikkelen gir en oversikt over funksjonene drevet av kunstig intelligens som leveres av Copilot i Business Central.

## Hva er varemarkedsføringstekst drevet av kunstig intelligens med Copilot

Copilot gir skrivehjelp drevet av kunstig intelligens Business Central-brukere som har ansvaret for å redigere markedsføringstekst (produktbeskrivelser) på varer solgt i nettbutikker som Shopify. Ved å klikke en knapp genererer Copilot tekst som er engasjerende og kreativ, og som fremhever attributtene for den bestemte varen. Med litt gjennomgang og redigering er den klar til publisering.

Copilot bruker [Microsoft Azure OpenAI-tjenesten](/azure/cognitive-services/openai/overview) til å få tilgang til språkmodeller som gjenkjenner, forutsier og genererer tekst som er basert på opplærte datasett.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Videoen gjenspeiler ikke nøyaktig hvordan funksjonen fungerer eller ser ut i produktet. Funksjonen har endret seg siden videoen ble produsert. Den gir deg likevel en generell idé om funksjonen og hva du kan bruke den til.*
  
## Hvor det brukes

Copilot er tilgjengelig på varekort i Business Central. I Business Central er varer som produkter i andre programmer og butikker. Hver vare kan behandles fra et kort der du angir opplysninger om varen, for eksempel dimensjonene, kostnaden eller bildet. Dette kortet inneholder også en boks for angivelse av markedsføringstekst. Denne markedsføringsteksten kan publiseres i nettbutikken for å promotere varen. Det er her Copilot kommer inn. Ved å velge handlingen **Opprett utkast med Copilot** på varekortet vil Copilot generere en intelligent utkasttekst for deg. Når du har fått det første utkastet, kan du kjøre Copilot flere ganger til du får et utkast du liker. Når du har et forslag du liker, går du gjennom og redigerer det for nøyaktighet og lagrer det.

Hvis Business Central er satt opp for å koble til nettbutikken på Shopify, kan du ta denne teksten enda lenger ved å publisere den med varen direkte i butikken ved å velge **Legg til i Shopify**.

## Hvorfor og hvordan du bruker den

Tekst generert med kunstig intelligens kan hjelpe deg med å fremskynde leveringstiden til produkter i nettbutikker ved å begrense tiden som brukes på kopiskriving. Noen av de viktigste fordelene omfatter:

- Hjelper brukere med å løse skriveblokkeringen ved å få dem i gang med et intelligent utkast.
- Låser opp kreativitet for å gi mer engasjerende produktbeskrivelser.
- Forbedrer konsekvensen i markedsføringsinnhold for produktserier.

Du bør vurdere teksten generert med kunstig intelligens som et *forslag bare*. Forslag kan i noen tilfeller inneholde feil og til og med upassende tekst, så det kreves menneskelig overstyring og gjennomgang. Før du gjør teksten offentlig tilgjengelig, må du kontrollere nøyaktigheten og gjøre nødvendige endringer.

## Gjeldende begrensninger

Denne delen forklarer nåværende begrensninger for tekst generert av kunstig intelligens levert av Copilot.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Dårlige forslag kan oppstå når vage eller generelle produktnavn brukes, og informasjon mangler om en vare, som nøkkelattributter eller en kategori.
- Copilot støttes bare av Business Central Online, ikke i produksjonsmiljøer eller Business Central on-premises-miljøer.
- Copilot støttes ikke gjennom tilkoblinger til din egen Azure OpenAI-tjenesteressurs i Azure-abonnementet.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## Neste trinn

For å komme i gang trenger du et Business Central-miljø (v23.1 og senere) som er aktivert med Copilot.

- Hvis du er en eksisterende Business Central-kunde, må Business Central-administratoren sette opp et miljø som er aktivert for markedsføringstekstforslag. Hvis du vil ha mer informasjon, kan du gå til [Konfigurere Copilot- og KI-funksjoner](enable-ai.md).

- Hvis du ikke er Business Central-kunde, men ønsker å prøve det, kan du registrerer du deg for en prøveversjon. Hvis du vil ha mer informasjon, kan du gå til [Registrer deg for en Dynamics 365 Business Central-prøveversjon](trial-signup.md).

Når du har et miljø eller en bane som er klar, går du til [Legge til markedsføringstekst i elementer med Copilot](item-marketing-text.md).  

## Se også

[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)  
[Legge til markedsføringstekst i elementer med Copilot](item-marketing-text.md)  
[Vanlige spørsmål om forslag til markedsføringstekst](faqs-marketing-text.md)  
[Kom i gang med Shopify-koblingen](shopify/get-started.md)  
