---
title: Vanlige spørsmål om analysehjelp (forhåndsversjon)
description: 'Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes for å analysere data på sider i Business Central. De omfatter viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den er testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 02/13/2024
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

# Vanlige spørsmål om analysehjelp (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for analysehjelpfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Hva er analysehjelp?

Analysehjelp er en Copilot som gir hjelp til å arbeide med [dataanalysemodusen](analysis-mode.md) i Business Central. Med dataanalysemodusen kan du organisere, samle og oppsummere data på sider og spørringer for å gjøre dem mer egnet til å analysere og trekke ut meningsfull innsikt. Med analysehjelp kan du automatisk konstruere visningen av dataene du vil analysere, ved å uttrykke behovene dine på et enkelt, naturlig språk, for eksempel «vis leverandører etter lokasjon sortert etter antall kjøp». Analysehjelp gjør det enklere å arbeide med data uten behov for komplekse tekniske ferdigheter.

## Hva er funksjonene til analysehjelpen?

Analysehjelp bygger på utviklerverktøyene for Copilot i Business Central. Den bruker Azure OpenAI til å konvertere ustrukturerte instruksjoner til en strukturert utforming for visning av data i analysemodus, uten å opprette, endre eller oppdatere selve kundeforretningsdataene.

## Hva er den tiltenkte bruken av analysehjelp?

Den tiltenkte bruken av analysehjelp er å bidra til å opprette analysefaner i dataanalysemodus for å presentere data på en måte som gjør det lettere å trekke konklusjoner. Det er imidlertid viktig å merke seg at analysehjelp ikke gir direkte innsikt eller konklusjoner om dataene. Det er et verktøy som hjelper brukere med å organisere og vise dataene sine. Det er imidlertid opp til brukeren å trekke ut handlingsbar informasjon, oppdage trender og ta informerte beslutninger for å drive forretningsverdi.

## Hvordan ble analysehjelp evaluert? Hvilke målinger brukes til å måle ytelse?

- Funksjonen gjennomgikk omfattende testingen basert på [!INCLUDE[prod_short](includes/prod_short.md)]s demonstrasjonsdata og andre fiktive produktkataloger. Copilot ble gitt mange spørringer på de støttede nasjonale innstillingene for engelsk. Spørringene dekket et bredt spekter av dataanalyseinstruksjoner og -stiler for å uttrykke hensikt. Resultatene ble evaluert mot nøyaktighet, relevans og sikkerhet.

- Funksjonen er bygget i samsvar med Microsoft-standarden for ansvarlig kunstig intelligens. [Finn ut mer om ansvarlig kunstig intelligens fra Microsoft](https://aka.ms/RAI).

## Hvordan overvåker Microsoft kvaliteten på generert innhold?

Microsoft har ulike systemer på plass for å sikre at innhold som genereres av Copilot, er av høyeste kvalitet, oppdager misbruk og sørger for sikkerheten for kundene og dataene deres.

Brukere har mulighet til å gi tilbakemelding til alle Copilot-svar og rapportere unøyaktig eller upassende innhold for å hjelpe Microsoft med å forbedre denne funksjonen.

- Hvis du støter på upassende generert innhold, rapporterer du det til Microsoft ved hjelp av dette tilbakemeldingsskjemaet: [Rapporter misbruk](https://go.microsoft.com/fwlink/?linkid=2249810).

- Vi analyserer og bruker tilbakemeldinger fra brukere om funksjonen for å hjelpe oss med å forbedre svarene.

  Du gir tilbakemelding ved å bruke ikonet for liker (tommel opp) eller misliker (tommel ned) i **Copilot**-ruten i [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft kan deaktivere Copilot-drevne funksjoner for utvalgte kunder hvis det oppdages misbruk av funksjonaliteten.

## Hva er begrensningene til analysehjelpen? Hvordan kan brukere minimere virkningen av analysehjelpbegrensninger når de bruker systemet?

- Generelle begrensninger for kunstig intelligens

  KI-systemer er verdifulle verktøy, men de er ikke-deterministiske. Innholdet de genererer, er kanskje ikke nøyaktig. Derfor er det viktig å bruke skjønn til å gjennomgå og verifisere svar fra Copilot før du tar beslutninger som kan påvirke interessenter som kunder og partnere.

- Språk og geografiske begrensninger:

  - Analysehjelp støttes bare på engelsk for følgende nasjonale innstillinger: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Hvis visningsspråket i Business Central ikke er et av de oppførte nasjonale innstillingene, er ikke funksjonen tilgjengelig.

  - Kvaliteten på svarene kan være lavere hvis:
    - Nasjonal innstilling i Business Central for språk er noe annet enn en-US.
    - Språkinnstillingen for brukeren i Business Central er forskjellig fra hovedspråket for forretningsdataene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.
  
  - Geografisk begrensning:
  
    Funksjonen er tilgjengelig i alle støttede [Business Central-land/-områder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) bortsett fra Canada, på grunn av regelverket for språkoverholdelse Funksjonen bruker imidlertid Microsoft Azure OpenAI-tjenesten, som for øyeblikket er tilgjengelig for Business Central i enkelte geografiske områder. Hvis miljøet ditt befinner seg i et land/område der Azure OpenAI-tjenesten ikke er tilgjengelig, må administratorer tillate at data flyttes på tvers av geografiske områder. [Finn ut mer](/dynamics365/business-central/ai-copilot-data-movement).

- Visse bransje-, produkt- og emnebegrensninger:

  Organisasjoner som opererer i enkelte forretningsdomener, for eksempel medisinsk, narkotika, juridisk og våpen, kan oppleve lavere kvalitet på tjenesten.

## Hvilke data samler analyse inn, og hvordan brukes de

Funksjonen for analysehjelp samler inn minimumsdataene som kreves av Business Central for å tilby tjenesten. Microsoft bruker ikke selskapsdataene, inkludert teksten du sender til Copilot, til å lære opp grunnleggende modeller til fordel for andre. Hvis du vil ha mer informasjon, kan du se [Dynamics 365-vilkår for Azure OpenAI-drevne funksjoner](https://go.microsoft.com/fwlink/?linkid=2236010).

Den samler også inn data fra tilbakemeldingen brukerne kan gi ved hjelp av ikonene liker (tommel opp) eller misliker (tommel ned) i analysehjelp på **Copilot**-siden. Dataene er anonyme og inkluderer valgene liker eller misliker, misliker-grunnen hvis oppgitt, og Copilot-funksjonen tilbakemeldingen gjelder.

## Se også

[Analyser data med Copilot (forhåndsversjon)](analysis-assist.md)
