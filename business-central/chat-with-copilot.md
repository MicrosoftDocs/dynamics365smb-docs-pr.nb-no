---
title: Nettprat med Copilot (forhåndsversjon)
description: Lær hvordan du bruker nettprat med Copilot til å finne data og få hjelp i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/18/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Nettprat med Copilot (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Denne artikkelen forklarer hvordan du nettprater med Copilot for å få svar om selskapsdata og hjelp med oppgaver og emner relatert til Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Om nettprat med Copilot

Microsoft Copilot er den KI-drevne assistenten som hjelper til med å stimulere kreativiteten, øke produktiviteten og eliminere kjedelige oppgaver. Du kan nettprate med Copilot i Business Central for å svare på spørsmål og finne forretningsdata ved å uttrykke det du leter etter på naturlig språk. Du kan bruke nettpraten til følgende:

- Finn forretningsdata for selskapet du arbeider med i Business Central. Bruk nettprat til å slå opp (og åpne) data om enheter/poster relatert til forretningsprosesser, for eksempel kunder, leverandører, ordrer og varer med mer. Du kan for eksempel spørre Copilot: «Vis meg den siste ordren for Adatum.»
- Forklar et konsept eller få veiledning om hvordan du utfører en oppgave. Spør for eksempel «Hjelp meg å forstå dimensjoner» eller «Hvordan bokfører jeg en ordre».
- Forstå formålet med og typisk bruk av enkeltfelter. Når du velger **Spør Copilot** i et verktøytips for et felt, åpnes nettpraten med en Forklar-ledetekst for feltnavnet, og Copilot gir informasjon om det. Copilot lenker til artiklene det refereres til, så det er enkelt å verifisere beskrivelsen.

  Svarene som Copilot gir, er utelukkende basert på den offisielle Dynamics 365 Business Central-dokumentasjonen, som er tilgjengelig på Microsoft Learn under [Dynamics 365 Business Central-dokumentasjon](/dynamics365/business-central/).

Nettprat med Copilot omgår behovet for å navigere i brukergrensesnittet eller produkthjelpen, noe som kan spare tid og øke produktiviteten.
  
> [Se video](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Forutsetninger

- Nettprat med Copilot-funksjonen er aktivert. Denne oppgaven utføres av en administrator. [Finn ut mer om konfigurering av Copilot- og KI-funksjoner](enable-ai.md).
- Visningsspråket i Business Central er satt til et av følgende nasjonale innstillinger på engelsk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Finn ut mer om hvordan du endrer språket](ui-change-basic-settings.md#language).
- Business Central-miljøet er i alle land/områder unntatt Canada (denne funksjonen er ennå ikke tilgjengelig i Canada).

## <a name="get-started-using-chat-with-copilot"></a>Kom i gang med nettprat med Copilot

1. Øverst til høyre på skjermen velger du ikonet ![Viser ikonet for nettprat med Copilot](media/chat-copilot-icon.png) **Copilot** ![Viser kolonne nummer 1](media/callout-number-1.svg).

   **Copilot**-ruten vises til høyre som illustrert i følgende figur:

    ![Viser ikonet for nettprat med Copilot-ruten med bildeforklaringer](media/chat-with-copilot-pane.svg)

1. I boksen **Still et spørsmål** nederst ![Viser bildeforklaring nummer 2](media/callout-number-2.svg) skriver du inn spørsmålet og velger pilspissen eller trykker på <kbd>ENTER</kbd> for å få svar.

   Teksten du skriver inn, som ofte kalles en *spørring* i Copilot, kan være i form av et spørsmål, en uttalelse eller en kommando.

   > [!TIP]
   > Copilot inneholder et par funksjoner som kan hjelpe deg med å skrive spørsmål:
   > - Hvis du vil komme i gang med å formulere et spørsmål, velger du en av spørringsveiledningene, **Finn**, **Forklar** eller **Veiledning**, som er tilgjengelig øverst i ruten ![Viser bildeforklaring nummer 3](media/callout-number-3.svg) eller fra ikonet ![Viser spørringsveiledningsikonet](media/prompt-guide-icon.png) **Vis spørringer** over boksen **Still et spørsmål** ![Viser bildeforklaring nummer 4](media/callout-number-4.svg). Spørringsveiledninger er forhåndsdefinerte korte uttrykk som innleder et spørsmål eller en spørring. I tillegg til å spare tid er de utformet for å veilede Copilots svar mot en kategori av svar. De hjelper deg også med å forstå hvordan du formulerer spørsmål for å få de beste svarene.
   > - Velg spørringsforslagene oven knappen **Vis spørring** ![Viser bildeforklaring nummer 5](media/callout-number-5.svg) for automatisk å stille et forhåndsdefinert spørsmål for å få innsikt i hvordan spørsmålene og svarene fungerer. Spørringsforslag er bare tilgjengelige når du bruker CRONUS-demonstrasjonsselskapet.

1. Gå gjennom svarene som vises i Copilot-ruten ![Viser bildeforklaring nummer 6](media/callout-number-6.svg).

   Avhengig av spørsmålet ditt kan svaret inneholde tekst, koblinger til poster eller sider i Business Central og koblinger til hjelpeartikler for Business Central på Microsoft Learn.

1. Still et annet spørsmål for å avgrense svaret.

   Nettprat husker konteksten, noe som betyr at du ikke trenger å gjenta viktige punkter fra det opprinnelige spørsmålet.

## <a name="clear-chat-to-start-over"></a>Tøm nettprat for å starte på nytt

Hvis du vil bytte til et annet samtaleemne med Copilot, velger du ikonet ![Viser Tøm nettprat-ikonet](media/clear-chat-icon.png) **Start en ny Copilot-økt** nederst i Copilot-ruten over spørsmålsboksen. Denne handlingen tømmer Copilots minne om de siste meldingene dine. Å starte på nytt er ofte nyttig etter en lang samtale med mange meldinger, og det kan hjelpe Copilot med å gi mer nøyaktige svar.

Nettpraten tømmes også hvis du lukker eller logger deg av Business Central.

## <a name="get-the-most-out-of-your-questions"></a><a name="tips"></a>Få mest mulig ut av spørsmålene dine

Denne delen viser hvordan du kan forbedre svarene du får fra Copilot.

- Still tydelige og spesifikke spørsmål.
- Vær kortfattet og unngå lange setninger eller flere setninger.
- Still ett spørsmål om gangen. <!--Avoid asking about multiple questions in one message.-->
- Bruk naturlig språk, og uttrykk spørsmålene du ønsker på en vennlig og samtalebasert måte.
- Bruk nøkkelord, uttrykk og ord som du vet brukes i Business Central, enten i appen eller dokumentasjonen.
- Hvis det første svaret ikke svarer helt på spørsmålene dine, kan du stille oppfølgingsspørsmål eller omformulere det siste spørsmålet.
- Hvis du stiller et spørsmål om et annet emne enn det forrige spørsmålet, fjerner du den nåværende nettpratøkten for å starte på nytt.

## <a name="example-prompts"></a>Eksempel på spørringer

Spørsmålene dine til Copilot varierer naturligvis avhengig av rollen din, nåværende oppgave, prosessene som organisasjonen din følger, og hvordan du uttrykker deg med ord. Følgende er eksempler som viser ulike måter å stille spørsmål på i nettpratruten, som kan inspirere deg til å skrive dine egne spørsmål basert på din egen unike situasjon.

Spørring: `Find the Item with Description 'ATHENS Desk'`

I dette eksemplet gir du klare instruksjoner for Copilot om å finne én enkelt post. Du antyder for eksempel at posten finnes i varelisten. Du angir at feltet Beskrivelse må være en spesifikk tekst som du har skrevet inn ved hjelp av anførselstegn og med riktig bruk av store og små bokstaver. Copilot reagerer vanligvis nøyaktig når han får noen presise hint, men du kan også bruke mer uformelt språk som i neste eksempel.

Spørring: `give me the latest invoice for adatum`

I dette eksemplet ber du Copilot om å finne en post, men spørsmålet er mindre presist og kan resultere i et mindre nøyaktig svar. Copilot kan ofte forstå, eller gjette, at fakturaen du leter etter, ikke er en kjøpsfaktura, men en salgsfaktura fra listen Bokført salgsfaktura. Copilot må også samsvare `adatum` med `Adatum Corporation`, det vil si det fullstendige og nøyaktige navnet på salg til-kundenavnet som er knyttet til fakturaen.

Spørring: `Show me customer ledger entries for Adatum from about three weeks ago`

I dette eksemplet ber du kopiloten om å løse et vanlig datopuslespill som vanligvis krever at du åpner en kalender som referanse, eller bruker avanserte datoperiodefiltre. Copilot kan vanligvis forstå vanlige uttrykk og forretningsord.

Spørring: `How does I save my filterrings to do them later?`

I dette eksemplet kan du be Copilot om veiledning om hvordan du utfører en oppgave i Business Central. Copilot kan vanligvis forstå hensikten med spørsmålet ditt, selv om det er noen grammatiske feil, stavefeil eller forkortelser.

Spørring: `Provide feedback on answers`

Du kan rangere svarene du får fra Copilot ved å bruke liker-knappen (tommel opp) for god vurdering, eller liker ikke-knappen (tommel ned) for en dårlig vurdering. Når du velger Liker ikke-knappen, kan du velge en årsak, inkludert unøyaktig, upassende eller annet. Denne informasjonen kan hjelpe oss med å forbedre forslagene.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
## <a name="see-also"></a>Se også

[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)  
[Vanlige spørsmål om ansvarlig kunstig intelligens for nettprat med Copilot](faqs-chat-with-copilot.md)  
[Ressurser for hjelp i Business Central](product-help-and-support.md)  
