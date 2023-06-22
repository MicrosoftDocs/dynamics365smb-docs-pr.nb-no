---
title: Installer og avinstaller apper
description: Finn ut hvordan du installerer og avinstallerer apper og utvidelser i Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 20350'
ms.date: 09/22/2022
ms.author: solsen
---

# <a name="install-and-uninstall-extensions-apps-in-business-central" />Installer og avinstaller utvidelser (apper) i Business Central

Du kan endre [!INCLUDE[prod_short](includes/prod_short.md)] ved å installere apper som for eksempel legger til funksjonalitet, endrer virkemåten eller gir deg tilgang til nye elektroniske tjenester. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central med utvidelser](ui-extensions.md).

> [!NOTE]
> Du må ha de rette tillatelsene for å installere eller avinstallere apper fra AppSource eller legge til apper per leietaker. Du må enten være et medlem av ADMINISTRASJON AV UTVIDELSE - ADMINISTRATOR-brukergruppen, eller du må ha UTVIDELSE UTVIDELSE - ADMINISTRATOR-tillatelsessettet. Hvis du er administrator, kan du tilordne brukergrupper og -tillatelser til andre brukere i selskapet.
>
> Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

Hvis du vil bruke funksjonaliteten fra en utvidelse, for eksempel åpne sider, kjøre rapporter, velge handlinger og så videre, må du være tilordnet tillatelsessettene som er installert som en del av utvidelsen.

## <a name="a-nameinstallainstall-an-extension" /><a name="install"></a>Installere en utvidelse

Du administrerer appene og utvidelsene på siden **Administrasjon av utvidelse**. Du kan gå til denne siden fra Hjem. Du kan ogs å velge ikonet **Søk etter side eller rapport** ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi i øvre høyre hjørne **Utvidelse**, og deretter velger du den relaterte koblingen.  

Du kan få nye apper fra markedsplassen på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Markedsplass tilbyr alle tilgjengelige apper for [!INCLUDE[prod_short](includes/prod_short.md)] i tillegg til apper og innholdspakker for andre Microsoft-produkter. Definer de aktuelle filtrene, ta en titt på informasjonen for hver utvidelse, og få en utvidelse for [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Logg på [AppSource.microsoft.com](https://appsource.microsoft.com/) ved å bruke e-postkontoen du bruker med [!INCLUDE[prod_short](includes/prod_short.md)]. Bruk samme e-postkonto for andre tjenester og produkter for en problemfri opplevelse.  

Du kan også hente til AppSource fra [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Administrasjon av utvidelse** kan du se appene som er installert, og du kan åpne **Markedsplass for utvidelser**-siden som viser [!INCLUDE[prod_short](includes/prod_short.md)]-appene som for øyeblikket er tilgjengelige i AppSource. Hvis du velger *Flere apper*-koblingen, kommer du til [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Hvis du velger en app, kan du lese om hva appen gjør, og du kan få tilgang til hjelp for appen for å finne ut mer. Når du skaffer en app, må du godta vilkårene for bruk. Hvis du får appen fra nettstedet for AppSource, logges du på [!INCLUDE[prod_short](includes/prod_short.md)] for å fullføre installasjonen.  

Når du har installert en app, må du kanskje konfigurere den. Noen apper krever at du oppgir opplysninger før du kan bruke dem. Når du for eksempel har installert **Paypal Payments Standard**-appen, må du angi e-post- eller forhandlerkonto-ID-en for en PayPal-konto. Hvis du vil sette opp en app, eller finne ut hvilken informasjon du trenger, velger du **Oppsett**-handlingen på siden **Installerte utvidelser**.  

Andre apper legger for eksempel ganske enkelt til felt på en eksisterende side, eller de legger til en ny side.

Hvis du avinstallerer en app og du deretter ombestemmer deg, kan du installere den på nytt. Når du avinstallerer en app som du har brukt, beholdes dataene, slik at hvis du installerer appen på nytt, er dataene fremdeles tilgjengelige. Det er nødvendig med noen apper. Du nektes å avinstallere disse appene fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.

Noen apper leveres av Microsoft, og andre apper leveres av [andre selskaper](ui-extensions-other.md). Alle apper testes før de blir gjort tilgjengelige for deg, men vi anbefaler at du går til de angitte koblingene som følger med hver app, for å finne ut mer om appen før du velger å installere den.

Microsoft tilbyr følgende apper:

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
* [QuickBooks Payroll-filimport](ui-extensions-quickbooks-payroll.md)
* [Salgs- og lagerprognose](ui-extensions-sales-forecast.md)
* [Mva-gruppe](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Dansk – C5 datamigrering](ui-extensions-c5-data-migration.md)
* [Dansk – Betalinger og avstemminger](ui-extensions-payments-reconciliation-formats-dk.md)
* [Dansk – TAX-filformat](ui-extensions-tax-file-formats-dk.md)
* [GetAddress.io UK Postcodes-utvidelsen](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [US/CA/UK/AU/NZ/ZA – Send remitteringsønske](ui-extensions-send-remittance-advice.md)

## <a name="set-up-an-app" />Konfigurere en utvidelse
Når du har installert en app, må du kanskje konfigurere den. For eksempel for **PayPal Payments Standard for [!INCLUDE[prod_short](includes/prod_short.md)]**-appen må du angi PayPal-kontoen du vil bruke. Hvis det er tilfellet, når installasjonen er fullført, spør [!INCLUDE[prod_short](includes/prod_short.md)] om du vil sette opp appen umiddelbart. Oppsett kan kreves for at appen skal fungere eller være valgfri.

Hvis du velger å sette opp appen med en gang og den har et nødvendig oppsett, åpner [!INCLUDE[prod_short](includes/prod_short.md)] det nødvendige oppsettet. Oppsettet kan enten være en side der du kan skrive inn informasjon, eller en veiledning for assistert oppsett som hjelper deg gjennom trinnene. Hvis du ikke fullfører oppsettet med en gang, kan du bruke **Oppsett for _navn på app_**-siden, som viser alle oppsett for appen. Obligatoriske oppsett angitt av **fete bokstaver**.

## <a name="upload-a-per-tenant-extension-pte" />Last opp en per leietaker-utvidelse (PTE)

Du laster opp en PTE med siden **Utvidelsesbehandling**. På siden **Utvidelsesbehandling** går du til **Administrer** og velger **Last opp utvidelse**. På **siden Last opp og distribuer utvidelse** angir du .app-filen som skal lastes opp. Hvis du vil fortsette, velger du **Godta**-knappen og deretter **Distribuer**-knappen. Dette starter prosessen med å distribuere PTE-en.

Hvis PTE inneholder endringer i skiftede skjemaer, er det mulig å *fremtvinge* en opplasting av det. Dette gjør du ved å velge alternativet **Fremtving** i **Synkroniseringsmodus for skjema**. Du får en bekreftelsesdialogboks for å godta før du fortsetter.  

## <a name="uninstall-an-app" />Avinstallere en app

Du avinstallerer en app ved å bruke siden **Administrasjon av utvidelse**. Hvis du vil avinstallere en app, merker du den på siden og velger deretter handlingen **Avinstaller**. Hvis du avinstallerer en app og deretter ombestemmer deg, kan du installere appen på nytt.

Når du avinstallerer en app du har brukt, beholdes dataene som standard hvis du installerer appen på nytt. Du kan i stedet velge å slette dataene med appen. Denne operasjonen styres av bryteren **Slett utvidelsesdata**. Denne bryteren er **av** som standard. Når du prøver å aktivere bryteren **Slett utvidelsesdata** for appen, får du en bekreftelsesdialogboks, og du må velge **Ja** for å aktivere den. Når bryteren **Slett utvidelsesdata** er aktivert, kan du avinstallere appen. Du blir da bedt om å bekrefte på nytt at du vil avinstallere appen og slette dataene.

> [!IMPORTANT]  
> - Det kan være andre apper som krever eller er avhengige av appen du vil avinstallere, for å kunne fungere. Disse andre appene kalles *avhengigheter*. Du kan ikke avinstallere en app med mindre avhengighetene også avinstalleres.
> - Når du velger å avinstallere en app som har en eller flere avhengigheter, vises en bekreftelsesdialogboks med en oversikt over avhengighetene, og du blir spurt om du vil avinstallere appen og alle tilhørende avhengighetene. Du må velge **Ja** for å fortsette.
> - Hvis du aktiverer bryteren **Slett utvidelsesdata**, vil avinstallasjon av appen slette alle data for appen **pluss** data for alle avhengige apper. Du kan ikke angre denne handlingen.
> - Noen apper er nødvendige. Du nektes å avinstallere disse fra siden for **Administrasjon av utvidelse**. Hvis du prøver, vises en feilmelding.  

## <a name="see-also" />Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Business Central-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Aktivere kundebetalinger gjennom PayPal](sales-how-enable-payment-service-extensions.md)  
[Overføre forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere GetAddress.io UK Postal Code-utvidelsen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-utvidelser fra andre leverandører](ui-extensions-other.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
