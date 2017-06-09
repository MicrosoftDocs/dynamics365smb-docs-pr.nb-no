---
title: Bruke ressurser for prosjekter| Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker timelister til å administrere prosjekter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34d8b133a11324e1821780e3988158bb0989349b
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-resources-for-jobs"></a>Bruke ressurser for prosjekter
Du registrerer ressursforbruket i prosjektkladden for å holde oversikt over kostnader, priser og arbeidstypene som er knyttet til prosjekter. Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).

Du kan også bokføre ressursforbruket i en ressurskladd. Poster som er bokført i en ressurskladd, har ingen innvirkning på Finans.

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).

## <a name="to-assign-resources-to-jobs"></a>Slik tilordner du ressurser til prosjekter
Du kan tilordne ressurser til prosjekter ved å opprette prosjektplanleggingslinjer for prosjektet. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Slik registrerer du ressursforbruk for et prosjekt
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Prosjektkladder**, og deretter velger du den beslektede koblingen.
2. Åpne en relevant prosjektkladd, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Når kladden er fullført, kan du velge handlingen **Bokfør**.

## <a name="to-adjust-resource-prices"></a>Slik justerer du ressurspriser
Hvis du vil endre kost- eller salgspriser for en rekke ressurser, kan du bruke en kjørsel.  

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Juster ressurskost/priser**, og deretter velger du den beslektede koblingen.
2. Fyll ut feltene på en linje etter behov, og klikk deretter **OK**.

**Merk**: Denne kjørselen verken oppretter eller endrer alternative kostnader eller priser for ressurser. Den endrer bare innholdet i feltet på ressurskortet for **Juster felt**-feltet som du valgte i kjørselen. Justeringen vil tre i kraft umiddelbart for ressurser, så kontroller justeringsfaktorene før du kjører den satsvise jobben.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av eksisterende alternative priser
Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Ressursprisendringer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Foreslå ress.prisendr. (pris)** og fyll deretter ut feltene etter behov.
3. Velg **OK**-knappen.  
4. Når kjørselen er ferdig, viser vinduet **Ressursprisendringer** resultatene av kjørselen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av standardpriser
Hvis du vil definere flere alternative ressurspriser på bakgrunn av standardprisene på ressurskortene, kan du bruke en kjørsel.  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Ressursprisendringer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Foreslå ress.prisendr. (ress.)** og fyll deretter ut feltene etter behov.  
3. Velg **OK**-knappen.  
4. Når kjørselen er ferdig, åpner du vinduet **Ressursprisendringer** for å se resultatene av kjørselen.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Slik får du forslag til ressursprisendringer på bakgrunn av alternative priser
Hvis du allerede har definert alternative ressurspriser for noen ressurser, kan du bruke en kjørsel til å definere flere alternative ressurspriser.

1. Skriv inn **Foreslå ress.prisendr. (pris)** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.
3. Velg **OK**-knappen.  
4. Når kjørselen er ferdig, åpner du vinduet **Ressursprisendringer** for å se resultatene av kjørselen.

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

