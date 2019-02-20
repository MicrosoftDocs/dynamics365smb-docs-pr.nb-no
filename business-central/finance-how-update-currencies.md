---
title: Oppdatere valutakurser | Microsoft-dokumentasjon
description: Hvis du vil bruke flere valutaer i virksomheten, kan du definere en kode for hver valuta og bruke en ekstern valutakurstjeneste.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: nb-no
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a>Oppdatere valutakurser
Ettersom selskaper har drift i stadig flere land/regioner, blir det også stadig viktigere at de kan handle i og rapportere økonomien i mer enn én valuta. Du må definere en kode for hver valuta du bruker hvis du kjøper eller selger i andre valutaer enn din lokale valuta, har kundekonti eller leverandørkonti i andre valutaer, eller registrerer finanstransaksjoner i forskjellige valutaer.

Finans er definert til å bruke den lokale valutaen (NOK), men du kan definere at den skal bruke en annen valuta med en gjeldende valutakurs. Når du angir en ny valuta som en såkalt tilleggsrapporteringsvaluta, registrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] beløp automatisk i både NOK og denne tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster. Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Justere valutakurser
Ettersom valutakursene varierer konstant, må tilleggsvalutaangivelser i systemet justeres jevnlig. Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i NOK i Finans, være villedende. I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt. Kjørselen Juster valutakurser brukes til å justere valutakursene for bokførte kunde-, leverandør- og bankkontoposter. Den kan også oppdatere tilleggsrapporteringsvalutabeløp i finansposter.

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

