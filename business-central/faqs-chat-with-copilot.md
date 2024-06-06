---
title: Vanlige spørsmål om ansvarlig kunstig intelligens for nettprat med Copilot (forhåndsversjon)
description: 'Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes for nettprat med Copilot i Business Central. De omfatter viktige vurderinger og detaljer om hvordan kunstig intelligens brukes, hvordan den er testet og evaluert, og eventuelle spesifikke begrensninger.'
ms.date: 03/18/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# <a name="responsible-ai-faq-for-chat-with-copilot-preview"></a>Vanlige spørsmål om ansvarlig kunstig intelligens for nettprat med Copilot (forhåndsversjon)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for Nettprat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du har generelle spørsmål om bruk av funksjonen, kan du gå til [Vanlige spørsmål om nettprat med Copilot](chat-with-copilot-faq.md).

## <a name="what-is-chat-with-copilot"></a>Hva er Nettprat med Copilot?

Microsoft Copilot er den KI-drevne assistenten som hjelper til med å stimulere kreativiteten, øke produktiviteten og eliminere kjedelige oppgaver. Du kan nettprate med Copilot i Business Central for å svare på spørsmål og finne forretningsdata ved å uttrykke det du leter etter på naturlig språk.

Nettprat med Copilot, også kalt chat, er en interaktiv funksjon som svarer på spørsmål og finner forretningsdata relatert til [!INCLUDE[prod_short](includes/prod_short.md)], uten at brukerne trenger å navigere i brukergrensesnittet eller produktdokumentasjonen. Copilot-ruten er tilgjengelig fra hvor som helst i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten.

Brukere stiller spørsmål på naturlig språk, som «Hvordan leverer jeg varer til kundene mine direkte fra leverandørene mine?» Eller «Har vi noen kontorstoler på lager for under $ 600?» Som svar gir Copilot svar på naturlig språk. Avhengig av spørsmålene kan svarene inneholde ren tekst, koblinger til poster eller sider i [!INCLUDE[prod_short](includes/prod_short.md)] og koblinger til [!INCLUDE[prod_short](includes/prod_short.md)]-hjelpeartikler på Microsoft Learn.

## <a name="what-are-capabilities-of-chat-with-copilot"></a>Hva er mulighetene i Nettprat med Copilot?

Du kan nettprate med Copilot for å få svar på følgende spørsmål:

### <a name="explain-and-guide"></a>Forklar og veiled

Brukere kan be Copilot om å forklare et spesifikt konsept relatert til [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel hva som er dimensjoner, eller gi veiledning om hvordan du fullfører en oppgave, for eksempel hvordan en ordre bokføres. Copilot søker i den offisielle [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentasjonen publisert av Microsoft og gir et svar basert på dokumentasjonen.

- Copilot bruker kunnskapen på Microsoft Learn (ikke et bredt nettsøk) til semantisk å søke bare i Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentasjon på Microsoft Learn.

- Copilot iverksetter ikke tiltak, oppretter ikke nye data eller endrer noen konfigurasjon. Den oppsummerer ganske enkelt alle avsnitt den finner på Microsoft Learn som samsvarer med spørsmålet eller spørringen i nettpraten.

### <a name="find-business-data-and-related-pages"></a>Finn forretningsdata og relaterte sider

Brukere kan be Copilot om å finne sider etter navn eller be om poster basert på felter og begrensninger. Hvis Copilot finner et treff, svarer den med en kobling til den relevante oppføringen eller siden, som brukeren deretter kan velge å åpne.

- Copilot konverterer inndataene på naturlig språk til en spørring som består av kriterier for tabellsøk, sortering og filtrering.

  Funksjonen bruker [!INCLUDE[prod_short](includes/prod_short.md)]s datasøkefunksjoner til å finne samsvarende data fra tabeller i selskapsdatabasen. Søket kjører under brukerens egen identitet for sikkerhet og samsvar. Den søker ikke utenfor [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.

- Copilot iverksetter ikke tiltak, oppretter ikke nye data eller endrer noen konfigurasjon. Den oppsummerer bare postene mottatt fra datasøket i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## <a name="what-is-the-intended-use-of-chat-with-copilot"></a>Hva er den tiltenkte bruken av Nettprat med Copilot?

Nettprat er utformet for bedriftsbruk og for å svare på spørsmål som gjelder [!INCLUDE[prod_short](includes/prod_short.md)] og forretningsdataene den inneholder. Funksjonen gir folk mulighet til å løse vanlige oppgaver som å finne poster eller få veiledning ved å uttrykke seg med egne ord, noe som gjør det enklere og mer tilgjengelig å jobbe med [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="how-was-chat-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan ble Nettprat med Copilot evaluert? Hvilke målinger brukes til å måle ytelse?

- Funksjonen gjennomgikk omfattende testing der mange engelskspråklige tekster som dekker et bredt spekter av emner og stiler for å uttrykke hensikt, ble gitt til Copilot. Resultatene ble evaluert mot nøyaktighet, relevans og sikkerhet.
- Funksjonen er bygget i samsvar med Microsoft-standarden for ansvarlig kunstig intelligens. [Finn ut mer om ansvarlig kunstig intelligens fra Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hvordan overvåker Microsoft kvaliteten på generert innhold?

Microsoft har ulike systemer på plass for å sikre at innhold som genereres av Copilot, er av høyeste kvalitet, oppdager misbruk og sørger for sikkerheten for kundene og dataene deres.

Brukere har mulighet til å gi tilbakemelding til alle Copilot-svar og rapportere unøyaktig eller upassende innhold for å hjelpe Microsoft med å forbedre denne funksjonen. 

- Du gir tilbakemelding ved å bruke ikonet for liker (tommel opp) eller misliker (tommel ned) i **Copilot**-ruten i [!INCLUDE[prod_short](includes/prod_short.md)].
- Vi analyserer og bruker tilbakemeldinger fra brukere om funksjonen for å hjelpe oss med å forbedre svarene.
- Hvis du støter på upassende generert innhold, rapporterer du det til Microsoft ved hjelp av dette tilbakemeldingsskjemaet: [Rapporter misbruk](https://go.microsoft.com/fwlink/?linkid=2249810).
- Microsoft kan deaktivere Copilot-drevne funksjoner for utvalgte kunder hvis det oppdages misbruk av funksjonaliteten.

## <a name="what-are-the-limitations-of-chat-with-copilot-how-can-users-minimize-the-impact-of-the-chat-with-copilot-limitations-when-using-the-system"></a>Hva er begrensningene for Nettprat med Copilot? Hvordan kan brukere minimere virkningen av begrensningene for Nettprat med Copilot når de bruker systemet?

- Generelle begrensninger for kunstig intelligens

  KI-systemer er verdifulle verktøy, men de er ikke-deterministiske. Innholdet de genererer, er kanskje ikke helt nøyaktig. Derfor er det viktig å bruke skjønn til å gjennomgå og verifisere svar fra Copilot før du tar beslutninger som kan påvirke interessenter som kunder og partnere. For de fleste svar vil Copilot også inkludere sitater eller referansekoblinger som du kan bruke til raskt å verifisere om Copilot har kommet til riktig svar. Når du for eksempel blir spurt om hvordan du utfører en oppgave, inkluderer Copilot koblinger til kildeartikkelen. Når Copilot blir bedt om å finne en oppføring basert på bestemte kriterier, inkluderer de koblinger som beskriver listesiden den identifiserte som samtaleemne, samt eventuelle filtre eller sortering som ble brukt for å komme frem til et svar.

- Språklige begrensninger

  - Nettprat støttes bare på engelsk for følgende nasjonale innstillinger: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Hvis visningsspråket i [!INCLUDE[prod_short](includes/prod_short.md)] ikke er et av disse stedene, er ikke nettpraten tilgjengelig.

  - Kvaliteten på svarene kan være lavere under følgende forhold:
    - Nasjonal innstilling for språk er noe annet enn en-US.
    - Når språkinnstillingen for brukeren i [!INCLUDE[prod_short](includes/prod_short.md)] er forskjellig fra hovedspråket for dataene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.

- Spesifikke bransje-, produkt- og emnebegrensninger

   Nettprat inkluderer innebygde sikkerhetsmekanismer som forhindrer uønsket generering av skadelig innhold, for eksempel seksuelt eksplisitt innhold eller oppfordring til vold. Noen ganger opererer kunder i bransjer, selger produkter og tjenester, eller arbeider med prosesser som naturlig overlapper med det som kan anses som upassende i andre sammenhenger, eller arbeider med data som kan utløse disse sikkerhetstiltakene. Nettprat fungerer kanskje ikke like bra i disse tilfellene.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## <a name="what-data-does-chat-with-copilot-collect-and-how-is-it-used"></a>Hvilke data samler Nettprat med Copilot inn, og hvordan brukes de

Microsoft bruker ikke selskapsdataene, inkludert teksten du sender til Copilot, til å lære opp grunnleggende modeller for kunstig intelligens til fordel for andre. Selskapsadministratorer har full kontroll til å styre disse dataene som er en del av Azure-abonnementet. Fordi administratorer eller andre i selskapet kan ha tilgang til disse dataene som bestemt av arbeidsgiveren din, anbefaler vi at brukerne ikke oppgir sensitive data som passord eller andre hemmeligheter.

## <a name="what-does-chat-with-copilot-offer-for-security"></a>Hva tilbyr Nettprat with Copilot for sikkerhet

Nettprat er utformet for å være sikker og kjøres under brukerens identitet og arver dermed alle sikkerhetstillatelser og andre begrensninger og opererer aldri utenfor [!INCLUDE[prod_short](includes/prod_short.md)]s plattformsikkerhet. Dette betyr at Copilot bare kan få tilgang til data som brukeren har tilgang til.

For brukere med SUPER-tillatelse kan nettprat lettere finne usikrede data som vanligvis er vanskeligere å komme til for andre brukere. Organisasjoner som ikke bruker [!INCLUDE[prod_short](includes/prod_short.md)]s sikkerhetsmodell til å begrense hvilke tabeller og objekter hver bruker eller brukerrolle har tilgang til, kan være utsatt for økt risiko ved bruk av nettprat. Derfor anbefaler vi at organisasjonen din enten implementerer [!INCLUDE[prod_short](includes/prod_short.md)]s sikkerhetsmodell eller deaktiverer nettprat.

## <a name="see-also"></a>Se også

[Nettprat med Copilot (forhåndsversjon)](chat-with-copilot.md)

