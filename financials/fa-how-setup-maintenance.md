---
title: Definere vedlikehold av aktiva| Microsoft-dokumentasjon
description: Beskriver hvordan du setter opp systemet for vedlikehold av aktiva.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e97f3cec67fa8b0ef270d406a0efe804da82d99f
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-maintenance"></a>Definere vedlikehold av aktiva
For å styre vedlikehold av aktiva, må du først definere noen generelle vedlikeholdsopplysninger, en bokføringskonto for vedlikeholdskostnader og vedlikeholdskoder for typer arbeid, for eksempel rutineservice eller reparasjon.

## <a name="to-set-up-general-maintenance-information"></a>Slik definerer du generelle vedlikeholdsopplysninger:
Hvis du definerer vedlikeholdsfeltene, kan du bokføre vedlikeholdsutgifter fra aktivakladden.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktiva**, og deretter velger du den beslektede koblingen.
2. Velg aktivaet du vil definere forsikringsdekning for, og velg deretter handlingen **Rediger**.
3. Fyll ut feltene på hurtigfanen **Vedlikehold** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Slik definerer du vedlikeholdskoder
Når du bokfører vedlikeholdskostnader fra en finanskladd, fyller du ut feltet **Vedlikeholdskode** for å registrere hva slags vedlikehold som er utført, for eksempel rutineservice eller reparasjon.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Vedlikehold**, og deretter velger du den beslektede koblingen.
2. I **Vedlikehold**-vinduet definerer du koder for ulike typer vedlikeholdsarbeid.

## <a name="to-set-up-maintenance-expense-accounts"></a>Slik definerer du utgiftskonti for vedlikehold
Du må først angi et kontonummer i vinduet **Bokf.grupper - aktiva** for å kunne bokføre vedlikeholdskostnader.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokf.grupper - aktiva**, og deretter velger du den beslektede koblingen.
2. Fyll ut feltet **Konto for vedlikeholdsutgifter** for hver enkelt bokføringsgruppe.

**Merk:** Hvis du vil definere at vedlikeholdskostnader fordeles til avdelinger eller prosjekter, må du definere en fordelingsnøkkel. Se [Definere generelle aktivafunksjoner](fa-how-setup-general.md) for mer informasjon.

## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Anleggsmidler](fa-manage.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

