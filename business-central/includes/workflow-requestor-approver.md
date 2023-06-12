---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
---

Når du definerer brukere for godkjenning av arbeidsflyter, er det viktig at samme bruker ikke er både en anmoderen og en godkjenner i en arbeidsflytbrukergruppe. Når en bruker er både en anmoder og en godkjenner, fungerer godkjenninger for dem på følgende måte:

* Forespørslene godkjennes alltid automatisk.
* Hvis det finnes flere godkjennere, kan bare godkjennerne med et høyere sekvensnummer i arbeidsflytbrukergruppen endre statusen til en forespørsel til Godkjent. Godkjennere med et lavere sekvensnummer kan godkjenne forespørsler, men godkjenningene påvirker ikke statusen til en forespørsel.