---
title: Tilordne et prioritetsnivå til en leverandør | Microsoft-dokumentasjon
description: Du kan tilordne numre til leverandørene for å prioritere dem og forenkle betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87d2f7c7fe2d395d16b41b288500f22e16bd0ba0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758545"
---
# <a name="prioritize-vendors"></a>Prioritere leverandører
[!INCLUDE[prod_short](includes/prod_short.md)] kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).

Først må du prioritere leverandørene ved å tilordne numre til dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Slik prioriterer du leverandører
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle leverandøren, og velg deretter **Rediger**.
3. Angi et tall i feltet **Prioritet**.

[!INCLUDE[prod_short](includes/prod_short.md)] vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet. Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.

Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt. Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer. Du kan angi et ubegrenset antall prioritetsnivåer.

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]