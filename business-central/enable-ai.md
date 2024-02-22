---
title: Konfigurere Copilot- og KI-funksjoner
description: Denne artikkelen forklarer hvordan du aktiverer Copilot i et miljø.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Konfigurer Copilot- og KI-funksjoner

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Denne artikkelen forklarer hvordan du kontrollerer Copilot og andre KI-funksjoner i Business Central. Denne oppgaven utføres av en administrator. Copilot er en systemfunksjon og en integrert del av Business Central. I likhet med de fleste systemfunksjoner gir du ikke tilgang til individuelle brukere, og du kan heller ikke aktivere eller deaktivere Copilot. Imidlertid tilbyr Copilot datastyringskontroller og muligheten til å deaktivere individuelle Copilot- og KI-funksjoner for hvert miljø. Det er forskjellige nivåer av tilgangskontroll til KI-funksjoner, avhengig av funksjonen:

- Tillat dataflytting på tvers av geografiske områder

  Denne oppgaven er bare nødvendig hvis Business Central-miljøet er i en annen geografi enn Azure OpenAI-tjenesten det bruker. [Finn ut mer](#allow-data-movement-across-geographies)

- Aktiver funksjonen på siden **Copilot og KI-funksjoner**. [Finn ut mer](#activate-features)

- Aktiver den spesifikke funksjonen hvis den fortsatt styres av **Funksjonsbehandling**.

  I lanseringsbølge 2 for 2023 er både forslag til markedsføringstekst og hjelp til bankkontoavstemming inkludert under **Funksjonsbehandling**. [Finn ut mer](#enable-feature-in-feature-management)

Hvis et av disse kravene ikke er oppfylt, er ikke funksjonen tilgjengelig for bruk.

## <a name="prerequisites"></a>Forutsetninger

- Du bruker Business Central online, versjon 23.1 eller senere. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Du har administrator- eller supertillatelser i Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Tillat dataflytting på tvers av geografiske områder

Denne oppgaven gjelder bare hvis bryteren **Tillat dataflytting** vises nær toppen av siden **Copilot og KI-funksjoner**. Hvis koblingen **Hvordan styrer jeg kopilotdataene mine?** vises i stedet for **Tillat dataflytting**-bryteren, hopper du over dette trinnet.

![Viser et skjermbilde av bryteren Tillat dataflytting på siden Copilot og KI-funksjoner.](media/allow-data-movement-v2.png)

Bryteren **Tillat dataflytting** angir at Business Central-miljølokasjonen – det vil si geografien der data behandles og lagres – ikke er den samme som geografien i Azure OpenAI-tjenesten som brukes av Copilot. Hvis du vil aktivere Copilot, må du tillate dataflytting mellom geografiske områder. Hvis du vil lære mer om dataflytting, kan du gå til [Copilot-dataflytting på tvers av geografiske områder](ai-copilot-data-movement.md). 

Hvis du vil tillate dataflytting utenfor ditt geografiske område, gjør du følgende:

1. I Business Central søker du etter og åpner siden **Copilot og KI-funksjoner**.
1. Slå på bryteren **Tillat dataflytting**.

   Bryteren **Tillat dataflytting** er aktivert som standard for miljøer i Azure-områder i Vest-Europa og Nord-Europa.

Du kan velge bort dataflytting ved å slå av bryteren **Tillat dataflytting**. Når en Azure OpenAI-tjeneste blir tilgjengelig i Business Central-miljøets geografi, kobles miljøet automatisk til den, og bryteren er ikke lenger tilgjengelig.
<!--
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

Alle Copilot- og KI-funksjoner er aktive som standard når de gjøres tilgjengelige i forhåndsversjon eller blir tilgjengelige. Ved hjelp av siden **Copilot og KI-funksjoner** kan du deaktivere eller aktivere på nytt enkeltfunksjoner for alle brukere.

1. I Business Central søker du etter og åpner siden **Copilot og KI-funksjoner**.

1. Siden viser alle tilgjengelige Copilot- og KI-relaterte funksjoner og deres nåværende status, som kan være enten aktive eller inaktive. Funksjonene er delt inn i to deler &mdash; én del for funksjoner i forhåndsvisning og en annen for funksjoner som er generelt tilgjengelige. 

   [![Viser rollesenteret for Business Central og sjekklisten for Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Hvis du vil aktivere en funksjon, velger du den i listen og velger deretter **Aktiver**-handlingen.
   - Hvis du vil deaktivere en funksjon, velger du den og velger deretter **Dektiver**-handlingen. 


## <a name="enable-feature-in-feature-management"></a>Aktiver funksjon i Funksjonsstyring

Når individuelle Copilot-funksjoner utgis i mindre oppdateringer for Business Central, er disse funksjonene valgfrie frem til neste større oppdatering. **Funksjonsstyring** brukes til å aktivere eller deaktivere funksjoner som er i forhåndsversjon, for eksempel bankavstemming, og enkelte funksjoner som er tilgjengelige, for eksempel markedsføringstekstforslag. [Finn ut mer om funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. I Business Central søker du etter og åpner siden **Funksjonsstyring**.
2. Hvis du vil aktivere en funksjon, setter du kolonnen **Aktivert for** til **Alle brukere**. Hvis du vil deaktivere en funksjon, setter du kolonnen **Aktivert for** til **Ingen**. Bruk tabellen nedenfor til å finne bryteren som gjelder for Copilot- og KI-funksjonaliteten du vil aktivere:

   - **Funksjonsforhåndsversjon: Bankkontoavstemming med Copilot** aktiverer funksjonen for bankkontoavstemming.
   - **Funksjonsforhåndsversjon: Opprett KI-drevne produktbeskrivelser med Copilot** aktiverer funksjonen for forslag til markedsføringstekst.

   Hvis du vil ha mer informasjon om funksjonsstyring generelt, går du til [funksjonsstyring](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="granting-user-access"></a>Gi brukertilgang

Copilot- og KI-funksjoner kan tilby funksjonalitet beregnet for alle brukere på tvers av organisasjonen eller for spesifikke brukerroller. De fleste Copilot- og KI-funksjonene tilbyr tilgangskontroll ved å bruke tillatelser og tillatelsessett i Business Centrals tillatelsesstyringssystem. [Finn ut mer om tillatelser og tillatelsessett](ui-define-granular-permissions.md).

Hvis du vil gi eller nekte tilgang til spesifikke Copilot- og KI-funksjoner, kan du se dokumentasjonen eller utgiveren av funksjonen for å identifisere hvilke tillatelser som kreves. 

## <a name="next-steps"></a>Neste trinn

Når du har aktivert og samtykket til funksjonene, er du klar til å prøve dem. Gå til:

- [Legg til markedsføringstekst i varer](item-marketing-text.md) 
- [Avstemme ved hjelp av avstemmingshjelpen](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Se også

[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Oversikt over forslag til markedsføringstekst](ai-overview.md)   
[Vanlige spørsmål om forslag til markedsføringstekst](faqs-marketing-text.md)  
