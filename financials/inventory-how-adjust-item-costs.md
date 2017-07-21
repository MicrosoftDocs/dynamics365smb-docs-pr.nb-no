---
title: Justere kostnadene for varer manuelt | Microsoft-dokumentasjon
description: "Du kan justere lagerverdien for en vare, for eksempel med lagermetoden FIFO eller Gjennomsnitt, når varekost endres av andre årsaker enn transaksjoner."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Justere varekost manuelt
Kostnaden for en vare (lagerverdien) som du kjøper og senere selger, kan endres i løpet av levetiden, for eksempel fordi en fraktkostnader er lagt til innkjøpskostnaden etter at du har solgt varen. Kostjustering er spesielt relevant i situasjoner der du selger varer før du fakturerer kjøpet av varene. Hvis du alltid vil vite riktig lagerverdi, må varekostnader derfor justeres regelmessig. Dette sikrer at salgs- og fortjenestestatistikk er oppdatert og at økonomiske KPI-er er riktige.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] justeres varekostnader automatisk hver gang det oppstår en lagertransaksjon, for eksempel når du bokfører en kjøpsfaktura for en vare.

Du kan også bruke en funksjon til å justere kostnadene for en eller flere varer manuelt. Dette er nyttig, for eksempel når du vet at varekostnader er endret av andre grunner enn varetransaksjoner.

Varekost justeres med lagermetoden FIFO eller Gjennomsnitt, avhengig av hva du valgte i det assisterte oppsettet **Konfigurere Mitt selskap**. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

Hvis du bruker lagermetoden FIFO, er enhetskosten for en vare den faktiske verdien for alle mottak av varen. Lageret verdisettes basert på antakelsen om at de første varene som plasseres på lager, selges først.

Hvis du bruker lagermetoden Gjennomsnitt, blir enhetskosten for en vare beregnet som den gjennomsnittlige enhetskosten på hvert tidspunkt etter et kjøp. Lageret verdisettes basert på antakelsen om at alle beholdninger selges samtidig.

Funksjonen for kostnadsjustering behandler bare verdiposter som ennå ikke er justert. Hvis funksjonen støter på en situasjon der endrede inngående kost må videresendes til tilknyttede utgående poster, opprettes det nye justeringsoppføringer, som er basert på informasjonen i de opprinnelige verdipostene, men som inneholder justeringsbeløpet. Funksjonen for kostnadsjustering bruker bokføringsdatoen for den opprinnelige verdiposten i justeringsposten hvis denne datoen ikke er i en lukket lagerperiode. I så tilfelle bruker programmet startdatoen for den neste åpne lagerperioden. Hvis lagerperioder ikke brukes, styrer datoen i feltet **Bokf. tillatt fra** i vinduet **Finansoppsett** når justeringsposten bokføres.

Endringer i lagerverdien fra handel er automatisk avstemt med dine økonomiske bøker når du bokfører transaksjoner for varen. Hvis du vil ha mer informasjon, kan du se delen «Lageravstemming» i [Lager](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Justere varekost manuelt
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Juster kostverdi - vareposter**, og velg deretter den relaterte koblingen.
2. I vinduet **Juster kostverdi - vareposter** angir du hvilke varer du vil justere kostnader for.
3. Velg **OK**.

## <a name="see-also"></a>Se også
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

