---
title: Vanlige spørsmål om nettprat med Copilot
description: 'Finn ut hvordan du chatter med Copilot, en virtuell assistent som hjelper deg med å bruke Business Central. Finn svar på vanlige spørsmål om chattefunksjoner, innstillinger og begrensninger.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Vanlige spørsmål om nettprat med Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Denne artikkelen besvarer noen av de vanlige spørsmålene om nettprat med Copilot i [!INCLUDE[prod_short](includes/prod_short.md)]. For spørsmål relatert til kunstig intelligens og nettprat kan du se [Vanlige spørsmål om ansvarlig kunstig intelligens for nettprat med Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kan administratorer gi eller nekte enkeltbrukere tillatelse til å få tilgang til nettprat?

Nei, det er ingen tillatelse eller tillatelse angitt for nettprat. Hvis nettprat er aktivert på siden [Copilot- og KI-funksjoner](enable-ai.md), har alle brukere i et miljø tilgang til nettprat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Er nettprat tilgjengelig på nettbrett, telefon eller andre formfaktorer?

Nei, nettpratruten er bare tilgjengelig i [!INCLUDE[web_client](includes/web_client.md)]-nettklienten.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Jeg bruker ikke Business Central på engelsk. Hva er alternativene mine?

For øyeblikket er nettprat bare tilgjengelig på engelsk. Du kan endre brukerspråket ditt til engelsk i [Mine innstillinger](ui-change-basic-settings.md#language).

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>Hvilken Business Central-versjon trenger jeg for nettprat?

Nettprat er tilgjengelig i forhåndsversjon fra versjon 24.0 (lanseringsbølge 1 i 2024).

## <a name="does-chat-work-with-my-customizations"></a>Fungerer nettprat med tilpasningene mine?

Det avhenger av hvilken type spørsmål du stiller Copilot. Eksempel:

- Hvis du stiller spørsmål for å finne poster, kan den finne poster i de egendefinerte tabellene som bruker egendefinerte felter.
- Hvis du ber Copilot om en forklaring eller veiledning, har den ikke tilgang til informasjon om tilpasningene dine eller dokumentasjon for tilleggene dine.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Hvordan åpner jeg en oppføring eller side med nettprat?

Når du ber Copilot om å finne oppføringer i [!INCLUDE[prod_short](includes/prod_short.md)], vises alle oppføringer den finner, som valgbare fliser eller koblinger i nettpratruten. I forhåndsversjonen navigerer ikke Copilot automatisk til noen sider.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Hvorfor får jeg forskjellige svar fra Copilot på det samme spørsmålet?

Copilot kan av og til svare på forskjellige måter. Svarene er ikke alltid identiske.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>Hvordan bruker jeg kopieringsfunksjonen på nettpratmeldinger?

Du kan bruke Kopier-knappen til å kopiere en melding fra tidligere i samtalen med Copilot, lime den inn i inndataboksen for å prøve på nytt eller prøve en variant av meldingen til Copilot.

## <a name="can-i-customize-or-extend-chat"></a>Kan jeg tilpasse eller utvide nettpraten?

I forhåndsversjonen kan ikke nettpratruten og Copilots svar endres på noen måte gjennom tilpasning eller tillegg.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>Søker Copilot etter data i andre selskaper eller miljøer?

Copilot søker bare etter oppføringer i selskapet du er logget inn på. Den søker ikke etter data på tvers av flere miljøer eller selskaper.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>Hva kan jeg gjøre hvis nettpratruten ikke vises?

Kontroller at brukerspråket i **Mine innstillinger** er satt til engelsk, og at miljøet er av versjon 24.0 eller nyere. På siden Copilot- og KI-funksjoner må du sørge for at administratoren har aktivert samtykke for data på tvers av geografiske områder og har aktivert nettprat. Kontroller også at miljølokaliseringen ikke er Canada.

Hvis du fremdeles ikke ser nettpraten med Copilot-funksjonen, er det mulig at Microsoft fortsatt ruller ut funksjonen til området ditt. Copilot rullet ut til amerikanske kunder først i april 2024 og vil deretter i løpet av uker rulle ut til andre land/områder.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Hvorfor viser Copilot bare tre oppføringer i nettpratruten?

Når du ber Copilot om å finne oppføringer, bestemmer måten du formulerer spørsmålet på, hvordan Copilot identifiserer og bruker filtre på sider for å finne det du leter etter. For å holde svarene konsise viser nettpratruten maksimalt tre oppføringsfliser, selv når Copilot finner mer relevante oppføringer.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Hvorfor gir Copilot feil svar på beregninger?

I forhåndsversjonen kan Nettprat med Copilot hjelpe deg med å finne oppføringer, forklare konsepter og veilede deg om hvordan du fullfører oppgaver i Business Central. Andre brukstilfeller støttes ikke, for eksempel å summere et felt på tvers av oppføringer eller beregne gjennomsnittlig månedlig beløp. Vi håper å legge til grunnleggende matematikk i Copilot i fremtiden.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kan jeg bruke tale i stedet for å skrive inn spørsmålene?

Du kan prate med Copilot ved å bruke taleskriving til å snakke i stedet for å skrive inn ordene i nettpratruten. Taleskriving bruker elektronisk talegjenkjenning og er tilgjengelig med Windows. For å bruke tale, aktiver nettpratmeldingsboksen, bruk deretter snarveien <kbd>Windows</kbd>+<kbd>H</kbd> og begynn å snakke. Hvis du vil ha mer informasjon, kan du se [Bruk taleskriving til å snakke i stedet for å skrive på PC-en](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Neste trinn

- [Nettprat med Copilot (forhåndsversjon)](chat-with-copilot.md)
