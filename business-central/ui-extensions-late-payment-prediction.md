---
title: Forutsi forsinket betaling for salgsdokumenter
description: Denne artikkelen forklarer hvordan du bruker prognosemodellen vår til å forutse om en faktura blir betalt i tide.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/06/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Utvidelsen Prognose for forsinket betaling

Effektiv administrasjon av salg er viktig for den generelle økonomiske tilstanden statusen til en bedrift. Hvis du vil redusere utestående og trenger hjelp med å finjustere innkrevingsstrategien, forutsiert utvidelsen om du kan forvente sene betalinger. Hvis en betaling er forutsatt å bli sen, kan du bestemme deg for å justere betalingsbetingelsene eller betalingsmåten for kunden.

## Kom i gang

Når du åpner et bokført salgsdokument, vises en melding øverst på siden. Hvis du vil bruke utvidelsen Prognose for forsinket betaling, velger du dette ved å velge **Aktiver** i meldingen. Du kan også du sette opp utvidelsen manuelt. For eksempel hvis du angrer på at du lukket meldingen.

Hvis du vil aktivere utvidelsen manuelt, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av prognose for forsinket betaling** og velg den relaterte koblingen.  
2. Fyll ut feltene etter behov.

> [!NOTE]
> Hvis du velger å aktivere utvidelsen manuelt, må du være klar over at [!INCLUDE[prod_short](includes/prod_short.md)] ikke tillater at du gjør dette hvis kvaliteten på modellen er lav. Kvaliteten på modellen angir hvor nøyaktig modellens prognoser sannsynligvis vil være. Flere faktorer kan påvirke kvaliteten på en modell. Dette var for eksempel ikke er nok data, eller det er ikke nok variasjon i dataene. Du kan vise kvaliteten på modellen du bruker, på siden **Oppsett av prognose for forsinket betaling**. Du kan også angi e minimumsgrense for modellkvaliteten.

## Vis alle betalingsprognoser

Hvis du aktiverer utvidelsen, er flisen **Betalinger forutsatt til å være forsinket** tilgjengelig i **Forretningsleder**-rollesenteret. Flisen viser hvor mange betalinger som er forutsatt å bli sene, og lar deg åpne siden **Kundeposter**, der du kan se nærmere på de bokførte fakturaene. Det finnes tre kolonner til å være oppmerksom:  

* **Sen betaling** - angir om betalingen av fakturaen forutsettes å bli forsinket.
* **Prognosekonfidens** - angir hvor pålitelig du bør vurdere prognosen til å være. **Høy** betyr at prognosen er minst 90 % sikker, **Middels** er mellom 80 og 90 % og **Lav** er under 80 %.
* **Prognosekonfidens %** - viser den faktiske prosenten bak prognoserangeringen. Denne kolonnen er skjult som standard, men kan du legge den til hvis du vil. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

> [!TIP]
> Kundeposter-siden viser en faktaboks på høyre side. Når du ser prognoser, informasjon i vinduet **Kundeinformasjon** kan være nyttig. Når du velger fakturaen i oversikten, viser delen informasjon om kunden. Du kan også handle umiddelbart. Hvis en kunde ofte glemmer å betale, kan du åpne kundekortet fra faktaboksen og sperre kunden for fremtidig salg.  

## Utformingsdetaljer

Microsoft distribuerer og opererer forutsigbare nettjenester i alle områder der [!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig. Tilgang til disse webtjenestene er inkludert i [!INCLUDE[prod_short](includes/prod_short.md)]-abonnementet. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/business-central/overview/)-nettstedet.

Nettjenestene fungerer i tre moduser:

* Opplæringsmodell. Webtjenesten lærer opp modellen basert på det angitte datasettet.
* Evalueringsmodell. Webtjenesten kontrollerer om modellen returnerer pålitelige data for det angitte datasettet.
* Forutsigelsesmodell. Webtjenesten bruker modellen i det angitte datasettet til å lage en forutsigelse.

Disse webtjenestene er tilstandsløse, noe som betyr at de bare bruker data til å beregne forutsigelser etter behov. De lagrer ikke data.

> [!NOTE]  
> Du kan bruke din egen prediktive webtjeneste i stedet for vår. Hvis du vil ha mer informasjon, kan du se [Opprette og bruke din egen prediktive webtjeneste for prognose for forsinket betaling](#AnchorText).

### Data som kreves for å lære opp og evaluere modellen

For hver **kundepost** som har en tilhørende **bokført salgsfaktura**:

* Beløp (lokal valuta) inkl. mva.
* Betalingsbetingelser i dager beregnes som **forfallsdato** minus **bokføringsdato**
* Om det finnes en kreditnota som er utlignet

I tillegg har posten aggregerte data fra andre fakturaer som er knyttet til samme kunde.

- Totalt antall og beløp på betalte fakturaer
- Totalt antall og beløp på fakturaer som ble betalt for sent
- Totalt antall og beløp på utestående fakturaer
- Totalt antall og beløp på utestående fakturaer som allerede er for sene
- Gjennomsnittlig antall dager for sent
- Forhold: antall betalte fakturaer og fakturaer betalt for sent
- Forhold: beløp for betalte fakturaer og fakturaer betalt for sent
- Forhold: antall utestående fakturaer og fakturaer som er utestående eller betalt for sent
- Forhold: beløp for utestående fakturaer og fakturaer som er utestående eller betalt for sent

> [!NOTE]
> Informasjonen om kunden er ikke inkludert i datasettet.

### Standardmodell og Min modell

Prognosemodellen i utvidelsen Prognose for forsinket betaling er lært opp på data som representerer en rekke små og mellomstore bedrifter. Når du starter bokføring av fakturaer og mottaksbetalinger, vurderer [!INCLUDE[prod_short](includes/prod_short.md)] om standardmodellen passer til din forretningsflyt.

Hvis prosessene ikke samsvarer med standardmodellen, kan du bruke filtypen, men du må få mer data. Fortsett bare å bruke [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Vi bruker litt av databehandlingstiden din hver uke når vi evaluerer og lærer opp modellen på nytt.

[!INCLUDE[prod_short](includes/prod_short.md)] kjører opplæring og evaluering automatisk når nok betalte og sene fakturaer er tilgjengelige. Du kan imidlertid kjøre den manuelt når du vil.

#### Slik lærer du opp og bruker modellen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av prognose for forsinket betaling** og velg den relaterte koblingen.  
2. I vinduet **Valgt modell** velger du **Min modell**.
3. Velg handlingen **Opprett min modell** for å lære opp dataene dine.  

## <a name="AnchorText"> </a>Opprette og bruke din egen prediktive webtjeneste for prognose for forsinket betaling

Du kan også opprette din egen prediktive webtjeneste basert på en fellesmodell som heter **Prognoseeksperiment for Dynamics 365 Business Central**. Denne prediktive modellen er tilgjengelig elektronisk i Azure AI-galleriet. Hvis du vil bruke modellen, følger du denne fremgangsmåten:  

1. Åpne en nettleser, og gå til [Azure AI-galleri](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Søk etter **Prognoseeksperiment for Dynamics 365 Business Central**, og åpne deretter modellen i Azure Machine Learning Studio.  
3. Bruke Microsoft-kontoen til å registrere deg for et arbeidsområde, og kopier deretter modellen.  
4. Kjør modellen, og publisere den som en webtjeneste.  
5. Noter URL-API og API-nøkkel. Du vil bruke disse legitimasjonene for et oppsett for kontantstrømprognoser.  
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av prognose for forsinket betaling** og velg den relaterte koblingen.  
7. Merk av for **Bruk Azure-abonnementet mitt**.
8. På hurtigfanen **Legitimasjon for min modell** angir API URL-adressen og API-nøkkelen for modellen.  

## Se også

[Dokumentasjon for Azure Machine Learning Studio](/azure/machine-learning/classic/)  
[Tilpasse Business Central for med utvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Bruk kunstig intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
