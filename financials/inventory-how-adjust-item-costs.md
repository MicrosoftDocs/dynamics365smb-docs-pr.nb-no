---
title: Justere varekost manuelt| Microsoft-dokumentasjon
description: Justere varekost
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Justere varekost manuelt
Kostnaden for en vare (lagerverdien) som du kjøper og senere selger, kan endres i løpet av levetiden, for eksempel fordi en fraktkostnader er lagt til innkjøpskostnaden etter at du har solgt varen. Kostjustering er spesielt relevant i situasjoner der du selger varer før du fakturerer kjøpet av varene. Hvis du alltid vil vite riktig lagerverdi, må varekostnader derfor justeres regelmessig. Dette sikrer at salgs- og fortjenestestatistikk er oppdatert og at økonomiske KPI-er er riktige.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] justeres varekostnader automatisk hver gang det oppstår en lagertransaksjon, for eksempel når du bokfører en kjøpsfaktura for en vare.

Du kan også bruke en funksjon til å justere kostnadene for en eller flere varer manuelt. Dette er nyttig, for eksempel når du vet at varekostnader er endret av andre grunner enn varetransaksjoner.

**Merk**: Varekostnader er justert bare av FIFO-lagermetoden. Dette betyr at enhetskosten for en vare er den faktiske verdien for et hvilket som helst mottak av varen, og at lageret er vurdering med antakelsen av at de første elementene som er plassert i lageret, selges først.

Funksjonen for kostnadsjustering behandler bare verdiposter som ennå ikke er justert. Hvis funksjonen støter på en situasjon der endrede inngående kost må videresendes til tilknyttede utgående poster, opprettes det nye justeringsoppføringer, som er basert på informasjonen i de opprinnelige verdipostene, men som inneholder justeringsbeløpet. Funksjonen for kostnadsjustering bruker bokføringsdatoen for den opprinnelige verdiposten i justeringsposten hvis denne datoen ikke er i en lukket lagerperiode. I så tilfelle bruker programmet startdatoen for den neste åpne lagerperioden. Hvis lagerperioder ikke brukes, styrer datoen i feltet **Bokf. tillatt fra** i vinduet **Finansoppsett** når justeringsposten bokføres.

Endringer i lagerverdien fra handel er automatisk avstemt med dine økonomiske bøker når du bokfører transaksjoner for varen. Du finner mer informasjon under [Avansert: Lageravstemming](advanced-inventory-reconciliation.md).

## <a name="to-adjust-item-costs-manually"></a>Justere varekost manuelt
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Juster kostverdi - vareposter**, og deretter velger du den beslektede koblingen.
2. I vinduet **Juster kostverdi - vareposter** angir du hvilke varer du vil justere kostnader for.
3. Velg **OK**-knappen.

## <a name="see-also"></a>Se også
[Avansert: Lageravstemming](advanced-inventory-reconciliation.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

