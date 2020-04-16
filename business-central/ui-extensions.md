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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 15f88c2ab05914db71820d45c6326af36235a9d2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193542"
---
# <a name="customizing-business-central-using-extensions"></a>Tilpasse Business Central for med utvidelser
Du kan endre [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.

> [!NOTE]
> Du må ha de rette tillatelsene for å installere utvidelser fra AppSource eller legge til utvidelser per leietaker. Du må enten være medlem av Adm. av D365-utv.-brukergruppen eller ha tillatelsessettet Adm. av D365-utv. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet.<br /><br />
Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

Når du starter [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, er noen utvidelser allerede installert for deg. Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.

Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard.
Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Du administrerer utvidelsene på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre, angi **Utvidelse**, og deretter velge den relaterte koblingen.  

> [!NOTE]  
>   Hvis du mener at du skal ha tilgang til en utvidelse, men ikke finner funksjonaliteten, kontrollerer du siden **Administrasjon av utvidelse**. Hvis utvidelsen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.  

## <a name="installing-an-extension"></a>Installere en utvidelse
Du kan få nye utvidelser fra markedsplassen på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1). Her kan du se alle tilgjengelige utvidelser for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan få apper, utvidelser og innholdspakker for andre Microsoft-produkter. Definer de aktuelle filtrene, ta en titt på informasjonen for hver utvidelse, og få en utvidelse for [!INCLUDE[d365fin](includes/d365fin_md.md)].  
> [!NOTE]  
>   Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. På siden **Administrasjon av utvidelse** kan du se utvidelsene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[d365fin](includes/d365fin_md.md)]-utvidelsene som for øyeblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Hvis du velger en utvidelse, kan du lese om hva utvidelsen gjør, og du kan få tilgang til hjelp for utvidelsen for å finne ut mer. Når du skaffer en utvidelse, må du godta vilkårene for bruk. Hvis du får utvidelsen fra webområdet for AppSource, logges du på [!INCLUDE[d365fin](includes/d365fin_md.md)] for å fullføre installasjonen.  

Når du installerer en utvidelse, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **PayPal Payment Standard for [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Andre utvidelser legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.   

Hvis du avinstallerer en utvidelse og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en utvidelse som du har brukt, beholdes dataene, slik at hvis du installerer utvidelsen på nytt, er dataene fremdeles tilgjengelige. Det er nødvendig med noen utvidelser. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.  

Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av [andre selskaper](ui-extensions-other.md). Alle utvidelser testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om utvidelsen før du velger å installere den.  

Microsoft tilbyr følgende utvidelser:  

* [Regnskapsførerportal for Business Central](ui-extensions-accountant-portal.md)
* [Ceridian lønn](ui-extensions-ceridian-payroll.md)
* [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Viktig forretningsinnsikt](ui-extensions-essential-business-insights.md)
* [Bildeanalyse](ui-extensions-image-analyzer.md)
* [Intelligent sky](ui-extensions-data-replication.md)
* [Intelligent skybase](ui-extensions-intelligent-cloud.md)
* [Prognose for forsinket betaling](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online-datamigrering](ui-extensions-quickbooks-online-data-migration.md)
* [Quickbooks Payroll-filimport](ui-extensions-quickbooks-payroll.md)
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [Dansk – C5 datamigrering](ui-extensions-c5-data-migration.md)
* [Dansk – Betalinger og avstemminger](ui-extensions-payments-reconciliation-formats-dk.md)
* [Dansk – TAX-filformat](ui-extensions-tax-file-formats-dk.md)
* [Storbritannia – GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
* [US/CA/UK/AU/NZ/ZA – Send remitteringsønske](ui-extensions-send-remittance-advice.md)
* [Business Central-utvidelser fra andre leverandører](ui-extensions-other.md)

> [!NOTE]  
>  Nye utvidelser er ikke tilgjengelige i AppSource like etter at vi har kunngjort en oppdatering. Du kan følge med på utvidelsene på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

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
