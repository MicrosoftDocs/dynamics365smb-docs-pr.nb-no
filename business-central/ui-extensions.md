---
title: Tilpasse Business Central Online med apper
description: Finn ut alt om hvordan du legger til funksjoner og tilpasser Business Central ved å installere apper i denne artikkelen.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: bholtorf
---
# Tilpasse Business Central Online med apper

Du kan endre [!INCLUDE[prod_short](includes/prod_short.md)] Online ved å installere apper som for eksempel legger til funksjonalitet, endrer virkemåte eller gir deg tilgang til nye elektroniske tjenester. Disse appene kalles også *utvidelser* fordi de *utvider* [!INCLUDE [prod_short](includes/prod_short.md)].

## Administrer apper

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Når du starter [!INCLUDE[prod_short](includes/prod_short.md)] for første gang, er noen apper allerede installert for deg. Over tid gjøres flere apper tilgjengelig for deg, og du kan deretter velge om du vil bruke appen eller ikke.

Microsoft tilbyr for eksempel en app som kan gi integrering med PayPal Payments Standard. Denne utvidelsen er installert som standard. Hvis en annen utvidelse gjøres tilgjengelig som gir integrasjon med en annen betalingstjenesten, kan du installere den nye utvidelsen og deretter velger hvilke av de to tjenestene du vil bruke.  

Hvis du vil bruke funksjonaliteten fra en app, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av appen.

Du må ha de rette tillatelsene for å installere eller avinstallere apper fra AppSource eller legge til utvidelser per leietaker. Du må enten være medlem av **Adm. av D365-utv.**-brukergruppen eller ha tillatelsessettet **ADMINISTRASJON AV UTVIDELSE – ADMINISTRATOR** eksplisitt. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises kan du ikke laste opp per leier-utvidelser eller installere AppSource-apper via siden **Administrasjon av utvidelse**. Du kan ikke installere AppSource-apper lokalt, inkludert i Docker-baserte distribusjoner.

Du administrerer appene på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan også velge ikonet **Søk etter en side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre, angi **Utvidelse**, og deretter velge den relaterte koblingen. Hvis du vil ha mer informasjon, kan du se [Installere og avinstallere apper](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Hvis du mener at du skal ha tilgang til en app, men ikke finner funksjonaliteten, kontrollerer du siden **Administrasjon av utvidelse**. Hvis appen ikke er oppført der, kan du installere den, som beskrevet i delen nedenfor.  

> [!NOTE]  
> Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[prod_short](includes/prod_short.md)] Online. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også gå til markedsplassen fra [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Administrasjon av utvidelse** kan du se appene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[prod_short](includes/prod_short.md)]-appene som for øyeblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Hvis du velger en app, kan du lese om hva appen gjør, og du kan få tilgang til hjelp for appen for å finne ut mer. Når du skaffer en app, må du godta vilkårene for bruk. Hvis du får appen fra nettstedet for AppSource, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for å fullføre installasjonen.  

Når du installerer en app, må du kanskje konfigurere den, for eksempel angi en konto for bruk med utvidelsen **Paypal Payments Standard for [!INCLUDE[prod_short](includes/prod_short.md)]**.
Andre apper legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.   

Hvis du avinstallerer en app og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en app som du har brukt, beholdes dataene, slik at hvis du installerer appen på nytt, er dataene fremdeles tilgjengelige. Det er nødvendig med noen apper. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.  

Noen apper leveres av Microsoft, og andre apper leveres av [andre selskaper](ui-extensions-other.md). Alle apper testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver utvidelse, for å finne ut mer om appen før du velger å installere den.  

> [!NOTE]  
> Du kan holde øye med nye apper fra Microsoft og andre leverandører på [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## Apper og dataoverføring

siden følgende apper kommuniserer med andre tjenester, kan de overføre data fra det geografiske området for [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet:

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

## Koble til virksomheten

Fra og med lanseringsbølge 2 i 2022 kan nettbaserte miljøer for [!INCLUDE [prod_short](includes/prod_short.md)] vise en eller flere apper på sidene **Tilkoblingsapper** og **Bankapper**. Disse appene kan koble virksomheten til eksterne tjenester som øker produktiviteten ved å automatisere prosesser. Du kan for eksempel koble til banker og automatisk importere banktransaksjoner. Appene er enkle å installere og konfigurere direkte fra denne siden. Velg en app for å lære mer om funksjoner og priser.  

Vis listen over foreslåtte apper ved å velge handlingen **Tilkoblingsapper** på siden **Administrasjon av utvidelse**.  

> [!NOTE]
> Den første personen som åpner siden **Tilkoblingsapper**, må tillate at utvidelsen kobler til en ekstern tjeneste. Tillat tilkoblingen én gang eller alltid. Hvis du velger å sperre tilkoblingen, må du finne de aktuelle appene på AppSource.

Denne eksterne tjenesten vil generere en liste over relevante apper basert på ditt land eller område

## Anbefalte apper

Microsoft-partnere og -forhandlere kan opprette en app som de kan bruke til å kompilere lister over apper de ofte anbefaler til kundene sine. Hvis de gjør det og har distribuert appen til leietakeren din, er appene tilgjengelige på siden **Anbefalte apper**. Der kan du lese om hver app og avgjøre om du vil installere dem.

> [!NOTE]
> Hvis du er en Microsoft-partner eller -forhandler, og du er interessert i å tilby en liste over anbefalte apper, kan du se [Anbefale apper fra AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) i administrasjonsinnholdet.

## Se relatert [Microsoft-opplæring](/training/modules/customize-dynamics-365-business-central/)

## Se også

[Installer og avinstaller apper](ui-extensions-install-uninstall.md)  
[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-apper fra andre leverandører](ui-extensions-other.md)  
[Konfigurer Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md)  
[Overføre forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-apper fra andre leverandører](ui-extensions-other.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
