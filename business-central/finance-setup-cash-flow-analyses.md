---
title: Definere kontantstrømanalyse
description: 'Bruk diagrammer i rollesenteret for regnskapsfører til å analysere pengestrømmen i virksomheten, inkludert utgifter, inntekter, likviditet og innbetalinger minus utbetalinger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
---
# <a name="setting-up-cash-flow-analysis"></a>Definere kontantstrømanalyse

Hvis du vil ha hjelp til å avgjøre hva du skal gjøre med din kontanter, kan du ta en titt på diagrammene i rollesenteret regnskapsfører:

* **Kontantsyklus**  
* **Inntekter og utgifter**  
* **Kontantstrøm**  
* **Kontantstrømprognoser**  

Denne artikkelen beskriver hvor dataene i diagrammene kommer fra, og om nødvendig, hva du skal gjøre for å begynne å bruke diagrammene.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Diagrammene Kontaktsyklus og Inntekter og utgifter

Diagrammene **Kontantsyklus** og **Inntekter og utgifter** er klare til å starte, basert på kontoplanene og finansrapportene. Kontoene er hvor dataene kommer fra, og finansrapporter beregner forholdet mellom salg og tilgodehavender. Enkelte kontoer og finansrapporter tilbys. Du kan bruke dem som de er, endre dem, og legge til nye. Hvis du legger til finanskonti i kontoplanen, for eksempel ved å importere dem fra QuickBooks, tilordner kontoene på siden **Finansrapporter** for følgende rapporter:

| Finansrapportnavn | Hvor det brukes |
| --- | --- |
| **I_KONTSYKL** |Kontantsyklus |
| **I_KONTSTR** |Kontantstrøm |
| **I_INNTUTG** |Inntekter og utgifter |
| **I_MINRÅBAL** |Som et resultatregnskap hvis du ikke bruker kontoplanen |

> [!NOTE]
> Det er en god idé å beholde beregningene som er angitt for finansrapporten.

Angi kontoer i feltet **Sammentelling** for **Totalinntekt**, **Totalt salg**, **Totalt kjøp** og **Total lagerverdi**. Hvis du vil tildele en rekke kontoer, angir du kontonumrene atskilt av .. som **1111.. 4444**. Du kan også angi kontonumrene atskilt med en vertikal strek som **2222|3333|5555** for å tildele bestemte kontoer.  

> [!TIP] 
> Bekreft tilordningen ved å velge handlingen **Oversikt**.  

## <a name="set-up-the-cash-flow-chart"></a>Definere Kontantstrøm-diagrammet

Kontantstrøm-diagrammet er basert på følgende:  

* Et diagram over kontantstrømkonti.
* Ett eller flere kontantstrømoppsett. Disse oppsettene angir kontoene som skal brukes for finans, innkjøp, salg, tjenester og aktiva.  

For å hjelpe deg med å komme i gang, inneholder [!INCLUDE [prod_short](includes/prod_short.md)] noen konto- og kontantstrømoppsett. Du kan legge til, endre eller fjerne dem.  

Hvis du vil konfigurere kontoene, søker du etter **Diagram over kontantstrømkontoer**, velger koblingen, og deretter fyller du ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Gjenta disse trinnene for **kontantstrømoppsett**.

## <a name="set-up-cash-flow-forecasts"></a>Konfigurere kontantstrømprognoser

Diagrammet **Kontantstrømprognose** inneholder kontoer for kontantstrøm, kontantstrømoppsett og kontantstrømprognoser. Noen er angitt, men du kan definere dine egne ved hjelp av en assistert installasjonsveiledningen. Veiledningen hjelper deg med å spesifisere ting som:

* Når salgsprognosen skal oppdateres
* Hvilke kontoer du skal basere den på
* Når du betaler skatt
* Om [Azure AI](https://azure.microsoft.com/overview/ai-platform/)  skal aktiveres.  

Kontantstrømprognoser kan bruke Azure AI for å skape en mer omfattende prognose. Tilkoblingen til Azure AI er allerede satt opp for deg. Du trenger bare å aktivere den. Når du logger deg på [!INCLUDE[prod_short](includes/prod_short.md)], en melding vises i en blå linje, og inneholder en kobling til kontantstrøm standardoppsettet. Varslingen viser bare én gang. Hvis du lukker den, men bestemmer deg for å aktivere Azure AI, kan du bruke veiledningen for assistert oppsett eller en manuell prosess.  

> [!NOTE]
>
> Du kan også bruke din egen prediktive webtjeneste. Hvis du vil ha mer informasjon, kan du se [Opprette og bruke funksjonen for forutsigbar webtjeneste for kontantstrømprognoser](#AnchorText).  

Slik bruker du den assisterte oppsettsveiledningen:  

1. I rollesenter for regnskapsfører, under diagrammet **Kontantstrømprognose**, velger du handlingen **Åpne assistert oppsett**.
2. Fyll ut feltene i hvert trinn av veiledningen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Tilbake i rollesenteret for regnskapsfører velger du handlingen **Omberegn prognose** under diagrammet **Kontantstrømprognose**.

Slik bruker du en manuell prosess:  

1. I rollesenteret for regnskapsfører velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontantstrømoppsett**, og velg deretter den relaterte koblingen.
2. Utvid **Azure Al**-hurtigfanen, og velg feltet **Azure AI aktivert**.
3. Tilbake i rollesenteret for regnskapsfører velger du handlingen **Omberegn prognose** under diagrammet **Kontantstrømprognose**.

> [!TIP]  
> Ta hensyn til lengden på periodene som tjenesten bruker i beregningene. Jo mer data du angir, jo mer nøyaktig vil forutsigelsene være. Vær også oppmerksom på store avvik i perioder. De vil også ha innvirkning på forutsigelser. Hvis Azure AI ikke finner nok data eller dataene varierer mye, vil ikke tjenesten utføre en forutsigelse.  

## <a name="design-details"></a>Designdetaljer

Abonnementer for [!INCLUDE[prod_short](includes/prod_short.md)] gir tilgang til flere prediktive webtjenester i alle områder der [!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig. Finn ut mer i lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/business-central/overview/)-nettstedet.

Disse webtjenestene er tilstandsløse, noe som betyr at de bare bruker data til å beregne forutsigelser etter behov. De lagrer ikke data.

> [!NOTE]
>
> Du kan bruke din egen prediktive webtjeneste i stedet for vår. Hvis du vil ha mer informasjon, kan du se [Opprette og bruke funksjonen for forutsigbar webtjeneste for kontantstrømprognoser](#AnchorText).

### <a name="data-required-for-forecast"></a>Data som kreves for prognose

For å lage prognoser om fremtidige inntekter og utgifter, krever webtjenester historiske data fra salg, leverandører og mva.

#### <a name="receivables"></a>Salg

Feltene **Forfallsdato** og **Beløp (LV)** på siden **Kundeposter**, der:

* Dokumenttypen er *Faktura* eller *Kreditnota*.
* Forfallsdatoen er mellom datoen som beregnes basert på verdiene i feltene **Historiske perioder** og **Periodetype** på siden **Kontantstrømoppsett** og arbeidsdatoen.

Før du bruker den forutsigbare webtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaksjoner etter **Forfallsdato** basert på verdien i feltet **Periodetype** på siden **Kontantstrømoppsett**.

#### <a name="payables"></a>Kjøp

Feltene **Forfallsdato** og **Beløp (LV)** på siden **Leverandørposter**, der:

* Dokumenttypen er *Faktura* eller *Kreditnota*.
* Forfallsdatoen er mellom datoen som beregnes basert på verdiene i feltene **Historiske perioder** og **Periodetype** på siden **Kontantstrømoppsett** og arbeidsdatoen.

Før du bruker den forutsigbare webtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaksjoner etter **Forfallsdato** basert på verdien i feltet **Periodetype** på siden **Kontantstrømoppsett**.

#### <a name="tax"></a>Avgift

Feltene **Dokumentdato** og **Beløp** på siden **Mva-poster (avgift)**, der:

* Dokumenttypen er *Salg*.
* Dokumentdatoen er mellom datoen som beregnes basert på verdiene i feltene **Historiske perioder** og **Periodetype** på siden **Kontantstrømoppsett** og arbeidsdatoen.

Før du bruker den forutsigbare webtjenesten, komprimerer [!INCLUDE[prod_short](includes/prod_short.md)] transaksjoner etter **Dokumentdato** basert på verdien i feltet **Periodetype** på siden **Kontantstrømoppsett**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Opprett og bruk funksjonen for forutsigbar webtjeneste for kontantstrømprognoser

For [!INCLUDE[prod_short](includes/prod_short.md)] online er modellen publisert av Microsoft og koblet til Microsoft-abonnementet. For andre distribusjonsalternativer må du opprette Machine Learning-ressurser i ditt eget Azure-abonnement. Du finner eksempeltrinn i [eksempelrepositoriet](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Formålet med denne oppgave er å få API-URI-en og API-nøkkelen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontantstrømoppsett**, og velg deretter den relaterte koblingen.  
2. Utvid hurtigfanen **Azure AI**, og fyll deretter ut feltene, inkludert nettadressen for API og API-nøkkelen som er oppgitt fra Azure Machine Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I rollesenteret for regnskapsfører velger du handlingen **Omberegn prognose** under diagrammet **Kontantstrømprognose**.

## <a name="see-also"></a>Se også

[Analyser kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Oversikt over prognose-APIer](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
