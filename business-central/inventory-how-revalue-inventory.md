---
title: Opprette nye verdiposter for varer på lageret | Microsoft-dokumentasjon
description: Beskriver hvordan du foretar oppskrivning eller avskrivning av verdiposter for én eller flere varer på lageret, ved å bokføre den gjeldende, beregnede verdien.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c961d15d04da5fcad18a460adc269f3099962f6a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182135"
---
# <a name="revalue-inventory"></a>Revaluere beholdning
Hvis du vil endre lagerverdien for en vare eller en bestemt varepost, må du bruke revalueringskladden.

## <a name="to-revalue-inventory"></a>Slik revaluerer du beholdning
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Revalueringskladd**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn lagerverdi**.
3. På siden **Beregn lagerverdi** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velg **OK**.
5. På hver linje på siden **Revalueringskladd** i feltet **Enhetskost (revaluert)** angir du den nye enhetskosten. Du kan eventuelt angi det nye totalbeløpet i feltet **Lagerverdi (revaluert)**.

    De relevante feltene oppdateres automatisk. Merk deg at feltet **Beløp** viser den faktiske endringen i lagerverdien for den vareposten du har valgt. I dette feltet beregnes differansen mellom feltene **Lagerverdi (beregnet)** og **Lagerverdi (revaluert)**.
6. Når du har fullført alle linjene i revalueringskladden, kan du velge handlingen **Bokfør**.

Nye verdiposter opprettes nå for å gjenspeile revalueringer som du har bokført. Du kan se de nye verdiene på de respektive varekortene.

## <a name="see-also"></a>Se også
[Designdetaljer: Revaluering](design-details-revaluation.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
