---
title: Konfigurer varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot
description: Denne artikkelen forklarer hvordan du skaffer en Copilot-prøveversjon av Business Central og aktiverer Copilot i et miljø.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="configure-ai-powered-item-marketing-text-preview-with-copilot"></a>Konfigurer varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Denne artikkelen forklarer hvordan du kan kontrollere muligheten til å opprette varemarkedsføringstekst drevet av kunstig intelligens med Copilot for organisasjonen. Denne oppgaven utføres av en administrator. Det er to krav du må oppfylle for å gjøre funksjonen tilgjengelig for brukere:

- Aktiver funksjonen **Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot**
- Samtykk i vilkårene for [forhåndsversjonen](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [Microsofts personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=521839) på vegne av organisasjonen.

Hvis et av disse kravene ikke er oppfylt, er ikke funksjonen tilgjengelig for bruk.

## <a name="prerequisites"></a>Forutsetninger

Du bruker en [forhåndsversjon](ai-preview-getstarted.md) av Business Central som er aktivert for Copilot. Aktivering av Copilot gjøres av en administrator. Hvis du vil ha mer informasjon, kan du gå til [Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot](enable-ai.md).

## <a name="enable-or-disable-create-ai-powered-product-descriptions-with-copilot"></a>Aktiver eller deaktiver Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot

1. I Business Central søker du etter og åpner siden **Funksjonsstyring**.
2. Angi **Aktivert for**-kolonnen for **Funksjonsforhåndsversjon: Opprett produktbeskrivelser drevet av kunstig intelligens med Copilot** til **Alle brukere** for å aktivere funksjonen eller **Ingen** for å deaktivere den.

   Hvis du vil ha mer informasjon om funksjonsstyring generelt, går du til [funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users"></a>Samtykk i eller avvis vilkårene for forhåndsversjon og personvern for alle brukere

1. I Business Central søker du etter og åpner siden **Status for personvernerklæringer**.
2. I kolonnen **Integreringsnavn** velger du **Azure OpenAI**, og deretter leser du vilkårene som vises.
3. Merk av for **Godta for alle** i **Azure OpenAI**-raden for å samtykke eller **Ikke godta for alle** for å avslå.

## <a name="next-steps"></a>Neste trinn

Når du har aktivert og samtykke i funksjonen, er du klar til å prøve ut Copilot på varer i Business Central. Gå til [Legg til markedsføringstekst i varer](item-marketing-text.md).  

## <a name="see-also"></a>Se også

[Oversikt over varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-overview.md)  
[Opprett markedsføringstekst til varer ved hjelp av Copilot](item-marketing-text.md)  
[Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-faq.md)  
