---
title: Registrere og justere ressursforbruk og priser | Microsoft-dokumentasjon
description: "Beskriver hvordan du kan registrere ressursforbruket eller forbruket som er knyttet til et prosjekt, for å holde rede på og håndtere kostnader, priser og arbeidstyper."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f86fed1b300df98ef120e2f91fdd0785670d04f1
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="use-resources-for-jobs"></a>Bruke ressurser for prosjekter
Du registrerer ressursforbruket i prosjektkladden for å holde oversikt over kostnader, priser og arbeidstypene som er knyttet til prosjekter. Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).

Du kan også bokføre ressursforbruket i en ressurskladd. Poster som er bokført i en ressurskladd, har ingen innvirkning på Finans.

## <a name="to-assign-resources-to-jobs"></a>Slik tilordner du ressurser til prosjekter
Du kan tilordne ressurser til prosjekter ved å opprette prosjektplanleggingslinjer for prosjektet. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Slik registrerer du ressursforbruk for et prosjekt
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.
2. Åpne en relevant prosjektkladd, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Når kladden er fullført, kan du velge handlingen **Bokfør**.

## <a name="to-adjust-resource-prices"></a>Slik justerer du ressurspriser
Hvis du vil endre kost- eller salgspriser for en rekke ressurser, kan du bruke en kjørsel.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Juster ressurskost/priser**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på en linje etter behov, og klikk deretter **OK**.

> [!NOTE]  
>   Denne kjørselen verken oppretter eller justerer alternative kostnader eller priser for ressurser. Den endrer bare innholdet i feltet på ressurskortet for **Juster felt**-feltet som du valgte i kjørselen. Justeringen vil tre i kraft umiddelbart for ressurser, så kontroller justeringsfaktorene før du kjører den satsvise jobben.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av eksisterende alternative priser
Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Foreslå ress.prisendr. (pris)** og fyll deretter ut feltene etter behov.
3. Velg **OK**.  
4. Når kjørselen er ferdig, viser vinduet **Ressursprisendringer** resultatene av kjørselen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av standardpriser
Hvis du vil definere flere alternative ressurspriser på bakgrunn av standardprisene på ressurskortene, kan du bruke en kjørsel.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ressursprisendringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Foreslå ress.prisendr. (ress.)** og fyll deretter ut feltene etter behov.  
3. Velg **OK**.  
4. Når kjørselen er ferdig, åpner du vinduet **Ressursprisendringer** for å se resultatene av kjørselen.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av alternative priser
Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Foreslå ress.prisendr. (pris)**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.
3. Velg **OK**.  
4. Når kjørselen er ferdig, åpner du vinduet **Ressursprisendringer** for å se resultatene av kjørselen.

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

