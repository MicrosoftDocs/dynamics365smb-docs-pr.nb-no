---
title: "Opprette nye verdiposter for varer på lageret | Microsoft-dokumentasjon"
description: "Beskriver hvordan du foretar oppskrivning eller avskrivning av verdiposter for én eller flere varer på lageret, ved å bokføre den gjeldende, beregnede verdien."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8460dac8478fa101a255d93110578fa9ea20516f
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="revalue-inventory"></a>Revaluere beholdning
Hvis du vil endre lagerverdien for en vare eller en bestemt varepost, må du bruke revalueringskladden.

## <a name="to-revalue-inventory"></a>Slik revaluerer du beholdning
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Revalueringskladd**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn lagerverdi**.
3. I vinduet **Beregn lagerverdi** fyller du ut feltene etter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **OK**.
5. På hver linje i vinduet **Revalueringskladd** i feltet **Enhetskost (revaluert)** angir du den nye enhetskosten. Du kan eventuelt angi det nye totalbeløpet i feltet **Lagerverdi (revaluert)**.

    De relevante feltene oppdateres automatisk. Merk deg at feltet **Beløp** viser den faktiske endringen i lagerverdien for den vareposten du har valgt. I dette feltet beregnes differansen mellom feltene **Lagerverdi (beregnet)** og **Lagerverdi (revaluert)**.
6. Når du har fullført alle linjene i revalueringskladden, kan du velge handlingen **Bokfør**.

Nye verdiposter opprettes nå for å gjenspeile revalueringer som du har bokført. Du kan se de nye verdiene på de respektive varekortene.

## <a name="see-also"></a>Se også
[Designdetaljer: Revaluering](design-details-revaluation.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

