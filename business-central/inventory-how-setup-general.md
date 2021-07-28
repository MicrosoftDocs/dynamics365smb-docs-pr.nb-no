---
title: Definere det generelle lageroppsettet
description: Beskriver hvordan du definerer det generelle lageroppsettet slik at du kan styre lageret og varene.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a99de8575891e15712e221f28bbf3f4a46f2f771
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435625"
---
# <a name="set-up-general-inventory-information"></a>Definere generell informasjon om lagerbeholdning

Du angir det generelle lageroppsettet på siden **Lageroppsett**.

## <a name="to-set-up-general-inventory-information"></a>Slik definerer du generell informasjon om lagerbeholdning

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.
2. På siden **Lageroppsett** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Hvis du vil ha mer informasjon om kostnadsfelt, **Automatisk kostbokføring**, **Bokf. av forventet kost i Finans** og **Standard lagermetode**, se [Avstemme lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md) og [Designdetaljer: Bokføre forventet kost](design-details-expected-cost-posting.md). Hvis du vil ha mer informasjon om kostberegning generelt, se [Administrere lagerkostnader](finance-manage-inventory-costs.md).  

Hvis du vil at inngående lagerhåndteringstid skal tas med i beregningen av ordrebekreftelse på bestillingslinjen, kan du definere den som standard for lageret, på siden **Lageroppsett**, og for lokasjonen. Hvis du vil ha mer informasjon, kan du se [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Alternativet **Automatisk kostjustering** er aktivert som standard for å sikre at lagerverdier alltid er riktige i finans, som i sin tur holder salgs- og fortjenestestatistikk oppdatert. Kostendringer fra inngående poster, for eksempel de for kjøp eller produksjonsavgang, tilordnes til de relaterte utgående postene, for eksempel salg eller overføringer. Dette er nyttig for nye [!INCLUDE[prod_short](includes/prod_short.md)]-kunder og små bedrifter med relativt lave lagertransaksjonsnivåer. Når virksomheten vokser og lagernivåer øker, kan imidlertid dette redusere systemets ytelse. Hvis du vil minimere redusert ytelse under bokføringen, velger du et tidsalternativ for å definere hvor langt tilbake i tid fra arbeidsdatoen en inngående transaksjon kan forekomme for potensielt å utløse justering av relaterte utgående verdiposter. Alternativt kan du justere kostnader manuelt ved jevne mellomrom med kjørselen Juster kostverdi – vareposter.

## <a name="see-also"></a>Se også
[Definere lager](inventory-setup-inventory.md)  
[Designdetaljer: Kostmetoder](design-details-costing-methods.md)    
[Håndtere lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]