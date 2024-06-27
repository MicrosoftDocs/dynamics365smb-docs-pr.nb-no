---
title: Vanlige spørsmål om analysehjelp (forhåndsversjon)
description: 'Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes for å analysere data på sider i Business Central. De omfatter viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den er testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 06/13/2024
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

# <a name="faq-for-analysis-assist-preview"></a>Vanlige spørsmål om analysehjelp (forhåndsversjon)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for analysehjelpfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-analysis-assist"></a>Hva er analysehjelp?

Analysehjelp er en kopilot som gir hjelp til å arbeide med [dataanalysemodusen](analysis-mode.md) i Business Central. Med dataanalysemodusen kan du organisere, samle og oppsummere data på sider og spørringer for å gjøre dem mer egnet til å analysere og trekke ut meningsfull innsikt. Med analysehjelp kan du automatisk konstruere visningen av dataene du vil analysere, ved å uttrykke behovene dine på et enkelt, naturlig språk, for eksempel «vis leverandører etter lokasjon sortert etter antall kjøp». Analysehjelp gjør det enklere å arbeide med data uten behov for komplekse tekniske ferdigheter.

## <a name="what-are-capabilities-of-analysis-assist"></a>Hva er funksjonene til analysehjelpen?

Analysehjelp bygger på utviklerverktøyene for Copilot i Business Central. Den bruker Azure OpenAI-tjensten til å konvertere ustrukturerte instruksjoner til en strukturert utforming for visning av data i analysemodus, uten å opprette, endre eller oppdatere selve kundeforretningsdataene.

## <a name="what-is-the-intended-use-of-analysis-assist"></a>Hva er den tiltenkte bruken av analysehjelp?

Analysehjelpen bidrar til å opprette analysefaner i dataanalysemodus for å presentere data på en måte som gjør det lettere å trekke konklusjoner. Det er imidlertid viktig å merke seg at analysehjelp ikke gir direkte innsikt eller konklusjoner om dataene. Det er et verktøy som hjelper brukere med å organisere og vise dataene sine. Det er opp til brukeren å trekke ut handlingsbar informasjon, oppdage trender og ta informerte beslutninger for å drive forretningsverdi.

## <a name="how-was-analysis-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan ble analysehjelp evaluert? Hvilke målinger brukes til å måle ytelse?

- Funksjonen gjennomgikk omfattende testingen basert på [!INCLUDE[prod_short](includes/prod_short.md)]s demonstrasjonsdata og andre fiktive produktkataloger. Copilot ble gitt mange spørringer på de støttede nasjonale innstillingene for engelsk. Spørringene dekket et bredt spekter av dataanalyseinstruksjoner og -stiler for å uttrykke hensikt. Resultatene ble evaluert mot nøyaktighet, relevans og sikkerhet.

- Funksjonen er bygget i samsvar med Microsoft-standarden for ansvarlig kunstig intelligens. [Finn ut mer om ansvarlig kunstig intelligens fra Microsoft.](https://aka.ms/RAI)

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hvordan overvåker Microsoft kvaliteten på generert innhold?

Microsoft har ulike systemer på plass for å sikre at innhold som genereres av Copilot, er av høyeste kvalitet, oppdager misbruk og sørger for sikkerheten for kundene og dataene deres.

Brukere har mulighet til å gi tilbakemelding til alle Copilot-svar og rapportere unøyaktig eller upassende innhold for å hjelpe Microsoft med å forbedre denne funksjonen.

- Hvis du støter på upassende generert innhold, rapporterer du det til Microsoft ved hjelp av dette tilbakemeldingsskjemaet: [Rapporter misbruk](https://go.microsoft.com/fwlink/?linkid=2249810)

- Vi analyserer tilbakemeldinger fra brukere om funksjonen og bruker den til å hjelpe oss med å forbedre svarene.

  Du gir tilbakemelding ved å bruke ikonet for liker (tommel opp) eller misliker (tommel ned) i **Copilot**-ruten i [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft kan deaktivere Copilot-drevne funksjoner for utvalgte kunder hvis det oppdages misbruk av funksjonaliteten.

## <a name="what-are-the-limitations-of-analysis-assist-how-can-users-minimize-the-impact-of-the-analysis-assist-limitations-when-using-the-system"></a>Hva er begrensningene til analysehjelpen? Hvordan kan brukere minimere virkningen av analysehjelpbegrensninger når de bruker systemet?

- Generelle begrensninger for kunstig intelligens:

  KI-systemer er verdifulle verktøy, men de er ikke-deterministiske. Innholdet de genererer, er kanskje ikke nøyaktig. Derfor er det viktig å bruke skjønn til å gjennomgå og verifisere svar før du tar beslutninger som kan påvirke interessenter som kunder og partnere.

- Tilgjengelige språk

   [!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

   Kvaliteten i svarene kan også være lavere hvis språkinnstillingen for brukeren i Business Central er forskjellig fra hovedspråket for forretningsdataene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.
  
- Geografisk begrensning:
  
   Funksjonen er tilgjengelig i alle støttede [land/områder i Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)<!-- except for Canada-->. Funksjonen bruker imidlertid Microsoft Azure OpenAI-tjenesten, som for øyeblikket er tilgjengelig for Business Central i enkelte geografiske områder. Hvis miljøet ditt befinner seg i et land/område der Azure OpenAI-tjenesten ikke er tilgjengelig, må administratorer tillate at data flyttes på tvers av geografiske områder. [Finn ut mer om Copilot-dataflytting på tvers av geografiske områder](/dynamics365/business-central/ai-copilot-data-movement).

- Visse bransje-, produkt- og emnebegrensninger:

  Organisasjoner som opererer i enkelte forretningsdomener, for eksempel medisinsk, narkotika, juridisk og våpen, kan oppleve lavere kvalitet på tjenesten.

## <a name="what-data-does-analysis-collect-and-how-is-it-used"></a>Hvilke data samler analyse inn, og hvordan brukes de?

Funksjonen for analysehjelp samler inn minimumsdataene som kreves av Business Central for å tilby tjenesten. Microsoft bruker ikke selskapsdataene, inkludert teksten du sender til Copilot, til å lære opp grunnleggende modeller til fordel for andre. Hvis du vil ha mer informasjon, kan du se [Dynamics 365-vilkår for Azure OpenAI-drevne funksjoner](https://go.microsoft.com/fwlink/?linkid=2236010).

Den samler også inn data fra tilbakemeldingen brukerne kan gi ved hjelp av ikonene liker (tommel opp) eller misliker (tommel ned) i analysehjelp på **Copilot**-siden. Dataene er anonyme og inkluderer valgene liker eller misliker, misliker-grunnen hvis oppgitt, og Copilot-funksjonen tilbakemeldingen gjelder.

## <a name="see-also"></a>Se også

[Analyser data med Copilot (forhåndsversjon)](analysis-assist.md)
