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
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 0b1353631aa9e727c25fd6e47dcb7f5699f3e9e1
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877090"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Utvidelsen Salgs- og lagerprognose
Lagerstyring er en avveining mellom kundeservice og håndtering av kostnader. På den ene siden krever en lav beholdning mindre arbeidskapital, men på den annen side kan tomme lagre føre til tapt salg. Salgs- og lagerprognose-utvidelsen forutsier mulig salg ved hjelp av historiske data og gir en tydelig oversikt over forventet tomt lager. Basert på prognosen hjelper utvidelsen med å opprette etterfyllingsforespørsler til leverandørene og sparer deg for tid.  

## <a name="setting-up-forecasting"></a>Sette opp prognoser
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er tilkoblingen til [Azure AI](https://azure.microsoft.com/overview/ai-platform/) allerede satt opp for deg. Men du kan konfigurere prognosen til å bruke en annen type periode å rapportere etter, for eksempel endre fra prognose etter måned til prognose etter kvartal. Du kan også velge antall perioder som prognosene skal beregnes for, avhengig av hvor detaljert du vil at prognosen skal være. Vi foreslår at du lager månedlige prognoser, og med en 12 måneders horisont for prognosen.  

## <a name="using-the-forecasts"></a>Bruke prognosene
Utvidelsen bruker Azure AI til å forutse fremtidige salg basert på din salgshistorikk for å unngå for liten lagerbeholdning. Når du for eksempel velger en vare på siden **Varer**, viser diagrammet i **Vareprognose**-ruten beregnet salg av denne varen i den kommende perioden. På denne måten kan du se om det er sannsynlig at du snart går tom for varen på lageret.  

Du kan også bruke utvidelsen til å foreslå når lageret bør fylles på. Hvis du for eksempel oppretter en bestilling for Fabrikam fordi du vil kjøpe deres nye skrivebordsstol, foreslår Salgs- og lagerprognose-utvidelsen at du også fyller på med LONDON-svingstolen som du vanligvis kjøper fra denne leverandøren. Dette er fordi utvidelsen forutsier at du vil gå tom for LONDON-svingstolen i løpet av de neste to månedene, og at du kanskje vil bestille flere stoler allerede nå.  

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
