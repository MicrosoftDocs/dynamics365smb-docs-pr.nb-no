---
title: 'Utformingsdetljaer – Flyter for produksjon, montering og prosjekter'
description: 'Finn ut om flytene mellom hyller for plukking av komponenter og plassering av sluttvarer for montering, produksjon eller jobbordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 02/05/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a>Flyter for produksjon, montering og prosjekter

Interne flyter, for eksempel plukkking av komponenter og plassering av sluttvarer for monterings-, jobb-og produksjonsordrer, ligner på inngående eller utgående flyter. Mange av prosessene kan se kjente ut. Denne artikkelen inneholder informasjon om hvordan du arbeider med interne lagerflyter med ulike typer kompleksitet.

## <a name="overview-of-different-configuration-options"></a>Oversikt over ulike konfigurasjonsalternativer

Du kan konfigurere lagerfunksjoner på ulike måter. Det er viktig at alternativene du velger, forbedrer prosessene uten å forårsake indirekte kostnader. Følgende tabeller beskriver typiske konfigurasjoner for håndtering av fysiske varer for produksjon, jobber og monteringsordrer.

### <a name="inbound-flow-put-away"></a>Inngående flyt (plassering)

|Kompleksitetsnivå|Beskrivelse|Innstillinger|Hyllekode|Inngående flyt av produksjonsordre|Inngående flyt av monteringsordre|Inngående flyt av jobber|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikert lageraktivitet.|Bokfør fra ordrer og kladder.||Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonskladd -> Ferdigmeldingskladd</br><br/> **Obs**: Du kan bokføre avgang ved hjelp av **Produksjonskladd**.|Monteringsordre|Plassering er ikke tilgjengelig for jobber|  
|Grunnleggende|Ordre for ordre.|Plukk nødv. </br><br/> **Obs**: Selv om innstillingen kalles **Plassering nødv.**, kan du fremdeles bokføre avgang fra kildedokumenter på lokasjoner der du velger denne avmerkingsboksen. |Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordre-> Lagerplassering|Monteringsordre|Plassering er ikke tilgjengelig for jobber|
|Avansert|Konsoliderte plasseringsaktiviteter for flere kildedokumenter.|Mottak nødv. + Plukk nødv.|Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordrer -> Ferdigmeldingskladd|Monteringsordrer-> interne flyttinger | Plassering er ikke tilgjengelig for jobber|
|Avansert|Samme som over + lagerstyringsaktiviteter|Lagerstyring (avhengig av vekslebrytere blir aktivert automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Plassering er ikke tilgjengelig for jobber|

Enkelte konfigurasjoner tillater ikke at du bruker egne lagerdokumenter til å registrere plasseringer. Hvis lokasjonen bruker hyller, kan du imidlertid bruke generelle flyttedokumenter til å flytte produserte eller monterte varer til lager. Finn ut mer under [Flytt varer internt i grunnleggende lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Utgående flyt (plukk)

|Kompleksitetsnivå|Beskrivelse|Innstillinger|Hyllekode|Utgående flyt av produksjonsordre|Utgående flyt av monteringsordre|Utgående flyt av jobber|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikert lageraktivitet.|Bokfør fra ordrer og kladder.||Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonskladd -> Forbrukskladd </br><br/> **Obs**: Du kan bokføre forbruk ved hjelp av **Produksjonskladd**.|Monteringsordre|Jobb -> Prosjektkladd|  
|Grunnleggende|Ordre for ordre.|Plukk nødv. </br><br/> **Obs**: Selv om innstillingen kalles **Plukk nødv.**, kan du fremdeles bokføre avgang fra kildedokumenter på lokasjoner der du velger denne avmerkingsboksen. <!-- ToDo Test prod output-->|Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Produksjonsordre-> Lagerplukk|Monteringsordre-> lagerflytting</br><br/>**Lagerflyttingen** kan bare brukes med hyller.|Jobb -> Lagerplukk|
|Avansert|Konsoliderte plukkaktiviteter for flere kildedokumenter.|Forsendelse nødv. + Plukk nødv.|Valgfritt. Kontrollert av vekslebryteren Hyllekode er obligatorisk|Produksjonsordrer-> Lagerplukk-> Forbrukskladd |Monteringsordrer-> Lagerplukk| Jobber -> Lagerplukk -> Jobbkladd |
|Avansert|Samme som over + lagerstyringsaktiviteter|Lagerstyring (avhengig av vekslebrytere blir aktivert automatisk)|Obligatorisk|Samme som ovenfor|Samme som ovenfor| Lagerstyring støttes ikke for jobber|

I likhet med inngående flyt tillater ikke enkelte konfigurasjoner at du bruker egne lagerdokumenter til å registrere plasseringer. Hvis lokasjonen bruker hyller, kan du bruke generelle flyttedokumenter til å flytte produserte eller monterte varer. Finn ut mer under [Flytt varer](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Lagre uten fast lageraktivitet

Selv om du ikke har egne lageraktiviteter, vil du sikkert likevel holde oversikt over ting som forbruk og produksjonsavgang. Følgende artikler inneholder informasjon om hvordan du behandler mottak for kildedokumenter.

* [Registrere forbruk og avgang for én frigitt produksjonsordrelinje](production-how-to-register-consumption-and-output.md)
* [Montere elementer](assembly-how-to-assemble-items.md)
* [Registrer forbruk eller forbruk for prosjekter](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Enkelt lageroppsett

De inngående og utgående flytene i et enkelt lageroppsett omfatter følgende innstillinger på siden **Lokasjonskort** for lokasjonen:

* For inngående flyt (plassering) aktiverer du alternativet **Plassering nødv.**, men deaktiverer alternativet **Mottak nødv.**.
* For utgående flyt (plukk) aktiverer du alternativet **Plukk nødv.**, men deaktiverer alternativet **Forsendelse nødv.**.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flyter til og fra produksjon i et enkelt lageroppsett

Bruk **lagerplukkdokumenter** til å plukke produksjonskomponenter i flyten til produksjon. Hvis du vil plassere produktene du produserer, bruker **lagerplasseringsdokumenter**.

For lokasjoner som bruker hyller, er lagerflyttingsdokumenter spesielt nyttige for komponenttrekking. Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du gå til [Trekke produksjonskomponenter i lageret](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerflyttinger er viktige dokumenter hvis du bruker trekkmetodene **Plukk + fremover** eller **Plukk + bakover**. Finn ut mer under [Trekkmetoder](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjon eller produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.
* Behandle flyttingen av produserte varer på siden **Intern flytting** uten tilknytning til en produksjonsordre.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flyter til og fra montering i et enkelt lageroppsett

Bokfør utdata og forbruk for montering direkte fra en monteringsordre.

> [!NOTE]
> **Lagerplukk-** og **lagerplasseringsdokumenter** støttes ikke for monteringsordrer.

For lokasjoner som bruker hyller:

* Bruk **lagerflyttingsdokumenter** til å flytte monteringskomponenter til monteringsområdet.
* Feltene **Til-Hyllekode for montering**, **Fra-Hyllekode for montering** på lokasjonskortet definerer standardflyter til og fra monteringsområder.
* Behandle flyttingen av monterte varer på siden **Intern flytting** uten tilknytning til en monteringsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-flyter. Finn ut mer under [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). I forbindelse med lagerstyring er monter-til-lager en del av den interne lagerflyten, og monter-til-ordre er i den utgående lagerflyten. Finn ut mer under [Håndter montere-til-ordre-varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flyter for prosjektstyring i et enkelt lageroppsett

Bruk **lagerplukkdokumenter** til å plukke jobbkomponenter i flyten til prosjektstyring.

For en lokasjon som bruker hyller definerer **Til-prosjekthyllekode**-feltet på lokasjonen standardflytene til prosjektstyring.

## <a name="advanced-warehouse-configurations"></a>Avanserte lageroppsett

De inngående og utgående flytene i et avansert lageroppsett omfatter følgende innstillinger på siden **Lokasjonskort** for lokasjonen:

* For inngående flyt (plassering) aktiverer du alternativene **Mottak nødv.** og **Plassering nødv.**.
* For utgående flyt (plukk) aktiverer du alternativene **Forsendelse nødv.** og **Mottak nødv.**.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flyter til og fra produksjon i avanserte lageroppsett

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter for produksjon.

For lokasjoner som bruker hyller:

* **Lagerflyttingsdokumenter** og siden **Flytteforslag** er spesielt nyttig for komponenttrekk. Finn ut mer under [Trekke produksjonskomponenter i lageret](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjon eller produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder. 
* Behandle flyttingen av produserte varer på sidene **Flytteforslag** eller **Intern plassering** uten tilknytning til en produksjonsordre.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flyter til og fra montering i avanserte lageroppsett

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter for montering.

For lokasjoner som bruker hyller:

* Feltene **Til-Hyllekode for montering** og **Fra-Hyllekode for montering** på lokasjon definerer standardflyter til og fra monteringsområder.
* Behandle flyttingen av monteringsvarer på sidene **Flytteforslag** eller **Intern plassering** uten tilknytning til en monteringsordre.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-flyter. Finn ut mer under [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Monter-til-lager en del av den interne lagerflyten, og monter-til-ordre er i den utgående lagerflyten. Finn ut mer under [Håndtere montere-til-ordre-varer i lagerleveringer](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flyter til prosjektstyring i avanserte lageroppsett

Bruk **lagerplukkdokumentene** og siden **Plukkforslag** til å plukke komponenter i flyten til prosjektstyring.

For lokasjoner som bruker hyller definerer **Til-prosjekthyllekode**-feltet på lokasjonen standardflytene til prosjektområdet.

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
