---
title: Installere utvidelser for å tilpasse Dynamics 365 Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du legger til funksjoner og tilpasser Business Central ved å installere utvidelser.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765924"
---
# <a name="customizing-business-central-using-extensions"></a>Tilpasse Business Central for med utvidelser

Du kan endre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.

> [!NOTE]
> Du må ha de rette tillatelsene for å installere utvidelser fra AppSource eller legge til utvidelser per leietaker. Du må enten være medlem av Adm. av D365-utv.-brukergruppen eller ha tillatelsessettet Adm. av D365-utv. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet.<br /><br />
Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

> [!IMPORTANT]  
> Det er ikke støtte for opplasting av per leier-utvidelser og installasjon av AppSource-utvidelser fra **Administrasjon av utvidelse**-siden for lokale installasjoner.

Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, er noen utvidelser allerede installert for deg. Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.

Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard.
Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Du administrerer utvidelsene på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre, angi **Utvidelse**, og deretter velge den relaterte koblingen. Hvis du vil ha mer informasjon, kan du se [Installere og avinstallere utvidelser](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener at du skal ha tilgang til en utvidelse, men ikke finner funksjonaliteten, kontrollerer du siden **Administrasjon av utvidelse**. Hvis utvidelsen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.  

> [!NOTE]  
> Nye utvidelser er ikke tilgjengelige i AppSource like etter at vi har kunngjort en oppdatering. Du kan følge med på utvidelsene på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="see-also"></a>Se også

[Utvide Dynamics 365 Business Central](about-develop-extensions.md)  
[Business Central-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Sett opp Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Aktivere kundebetalinger gjennom PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Komme i gang](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
