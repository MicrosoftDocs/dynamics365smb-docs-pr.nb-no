---
title: Konfigurer Copilot- og KI-funksjoner
description: Denne artikkelen forklarer hvordan du aktiverer Copilot i et miljø.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: '7771,7772_Primary,7775_Primary'
---

# <a name="configure-copilot-and-ai-capabilities"></a>Konfigurer Copilot- og KI-funksjoner

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Denne artikkelen forklarer hvordan du kontrollerer Microsoft Copilot og andre KI-funksjoner i Dynamics 365 Business Central. En administrator må utføre disse oppgavene.

Copilot er en systemfunksjon og en integrert del av Business Central. I likhet med de fleste systemfunksjoner gir du ikke tilgang til individuelle brukere, og du kan heller ikke aktivere eller deaktivere Copilot. Imidlertid tilbyr Copilot datastyringskontroller og muligheten til å deaktivere individuelle Copilot- og KI-funksjoner for hvert miljø. Det er forskjellige nivåer av tilgangskontroll for KI-funksjoner, avhengig av funksjonen:

- Tillat dataflytting på tvers av geografiske områder.

    Denne oppgaven er bare nødvendig hvis Business Central-miljøet er i en annen geografi enn Azure OpenAI-tjenesten det bruker. [Finn ut mer om denne oppgaven](#allow-data-movement-across-geographies).

- Aktiver funksjonen på siden **Copilot og KI-funksjoner**. [Finn ut mer om denne oppgaven](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Hvis et av disse kravene ikke er oppfylt, er ikke funksjonen tilgjengelig for bruk.

## <a name="prerequisites"></a>Forutsetninger

- Du bruker Business Central Online.
- Du er en [administrator](#requirements-for-being-an-administrator) i Business Central.

## <a name="allow-data-movement-across-geographies"></a>Tillat dataflytting på tvers av geografiske områder

Denne oppgaven gjelder bare hvis alternativet **Tillat dataflytting** vises nær toppen av siden **Copilot og KI-funksjoner**. Hvis koblingen **Hvordan styrer jeg kopilotdataene mine?** vises i stedet for alternativet **Tillat dataflytting**, hopper du over denne oppgaven.

![Skjermbilde som viser alternativet Tillat dataflytting på siden Copilot og KI-funksjoner.](media/allow-data-movement-v2.png)

Tilstedeværelsen av alternativet **Allow data Tillat dataflytting** angir at lokasjonen av Business Central-miljølet(det vil si geografien der data behandles og lagres) er forskjellig fra geografien i Azure OpenAI Service som brukes av Copilot. Hvis du vil aktivere Copilot, må du tillate dataflytting mellom geografiske områder. [Finn ut mer om dataflytting](ai-copilot-data-movement.md).

Hvis du vil tillate dataflytting utenfor ditt geografiske område, gjør du følgende:

1. I Business Central søker du etter og åpner siden **Copilot og KI-funksjoner**.
1. Slå på alternativet **Tillat dataflytting**.

    > [!NOTE]
    > For miljøer i Azure-områder i Vest-Europa og Nord-Europa er alternativet **Tillat dataflytting** aktivert som standard.

Du kan velge bort dataflytting ved å slå av alternativet **Tillat dataflytting**.

Når en Azure OpenAI-tjeneste blir tilgjengelig i Business Central-miljøets geografi, kobles miljøet automatisk til den. Ved dette punktet vises ikke alternativet **Tillat dataflytting** lenger på siden **Copilot og KI-funksjoner**.

<!-- Don't review
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->

## <a name="activate-features"></a>Aktivere funksjoner

Alle Copilot- og KI-funksjoner er aktive som standard når de gjøres tilgjengelige i forhåndsversjon eller blir tilgjengelige. På siden **Copilot og KI-funksjoner** kan du deaktivere eller aktivere på nytt enkeltfunksjoner for alle brukere.

1. I Business Central søker du etter og åpner siden **Copilot og KI-funksjoner**.
1. Siden viser alle tilgjengelige Copilot- og KI-relaterte funksjoner og deres nåværende status. (Statusen kan være *Aktiv* eller *Inaktiv*.) Funksjonene er delt inn i to deler: én del for funksjoner som er i forhåndsversjon, og en annen for funksjoner som er generelt tilgjengelige.

    - Hvis du vil aktivere en funksjon, velger du den i listen og velger deretter **Aktiver**.
    - Hvis du vil deaktivere en funksjon, velger du den i listen og velger deretter **Dektiver**.

    [![Skjermbilde som viser knappene Aktiver og Deaktiver for funksjonslistene på siden Copilot og KI-funksjoner.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Gi brukertilgang

Copilot- og KI-funksjoner kan tilby funksjonalitet som er beregnet for alle brukere på tvers av organisasjonen eller for spesifikke brukerroller. De fleste Copilot- og KI-funksjonene tilbyr tilgangskontroll via tillatelser og tillatelsessett i Business Centrals tillatelsesstyringssystem. [Finn ut mer om tillatelser og tillatelsessett](ui-define-granular-permissions.md).

Tabellen nedenfor viser tillatelsene som kreves for å bruke Copilot-funksjoner fra Business Central.

| Copilot-funksjon | Nødvendige tillatelser |
|---|---|
| Analysehjelp | **DATAANALYSE - EXEC**-tillatelsessettet eller utførelsestillatelse på systemobjekt 9640, **Tillat dataanalysemodus**. Disse tillatelsene er de samme tillatelsene som kreves for å få tilgang til analysemodus. |
| Bankkontoavstemmingshjelp | Tillatelse på side 7250, **Bankkontoavstemming, KI-forslag**, og side 7252, **Overfør til finanskonto, KI-forslag**. |
| Nettprat | Det er ingen tillatelser eller tillatelsessett som styrer tilgangen til nettprat på per bruker-basis. Hvis nettprat er aktivert, er det tilgjengelig for alle brukere. |
| Tildel e-dokumenter | Tillatelse på side 6166, **Copilot-spørring for e-dokumentbestilling** |
| Forslag til markedsføringstekst | Tillatelse på side 5836, **Copilot-markedsføringstekst** |
| Salgslinjeforslag | Tillatelse på side 7275, **KI-forslag for salgslinjer**, og side 7276, **KI-forslagserst. for salgslinje** |

Hvis du vil gi eller nekte tilgang til spesifikke kopilot- og KI-funksjoner som ikke er fra Microsoft, kan du se funksjonens dokumentasjon eller utgiver for å identifisere de nødvendige tillatelsene.

## <a name="requirements-for-being-an-administrator"></a>Krav for å være administrator

Du må ha SUPER-tillatelser i Business Central-brukerkontoen eller en av følgende Business Central-lisenser:

- Delegert administratoragent – partner
- Delegert brukerstøtteagent – partner
- Intern administrator
- Intern BC-administrator
- Dynamics 365-administrator

Business Central tilbyr ennå ikke detaljerte tillatelser på objektnivå, slik at bare bestemte administratorer kan konfigurere Copilot.

## <a name="next-steps"></a>Neste trinn

Når du har aktivert og samtykket til funksjonene, er du klar til å prøve dem. Gå til følgende artikler:

- [Legge til markedsføringstekst i elementer med Copilot](item-marketing-text.md)
- [Analyser listedata med hjelp fra Copilot](analysis-assist.md)
- [Nettprat med Copilot](chat-with-copilot.md)
- [Tildel e-dokumenter til bestillingslinjer med Copilot](map-edocuments-with-copilot.md)
- [Avstem bankkontoer med Copilot](bank-reconciliation-with-copilot.md)
- [Foreslå linjer i ordrer med Copilot](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Se også

[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Vanlige spørsmål om analysehjelp](faqs-analysis-assist.md)  
[Vanlige spørsmål om bankkontoavstemmingshjelp](faqs-bank-reconciliation.md)  
[Vanlige spørsmål om nettprat med Copilot](faqs-chat-with-copilot.md)  
[Vanlige spørsmål om tildelinger av e-dokumenter med bestillinger](faqs-map-edocuments.md)  
[Vanlige spørsmål om forslag til markedsføringstekst](faqs-marketing-text.md)  
[Vanlige spørsmål om salgslinjeforslag](faq-sales-suggest-sales-lines-with-copilot.md)  
[Oversikt over forslag til markedsføringstekst](ai-overview.md)
