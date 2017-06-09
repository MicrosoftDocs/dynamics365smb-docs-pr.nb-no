---
title: Salgs- og lagerprognose | Microsoft-dokumentasjon
description: Inneholder informasjon om Salgs- og lagerprognose-utvidelsen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ebaea8b98264e981f9ad2e0abda592e2e4a72427
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Salgs- og lagerprognose for Dynamics 365 for Financials
Lagerstyring er en avveining mellom kundeservice og håndtering av kostnader. På den ene siden krever en lav beholdning mindre arbeidskapital, men på den annen side kan tomme lagre føre til tapt salg. Salgs- og lagerprognose-utvidelsen forutsier mulig salg ved hjelp av historiske data og gir en tydelig oversikt over forventet tomt lager. Basert på prognosen hjelper utvidelsen med å opprette etterfyllingsforespørsler til leverandørene og sparer deg for tid.  

## <a name="setting-up-forecasting"></a>Sette opp prognoser
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er tilkoblingen til [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) allerede satt opp for deg. Men du kan konfigurere prognosen til å bruke en annen type periode å rapportere etter, for eksempel endre fra prognose etter måned til prognose etter kvartal. Du kan også velge antall perioder som prognosene skal beregnes for, avhengig av hvor detaljert du vil at prognosen skal være. Vi foreslår at du lager månedlige prognoser, og med en 12 måneders horisont for prognosen.  

## <a name="using-the-forecasts"></a>Bruke prognosene
Utvidelsen bruker Cortana Intelligence til å forutse fremtidige salg basert på din salgshistorikk for å unngå for liten lagerbeholdning. Når du for eksempel velger en vare i **Varer**-vinduet, viser diagrammet i **Vareprognose**-ruten beregnet salg av denne varen i den kommende perioden. På denne måten kan du se om det er sannsynlig at du snart går tom for varen på lageret.  

Du kan også bruke utvidelsen til å foreslå når lageret bør fylles på. Hvis du for eksempel oppretter en bestilling for Fabrikam fordi du vil kjøpe deres nye skrivebordsstol, foreslår Salgs- og lagerprognose-utvidelsen at du også fyller på med LONDON-svingstolen som du vanligvis kjøper fra denne leverandøren. Dette er fordi utvidelsen forutsier at du vil gå tom for LONDON-svingstolen i løpet av de neste to månedene, og at du kanskje vil bestille flere stoler allerede nå.  

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av tillegg] (ui-extensions.md)  

