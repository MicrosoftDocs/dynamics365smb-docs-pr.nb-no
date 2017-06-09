---
title: Tilpasse Dynamics 365 for Financials med utvidelser | Microsoft-dokumentasjon
description: Tilpasse Dynamics 365 for Financials med utvidelser
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize
ms.date: 04/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1de01d9944489f862dfc6db145c1542c3d0dd2e3
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="customizing-dynamics-365-for-financials-using-extensions"></a>Tilpasse Dynamics 365 for Financials med utvidelser
Du kan endre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.
Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, er noen utvidelser allerede installert for deg. Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.

Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard.
Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Du administrerer utvidelsene i vinduet **Administrasjon av utvidelse**. Du kan gå til dette vinduet fra Hjem. Du kan også velge ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport") i øvre høyre hjørne, angi **Utvidelse**, og deretter velger du den beslektede koblingen.  

**Merk**: Hvis du tror du skal ha tilgang til en annen filtype, men du finner ikke funksjonaliteten, må du kontrollere den vinduet **Administrasjon av utvidelse** - hvis utvidelsen ikke er oppført, kan du installere den som beskrevet i delen nedenfor.  

## <a name="installing-an-extension"></a>Installere en utvidelse
Du kan få nye utvidelser fra markedsplassen på [AppSource.microsoft.com](https://appsource.microsoft.com/). Her kan du se alle tilgjengelige utvidelser for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan få apper, utvidelser og innholdspakker for andre Microsoft-produkter. Definer de aktuelle filtrene, ta en titt på informasjonen for hver utvidelse, og få en utvidelse for [!INCLUDE[d365fin](includes/d365fin_md.md)].  
**Merk**: Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved hjelp av e postkontoen du bruker for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Administrasjon av utvidelse** kan du se utvidelsene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelsene som for øyheblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSource.microsoft.com](https://appsource.microsoft.com/).  

Hvis du velger en utvidelse, kan du lese om hva utvidelsen gjør, og du kan få tilgang til hjelp for utvidelsen for å finne ut mer. Når du skaffer en utvidelse, må du godta vilkårene for bruk. Hvis du får utvidelsen fra webområdet for AppSource, logges du på [!INCLUDE[d365fin](includes/d365fin_md.md)] for å fullføre installasjonen.  

Når du installerer en utvidelse, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **PayPal-betalingsstandard for [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andre utvidelser legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.   

Hvis du avinstallerer en utvidelse og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en utvidelse som du har brukt, beholdes dataene, slik at hvis du installerer utvidelsen på nytt, er dataene fremdeles tilgjengelige.  

Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av [andre selskaper](ui-extensions-other.md). Alle utvidelser testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om utvidelsen før du velger å installere den.  

Microsoft tilbyr følgende utvidelser:  

* [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
* [Bankfeeder for Envestnet Yodlee](ui-extensions-yodlee-bank-feeds.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)  
* [Salgs- og beholdningsprognose](ui-extensions-sales-forecast.md)  
* [Ceridian lønn](ui-extensions-ceridian-payroll.md)  
* [Quickbooks Payroll-filimport](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)

## <a name="see-also"></a>Se også
[Konfigurere bankfeedservicen Envestnet Yodlee](bank-how-setup-bank-statement-service.md)  
[Aktiver kundebetalinger gjennom PayPal](sales-how-enable-payment-service-extensions.md)  
[Overfør forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Utvidelser fra andre leverandører](ui-extensions-other.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
