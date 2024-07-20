---
title: Bruke Salgs- og lagerprognose-utvidelsen til lagerstyring
description: 'Utvidelsen bidrar til å forutsi salg, få en klar oversikt over forventet tomt lager, og hjelper deg til og med å opprette etterfyllingsforespørsler til leverandører.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Utvidelsen Salgs- og lagerprognose

Lagerstyring er en avveining mellom kundeservice og håndtering av kostnader. På den ene siden krever en lav beholdning mindre arbeidskapital, men på den annen side kan tomme lagre føre til tapt salg. Salgs- og lagerprognose-utvidelsen forutsier mulig salg ved hjelp av historiske data og gir en tydelig oversikt over forventet tomt lager. Basert på prognosen hjelper utvidelsen med å opprette etterfyllingsforespørsler til leverandørene og sparer deg for tid.  

## <a name="setting-up-forecasting"></a>Sette opp prognoser

I [!INCLUDE[prod_short](includes/prod_short.md)] er tilkoblingen til [Azure AI](https://azure.microsoft.com/overview/ai-platform/) allerede satt opp for deg. Men du kan konfigurere prognosen til å bruke en annen type periode å rapportere etter, for eksempel endre fra prognose etter måned til prognose etter kvartal. Du kan også velge antall perioder som prognosene skal beregnes for, avhengig av hvor detaljert du vil at prognosen skal være. Vi foreslår at du lager månedlige prognoser, og med en 12 måneders horisont for prognosen.

> [!TIP]  
> Ta hensyn til lengden på periodene som tjenesten bruker i beregningene. Jo mer data du angir, jo mer nøyaktig vil forutsigelsene være. Vær også oppmerksom på store avvik i perioder. De vil også ha innvirkning på forutsigelser. Hvis Azure AI ikke finner nok data eller dataene varierer mye, vil ikke tjenesten utføre en forutsigelse.

## <a name="use-the-forecasts"></a>Bruk prognosene

Utvidelsen bruker Azure AI til å forutse fremtidige salg basert på din salgshistorikk for å unngå for liten lagerbeholdning. Når du for eksempel velger en vare på siden **Varer**, viser diagrammet i **Vareprognose**-ruten beregnet salg av denne varen i den kommende perioden. På denne måten kan du se om det er sannsynlig at du snart går tom for varen på lageret.  

Du kan også bruke utvidelsen til å foreslå når lageret bør fylles på. Du kan for eksempel opprette en bestilling for Fabrikam for å kjøpe den nye kontorstolen. Utvidelsen Salgs- og lagerprognose kan tyde på at du også fyller på LONDON-svingstolen som du vanligvis kjøper fra denne leverandøren. Utvidelsen kan forutsi at du snart går tom for LONDON-svingstolen, og at du kanskje bør bestille flere stoler allerede nå.  

## <a name="design-details"></a>Utformingsdetaljer

Abonnementer for [!INCLUDE[prod_short](includes/prod_short.md)] gir tilgang til flere prediktive webtjenester i alle områder der [!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/)-nettstedet. 

Disse webtjenestene er tilstandsløse, noe som betyr at de bare bruker data til å beregne forutsigelser etter behov. De lagrer ikke data.

> [!NOTE]  
>   Du kan også bruke din egen prediktive webtjeneste i stedet for vår. Hvis du vil ha mer informasjon, kan du se [Opprette og bruke din egen forutsigbare webtjeneste for salgs- og lagerprognose](#AnchorText). 

### <a name="data-required-for-forecast"></a>Data som kreves for prognose

For å lage prognoser om fremtidig salg, krever webtjenesten kvantitative data om tidligere salg. De dataene kommer fra feltene **Bokføringsdato**, **Varenr.** og **Antall** på siden **Vareposter**, der:

- Posttypen er Salg.
- Bokføringsdatoen er mellom datoen som beregnes basert på verdiene i feltene **Historiske perioder** og **Periodetype** på siden **Oppsett for salgs- og varelagerprognose** og arbeidsdatoen.

Før webtjenesten brukes, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaksjoner etter **Varenr.** og **Bokføringsdato** basert på verdien i feltet **Periodetype** på siden **Oppsett for salgs- og varelagerprognose**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Opprette og bruke din egen forutsigbare webtjeneste for salgs- og lagerprognose

For [!INCLUDE[prod_short](includes/prod_short.md)] online er modellen publisert av Microsoft og koblet til Microsoft-abonnementet. For andre distribusjonsalternativer må du opprette Machine Learning-ressurser i ditt eget Azure-abonnement. Du finner eksempeltrinn i [eksempelrepositoriet](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Formålet med denne oppgave er å få API-URI-en og API-nøkkelen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Oppsett for salgs- og varelagerprognose**, og velg deretter den relaterte koblingen.  
2. Utvid hurtigfanen **Generelt**, og fyll deretter ut feltene URL-adresse for API og API-nøkkel.  

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Bruk kunstig intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Oversikt over prognose-APIer](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
