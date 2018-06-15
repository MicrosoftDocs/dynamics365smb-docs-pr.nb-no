---
title: Konfigurere API-maler | Microsoft Docs
description: "Beskrive trinnene du må gå gjennom for å konfigurere API-maler for Dynamics 365 Business Central."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: nb-no
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a>Konfigurere API-maler
API-biblioteket for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] gir en forenklet visning av de underliggende enhetene. Alle egenskapene i programmet vises ikke via det tilknyttede API-et. I **API-oppsett**-vinduet kan du definere maler som brukes til å fylle ut tomme egenskaper på en enhet når du oppretter en POST-handling gjennom API-et. 

Hvis for eksempel en konfigurasjonsmal er definert for vareenheten, når en ny varepost opprettes gjennom vare-API-et, blir egenskaper for den nye varen som ikke er definert i API-kallet, fylt ut fra den valgte malen. Hvis for eksempel ingen verdi er definert for **Bokføringsgruppe - vare**-feltet gjennom API-et, men en verdi er definert i den valgte malen, brukes bokføringsgruppeverdien som er definert i malen, for den nye varen. 

## <a name="setting-up-the-entity-template"></a>Definere enhetsmalen
Hvis du vil bruke maler med API-biblioteket, må du først konfigurere og definere egenskaper for malene. Du kan sette opp malene i vinduet **Konfigurasjonsmaler**. Hvis du vil ha mer informasjon, kan du se [Klargjøre for å flytte kundedata](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Tilordne malen til et API

Hvis du vil tilordne en mal til et API, må du gå gjennom fremgangsmåten nedenfor.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **API-oppsett**, og angi den relaterte koblingen.
2. Velg **Ny**, og velg deretter **Rekkefølge**-verdien for posten.  
Hvis det er mer enn én mal som er valgt for et API (side-ID), brukes malene i rekkefølgen som er definert i **Rekkefølge**-kolonnen.   
Når hver mal er brukt, brukes bare feltverdiene som er definert i malen, på felt som ikke allerede har fått en verdi definert, enten eksplisitt i API-et eller i en mal som er brukt tidligere i rekkefølgen. 
3. Velg en verdi for **Side-ID**.  
Dette er siden for API-et som malen skal brukes på. **Side-ID**-oppslaget gir en oversikt over alle API-er som er tilgjengelige i biblioteket.
4. Velg en verdi i **Malkode**-feltet.  
Malkoden er koden for malen som ble definert i **Konfigurasjonsmaler**-vinduet. Malverdiene som er definert, brukes på API-et. 
5. I feltet **Betingelser** angir du hvilken mal som skal brukes.  
Den definerte malen brukes på en ny post som er opprettet gjennom API-et, hvis, og bare hvis, betingelsene som er definert i **Betingelser**-feltet er oppfylt av verdiene som allerede er definert for den nye forekomsten av enheten.

## <a name="see-also"></a>Se også
[API-dokumentasjon](/dynamics-nav/fin-graph)  
[Utvikle tilkoblingsapper for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivere API-ene](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endepunkt for API-ene](/dynamics-nav/endpoints-apis-for-dynamics)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)
