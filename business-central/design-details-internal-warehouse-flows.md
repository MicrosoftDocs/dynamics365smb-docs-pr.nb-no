---
title: 'Designdetaljer – flyter for produksjon, montering og prosjekter'
description: 'Finn ut om flytene mellom hyller for plukking av komponenter og plassering av sluttvarer for montering, produksjon eller prosjektordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# Flyter for produksjon, montering og prosjekter

Interne flyter, for eksempel plukking av komponenter og plassering av sluttvarer for monterings-, prosjekt- og produksjonsordrer, ligner på inngående eller utgående flyter. Mange av prosessene kan virke kjente. Denne artikkelen inneholder informasjon om hvordan du arbeider med interne lagerflyter med ulike typer kompleksitet.

## Oversikt over ulike konfigurasjonsalternativer

Du kan konfigurere lagerfunksjoner på ulike måter. Det er viktig at alternativene du velger, forbedrer prosessene uten å forårsake indirekte kostnader. Følgende tabeller beskriver typiske konfigurasjoner for håndtering av fysiske varer for produksjon, prosjekter og monteringsordrer.

### Inngående flyt (plassering)

|Kompleksitetsnivå|Beskrivelse|Innstillinger|Hyllekode|Inngående flyt av produksjonsordre|Inngående flyt av monteringsordre|Inngående flyt for prosjekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikert lageraktivitet.|Bokfør fra ordrer og kladder.||Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonskladd -> Ferdigmeldingskladd</br><br/> **Obs**: Du kan bokføre avgang ved hjelp av **Produksjonskladd**.|Monteringsordre|Plassering gjelder ikke for prosjekter|  
|Grunnleggende|Ordre for ordre.|Produksjonsutgang Lagerhåndtering: Lagerplassering. </br><br/> **MERK:** Du kan fortsatt bokføre utdata direkte fra kildedokumentene på steder der du aktiverte disse innstillingene. |Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordre-> Lagerplassering|Monteringsordre|Plassering gjelder ikke for prosjekter|
|Avansert|Konsoliderte plasseringsaktiviteter for flere kildedokumenter.|Ingen dedikerte innstillinger|Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordrer -> Ferdigmeldingskladd|Monteringsordrer-> interne flyttinger | Plassering gjelder ikke for prosjekter|
|Avansert|Samme som ovenfor pluss rettet plukke / put-away aktiviteter|Lagerstyring (avhengig av vekslebrytere aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Plassering gjelder ikke for prosjekter|

Noen konfigurasjoner lar deg ikke bruke dedikerte lagerdokumenter til å registrere plasseringer. Hvis lokasjonen bruker hyller, kan du imidlertid bruke generelle flyttedokumenter til å flytte produserte eller monterte varer til lager. Finn ut mer under [Flytt varer](warehouse-move-items.md).

### Utgående flyt (plukk)

|Kompleksitetsnivå|Description|Innstillinger|Hyllekode|Utgående flyt av produksjonsordre|Utgående flyt av monteringsordre|Utgående flyt for prosjekter|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikert lageraktivitet.|Bokfør fra ordrer og kladder.||Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonskladd -> Forbrukskladd </br><br/> **Obs**: Du kan bokføre forbruk ved hjelp av **Produksjonskladd**.|Monteringsordre|Prosjekt -> Prosjektkladder|  
|Grunnleggende|Ordre for ordre.|Produksjon, Montering, Prosjekter: Lagerplukk, Lagerflytting </br><br/> **MERK:** Du kan fortsatt bokføre forbruk direkte fra kildedokumentene på steder der du aktiverte disse innstillingene.|Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordre-> Lagerplukk|Monteringsordre-> lagerflytting</br><br/>**Lagerflyttingen** kan bare brukes med hyller.|Prosjekt -> Lagerplukk|
|Avansert|Konsoliderte plukkaktiviteter for flere kildedokumenter.|Produksjon, Montering, Prosjekter: Plukk|Valgfritt. Kontrollert av vekslebryteren Hyllekode er obligatorisk|Produksjonsordrer-> Lagerplukk-> Forbrukskladd |Monteringsordrer-> Lagerplukk| Prosjekt(er) -> Lagerplukk -> Prosjektkladd |
|Avansert|Samme som over + lagerstyringsaktiviteter|Lagerstyring (avhengig av vekslebrytere aktiveres automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Direkte plukking og plassering støttes ikke for prosjekter|

## Lagre uten fast lageraktivitet

Selv om du ikke bruker dedikerte lageraktiviteter, vil du kanskje spore ting som forbruk og produksjonsavgang. Følgende artikler inneholder informasjon om hvordan du behandler mottak for kildedokumenter.

* [Registrere forbruk og avgang for én frigitt produksjonsordrelinje](production-how-to-register-consumption-and-output.md)
* [Monter varer](assembly-how-to-assemble-items.md)
* [Registrere forbruk eller bruk for prosjekter](projects-how-record-job-usage.md)

## Enkelt lageroppsett

### Flyter til og fra produksjon i et enkelt lageroppsett  

De inngående og utgående flytene i et enkelt lageroppsett omfatter følgende innstillinger på siden **Lokasjonskort** for lokasjonen:

* For den inngående flyten (plasseringen), i Prod **. Output Whse. Håndtering-feltet**, Velg **Lagerplassering**.
* For den utgående flyten (plukking), i Prod.forbruk **Whse. Håndteringsfelt**, Velg **Lagerplukk/-flytting**.

Bruk **lagerplukkdokumenter** til å plukke produksjonskomponenter i flyten til produksjon. Hvis du vil plassere produktene du produserer, bruker **lagerplasseringsdokumenter**.

For lokasjoner som bruker hyller, er lagerflyttingsdokumenter spesielt nyttige for komponenttrekking. Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du gå til [Trekke produksjonskomponenter i lageret](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerflyttinger er viktige dokumenter hvis du bruker trekkmetodene **Plukk + fremover** eller **Plukk + bakover**. Finn ut mer under [Trekkmetoder](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjon eller produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.
* Behandle flyttingen av produserte varer på siden **Intern flytting** uten tilknytning til en produksjonsordre.

### Flyter til og fra montering i et enkelt lageroppsett  

Den utgående flyten i en grunnleggende lagerkonfigurasjon omfatter følgende innstillinger for lokasjonen **på Lokasjon kort-siden** :

* For den utgående flyten (plukk), i Asm **. Forbruk Whse. Håndtering-feltet**, Velg **Lagerflytting**.

Bruke **dokumenter for lagerflytting** til å plukke monteringskomponenter i flyten til montering. Bokfør utdata og forbruk for montering direkte fra en monteringsordre.

> [!NOTE]
> **Lagerplukk-** og **lagerplasseringsdokumenter** støttes ikke for monteringsordrer.

For lokasjoner som bruker hyller:

* Bruk **lagerflyttingsdokumenter** til å flytte monteringskomponenter til monteringsområdet.
* Feltene **Til-Hyllekode for montering**, **Fra-Hyllekode for montering** på lokasjonskortet definerer standardflyter til og fra monteringsområder.
* Behandle flyttingen av monterte varer på siden **Intern flytting** uten tilknytning til en monteringsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-flyter. Finn ut mer under [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). I forbindelse med lagerstyring er monter-til-lager en del av den interne lagerflyten, og monter-til-ordre er i den utgående lagerflyten. Finn ut mer under [Håndter montere-til-ordre-varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flyter for prosjektstyring i et enkelt lageroppsett

Den utgående flyten i en grunnleggende lagerkonfigurasjon omfatter følgende innstillinger for lokasjonen **på Lokasjon kort-siden** :

* For den utgående flyten (plukk), i Prosjektforbruk **Whse. Håndtering-feltet**, Velg **Lagerplukk**.

Bruk **lagerplukkdokumenter** til å plukke prosjektkomponenter i flyten til prosjektstyring.

For en lokasjon som bruker hyller definerer **Til-prosjekthyllekode**-feltet på lokasjonen standardflytene til prosjektstyring.

## Avanserte lageroppsett  

### Flyter til og fra produksjon i avanserte lageroppsett

Den utgående flyten i en avansert lagerkonfigurasjon omfatter følgende innstillinger på **Lokasjon kort-siden**  for lokasjonen:

* For den utgående flyten (plukking), i Prod.forbruk **Whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk).**

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter for produksjon.

> [!NOTE]
> **Lagerplasseringsdokumenter** støttes ikke for produksjonsavgang.

For lokasjoner som bruker hyller:

* **Lagerflyttingsdokumenter** og siden **Flytteforslag** er spesielt nyttig for komponenttrekk. Finn ut mer under [Trekke produksjonskomponenter i lageret](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjon eller produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder. 
* Behandle flyttingen av produserte varer på sidene **Flytteforslag** eller **Intern plassering** uten tilknytning til en produksjonsordre.

### Flyter til og fra montering i avanserte lageroppsett

Den utgående flyten i en avansert lagerkonfigurasjon omfatter følgende innstillinger på **Lokasjon kort-siden**  for lokasjonen:

* For den utgående flyten (plukk), i Asm **. Forbruk Whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk).** 

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter for montering.

> [!NOTE]
> **Lagerplasseringsdokument** støttes ikke for monteringsordrer.

For lokasjoner som bruker hyller:

* Feltene **Til-Hyllekode for montering** og **Fra-Hyllekode for montering** på lokasjon definerer standardflyter til og fra monteringsområder.
* Behandle flyttingen av monteringsvarer på sidene **Flytteforslag** eller **Intern plassering** uten tilknytning til en monteringsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-flyter. Finn ut mer under [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Monter-til-lager en del av den interne lagerflyten, og monter-til-ordre er i den utgående lagerflyten. Finn ut mer under [Håndtere montere-til-ordre-varer i lagerleveringer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flyter til prosjektstyring i avanserte lageroppsett

Den utgående flyten i en avansert lagerkonfigurasjon omfatter følgende innstillinger på **Lokasjon kort-siden**  for lokasjonen:

* For den utgående flyten (plukk), i Prosjektforbruk **Whse. Håndteringsfelt**, Velg **Lagerplukk (valgfritt)**  eller **Lagerplukk (obligatorisk).**

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter i flyten til prosjektstyring.

For lokasjoner som bruker hyller definerer **Til-prosjekthyllekode**-feltet på lokasjonen standardflytene til prosjektområdet.

## Se også  

[Oversikt over lagerstyring](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
