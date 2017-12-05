---
title: Angi datointervaller i Dynamics 365 Business edition | Microsoft-dokumentasjon
description: "Finn ut hvordan du får en rapport til å vise data fra bestemte tidsperioder ved å bruke datointervaller i Dynamics 365 Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fee6a5d7ce6603829ed98913b7e370a53239ee3e
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="entering-date-ranges-in-dynamics-365-business-edition"></a>Angi datointervaller i Dynamics 365 Business edition 
Du kan angi filtre som inneholder en startdato og en sluttdato, for å vise bare dataene innenfor dette datointervallet eller tidsintervallet. Særlige regler gjelder for angivelse av datointervaller. La oss ta **Kunde - ti på topp** som eksempel:

![Angi et datointervall på forespørselssiden for Kunde - ti på topp-listen](./media/ui-enter-date-ranges/customer-top10-list.png)

Her kan du begrense rapporten til et datointervall, for eksempel de to siste ukene eller totalt seks uker, eller et hvilket som helst intervall du vil bruke. Du angir datointervaller ved å angi datoene og deretter bruke **..** eller **|** til å angi intervallet. Hvis du vil vise de ti beste kundene for de to første ukene i mai i eksemplet vårt, setter du datofilteret til *05 01 17..05 14 17*.
Her er noen andre eksempler:

| Betyr | Eksempel | Tar med poster |
|---|---|---|
|Lik| 12 15 16 |Bare de som er bokført 15. desember 2016.|
|Intervall| 12 15 16..01 15 17<br /><br />..12 15 16|De som er bokført på datoer mellom og inkludert 15. desember 2016 og 15. januar 2017.<br /><br />De som er bokført 15. desember 2016 eller tidligere.|
|Enten/eller|12 15 16&#124;12 16 16|De som er bokført 15. eller 16. desember 2016. Hvis det er bokført poster begge dagene, vises alle postene.|

Grunnformene kan også kombineres innbyrdes.

| Eksempel | Tar med poster |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Poster som enten er bokført 15. desember 2016 eller på datoer mellom og inkludert 1. desember 2016 og 31. mai 2017. |
|..12 14 16&#124;12 30 16.. | Poster som er bokført 14. desember eller tidligere, eller poster som er bokført 30. desember eller senere, det vil si alle poster unntatt de som er bokført på datoer mellom og inkludert 15. og 29. desember. |

Vær oppmerksom på at vi har brukt det amerikanske datoformatet MMDDÅÅ her. Etter hvert som [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tilgjengelig på andre markeder, kan du bruke formatene du er vant med.

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Angi vilkår i filtre](ui-enter-criteria-filters.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

