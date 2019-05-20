---
title: Konfigurere API-maler | Microsoft Docs
description: Beskrive trinnene du må gå gjennom for å konfigurere API-maler for Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: ef6b6d89ccea59de6a87c062cc6e29a27abe2c88
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245481"
---
# <a name="configuring-api-templates"></a>Konfigurere API-maler
API-biblioteket for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] gir en forenklet visning av de underliggende enhetene. Alle egenskapene i programmet vises ikke via det tilknyttede API-et. På **API-oppsett**-siden kan du definere maler som brukes til å fylle ut tomme egenskaper på en enhet når du oppretter en POST-handling gjennom API-et. 

Hvis for eksempel en konfigurasjonsmal er definert for vareenheten, når en ny varepost opprettes gjennom vare-API-et, blir egenskaper for den nye varen som ikke er definert i API-kallet, fylt ut fra den valgte malen. Hvis for eksempel ingen verdi er definert for **Bokføringsgruppe - vare**-feltet gjennom API-et, men en verdi er definert i den valgte malen, brukes bokføringsgruppeverdien som er definert i malen, for den nye varen. 

## <a name="setting-up-the-entity-template"></a>Definere enhetsmalen
Hvis du vil bruke maler med API-biblioteket, må du først konfigurere og definere egenskaper for malene. Du kan sette opp malene på siden **Konfigurasjonsmaler**. Hvis du vil ha mer informasjon, kan du se [Klargjøre for å flytte kundedata](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>Tilordne malen til et API

Hvis du vil tilordne en mal til et API, må du gå gjennom fremgangsmåten nedenfor.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **API-oppsett**, og velg den relaterte koblingen.
2. Velg **Ny**, og velg deretter **Rekkefølge**-verdien for posten.  
Hvis det er mer enn én mal som er valgt for et API (side-ID), brukes malene i rekkefølgen som er definert i **Rekkefølge**-kolonnen.   
Når hver mal er brukt, brukes bare feltverdiene som er definert i malen, på felt som ikke allerede har fått en verdi definert, enten eksplisitt i API-et eller i en mal som er brukt tidligere i rekkefølgen. 
3. Velg en verdi for **Side-ID**.  
Dette er siden for API-et som malen skal brukes på. **Side-ID**-oppslaget gir en oversikt over alle API-er som er tilgjengelige i biblioteket.
4. Velg en verdi i **Malkode**-feltet.  
Malkoden er koden for malen som ble definert på **Konfigurasjonsmaler**-siden. Malverdiene som er definert, brukes på API-et. 
5. I feltet **Betingelser** angir du hvilken mal som skal brukes.  
Den definerte malen brukes på en ny post som er opprettet gjennom API-et, hvis, og bare hvis, betingelsene som er definert i **Betingelser**-feltet er oppfylt av verdiene som allerede er definert for den nye forekomsten av enheten.

## <a name="see-also"></a>Se også
[API-dokumentasjon](/dynamics-nav/fin-graph)  
[Utvikle tilkoblingsapper for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Aktivere API-ene](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Endepunkt for API-ene](/dynamics-nav/endpoints-apis-for-dynamics)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)