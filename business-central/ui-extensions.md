---
title: Tilpasse Business Central Online med utvidelser
description: Finn ut alt hvordan du legger til funksjoner og tilpasser Business Central ved å installere utvidelser her.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 8ff68bbeb2d7603b1c4d1b612413279cca5eec86
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530462"
---
# <a name="customizing-business-central-online-using-extensions"></a>Tilpasse Business Central Online med utvidelser

Du kan endre [!INCLUDE[prod_short](includes/prod_short.md)] Online ved å installere utvidelser som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester.

> [!NOTE]
> Du må ha de rette tillatelsene for å installere eller avinstallere utvidelser fra AppSource eller legge til utvidelser per leietaker. Du må enten være medlem av **Adm. av D365-utv.**-brukergruppen eller ha tillatelsessettet **ADMINISTRASJON AV UTVIDELSE – ADMINISTRATOR** eksplisitt. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).  
>
> Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Det er ikke støtte for opplasting av per leier-utvidelser og installasjon av AppSource-utvidelser fra **Administrasjon av utvidelse**-siden for lokale installasjoner. Du kan ikke installere AppSource-utvidelser lokalt, inkludert i Docker-baserte distribusjoner.

Når du starter [!INCLUDE[prod_short](includes/prod_short.md)] for første gang, er noen utvidelser allerede installert for deg. Over tid gjøres flere utvidelser tilgjengelig for deg, og du kan deretter velge om du vil bruke utvidelsen eller ikke.

Microsoft tilbyr for eksempel en utvidelse som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard.
Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Du administrerer utvidelsene på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre, angi **Utvidelse**, og deretter velge den relaterte koblingen. Hvis du vil ha mer informasjon, kan du se [Installere og avinstallere utvidelser](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener at du skal ha tilgang til en utvidelse, men ikke finner funksjonaliteten, kontrollerer du siden **Administrasjon av utvidelse**. Hvis utvidelsen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.  

> [!NOTE]  
> Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[prod_short](includes/prod_short.md)] Online. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Administrasjon av utvidelse** kan du se utvidelsene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[prod_short](includes/prod_short.md)]-utvidelsene som for øyeblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Hvis du velger en utvidelse, kan du lese om hva utvidelsen gjør, og du kan få tilgang til hjelp for utvidelsen for å finne ut mer. Når du skaffer en utvidelse, må du godta vilkårene for bruk. Hvis du får utvidelsen fra webområdet for AppSource, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for å fullføre installasjonen.  

Når du installerer en utvidelse, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **PayPal Payment Standard for [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andre utvidelser legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.   

Hvis du avinstallerer en utvidelse og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en utvidelse som du har brukt, beholdes dataene, slik at hvis du installerer utvidelsen på nytt, er dataene fremdeles tilgjengelige. Det er nødvendig med noen utvidelser. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.  

Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av [andre selskaper](ui-extensions-other.md). Alle utvidelser testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om utvidelsen før du velger å installere den.  

> [!NOTE]  
> Du kan holde øye med nye utvidelser fra Microsoft og andre leverandører på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Utvidelser og dataoverføring

siden følgende utvidelser kommuniserer med andre tjenester, kan de overføre data fra det geografiske området for [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet:

* AMC Banking 365 Fundamentals-utvidelse
* Bildeanalyse
* Prognose for forsinket betaling
* PayPal Payments Standard
* Salgs- og lagerprognose
* WorldPay Payments Standard

Dette gjelder også for enkelte funksjoner i basisprogrammet, for eksempel følgende funksjoner:

* Kontantstrømprognose
* Dokumentutvekslingstjeneste
* Dataverse-tilkoblinger
* OCR-tjeneste
* Online Map
* EU-mva.-reg.nr. Tjeneste

## <a name="recommended-apps"></a>Anbefalte apper
Microsoft-partnere og -forhandlere kan opprette en utvidelse som de kan bruke til å kompilere lister over apper de ofte anbefaler til kundene sine. Hvis de gjør det og har distribuert utvidelsen til leietakeren din, er appene tilgjengelige på siden **Anbefalte apper**. Der kan du lese om hver app og avgjøre om du vil installere dem.

> [!NOTE]
> Hvis du er en Microsoft-partner eller -forhandler, og du er interessert i å tilby en liste over anbefalte apper, kan du se [Anbefale apper fra AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Installer og avinstaller utvidelser](ui-extensions-install-uninstall.md)  
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
