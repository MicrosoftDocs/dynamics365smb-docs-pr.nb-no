---
title: "Installere utvidelser for å tilpasse Dynamics 365 Business Central | Microsoft-dokumentasjon"
description: "Finn ut hvordan du legger til funksjoner og tilpasser Business Central ved å installere utvidelser."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e3c0dfdc1eb1739a1d756fcb359c99e51ceec1e7
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="customizing-business-central-using-extensions"></a>Tilpasse Business Central for med utvidelser
Du kan endre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.
Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, er noen utvidelser allerede installert for deg. Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.

Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard.
Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Du administrerer utvidelsene i vinduet **Administrasjon av utvidelse**. Du kan gå til dette vinduet fra Hjem. Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst høyre, angi **Utvidelse** og deretter velg den relaterte koblingen.  

> [!NOTE]  
>   Hvis du mener at du skal ha tilgang til en utvidelse, men ikke finner funksjonaliteten, kontrollerer du vinduet **Administrasjon av utvidelse**. Hvis utvidelsen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.  

## <a name="installing-an-extension"></a>Installere en utvidelse
Du kan få nye utvidelser fra markedsplassen på [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?src=dynamics365website&product=dynamics-365-business-central). Her kan du se alle tilgjengelige utvidelser for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan få apper, utvidelser og innholdspakker for andre Microsoft-produkter. Definer de aktuelle filtrene, ta en titt på informasjonen for hver utvidelse, og få en utvidelse for [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Administrasjon av utvidelse** kan du se utvidelsene som er installert, og du kan åpne vinduet **Markedsplass for utvidelser** som viser [!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelsene som for øyheblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Hvis du velger en utvidelse, kan du lese om hva utvidelsen gjør, og du kan få tilgang til hjelp for utvidelsen for å finne ut mer. Når du skaffer en utvidelse, må du godta vilkårene for bruk. Hvis du får utvidelsen fra webområdet for AppSource, logges du på [!INCLUDE[d365fin](includes/d365fin_md.md)] for å fullføre installasjonen.  

Når du installerer en utvidelse, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **PayPal Payment Standard for [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andre utvidelser legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.   

Hvis du avinstallerer en utvidelse og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en utvidelse som du har brukt, beholdes dataene, slik at hvis du installerer utvidelsen på nytt, er dataene fremdeles tilgjengelige.  

Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av [andre selskaper](ui-extensions-other.md). Alle utvidelser testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om utvidelsen før du velger å installere den.  

Microsoft tilbyr følgende utvidelser:  

* [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
* [Bankfeeder for Envestnet Yodlee](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)  
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)  
* [Ceridian lønn](ui-extensions-ceridian-payroll.md)  
* [Quickbooks Payroll-filimport](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)  
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)  
* [QuickBooks Online Data Migration](ui-extensions-quickbooks-online-data-migration.md)  
* [Regnskapsførerportal](ui-extensions-accountant-portal.md)  
* [Image Analyzer](ui-extensions-image-analyzer.md)  
* [Betalinger og avstemminger (Danmark)](ui-extensions-payments-reconciliation-formats-dk.md)  
* [C5 datamigrering](ui-extensions-c5-data-migration.md)  
* [Viktig forretningsinnsikt](ui-extensions-essential-business-insights.md)  
* [Prognose for forsinket betaling](ui-extensions-late-payment-prediction.md  )

> [!NOTE]  
>  Nye utvidelser er ikke tilgjengelige i AppSource like etter at vi har kunngjort en oppdatering. Du kan følge med på utvidelsene på [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Se også
[Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Aktivere kundebetalinger gjennom PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Komme i gang](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

