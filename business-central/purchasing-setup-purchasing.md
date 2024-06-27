---
title: Oversikt over oppgaver for å definere kjøp
description: Beskriver oppgaver for å definere selskapets innkjøpspolicyer og definere kjøpsprosessene.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Definere kjøp

Før du kan håndtere kjøpsprosesser, må du konfigurere regler og verdier som definerer selskapets kjøpsprinsipper.

Du må definere det generelle oppsettet på siden **Kjøpsoppsett**, som vanligvis gjøres én gang under den første implementeringen. Finn ut mer i følgende del, [Kjøpsoppsett](#purchases-and-payables-setup).

En egen rekke oppgaver relatert til registrering av nye leverandører er å registrere alle spesialpris eller rabattavtaler som du har med hver leverandør.

Finansrelatert kjøpsoppsett, for eksempel betalingsmåte og valutaer, beskrives i avsnittet Finansoppsett. Finn ut mer under [Konfigurer finans](finance-setup-finance.md). På samme måte kan du finne lagerrelaterte kjøpsoppsett, for eksempel enheter og varesporingskoder, i [delen Lageroppsett](inventory-setup-inventory.md).

## Kjøpsoppsett

Før du arbeider med kjøp, må du angi på siden **Kjøpsoppsett** hvordan kjøpsverdier bokføres, og nummerserien som brukes for leverandører og kjøpsdokumenter.

### Generelle innstillinger

På hurtigfanen **Generelt** angir du alternativer, for eksempel hvordan du vil beregne og bokføre rabatter, og om du vil avrunde fakturabeløp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Noen felter krever spesielt oppmerksomhet, for eksempel feltet **Beregn fakturarabatt per mva-type**, som angir om fakturarabatten beregnes i henhold til mva-typen eller fakturaens totalbeløp. Finn ut mer under [Kombiner mva-bokføringsgrupper i mva-bokføringsoppsett](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups).

På samme måte kan feltet **Utligning mellom valutaer** gi små avrundingsdifferanser når poster i forskjellige valutaer utlignes mot hverandre. Finn ut mer under [Aktivere utligning av kundeposter i forskjellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).

Noen felter endrer i tillegg virkemåten sine eller avhenger av hvordan andre felter angis. Funksjonen **Kontroller forskudd ved bokføring** påvirkes for eksempel av hvordan feltet **Hyppighet for automatisk oppdatering av forskudd** er satt til å kontrollere om det finnes ventende forskudd.

Les detaljer om feltene [**Obligatorisk nr. for eksternt dokument**](#external-document-number) og [**Bruk opprinnelig kostpris**](#exact-cost-reversing) senere i artikkelen.

### Innstillinger for nummerserier

På hurtigfanen **Nummerserier** må du angi unike identifikasjonskoder som skal brukes for leverandører, fakturaer og andre kjøpsdokumenter. Nummerering er ikke bare viktig for interne prosesser, men det kan også hende at du må følge lokale forskrifter. Derfor kan det være verdt å vurdere å definere alle serier på siden **Nr. serie** før i stedet for å opprette nye fra **Kjøpsoppsett**. Finn ut mer under [Opprett nummerserier](ui-create-number-series.md).

## Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Nøyaktig kosttilbakeføring

Funksjonen **Bruk opprinnelig kostpris** bidrar til å sikre at returnerte varer verdsettes til samme kostnad som da de opprinnelig ble trukket fra lageret, ved hjelp av en fast utligning i stedet for en lagermetode av typen gjennomsnitt eller bare FIFU (først inn, først ut). Lær mer under delen [Utformingsdetaljer: fast utligning](design-details-item-application.md#fixed-application). Hvis det senere legges til en ekstra kostnad i den opprinnelige bestillingen, oppdaterer programmet verdien på bestillingsreturen.

Med funksjonen aktiver kan en returtransaksjon bare bokføres ved å angi varepostnummeret i feltet **Utligningsvarepost** på bestillingsreturlinjen. Som standard vises ikke feltet på hurtigfanen **Linjer**. Lær hvordan du legger til felter på sider ved å gå til [Tilpass arbeidsområdet](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Flere kjøpsoppsett

| Til | Se |
| --- | --- |
| Opprett et leverandørkort for hver leverandør som du kjøper fra. |[Registrere nye leverandører](purchasing-how-register-new-vendors.md) |
| Prioriter leverandører. |[Prioritere leverandører](purchasing-how-prioritize-vendors.md) |
| Angi bankkontoopplysninger, inkludert IBAN-kode (internasjonalt bankkontonummer) og SWIFT-koder, på leverandørens kort. | [Konfigurer leverandørbankkontoer](purchasing-how-set-up-vendors-bank-accounts.md) |
| Konfigurer innkjøpere, tildel dem leverandører og koder for å spore statistikk. |[Definere innkjøpere](purchasing-how-setup-purchasers.md) |
| Angi de forskjellige rabattene og spesialprisene som leverandør gir deg avhengig av vare, antall eller dato. |[Registrere avtaler om kjøpspris, rabatt og betaling](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definer det du betaler for varene og tjenestene leverandøren har kjøpt.  | [Konfigurer priser og rabatter](across-prices-and-discounts.md) |
| Opprett standardlinjer som skal settes inn på gjentakende kjøpsdokumenter. | [Konfigurer gjentakende kjøpslinjer](purchasing-how-work-recurring-purchase-lines.md) |
| Opprett sekvenser av oppgaver for å koble sammen prosesser som er utført av forskjellige brukere, for eksempel å be om og godkjenne bestillinger. | [Konfigurer arbeidsflyter for kjøpsgodkjenning](across-set-up-workflows.md) |
| Håndter forretningssamhandlinger med leverandører, importer mottatte fakturadokumenter og registrer nye leverandører ved hjelp av e-postklienten i Outlook. | [Konfigurer Business Central-tillegget for Outlook](admin-outlook.md) |
| Gå gjennom utgiftskvitteringer, konverter papir og elektroniske dokumenter til kladdelinjer og digitalisere papirfakturaer fra leverandører. | [Konfigurere inngående dokumenter](across-how-setup-income-documents.md) |
| Angi standardrapporter som skal brukes for ulike dokumenttyper. |[Rapportvalg i Business Central](across-report-selections.md)|
|Angi om brukere kan bokføre kjøpsfakturaer, og om de må bokføre dem sammen med en levering. |[Definer en fakturabokføringspolicy for brukere](admin-setup-invoice-posting-policy.md)|

## Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Oversikt over oppsett](setup.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
