---
title: Vanlige spørsmål om nettprat med Copilot
description: Denne artikkelen besvarer noen av de vanlige spørsmålene om nettprat med Copilot i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Vanlige spørsmål om nettprat med Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Denne artikkelen besvarer noen av de vanlige spørsmålene om nettprat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. For spørsmål relatert til kunstig intelligens og nettprat kan du se [Vanlige spørsmål om ansvarlig kunstig intelligens for nettprat med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratorer gi eller nekte enkeltbrukere tillatelse til å få tilgang til nettprat?

Nei, det er ingen tillatelse eller tillatelse angitt for nettprat. Hvis nettprat er aktivert på siden [Copilot- og KI-funksjoner](enable-ai.md), har alle brukere i et miljø tilgang til nettprat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Er nettprat tilgjengelig på nettbrett, telefon eller andre formfaktorer?

Nei, nettpratruten er bare tilgjengelig i [!INCLUDE[web_client](includes/web_client.md)]-nettklienten.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jeg bruker ikke Business Central på engelsk. Hva er alternativene mine?

For øyeblikket er nettprat bare tilgjengelig på engelsk. Du kan endre brukerspråket ditt til engelsk i [Mine innstillinger](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Hvilken Business Central-versjon trenger jeg for å bruke nettprat?

Nettprat er tilgjengelig i forhåndsversjon fra versjon 24.0 (lanseringsbølge 1 i 2024).

## <a name="does-chat-work-with-my-customizations"></a>Fungerer nettprat med tilpasningene mine?

Det avhenger av hvilken type spørsmål du stiller Copilot. Eksempel:

- Når du stiller spørsmål for å finne poster, kan Copilot finne poster i de egendefinerte tabellene som identifiseres ved hjelp av egendefinerte felter.
- Når du ber om en forklaring eller veiledning, har ikke Copilot tilgang til informasjon om tilpasningene dine eller dokumentasjon for tilleggene dine.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Copilot ser aldri ut til å åpne posten eller siden jeg ba om. Hva gjør jeg galt?

Når du ber Copilot om å finne oppføringer i [!INCLUDE[prod_short](includes/prod_short.md)], vises alle oppføringer den finner, som valgbare fliser eller koblinger i nettpratruten. I forhåndsversjonen navigerer ikke Copilot automatisk til noen sider.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Svarene jeg får fra Copilot varierer selv om jeg stiller det samme spørsmålet. Er det en feil?

Copilot kan av og til svare på forskjellige måter. Svarene er ikke nødvendigvis identiske.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Når bør jeg bruke kopieringsfunksjonen på nettpratmeldinger?

Du kan bruke Kopier-knappen til å kopiere en melding fra tidligere i samtalen med Copilot, lime den inn i inndataboksen for å prøve på nytt eller prøve en variant av meldingen til Copilot.

## <a name="how-do-i-customize-or-extend-chat"></a>Hvordan tilpasser eller utvider jeg nettpraten?

I forhåndsversjonen kan ikke nettpratruten og Copilots svar endres på noen måte gjennom tilpasning eller tillegg.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Finner Copilot data i andre selskaper eller miljøer?

Copilot søker bare etter oppføringer i selskapet du er logget på&mdash;, selv om organisasjonen bruker flere miljøer eller selskaper til å skille data.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Copilot-nettpratruten vises ikke. Hva kan jeg gjøre?

Kontroller at brukerspråket i Mine innstillinger er satt til engelsk, og at miljøet er av versjon 24.0 eller nyere. På siden Copilot- og KI-funksjoner må du sørge for at administratorer har aktivert samtykke for data på tvers av geografiske områder og har aktivert nettprat. Kontroller at miljølokaliseringen ikke er Canada.

Hvis du fremdeles ikke ser chatten med Copilot-funksjonen, er det mulig at Microsoft fortsatt ruller ut funksjonen til din region. Copilot rulles ut til amerikanske kunder først i april 2024, og vil deretter i løpet av noen uker rulles ut til andre land/region-lokaliseringer.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Hvorfor viser Copilot bare tre oppføringer i chatteruten?

Når du ber Copilot om å hente poster, bestemmer måten du formulerer spørsmålet på, hvordan Copilot identifiserer og bruker filtre på sider for å finne det du leter etter. For å holde svarene kompakte og konsise viser chatteruten maksimalt tre postfliser, selv når Copilot finner et større antall relevante oppføringer.

## <a name="copilot-returns-incorrect-answers-to-totals-and-other-calculations"></a>Copilot returnerer feil svar på totaler og andre beregninger

I forhåndsversjonen kan Chat with Copilot finne poster, forklare konsepter og veilede deg til hvordan du fullfører oppgaver i Business Central. Andre brukstilfeller støttes ikke, for eksempel å legge sammen et felt på tvers av poster eller beregne gjennomsnittlig månedlig beløp. Vi håper å legge til grunnleggende matematikk evner til Copilot i fremtiden.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kan jeg bruke tale i stedet for å skrive inn spørsmålene?

Du kan chatte med Copilot ved å bruke taleskriving til å snakke i stedet for å skrive inn ordene i samtaleruten. Stemmeskriving bruker elektronisk talegjenkjenning og er tilgjengelig med Windows. For å bruke tale, aktiver chatmeldingsboksen, bruk deretter Windows <kbd>H-snarveien</kbd>+<kbd></kbd> og begynn å snakke. Hvis du vil ha mer informasjon, kan du se [Bruke taleskriving til å snakke i stedet for å skrive på PCen](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Neste trinn

[Nettprat med Copilot (forhåndsversjon)](chat-with-copilot.md)
