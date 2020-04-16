---
title: Bruke Salgs- og lagerprognose-utvidelsen til lagerstyring | Microsoft-dokumentasjon
description: Utvidelsen bidrar til å forutsi salg, få en klar oversikt over forventet tomt lager, og hjelper deg til og med å opprette etterfyllingsforespørsler til leverandører.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: daff9e471ce62f4885703a1fd11bbf35620360f9
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189678"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Utvidelsen Salgs- og lagerprognose
Lagerstyring er en avveining mellom kundeservice og håndtering av kostnader. På den ene siden krever en lav beholdning mindre arbeidskapital, men på den annen side kan tomme lagre føre til tapt salg. Salgs- og lagerprognose-utvidelsen forutsier mulig salg ved hjelp av historiske data og gir en tydelig oversikt over forventet tomt lager. Basert på prognosen hjelper utvidelsen med å opprette etterfyllingsforespørsler til leverandørene og sparer deg for tid.  

## <a name="setting-up-forecasting"></a>Sette opp prognoser
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er tilkoblingen til [Azure AI](https://azure.microsoft.com/overview/ai-platform/) allerede satt opp for deg. Men du kan konfigurere prognosen til å bruke en annen type periode å rapportere etter, for eksempel endre fra prognose etter måned til prognose etter kvartal. Du kan også velge antall perioder som prognosene skal beregnes for, avhengig av hvor detaljert du vil at prognosen skal være. Vi foreslår at du lager månedlige prognoser, og med en 12 måneders horisont for prognosen. 

> [!TIP]  
>   Ta hensyn til lengden på periodene som tjenesten bruker i beregningene. Jo mer data du angir, jo mer nøyaktig vil forutsigelsene være. Vær også oppmerksom på store avvik i perioder. De vil også ha innvirkning på forutsigelser. Hvis Azure AI ikke finner nok data eller dataene varierer mye, vil ikke tjenesten utføre en forutsigelse.

## <a name="using-the-forecasts"></a>Bruke prognosene
Utvidelsen bruker Azure AI til å forutse fremtidige salg basert på din salgshistorikk for å unngå for liten lagerbeholdning. Når du for eksempel velger en vare på siden **Varer**, viser diagrammet i **Vareprognose**-ruten beregnet salg av denne varen i den kommende perioden. På denne måten kan du se om det er sannsynlig at du snart går tom for varen på lageret.  

Du kan også bruke utvidelsen til å foreslå når lageret bør fylles på. Hvis du for eksempel oppretter en bestilling for Fabrikam fordi du vil kjøpe deres nye skrivebordsstol, foreslår Salgs- og lagerprognose-utvidelsen at du også fyller på med LONDON-svingstolen som du vanligvis kjøper fra denne leverandøren. Dette er fordi utvidelsen forutsier at du vil gå tom for LONDON-svingstolen i løpet av de neste to månedene, og at du kanskje vil bestille flere stoler allerede nå.  

## <a name="design-details"></a>Designdetaljer
Abonnementer for [!INCLUDE[d365fin](includes/d365fin_md.md)] gir tilgang til flere prediktive webtjenester i alle områder der [!INCLUDE[d365fin](includes/d365fin_md.md)] er tilgjengelig. Hvis du vil ha mer informasjon, kan du se lisensveiledningen for Microsoft Dynamics 365 Business Central. Veiledningen er tilgjengelig for nedlasting på [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/)-nettstedet. 

Disse webtjenestene er tilstandsløse, noe som betyr at de bare bruker data til å beregne forutsigelser etter behov. De lagrer ikke data.

> [!NOTE]  
>   Du kan også bruke din egen prediktive webtjeneste i stedet for vår. Hvis du vil ha mer informasjon, kan du se [Opprette og bruke din egen forutsigbare webtjeneste for salgs- og lagerprognose](#AnchorText). 

### <a name="data-required-for-forecast"></a>Data som kreves for prognose
For å lage prognoser om fremtidig salg, krever webtjenesten kvantitative data om tidligere salg. De dataene kommer fra feltene **Bokføringsdato**, **Varenr.** og **Antall** på siden **Vareposter**, der:
-    Posttypen er Salg.
- Bokføringsdatoen er mellom datoen som beregnes basert på verdiene i feltene **Historiske perioder** og **Periodetype** på siden **Oppsett for salgs- og varelagerprognose** og arbeidsdatoen.

Før webtjenesten brukes, komprimerer [!INCLUDE[d365fin](includes/d365fin_md.md)] transaksjoner etter **Varenr.** og **Bokføringsdato** basert på verdien i feltet **Periodetype** på siden **Oppsett for salgs- og varelagerprognose**.

## <a name="create-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Opprette og bruke din egen forutsigbare webtjeneste for salgs- og lagerprognose
Du kan også opprette din egen prediktive webtjeneste basert på en felles modell som heter **Prognosemodell for Microsoft Business Central**. Denne prediktive modellen er tilgjengelig elektronisk i Azure AI-galleriet. Hvis du vil bruke modellen, følger du denne fremgangsmåten:  

1. Åpne en nettleser, og gå til [Azure AI-galleri](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Søk etter **Prognosemodell for Microsoft Business Central**, og åpne deretter modellen i Azure Machine Learning Studio.  
3. Bruke Microsoft-kontoen til å registrere deg for et arbeidsområde, og kopier deretter modellen.  
4. Kjør modellen, og publisere den som en webtjeneste.  
5. Noter URL-API og API-nøkkel. Du vil bruke disse legitimasjonene for et oppsett for kontantstrømprognoser.  
6. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for salgs- og varelagerprognose**, og velg deretter den relaterte koblingen.  
7. Utvid hurtigfanen **Generelt**, og fyll deretter ut feltene URL-adresse for API og API-nøkkel.  


## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
