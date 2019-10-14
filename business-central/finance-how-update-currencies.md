---
title: Oppdatere valutakurser | Microsoft-dokumentasjon
description: Spor beløp i ulike valutaer ved hjelp av valutakoder, og la Business Central hjelpe deg med å justere valutakurser for bokførte poster med en ekstern service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7376abd7806eb664bbfcbf3f3505df00ababba9e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305815"
---
# <a name="update-currency-exchange-rates"></a>Oppdatere valutakurser
Ettersom selskaper har drift i stadig flere land/regioner, blir det også stadig viktigere at de kan handle i og rapportere økonomien i mer enn én valuta. Du må definere en kode for hver valuta du bruker hvis du kjøper eller selger i andre valutaer enn din lokale valuta, har kundekonti eller leverandørkonti i andre valutaer, eller registrerer finanstransaksjoner i forskjellige valutaer.

Finans er definert til å bruke den lokale valutaen (NOK), men du kan definere at den skal bruke en annen valuta med en gjeldende valutakurs. Når du angir en ny valuta som en såkalt tilleggsrapporteringsvaluta, registrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] beløp automatisk i både NOK og denne tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Justere valutakurser
Ettersom valutakursene varierer konstant, må tilleggsvalutaangivelser i systemet justeres jevnlig. Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i NOK i Finans, være villedende. I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt.

Kjørselen **Juster valutakurser** brukes til å justere valutakursene manuelt for bokførte kunde-, leverandør- og bankkontoposter. Den kan også oppdatere tilleggsrapporteringsvalutabeløp i finansposter. Du kan også få valutakursene justert automatisk ved hjelp av en tjeneste. Hvis du vil ha mer informasjon, kan du se [Slik konfigurerer du en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Innvirkning på kunder og leverandører
For kunde- og leverandørkonti justerer kjørselen valutaen ved å bruke valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte valutabalansene og bokfører beløpene til finanskontoen angitt i feltet **Konto for urealisert agio** eller feltet **Konto for urealisert disagio** på siden **Valuta**. Motposteringer bokføres automatisk på samlekontoen i Finans.

Kjørselen behandler aller åpne kundeposter og leverandørposter. Hvis det finnes en valutadifferanse for en post, oppretter kjørselen en ny detaljert kunde- eller leverandørpost som gjenspeiler de justerte beløpene på kunde- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensjoner på kunde- og leverandørposter
Justeringspostene tilordnes dimensjonene fra kunde- eller leverandørpostene, og justeringene bokføres av dimensjonsverdiene.

### <a name="effect-on-bank-accounts"></a>Innvirkning på bankkonti
For bankkonti justerer kjørselen valutaen med valutakursen som gjelder på bokføringsdatoen som er angitt i kjørselen. Kjørselen beregner differansene for de enkelte bankkontiene som har en valutakode, og bokfører beløpene til finanskontoen som er angitt i feltet **Kto. for realisert agio** eller feltet **Konto for realisert disagio** på siden **Valuta**. Motposter bokføres automatisk på finanskontiene som er angitt i bankbokføringsgruppene. Kjørselen beregner én post per valuta, per bokføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensjoner på bankkontoposter
Justeringspostene for bankkontoens finanskonto, og for tap/vinning-kontoen tilordnes bankkontoens standarddimensjon.

### <a name="effect-on-gl-accounts"></a>Innvirkning på finanskonti
Hvis du bokfører i en tilleggsrapporteringsvaluta, kan du få kjørselen til å opprette nye finansposter for valutajusteringer mellom NOK og tilleggsrapporteringsvalutaen. Kjørselen beregner forskjellene for hver finanspost og justerer finansposten i henhold til innholdet i feltet **Valutakursjustering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensjoner på finanskontoposter
Justeringspostene tilordnes standarddimensjonene fra kontiene de bokføres på.

> [!Important]
> Før du kan bruke kjørselen, må du angi justeringskursene som brukes til å justere valutasaldoen. Du gjør dette på siden **Valutakurser**.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Slik konfigurerer du en valutakurstjeneste
Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert, for eksempel FloatRates.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutakurstjenester**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Valutakurstjeneste** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Merk av for **Aktivert** for å aktivere tjenesten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Oppdatere valutakurser via en tjeneste
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutaer**, og velg deretter den relaterte koblingen.
2. Velg **Oppdater valutakurser**.

Verdien i **Valutakurs**-feltet på **Valutaer**-siden oppdateres med den nyeste valutakursen.

## <a name="see-also"></a>Se også
[Definere en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
