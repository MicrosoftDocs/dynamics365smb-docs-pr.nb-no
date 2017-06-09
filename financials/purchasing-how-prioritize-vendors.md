---
title: "Prioritere leverandører| Microsoft-dokumentasjon"
description: "Prioritere leverandører"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae80ae9ecc15838b59999ded775c7fa0063c8a54
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-prioritize-vendors"></a>Prioritere leverandører
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md).

Først må du prioritere leverandørene ved å tilordne numre til dem..

## <a name="to-prioritize-vendors"></a>Slik prioriterer du leverandører
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Leverandører**, og deretter velger du den beslektede koblingen.
2. Velg den aktuelle leverandøren, og velg deretter **Rediger**.
3. Angi et tall i feltet **Prioritet**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet. Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.

Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt. Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer. Du kan angi et ubegrenset antall prioritetsnivåer.

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

