---
title: Installere og avinstallere utvidelser i Business Central | Microsoft Docs
description: Finn ut hvordan du installerer og avinstallerer utvidelser i Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 06/03/2021
ms.author: solsen
ms.openlocfilehash: 09d1998bcd8cdf522b1533fe4768a0bbf0aca776
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435039"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Installere og avinstallere utvidelser i Business Central

Du kan endre [!INCLUDE[prod_short](includes/prod_short.md)] ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåten eller gir deg tilgang til nye elektroniske tjenester. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central med utvidelser](ui-extensions.md).

> [!NOTE]
> Du må ha de rette tillatelsene for å installere utvidelser fra AppSource eller legge til utvidelser per leietaker. Du må enten være et medlem av ADMINISTRASJON AV UTVIDELSE - ADMINISTRATOR-brukergruppen, eller du må ha UTVIDELSE UTVIDELSE - ADMINISTRATOR-tillatelsessettet. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet.
>
> Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

> [!NOTE]  
> Tillatelsessettet **ADMINISTRASJON AV UTVIDELSE – ADMINISTRATOR** ble introdusert i lanseringsbølge 1 for Business Central 2021 som erstatning for tillatelsessettet **ADMINISTRASJON AV D365-UTVIDELSE** angitt i tidligere versjoner.

## <a name="installing-an-extension"></a>Installere en utvidelse

Du administrerer utvidelser på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan ogs å velge ikonet **Søk etter side eller rapport** ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi i øvre høyre hjørne **Utvidelse**, og deretter velger du den relaterte koblingen.  

Du kan få nye utvidelser fra markedsplassen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Her kan du se alle tilgjengelige utvidelser for [!INCLUDE[prod_short](includes/prod_short.md)], og du kan få apper, utvidelser og innholdspakker for andre Microsoft-produkter. Definer de aktuelle filtrene, ta en titt på informasjonen for hver utvidelse, og få en utvidelse for [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[prod_short](includes/prod_short.md)]. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Administrasjon av utvidelse** kan du se utvidelsene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[prod_short](includes/prod_short.md)]-utvidelsene som for øyeblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSourceAppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Hvis du velger en utvidelse, kan du lese om hva utvidelsen gjør, og du kan få tilgang til hjelp for utvidelsen for å finne ut mer. Når du skaffer en utvidelse, må du godta vilkårene for bruk. Hvis du får utvidelsen fra webområdet for AppSource, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for å fullføre installasjonen.  

Når du installerer en utvidelse, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **PayPal Payment Standard for [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andre utvidelser legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.

Hvis du avinstallerer en utvidelse og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en utvidelse som du har brukt, beholdes dataene, slik at hvis du installerer utvidelsen på nytt, er dataene fremdeles tilgjengelige. Det er nødvendig med noen utvidelser. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.

Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av [andre selskaper](ui-extensions-other.md). Alle utvidelser testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om utvidelsen før du velger å installere den.

Microsoft tilbyr følgende utvidelser:

* [AMC Banking 365 Fundamentals-utvidelse](ui-extensions-amc-banking.md)
* [Ceridian lønn](ui-extensions-ceridian-payroll.md)
* [Selskapshub](ui-extensions-company-hub.md)  
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
* [Mva-gruppe](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Dansk – C5 datamigrering](ui-extensions-c5-data-migration.md)
* [Dansk – Betalinger og avstemminger](ui-extensions-payments-reconciliation-formats-dk.md)
* [Dansk – TAX-filformat](ui-extensions-tax-file-formats-dk.md)
* [GetAddress.io UK Postcodes-utvidelsen](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA – Send remitteringsønske](ui-extensions-send-remittance-advice.md)

## <a name="uninstalling-an-extension"></a>Avinstallere en utvidelse

Du avinstallerer en utvidelse ved å bruke siden **Administrasjon av utvidelse**. Hvis du avinstallerer en utvidelse og deretter ombestemmer deg, kan du installere utvidelsen på nytt. Når du avinstallerer en utvidelse du har brukt, beholdes dataene som standard, slik at hvis du installerer den på nytt, er dataene fremdeles tilgjengelige. Du kan i stedet velge å slette dataene med utvidelsen. Du kontrollerer dette med alternativet **Slett utvidelsesdata**. Denne alternativet er som standard *ikke aktivert*.

> [!IMPORTANT]  
> Hvis du merker av for alternativet **Slett utvidelsesdata**, vises en bekreftelsesdialogboks der du må velge **OK**. Når det er merket av for **Slett utvidelsesdata**, kan du nå avinstallere utvidelsen. Du blir da bedt om å bekrefte på nytt at du vil avinstallere utvidelsen og slette dataene. Du kan ikke angre denne handlingen.
Noen utvidelser er nødvendige. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.  

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Aktivere kundebetalinger gjennom PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]