---
title: Tilordne et prioritetsnivå til en leverandør (inneholder video)
description: Du kan tilordne numre til leverandørene for å prioritere dem og forenkle betalingsforslag i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.search.form: 26, 27
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 41977fdf7d90082094e3cc9ff025a56b878a6b2c
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131226"
---
# <a name="prioritize-vendors"></a>Prioritere leverandører
[!INCLUDE[prod_short](includes/prod_short.md)] kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).

Først må du prioritere leverandørene ved å tilordne numre til dem.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Slik prioriterer du leverandører
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Velg den aktuelle leverandøren, og velg deretter **Rediger**.
3. Angi et tall i feltet **Prioritet**.

[!INCLUDE[prod_short](includes/prod_short.md)] vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet. Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.

Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt. Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer. Du kan angi et ubegrenset antall prioritetsnivåer.

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]